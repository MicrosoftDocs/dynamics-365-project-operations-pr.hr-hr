---
title: Novosti u valu 2 ranom pristupu u 2021. – osnovna implementacija aplikacije Project Operations
description: U ovoj temi nalaze se informacije o značajkama dostupnim u valu 2 ranog pristupa izdanja implementacije osnovne aplikacije Project Operations u 2021. godini.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323902"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Novosti u valu 2 ranom pristupu u 2021. – osnovna implementacija aplikacije Project Operations

_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_

Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

  - Project Operations u verziji 4.23.0.4 okruženja platforme Dataverse

Izdanje se primjenjuje samo kada je okruženje [uključeno u Rani pristup](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

[Upravljanje podugovorima](../subcontracting/subcontracting_EA_scope.md) – Ova značajka omogućuje bolju preglednost i kontrolu nad svim aspektima rada na projektu. Pretpregled upravljanja podugovorom uključuje sljedeće mogućnosti:

  - Voditelj projekta može stvoriti podugovor s dobavljačem. Prema zadanim postavkama, cjenici koji su priloženi zapisu o dobavljaču upotrebljavaju se za podugovor. Račun dobavljača ima vrstu odnosa **Dobavljač** ili **Isporučitelj**.
  - Voditelj projekta može sve kupnje specificirati kao stavke retka na podugovoru. Redci podugovora mogu se odnositi na vrijeme, troškove ili proizvode. Klasa transakcije retka podugovora određuje čemu taj redak služi.
  - Voditelj računa dobavljača i voditelj projekta mogu ponavljati podugovor. U nabavnim cjenicima priloženim podugovoru cijene se mogu prilagoditi.
  - Tijekom postupka, ako je redak podugovora za vrijeme, upravitelj računa dobavljača može povezati kontakte dobavljača sa svakim retkom podugovora. Ova povezanost pruža informacije voditelju projekta koji radi na podugovoru. Kad je kontakt dobavljača povezan s retkom podugovora, sustav iz kontakta automatski stvara kontakt koji se može rezervirati, ako resurs koji se može rezervirati već ne postoji.
  - Način naplate na svakom retku podugovora može biti fiksna cijena ili vrijeme i materijal. Za retke podugovora s fiksnom cijenom postavljen je raspored faktura koji se temelji na kontrolnim točkama.
