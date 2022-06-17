---
title: Pregled redaka ugovora koji se temelje na proizvodu – jednostavno
description: U ovom se članku nalaze informacije o recima ugovora koji se temelje na proizvodu.
author: rumant
ms.date: 10/07/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4ad1fe6d5d56468d887535ddf107eefed3cbd28d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919867"
---
# <a name="product-based-contract-lines-overview---lite"></a>Pregled redaka ugovora koji se temelje na proizvodu – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Možete stvoriti retke ugovora koji se temelje na proizvodu u aplikaciji Dynamics 365 Project Operations. Redci ugovora koji se temelje na proizvodu mogu biti ručno stvoreni redci ili stavke iz kataloga proizvoda.

## <a name="product-catalog"></a>Katalog proizvoda

Proizvodi u katalogu proizvoda imaju zadanu jedinicu i grupu jedinica. Ako nekoliko proizvoda dijeli isti skup atributa, možete stvoriti skupinu proizvoda koja također ima te atribute. Svi proizvodi u jednoj skupini proizvoda nasljeđuju isti skup atributa.

Na primjer, tvrtka prodaje pretplatničke licence za razne vrste softvera. Svi pretplatnički programi imaju sljedeća dva atributa:

- Broj korisnika
- Trajanje pretplate (u mjesecima)

Kako biste održali ovu vrstu kataloga, stvorite asortiman proizvoda pod nazivom **Softver za pretplatu**. Asortimanu proizvoda dodajte atribute **Broj korisnika** i **Trajanje pretplate**. Zatim dodajte pojedinačne proizvode u asortiman proizvoda **Softver za pretplatu**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Dodavanje stavki kataloga proizvoda u ugovor o projektu

Ugovori o projektu imaju odjeljke za dvije vrste redaka, one koji se temelje na projektu i one koji se temelje na proizvodu. Redci koji se temelje na proizvodu uključuju sve proizvode i jedinice u cjeniku proizvoda na ugovoru. Proizvodi koji nisu dio cjenika proizvoda iz ugovora mogu se dodati.

Proizvode možete odabrati iz drugih cjenika ili izravno iz kataloga proizvoda. Kada odaberete proizvode izravno iz kataloga proizvoda, zadani cjenik tog proizvoda upotrebljava se za dohvaćanje prodajne cijene proizvoda. Ako zadani cjenik nije postavljen, cijena je postavljena na vrijednost 0 (nula).

Ako se redak ugovora temelji na katalogu proizvoda, prodajnu cijenu možete izravno zamijeniti u retku. Redak ugovora sadrži polje **Određivanje cijene** s dvije vrijednosti:

- **Zamijeni cijene**
- **Koristi zadano**

Ako polje **Određivanje cijene** postavite na **Zamjensko određivanje cijene**, zadana se cijena ne postavlja. Unesite cijenu za proizvod u redak ugovora. Ako polje postavite na **Upotrijebi zadano**, upotrebljava se zadana prodajna cijena i polje se ne može uređivati.

Nakon instaliranja aplikacije Project Operations, zadane prodajne cijene unose se u retke koji se temelje na proizvodu u ugovoru. Polje **Određivanje cijena** postavlja se na **Zamijeni cijene** kako biste mogli urediti zadanu cijenu u redcima ugovora. Ova je zamjena za ponašanje redaka koji se temelje na proizvodu u aplikaciji Dynamics 365 Sales specifična za aplikaciju Project Operations.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]