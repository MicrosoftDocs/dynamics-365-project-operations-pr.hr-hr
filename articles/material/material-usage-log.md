---
title: Bilježenje utrošenog materijala na projektima i projektnim zadacima
description: U ovom se članku navode informacije o tome kako zabilježiti upotrebu materijala u odnosu na projekte i projektne zadatke.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eeb8303821bc4c246e37333ddbcb77ca798d2e8f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920051"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Bilježenje utrošenog materijala na projektima i projektnim zadacima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dok projektni tim obavlja zadatke na projektu, oni troše ili upotrebljavaju materijale. Zapisnik o utrošenom materijalu pruža način za bilježenje te upotrebe kako bi je voditelj projekta mogao odobriti i na kraju fakturirati klijentu. 

Kako biste zabilježili uporabu kataloga ili umetnutih materijala i poslali ih odobravatelju, slijedite ove korake: 

1. U navigacijskom oknu odaberite **Utrošeni materijal**, a zatim odaberite **Novi**.
2. Na stranici **Utrošeni novi materijal** unesite potrebne podatke o uporabi materijala, a zatim odaberite **Spremi**.

Tablica u nastavku pruža informacije o poljima na stranici **Zapisnik o utrošenom materijalu**. 

| **Polje** | **Opis** | **Utjecaj prema dolje** |
| --- | --- | --- |
| Opis | Opis utrošenog posebnog materijala. | Ovo polje ne utječe na niže razine. |
| Datum | Datum očekivane uporabe materijala. | Ovo polje ne utječe na niže razine. |
| Project | Popis aktivnih projekata. | Odabir projekta za zapisnik o utrošenom materijalu utječe na polje **Zadatak** za prikaz samo onih zadataka koji se tiču projekta. |
| Zadatak | Popis projektnih zadataka obuhvaća sažetak i zadatke lisnog čvora. | Odabir zadatka za zapisnik o utrošenom materijalu utječe na stvarni trošak materijala i stvarnu prodaju materijala za zadatak. Ako je ovo polje prazno, odgovarajuće cijene troška i prodaje materijala prate se i zbrajaju samo na razini projekta. |
| Odabir proizvoda | Navedite je li ovaj materijal utrošen za **Postojeći** (kataloški) proizvod ili **Umetnuti** proizvod. | Ovo polje određuje vrstu proizvoda. |
| Proizvod | ID proizvoda iz kataloga proizvoda. Kada odaberete ID proizvoda, polje **Odaberi proizvod** automatski se ažurira na **Postojeći proizvod**. ID se upotrebljava za dohvaćanje cijena troška i prodaje iz cjenika. | Ovo polje ne utječe na niže razine. |
| Opis Umetnutog proizvoda | Tekstno polje za upisivanje naziva proizvoda. Ovo je polje omogućeno samo nakon što odaberete proizvod za **Umetanje** u polju **Odaberi proizvod**.| Ovo polje ne utječe na niže razine. |
| Resurs koji je moguće rezervirati| Resurs koji je upotrebljavao ovaj materijal na projektu. Zadana je postavka ovog polja resurs prijavljenog korisnika koji se može rezervirati, ali se može promijeniti tako da bilježi uporabu u ime ostalih članova projektnog tima. | Ovo polje ne utječe na niže razine. |
| Grupa jedinica | Zadana vrijednost u ovom polju proizlazi iz grupe jedinica koja je postavljena kao zadana na kataloškom proizvodu. Ovo polje možete ažurirati kako biste odabrali drugu grupu jedinica. | Ovo polje ne utječe na niže razine. |
| Jedinica | Zadana vrijednost u ovom polju zadana je jedinica odabranog proizvoda. Ovo polje možete ažurirati kako biste odabrali drugu jedinicu. | Promjena jedinice rezultira drugačijom zadanom cijenom i troškom jedinice. |
| Količina | Količina proizvoda koja upotrijebljena na projektu ili projektnom zadatku. | Ovo polje ne utječe na niže razine. |
| Jedinična cijena | Jedinični trošak odabranog proizvoda i kombinacije jedinica kako su postavljeni u mjerodavnom troškovniku. | Jedinični trošak uvijek se prikazuje u valuti troška projekta. Ako u cjeniku nema jediničnog troška za kombinaciju proizvoda i jedinice, jedinični trošak zadat će se na 0,00. |
| Ukupni trošak | Iznos troška koji se izračunava kao količina \* jedinični trošak.| Iznos troška uvijek se prikazuje u valuti troška projekta. |


## <a name="submit-material-usage-for-review-and-approval"></a>Slanje utrošenog materijala na pregled i odobrenje 
Nakon što zabilježite sav utrošeni materijal i spremni ste dati ga na odobrenje, podatke o potrošnji morate poslati na pregled.

1. Idite na **Zapisnik o utrošenom materijalu** i odaberite jedan ili više unosa. Ili odaberite sve zapise o utrošenom materijalu s pomoću potvrdnog okvira na zaglavlju.
2. Odaberite **Šalji**. Sustav obrađuje odabrane unose, a zatim stvara zahtjeve za odobrenje utrošenog materijala.

## <a name="recall-a-material-usage-log"></a>Opozovi zapisnika o utrošenom materijalu

Kad je potrebno, možete opozvati prijavljeni utrošak materijala. Vrijeme potrebno za opoziv unosa utrošenog materijala ovisi o fazi odobrenja.  Ako odobravatelj još nije odobrio unos, storniranje se može izvršiti odmah. Međutim, ako je unos već odobren, od odobravatelja se treba zatražiti odobrenje opoziva i storniranja transakcija.

1. Idite na **Utrošeni materijal** i na popisu zapisnika o utrošenom materijalu odaberite utrošeni materijal za opoziv.
2. Odaberite **Storniraj**. Ako unos utrošenog materijala još nije odobren, sustav ga odmah opoziva. Ako je unos materijala već odobren, stvara se zahtjev za opoziv kako bi se odobravatelja obavijestilo da želite opozvati utrošeni materijal. Odobravatelj će tada potvrditi da se storniranje može izvršiti i unos će biti vraćen.

## <a name="delete-a-material-usage-log"></a>Brisanje zapisnika o utrošenom materijalu

Možete izbrisati zapisnike o utrošenom materijalu koji nisu poslani. Kako biste izbrisali zapisnik o utrošenom materijalu koji je već poslan, prvo ga morate opozvati.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
