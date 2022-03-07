---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 24, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 24, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 51d08dd147b7804cb5c9255159aeab2ecd94f4597d6e99c5fa92efe1246c44d0
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998047"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation, izdanje ažuriranja 24, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 24. Broj izrade ove verzije jest V 3.10.42.43, a ona je uglavnom dostupna putem samostalnog ažuriranja u listopadu 2020.

## <a name="update-release-24"></a>Izdanje ažuriranja 24

### <a name="bug-fixes"></a>Ispravke pogrešaka

**Sales**

Popravljeni su sljedeći problemi:

- Problem tijekom postavljanja zadanog cjenika proizvoda.
- Izvršavanje dobivenih ponuda sporo je zbog ugrađenog cjenika i kopija zapisa cijena uloga.
- **Ugovor o projektu / prodajno središte** > **Stavka retka proizvoda / količina retka narudžbe** automatski se zaokružuje na najbliži cijeli broj.
- Tijekom čitanja cjenika podignite do povlastica sustava.
- Kopirajte polja adrese klijenta **address1_freighttermscode** i **address1_shippingmethodcode** u ponudu / narudžbu. 


**Vrijeme i trošak**

Popravljeni su sljedeći problemi:

- **Rešetka za unos vremena** ne podržava reakciju vremena **Samo datum**.
- **Vremenski unos** ne osvježava se automatski. Potrebno je ručno osvježavanje.
- Nije moguće uvesti vremenske unose iz zadatka kada postoji prekid (0 sati) u zadacima resursa.
- Kada stvarate vremenski unos, postavite početak na isto kao **msdyn_date**.
- Ponovno omogućite skupno uređivanje za vremenski unos.

**Upravljanje resursima**

Popravljeni su sljedeći problemi:

- Pokušaj ažuriranja statusa rezervacije unutar dana bez zahtjeva izbacit će iznimku null-ref.
- Pogreška pri učitavanju mogućnosti **Prikaz usklađivanja**.


**Upravljanje projektom**

Popravljeni su sljedeći problemi:

- U mogućnosti **Raspored projekta**, pri promjeni iz **Ručno** u **Automatski**, automatsko se spremanje ne dovršava.
- Troškovi izdatka ne bi se trebali računati prema odstupanjima na stavci **Rešetka za praćenje projekata**.
- Nedosljedno ponašanje stupaca **Oznaka procjena** tijekom opterećenja naspram promjene vrste **Vremenska faza**.
- Stvarni trošak projekta možda neće odražavati ukupne iznose iz mogućnosti **Stvarni podaci**.
- **Procijenjeni datum završetka** na kartici **Sažetak** ne podudara se sa stavkom **SAR raspored**.
- **Ažuriranje stvarnih sati** na outdent ne radi ispravno.
- Voditelj projekta izvan korijena **BU** ne može stvoriti projekt.
- Promjene u zadatku ili kategoriji u stavci **Procjene troškova** nisu ostale.
- **Kopija ugovora** kopira rasporede faktura i status pokretanja.
- Gumb **Osvježi stvarne podatke** pogrešno izračunava sažetke zadataka.
- Dodatak za aplikaciju Microsoft Project: Ispravite pogrešku reference nule ako neki član tima ima praznu jedinicu resursa.



[!INCLUDE[footer-include](../includes/footer-banner.md)]