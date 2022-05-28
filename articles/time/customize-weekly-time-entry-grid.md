---
title: Produljenje unosa vremena
description: U ovoj temi nalaze se informacije o načinu na koji razvojni inženjeri mogu proširiti kontrolu unosa vremena.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582977"
---
# <a name="extending-time-entries"></a>Produljenje unosa vremena

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations uključuje proširivu prilagođenu kontrolu unosa vremena. Ta kontrola obuhvaća sljedeće značajke:

- Unos vremena vodoravno tijekom tjedna
- Ukupno po danu, retku ili tjednu
- Kopiranje redaka ili tjedana
- Unos vremena putem HH:mm ili HH.hh (automatski se pretvara u HH.hh)
- Uvoz iz zadataka, rezervacija ili obveza

Produljenja unosa vremena mogući su u dva područja:
- [Dodavanje prilagođenih unosa vremena za vlastitu uporabu](#add)
- [Prilagodba kontrole tjednog unosa vremena](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Dodavanje prilagođenih unosa vremena za vlastitu uporabu

Unosi vremena osnovni su entitet koji se upotrebljava u više scenarija. U valu 1. za ožujak 2020. predstavljeno je osnovno rješenje TESA. TESA osigurava entitet **Postavke** i novu sigurnosnu ulogu **Korisnik vremenskog unosa**. Nova polja **msdyn_start** i **msdyn_end**, koja imaju izravan odnos prema **msdyn_duration**, također su bila uključena. Novi entitet, sigurnosna uloga i polja omogućuju objedinjeniji pristup vremenu diljem više proizvoda.


### <a name="time-source-entity"></a>Entitet izvora vremena
| Polje | Opis | 
|-------|------------|
| Ime  | Naziv unosa izvora vremena upotrebljava se kao vrijednost odabira tijekom stvaranja vremenskih unosa. |
| Zadani izvor vremena [Izvor vremena: jezadan] | Prema zadanim postavkama, samo jedan izvor vremena može biti označen kao zadani. Ova omogućuje da se unosima zadaju vrijednosti za izvor vremena ako nije naveden. |
|Vrsta izvora vremena [Izvor vremena: izvorvremena] | Vrsta izvora je mogućnost (Vrsta izvora unosa vremena) koja omogućuje povezivanje izvora vremena s aplikacijom. Microsoft rezervira vrijednosti veće od 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Vremenski unosi i Entitet izvora vremena
Svaki unos vremena povezan sa zapisom izvora vremena. Ovaj zapis određuje koje bi aplikacije trebale obraditi unos vremena i kako.

Unosi vremena uvijek su jedan neprekinuti vremenski blok povezanog početka, kraja i trajanja.

Logika će automatski ažurirati zapis unosa vremena u sljedećim situacijama:

- Ako su navedena dva od tri sljedeća polja, treće se izračunava automatski: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Polja **msdyn_start** i **msdyn_end** svjesna su vremenske zone.
- Vremenski unosi stvoreni samo s navedenim **msdyn_date** i **msdyn_duration** započeti će u ponoć. Polja **msdyn_start** i **msdyn_end** ažurirat će se u skladu s tim.

#### <a name="time-entry-types"></a>Vrste unosa vremena

Zapisi unosa vremena imaju povezanu vrstu koja definira ponašanje u tijeku slanja za povezanu aplikaciju.

|Natpis | Value|
|-----|-----|
|Na pauzi   |192,355,000|
|Putovanja | 192,355,001|
|Prekovremeni rad   | 192,354,320|
|Posao   | 192,350,000|
|Odsutnost    | 192,350,001|
|Godišnji odmor   | 192,350,002|


## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Prilagodba kontrole tjednog unosa vremena
Razvojni inženjeri mogu dodati dodatna polja i pretraživanja drugim entitetima i implementirati prilagođena poslovna pravila kako bi podržali svoje poslovne scenarije.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Dodavanje prilagođenih polja s pretraživanjima drugim entitetima
Postoje tri glavna koraka za dodavanje prilagođenog polja u rešetku tjednih vremenskih unosa.

1. Dodajte prilagođeno polje u **dijaloški okvir Brzo stvaranje**.
2. Konfigurirajte rešetku kako bi se prikazivalo prilagođeno polje.
3. Prema potrebi dodajte prilagođeno polje na **stranicu Uređivanje** retka ili **Uređivanje** unosa vremena.

Provjerite ima li novo polje potrebne provjere valjanosti na **stranici Uređivanje** retka ili **Uređivanje** unosa vremena. Kao dio ovog zadatka zaključajte polje na temelju statusa unosa vremena.

Kada dodate prilagođeno polje u rešetku **stavke** vremena, a zatim stvorite stavke vremena izravno u rešetki, prilagođeno polje za te stavke automatski se postavlja tako da odgovara retku. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Dodavanje prilagođenog polja u dijaloški okvir Brzo stvaranje
Dodajte prilagođeno polje u **dijaloški okvir Brzo stvaranje: stvaranje unosa vremena**. Korisnici tada, tijekom dodavanja unosa vremena, mogu unijeti vrijednost odabirom mogućnosti **Novi**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfiguriranje rešetke kako bi se prikazivalo prilagođeno polje
Postoje dva načina dodavanja prilagođenog polja u rešetku unosa **vremena** Tjedno.

- Prilagodite **prikaz Stavke** mog tjednog vremena i dodajte mu prilagođeno polje. Položaj i veličinu prilagođenog polja u rešetki možete odrediti uređivanjem svojstava u prikazu.
- Stvorite novi prilagođeni prikaz unosa vremena i postavite ga kao zadani prikaz. Ovaj prikaz trebao bi sadržavati **polja Opis** i **Vanjski komentari uz stupce** koje želite uključiti u rešetku. Uređivanjem svojstava u prikazu možete odrediti položaj, veličinu i zadani redoslijed sortiranja rešetke. Zatim konfigurirajte prilagođenu kontrolu za ovaj prikaz tako da je podesite kao kontrolu **Rešetka unosa vremena**. Dodajte kontrolu u prikaz i odaberite je za **web**, **telefon** i **tablet**. Zatim konfigurirajte parametre za mrežu tjednog unosa **vremena**. **Postavite polje Datum** početka na **msdyn\_ datum**, postavite **polje Trajanje** na **msdyn\_ trajanje** i postavite **polje Status** na **msdyn\_ entrystatus**. Polje Popis statusa **samo za čitanje postavljeno je na** 192350002 (odobreno) **,** 192350003 (poslano) **ili** 192350004 (zatražen opoziv) **.**

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Dodavanje prilagođenog polja na odgovarajuću stranicu za uređivanje
Stranice koje se koriste za uređivanje unosa vremena ili unosa retka vremena mogu se pronaći u odjeljku **Obrasci**. Gumb **Uredi unos** u rešetki otvara stranicu Uređivanje **unosa**, a **gumb Uredi redak** otvara stranicu za uređivanje **retka**. Te stranice možete uređivati tako da sadrže prilagođena polja.

Obje mogućnosti uklanjaju neko zastarjelo filtriranje na **entitetima Project** i **Project Task**, tako da su svi prikazi pretraživanja za entitete vidljivi. Prikazuju se samo unaprijed pripremljeni relevantni prikazi za traženje.

Morate odrediti odgovarajuću stranicu za prilagođeno polje. Najvjerojatnije, ako ste polje dodali u rešetku, ono bi trebalo ići na **stranicu za uređivanje** retka koja se koristi za polja koja se primjenjuju na cijeli redak unosa vremena. Ako prilagođeno polje ima jedinstvenu vrijednost u retku svaki dan (na primjer, ako se radi o prilagođenom polju za vrijeme završetka), trebalo bi se pojaviti **na stranici uređivanje unosa vremena**.

Da biste dodali prilagođeno polje na stranicu, povucite **element Polja** na odgovarajući položaj na stranici, a zatim postavite njegova svojstva.

### <a name="add-new-option-set-values"></a>Dodavanje novih vrijednosti skupa mogućnosti
Da biste u tvorničko polje dodali skup mogućnosti vrijednosti, slijedite ove korake.

1. Otvorite stranicu za uređivanje polja, a zatim u odjeljku **Vrsta** odaberite **Uredi** pokraj skup mogućnosti.
2. Dodajte novu mogućnost koja ima prilagođenu oznaku i boju. Ako želite dodati novi status unosa vremena, polje za van okvira nosi naziv **Status** unosa.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Određivanje novog statusa unosa vremena kao unosa samo za čitanje
Kako biste odredili novi status unosa vremena kao unosa samo za čitanje, dodajte novu vrijednost unosa vremena u svojstvo **Popis statusa samo za čitanje**. Svakako dodajte broj, a ne oznaku. Dio rešetke za unos vremena koji se može uređivati sada će biti zaključan za retke koji imaju novi status. Da biste svojstvo Popisa **stanja samo za čitanje postavili** drugačije za različite **prikaze unosa** vremena, dodajte **rešetku unosa** vremena u sekciju Prilagođene kontrole **prikaza** i konfigurirajte parametre prema potrebi.

Zatim dodajte poslovna pravila da biste zaključali sva polja na stranicama Uređivanje **retka** i **Uređivanje** unosa vremena. Da biste pristupili poslovnim pravilima za te stranice, otvorite uređivač obrazaca za svaku stranicu, a zatim odaberite **Poslovna pravila**. Možete dodati novi status uvjetu u postojećim poslovnim pravilima ili možete dodati novo poslovno pravilo za novi status.

### <a name="add-custom-validation-rules"></a>Dodavanje prilagođenih pravila provjere valjanosti
Možete dodati dvije vrste pravila provjere valjanosti za iskustvo rešetke tjednog unosa **vremena**:

- Poslovna pravila na strani klijenta koja rade na stranicama
- Provjere valjanosti dodatka na strani poslužitelja koje se primjenjuju na ažuriranja unosa tijekom cijelog vremena

#### <a name="client-side-business-rules"></a>Poslovna pravila na strani klijenta
Poslovna pravila služe za zaključavanje i otključavanje polja, unos zadanih vrijednosti u polja i određivanje provjera valjanosti koje zahtijevaju informacije samo iz trenutačnog zapisa unosa vremena. Da biste pristupili poslovnim pravilima za stranicu, otvorite uređivač obrazaca, a zatim odaberite **Poslovna pravila**. Zatim možete urediti postojeća poslovna pravila ili dodati novo poslovno pravilo.

#### <a name="server-side-plug-in-validations"></a>Provjere valjanosti dodatka na strani poslužitelja
Provjere valjanosti dodatka trebali biste koristiti za sve provjere valjanosti koje zahtijevaju više konteksta nego što je dostupno u jednom zapisu o unosu vremena. Trebali biste ih koristiti i za sve provjere valjanosti koje želite pokrenuti na umetnutim ažuriranjima u rešetki. Da biste dovršili provjeru valjanosti, stvorite prilagođeni dodatak za **entitet Unos** vremena.

### <a name="limits"></a>Limiti
Trenutno rešetka unosa **vremena** ima ograničenje veličine od 500 redaka. Ako postoji više od 500 redaka, višak redaka neće biti prikazan. Ne postoji način da se poveća ovo ograničenje veličine.

### <a name="copying-time-entries"></a>Kopiranje vremenskih unosa
Upotrijebite prikaz **Kopiraj stupce za unos vremena** za definiranje popisa polja za kopiranje tijekom vremenskog unosa. **Datum** i **Trajanje** obvezna su polja i ne biste ih trebali ukloniti iz prikaza.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
