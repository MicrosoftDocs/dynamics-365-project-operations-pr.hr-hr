---
title: Prijavite se za pretplate za pretpregled aplikacije Project Operations za scenarije resursa / bez zalihe
description: U ovoj temi nalaze se informacije o načinu pretplate i implementiranja aplikacije Project Operations za scenarije koji se temelje na resursu / bez zalihe.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1b8c8982ede83191ce346e76718322d47abf0dd8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000427"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Prijavite se za pretplate za pretpregled aplikacije Project Operations za scenarije resursa / bez zalihe

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

U ovoj temi pojašnjava se način pretplate na pretpregled / ponudu partnera i implementaciju okruženja aplikacije Project Operations za scenarije koji se temelje na resursima / bez zaliha.

## <a name="prerequisites"></a>Preduvjeti

- Dobit ćete e-poštu s pozivom da sudjelujete u pretpregledu. Možete zatražiti pretpregled na [Web-mjestu aplikacije Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Korisnik koji uvodi pretpregled mora imati globalna prava administratora za klijent platforme Azure.
- Za implementaciju okruženja aplikacije Finance potrebna je valjana pretplata za platformu Azure koja će se naplaćivati po okruženju. Kako biste započeli, možete upotrijebiti postojeću pretplatu svoje tvrtke ili ustanove ili [probnu verziju platforme Azure](https://azure.microsoft.com/en-us/free/). CDS okruženje bit će besplatno za ograničeno razdoblje od 30 dana.

## <a name="subscribe"></a>Pretplata

Kada se odobri vaš [zahtjeva za pretpregled](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), e-poštom ćete primiti tri ponude od tvrtke Microsoft. Te ponude omogućuju vam postavljanje pretpregleda aplikacije Project Operations:

- Dynamics 365 Project Operations (CRM) – probni pretpregled
- Office 365 Project Operations –Probni pretpregled
- Probni pretpregled – Dynamics 365 Finance

> [!IMPORTANT]
> Samo jedna osoba u tvrtki ili ustanovi, administrator klijenta, mora izvršiti ovaj zadatak. Ako niste pretplatnik na ovo izdanje, pričekajte dok se vaša tvrtka ili ustanova ne prijavi i ne dobijete svoje vjerodajnice.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – probni pretpregled 

Prije nego što započnete, provjerite jeste li prijavljeni u preglednik s korisničkim radnim računom na klijentu u kojem želite pretpregled aplikacije Project Operations.

1. Iskoristite kod prve ponude, **Dynamics 365 Project Operations (CRM) – Pretpregled probe** tako da ga zalijepite na URL-adresu preglednika.

![Korištenje ponude](./media/16RedeemFirstOfferNew.png)

2. Potvrdite svoj nalog.

![Potvrda naloga](./media/17ConfirmOrderNew.png)

Vidjet ćete da je nalog potvrde uspješno iskorišten.

![Potvrda](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations –Probni pretpregled

Ponovite iste korake kao i s prvim kodom ponude. Obvezno dodajte kod iz druge ponude s pomoću istog korisničkog računa koji je upotrebljavan s kodom iz prve ponude.

### <a name="dynamics-365-finance-preview-trial"></a>Probni pretpregled aplikacije Dynamics 365 Finance

Ponovite iste korake s posljednjom ponudom iz e-pošte dobrodošlice.

## <a name="assign-licenses"></a>Dodjela licenci

> [!IMPORTANT]
> Trebat će vam administrativni pristup portalu sustava Microsoft 365 vaše tvrtke ili ustanove za dovršetak sljedećih koraka.

1. Idite do [Centra za administratore sustava Microsoft 365](https://portal.office.com/) kako biste dodijelili licence svojim korisnicima.

![Početna stranica Centra za administratore](./media/14AdminPortal.png)

2. Na stranici **Aktivni korisnici** odaberite korisnike kojima želite dodijeliti licencu.

![Dodjela licenci](./media/15AssignLicenses.png)

3. Provjerite je li odabrana licenca za aplikacije **Dynamics 365 Project Operations (CRM) Pretpregled** i **Office 365 Project Operations – Pretpregled** i odaberite mogućnost **Spremi promjene**.

> [!NOTE]
> Ponudu za probnu aplikaciju Finance ne treba dodijeliti korisniku.

## <a name="start-a-new-project-in-lcs"></a>Pokretanje novog projekta u LCS-u

Stvaranje novog LCS projekta kako je opisano u temi [Pokretanje novog projekta u LCS-u](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Dodavanje pretplate za platformu Azure LCS projektu

Kako biste dovršili ovaj zadatak, slijedite korake u temi [Dodavanje pretplate za platformu Azure u LCS projekt](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implementiranje pokaznog okruženja aplikacije Finance s aplikacijom Project Operations za scenarije resursa / bez zalihe

Slijedite smjernice u temi [Dodjela novog okruženja](resource-provision-new-environment.md) kako biste dovršili implementaciju. Upotrijebite vrstu implementacije [pokaznog okruženja](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) za pretpregled. 

## <a name="install-cds-setup-and-configuration-data"></a>Instalacija postavljanja CDS-a i konfiguracijskih podataka

Instalirajte podatke o postavljanju i konfiguraciji CDS-a na način opisan u temi [Postavljanje i primjena konfiguracijskih podataka na platformi Common Data Service](resource-apply-pro-setup-config-data.md).
Dovršite ovaj korak tek nakon što se implementira pokazna verzija okruženja aplikacije Finance i budu spremni pokazni podaci u FO.


[!INCLUDE[footer-include](../includes/footer-banner.md)]