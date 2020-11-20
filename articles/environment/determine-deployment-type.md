---
title: Odredite vrstu implementacije
description: U ovoj temi nalaze se informacije koje vam pomažu pri određivanju ispravne vrste implementacije projektnih operacija za vašu tvrtku.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401209"
---
# <a name="determine-your-deployment-type"></a>Odredite vrstu implementacije

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

> [!IMPORTANT]
> Nakon kupnje licence započnite ovdje kako biste odredili najbolji model implementacije aplikacije Dynamics 365 Project Operations s pomoću odjeljka [Vođeni tijek instalacije](https://aka.ms/provisionprojectoperations).
> Nakon što dovršite Vođeni tijek instalacije, bit ćete preusmjereni na ispravan portal za upravljanje kako biste dovršili instalaciju. Pogledajte pojedinosti o implementaciji kako biste dovršili instalaciju.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Postojeći klijenti sustava Dynamics upotrebljavaju aplikaciju Dynamics 365 Project Service Automation
Project Operations uključuje mogućnosti isporučene uz uslugu Project Service Automation. Putanja nadogradnje objavit će se za te klijente u valu 1 izdanja za 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Postojeći klijenti aplikacije Dynamics 365 Finance upotrebljavaju Upravljanje projektima i računovodstvo 

Postojeći klijenti aplikacije Finance koji upotrebljavaju funkciju Upravljanje projektom i računovodstvo mogu je i dalje upotrebljavati takvu kakva jest. Pogledajte [Project Operations za scenarije sa zalihama / radnim nalozima](#pma).


## <a name="deployment-types"></a>Vrsta implementacije
Project Operations podržava više mogućnosti implementacije radi prilagodbe vašim zahtjevima. Bez obzira jeste li novi ili postojeći klijent sustava Dynamics 365, Project Operations može podržati vaše potrebe.

Naš [Upitnik za raspoređivanje](https://aka.ms/provisionprojectoperations) pomoći će vam pri određivanju ispravne implementacije. Rezultati će vas voditi prema jednoj od sljedećih vrsta implementacije:

- [Jednostavna implementacija – od sklapanja dogovora do proforma fakture](#lite)
- [Project Operations za scenarije temeljene na resursima / bez zaliha](#integrated)
- [Project Operations za scenarije temeljene na zalihama / radnim nalozima](#pma)

Project Operations podržava scenarije sa zalihama / proizvodnim nalozima i scenarije bez zaliha / na temelju resursa u istom okruženju putem konfiguracija na razini pravne osobe. Na primjer, Contoso može upotrebljavati mogućnosti skladištenja/narudžbe u svom američkom proizvodnom pogonu (pravna osoba = Contoso Manufacturing United States). Contoso može upotrebljavati mogućnosti koje nisu skladišne / koje su zasnovane na resursima u svojem servisnom pogonu Contoso Robotics Arms u Velikoj Britaniji (pravna osoba = Contoso Robotics Ujedinjeno Kraljevstvo).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Jednostavna implementacija – od sklapanja dogovora do predračuna

Jednostavna implementacija uključuje sljedeće mogućnosti:

- Postupak prodaje za projekte koji proširuju iskustva s aplikacijom Dynamics 365 Sales
- Planiranje projekta s pomoću aplikacije Microsoft Project za mrežu
- Višedimenzionalno određivanje cijena
- Objedinjeno upravljanje resursima
- Praćenje vremena
- Osnovni trošak
- Predračun i fakturiranje prema klijentima 

#### <a name="deployment-steps"></a>Koraci implementacije
Odredite najbolji model implementacije aplikacije Project Operations s pomoću odjeljka [Upitnik za implementaciju](https://aka.ms/provisionprojectoperations).

Za ovu implementaciju pogledajte odjeljke [Prijava za pretplate na pretpregled](lite-preview-subscription-sign-up.md) i [Priprema novog okruženja](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations za scenarije temeljene na resursima / bez zaliha
Project Operations za scenarije s resursom / bez zaliha uključuju sljedeće mogućnosti:
 
- Postupak prodaje za projekte koji proširuju aplikaciju Dynamics 365 Sales
- Planiranje projekta s pomoću aplikacije Microsoft Project za mrežu
- Višedimenzionalno određivanje cijena
- Objedinjeno upravljanje resursima
- Praćenje vremena
- Osnovni trošak
- Puni trošak
- OCR računa
- Predračun i fakturiranje prema klijentima 
- Priznavanje prihoda za projekte

#### <a name="deployment-steps"></a>Koraci implementacije
Odredite najbolji model implementacije aplikacije Project Operations s pomoću odjeljka [Upitnik za implementaciju](https://aka.ms/provisionprojectoperations).

Za ovu implementaciju pogledajte odjeljke [Prijava za pretplate na pretpregled](resource-sign-up-preview-subscription.md) i [Priprema novog okruženja](resource-provision-new-environment.md). 


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

#### <a name="deployment-steps"></a>Koraci implementacije
Odredite najbolji model implementacije aplikacije Project Operations s pomoću odjeljka [Upitnik za implementaciju](https://aka.ms/provisionprojectoperations).

Za ovu implementaciju pogledajte odjeljke [Prijava za pretplate na pretpregled](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Priprema novog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 

