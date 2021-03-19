---
title: Prilagođeni tjedni Unos vremena
description: Ovaj tema pruža informacije o implementaciji prilagođenih poslovnih pravila koja podržavaju praksu tvrtke ili ustanove.
author: stsporen
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f1c8e150500334e87b25a1c8d04cf28c7b7beaeb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282054"
---
# <a name="customize-weekly-time-entry"></a>Prilagođeni tjedni unos vremena 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

U verziji 3.3 aplikacije Microsoft Dynamics 365 Project Service Automation, Microsoft je uveo modernu rešetku koja resursima projekta omogućuje brzi Unos vremena do jednog tjedna odjednom. Nova rešetka tjednih vremenskih unosa može prikazivati ukupne vrijednosti za unose po datumu, retku ili tjednu. Resursi mogu napraviti kopije vremenskih unosa u roku od tjedan dana, kao i skupnu kopiju iz prethodnih tjedana. Osobe zadužene za prilagodbu sustava mogu prilagoditi prikaz dodavanjem polja, dodavanjem pretraživanja drugim entitetima i primjenom prilagođenih poslovnih pravila koja odražavaju prakse njihove tvrtke ili ustanove.

Unosu vremena i novoj rešetki tjednih vremenskih unosa pristupa se na karti web-mjesta. Prilagođeni Unos vremena bez proširivanja koji je bio dio starijih verzija aplikacije PSA zamijenjen je proširivom rešetkom tjednih vremenskih unosa te dodatnim prikazom u rešetki i kalendaru samo za čitanje. Zbog te promjene korisnici mogu unijeti vrijeme po tjednima.

## <a name="page-layout"></a>Izgled stanice
Nova rešetka tjednih vremenskih unosa prilagođena je kontrola koja ima alatnu traku i dva glavna odjeljka: **Dimenzije** i **Trajanje**. Alatna traka sadrži gumb koji se primjenjuje samo na ovu prilagođenu kontrolu za rešetku vremenskih unosa. Nasuprot tome, gumbi u oknu radnje pri vrhu stranice primjenjuju se na tri vrste kontrola koje služe za Unos vremena: kontrolu za tjedni Unos vremena, kontrolu samo za čitanje i kontrolu kalendara.

### <a name="dimensions"></a>Dimenzije
U odjeljku **Dimenzije** sve dimenzije za koje se može unijeti vrijeme prikazuju se kao naslovi stupca. Sljedeće dimenzije podržane su kao gotova rješenja:

- Projekt
- Projektni zadatak
- Uloga
- Vrsta
- Status unosa

U odjeljku **Dimenzije** nije moguće uređivanje unutar retka. Ovaj odjeljak temelji se na prikazu koji omogućuje dodavanje prilagođenih polja u rešetku tjednih vremenskih unosa. Više informacija o tome kako dodati prilagođena polja potražite u odjeljku „Proširivost” u nastavku ove teme.

### <a name="duration"></a>Trajanje
U odjeljku Trajanje dani u tjednu prikazuju se kao zaglavlja stupaca. Ovaj odjeljak omogućuje uređivanje u retku. Nakon stvaranja retka unosa vremena koji ima odgovarajuće dimenzije, korisnici mogu brzo unutar retka unijeti vrijeme koje su potrošili na te dimenzije.

## <a name="create-a-new-time-entry"></a>Stvaranje novog unosa vremena
Da biste stvorili novi Unos vremena u rešetki vremenskih unosa, odaberite **Novo**. Prikazuje se dijaloški okvir **Brzo stvaranje unosa vremena**. U ovom dijaloškom okviru korisnici mogu odabrati datum unosa vremena, a zatim unijeti podatke za dimenzije **Projekt**, **Projektni zadatak**, **Uloga** i **Trajanje** u minutama, satima ili danima tako da uz broj unesu **h**, **m** ili **d**. Isto tako, korisnici također unijeti opis i komentare koji se mogu dijeliti s vanjskim korisnicima za Unos vremena. Kada korisnici spreme promjene, vrijednosti koje su unijeli po dimenzijama prikazuju se u odjeljku **Dimenzije**. Podaci o trajanju koje su unijeli u polje **Trajanje** prikazuju se na datumu za koji je Unos vremena stvoren.

Polja za traženje podržavaju sistemski prikazi. Na primjer, nakon što korisnik unese projekt, polje **Projektni zadatak** prema zadanim postavkama postavljeno je na prikaz **Kopiranje**. Da biste stvorili vremenske unose za zadatke koji nisu dodijeljeni korisniku, odaberite **Promijeni prikaz** u dijaloškom okviru za traženje, a zatim odaberite prikaz **Svi aktivni zadaci projekta**.

