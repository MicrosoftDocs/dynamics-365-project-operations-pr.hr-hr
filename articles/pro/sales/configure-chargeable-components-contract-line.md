---
title: Konfiguriranje naplative komponente retka ugovora koji se temelji na projektu – jednostavno
description: U ovoj temi nalaze se informacije o načinu dodavanja naplatnih komponenti u retke ugovora u projektnim operacijama.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b881e03a2bb085c6d7cfccb7eec70442e696e62c
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513870"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Konfiguriranje naplative komponente retka ugovora koji se temelji na projektu – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Redak ugovora koji se temelji na projektu ima *naplative* komponente i *naplative* komponente.

Uključene komponente, komponente su koje podliježu:

  - Način naplate i podjele klijenta
  - Ograničenja koja se ne smiju prekoračiti 
  - Postavke učestalosti fakture definirane u retku ugovora koji se temelji na projektu

Podskup uključenih komponenti može se označiti kao naplativ s pomoću polja **Vrsta naplate**. Polje **Vrsta naplate** skup je mogućnosti koji dopušta sljedeće vrijednosti u kontekstu retka ugovora:

  - Naplativo
  - Nenaplativo

Komponente koje se naplaćuju mogu se definirati u zadacima, ulogama i kategorijama transakcija.

Mogućnost naplate definirana je na zadacima za redak ugovora o projektu i primjenjuje se na sve klase transakcija uključene u redak. Ako je polje **Uključi zadatke** u retku ugovora prazno ili postavljeno na **Cijeli projekt**, kartica **Naplativi zadaci** neće biti dostupna.

Mogućnost naplate definirana u ulogama za redak ugovora o projektu odnosi se samo na klasu transakcije **Vrijeme**. Ako je polje **Uključi vrijeme** u retku ugovora o projektu postavljeno na **Ne**, kartica **Naplative uloge** neće biti dostupna.

Mogućnost naplate definirana je u kategorijama transakcije za redak ugovora o projektu i primjenjuje se samo na klasu transakcije **Trošak**. Ako je polje **Uključi troškove** postavljeno na **Ne**, kartica **Naplative kategorije** neće biti dostupna.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Ažuriranje projektnog zadatka kao naplativog ili nenaplativog

Projektni zadatak može biti naplativ ili nenaplativ u određenom retku ugovora koji omogućuje sljedeće postavljanje:

Ako redak ugovora koji se temelji na projektu uključuje **Vrijeme** i određeni zadatak, **T1** povezan je s njim kao naplativ. Ako postoji drugi redak ugovora koji uključuje stavku **Trošak**, možete povezati zadatak T1 s retkom ugovora kao nenaplativ. Rezultat je da se svo vrijeme zabilježeno na zadatku naplaćuje, dok su svi troškovi nenaplativi.

Vrsta naplate zadatka može se konfigurirati na kartici **Naplativi zadaci** retka ugovora ažuriranjem polja **Vrsta naplate** u podrešetki zadataka retka ugovora. Umjesto toga, možete ažurirati polje **Vrsta naplate** na podrešetki postavke naplate zadatka projekta koja prikazuje retke povezane sa zadatkom.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Ažuriranje uloge kao naplative ili nenaplative

Uloga može biti naplativa ili nenaplativa u određenom retku ugovora.

Vrsta naplate za ulogu može se konfigurirati na kartici **Naplative uloge** retka ugovora. Kako biste to učinili, ažurirajte polje **Vrsta naplate** u podrešetki **Naplative uloge**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Ažuriranje kategorije transakcije kao naplativa ili nenaplativa

Kategorije transakcije može biti naplativa ili nenaplativa na određenom retku ugovora.

Vrsta naplate transakcije može se konfigurirati na kartici **Naplative kategorije** retka ugovora koji se temelji na projektu. Kako biste to učinili, ažurirajte polje **Vrsta naplate** u podrešetki **Naplative kategorije**.

### <a name="resolve-chargeability"></a>Rješavanje naplativosti

Procijenjeno ili stvarno stvoreno vrijeme smatrat će se naplativima samo ako je **Vrijeme** uključeno u redak ugovora i ako su **Zadatak** i **Uloga** konfigurirani kao naplativi u retku ugovora.

Procijenjeni ili stvarno stvoreni trošak smatrat će se naplativim samo ako je **Trošak** uključen u redak ugovora i ako su kategorije **Zadatak** i **Transakcije** u retku ugovora konfigurirani kao naplativi.


| Uključuje Vrijeme | Uključuje Trošak | Uključuje zadatke | Uloga           | Kategorija       | Zadatak                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Jest           | Jest              | Cijeli projekt | Naplativo     | Naplativo     | Naplata stvarnih podataka o Vremenu: **Naplativo** </br> Vrsta naplate stvarnih podataka o Trošku: **Naplativo**           |
| Jest           | Jest              | Odabrani zadaci | Naplativo     | Naplativo     | Naplata stvarnih podataka o Vremenu: **Naplativo** </br> Vrsta naplate stvarnih podataka o Trošku: **Naplativo**           |
| Jest           | Jest              | Odabrani zadaci | Nenaplativo | Naplativo     | Naplata stvarnih podataka o Vremenu: **Nenaplativo** </br> Vrsta naplate stvarnih podataka o Trošku: **Naplativo**       |
| Jest           | Jest              | Odabrani zadaci | Naplativo     | Naplativo     | Naplata stvarnih podataka o Vremenu: **Nenaplativo** </br> Vrsta naplate stvarnih podataka o Trošku: **Nenaplativo** |
| Jest           | Jest              | Odabrani zadaci | Nenaplativo | Naplativo     | Naplata stvarnih podataka o Vremenu: **Nenaplativo** </br> Vrsta naplate stvarnih podataka o Trošku: **Nenaplativo** |
| Jest           | Jest              | Odabrani zadaci | Nenaplativo | Nenaplativo | Naplata stvarnih podataka o Vremenu: **Nenaplativo** </br> Vrsta naplate stvarnih podataka o Trošku: **Nenaplativo** |
| No            | Jest              | Cijeli projekt | Nije moguće postaviti   | Naplativo     | Naplata stvarnih podataka o Vremenu: **Nenaplativo**</br>Vrsta naplate stvarnih podataka o Trošku: **Naplativo**          |
| No            | Jest              | Cijeli projekt | Nije moguće postaviti   | Nenaplativo | Naplata stvarnih podataka o Vremenu: **Nenaplativo**</br> Vrsta naplate stvarnih podataka o Trošku: **Nenaplativo**     |
| Jest           | No               | Cijeli projekt | Naplativo     | Nije moguće postaviti   | Naplata stvarnih podataka o Vremenu: **Naplativo** </br> Vrsta naplate stvarnih podataka o Trošku: **Nenaplativo**        |
| Jest           | No               | Cijeli projekt | Nenaplativo | Nije moguće postaviti   | Naplata stvarnih podataka o Vremenu: **Nenaplativo** </br>Vrsta naplate stvarnih podataka o Trošku: **Nenaplativo**   |
