---
title: Odredite vrstu uvođenja
description: U ovoj temi nalaze se informacije koje vam pomažu pri određivanju ispravne vrste uvođenja projektnih operacija za vašu tvrtku.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073392"
---
# <a name="determine-your-deployment-type"></a>Odredite vrstu uvođenja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

> [!IMPORTANT]
> Nakon kupnje licence započnite ovdje kako biste odredili najbolji model uvođenja aplikacije Dynamics 365 Project Operations s pomoću odjeljka [Vođeni tijek instalacije](https://aka.ms/provisionprojectoperations).
> Nakon što dovršite Vođeni tijek instalacije, bit ćete preusmjereni na ispravan portal za upravljanje kako biste dovršili instalaciju. Pogledajte pojedinosti o implementaciji kako biste dovršili instalaciju.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Postojeći klijenti sustava Dynamics upotrebljavaju aplikaciju Dynamics 365 Project Service Automation
Project Operations uključuje mogućnosti isporučene uz uslugu Project Service Automation. Putanja nadogradnje za te klijente objavit će se u budućnosti.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Postojeći klijenti aplikacije Dynamics 365 Finance upotrebljavaju Upravljanje projektima i računovodstvo 

Postojeći klijenti aplikacije Finance koji upotrebljavaju funkciju Upravljanje projektima i računovodstvo mogu je i dalje upotrebljavati takvu kakva jest. Pogledajte [Project Operations za scenarije sa zalihama / radnim nalozima](#pma).


## <a name="deployment-types"></a>Vrsta uvođenja
Project Operations podržava više mogućnosti uvođenja radi prilagodbe vašim zahtjevima. Bez obzira jeste li novi ili postojeći klijent sustava Dynamics 365, Project Operations može podržati vaše potrebe.

Naš [Upitnik za raspoređivanje](https://aka.ms/provisionprojectoperations) pomoći će vam pri određivanju ispravnog uvođenja. Rezultati će vas voditi prema jednoj od sljedećih vrsta uvođenja:

- [Jednostavno uvođenje – od sklapanja dogovora do proforma fakture](#lite)
- [Project Operations za scenarije temeljene na resursima / bez zaliha](#integrated)
- [Project Operations za scenarije temeljene na zalihama / radnim nalozima](#pma)

Project Operations podržava scenarije sa zalihama / proizvodnim nalozima i scenarije bez zaliha / na temelju resursa u istom okruženju putem konfiguracija na razini pravne osobe. Na primjer, Contoso može upotrebljavati mogućnosti skladištenja/narudžbe u svom američkom proizvodnom pogonu (pravna osoba = Contoso Manufacturing United States). Contoso može upotrebljavati mogućnosti koje nisu skladišne / koje su zasnovane na resursima u svojem servisnom pogonu Contoso Robotics Arms u Velikoj Britaniji (pravna osoba = Contoso Robotics Ujedinjeno Kraljevstvo).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Jednostavno uvođenje – od sklapanja dogovora do predračuna

Jednostavno uvođenje uključuje sljedeće mogućnosti:

- Planiranje projekta s pomoću aplikacije Microsoft Project za mrežu
- Višedimenzionalno određivanje cijena
- Objedinjeno upravljanja resursima
- Praćenje vremena
- Osnovni trošak
- Prijedlog fakture

#### <a name="deployment-steps"></a>Koraci uvođenja
Odredite najbolji model uvođenja aplikacije Project Operations s pomoću odjeljka [Upitnik za uvođenje](https://aka.ms/provisionprojectoperations).

Za ovo uvođenje pogledajte odjeljke [Prijava za pretplate na pretpregled](lite-preview-subscription-sign-up.md) i [Priprema novog okruženja](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations za scenarije temeljene na resursima / bez zaliha
Project Operations za scenarije s resursom / bez zaliha uključuju sljedeće mogućnosti:
  
- Planiranje projekta s pomoću aplikacije Microsoft Project za mrežu
- Višedimenzionalno određivanje cijena
- Objedinjeno upravljanja resursima
- Praćenje vremena
- Osnovni trošak
- Puni izdatak
- OCR računa
- Potpuno fakturiranje
- Priznavanje prihoda

#### <a name="deployment-steps"></a>Koraci uvođenja
Odredite najbolji model uvođenja aplikacije Project Operations s pomoću odjeljka [Upitnik za uvođenje](https://aka.ms/provisionprojectoperations).

Za ovo uvođenje pogledajte odjeljke [Prijava za pretplate na pretpregled](resource-sign-up-preview-subscription.md) i [Priprema novog okruženja](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations za scenarije temeljene na zalihama / radnim nalozima

- Planiranje projekta s pomoću WBS-a
- Upravljanje resursima
- Praćenje vremena
- Puni izdatak
- OCR računa
- Potpuno fakturiranje
- Priznavanje prihoda
- Proizvodni nalozi
- Podrška za materijale

#### <a name="deployment-steps"></a>Koraci uvođenja
Odredite najbolji model uvođenja aplikacije Project Operations s pomoću odjeljka [Upitnik za uvođenje](https://aka.ms/provisionprojectoperations).

Za ovo uvođenje pogledajte odjeljke [Prijava za pretplate na pretpregled](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Priprema novog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 

