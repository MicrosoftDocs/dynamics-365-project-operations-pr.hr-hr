---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 12, V3
description: U ovom se članku nalaze informacije o novostima u ažuriranju ažuriranja automatizacije usluga programa Project Service 12, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 28539b2e1331c8509e40aaf771f4d88d6f54e022
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922627"
---
# <a name="project-service-automation-update-release-12-v3"></a>Project Service Automation, izdanje ažuriranja 12, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje za aplikaciju Dynamics 365 Project Service Automation (PSA). Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite Centar za administratore sustava Dynamics 365 na mreži i idite na stranicu s rješenjima kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovom se članku navode značajke i popravci koji su novi ili promijenjeni za automatizaciju projektnih usluga V3, Ažuriraj izdanje 12. Broj izrade ove verzije jest V3.10.2.34, a ona je uglavnom dostupna putem samostalnog ažuriranja u listopadu 2019.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
