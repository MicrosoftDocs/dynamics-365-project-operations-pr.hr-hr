---
title: Ponašanje korisničkog sučelja za unos vremena
description: U ovoj temi nalaze se informacije o ponašanju korisničkog sučelja za unos vremena.
author: stsporen
ms.date: 03/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0cb62231eb3b387b610b7510023994dce66b1cc9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995882"
---
# <a name="time-entry-ui-behavior"></a>Ponašanje korisničkog sučelja za unos vremena

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_


Rešetka **Tjedni unos vremena** prilagođena je kontrola koja ima dva glavna odjeljka, **Dimenzije** i **Trajanje**.

## <a name="keyboard-shortcuts"></a>Tipkovni prečaci
| Akcija        | Prečac                  |
|------------   |------------------------   |
| Novo           | Alt + Shift + n           |
| Kopiraj redak      | Alt + Shift + c           |
| Uredi unos    | Alt + Shift + e           |
| Uredi redak      | Alt + Shift + Ctrl + e    |
| Otvori unos    | Alt + Shift + o           |
| Slanje        | Alt + Shift + s           |
| Opoziv        | Alt + Shift + r           |
| Izbriši        | Alt + Shift + d           |
| Kopiraj tjedan     | Alt + Shift + w           |

## <a name="dimensions"></a>Dimenzije
U odjeljku **Dimenzije** prikazuju se sve dimenzije prema kojima se može unijeti vrijeme. Sljedeće dimenzije podržane su kao gotova rješenja:

  - Project
  - Projektni zadatak
  - Uloga
  - Tip
  - Status unosa

U odjeljku **Dimenzije** nije dozvoljeno uređivanje unutar retka. Ovaj odjeljak temelji se na prikazu koji omogućuje dodavanje prilagođenih polja u rešetku tjednih vremenskih unosa.

## <a name="duration"></a>Trajanje
U odjeljku Trajanje dani u tjednu prikazuju se kao zaglavlja stupaca. Ovaj odjeljak omogućuje uređivanje u retku. Nakon stvaranja retka za unos vremena odgovarajućih dimenzija, korisnici mogu brzo unutar retka unijeti vrijeme koje su potrošili na te dimenzije.

## <a name="create-a-new-time-entry"></a>Stvaranje novog unosa vremena

1. U rešetki za unos vremena odaberite **Novo**. 
2. U dijaloškom okviru **Brzo stvaranje unosa vremena** odaberite datum unosa vremena.
3. Unesite podatke za dimenzije **Projekt**, **Projektni zadatak**, **Uloga** i **Trajanje**. Ove podatke trebate dodati u minutama, satima ili danima upisivanjem **h**, **m** ili **d**, zajedno s brojem. 
4. Unesite opis unosa i sve komentare koji se mogu dijeliti s vanjskim korisnicima koji se odnose na unos vremena. 

Kada spremite unos, unesene vrijednosti prikazuju se u odjeljku **Dimenzije**. Podaci uneseni u polje **Trajanje** prikazuju se na datumu za koji je unos vremena stvoren.

Polja za traženje podržavaju sistemski prikazi. Na primjer, nakon što korisnik unese projekt, polje **Projektni zadatak** prema zadanim postavkama postavljeno je na prikaz **Kopiranje**. Da biste stvorili vremenske unose za zadatke koji nisu dodijeljeni korisniku, odaberite **Promijeni prikaz** u dijaloškom okviru za traženje, a zatim odaberite prikaz **Svi aktivni zadaci projekta**.

## <a name="edit-a-time-entry"></a>Uređivanje unosa vremena 
Pojedinosti iz nekih polja na stranici za Unos vremena, kao što su **Opis** i **Vanjski komentari**, ne prikazuju se u rešetki tjednih vremenskih unosa. Umjesto toga, u ćelijama **Trajanje** koje imaju te dodatne pojedinosti prikazuje se mali trokutasti indikator. 

1. Kako biste uredili unos vremena, odaberite ćeliju koju želite ažurirati u unosu vremena.
2. Odaberite mogućnost **Uredi pojedinosti** kako biste ažurirali podatke u oknu **Glavni obrazac za unos vremena**. 

