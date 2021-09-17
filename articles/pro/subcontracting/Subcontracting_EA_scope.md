---
title: Podugovaranje u listopadu 2021., izdanje Ranog pristupa
description: U ovoj temi nalazi se pregled mogućnosti podugovaranja u aplikaciji Project Operations koje su dio izdanja ranog pristupa u listopadu 2021. godine.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383686"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Podugovaranje u listopadu 2021., izdanje Ranog pristupa

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

U ovoj temi nalazi se pregled mogućnosti podugovaranja u aplikaciji Dynamics 365 Project Operations koje su dio izdanja ranog pristupa u listopadu 2021. godine. Ovaj skup značajki nije spreman za proizvodno okruženje ili ono koje ide uživo, pa će te značajke ostati u izdanju za rani pristup sve dok se ne objavi cijeli skup značajki. Preporučujemo da ne upotrebljavate skup značajki podugovaranja za proizvodne scenarije koji idu uživo sve dok se natpis pretpregleda ne ukloni. 

Popis u nastavku pregled je onoga što je trenutačno dostupno u izdanju za rani pristup u listopadu 2021.:

1. Voditelj projekta sklapa podugovor s dobavljačem. Prema zadanim postavkama, cjenici koji su priloženi zapisu o dobavljaču upotrebljavaju se za podugovor. Račun dobavljača ima vrstu odnosa **Dobavljač** ili **Isporučitelj**.

2. Voditelj projekta može sve kupnje specificirati kao stavke retka na podugovoru. Redci podugovora mogu se odnositi na vrijeme, troškove ili proizvode. Klasa transakcije retka podugovora određuje čemu taj redak služi.

3. Voditelj računa dobavljača i voditelj projekta mogu ponavljati podugovor. U nabavnim cjenicima priloženim podugovoru cijene se mogu prilagoditi.

4. U ovom trenutku ili kasnije u postupku, ako je redak podugovora za vrijeme, upravitelj računa dobavljača povezuje kontakte dobavljača sa svakim retkom podugovora. Ova povezanost pruža informacije voditelju projekta koji radi na podugovoru. Kad je kontakt dobavljača povezan s retkom podugovora, sustav iz kontakta automatski stvara kontakt koji se može rezervirati, ako resurs koji se može rezervirati već ne postoji.

5. Način naplate na svakom retku podugovora može biti **Fiksna cijena** ili **Vrijeme i materijal**. Za retke podugovora s fiksnom cijenom postavljen je raspored faktura koji se temelji na kontrolnim točkama.

Preostali koraci u tijek poslovnog procesa za podugovaranje koji su navedeni u Pregledu trenutačno nisu dostupni. S dodavanjem nove funkcionalnosti, ova će se tema ažurirati. 

Ilustracija u nastavku predstavlja izdanje Ranog pristupa podugovaranja u usporedbi s cjelokupnim poslovnim procesom.

![Tijek postupka podugovaranja](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Izdanje ranog pristupa redaka podugovora koji se temelje na količini i redaka podugovora koji se temelje na radu
U izdanju Ranog pristupa za listopad 2021. podržani su samo redci podugovora koji se temelje na količini. To znači da se redak podugovora može upotrebljavati za kupnju vremena, troškova ili materijala od dobavljača, ali ne i za cijelu ukupnost rada. To također znači da se količina koja se kupuje (jedinice vremena, troškova ili količine materijala) na retku podugovora može upotrebljavati za svaki projekt u sustavu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
