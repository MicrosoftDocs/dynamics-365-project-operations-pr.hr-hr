---
title: Mobilna aplikacija Project Timesheet
description: Ovaj članak pruža informacije o mobilnoj aplikaciji Microsoft Dynamics 365 Project Timesheet. Mobilna aplikacija Project Timesheet omogućuje korisnicima slanje i odobravanje evidencija radnog vremena za projekte na mobilnom uređaju.
author: abruer
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110966"
---
# <a name="project-timesheet-mobile-application"></a>Mobilna aplikacija Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Pretpregled

Mobilna Microsoft Dynamics 365 Project Timesheet aplikacija omogućuje korisnicima slanje i odobravanje vremenskih tablica za projekte na svom mobilnom uređaju (iPhone ili Android). Ova mobilna aplikacija prikazuje funkcionalnost vremenske tablice koja se nalazi u području upravljanja projektima i računovodstva u Dynamics 365 Finance. Pomaže u poboljšanju produktivnosti i učinkovitosti korisnika, a također omogućuje pravovremeni ulazak i odobravanje vremenskih tablica projekta.

## <a name="download-and-install-the-mobile-app"></a>Preuzimanje i instaliranje mobilnu aplikaciju

Preuzmite i instalirajte mobilnu aplikaciju Microsoft Dynamics 365 Project Timesheet za sustave Android ili iPhone iz mobilne trgovine za vaš uređaj.

## <a name="enable-the-app"></a>Omogućivanje aplikacije 

U Financijama mora biti omogućena mobilna aplikacija Project Timesheet. Kako biste omogućili funkcionalnost, idite na **Parametri za upravljanje projektom i računovodstveni parametri \> Evidencija radnog vremena** i odaberite parametar **Omogući aplikaciju Microsoft Dynamics 365 Project Timesheet**.

### <a name="resolve-sign-in-issues"></a>Rješavanje problema s prijavom

**Problem:** tijekom prijave u aplikaciju Project Timesheet Mobile korisnici dobivaju poruku o pogrešci u kojoj se navodi da "ne mogu pristupiti aplikaciji "2bc50526-cdc3-4e36-a970-c284c34cbd6e" u tom klijentu".

**Problem:** tijekom prijave u aplikaciju Project Timesheet Mobile korisnici dobivaju pogrešku sličnu jednom od sljedećih primjera:

- "AADSTS50020: Korisnički račun "[korisničko ime]' od davatelja identiteta 'https://sts.windows.net/[ID aplikacije]' ne postoji u klijentu '[id klijenta]' i ne može pristupiti aplikaciji '[ID aplikacije]' u tom klijentu."
- "Odabrani korisnički račun ne postoji u klijentu '[ID klijenta]' i ne može pristupiti aplikaciji '[ID aplikacije]' u tom klijentu."

**Objašnjenje:** Ti su problemi uzrokovani promjenom koja je napravljena na Azure Active Directory (Azure AD) u svibnju 2022. i koja se odnosi na vanjske korisnike. Budući da ova promjena nije napravljena u aplikacijama za financiranje i operacije, može utjecati na korisnike na bilo kojoj verziji platforme ili aplikacije.

