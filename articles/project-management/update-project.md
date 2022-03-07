---
title: Stvaranje i ažuriranje projekta
description: U ovoj temi nalaze se informacije o ažuriranju projekata u aplikaciji Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d0847b5343cf3e353b91eae04c94509f14213ba5
ms.sourcegitcommit: 51224cb3bf7cdeae6614d39fc8d899c83dbad5f2
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/23/2021
ms.locfileid: "7678340"
---
# <a name="create-and-update-a-project"></a>Stvaranje i ažuriranje projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Slijedi sažetak polja koja se mogu ažurirati na projektu nakon što je stvoren. To također uključuje sve primjenjive implikacije koje se temelje na ovim ažuriranjima.

## <a name="project-detail-fields"></a>Polja pojedinosti projekta

- **Naziv**: Naziv projekta.
- **Opis**: Pregled projekta.
- **Klijent**: Tvrtka kojoj će projekt biti isporučen.
- **Predložak kalendara** : Radno vrijeme projekta. Kada se polje promijeni, preračunava se cijeli raspored.
- **Valuta**: Valutu projekta. Zadana vrijednost za ovo polje temelji se na valuti definiranoj u ugovornoj jedinici. Kada se ugovorna jedinica ažurira, ažurira se i polje.
- **Ugovorna jedinica**: Organizacijska jedinica koja predstavlja grupu ili odjel poduzeća koja je prvenstveno odgovorna za ostvarivanje prodaje i upravljanje isporukom rada i usluga klijentu.  Kada organizacijska jedinica voditelja projekta nije definirana, ovo je polje zadano za vrijednost definiranu u parametrima projekta.
- **Voditelj projekta**: Član projektnog tima koji ima ovlast pregledavati i odobravati unose vremena i troškove.

## <a name="estimate-fields"></a>Polja za procjenu

- **Procijenjeni datum početka**: Datum kada će započeti projekt. Kada se ovo polje ažurira, svi zadaci na projektu kretat će se proporcionalno s početkom novog datuma početka.
- **Datum završetka**: Datum kada je planiran završetak projekta.
- **Rad**: Procijenjeni rad na projektu. Kada se zadaci dodaju u projekt, ovo se polje više ne može uređivati.
- **Procijenjeni trošak rada**: Procijenjeni trošak rada na projektu. Kada se troškovi rada dodaju u projekt, ovo se polje više ne može uređivati.
- **Procijenjeni troškovi**: Procijenjeni troškovi projekta. Kada se troškovi dodaju u projekt, ovo se polje više ne može uređivati.

## <a name="project-actual-fields"></a>Polja projekta sa stvarnim podacima
- **Stvarni početak**: Datum početka projekta.
- **Stvarni završetak**: Treba se ažurirati kada se projekt dovrši.

## <a name="project-status-fields"></a>Statusna polja projekta

- **Ukupni status projekta**: Ukupno stanje projekta koje osigurava voditelj projekta.
- **Komentari**: Izvješće o trenutačnom stanju projekta koje daje voditelj projekta.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