## <a name="edit-a-time-entry"></a>Uređivanje unosa vremena
Pojedinosti iz nekih polja na stranici za Unos vremena, kao što su **Opis** i **Vanjski komentari**, ne prikazuju se u rešetki tjednih vremenskih unosa. Umjesto toga se u ćelijama s trajanjem koje imaju te dodatne pojedinosti prikazuje mali trokut. Odaberite ćeliju, a zatim **Uredi pojedinosti** da biste pregledali podatke u oknu **Brzo uređivanje**. Da bi uredili ili ažurirali pojedinosti za određeni Unos vremena koji nije dio rešetke tjednih vremenskih unosa, korisnici moraju otvoriti okno **Brzo uređivanje**.

## <a name="copy-a-time-entry-row"></a>Kopiranje retka unosa vremena
Nakon stvaranja prvog retka unosa vremena korisnici mogu odabrati **Kopiraj redak** za kopiranje cijelog retka u novi redak. Kada se redak kopira na taj način, kopiraju se i dimenzije i trajanje. Isto tako, korisnici mogu odabrati **Uredi redak** za ažuriranje vrijednosti dimenzija i trajanja unutar retka u odjeljku **Trajanje**.

## <a name="open-a-time-entry"></a>Otvaranje unosa vremena
Za optimalan i brz unos u najistaknutija polja rešetka tjednih vremenskih unosa prikazuje podskup odabranih dimenzija i trajanja. Da biste pregledali sve pojedinosti jednog unosa vremena, u odjeljku **Uređivanje unosa** odaberite **Otvori**.

## <a name="submit-a-time-entry"></a>Slanje unosa vremena
Korisnici mogu poslati jedan Unos vremena ili grupu vremenskih unosa tako da odaberu blok ćelija ili cijeli redak vremenskih unosa, a zatim odaberu **Pošalji**. Poslani Unos vremenai prikazuju se kao unosi koji čekaju odobravanje na stranici **Odobrenje** odobravatelja. Nakon što se Unos vremenai uspješno pošalju, ne mogu se uređivati.

## <a name="recall-a-time-entry"></a>Opoziv unosa vremena
Možete opozvati unose koje ste poslali. Možete opozvati jedan Unos vremena, blok vremenskih unosa ili cijeli redak vremenskih unosa. Opozvani Unos vremenai dostupni su resursima za uređivanje.

## <a name="time-entry-status"></a>Status unosa vremena
Novim vremenskim unosima automatski se dodjeljuje status **Skica**. Kada se Unos vremena pošalje, status se ažurira na **Poslano**. Kada se poslani Unos vremena odobri, status se ažurira na **Odobreno**. Ako je Unos vremena odbijen, status se ažurira na **Vraćeno**, a unos postaje dostupan za ispravak i ponovno slanje. Mogu se izbrisati samo Unos vremenai koji imaju status **Skica**.

## <a name="view-rejection-comments"></a>Prikaz komentara o odbijanju
Kada odobravatelj odbije Unos vremena, odobravatelj može dodati komentare o odbijanju kako bi resurs saznao zašto je unos odbijen. Za prikaz komentara o odbijanju za Unos vremena odaberite **Otvori unos**. Komentari o odbijanju prikazuju se na vremenskoj traci. Resurs na vremenskoj traci može odgovoriti na komentare o odbijanju prije nego što ponovno pošalje unos.

## <a name="copy-week"></a>Kopiranje tjedna
Nakon što se stvori nekoliko unosa vremena, korisnici mogu odabrati **Kopiraj tjedan** za masovno stvaranje dodatnih vremenskih unosa. Prikazuje se dijaloški okvir **Kopiraj**. U odjeljku **Razdoblje od** u poljima **Datum početka** i **Datum završetka** definirajte raspon datuma iz kojih ćete kopirati vremenske unose. U odjeljku **Razdoblje do** u polju **Datum početka** navedite datum za koji stvarate vremenske unose. Zatim odaberite **Kopiraj**. Za navedeni datum u razdoblju „do” stvara se kopija unosa vremena za odgovarajući dan u tjednu u razdoblju „od”. Na primjer, Unos vremena za ponedjeljak od prošlog tjedna kopira se u ponedjeljak u tjednu koji je naveden kao razdoblje „do”.

