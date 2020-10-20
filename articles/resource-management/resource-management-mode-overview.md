---
title: Pregled načina upravljanja resursima
description: U ovoj temi nalaze se informacije o funkcionalnosti Upravljanja resursima u sustavu Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930082"
---
# <a name="resource-management-modes-overview"></a>Pregled načina upravljanja resursima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_


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
