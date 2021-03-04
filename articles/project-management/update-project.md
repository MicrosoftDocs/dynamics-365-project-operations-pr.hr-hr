---
title: Ažuriranje projekta
description: U ovoj temi nalaze se informacije o ažuriranju projekata u aplikaciji Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131424"
---
# <a name="update-a-project"></a>Ažuriranje projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U nastavku je sažetak polja koja se mogu ažurirati na projektu nakon što se on stvori i sve primjenjive implikacije ažuriranja.

## <a name="project-detail-fields"></a>Polja pojedinosti projekta

- **Naziv**: Naziv projekta.
- **Opis**: Pregled projekta.
- **Klijent**: Tvrtka kojoj će projekt biti isporučen.
- **Predložak kalendara** : Radno vrijeme projekta. Kada se polje promijeni, preračunava se cijeli raspored.
- **Valuta**: Valutu projekta. Zadana je za ovo polje na temelju valute definirane u ugovornoj jedinici. Kada se ugovorna jedinica ažurira, ažurira se i polje.
- **Ugovorna jedinica**: Organizacijska jedinica koja predstavlja grupu ili odjel poduzeća koja je prvenstveno odgovorna za ostvarivanje prodaje i upravljanje isporukom rada i usluga klijentu. 
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