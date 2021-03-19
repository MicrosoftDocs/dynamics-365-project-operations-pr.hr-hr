---
title: Pregled načina upravljanja resursima
description: U ovoj temi nalaze se informacije o upravljanju funkcionalnošću resursa u aplikaciji Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279444"
---
# <a name="resource-management-modes-overview"></a>Pregled načina upravljanja resursima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_


Dynamics 365 Project Operations podržava dva načina kako biste izvršili cjelokupni tijek rezervacije. Način upravljanja definiran je kao parametar projekta i može se izmijeniti ako vaše poslovanje treba promjenu.    

## <a name="central-mode"></a>Središnji način rada
Za tvrtke ili ustanove koje centraliziraju dodjelu resursa projektima, središnji način omogućuje način da menadžeri projekata mogu definirati preduvjete resursa na razini projekta. Ispunjavanje preduvjeta resursa delegira se upravitelju resursa. Upravitelji projekata mogu prihvatiti ili odbaciti resurse koje predloži upravitelj resursa.

![Središnji način](./media/resource-management-central.png)

Kako biste upravljali resursima s pomoću Središnjeg načina, pogledajte sljedeće:

- [Dodjeljivanje zadatku generičkih resursa koji se mogu rezervirati i generiranje preduvjeta resursa](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezerviranje imenovanih resursa iz preduvjeta resursa](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Slanje zahtjeva za resurs](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Ispunjavanje zahtjeva za resurse](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Prihvaćanje ili odbacivanje predloženog resursa za projekt iz zahtjeva za resurs](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hibridni način
Za tvrtke ili ustanove kojima je potrebna fleksibilnost u raspodjeli resursa, hibridni način pruža upraviteljima projekata i upraviteljima resursa mogućnost rezerviranja resursa.

![Hibridni način](./media/resource-management-hybrid.png)

Uz podržani postupak Središnjeg načina, pogledajte sljedeće teme za upravljanje svim ostalim podržanim tijekovima rezervacije u hibridnom načinu:

Rezervirajte resurs izravno projektu:
- [Rezerviraj imenovane resurse koji se mogu rezervirati za projektni tim i dodijeli zadatke](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Rezervirajte resurs iz preduvjeta resursa:
- [Dodjeljivanje zadatku generičkih resursa koji se mogu rezervirati i generiranje preduvjeta resursa](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezerviranje imenovanih resursa iz preduvjeta resursa](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]