## <a name="import"></a>Uvezi
Isti osnovni postupak koristi se za uvoz iz rezervacija, dodjela i razmjena. Korisnici mogu odrediti raspon datuma iz kojeg se uvoze rezervacije. Zatim moraju posebno odabrati rezervacije koje treba kopirati u nacrte vremenskih unosa. U prethodnom izdanju predloženi Unos vremenai prikazivali su se u rešetki i kalendaru, a gubili su se kad bi se sesija osvježila.

## <a name="extensibility"></a>Proširivost
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Dodavanje prilagođenih polja koja imaju pretraživanja za druge entitete
Postoje tri glavna koraka za dodavanje prilagođenog polja u rešetku tjednih vremenskih unosa.

1.  Dodajte prilagođeno polje u dijaloški okvir za brzo stvaranje.
2.  Konfigurirajte rešetku kako bi se prikazivalo prilagođeno polje.
3.  Dodajte prilagođeno polje u izvođenje zadatka uređivanja retka ili u izvođenje zadatka uređivanja ćelije, prema potrebi.

Isto tako, morate provjeriti ima li novo polje ima potrebne provjere valjanosti u izvođenju zadatka uređivanja retka ili ćelije. U ovom koraku morate zaključati polje na temelju statusa unosa vremena.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Dodavanje prilagođenog polja u dijaloški okvir za brzo stvaranje
Potrebno je dodati prilagođeno polje u dijaloški okvir Brzo stvaranje unosa vremena tako da korisnici mogu unijeti vrijednost za njega kada dodaju vremenske unose pomoću gumba **Novo**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfiguriranje rešetke kako bi se prikazivalo prilagođeno polje
Postoje dva načina dodavanja prilagođenog polja u rešetku tjednih vremenskih unosa. Prva je mogućnost prilagođavanje prikaza **Moji tjedni Unos vremenai** i dodavanje prilagođenog polja u njega. Možete odabrati položaj i veličinu prilagođenog polja u rešetki uređivanjem tih svojstava u prikazu.

Druga je mogućnost stvaranje novog prilagođenog prikaza unosa vremena i postavljanje tog unosa kao zadani prikaz. Ovaj prikaz mora sadržavati polja **Opis** i **Vanjski komentari**, kao i stupce koje želite dodati u rešetku. Možete odabrati položaj, veličinu i zadani redoslijed sortiranja u rešetki uređivanjem tih svojstava u prikazu. Zatim konfigurirajte prilagođenu kontrolu za ovaj prikaz tako da je podesite kao kontrolu **Rešetka unosa vremena**. Dodajte ovu kontrolu u prikaz i odaberite ga za web, telefone i tablete. Zatim konfigurirajte parametre za rešetku tjednih vremenskih unosa. Polje **Datum početka** postavite na **msdyn_date**, polje **Trajanje** na **msdyn_duration**, a polje **Status** na **msdyn_entrystatus**. Za zadani prikaz polje **Popis statusa samo za čitanje** postavljeno je na **192350002, 192350003, 192350004**, polje **Izvođenje zadatka uređivanja retka** postavljeno je na **msdyn_timeentryrowedit**, a polje **Izvođenje zadatka uređivanja ćelije** postavljeno je na **msdyn_timeentryedit**. Ta polja možete prilagoditi za dodavanje ili uklanjanje statusa samo za čitanje ili za upotrebu drugog iskustva na temelju zadatka (TBX) za uređivanje retka ili ćelije. Ta polja trebaju biti vezana za statičku vrijednost.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Dodavanje prilagođenog polja odgovarajućem izvođenju zadatka uređivanja
TBX stranice koje se koriste za uređivanje mogu se pronaći u odjeljku **Procesi**. Zadane stranice su **Project Service – uređivanje retka unosa vremena** i **Project Service – uređivanje unosa vremena** Možete urediti te zadane stranice ili stvoriti nove prilagođene TBX stranice.

> [!NOTE] 
> Obje mogućnosti uklonit će neke unaprijed pripremljene filtre u entitetima **Projekt** i **Projektni zadatak** tako da će svi prikazi za traženje za entitete biti vidljivi. Prikazuju se samo unaprijed pripremljeni relevantni prikazi za traženje.

Morate odrediti odgovarajuće izvođenje zadatka za prilagođeno polje. Ako ste dodali polje u rešetku, ono bi vjerojatno trebalo ići u izvođenje zadatka uređivanja retka koje se koristi za polja koja se primjenjuju na cijeli redak vremenskih unosa. Ako prilagođeno polje ima jedinstvenu vrijednost svaki dan, kao što je prilagođeno polje za **Vrijeme završetka**, ono bi trebalo ići u izvođenje zadatka uređivanja ćelije.

