---
title: Predlošci projekta
description: Ova tema pruža informacije o tome kako upotrebljavati predloške projekta za brzo postavljanje projekta.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: db42c9ea7280274cdc9cc90f1487f27e08f892e5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148049"
---
# <a name="project-templates"></a>Predlošci projekta 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Predložak projekta jest unaprijed definirani okvir koji vam omogućuje da brzo i jednostavno započnete projekt. Možete koristiti unaprijed definirani predložak za stvaranje novog projekta jednim klikom. Što se tiče projekata, morate definirati preduvjete za predloške projekata. Morate definirati kalendar projekta za svaki predložak projekta, a uloge i cjenici moraju biti unaprijed definirani u tvrtki ili ustanovi, tako da komponente predloška sadrže korisne podatke.

Predložak projekta sastoji se od tri komponente: rasporeda, procjena projekata i članova projektnog tima.

## <a name="schedule"></a>Raspored

Raspored u predlošku projekta ima isti skup elemenata kao raspored u projektu. Možete stvoriti hijerarhiju zadataka, povezati uloge sa zadacima, odrediti raspored atributa i postaviti ovisnosti. Raspored u predlošku projekta također podržava načine zadatka za svaki zadatak. Stoga podržava mehanizam zakazivanja. Kalendar projekta morate povezati s projektom. Prilikom stvaranja radnog rasporeda nema razlike između predloška projekta i projekta.

## <a name="project-estimates"></a>Procjene projekta

Procjene projekta u predlošku projekta funkcioniraju na isti način kao procjene projekta u projektu. Međutim, troškovi i prodajne cijene dohvaćaju se iz zadanih troškova i prodajnih cjenika koji su definirani u parametrima.

## <a name="creating-a-project-from-a-template"></a>Stvaranje projekta na temelju predloška
 
Postoji nekoliko načina stvaranja projekta na temelju predloška projekta:

- Kada stvorite projekt na temelju ponude, možete odabrati predložak projekta u dijaloškom okviru **Brza izrada: projekt**.

> ![Dijaloški okvir Brza izrada: projekt](media/project-11.png)

- Prilikom stvaranja projekta odabirom mogućnosti **Novi projekt** stranica **Projekt** prikazat će se prije spremanja zapisa. U polju **Odaberi predložak** odaberite jedan od unaprijed definiranih predložaka projekta u tvrtki ili ustanovi.
- Upotrijebite mogućnost **Stvori projekt na temelju predloška** na stranici **Entitet predloška**.

## <a name="copying-components-of-template-to-project"></a>Kopiranje komponenata predloška u projekt

Kada kopirate komponente predloška projekta u projekt, može doći do nekoliko nadjačavanja, ovisno o postavkama u projektu.

### <a name="copying-the-schedule"></a>Kopiranje rasporeda

Kada kopirate raspored iz predloška projekta, ako projekt ima kalendar projekta različit od predloška, radno vrijeme iz kalendara projekta primijenit će se na raspored zadataka. Na taj način raspored se prilagođava u skladu s kalendarom projekta. Isto tako, prvi zadatak u rasporedu preuzima datum početka projekta, a raspored ostatka hijerarhije ažurira na temelju trajanja i ovisnosti navedenih u predlošku. 

### <a name="copying-project-estimates"></a>Kopiranje procjena projekta 

Prilikom kopiranja u retke procjene projekta cjenici se ažuriraju. Za cjenik s cijenama koštanja ta se ažuriranja temelje na vlasničkoj jedinici projekta. Za prodajni cjenik temelje se na klijentu. Za projekte koji su povezani s entitetom prodaje cijene po jedinici i prodajne cijene određuju se na temelju ovih cjenika.

### <a name="copying-a-project-team"></a>Kopiranje projektnog tima

Kada projektni tim kopirate iz predloška projekta u projekt, generički resursi kopiraju se zajedno s vještinama i stručnostima definiranim u predlošku. Dodjele generičkih resursa također se zadržavaju kao u predlošku projekta. Imenovani resursi nisu podržani u predlošcima projekta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]