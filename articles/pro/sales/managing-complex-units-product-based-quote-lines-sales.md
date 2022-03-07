---
title: Upravljanje složenim jedinicama, primjerice po korisniku, po mjesecu za retke ponude utemeljene na proizvodu – jednostavno
description: U ovoj temi nalaze se informacije o upravljanju složenim jedinicama za retke ponude koji se temelje na projektu.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d53dde1d3b2705c5b0283f989d0e2eebfdcb5a0eb5f91cf4bf48e9c07aba79d1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989767"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Upravljanje složenim jedinicama, primjerice po korisniku, po mjesecu za retke ponude utemeljene na proizvodu – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Dynamics 365 Project Operations upotrebljava čimbenike količine za podršku pri prodaji proizvoda temeljenih na pretplati. Za proizvode temeljene na pretplati količina u retku ponude ili ugovora o projektu izražena je kao broj korisničkih mjeseci.

Cijena softvera za pretplatu obično se pohranjuje u katalog kao mjesečna cijena po korisniku. Tijekom prodajnog postupka cijena u retku ponude obično je dogovorena mjesečna cijena cijena po korisniku uz popust IT prodajnog predstavnika. Svaki ugovor ima različit broj korisnika i različit broj mjeseci pretplate. Količina koja se upotrebljava za izračun retka ponude proizvod je broja korisnika i broja mjeseci pretplate.

Kako bi podržao ovu vrstu prodaje, Project Operations je uveo koncept čimbenika količine. Čimbenici količine oslanjaju se na atribute proizvoda u sustavu Dynamics 365. Kada konfigurirate određena svojstva za proizvod, Project Operations omogućuje vam označavanje podskupa ili svih svojstava kao čimbenika količine.

Project Operations provjerava valjanost jesu li samo numerička svojstva ili svojstva proizvoda koja imaju numeričku vrstu podataka označena kao čimbenici količine. Kada u redak ponude dodate proizvod s čimbenicima količine, polje **Količina** postaje polje samo za čitanje. Nakon što unesete vrijednosti za svojstva proizvoda koja su čimbenici količine, Project Operations izračunava količinu retka ponude.

Na primjer, Dynamics 365 Sales može imati sljedeća svojstva:

- **Broj korisnika**: broj korisnika
- **Broj mjeseci**: broj mjeseci pretplate
- **SKU proizvoda**

Svojstva **Broj korisnika** i **Broj mjeseci** možete označiti kao čimbenike količine uređivanjem svojstava retka proizvoda.

Kako biste stvorili čimbenike količine iz svojstava proizvoda, slijedite ove korake:

1. U lijevom navigacijskom oknu aplikacije Project Operations idite na **Prodaja** > **Proizvodi**.
2. Otvorite proizvod za koji trebate konfigurirati čimbenike količine. Provjerite imaju li proizvodi već konfigurirana svojstva.
3. Na stranici **Informacije o projektu** za Proizvod, odaberite karticu **Čimbenici količine**.
4. U podrešetki odaberite **+ Izračun novog polja**.
5. Unesite naziv čimbenika količine i odaberite vrijednost svojstva koja se mapira u izračun polja.
6. Spremanje i zatvaranje obrasca. Ponovite ove korake za sva svojstva koja ćete upotrebljavati za izračunavanje količine za redak ponude koji se temelji na proizvodu.

Kada stvarate redak ponude koji se temelji na proizvodu, količina retka ponude bit će zaključana. Količina će se izračunati kao umnožak vrijednosti svojstva koje ste unijeli za taj redak ponude.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]