Za dodavanje prilagođenog polja u izvođenje zadatka, povucite element **Polje** u odgovarajući položaj na stranici, a zatim postavite njegova svojstva. Postavite svojstvo **Izvor** na **Unos vremena**, a svojstvo **Polje podataka** postavite na prilagođeno polje. Svojstvo **Polje** određuje zaslonski naziv na TBX stranici. Odaberite **Primijeni** za spremanje izmjena u polju. Zatim odaberite **Ažuriraj** za spremanje izmjena na stranici.

Da biste umjesto toga koristili novu prilagođenu TBX stranicu, stvorite novi proces. Postavite kategoriju na **Tijek poslovnog procesa**, postavite entitet na **Unos vremena** i postavite vrstu poslovnog procesa pomoću mogućnosti **Pokreni proces kao izvođenje zadatka**. U odjeljku **Svojstva** svojstvo **Naziv stranice** treba biti postavljeno na zaslonski naziv za stranicu. Dodajte sva relevantna polja na TBX stranicu. Spremite i aktivirajte proces, a zatim ažurirajte svojstvo prilagođene kontrole za odgovarajuće izvođenje zadatka na vrijednost **Naziv** u procesu.

### <a name="add-new-option-set-values"></a>Dodavanje novih vrijednosti skupa mogućnosti
Da biste dodali vrijednosti skupa mogućnosti u unaprijed pripremljeno polje, otvorite stranicu za uređivanje za polje, a zatim u odjeljku **Vrsta** odaberite **Uredi** pokraj skupa mogućnosti. Zatim dodajte novu mogućnost koja ima prilagođenu oznaku i boju. Ako želite dodati novi status unosa vremena, unaprijed pripremljeno polje pod nazivom **Status unosa**, a ne **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Određivanje novog statusa unosa vremena kao unosa samo za čitanje
Da biste odredili novi status unosa vremena kao samo za čitanje, dodajte novu vrijednost unosa vremena (broj, a ne oznaku) u svojstvo **Popis statusa samo za čitanje**. Dio rešetke vremenskih unosa za uređivanje bit će zaključan za retke koji imaju novi status.
Zatim dodajte poslovna pravila da biste zaključali sva polja na TBX stranicama **Uređivanje retka za unos vremena** i **Uređivanje unosa vremena**. Poslovnim pravilima za te stranice možete pristupiti tako da otvorite uređivač izvođenja poslovnog procesa za stranicu, a zatim odaberete **Poslovna pravila**. Možete dodati novi status uvjetu u postojećim poslovnim pravilima ili možete dodati novo poslovno pravilo za novi status.

### <a name="add-custom-validation-rules"></a>Dodavanje prilagođenih pravila provjere valjanosti
Postoje dvije vrste pravila provjere valjanosti koje možete dodati za rešetku tjednih vremenskih unosa: •   poslovna pravila sa strane klijenta koja funkcioniraju u dijaloškim okvirima za brzo stvaranje i na TBX stranicama •   provjere valjanosti dodatka sa strane poslužitelja koje se odnose na sva ažuriranja unosa vremena

#### <a name="business-rules"></a>Poslovna pravila
Poslovna pravila služe za zaključavanje i otključavanje polja, unos zadanih vrijednosti u polja i određivanje provjera valjanosti koje zahtijevaju informacije samo iz trenutačnog zapisa unosa vremena. Poslovnim pravilima za TBX stranice možete pristupiti tako da otvorite uređivač izvođenja poslovnog procesa za stranicu, a zatim odaberete **Poslovna pravila**. Zatim možete urediti postojeća poslovna pravila ili dodati novo poslovno pravilo. Za još više prilagođenih provjera valjanosti možete upotrijebiti poslovno pravilo za pokretanje JavaScripta.

#### <a name="plug-in-validations"></a>Provjere valjanosti dodatka
Provjere valjanosti dodatka trebate upotrebljavati za sve provjere valjanosti koje zahtijevaju više konteksta nego što je dostupno u jednom zapisu unosa vremena ili za provjere valjanosti koje želite pokrenuti na ažuriranjima unutar retka na rešetki. Da biste dovršili provjeru valjanosti, stvorite prilagođeni dodatak u entitetu **Unos vremena**.

> [!IMPORTANT] 
> Trenutačno poznati problem na TBX stranicama korisnicima onemogućuje ispravljanje podataka i ponovni odabir naredbe Gotovo kada ažuriranje ne uspije provjeriti valjanost dodatka. Zaobilazno je rješenje postavljanje provjere valjanosti poslovnog pravila kako bi se to što je više moguće izbjeglo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]