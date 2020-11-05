---
title: Konfiguriranje naplative komponente retka ponude
description: U ovoj temi nalaze se informacije o postavljanju naplativih i nenaplativih komponenti na retku ponude koji se temelji na projektu.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073509"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Konfiguriranje naplative komponente retka ponude

_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_

Redak ponude koji se temelji na projektu ima koncept *uključenih* komponenti i *naplativih* komponenti.

Uključene komponente podliježu:

  - Način naplate i podjele klijenta
  - Ograničenja koja se ne smiju prekoračiti 
  - Postavke učestalosti fakture definirane u retku ponude koji se temelji na projektu

Podskup uključenih komponenti može se označiti kao naplativ s pomoću polja **Vrsta naplate**. Polje **Vrsta naplate** skup je mogućnosti koji dopušta sljedeće vrijednosti u kontekstu retka ponude:

  - Naplativo
  - Nenaplativo

Komponente koje se naplaćuju mogu se definirati u zadacima, ulogama i kategorijama transakcija.

Mogućnost naplate definirana je na zadacima za redak ponude i primjenjuje se na sve klase transakcija uključene u taj redak. Ako je polje **Uključi zadatke** postavljeno na **Cijeli projekt** ili je ostavljeno prazno, kartica **Naplativi zadaci** nije dostupna.

Mogućnost naplate definirana je u ulogama za redak ponude i primjenjuje se samo na klasu transakcije **Vrijeme**. Ako je polje **Uključi vrijeme** postavljeno na **Ne** u retku ponude projekta, kartica **Naplative uloge** nije dostupna.

Mogućnost naplate definirana je u kategorijama transakcije za redak ponude i primjenjuje se samo na klasu transakcije **Trošak**. Ako je polje **Uključi troškove** postavljeno na **Ne** u retku ponude projekta, kartica **Naplative kategorije** nije dostupna.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Ažuriranje projektnog zadatka kako bi bio naplativ ili nenaplativ

Projektni zadatak može biti naplativ ili nenaplativ u kontekstu određenog retka ponude koji se temelji na projektu, što omogućuje sljedeće postavljanje:

Ako redak ponude koji se temelji na projektu uključuje **Vrijeme** i zadatak **T1** , zadatak je povezan s retkom ponude kao naplativ. Ako postoji drugi redak ponude koji uključuje stavku **Troškovi** , možete povezati zadatak **T1** s retkom ponude kao nenaplativ. Rezultat je da se svo vrijeme zabilježeno na zadatku naplaćuje, dok se svi troškovi zabilježeni na zadatku ne naplaćuju.

Vrsta naplate zadatka može se konfigurirati na kartici **Naplativi zadaci** retka ponude koji se temelji na projektu ažuriranjem polja **Vrsta naplate** na podrešetki **Zadaci retka ponude**. Alternativno, možete ažurirati vrstu naplate projektnog zadatka u polju **Vrsta naplate** na podrešetki na postavci naplate zadatka projekta koja prikazuje retke ponude povezane sa zadatkom.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Ažuriranje uloge kako bi bila naplativa ili nenaplativa

Uloga može biti naplativa ili nenaplativa u kontekstu određenog retka ponude koji se temelji na projektu.

Vrsta naplate uloge može se konfigurirati na kartici **Naplative uloge** retka ponude koji se temelji na projektu ažuriranjem polja **Vrsta naplate** na podrešetki **Naplative uloge**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Ažuriranje kategorije transakcije kako bi bila naplativa ili nenaplativa

Kategorije transakcije može biti naplativa ili nenaplativa na određenom retku ponude.

Vrsta naplate transakcije može se konfigurirati na kartici **Naplative kategorije** retka ponude koji se temelji na projektu ažuriranjem polja **Vrsta naplate** na podrešetki **Naplative kategorije**.

### <a name="resolve-chargeability"></a>Rješavanje naplativosti
Procijenjeno ili stvarno stvoreno vrijeme smatrat će se naplativima samo ako je **Vrijeme** uključeno u redak ponude i ako su **Zadatak** i **Uloga** konfigurirani kao naplativi u retku ponude.

Procijenjen ili stvarno stvoren trošak smatrat će se naplativim samo ako je **Trošak** uključen u redak ponude i ako su **Zadatak** i **Kategorija transakcije** konfigurirani kao naplativi u retku ponude.

| Uključuje Vrijeme | Uključuje Trošak | Uključeni zadaci | Uloga | Kategorija | Zadatak | Naplata |
| --- | --- | --- | --- | --- | --- | --- |
| Jest | Jest | Cijeli projekt | Naplativo | Naplativo | Nije moguće postaviti | Naplata za stvarno vrijeme: Naplativo </br>Vrsta naplate na stvarnom trošku: Naplativo |
| Jest | Jest | Samo odabrani zadaci | Naplativo | Naplativo | Naplativo | Naplata za stvarno vrijeme: Naplativo</br>Vrsta naplate na stvarnom trošku: Naplativo |
| Jest | Jest | Samo odabrani zadaci | Nenaplativo | Naplativo | Naplativo | Naplata za stvarno vrijeme: Nenaplativo</br>Vrsta naplate na stvarnom trošku: Naplativo |
| Jest | Jest | Samo odabrani zadaci | Naplativo | Naplativo | Nenaplativo | Naplata za stvarno vrijeme: Nenaplativo</br> Vrsta naplate na stvarnom trošku: Naplativo |
| Jest | Jest | Samo odabrani zadaci | Nenaplativo | Naplativo | Nenaplativo | Naplata za stvarno vrijeme: Nenaplativo</br> Vrsta naplate na stvarnom trošku: Naplativo |
| Jest | Jest | Samo odabrani zadaci | Nenaplativo | Nenaplativo | Naplativo | Naplata za stvarno vrijeme: Nenaplativo</br> Vrsta naplate na stvarnom trošku: Naplativo |
| No | Jest | Cijeli projekt | Nije moguće postaviti | Naplativo | Nije moguće postaviti | Naplata za stvarno vrijeme: Nenaplativo </br>Vrsta naplate na stvarnom trošku: Naplativo |
| No | Jest | Cijeli projekt | Nije moguće postaviti | Nenaplativo | Nije moguće postaviti | Naplata za stvarno vrijeme: Nenaplativo </br>Vrsta naplate na stvarnom trošku: Nenaplativo |
| Jest | No | Cijeli projekt | Naplativo | Nije moguće postaviti | Nije moguće postaviti | Naplata za stvarno vrijeme: Naplativo</br>Vrsta naplate na stvarnom trošku: Nenaplativo |
| Jest | No | Cijeli projekt | Nenaplativo | Nije moguće postaviti | Nije moguće postaviti | Naplata za stvarno vrijeme: Nenaplativo </br>Vrsta naplate na stvarnom trošku: Nenaplativo |
