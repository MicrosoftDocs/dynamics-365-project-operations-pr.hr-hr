---
title: Unos izdatka (jednostavan)
description: U ovoj temi nalaze se informacije o načinu unosa troška u jednostavnom uvođenju.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073272"
---
# <a name="expense-entry-lite"></a>Unos izdatka (jednostavan)

_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_

Osnovno ili jednostavno upravljanje troškovima mogućnost je evidentiranja jednostavnih troškova. Možete evidentirati troškove na projektu, a zatim će ih odobravatelj projekta pregledati i odobriti.

Dodatne informacije o mogućnostima troškova u aplikaciji Dynamics 365 Project Operations potražite u odjeljku [Pregled troškova](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Bilježenje osnovnog troška

Možete zabilježiti svoje troškove kako biste ih mogli poslati odobravatelju.

1. Idite na stavku **Troškovi** i odaberite mogućnost **Novi**.
2. Na stranici **Novi trošak** unesite potrebne podatke o trošku, a zatim odaberite mogućnost **Spremi**.

## <a name="submit-a-basic-expense"></a>Slanje osnovnog troška

Nakon što završite s bilježenjem svih troškova i spremni ste ih dati na odobrenje, morate ih poslati.

1. Idite na stavku **Troškovi** i odaberite trošak. Ili odaberite sve troškove s pomoću potvrdnog okvira u zaglavlju.
2. Odaberite **Šalji**. Sustav obrađuje odabrane unose, a zatim stvara zahtjeve za odobrenje troškova.

## <a name="recall-a-basic-expense"></a>Opoziv osnovnog troška

Kada greškom pošaljete trošak, možete ga stornirati. Vrijeme potrebno za storniranje unosa troška ovisi o fazi odobrenja u kojoj se nalazi.  Ako odobravatelj još nije odobrio unos, storniranje se može izvršiti odmah. Međutim, ako je unos već odobren, od odobravatelja se treba zatražiti odobrenje storniranja i poništenje transakcija.

1. Idite na stavku **Troškovi** , a zatim na popisu troškova odaberite trošak koji želite stornirati.
2. Odaberite **Storniraj**. Ako unos troška još nije odobren, sustav ga odmah stornira. Ako je unos troška već odobren, stvara se zahtjev za storniranje kako bi se obavijestio odobravatelj da želite stornirati trošak. Odobravatelj će tada potvrditi da se opoziv može izvršiti i unos će biti vraćen.

## <a name="delete-a-basic-expense"></a>Brisanje osnovnog troška

Troškovi koji još nisu poslani mogu se izbrisati. Kako biste izbrisali trošak koji je već poslan, prvo ga morate stornirati.

## <a name="see-also"></a>Pogledajte također

- [Pregled odobrenja](../approvals/approvals-overview.md)