**Popravak:** Svi vanjski korisnici moraju biti pozvani klijentu putem Azure AD sustava. Dodatne informacije potražite u članku [Pozivanje korisnika uz Azure Active Directory B2B suradnju](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Prijava u aplikaciju

1.  Pokrenite aplikaciju na mobilnom uređaju.

2.  Unesite URL-adresu Financija.

3.  Kad se prvi put prijavite, od vas će se zatražiti korisničko ime i lozinka. Unesite vjerodajnice.

4. Bit ćete prijavljeni u zadanu tvrtku.

## <a name="submit-a-project-timesheet"></a>Pošaljite evidenciju radnog vremena za projekt

U aplikaciji možete stvoriti i poslati evidenciju radnog vremena za projekt. Novu evidenciju radnog vremena možete temeljiti na podacima iz prethodne evidencije radnog vremena, spremljenim redcima ili projektnim zadacima. Ako ste određeni kao delegat, možete unijeti i vremensku tablicu za drugog radnika. Da biste stvorili vremensku tablicu kao delegat, odaberite **gumb Izbornik**, a zatim odaberite naziv resursa.

Stranica evidencije radnog vremena stvorit će novu evidenciju radnog vremena za razdoblje evidencije radnog vremena na temelju trenutačnog datuma. Prikazat će se radni tjedan. Ako razdoblje evidencije radnog vremena obuhvaća više tjedana, na karticama radnog tjedna možete odabrati drugi radni tjedan.
Ako postoji evidencije radnog vremena za trenutačni datum, prikazat će se. Ako trebate stvoriti novu evidencije radnog vremena u drugom razdoblju evidencije radnog vremena, odaberite gumb **Izbornik** i zatim **Nova evidencija radnog vremena**.

Podatke o projektu možete unijeti klikom na radnje **Dodaj vrijeme** ili **Kopiraj vrijeme iz**. Radnja **Kopiraj vrijeme iz** kopirat će podatke retka projekta, ali ne i sate rada. Izbornik **Kopiraj vrijeme iz** uključuje sljedeće mogućnosti:

- **Kopiraj iz postojeće evidencije radnog vremena** – Kopirajte retke evidencije radnog vremena iz postojeće evidencije radnog vremena.

- **Kopiraj iz favorita** – Stvorite nove retke evidencije radnog vremena s pomoću postavki evidencije radnog vremena koje ste odabrali kao favorite.

- **Kopiraj iz zadatka** – Stvorite nove retke evidencije radnog vremena iz dodijeljenih projekata.

Podaci o projektu koji se prikazuju ovise o mobilnim parametrima koje ste definirali na stranici **Parametri za upravljanje projektom i računovodstveni parametri**.

U polju **Pravna osoba** odaberite pravnu osobu za koju ste izvodili projektne radove. Polje **Pravna osoba** dostupno je samo ako je za vašu pravnu osobu omogućena podrška za evidenciju radnog vremena unutar tvrtke.

Za evidenciju radnog vremena odaberite klijenta koji je povezan s projektom. Za početno izdanje na Android, unos klijenta nije podržan, jer prvo morate odabrati projekt. Ako ste prvo odabrali projekt, polje **Klijent** popunjava se automatski.

**U polju Projekt** odaberite projekt za koji unosite vrijeme. Polje **Klijent** popunjava se automatski.

Pretraživanja klijenata i projekata omogućuju pretraživanje i klijenata i projekata.

Odaberite podatke u poljima **Kategorija**, **Aktivnost**, **Svojstvo retka**, **Grupa PDV-a** i **Grupa PDV-a na predmet**, ako je potrebno. Ta se polja mogu prebrisati.

Polje **Svojstvo retka** postavit će se na zadanu vrijednost, na temelju parametara za upravljanje projektom i računovodstvenih parametara. Kada su omogućeni parametri projekta/kategorije i kategorije/resursa, vrijednost **Svojstvo retka** postavit će se na zadanu vrijednost koju ste definirali za ovu provjeru valjanosti. Kada parametri projekta/kategorije i kategorije/resursa nisu omogućeni, **vrijednost svojstva** Redak zadana će postavka u skladu s **poljem Omogući zadano svojstvo** zadanog retka na **stranici Upravljanje projektom i računovodstveni parametri**. Vrijednost **Svojstvo retka** može se prebrisati.

Odaberite dan za dodavanje vremena. Unesite broj svakodnevno odrađenih sati.

Da biste dodali komentare o satima koje unosite, kliknite **Dodaj komentare**, a zatim unesite komentare za interni publika, publika kupaca ili oboje.
Interne komentare mogu pregledati voditelji projekata. Komentari klijenata uključeni su u fakture.

Kako biste redak spremili kao favorit, označite potvrdni okvir, a zatim kliknite **Spremi kao favorit**.

Financijska dimenzija i podrška za privitke ne pružaju se u mobilnoj aplikaciji.

Nastavite dodavati retke projekta po potrebi, kako biste popunili svoju evidenciju radnog vremena.

Kliknite **Pošalji** za slanje evidencije radnog vremena u tijek rada za odobrenje.

## <a name="review-timesheets"></a>Pregledavanje evidencija radnog vremena

Popis vremenskih tablica koje je potrebno pregledati dostupan je na izborniku. Ova mogućnost dostupna je samo ako ste imenovani kao odobravatelj tijeka rada. Podržani su i zaglavlje i redak odobrenja. Odobrenje na razini retka nudi mogućnost označavanja jednog ili više redaka za odobrenje. Nakon pregleda podataka iz evidencije o radnom vremenu, kliknite **Odobri**, **Delegiraj** ili **Povratak** kako biste nastavili tijeka rada.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
