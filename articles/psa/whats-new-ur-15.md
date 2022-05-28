---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 15, V3
description: Ova tema pruža informacije o novostima u aplikaciji Project Service Automation, izdanje ažuriranja 15, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 26b9ee0a6ff1ad81d6c77a6a7091733667c493ff
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585139"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation, izdanje ažuriranja 15, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje za aplikaciju Dynamics 365 Project Service Automation (PSA). Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite Centar za administratore sustava Dynamics 365 na mreži i idite na stranicu s rješenjima kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji PSA V3, izdanje ažuriranja 15. Broj izrade ove verzije jest V3.10.5.28, a ona je uglavnom dostupna putem samostalnog ažuriranja u siječnju 2020.

## <a name="update-release-15"></a>Izdanje ažuriranja 15 

### <a name="enhancements"></a>Poboljšanja

- Upravljanje projektom

### <a name="bug-fixes"></a>Ispravke pogrešaka

- Vrijeme i trošak

  - Popravljeno: Dodavanje upravljanja pogreškama u tijeku u prikazu usklađivanja.
  - Popravljeno: Središte resursa projekta: Preimenujte stavku **Količina** kako biste smanjili nejasnoće.
  - Popravljeno: Prilagodite prikaz **Kopiraj stupce unosa vremena** kako bi obuhvaćao vrstu.
  - Popravljeno: Uređivanje trajanja unosa vremena u prikazu rešetke s pomoću decimalnih brojeva stvara nepoznatu pogrešku za neke brojeve.

- Upravljanje projektom

  - Popravljeno: Padajući izbornik mogućnosti **Upotrijebi u prikazu praćenja** sada se proširuje na temelju širine mogućnosti.
  - Popravljeno: Kada upravljate projektima u vremenskoj zoni +13, proračuni zadataka mogu prikazati netočne rezultate.
  - Popravljeno: Mogućnost **Vrijeme završetka za člana tima** ispravljeno je u slučaju uporabe 24-satnog kalendara.
  - Popravljeno: Ponovno je aktivirana mogućnost **BPF** u glavnom obrascu **msdyn_project**.
  - Popravljeno: Izračuni dodjela više ne zanemaruju jedan dan.
  - Popravljeno: Novi natpis obavijesti dodan je obrascu projekta kada se vremenska zona korisnika i projekta razlikuje.

- Sales

  - Popravljeno: Pretraživanje kategorije procjene troškova može se upotrebljavati za filtriranje duplikata.
  - Popravljeno: Kod u stavci **PluginDomain.ExecuteInTryCatchBlock(..)** više ne skriva izvorište iznimke.
  - Popravljeno: Više se ne prikazuje poruka o pogrešci u stavci **Pretraživanje projekta** u obrascu **Redak ponude** kada ima više od 1000 projekata.
  - Popravljeno: Rešetka za procjenu rada i troškova **Procjene** sada prikazuje točan simbol valute.
  - Popravljeno: Nakon što tvrtka ili ustanova ažurira PSA s izdanja ažuriranja 14 u izdanje ažuriranja 15, kartica **Raspored** više se ne prikazuje prazna u obrascu **Projekt**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
