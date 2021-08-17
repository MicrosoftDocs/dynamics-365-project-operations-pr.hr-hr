---
title: Pregled odobrenja
description: U ovoj temi nalaze se informacije o radu s odobrenjima u aplikaciji Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: d77c62455c346d6d427d71af4b01d62b5132a2377c2c1a0a64f56fb313219c46
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991702"
---
# <a name="approvals-overview"></a>Pregled odobrenja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Prijave vremena, troškova i utrošenog materijala kreću se kroz radni tijek odobrenja. Nakon odobrenja unosa, transakcije se bilježe u stvarnim podacima ili se vrijeme rezervira u rasporedu.

## <a name="approvals-workflow"></a>Tijek rada odobrenja
Kada stvorite i pošaljete unos vremena, troška ili utrošenog materijala, stvara se zapis o odobrenju. Odobravatelji ili voditelj projekta pregledava i odobrava unos. Ako je unos povezan s projektom, stvarni podaci stvorit će se kada bude odobren. To omogućuje praćenje troškova i naplate.

## <a name="approve-an-entry"></a>Odobravanje unosa
Stranica **Odobrenja** omogućuje vam prebacivanje između različitih prikaza kako biste mogli pregledavati različite vrste odobrenja.
  
1. Idite na stranicu **Odobrenja** i odaberite **Troškovi**, **Vrijeme**, **Utrošeni materijal** ili **Opozivi**.
2. Pregledajte svako odobrenje i odaberite ona koja želite odobriti.
3. Odaberite mogućnost **Odobri** kako bite odobrili odabrane unose.
Sustav obrađuje ove unose i stvara stvarne podatke.

## <a name="reject-an-entry"></a>Odbacivanje unosa
Kao odobravatelj projekta, možda ćete korisniku morati vratiti unos na ispravak.
  
1. Idite na stranicu **Odobrenja** i odaberite unos koji želite odbiti. 
2. Odaberite **Odbaci**.
3. Neobvezno, dodajte komentar u dijaloški okvir **Komentari odbijanja** za obavještavanje korisnika zašto se unos odbija.
4. Odaberite **U redu**. Unos će se vratiti korisniku.
  
## <a name="cancel-approval"></a>Otkazivanje odobrenja
U nekim slučajevima možda ćete trebati otkazati prethodno odobreni unos. Otkazivanje prethodno odobrenog unosa imat će financijski učinak. 

## <a name="approving-recall-requests"></a>Zahtjevi za opoziv odobrenja
U nekim slučajevima savjetnik će možda morati opozvati prethodno odobreni unos. Otkazivanje prethodno odobrenog unosa imat će financijski učinak. Odobritelj projekta mora odobriti opoziv radi poništavanja transakcije u Stvarnim podacima.

## <a name="specify-project-approvers"></a>Određivanje odobravatelja projekta
Svaki projekt ima određeni broj članova projektnog tima. Možete odrediti koji su članovi tima ujedno i odobravatelji projekta.

1. Idite na stranicu **Projekti** i s popisa otvorite projekt.
2. Na kartici **Tim** odaberite člana tima koji će biti odobravatelj projekta, a zatim odaberite **Uredi**.
3. Postavite polje **Odobravatelj projekta** na **Da**.
4. Odaberite **Spremi**.
5. Ponovite korake 2 – 4 kako biste dodali dodatne odobravatelje projekta.

## <a name="configure-the-users-manager"></a>Konfiguriranje upravitelja korisnika

1. Otvorite **Postavke** > **Sigurnost** > **Korisnici**.
2. Odaberite korisnika kojem dodjeljujete upravitelja i u području **Informacije o tvrtki ili ustanovi** odaberite upravitelja s popisa. 
3. Odaberite **Spremi**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
