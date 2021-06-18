---
title: Pregled načina upravljanja resursima
description: U ovoj temi nalaze se informacije o upravljanju funkcionalnošću resursa u aplikaciji Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94db65a2ddbdc6a7226c70907bcce4c45b4a3923
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000877"
---
# <a name="resource-management-modes-overview"></a>Pregled načina upravljanja resursima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_


Dynamics 365 Project Operations podržava dva načina kako biste izvršili cjelokupni tijek rezervacije. Način upravljanja definiran je kao parametar projekta i može se izmijeniti ako vaše poslovanje treba promjenu.    

## <a name="central-mode"></a>Središnji način rada
Za tvrtke ili ustanove koje centraliziraju dodjelu resursa projektima, središnji način omogućuje način da menadžeri projekata mogu definirati preduvjete resursa na razini projekta. Ispunjavanje preduvjeta resursa delegira se upravitelju resursa. Upravitelji projekata mogu prihvatiti ili odbaciti resurse koje predloži upravitelj resursa.

![Središnji način](./media/resource-management-central.png)

Kako biste upravljali resursima s pomoću Središnjeg načina, pogledajte sljedeće:

- [Dodjeljivanje zadatku generičkih resursa koji se mogu rezervirati i generiranje zahtjeva za resursima](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezerviranje imenovanih resursa iz preduvjeta za resurs](/dynamics365/project-service/book-named-resource)
- [Slanje zahtjeva za resurs](/dynamics365/project-service/submit-resource-request)
- [Ispunjavanje zahtjeva za resurse](/dynamics365/project-service/resource-management-fulfill-requests)
- [Prihvaćanje ili odbijanje predloženog resursa za projekt iz zahtjeva za resurs](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hibridni način
Za tvrtke ili ustanove kojima je potrebna fleksibilnost u raspodjeli resursa, hibridni način pruža upraviteljima projekata i upraviteljima resursa mogućnost rezerviranja resursa.

![Hibridni način](./media/resource-management-hybrid.png)

Uz podržani postupak Središnjeg načina, pogledajte sljedeće teme za upravljanje svim ostalim podržanim tijekovima rezervacije u hibridnom načinu:

Rezervirajte resurs izravno projektu:
- [Rezerviraj imenovane resurse koji se mogu rezervirati za projektni tim i dodijeli zadatke](/dynamics365/project-service/assign-named-bookable-resource)

Rezervirajte resurs iz preduvjeta resursa:
- [Dodjeljivanje zadatku generičkih resursa koji se mogu rezervirati i generiranje zahtjeva za resursima](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezerviranje imenovanih resursa iz preduvjeta za resurs](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]