## <a name="copy-a-time-entry-row"></a>Kopiranje retka za unos vremena
Nakon stvaranja retka možete odabrati mogućnost **Kopiraj redak** kako biste cijeli redak kopirali u novi redak. Kada se redak kopira na taj način, kopiraju se i dimenzije i trajanje. Isto tako, možete odabrati **Uredi redak** kako biste u odjeljku **Trajanje** ažurirali vrijednosti dimenzija i trajanja.

## <a name="open-a-time-entry-behavior"></a>Otvaranje ponašanja unosa vremena
Za podršku optimalnom i brzom unosu u najistaknutija polja rešetka tjednih vremenskih unosa prikazuje podskup odabranih dimenzija i trajanja. Da biste pregledali sve pojedinosti jednog unosa vremena, u odjeljku **Uređivanje unosa** odaberite **Otvori**.

## <a name="submit-a-time-entry"></a>Slanje unosa vremena
Možete poslati jedan unos vremena ili grupu unosa vremena odabirom bloka ćelija ili cijelog stupca za unos vremena, a zatim odaberite **Pošalji**. Poslani Unos vremenai prikazuju se kao unosi koji čekaju odobravanje na stranici **Odobrenje** odobravatelja. Nakon što se Unos vremenai uspješno pošalju, ne mogu se uređivati.

## <a name="recall-a-time-entry"></a>Opoziv unosa vremena
Možete opozvati unose koje ste poslali. Možete opozvati jedan Unos vremena, blok vremenskih unosa ili cijeli redak vremenskih unosa. Opozvani unosi vremena mogu se uređivati.

## <a name="time-entry-status"></a>Status unosa vremena

- **Skica**: Novim vremenskim unosima automatski se dodjeljuje status **Skica**. Mogu se izbrisati samo Unos vremenai koji imaju status **Skica**.
- **Poslano**: Kada se unos vremena pošalje, status se ažurira na **Poslano**. 
- **Odobreno**: Kada se poslani unos vremena odobri, status se ažurira na **Odobreno**. 
- **Vraćeno**: Ako je unos vremena odbijen, status se ažurira na **Vraćeno**, a unos postaje dostupan za ispravak i ponovno slanje. 

## <a name="view-rejection-comments"></a>Prikaz komentara o odbacivanju
Kada odobravatelj odbije Unos vremena, odobravatelj može dodati komentare kako bi resurs saznao zašto je unos odbijen. Za prikaz komentara o odbacivanju za Unos vremena odaberite **Otvori unos**. Komentari o odbacivanju prikazuju se na vremenskoj traci. Korisnik može odgovoriti na komentare odbijanja prije nego što ponovo pošalju unos.

## <a name="copy-week"></a>Kopiraj tjedan
Nakon stvaranja nekoliko unosa vremena, korisnici mogu istodobno stvoriti više vremenskih unosa.

1. U obrascu **Unosi vremena** odaberite **Kopiraj tjedan** za skupno stvaranje dodatnih unosa vremena. 
2. U dijaloškom okviru **Kopiraj**, u odjeljku **Od razdoblja**, upotrijebite polja **Datum početka** i **Datum završetka** kako biste definirali raspon datuma iz kojih ćete kopirati unose vremena. 
3. U odjeljku **Razdoblje do** u polju **Datum početka** navedite datum za koji stvarate vremenske unose. 
4. Odaberite **Kopiraj**. Za navedeni datum u stavci **Do razdoblja**, stvara se kopija unosa vremena za odgovarajući dan u tjednu u stavci **Od razdoblja**. Na primjer, Unos vremena za ponedjeljak od prošlog tjedna kopira se u ponedjeljak u tjednu koji je naveden kao vrijednost stavke **Do razdoblja**.

## <a name="import"></a>Uvezi
Isti osnovni postupak koristi se za uvoz iz rezervacija, dodjela i razmjena. Možete navesti raspon datuma iz kojeg se vrši uvoz rezervacija, a zatim izričito odabrati rezervacije koje treba kopirati u skice unosa vremena. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
