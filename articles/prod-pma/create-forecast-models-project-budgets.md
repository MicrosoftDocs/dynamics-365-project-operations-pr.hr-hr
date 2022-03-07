---
title: Stvaranje modela predviđanja za proračune projekata
description: U ovoj temi opisan je način stvaranja modela predviđanja za proračunske iznose koji su preostali.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3549b41fce72b44230ab27de081dade15a912266
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006277"
---
# <a name="create-forecast-models-for-project-budgets"></a>Stvaranje modela predviđanja za proračune projekata 

[!include [banner](../includes/banner.md)]

U ovoj temi opisan je način stvaranja modela predviđanja za proračunske iznose koji su preostali. U projektu koji je podložan kontroli proračuna upotrebljavaju se dvije vrste proračuna: izvorni i preostali. Kada stvarate proračun projekta, morate navesti modele predviđanja izvornog i preostalog proračuna koji su stvoreni na stranici **Modeli predviđanja**. Proračuni projekta na temelju navedenih modela stvaraju se kada napravite proračun projekta.

> [!NOTE]
> Model predviđanja koji se upotrebljava za kontrolu proračuna ne može imati podmodel niti se može upotrebljavati kao podmodel.

1. Odaberite **Upravljanje projektima i računovodstvo** > **Postavi** > **Predviđanje**  > **Modeli predviđanja**.
2. Odaberite **Novi** za stvaranje novog modela predviđanja, a zatim unesite ID broj modela i naziv za novi model. 
3. Postavite mogućnost **Zaustavljeno** na **Da** kako biste spriječili svaku promjenu u redcima predviđanja za model predviđanja. 
4. Ako redci predviđanja s kojima je model povezan trebaju generirati predviđanja novčanog tijeka u glavnoj knjizi, mogućnost **Uključi u predviđanja novčanog tijeka** postavite na **Da**. 
5. Kako biste datum projekta upotrijebili kao datum fakture, mogućnost **Datum predviđanja fakture** na **Da**. 
6. U polju **Vrsta proračuna** odaberite jednu od sljedećih vrsta modela:

   - **Izvorni proračun**: Upotrijebite izvorne proračunske iznose koji su dodijeljeni tijekom stvaranja i odobravanja početnog proračuna.
   - **Preostali proračun**: Upotrijebite proračunske iznose koji su preostali tijekom trajanja projekta. Salda u ovom modelu predviđanja smanjuju se stvarnim transakcijama, a povećavaju ili smanjuju revizijama proračuna.
   - **Preneseni**: Upotrijebite prenesene proračunske iznose za projekt. Prijenos je neobvezan postupak koji se može pokrenuti za prijenos neupotrijebljenih proračunskih iznosa s jedne poslovne godine u drugu.

7. Prema potrebi, postavite sljedeće mogućnosti:

   - Omogućite **Datum predviđanja fakture** kako biste datum projekta upotrijebili kao datum fakture.
   - Omogućite **Predviđanje s pomoću WIP-a** za predviđanje koje se temelji na radu u tijeku (WIP), a zatim odaberite vrstu WIP-a. 
   - Možete zadržati zadanu vrijednost **Vrsta proračuna** kao **Nijedna** ili unesite novu vrstu. Vrsta proračuna ne može se mijenjati nakon što promijenite zapis.     
    > [!NOTE]
    > Ako promijenite zadanu vrstu proračuna, sve ostale mogućnosti postat će nedostupne za ažuriranja i taj model predviđanja ne možete ponovno upotrijebiti. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]