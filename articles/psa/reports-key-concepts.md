---
title: Ključni koncepti
description: Ova tema pruža informacije o ključnim konceptima za upravljanje resursima u aplikaciji Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 75b2d2c520cc48eb59c266289ca2bdc1288f2920
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147734"
---
# <a name="key-concepts"></a>Ključni koncepti

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tablica u nastavku definira ključne koncepte koji se koriste u aplikaciji Dynamics 365 Project Service Automation.

| Koncept                    | Definicija |
|----------------------------|------------|
| Član projektnog tima        | Kao dio projektnog tima, član projektnog tima može biti imenovani resurs koji ima rezervacije, imenovani resurs koji nema rezervacije ili generički resurs. Generički resursi nemaju rezervacije, lokalno su dodani projektu i nemaju ograničenja kapaciteta u različitim projektima. |
| Generički resurs projekta   | Rezervirano mjesto resursa koje vam omogućuje osmišljavanje plana projekta za tim i osoblje bez imenovanog resursa. Kalendar projekta koristi se kao kalendar generičkog resursa. Generički resursi mogu se dodati u projektni tim i dodijeliti zadacima. |
| Rezervirani sati               | Sati resursa fiksno su rezervirani za projekt kako bi se osigurao dovršetak posla na projektu. Rezervirani sati troše se iz ukupnog kapaciteta resursa. Rezervacije se odnose samo na imenovane resurse, a ne na generičke resurse. |
| Dodijeljeni sati             | Sati resursa dodjeljuju se zadacima u rasporedu projekta. Dodjele mogu biti za imenovane resurse ili generičke resurse. Dodjele mogu biti neovisne o rezervacijama. |
| Potrebni sati             | Kapacitet koji je potreban, ali koji imenovani resurs još nije ostvario. Potrebni sati odnose se samo na generičke članove tima koji su generirali preduvjete resursa. |
| Potražnja                     | Trenutačno i dolazno radno opterećenje. U aplikaciji Project Service Automation potražnja se prikazuje kao preduvjeti resursa ili zahtjevi za resurse. |
| Uvjeti resursa       | Entitet koji služi za bilježenje potrebnih sati, datuma početka i završetka, vještina, geografskih podataka i drugih dimenzija cijena za potrebne resurse. Preduvjeti resursa generiraju se iz članova projektnog tima ili se izrađuju zasebno. |
| Zahtjev za resurs           | Entitet koji služi kao "okvir" za preduvjet resursa koji mora ispuniti upravitelj resursa. |
| Zadana uloga resursa      | Uloga u koju je resurs grupiran za izračun iskorištenosti. Pretpostavlja se da resurs ima potrebne vještine za ulogu i da zadovolji ciljanu iskorištenost za tu ulogu. |
| Organizacijska jedinica resursa | Organizacijska jedinica kojoj je resurs dodijeljen. |
| Kontura                    | Zadatak, preduvjet ili dodijeljeni sati razvrstani po dnevnoj distribuciji. Na primjer, petodnevni zadatak od 40 sati može biti raspodijeljen na osam sati dnevno tijekom pet dana. |
| Prikaz usklađivanja        | Prikaz koji predstavlja rezervacije i dodjele za svakog člana projektnog tima. U ovom prikazu voditelj projekta može provjeriti ima li nepodudaranja između rezervacija i dodjela te poduzeti korektivne radnje ako ih ima. |
| Radno vrijeme                 | Entitet koji služi za identifikaciju kapaciteta resursa te radnih i neradnih sati. Ovaj se entitet naziva i kalendarom resursa. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]