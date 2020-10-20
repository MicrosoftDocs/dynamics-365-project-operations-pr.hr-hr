---
title: Produljenje unosa vremena
description: U ovoj temi nalaze se informacije o načinu na koji razvojni inženjeri mogu proširiti kontrolu unosa vremena.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930871"
---
# <a name="extending-time-entries"></a>Produljenje unosa vremena

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Dynamics 365 Project Operations uključuje prilagođenu kontrolu produljenja unosa vremena. Ta kontrola obuhvaća sljedeće značajke:

- Unos vremena vodoravno tijekom tjedna
- Ukupno po danu, retku ili tjednu
- Kopiranje redaka ili tjedana
- Unos vremena putem HH:mm ili HH.hh (automatski se pretvara u HH.hh)
- Uvoz iz zadataka, rezervacija ili obveza

Produljenja unosa vremena mogući su u dva područja:
- [Dodavanje prilagođenih unosa vremena za vlastitu uporabu](#add)
- [Prilagodba kontrole tjednog unosa vremena](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Dodavanje prilagođenih unosa vremena za vlastitu uporabu.

Unosi vremena temeljni su entitet koji je dizajniran za uporabu u više scenarija. U aprilskom valu 1 2020., predstavljeno je osnovno rješenje TESA, koje pruža entitet **Postavke** i novu sigurnosnu ulogu **Korisnik unosa vremena**. Nova polja **msdyn_start** i **msdyn_end** koja imaju izravan odnos prema **msdyn_duration**, također su bila uključena. Novi entitet, sigurnosna uloga i polja omogućuju objedinjeniji pristup vremenu diljem više proizvoda.


### <a name="time-source-entity"></a>Entitet izvora vremena
| Polje | Opis | 
|-------|------------|
| Ime  | Naziv unosa izvora vremena upotrebljava se kao vrijednost odabira tijekom stvaranja unosa vremena. |
| Zadani izvor vremena [Izvor vremena: jezadan] | Prema zadanim postavkama, samo jedan izvor vremena može biti označen kao zadani izvor vremena. Ova mogućnost omogućuje unosima zadane vrijednosti za izvor vremena ako nije naveden. |
|Vrsta izvora vremena [Izvor vremena: izvorvremena] | Vrsta izvora je mogućnost (Vrsta izvora unosa vremena) koja omogućuje povezivanje izvora vremena s aplikacijom. Dodatne vrijednosti će se dodati ovom skup mogućnosti kako se dodaju dodatne aplikacije. Imajte na umu da Microsoft rezervira vrijednosti veće od 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Unosi vremena i Entitet izvora vremena
Svaki unos vremena povezan sa zapisom izvora vremena. Ovaj zapis određuje kako treba obraditi unos vremena i koje aplikacije to trebaju učiniti.

Unosi vremena uvijek su jedan neprekinuti vremenski blok povezanog početka, kraja i trajanja.

Logika će automatski ažurirati zapis unosa vremena u sljedećim situacijama:

- Ako su navedena dva od tri sljedeća polja, treće se izračunava automatski 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Polja **msdyn_start** i **msdyn_end** poznate su vremenske zone.
- Unosi vremena stvoreni samo a navedenim **msdyn_date** i **msdyn_duration** započet će u ponoć, a sukladno tome ažurirat će se **msdyn_start** i **msdyn_end**.

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

- Dodajte prilagođeno polje u dijaloški okvir za brzo stvaranje.
- Konfigurirajte rešetku kako bi se prikazivalo prilagođeno polje.
- Dodajte prilagođeno polje ili u izvođenje zadatka uređivanja retka ili u izvođenje zadatka uređivanja ćelije.

Isto tako, morate provjeriti ima li novo polje ima potrebne provjere valjanosti u izvođenju zadatka uređivanja retka ili ćelije. U ovom koraku morate zaključati polje na temelju statusa unosa vremena.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Dodavanje prilagođenog polja u dijaloški okvir za brzo stvaranje
Potrebno je dodati prilagođeno polje u dijaloški okvir **Brzo stvaranje unosa vremena**. Korisnici tada, tijekom dodavanja unosa vremena, mogu unijeti vrijednost odabirom mogućnosti **Novi**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfiguriranje rešetke kako bi se prikazivalo prilagođeno polje
Postoje dva načina dodavanja prilagođenog polja u rešetku tjednih vremenskih unosa:

  - Prilagodba prikaza i dodavanje prilagođenog polja
  - Stvaranje novog zadanog prilagođenog unosa vremena 


**Prilagodba prikaza i dodavanje prilagođenog polja**

Možete prilagođavati prikaz **Moji tjedni unosi vremena** i dodavati mu prilagođeno polje. Možete odabrati položaj i veličinu prilagođenog polja u rešetki uređivanjem tih svojstava u prikazu.

**Stvaranje novog zadanog prilagođenog unosa vremena** 

Ovaj prikaz mora sadržavati polja **Opis** i **Vanjski komentari**, kao i stupce koje želite dodati u rešetku. 

1. Odaberite položaj, veličinu i zadani redoslijed sortiranja u rešetki uređivanjem tih svojstava u prikazu. 
2. Konfigurirajte prilagođenu kontrolu za ovaj prikaz tako da je podesite kao kontrolu **Rešetka unosa vremena**. 
3. Dodajte ovu kontrolu u prikaz i odaberite ga za web, telefone i tablete. 
4. Konfigurirajte parametre za rešetku tjednih vremenskih unosa. Polje **Datum početka** postavite na **msdyn_date**, polje **Trajanje** na **msdyn_duration**, a polje **Status** na **msdyn_entrystatus**. 
5. Za zadani prikaz polje **Popis statusa samo za čitanje** postavljeno je na **192350002, 192350003, 192350004**, polje **Izvođenje zadatka uređivanja retka** postavljeno je na **msdyn_timeentryrowedit**, a polje **Izvođenje zadatka uređivanja ćelije** postavljeno je na **msdyn_timeentryedit**. 
6. Ta polja možete prilagoditi za dodavanje ili uklanjanje statusa samo za čitanje ili za upotrebu drugog iskustva na temelju zadatka (TBX) za uređivanje retka ili ćelije. Ta polja trebaju biti vezana za statičku vrijednost.


> [!NOTE] 
> Obje mogućnosti uklonit će neke gotove filtre u entitetima **Projekt** i **Projektni zadatak** tako da će se vidjeti svi prikazi za traženje za entitete. Gotova rješenja omogućuju vidljivost samo relevantnih prikaza za traženje.
Morate odrediti odgovarajuće izvođenje zadatka za prilagođeno polje. Ako ste dodali polje u rešetku, ono bi vjerojatno trebalo ići u izvođenje zadatka uređivanja retka koje se koristi za polja koja se primjenjuju na cijeli redak vremenskih unosa. Ako prilagođeno polje ima jedinstvenu vrijednost svaki dan, kao što je prilagođeno polje za **Vrijeme završetka**, ono bi trebalo ići u izvođenje zadatka uređivanja ćelije.

Za dodavanje prilagođenog polja u izvođenje zadatka, povucite element **Polje** u odgovarajući položaj na stranici, a zatim postavite svojstva polja. Postavite svojstvo **Izvor** na **Unos vremena**, a svojstvo **Polje podataka** postavite na prilagođeno polje. Svojstvo **Polje** određuje zaslonski naziv na TBX stranici. Odaberite **Primijeni** kako biste u polje spremili promjene, a zatim odaberite **Ažuriraj** kako biste spremili promjene na stranici.

Da biste umjesto toga koristili novu prilagođenu TBX stranicu, stvorite novi proces. Postavite kategoriju na **Tijek poslovnog procesa**, postavite entitet na **Unos vremena** i postavite vrstu poslovnog procesa pomoću mogućnosti **Pokreni proces kao izvođenje zadatka**. U odjeljku **Svojstva** svojstvo **Naziv stranice** treba biti postavljeno na zaslonski naziv za stranicu. Dodajte sva relevantna polja na TBX stranicu. Spremite i aktivirajte proces, a zatim ažurirajte svojstvo prilagođene kontrole za odgovarajuće izvođenje zadatka na vrijednost **Naziv** u procesu.

### <a name="add-new-option-set-values"></a>Dodavanje novih vrijednosti skupa mogućnosti
Da biste dodali vrijednosti skupa mogućnosti u unaprijed pripremljeno polje, otvorite stranicu za uređivanje za polje, a zatim u odjeljku **Vrsta**odaberite **Uredi** pokraj skupa mogućnosti. Zatim dodajte novu mogućnost koja ima prilagođenu oznaku i boju. Ako želite dodati novi status unosa vremena, unaprijed pripremljeno polje pod nazivom **Status unosa**, a ne **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Određivanje novog statusa unosa vremena kao unosa samo za čitanje
Kako biste odredili novi status unosa vremena kao unosa samo za čitanje, dodajte novu vrijednost unosa vremena u svojstvo **Popis statusa samo za čitanje**. Dio rešetke vremenskih unosa za uređivanje bit će zaključan za retke koji imaju novi status.
Zatim dodajte poslovna pravila da biste zaključali sva polja na TBX stranicama **Uređivanje retka za unos vremena** i **Uređivanje unosa vremena**. Poslovnim pravilima za te stranice možete pristupiti tako da otvorite uređivač izvođenja poslovnog procesa za stranicu, a zatim odaberete **Poslovna pravila**. Možete dodati novi status uvjetu u postojećim poslovnim pravilima ili možete dodati novo poslovno pravilo za novi status.

### <a name="add-custom-validation-rules"></a>Dodavanje prilagođenih pravila provjere valjanosti
Dvije su vrste pravila provjere valjanosti koje možete dodati iskustvu rešetke tjednog unosa vremena:

- Poslovna pravila na strani klijenta koja rade u dijaloškim okvirima za brzo stvaranje i na TBX stranicama.
- Provjere valjanosti dodataka na strani poslužitelja koje se primjenjuju na sva ažuriranja unosa vremena.

#### <a name="business-rules"></a>Poslovna pravila
Poslovna pravila služe za zaključavanje i otključavanje polja, unos zadanih vrijednosti u polja i određivanje provjera valjanosti koje zahtijevaju informacije samo iz trenutačnog zapisa unosa vremena. Poslovnim pravilima za TBX stranice možete pristupiti tako da otvorite uređivač izvođenja poslovnog procesa za stranicu, a zatim odaberete **Poslovna pravila**. Zatim možete urediti postojeća poslovna pravila ili dodati novo poslovno pravilo. Za još više prilagođenih provjera valjanosti možete upotrijebiti poslovno pravilo za pokretanje JavaScripta.

#### <a name="plug-in-validations"></a>Provjere valjanosti dodatka
Provjere valjanosti dodatka trebate upotrebljavati za sve provjere valjanosti koje zahtijevaju više konteksta nego što je dostupno u jednom zapisu unosa vremena ili za provjere valjanosti koje želite pokrenuti na ažuriranjima unutar retka na rešetki. Da biste dovršili provjeru valjanosti, stvorite prilagođeni dodatak u entitetu **Unos vremena**.
