---
title: Pregled odobrenja
description: U ovoj temi nalaze se informacije o radu s odobrenjima u aplikaciji Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073248"
---
# <a name="approvals-overview"></a>Pregled odobrenja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Slanja vremena i troška kreću se kroz tijek rada odobrenja. Nakon odobrenja unosa, transakcije se bilježe u stvarnim podacima ili se vrijeme rezervira u rasporedu.

## <a name="approvals-workflow"></a>Tijek rada odobrenja
Kada stvarate i šaljete unos vremena ili troška, stvara se unos odobrenja. Odobravatelj projekta ili vaš upravitelj pregledava i odobrava vaš unos. Ako se unos odnosi na projekt, kada se odobri, stvorit će se stvarni podaci. To omogućuje praćenje troškova i naplate. 

## <a name="approve-an-entry"></a>Odobravanje unosa
Obrazac **Odobrenja** omogućuje vam prebacivanje između različitih prikaza kako biste mogli vidjeti različite vrste odobrenja.
  
1. Idite na obrazac **Odobrenja** i odaberite mogućnost **Troškovi** , **Vrijeme** ili **Storniranja**.
2. Pregledajte svako odobrenje i odaberite ona koja želite odobriti.
3. Odaberite mogućnost **Odobri** kako bite odobrili odabrane unose.
Sustav će obraditi te unose i stvoriti stvarne podatke ili rezervaciju.

## <a name="reject-an-entry"></a>Odbacivanje unosa
Kao odobravatelj projekta, možda ćete korisniku morati vratiti unos na ispravak.
  
1. Idite na obrazac **Odobrenja** i odaberite unos koji želite odbaciti. 
2. Odaberite **Odbaci**.
3. Neobvezno – Dodajte komentar u dijaloški okvir **Komentari odbacivanja** kako biste obavijestili korisnika zašto se unos odbacuje.
4. Odaberite **U redu**. Unos će se vratiti korisniku.
  
## <a name="recall-entries"></a>Storniranje unosa
U jednom trenutku, možda ćete morati stornirati poslani unos. Ako unos nije odobren, odmah će se vratiti. No, odobreni unos može imati materijalni utjecaj. Odobravatelj projekta mora odobriti storniranje kako bi se poništila transakcija u stvarnim podacima.

## <a name="specify-project-approvers"></a>Određivanje odobravatelja projekta
Svaki projekt ima određeni broj članova projektnog tima. Možete odrediti koji su članovi tima ujedno i odobravatelji projekta.

1. Idite na obrazac **Projekti** i otvorite projekt s popisa.
2. Na kartici **Tim** odaberite člana tima koji će biti odobravatelj projekta, a zatim odaberite **Uredi**.
3. Postavite polje **Odobravatelj projekta** na **Da**.
4. Odaberite **Spremi**.
5. Ponovite korake 2 – 4 kako biste dodali dodatne odobravatelje projekta.

## <a name="configure-the-users-manager"></a>Konfiguriranje upravitelja korisnika

1. Otvorite **Postavke** > **Sigurnost** > **Korisnici**.
2. Odaberite korisnika kojem dodjeljujete upravitelja i u području **Informacije o tvrtki ili ustanovi** odaberite upravitelja s popisa. 
3. Odaberite **Spremi**.


