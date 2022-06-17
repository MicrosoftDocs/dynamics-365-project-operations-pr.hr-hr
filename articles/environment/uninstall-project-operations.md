---
title: Deinstalirajte Dynamics 365 Project Operations.
description: U ovom se članku nalaze informacije o deinstalaciji Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911955"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Deinstalirajte Dynamics 365 Project Operations. 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Kako biste deinstalirali aplikaciju Dynamics 365 Project Operations, morate dobiti ulogu administratora.

1. Idite na **Postavke** > **Rješenja**.

    ![Stranica s postavkama.](./media/uninstall-proj-ops-solutions.png)
  
2. Uklonite rješenja točnim redoslijedom kojim su navedena u tablici u nastavku. 

    | Korak | Naziv rješenja                                    | Bilješka                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 2 | ProjectOperations_Anchor                           | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 5 | ProjectService                                     | Nema dodatnih napomena.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Nema dodatnih napomena.                                                                         |
    | 7 | ProjectServiceCore                                 | Nema dodatnih napomena.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 9 | FieldServiceCommon                                 | Obavezno za dvostruko pisanje s Dynamics 365 Finance ili Dynamics 365 Supply Chain Management.   |
    | 1,0 | msdyn_AssetCommon                                  | Obavezno za dvostruko pisanje s Dynamics 365 Finance ili Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Obvezno polje za aplikaciju Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Obvezno polje za aplikaciju Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Obvezno polje za aplikaciju Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Obvezno polje za aplikaciju Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Obvezno polje za aplikaciju Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Obvezno polje za aplikaciju Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Obvezno polje za aplikaciju Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 19 | Dynamics365Notes                                   | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 21 | DualWriteCore                                      | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 23 | Dynamics365AssetManagement                         | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 26 | HCMCommon                                          | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 28 | Nositelj                                              | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 29 | Dynamics365Company                                 | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 30 | CurrencyExchangeRates                              | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
    | 31 | AssetCommon                                        | Ako nije pronađeno, preskočite ovo rješenje.                                                            |
