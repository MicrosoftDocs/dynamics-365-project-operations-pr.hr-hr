---
title: Resursi retka podugovora
description: U ovom članku objašnjava se način navođenja namjenskih resursa koje dobavljač daje za određeni redak podugovora za vrijeme.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 04e3e5ee70c50068304a8a6c8f7e93df48ed7e85
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522363"
---
# <a name="subcontract-line-resources"></a>Resursi retka podugovora

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U aplikaciji Dynamics 365 Project Operations dobavljač može navesti resurse koji će se upotrebljavati za opskrbu kapaciteta resursa koji se kupuje na retku podugovora za vrijeme.

## <a name="create-subcontract-line-resources"></a>Stvaranje resursa retka podugovora

Kako biste stvorili resurse retka podugovora, poduzmite sljedeće korake.

1. U navigacijskom oknu odaberite **Podugovori** i otvorite podugovor na kojem želite raditi.
2. Otvorite redak podugovora za vrijeme na kojem želite navesti resurse dobavljača.
3. Na kartici **Resursi retka podugovora**, u podrešetki, odaberite **+ Novi resurs retka podugovora**.
4. Na stranici **Novi resurs retka podugovora** unesite potrebne podatke, a zatim odaberite **Spremi i zatvori**.

U tablici u nastavku objašnjena su polja na resursu retka podugovora.

| Polje | Opis | Funkcionalni utjecaj |
| ----- | ----------- | ----------------- |
| Resurs koji je moguće rezervirati | Odaberite resurs vrste **Radnik po ugovoru** koji se može rezervirati i koji želite upotrebljavati kao resurs u retku podugovora.| Ako za ugovornog radnika niste stvorili resurs koji se može rezervirati, ostavite to polje prazno. Resurs koji se može rezervirati stvorit će se kada spremite zapis.  |
| Kontakt | Resurs retka svojeg podugovora možete stvoriti iz postojećeg kontakta. Upotrijebite pretraživanje za prikaz popisa aktivnih kontakata u sustavu. Odaberite kontakt za dobavljača ovog podugovora. Ako kontakt koji ste odabrali nije valjani kontakt za dobavljača na podugovoru, zapis resursa retka podugovora neće se spremiti.| Ako za odabrani kontakt nema resursa koji se može rezervirati, sustav stvara resurs koji se može rezervirati za odabrani kontakt prije stvaranja resursa retka podugovora. |
| Korisnik | Resurs retka podugovora možete stvoriti odabirom djelatnog korisnika. Upotrijebite pretraživanje za prikaz popisa aktivnih korisnika u sustavu.| Ako za odabranog korisnika nema resursa koji se može rezervirati, sustav stvara resurs koji se može rezervirati za odabranog korisnika prije stvaranja resursa retka podugovora. |
| Datum početka | Datum početka zadatka radnika iz podugovora.| Ako je ovaj resurs rezerviran za razdoblje koje prethodi ovom datumskom rasponu, prikazat će se upozorenje. |
| Datum završetka | Datum završetka zadatka radnika iz podugovora.| Ako je ovaj resurs rezerviran za razdoblje koje nastupa nakon ovog datumskog raspona, prikazat će se upozorenje. |
| Rad | Ukupan broj sati rada koji će ugovorni radnik potrošiti na ovaj redak podugovora.| Ako je ovaj resurs rezerviran izvan rada koji je dodijeljen ovom podugovoru, prikazat će se upozorenje. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
