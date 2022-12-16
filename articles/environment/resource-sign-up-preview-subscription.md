---
title: Prijavite se za pretplate za pretpregled aplikacije Project Operations za scenarije resursa / bez zalihe
description: U ovom se članku nalaze informacije o tome kako se pretplatiti na projektne operacije i uvesti ih za scenarije koji se temelje na resursima/nenaseljenim resursima.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3164add153d77a52f85c2aac442dcf90baa24440
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/10/2022
ms.locfileid: "9842006"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Prijavite se za pretplate za pretpregled aplikacije Project Operations za scenarije resursa / bez zalihe

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_



U ovom se članku objašnjava način na koji se vrši pretplata za probnu ponudu i implementacija okruženja aplikacije Project Operations za scenarije koji se temelje na resursima / bez zaliha.

## <a name="prerequisites"></a>Preduvjeti
- Korisnik koji uvodi pretpregled mora imati globalna prava administratora za klijent platforme Azure. Klijenta možete stvoriti tijekom iskorištavanja prve ponude. 
- Za implementaciju okruženja aplikacije Finance potrebna je valjana pretplata za platformu Azure koja će se naplaćivati po okruženju. Kako biste započeli, možete upotrijebiti postojeću pretplatu svoje tvrtke ili ustanove ili [probnu verziju platforme Azure](https://azure.microsoft.com/free/). CDS okruženje bit će besplatno za ograničeno razdoblje od 30 dana.

> [!IMPORTANT]
> Samo jedna osoba u tvrtki ili ustanovi, administrator klijenta, mora izvršiti ovaj zadatak. Ako niste pretplatnik na ovo izdanje, pričekajte dok se vaša tvrtka ili ustanova ne prijavi i ne dobijete svoje vjerodajnice.
> 
> Probne verzije na klijentu upotrebljavaju se jednokratno. Probnu verziju možete pokrenuti samo jednom. Preporučujemo vam da u svrhu probne verzije stvorite novog klijenta.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) – Probna verzija pretpregleda 

Prije nego što započnete, provjerite jeste li prijavljeni u preglednik s korisničkim radnim računom na klijentu u kojem želite pretpregled aplikacije Project Operations.

1. Iskoristite prvu šifru ponude, **Dynamics 365 Project Operations** ovdje [probna verzija aplikacije Project Operations](https://aka.ms/try-po).
2. Potvrdite svoj nalog.

  Vidjet ćete da je nalog potvrde uspješno iskorišten.

### <a name="dynamics-365-finance-preview-trial"></a>Probna verzija pretpregleda Dynamics 365 Finance

Idite na [Probnu verziju pretpregleda aplikacije Dynamics 365 for Finance](https://aka.ms/trypoche) i ponovite korake iz prethodnog odjeljka s ponudom, prijavite se za okruženje hostirano u oblaku.  

## <a name="assign-licenses"></a>Dodjela licenci

> [!IMPORTANT]
> Trebat će vam administrativni pristup portalu sustava Microsoft 365 vaše tvrtke ili ustanove za dovršetak sljedećih koraka.

1. Idite do [Centra za administratore sustava Microsoft 365](https://portal.office.com/) kako biste dodijelili licence svojim korisnicima.

2. Na stranici **Aktivni korisnici** odaberite korisnike kojima želite dodijeliti licencu.

3. Provjerite je li odabrana licenca **Dynamics 365 Project Operations** i odaberite **Spremi promjene**.

> [!NOTE]
> Ponudu za probnu aplikaciju Finance ne treba dodijeliti korisniku.

## <a name="start-a-new-project-in-lcs"></a>Pokretanje novog projekta u LCS-u

Stvaranje novog LCS projekta kako je opisano u članku [Pokretanje novog projekta u LCS-u](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Dodavanje pretplate za platformu Azure LCS projektu

Kako biste dovršili ovaj zadatak, slijedite korake u članku [Dodavanje pretplate za platformu Azure u LCS projekt](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implementiranje pokaznog okruženja aplikacije Finance s aplikacijom Project Operations za scenarije resursa / bez zalihe

Slijedite smjernice u članku [Dodjela novog okruženja](resource-provision-new-environment.md) kako biste dovršili implementaciju. Upotrijebite vrstu implementacije [pokaznog okruženja](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) za pretpregled. 

## <a name="install-cds-setup-and-configuration-data"></a>Instalacija postavljanja CDS-a i konfiguracijskih podataka

Instalirajte podatke o postavljanju i konfiguraciji CDS-a na način opisan u članku [Postavljanje i primjena konfiguracijskih podataka na platformi Common Data Service](resource-apply-pro-setup-config-data.md).
Dovršite ovaj korak tek nakon što se implementira pokazna verzija okruženja aplikacije Financije i pokazni podaci budu spremni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
