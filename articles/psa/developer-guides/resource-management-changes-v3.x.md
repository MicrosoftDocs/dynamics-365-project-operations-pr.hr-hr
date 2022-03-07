---
title: Promjene upravljanja resursima (Project Service Automation 3.x)
description: Ovaj tema sadrži informacije o promjenama u području upravljanja resursima.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: bc293e7686b7fd7d50d232cb8b26bfc03eb29c8911b52536d2b0a3a4929730c9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000297"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Promjene upravljanja resursima (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Odjeljci ove teme sadrže informacije o promjenama koje su uvedene u području upravljanja resursima verzije 3.x aplikacije Dynamics 365 Project Service Automation.

## <a name="project-estimates"></a>Procjene projekta

Umjesto entiteta **msdyn\_projecttask** (**Projektni zadatak**), procjene projekta temelje se na entitetu **msdyn\_resourceassignment** (**Dodjela resursa**). Dodjele resursa postale su "izvor podataka" za planiranje zadataka i određivanje cijena.

## <a name="line-tasks"></a>Zadaci retka

U aplikaciji PSA 3.x zadaci retka su zastarjeli (obustavljeni). Dodjele više ne ukazuju na zadatke retka, već na cijeli zadatak.

Primjer u nastavku pokazuje kako se zadatak koji se zove "Probni zadatak" dodjeljuje članovima tima A i B u ranijim verzijama aplikacije PSA i u aplikaciji PSA 3. x.

- **Prije PSA 3.x:**

    - Probni zadatak

        - Probni zadatak – zadatak retka 1

            - Dodjela u tim A

        - Probni zadatak – zadatak retka 2

            - Dodjela u tim B

- **PSA 3.x:**

    - Probni zadatak

        - Dodjela u tim A
        - Dodjela u tim B

## <a name="unassigned-assignment"></a>Nedodijeljena dodjela

U aplikaciji PSA 3. x nedodijeljena dodjela je dodjela koja je dodijeljena članu tima **NULL** i resursu **NULL**. Nedodijeljene dodjele mogu se pojaviti u nekoliko scenarija:

- Ako je zadatak izrađen, ali još nije dodijeljen članu tima, uvijek se stvara nedodijeljena dodjela. 
- Ako se uklone svi primatelji u zadatku, za taj zadatak će se ponovno izraditi nedodijeljena dodjela.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Polja rasporeda u entitetu Projektni zadatak

Polja u entitetu **msdyn\_projecttask** obustavljena su ili premještena u entitet **msdyn\_resourceassignment** ili su sada povezana referencom iz entiteta **msdyn\_projectteam** (**Član projektnog tima**).

| Obustavljeno polje u entitetu msdyn\_projektnom zadatku (Projektni zadatak) | Novo polje u entitetu msdyn\_resourceassignment (Dodjela resursa) | Komentar |
|---|---|---|
| msdyn\_assignedresources | Nema | |
| msdyn\_assignedteammembers | Nema | |
| msdyn\_numberofresources | Nema | |
| msdyn\_scheduledhours | Nema | |
| msdyn\_effortcontour | msdyn\_plannedwork | Promijenjen je format podatkovne strukture JavaScript Object Notation (JSON) koja je spremljena u polju. |

## <a name="schedule-contour"></a>Kontura rasporeda

Kontura rasporeda spremljena je u polju **Planirani rad** (**msdyn\_plannedwork**) svakog entiteta **Dodjela resursa** (**msdyn\_resourceassignment**).

### <a name="structure"></a>Struktura

Nova struktura konture rasporeda sastoji se od fleksibilnih isječaka vremena definiranih za svaki dan u rasporedu. Svaki isječak vremena ima sljedeća svojstva:

- **Početak** – početak radnog vremena na određeni dan, prema kalendaru projekta.
- **Kraj** – kraj radnog vremena na određeni dan, prema kalendaru projekta.
- **Sati** – broj sati koji su dodijeljeni određeni dan.

**Primjer**

Za ovaj se primjer koristi kalendar projekta u kojem je radni dan od 9:00 do 17:00 u vremenskoj zoni UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Automatsko zakazivanje i ručno zakazivanje

Ako je zadatak automatski zakazan, sati su unaprijed učitani, a trajanje zadatka može se skratiti.

**Primjer**

Sljedeći zadatak automatski je zakazan na 18 sati tijekom tri dana (od 3. do 5. prosinca 2018.).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Ako je zadatak ručno zakazan, sati su ravnomjerno raspoređeni po svim danima.

**Primjer**

Sljedeći zadatak ručno je zakazan na 18 sati tijekom tri dana (od 3. do 5. prosinca 2018.).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Jedinica dodjele

Jedinica dodjele je obustavljena je u aplikaciji PSA 3.x. Sati rada za zadatak sada su podjednako podijeljeni po danu među svim dodijeljenim resursima.

**Primjer**

U ovom primjeru zadatak je dodijeljen dvama resursima i automatski je zakazan na 36 sati tijekom tri dana (od 3. do 5. prosinca 2018.).

- Dodjela 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Dodjela 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Dimenzije cijena

U aplikaciji PSA 3.x polja dimenzija cijena prema resursu (kao što su **Uloga** i **Organizacijska jedinica**) uklonjena su iz entiteta **msdyn\_projecttask**. Ta se polja sada mogu dohvatiti iz odgovarajućeg člana projektnog tima **(msdyn\_projectteam**) dodjele resursa (**msdyn\_resourceassignment**) kad se generiraju procjene projekta. Novo polje **, msdyn\_organizationalunit**, dodano je u entitet **msdyn\_projectteam**.

| Obustavljeno polje u entitetu msdyn\_projektnom zadatku (Projektni zadatak) | Polje iz entiteta msdyn\_projectteam (Član projektnog tima) koje se upotrebljava umjesto njega |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Konture

Polja konture cijena i procjene obustavljena su u entitetu **msdyn\_projecttask**. Premještena su u entitet **msdyn\_resourceassignment**.

| Obustavljeno polje u entitetu msdyn\_projektnom zadatku (Projektni zadatak) | Novo polje u entitetu msdyn\_resourceassignment (Dodjela resursa) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Polja u nastavku dodana su u entitet **msdyn.\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Sljedeća polja za planirani, stvarni i preostali trošak i prodaju ostaju ista u entitetu **msdyn\_projecttask**:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]