---
title: Odredite vrstu implementacije
description: U ovoj temi nalaze se informacije koje vam pomažu pri određivanju ispravne vrste implementacije projektnih operacija za vašu tvrtku.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 4be8e69c5b6ff1ed65e9484a9b427bb428f7ff3e6dc597c615d5586da52867ef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994627"
---
# <a name="determine-your-deployment-type"></a>Odredite vrstu implementacije

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

> [!IMPORTANT]
> Nakon kupnje licence započnite ovdje kako biste odredili najbolji model implementacije aplikacije Dynamics 365 Project Operations s pomoću [tijeka Vođene instalacije](https://aka.ms/provisionprojectoperations).
> Nakon što dovršite Vođeni tijek instalacije, bit ćete preusmjereni na ispravan portal za upravljanje kako biste dovršili instalaciju. Pogledajte pojedinosti o implementaciji kako biste dovršili instalaciju.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Postojeći klijenti sustava Dynamics upotrebljavaju aplikaciju Dynamics 365 Project Service Automation
Project Operations uključuje mogućnosti isporučene uz uslugu Project Service Automation. Putanja nadogradnje objavit će se za te klijente u valu 1 izdanja za 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Postojeći klijenti aplikacije Dynamics 365 Finance upotrebljavaju Upravljanje projektima i računovodstvo 

Postojeći klijenti aplikacije Finance koji upotrebljavaju funkciju Upravljanje projektom i računovodstvo mogu je i dalje upotrebljavati takvu kakva jest. Pogledajte [Project Operations za scenarije sa zalihama / radnim nalozima](#pma).


## <a name="deployment-regions"></a>Regija implementacije
Kako biste utvrdili koje regije podržavaju implementaciju aplikacije Project Operations, pogledajte [Geografska dostupnost izvješća sustava Dynamics 365 i Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Odaberite **Prikaži izvješće** i proširite **Dynamics 365 > Operacijske aplikacije > Dynamics 365 Project Operations** kako biste vidjeli podržane regije.

## <a name="deployment-types"></a>Vrsta implementacije
Project Operations podržava više mogućnosti implementacije radi prilagodbe vašim zahtjevima. Bez obzira jeste li novi ili postojeći klijent sustava Dynamics 365, Project Operations može podržati vaše potrebe.

Naš [Upitnik za raspoređivanje](https://aka.ms/provisionprojectoperations) pomoći će vam pri određivanju ispravne implementacije. Rezultati će vas voditi prema jednoj od sljedećih vrsta implementacije:

- [Jednostavna implementacija – od sklapanja dogovora do proforma fakture](#lite)
- [Project Operations za scenarije temeljene na resursima / bez zaliha](#integrated)
- [Project Operations za scenarije temeljene na zalihama / radnim nalozima](#pma)

Project Operations podržava scenarije sa zalihama / proizvodnim nalozima i scenarije bez zaliha / na temelju resursa u istom okruženju putem konfiguracija na razini pravne osobe. Na primjer, Contoso može upotrebljavati mogućnosti narudžbe iz skladišta/proizvodnje u svom američkom proizvodnom pogonu (pravna osoba = Contoso proizvodnja Sjedinjene Države). Contoso može upotrebljavati mogućnosti bez zaliha / na temelju resursa u svojem servisnom objektu Contoso Robotics Arms u Velikoj Britaniji (pravna osoba = Contoso Robotics Ujedinjeno Kraljevstvo).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Osnovna implementacija – od sklapanja posla do predračuna

Jednostavna implementacija uključuje sljedeće mogućnosti:

- Postupak prodaje za projekte koji proširuju iskustva s aplikacijom Dynamics 365 Sales
- Planiranje projekta s pomoću aplikacije Microsoft Project for the Web
- Višedimenzionalno određivanje cijena
- Objedinjeno upravljanje resursima
- Praćenje vremena
- Osnovni trošak
- Predračun za pregled i uređivanje od strane voditelja projekta 

#### <a name="deployment-steps"></a>Koraci implementacije
Odredite najbolji model implementacije aplikacije Project Operations s pomoću odjeljka [Upitnik za implementaciju](https://aka.ms/provisionprojectoperations).

Za ovu implementaciju pogledajte odjeljke [Prijava za pretplate na pretpregled](lite-preview-subscription-sign-up.md) i [Priprema novog okruženja](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations za scenarije temeljene na resursima / bez zaliha
Project Operations za scenarije s resursom / bez zaliha uključuju sljedeće mogućnosti:
 
- Postupak prodaje za projekte koji proširuju aplikaciju Dynamics 365 Sales
- Planiranje projekta s pomoću aplikacije Microsoft Project for the Web
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
- Puni trošak
- OCR računa
- Potpuno fakturiranje
- Priznavanje prihoda
- Proizvodni nalozi
- Podrška materijalima na zalihi s inventarom

#### <a name="deployment-steps"></a>Koraci implementacije
Odredite najbolji model implementacije aplikacije Project Operations s pomoću odjeljka [Upitnik za implementaciju](https://aka.ms/provisionprojectoperations).

Za ovu implementaciju pogledajte odjeljke [Prijava za pretplate na pretpregled](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) i [Priprema novog okruženja](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]