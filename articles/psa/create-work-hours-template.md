---
title: Stvaranje predloška radnog vremena
description: U ovoj temi opisuje se način stvaranja predloška radnog vremena u aplikaciji Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981246"
---
# <a name="create-a-work-hours-template-project-service"></a>Izradi predložak radnog vremena (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Kako biste stvorili projekt i upravljali njime, na projekt morate primijeniti predložak kalendara. Predložak kalendara definira sljedeće atribute projekta:

- Radno vrijeme, uključujući vrijeme početka i završetka
- Radni dani
- Iznimke kalendara poput neradnih dana

Predložak kalendara koji se primjenjuje na projekt kopija je predloška kalendara definiranog u postavkama vaše tvrtke ili ustanove.

> [!NOTE]
> Ako promijenite predložak kalendara, te se promjene neće proširiti na radno vrijeme projekta. Kako biste promijenili radno vrijeme projekta, morate primijeniti novi obrazac.

Dva su osnovna zahtjeva za stvaranje predloška kalendara za vašu tvrtku ili ustanovu:

- Definirajte željeno radno vrijeme predloška s pomoću novog ili postojećeg resursa koji se može rezervirati.
- Stvorite novi predložak kalendara i povežite ga s resursom koji se može rezervirati.

**Definiranje radnog vremena predloška**

1. Otvorite **Resursi** \> **Resursi**.
2. Stvorite novi resurs za referencu u predlošku kalendara ili odaberite postojeći.
3. Odaberite karticu **Radno vrijeme** resursa i dovršite upute iz članka [Postavljanje radnog vremena za resurs](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) kako biste konfigurirali pravila kalendara.

**Stvaranje novog predloška kalendara**

1. Idite na **Postavke** \> **Predložak kalendara**.
2. Odaberite **Novi** i unesite naziv, opis i resurs predloška.


> [!NOTE]
> Kada se u predlošku kalendara upućuje na resurs, kopija kalendara resursa povezuje se s predloškom kalendara. Ako se promijeni radno vrijeme kopiranog predloška, te se promjene neće proširiti na predložak kalendara.


### <a name="see-also"></a>Pogledajte također  
 [Postavljanje resursa](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
