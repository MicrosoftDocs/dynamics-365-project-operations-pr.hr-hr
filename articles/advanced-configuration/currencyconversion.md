---
title: Postavljanje pretvorbe valuta da biste izračunali prodajne cijene iz stopa troškova
description: U ovom se članku objašnjava kako konfigurirati ponašanje pretvorbe valuta koje će se koristiti u Microsoftu Dynamics 365 Project Operations kada se prodajne transakcije generiraju iz transakcija troškova.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816687"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Postavljanje pretvorbe valuta da biste izračunali prodajne cijene iz stopa troškova

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U Microsoftu Dynamics 365 Project Operations se prodajne cijene za kategorije troškova mogu postaviti kao numeričke vrijednosti ili se mogu postaviti tako da se izračunavaju na temelju nastalog troška.

Kada su postavljeni tako da se izračunavaju na temelju nastalog troška, dostupne su sljedeće mogućnosti:

- Uz trošak
- Označite postotak iznad troška

U scenarijima u kojima je trošak troška nastao u valuti koja se razlikuje od prodajne valute za ugovor o projektu, pretvorba valute potrebna je za izračun prodajne cijene na temelju troška.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Ponašanje pretvorbe valuta koje koristi nativne Dataverse tečajeve

Prema zadanim postavkama, Project Operations koristi tečajeve valute pohranjene u tablici Valuta u sustavu Dataverse. Da biste konfigurirali operacije projekta tako da koriste nativne tečajeve za izračunavanje prodajnih cijena od troška, slijedite ove korake.

1. Otvorite Parametri **postavki \> operacija \> projekta**.
1. Otvorite stranicu s **detaljima o parametru** projekta.
1. Postavite logičko **polje** pretvorbe valute na praznu vrijednost.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Ponašanje pretvorbe valuta koje koristi tečajeve iz financijskih i operativnih aplikacija

Tečajevi u tablici Valuta koja je izvorno dostupna u Dataverse sustavu ne stupaju na snagu datumom. Stoga se možda neće uvijek skalirati na zahtjeve koje imate za izračun prodajnih cijena iz cijena troškova.

Tečajeve iz financijskog i operativnog okruženja možete koristiti za izračunavanje prodajne cijene u prodajnoj valuti iz tečaja u valuti troška. Da biste konfigurirali ovo ponašanje pretvorbe valuta, slijedite ove korake.

1.  **Na stranici Parametri** projekta dodajte polje logike **pretvorbe valute** . Zatim spremite i objavite prilagodbu.
1. Otvorite Parametri **postavki \> operacija \> projekta**.
1. Otvorite stranicu s **detaljima o parametru** projekta. 
1. Postavite polje ponašanja **pretvorbe** valute na **Prošireno s rezervnom pozadinom na zadano**.
1. Dajte **korisniku**  aplikacije s dvostrukim pisanjem sigurnosna uloga **Global Read** dopuštenje za sljedeće tablice:

    - msdyn\_ currencyexchangerates
    - msdyn\_ currencyexchangeratepairs
    - msdyn\_ exchangeratetypes

1. U financijskom i operativnom okruženju pokrenite sljedeće karte s dvostrukim pisanjem s početnom sinkronizacijom:

    - Vrsta tečaja (msdyn\_ exchangeratetypes)
    - Par deviznih tečajeva (msdyn\_ valutaexchangeratepairs)
    - Tečajevi CDS-a (msdyncurrencyexchangerates\_)

Nakon što se te promjene završe, dual-write će učiniti tečajeve iz financijskog i operativnog okruženja dostupnima u Dataverse. Project Operations će zatim koristiti te tečajeve za pretvaranje troškovnih tečajeva u prodajnu valutu ugovora.

> [!NOTE]
> Ovo ponašanje konverzije valute primjenjuje se samo na izračun prodajnih cijena iz stopa troškova. Neće se koristiti za generički izračunavanje vrijednosti osnovne valute. Vrijednosti osnovne valute uvijek će koristiti izvorne Dataverse tečajeve, bez obzira na to jeste li dovršili ovaj postupak.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
