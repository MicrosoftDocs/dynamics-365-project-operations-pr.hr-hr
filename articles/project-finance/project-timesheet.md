---
title: Mobilna aplikacija Project Timesheet
description: U ovoj se temi nalaze informacije o mobilnoj aplikaciji Microsoft Dynamics 365 Project Timesheet. Mobilna aplikacija Project Timesheet omogućuje korisnicima slanje i odobravanje evidencija radnog vremena za projekte na mobilnom uređaju.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: e2eb387f-5bb3-419c-953b-3bbc2f050059
ms.search.region: Global
ms.search.industry: Service industries
ms.author: josaw1
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 6cd4629e9380fbe3d1839ba31a819c9057d1258c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750149"
---
# <a name="project-timesheet-mobile-application"></a>Mobilna aplikacija Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Pregled

Mobilna aplikacija Microsoft Dynamics 365 Project Timesheet omogućuje korisnicima slanje i odobravanje evidencija radnog vremena za projekte na mobilnom uređaju (iPhone ili Android). Ova mobilna aplikacija prikazuje funkcionalnost evidencije radnog vremena koja se nalazi u području Upravljanje projektima i računovodstvo aplikacije Dynamics 365 Finance, poboljšava produktivnost i učinkovitost korisnika i omogućuje pravodoban unos i odobravanja evidencija radnog vremena za projekt.

## <a name="download-and-install-the-mobile-app"></a>Preuzimanje i instaliranje mobilnu aplikaciju

Preuzmite i instalirajte mobilnu aplikaciju Microsoft Dynamics 365 Project Timesheet za sustave Android ili iPhone iz mobilne trgovine za vaš uređaj.

## <a name="enable-the-app"></a>Omogućivanje aplikacije 

U Financijama mora biti omogućena mobilna aplikacija Project Timesheet. Kako biste omogućili funkcionalnost, idite na **Parametri za upravljanje projektom i računovodstveni parametri \> Evidencija radnog vremena** i odaberite parametar **Omogući aplikaciju Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Prijava u aplikaciju

1.  Pokrenite aplikaciju na mobilnom uređaju.

2.  Unesite URL-adresu Financija.

3.  Kad se prvi put prijavite, od vas će se zatražiti korisničko ime i lozinka. Unesite vjerodajnice.

4.  Bit ćete prijavljeni u svoju zadanu tvrtku.

## <a name="submit-a-project-timesheet"></a>Pošaljite evidenciju radnog vremena za projekt

U aplikaciji možete stvoriti i poslati evidenciju radnog vremena za projekt. Novu evidenciju radnog vremena možete temeljiti na podacima iz prethodne evidencije radnog vremena, spremljenim redcima ili projektnim zadacima. Ako ste određeni za delegata, možete unijeti evidenciju radnog vremena i za drugog radnika. Za stvaranje evidencije radnog vremena kao delegata odaberite gumb **izbornik** i zatim odaberite naziv resursa.

Stranica evidencije radnog vremena stvorit će novu evidenciju radnog vremena za razdoblje evidencije radnog vremena na temelju trenutačnog datuma. Prikazat će se radni tjedan. Ako razdoblje evidencije radnog vremena obuhvaća više tjedana, na karticama radnog tjedna možete odabrati drugi radni tjedan.
Ako postoji evidencije radnog vremena za trenutačni datum, prikazat će se. Ako trebate stvoriti novu evidencije radnog vremena u drugom razdoblju evidencije radnog vremena, odaberite gumb **Izbornik** i zatim **Nova evidencija radnog vremena**.

Podatke o projektu možete unijeti klikom na radnje **Dodaj vrijeme** ili **Kopiraj vrijeme iz**. Radnja **Kopiraj vrijeme iz** kopirat će podatke retka projekta, ali ne i sate rada. Izbornik **Kopiraj vrijeme iz** uključuje sljedeće mogućnosti:

- **Kopiraj iz postojeće evidencije radnog vremena** – Kopirajte retke evidencije radnog vremena iz postojeće evidencije radnog vremena.

- **Kopiraj iz favorita** – Stvorite nove retke evidencije radnog vremena s pomoću postavki evidencije radnog vremena koje ste odabrali kao favorite.

- **Kopiraj iz zadatka** – Stvorite nove retke evidencije radnog vremena iz dodijeljenih projekata.

Podaci o projektu koji se prikazuju ovise o mobilnim parametrima koje ste definirali na stranici **Parametri za upravljanje projektom i računovodstveni parametri**.

U polju **Pravna osoba** odaberite pravnu osobu za koju ste izvodili projektne radove. Polje **Pravna osoba** dostupno je samo ako je za vašu pravnu osobu omogućena podrška za evidenciju radnog vremena unutar tvrtke.

Za evidenciju radnog vremena odaberite klijenta koji je povezan s projektom. Za početno izdanje na sustavu Android, unos od strane klijenta nije podržan, jer najprije morate odabrati projekt. Ako ste prvo odabrali projekt, polje **Klijent** popunjava se automatski.

U polju **Projekt** odaberite projekt za koji unosite vrijeme. Polje **Klijent** popunjava se automatski.

Pretraživanja klijenata i projekata omogućuju pretraživanje i klijenata i projekata.

Odaberite podatke u poljima **Kategorija**, **Aktivnost**, **Svojstvo retka**, **Grupa PDV-a** i **Grupa PDV-a na predmet**, ako je potrebno. Ta se polja mogu prebrisati.

Polje **Svojstvo retka** postavit će se na zadanu vrijednost, na temelju parametara za upravljanje projektom i računovodstvenih parametara. Kada su omogućeni parametri projekta/kategorije i kategorije/resursa, vrijednost **Svojstvo retka** postavit će se na zadanu vrijednost koju ste definirali za ovu provjeru valjanosti. Kada parametri projekta/kategorije i kategorije/resursa nisu omogućeni, vrijednost postavke **Svojstvo retka** zadat će se prema polju **Omogući zadano svojstvo retka** na stranici **Parametri za upravljanje projektom i računovodstveni parametri**. Vrijednost **Svojstvo retka** može se prebrisati.

Odaberite dan za dodavanje vremena. Unesite broj svakodnevno odrađenih sati.

Kako biste dodali komentare o satima koje unosite, kliknite **Dodaj komentare**, a zatim unesite komentare za internu ciljnu skupinu, ciljnu skupinu klijenata ili za oboje.
Interne komentare mogu pregledati voditelji projekata. Komentari klijenata uključeni su u fakture.

Kako biste redak spremili kao favorit, označite potvrdni okvir, a zatim kliknite **Spremi kao favorit**.

Financijska dimenzija i podrška privitaka nisu osigurani u mobilnoj aplikaciji.

Nastavite dodavati retke projekta po potrebi, kako biste popunili svoju evidenciju radnog vremena.

Kliknite **Pošalji** za slanje evidencije radnog vremena u tijek rada za odobrenje.

## <a name="review-timesheets"></a>Pregledavanje evidencija radnog vremena

Popis evidencija radnog vremena koje treba pregledati dostupan je u izborniku. Ova je mogućnost dostupna samo ako ste određeni za odobravatelja tijeka rada. Podržani su i zaglavlje i redak odobrenja. Odobrenje na razini retka nudi mogućnost označavanja jednog ili više redaka za odobrenje. Nakon pregleda podataka iz evidencije o radnom vremenu, kliknite **Odobri**, **Delegiraj** ili **Povratak** kako biste nastavili tijeka rada.
