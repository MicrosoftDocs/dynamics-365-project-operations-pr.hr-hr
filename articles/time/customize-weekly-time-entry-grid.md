---
title: Produljenje unosa vremena
description: U ovom se članku pružaju informacije o načinu na koji razvojni inženjeri mogu produljiti kontrolu unosa vremena.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914761"
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
Svaki unos vremena povezan sa zapisom izvora vremena. Taj zapis određuje koje aplikacije trebaju obraditi unos vremena i na koji način.

Unosi vremena uvijek su jedan neprekinuti vremenski blok povezanog početka, kraja i trajanja.

Logika će automatski ažurirati zapis unosa vremena u sljedećim situacijama:

- Ako su navedena dva od tri sljedeća polja, treće se izračunava automatski: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Polja **msdyn_start** i **msdyn_end** imaju svijest o vremenskim zonama.
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

1. Dodajte prilagođeno polje u dijaloški okvir **Brza izrada**.
2. Konfigurirajte rešetku kako bi se prikazivalo prilagođeno polje.
3. Dodajte prilagođeno polje na stranicu **Uređivanje retka** ili **Uređivanje unosa vremena** prema potrebi.

Provjerite ima li novo polje potrebne provjere valjanosti na stranici **Uređivanje retka** ili **Uređivanje unosa vremena**. U ovom zadatku zaključajte polje koje se temelji na statusu unosa vremena.

Kada dodate prilagođeno polje u rešetku **Unos vremena**, a zatim izradite unose vremena izravno u rešetki, prilagođeno polje za te unose automatski se postavlja tako da odgovara retku. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Dodavanje prilagođenog polja u dijaloški okvir Brza izrada
Dodajte prilagođeno polje u dijaloški okvir **Brza izrada: izrada unosa vremena**. Korisnici tada, tijekom dodavanja unosa vremena, mogu unijeti vrijednost odabirom mogućnosti **Novi**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfiguriranje rešetke kako bi se prikazivalo prilagođeno polje
Postoje dva načina dodavanja prilagođenog polja u rešetku **Tjedni unos vremena**.

- Prilagodite prikaz **Moji tjedni unosi vremena** i dodajte mu prilagođeno polje. Možete odrediti položaj i veličinu prilagođenog polja u rešetki uređivanjem svojstava u prikazu.
- Izradite novi prilagođeni prikaz unosa vremena i postavite ga kao zadani prikaz. Ovaj prikaz mora sadržavati polja **Opis** i **Vanjski komentari**, kao i stupce za koje želite da se nalaze u rešetki. Možete odrediti položaj, veličinu i zadani redoslijed sortiranja u rešetki uređivanjem svojstava u prikazu. Zatim konfigurirajte prilagođenu kontrolu za ovaj prikaz tako da je podesite kao kontrolu **Rešetka unosa vremena**. Dodajte ovu kontrolu u prikaz i odaberite ga za **Web**, **Telefon** i **Tablet**. Zatim konfigurirajte parametre za rešetku **Tjedni unos vremena**. Postavite polje **Datum početka** na **msdyn\_date**, polje **Duration** na **msdyn\_duration**, a polje **Status** na **msdyn\_entrystatus**. Polje **Popis statusa samo za čitanje** postavljeno je na **192350002 (Odobreno)**, **192350003 (Poslano)** ili **192350004 (Zatražen opoziv)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Dodavanje prilagođenog polja odgovarajućoj stranici uređivanja
Stranice koje se koriste za uređivanje unosa vremena ili retka unosa vremena nalaze se pod **Obrasci**. Gumb **Uredi unos** u rešetki otvara stranicu **Uredi unos**, a gumb **Uredi redak** stranicu **Uredi redak**. Možete urediti ove stranice tako da uključuju prilagođena polja.

Obje mogućnosti uklanjaju neke gotove filtre u entitetima **Projekt** i **Projektni zadatak** tako da će se vidjeti svi prikazi za traženje za entitete. Prikazuju se samo unaprijed pripremljeni relevantni prikazi za traženje.

