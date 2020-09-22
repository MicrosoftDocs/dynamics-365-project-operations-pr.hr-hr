---
title: Novosti u aplikaciji Project Service Automation, izdanje ažuriranja 12, V3
description: Ova tema pruža informacije o novostima u aplikaciji Project Service Automation, izdanje ažuriranja 12, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750125"
---
# <a name="project-service-automation-v3-update-release-12"></a>Project Service Automation V3, izdanje ažuriranja 12
Zadovoljstvo nam je najaviti najnovije ažuriranje za aplikaciju Dynamics 365 Project Service Automation (PSA). Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite Centar za administratore sustava Dynamics 365 na mreži i idite na stranicu s rješenjima kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 12. Broj izrade ove verzije jest V3.10.2.34, a ona je uglavnom dostupna putem samostalnog ažuriranja u listopadu 2019.

## <a name="update-release-12"></a>Izdanje ažuriranja 12

### <a name="bug-fixes"></a>Ispravke pogrešaka

- Vrijeme i trošak

    - Popravljeno: Poruka o pogrešci pri unosu vremena ažurirana je s pomoću relevantnijeg konteksta.
    - Popravljeno: Raspored i rešetka unosa vremena ispravno prikazuju vertikalnu traku za pomicanje kada je to potrebno.
    - Popravljeno: Poslani troškovi i Unos vremenai mogu se odobriti.
    - Popravljeno: Otkazivanje dijaloške poruke o potvrdi odobrenja ispravljeno je tako da odražava status odobrenja kada je promijenjen iz mogućnosti **Odobren** u **Poslan**.
    - Popravljeno: Polja **Cijena**, **Jedinica** i **Količina** sada su zaključana u zapisu troška nakon odobravanja.

- Upravljanje projektom

    - Popravljeno: Uklonjena je radnja **Novo** u glavnom obrascu stavke **Član tima**.
    - Popravljeno: Dodijele resursa ažurirane su kako bi se evidentirale netočne pogreške u zaokruživanju, koje dovode do pomicanja datuma završetka zadatka.
    - Popravljeno: Korisniku će se u rešetki zadataka prikazati relevantne pogreške na strani poslužitelja.
    - Popravljeno: U biraču osoba za izvršenje zadataka, umjesto naziva položaja sada se prikazuje ime člana tima.

- Upravljanje resursima

    - Popravljeno: Pojedinosti o preduvjetima resursa za projekte stvorene iz predloška sada upotrebljavaju kalendar projekta.
    - Popravljeno: Vještine i kompetencije sada su zadane od glavnih podataka uloga do preduvjeta resursa stvorenih za tu ulogu.

- Sales

    - Popravljeno: Dvostruki ID-i objekata pronađeni na obrascu **Glavni ugovor**.
    - Popravljeno: Ažurirana je logika tako da kartica **Analiza ponude** bude vidljiva i prikazuje postavke metapodataka kartice.
    - Popravljeno: Datum obračuna na stvarnoj evidenciji sada potječe od datuma unosa vremena/troška, a ne od datuma odobrenja.
