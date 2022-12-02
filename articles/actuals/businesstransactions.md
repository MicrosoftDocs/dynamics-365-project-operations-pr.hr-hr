---
title: Poslovne transakcije u aplikaciji Project Operations
description: U ovom se članku navodi pregled koncepta poslovnih transakcija u aplikaciji Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923271"
---
# <a name="business-transactions-in-project-operations"></a>Poslovne transakcije u aplikaciji Project Operations

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U aplikaciji Microsoft Dynamics 365 Project Operations, *poslovna transakcija* je apstraktni koncept kojeg niti jedan entitet ne predstavlja. Međutim, neka uobičajena polja i procesi na entitetima osmišljeni su za korištenje koncepta poslovnih transakcija. Sljedeći entiteti koriste ovu apstrakciju:

- Detalji retka ponude
- Detalji retka ugovora
- Reci procjene
- Reci u dnevniku
- Stvarne vrijednosti

Od tih entiteta, Pojedinosti retka ponude, Pojedinosti retka ugovora i Redci procjene mapiraju se u *fazu procjene* u životnom ciklusu projekta. Redci dnevnika i Entiteti stvarnih podataka mapiraju se u *fazu izvršavanja* u životnom ciklusu projekta.

Aplikacija Project Operations tretira zapise u svim od tih pet entiteta kao poslovne transakcije. Jedina je razlika u tome što se zapisi u entitetima koji su mapirani u fazu procjene (Pojedinosti retka ponude, Pojedinosti retka ugovora i Redci procjene) smatraju *financijskim prognozama*, dok se zapisi u entitetima koji su mapirani u fazu izvršenja (Redci dnevnika i Stvarni podaci) smatraju *financijskim činjenicama* koje su se već dogodile.

Za dodatne informacije, pogledajte [Procjene](../project-management/estimating-projects-overview.md) i [Stvarne vrijednosti](actuals-overview.md)

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepti koji su jedinstveni za poslovne transakcije

Sljedeći koncepti jedinstveni su za koncept poslovnih transakcija:

- Vrsta transakcije
- Razred transakcije
- Porijeklo transakcije
- Veza transakcije

### <a name="transaction-type"></a>Vrsta transakcije

Vrsta transakcije predstavlja vrijeme i kontekst financijskog učinka na projekt. Definira se skupom mogućnosti koji ima sljedeće podržane vrijednosti u aplikaciji Project Operations:

- Cijena
- Ugovor o projektu
- Nenaplaćene prodaje
- Naplaćene prodaje
- Međuorganizacijska prodaja
- Jedinična cijena resursa

### <a name="transaction-class"></a>Razred transakcije

Razred transakcije predstavlja različite vrste troškova nastalih na projektima. Definira se skupom mogućnosti koji ima sljedeće podržane vrijednosti u aplikaciji Project Operations:

- Vrijeme
- Izdatak
- Materijal
- Naknada
- Kontrolna točka
- Porez

> [!NOTE]
> Vrijednost **Kontrolna točka** obično upotrebljava poslovna logika za naplatu fiksne cijene u aplikaciji Project Operations.

### <a name="transaction-origin"></a>Porijeklo transakcije

Izvor transakcije entitet je koji pohranjuje podatke o izvoru svake poslovne transakcije radi lakšeg izvješćivanja i praćenja. Početkom izvršavanja projekt svaka poslovna transakcija izrađuje još jednu poslovnu transakciju koja će zauzvrat izraditi sljedeću poslovnu transakciju i tako dalje.

### <a name="transaction-connection"></a>Veza transakcije

Transakcijska veza entitet je koji pohranjuje odnos između dviju sličnih poslovnih transakcija, kao što su troškovi i povezani prodajni stvarni podaci ili preokreti transakcija koje pokreću aktivnosti naplate kao što su potvrda fakture ili ispravci fakture.

Zajedno, entiteti Porijeklo transakcije i Veza transakcije pomažu vam da pratite odnose između poslovnih transakcija i radnji koje su uzrokovale izradu određene poslovne transakcije.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
