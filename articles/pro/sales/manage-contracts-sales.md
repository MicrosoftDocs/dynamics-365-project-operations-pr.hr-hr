---
title: Upravljanje ugovorima o projektu
description: U ovoj temi nalaze se informacije o načinu prikazivanja ugovora koji se temelje na projektu.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 64e81593065d97272af6261e17175c76bd8dca7a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590475"
---
# <a name="manage-project-contracts"></a>Upravljanje ugovorima o projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Ugovori o projektu u aplikaciji Dynamics 365 Project Operations dohvaćaju i upravljaju ugovorno dogovorenim obvezama i pojedinostima o naplati projekta. Struktura ugovora o projektu u aplikaciji Project Operations prilagođena je poslu koji se temelji na projektu sa sljedećim komponentama:

- Redci ugovora koji identificiraju određene komponente posla koje će se na fakturi za projekt predstaviti kao komponente visoke razine.
- Pojedinosti retka ugovora koje identificiraju i procjenjuju posao za svaku komponentu ili redak ugovora visoke razine. Procjena uključuje raspored i financijske aspekte posla vezanog uz redak ugovora.
- Modeli ugovaranja i naplative komponente postavljaju se za svaki redak ugovora koji sadrži način naplate za svaki redak ugovora i cjelokupni ugovor.

## <a name="view-all-project-based-contracts"></a>Prikaz ugovora koji se temelje na projektu

Popis svih ugovora o projektu koji se mogu vidjeti na stranici s popisom **Ugovori**. 

1. Idite na **Prodaja** > **Ugovori**. Prikazan je popis svih vaših ugovora o projektu u sustavu. 
2. Odaberite **Preklopnik prikaza** (strelica padajućeg izbornika pokraj naziva prikaza) za odabir ostalih filtriranih prikaza. Možete stvoriti vlastite prikaze s prilagođenim kriterijima filtra.

Ugovori se mogu stvoriti ili izbrisati s ove stranice s popisom ili stranica s pojedinostima.

> [!NOTE]
> Ugovori s kojima su povezani projekti, zadaci, procjene, temeljnice i/ili stvarne vrijednosti ne mogu se izbrisati. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
