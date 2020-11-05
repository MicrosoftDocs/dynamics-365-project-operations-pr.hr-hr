---
title: Reci ponude temeljeni na proizvodu
description: Ova tema pruža informacije o recima ponude temeljenim na proizvodu.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 55a5b5041a494892e6d96bf24e1bc132a26521dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073568"
---
# <a name="product-based-quote-lines"></a>Reci ponude temeljeni na proizvodu

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Možete stvoriti retke ponude temeljene na proizvodu u sustavu Dynamics 365 Project Service Automation. Reci ponude temeljeni na proizvodu mogu biti reci "upisa" ili mogu biti stavke iz kataloga proizvoda.

## <a name="product-catalog"></a>Katalog proizvoda

Proizvodi u katalogu proizvoda sustava Dynamics 365 imaju zadanu jedinicu i grupu jedinica. Ako nekoliko proizvoda dijeli isti skup atributa, možete stvoriti skupinu proizvoda koja također ima te atribute. Svi proizvodi u jednoj skupini proizvoda nasljeđuju isti skup atributa.

Na primjer, tvrtka prodaje pretplatničke licence za razne programe. Svi pretplatnički programi imaju sljedeća dva atributa:

- Broj korisnika 
- Trajanje pretplate (u mjesecima)

Dobar način za održavanje ove vrste kataloga jest stvaranje skupine proizvoda naziva **Softver za pretplatu** koja sadrži atribute **Broj korisnika** i **Trajanje pretplate**. Skupini proizvoda **Softver za pretplatu** zatim možete dodati pojedinačne proizvode, kao što su **Dynamics 365 Sales** ili **Dynamics 365 Field Service**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Dodavanje stavki kataloga proizvoda u ponudu projekta

Stranice ponude projekta i ugovora o projektu imaju odjeljke za dvije vrste redaka: retke temeljene na projektu i retke temeljene na proizvodu. Za retke temeljene na proizvodu Dynamics 365 koristi se za dodavanje stavki iz kataloga proizvoda u ponudu. Padajući popis u retku ponude ili retku ugovora o projektu obuhvaća sve proizvode i jedinice u cjeniku proizvoda koji je priložen ponudi ili ugovoru o projektu. Možete i dodati proizvode koji nisu dio cjenika proizvoda ponude.

Osim toga, možete odabrati proizvode s drugih cjenika ili možete odabrati proizvode izravno iz kataloga proizvoda. Kada odaberete proizvode izravno iz kataloga proizvoda, zadani cjenik tog proizvoda koristi se za dohvaćanje prodajne cijene proizvoda. Ako zadani cjenik nije postavljen, cijena je postavljena na vrijednost 0 (nula).

Ako se redak ponude temelji na katalogu proizvoda, prodajnu cijenu možete izravno zamijeniti u retku ponude. Imajte na umu da redak ponude u sustavu Dynamics 365 sadrži polje **Određivanje cijena**. Dostupne su dvije vrijednosti:

- Zamijeni cijene  
- Koristi zadano

Ako ovo polje postavite na **Zamijeni cijene** , Dynamics 365 ne postavlja zadanu cijenu. Morate unijeti cijenu proizvoda u retku ponude. Ako ovo polje postavite na **Koristi zadano** , Dynamics 365 koristi zadanu prodajnu cijenu i zaključava polje kako bi se spriječilo uređivanje.

Nakon instaliranja PSA-a zadane prodajne cijene unose se u retke temeljene na proizvodu u ponudi. Polje **Određivanje cijena** zatim se postavlja na **Zamijeni cijene** kako biste mogli urediti zadanu cijenu u recima ponude.

> ![Postavljanje zamjene cijena](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Čimbenici količine za proizvode

PSA koristi čimbenike količine za podršku pri prodaji proizvoda temeljenih na pretplati. Za proizvode temeljene na pretplati količina u retku ponude ili ugovora o projektu izražena je kao broj korisničkih mjeseci.

Cijena softvera za pretplatu obično se pohranjuje u katalog kao mjesečna cijena po korisniku. Međutim, umjesto toga možete koristiti druge vremenske opise. Tijekom prodajnog postupka cijena u retku ponude obično je dogovorena mjesečna cijena cijena po korisniku uz popust IT prodajnog predstavnika. Svaki ugovor ima različit broj korisnika i različit broj mjeseci pretplate. Količina koja se koristi za izračun iznosa retka ponude proizvod je broja korisnika i broja mjeseci pretplate.

Da bi podržao ovu vrstu prodaje, PSA je uveo koncept čimbenika količine. Čimbenici količine oslanjaju se na atribute proizvoda u sustavu Dynamics 365. Kada konfigurirate određena svojstva za proizvod, PSA vam omogućuje označavanje podskupa tih svojstava ili svih svojstava kao čimbenika količine.

PSA potvrđuje da su samo numerička svojstva ili svojstva proizvoda koja imaju numeričku vrstu podataka označena kao čimbenici količine. Kada se proizvod za koji su konfigurirani čimbenici količine doda u redak ponude, polje **Količina** u retku ponude postaje polje samo za čitanje. Nakon što unesete vrijednosti za svojstva proizvoda koja su čimbenici količine, PSA izračunava količinu retka ponude.

Na primjer, Dynamics 365 može imati sljedeća svojstva: 

- **Broj korisnika** – broj korisnika 
- **Broj mjeseci** – broj mjeseci pretplate
- **SKU proizvoda** 

Svojstva **Broj korisnika** i **Broj mjeseci** mogu se označiti kao čimbenici količine uređivanjem svojstava retka proizvoda. 

> ![Označavanje broja korisnika i mjeseci kao čimbenika kvalitete](media/basic-guide-11.png)
 
