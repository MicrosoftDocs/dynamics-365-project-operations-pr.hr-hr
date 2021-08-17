---
title: Upravljanje podugovorima u aplikaciji Project Operations
description: U ovoj temi nalazi se pregled cjelovitog postupka upravljanja podugovorima u aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994222"
---
# <a name="subcontract-management-in-project-operations"></a>Upravljanje podugovorima u aplikaciji Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Podugovaranje u aplikaciji Microsoft Dynamics 365 Project Operations podržava sljedeći tijek poslovnog procesa.

![Tijek postupka podugovaranja](../media/SubcontractingProcessFlow.png)

Evo podrobnog opisa procesa podugovaranja.

1. Voditelj projekta sklapa podugovor s dobavljačem. Prema zadanim postavkama, cjenici koji su priloženi zapisu o dobavljaču upotrebljavaju se za podugovor. Račun dobavljača ima vrstu odnosa **Dobavljač** ili **Isporučitelj**.
2. Voditelj projekta može sve kupnje specificirati kao stavke retka na podugovoru. Redci podugovora mogu se odnositi na vrijeme, troškove ili proizvode. Klasa transakcije koja je odabrana na svakom retku podugovora određuje čemu taj redak služi.
3. Voditelj računa dobavljača i voditelj projekta mogu ponavljati podugovor. U nabavnim cjenicima priloženim podugovoru cijene se mogu prilagoditi.
4. U ovom trenutku ili kasnije u postupku, ako je redak podugovora za vrijeme, upravitelj računa dobavljača povezuje kontakte sa svakim retkom podugovora. Ova povezanost pruža informacije voditelju projekta koji radi na podugovoru. Kad je kontakt povezan s retkom podugovora, sustav iz kontakta automatski stvara kontakt koji se može rezervirati, ako resurs koji se može rezervirati već ne postoji.
5. Način naplate na svakom retku podugovora može biti **Fiksna cijena** ili **Vrijeme i materijal**. Za retke podugovora s fiksnom cijenom možete postaviti raspored faktura koji se temelji na kontrolnim točkama.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
