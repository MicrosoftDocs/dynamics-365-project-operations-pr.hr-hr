---
title: Poslovne transakcije u projektnim operacijama
description: Ovaj tema daje pregled koncepta poslovnih transakcija u Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582195"
---
# <a name="business-transactions-in-project-operations"></a>Poslovne transakcije u projektnim operacijama

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U programu Microsoft Dynamics 365 Project Operations poslovna *transakcija* apstraktni je koncept koji ne predstavlja nijedan entitet. Međutim, neka uobičajena polja i procesi na entitetima osmišljeni su za korištenje koncepta poslovnih transakcija. Sljedeći entiteti koriste ovu apstrakciju:

- Detalji retka ponude
- Detalji retka ugovora
- Reci procjene
- Reci u dnevniku
- Stvarne vrijednosti

Od tih entiteta detalji retka ponude, detalji retka ugovora i reci procjene mapiraju se *u fazu* procjene u životnom ciklusu projekta. Reci temeljnice i entiteti Stvarni podaci mapirani su u *fazu* izvršenja u životnom ciklusu projekta.

Project Operations tretira zapise u svih pet tih entiteta kao poslovne transakcije. Jedina razlika je u tome što se zapisi u entitetima koji su mapirani u fazu procjene (detalji retka ponude, detalji retka ugovora i reci procjene) smatraju financijskim predviđanjima *, dok se* zapisi u entitetima koji su mapirani u fazu izvršenja (reci temeljnice i stvarni podaci) smatraju *financijskim činjenicama* koje su se već dogodile.

Za dodatne informacije, pogledajte [Procjene](../project-management/estimating-projects-overview.md) i [Stvarne vrijednosti](actuals-overview.md)

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepti koji su jedinstveni za poslovne transakcije

Sljedeći koncepti jedinstveni su za koncept poslovnih transakcija:

- Vrsta transakcije
- Razred transakcije
- Porijeklo transakcije
- Veza transakcije

### <a name="transaction-type"></a>Vrsta transakcije

Vrsta transakcije predstavlja vrijeme i kontekst financijskog učinka na projekt. Definiran je skup mogućnosti koja ima sljedeće podržane vrijednosti u operacijama projekta:

- Cijena
- Ugovor o projektu
- Nenaplaćene prodaje
- Naplaćene prodaje
- Međuorganizacijska prodaja
- Jedinična cijena resursa

### <a name="transaction-class"></a>Razred transakcije

Razred transakcije predstavlja različite vrste troškova nastalih na projektima. Definiran je skup mogućnosti koja ima sljedeće podržane vrijednosti u operacijama projekta:

- Vrijeme
- Izdatak
- Materijal
- Naknada
- Kontrolna točka
- Porez

> [!NOTE]
> Vrijednost **ključne etape** obično se koristi poslovnom logikom za naplatu s fiksnom cijenom u operacijama projekta.

### <a name="transaction-origin"></a>Porijeklo transakcije

Podrijetlo transakcije je subjekt koji pohranjuje podrijetlo svake poslovne transakcije kako bi pomogao u izvješćivanju i sljedivosti. Kako započinje izvršenje projekta, svaka poslovna transakcija stvara drugu poslovnu transakciju koja će zauzvrat stvoriti drugu poslovnu transakciju i tako dalje.

### <a name="transaction-connection"></a>Veza transakcije

Transaction connection je subjekt koji pohranjuje odnos između dvije slične poslovne transakcije, kao što su troškovi i povezani podaci o prodaji ili storniranje transakcija koje pokreću aktivnosti naplate, kao što su potvrda fakture ili ispravci fakture.

Entiteti povezivanja s podrijetlom transakcije i transakcijom zajedno vam pomažu u praćenju Odnosi između poslovnih transakcija i akcija koje su uzrokovale kreiranje određene poslovne transakcije.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