Morate odrediti odgovarajuću stranicu za prilagođeno polje. Ako ste dodali polje u rešetku, ono bi vjerojatno trebalo ići na stranicu **Uređivanje retka** koja se koristi za polja koja se primjenjuju na cijeli redak vremenskih unosa. Ako prilagođeno polje ima jedinstvenu vrijednost u retku za svaki dan (npr., ako se radi o prilagođenom vremenu za vrijeme završetka), trebalo bi ići na stranicu **Uređivanje unosa vremena**.

Za dodavanje prilagođenog polja stranici, povucite element **Polje** u odgovarajući položaj na stranici, a zatim postavite njegova svojstva.

### <a name="add-new-option-set-values"></a>Dodavanje novih vrijednosti skupa mogućnosti
Da biste dodali vrijednosti skupa mogućnosti gotovom polju, slijedite ove korake.

1. Otvorite stranicu za uređivanje za polje, a zatim u odjeljku **Vrsta** odaberite **Uredi** pokraj skupa mogućnosti.
2. Dodajte novu mogućnost koja ima prilagođenu oznaku i boju. Ako želite dodati novi status unosa vremena, naziv gotovog polja glasi **Status unosa**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Određivanje novog statusa unosa vremena kao unosa samo za čitanje
Kako biste odredili novi status unosa vremena kao unosa samo za čitanje, dodajte novu vrijednost unosa vremena u svojstvo **Popis statusa samo za čitanje**. Pazite na to da dodate broj, a ne oznaku. Dio rešetke unosa vremena koji se može uređivati sada će biti zaključan za retke koji imaju novi status. Za postavljanje različitih svojstava **Popis statusa samo za čitanje** za različite prikaze **Unos vremena**, dodajte rešetku **Unos vremena** u odjeljak **Prilagođene kontrole** prikaza i konfigurirajte parametre prema potrebi.

Zatim dodajte poslovna pravila da biste zaključali sva polja na stranicama **Uređivanje retka** i **Uređivanje unosa vremena**. Poslovnim pravilima za te stranice možete pristupiti tako da za svaku stranicu otvorite uređivač obrasca i zatim odaberete **Poslovna pravila**. Možete dodati novi status uvjetu u postojećim poslovnim pravilima ili možete dodati novo poslovno pravilo za novi status.

### <a name="add-custom-validation-rules"></a>Dodavanje prilagođenih pravila provjere valjanosti
Doživljaju rada s rešetkom **Tjedni unos vremena** možete dodati dvije vrste pravila provjere valjanosti.

- Poslovna pravila na strani klijenta koja rade na stranicama
- Provjere valjanosti dodataka na strani poslužitelja koje se primjenjuju na sva ažuriranja unosa vremena

#### <a name="client-side-business-rules"></a>Poslovna pravila na strani klijenta
Poslovna pravila služe za zaključavanje i otključavanje polja, unos zadanih vrijednosti u polja i određivanje provjera valjanosti koje zahtijevaju informacije samo iz trenutačnog zapisa unosa vremena. Poslovnim pravilima za stranicu možete pristupiti tako da otvorite uređivač obrasca i zatim odaberete **Poslovna pravila**. Zatim možete urediti postojeća poslovna pravila ili dodati novo poslovno pravilo.

#### <a name="server-side-plug-in-validations"></a>Provjere valjanosti dodatka na strani poslužitelja
Provjere valjanosti dodatka trebate upotrebljavati za sve provjere valjanosti koje zahtijevaju više konteksta nego što je dostupno u jednom zapisu unosa vremena. Također biste ih trebali koristiti za sve provjere valjanosti koje želite pokrenuti na ažuriranjima unutar retka na rešetki. Da biste dovršili provjere valjanosti, izradite prilagođeni dodatak u entitetu **Unos vremena**.

### <a name="limits"></a>Limiti
Rešetka **Unos vremena** trenutačno ima ograničenje veličine od 500 redaka. Ako ima više od 500 redaka, višak redaka neće biti prikazan. Ne postoji način za povećanje ovog ograničenja veličine.

### <a name="copying-time-entries"></a>Kopiranje vremenskih unosa
Upotrijebite prikaz **Kopiraj stupce za unos vremena** za definiranje popisa polja za kopiranje tijekom vremenskog unosa. **Datum** i **Trajanje** obvezna su polja i ne biste ih trebali ukloniti iz prikaza.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
