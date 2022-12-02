---
title: Stvaranje i primjena uvjeta zadržanog plaćanja dobavljaču
description: U ovom se članku navode informacije o načinu postavljanja i održavanja uvjeta zadržavanja za plaćanja dobavljaču.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 2cd18375d93e503ac532cb3839c691231ea46681
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916739"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Stvaranje i primjena uvjeta zadržanog plaćanja dobavljaču

[!include [banner](../includes/banner.md)] 

Postavljanje uvjeta zadržavanja plaćanja dobavljaču za projekt korisno je kada vaša tvrtka ili ustanova želi zadržati dio od ukupnog iznosa koji je dužna dobavljaču. Na primjer, kada želite zadržati plaćanje dobavljaču dok isporučeni proizvodi ne ispune vaša očekivanja. Uvjeti zadržavanja plaćanja dobavljaču mogu se odrediti kada pregovarate o ugovoru o nabavi.

## <a name="create-vendor-payment-retention-terms"></a>Stvaranje uvjeta zadržavanja plaćanja dobavljaču

Možete unijeti postotak zadržavanja od ukupnog plaćanja dobavljaču i postotak prethodno zadržanih iznosa koji će se osloboditi. Iznosi se automatski zadržavaju od faktura dobavljača sve dok ugovor ne dosegne određeno stanje završenosti. Nakon što postavite uvjete zadržavanja, možete ih primijeniti na svaki projekt tog dobavljača.

Upotrijebite sljedeće korake za postavljanje i održavanje uvjeta zadržavanja plaćanja dobavljaču. 

1. Idite na **Upravljanje projektima i računovodstvo** > **Zadržavanje** > **Uvjeti zadržavanja plaćanja dobavljaču**.
2. Odaberite **Novo** kako biste dodali novi uvjet za zadržavanje plaćanja dobavljaču. Vrijednost **ID pravila** za novi uvjet unosi se automatski. 
3. U polje **Opis** unesite kratki opis i na Brzoj kartici **Uvjeti** odaberite **Dodaj redak** za unos vrijednosti uvjeta za sljedeće:

   - **Postotak isporučenih jedinica**: Unesite postotak završetka za uvjet. Iznosi se automatski zadržavaju od faktura dobavljača sve dok se stanje završenosti ne izjednači s navedenim postotkom. Na primjer, ako unesete 50,00, iznosi se zadržavaju sve dok projekt ne bude završen 50 posto.
   - **Postotak zadržavanja**: Unesite postotak iznosa fakture dobavljača koji će se zadržati. Na primjer, ako unesete 10,00, tada se zadržava 10 posto iznosa od fakture dobavljača dok projekt ne dosegne postotak dovršenosti kako je postavljeno u polju **Postotak isporučenih jedinica**.
   - **Postotak za oslobađanje**: Odaberite **Dodaj redak** za unos postotka svih prethodno zadržanih iznosa koji se oslobađaju na odabranoj razini dovršenosti projekta.

> [!NOTE]
> Ako imate više od jedne kontrolne točke za različite razine dovršenosti projekta, unesite zasebni redak zadržavanja plaćanja dobavljaču za svako pravilo zadržavanja. Svaki redak može odrediti različiti postotak zadržavanja i različiti postotak oslobađanja za svaku naznačenu razinu dovršenosti projekta.

Nakon što stvorite uvjete zadržavanja plaćanja dobavljaču, možete ih primijeniti na projekt.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Primjena uvjeta zadržavanja dobavljača na projekt

1. Idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Svi projekti** i otvorite projekt sa stranice s popisom projekata.
2. Na Brzoj kartici **Ugovori s dobavljačima** odaberite **Dodaj redak**.
3. U polju **koda računa** odaberite jednu od sljedećih mogućnosti: 

   - **Tablica**: Uvjeti zadržavanja plaćanja dobavljaču primjenjuju se na pojedinog dobavljača.
   - **Grupa**: Uvjeti zadržavanja plaćanja dobavljaču primjenjuju se na sve dobavljače u grupi dobavljača.
   - **Svi**: Uvjeti zadržavanja plaćanja dobavljaču primjenjuju se na sve dobavljače.

4. U polju **Dobavljač /grupa dobavljača** odaberite dobavljača ili grupu dobavljača na koje se primjenjuju uvjeti zadržavanja plaćanja. Ako ste u prethodnom koraku odabrali **Svi**, ovo polje nije dostupno.
5. U polju **Uvjeti zadržavanja plaćanja dobavljaču** odaberite uvjete zadržavanja koje ste stvorili u prethodnom postupku.
6. Ako projekt za dobavljača ima postavljene i uvjete „plati kad bude plaćeno” (PWP, pay-when-paid), unesite postotak praga za projekt u polje **Postotak praga PWP-a**.

Uvjeti zadržavanja plaćanja dobavljaču prikazuju se i na narudžbenicama koje stvarate za dobavljača.


[!INCLUDE[footer-include](../includes/footer-banner.md)]