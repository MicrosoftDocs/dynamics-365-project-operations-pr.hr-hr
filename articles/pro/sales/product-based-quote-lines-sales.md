---
title: Pregled redaka ponude koji se temelje na proizvodu – jednostavno
description: U ovoj temi nalaze se informacije o radu s redcima ponude koji se temelje na proizvodu.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369772"
---
# <a name="product-based-quote-lines-overview---lite"></a>Pregled redaka ponude koji se temelje na proizvodu – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Možete stvoriti retke ponude temeljene na proizvodu u sustavu Dynamics 365 Project Operations. Redci ponude koji se temelje na proizvodu mogu se ručno dodati ili mogu biti stavke iz kataloga proizvoda.

## <a name="product-catalog"></a>Katalog proizvoda

Svaki proizvod u katalogu proizvoda ima zadanu jedinicu i grupu jedinica. Ako više proizvoda dijeli isti skup atributa, možete stvoriti skupinu proizvoda koja dijeli te atribute. 

Na primjer, tvrtka prodaje pretplatničke licence za razne vrste softvera. Svi pretplatnički programi imaju sljedeća dva atributa:

- Broj korisnika
- Trajanje pretplate mjereno u mjesecima

Za održavanje ove vrste kataloga stvorite skupine proizvoda naziva **Softver za pretplatu** i dodajte broj korisnika i trajanje pretplate kao atribute. Nadalje, možete dodati pojedinačne proizvode u skupinu proizvoda **Softver za pretplatu**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Dodavanje stavki kataloga proizvoda u ponudu projekta

Stranice **Ponuda projekta** i **Ugovor o projektu** imaju odjeljke za retke koji se temelje na projektu i retke koji se temelje na proizvodu. Za retke koji se temelje na proizvodu, padajući popis u retku ponude ili retku ugovora o projektu obuhvaća sve proizvode i jedinice u cjeniku proizvoda. Možete i dodati proizvode koji nisu dio cjenika proizvoda.

Osim toga, možete odabrati proizvode iz drugih cjenika ili izravno iz kataloga proizvoda. Kada odaberete proizvode izravno iz kataloga proizvoda, zadani cjenik tog proizvoda koristi se za dohvaćanje prodajne cijene proizvoda. Ako zadani cjenik nije postavljen, cijena je postavljena na vrijednost nula (0).

Kada se redak ponude temelji na katalogu proizvoda, prodajnu cijenu možete nadjačati izravno u retku ponude. Redak ponude u polju **Cijene** s dvije dostupne vrijednosti:

- **Nadjačaj cijenu**
- **Koristi zadano**

Ako odaberete mogućnost **Nadjačaj cijenu**, zadana se cijena ne postavlja. Umjesto toga, cijenu proizvoda morate unijeti u redak ponude. Ako odaberete **Upotrijebi zadano**, upotrebljava se zadana prodajna cijena i polje se zaključava za uređivanje.

Zadane prodajne cijene unose se u retke ponude koji se temelje na proizvodu u ponudi. Polje **Cijene** zatim se postavlja na **Nadjačaj cijene** kako biste mogli urediti zadanu cijenu u redcima ponude. Ovo nadjačavanje ponašanja redaka koji se temelje na proizvodima u aplikaciji Dynamics 365 Sales, specifično je za aplikaciju Project Operations.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]