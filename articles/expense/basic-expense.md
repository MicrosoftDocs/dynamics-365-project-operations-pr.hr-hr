---
title: Unos izdatka (jednostavno)
description: U ovoj temi nalaze se informacije o načinu unosa troška u jednostavnoj implementaciji.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e75a61c25be06a9db121e8165e8ccd25d4719d08
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002182"
---
# <a name="expense-entry-lite"></a>Unos izdatka (jednostavno)

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Osnovno ili jednostavno upravljanje troškovima mogućnost je evidentiranja jednostavnih troškova. Možete evidentirati troškove na projektu, a zatim će ih odobravatelj projekta pregledati i odobriti.

Dodatne informacija o mogućnostima troškova u rješenju Dynamics 365 Project Operations potražite u odjeljku [Pregled troškova](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Bilježenje osnovnog troška

Možete zabilježiti svoje troškove kako biste ih mogli poslati odobravatelju.

1. Idite na stavku **Troškovi** i odaberite mogućnost **Novi**.
2. Na stranici **Novi trošak** unesite potrebne podatke o trošku, a zatim odaberite mogućnost **Spremi**.

## <a name="submit-a-basic-expense"></a>Slanje osnovnog troška

Nakon što završite s bilježenjem svih troškova i spremni ste ih dati na odobrenje, morate ih poslati.

1. Idite na stavku **Troškovi** i odaberite trošak. Ili odaberite sve troškove s pomoću potvrdnog okvira u zaglavlju.
2. Odaberite **Šalji**. Sustav obrađuje odabrane unose, a zatim stvara zahtjeve za odobrenje troškova.

## <a name="add-an-attachment"></a>Dodaj privitak

Možda ćete odobravatelju morati dostaviti dodatnu dokumentaciju o trošku. Potvrdu možete priložiti vremenskoj traci unosa troškova. Izaberite **Uredi** i u odjeljku **Vremenska traka**, a zatim odaberite ikonu spajalice kako biste priložili potvrdu.

## <a name="recall-a-basic-expense"></a>Opoziv osnovnog troška

Kada greškom pošaljete trošak, možete ga stornirati. Vrijeme potrebno za storniranje unosa troška ovisi o fazi odobrenja u kojoj se nalazi.  Ako odobravatelj još nije odobrio unos, storniranje se može izvršiti odmah. Međutim, ako je unos već odobren, od odobravatelja se treba zatražiti odobrenje opoziva i storniranja transakcija.

1. Idite na stavku **Troškovi**, a zatim na popisu troškova odaberite trošak koji želite stornirati.
2. Odaberite **Storniraj**. Ako unos troška još nije odobren, sustav ga odmah stornira. Ako je unos troška već odobren, stvara se zahtjev za storniranje kako bi se obavijestio odobravatelj da želite stornirati trošak. Odobravatelj će tada potvrditi da se storniranje može izvršiti i unos će biti vraćen.

## <a name="delete-a-basic-expense"></a>Brisanje osnovnog troška

Troškovi koji još nisu poslani mogu se izbrisati. Kako biste izbrisali trošak koji je već poslan, prvo ga morate stornirati.

## <a name="see-also"></a>Pogledajte također

- [Pregled odobrenja](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]