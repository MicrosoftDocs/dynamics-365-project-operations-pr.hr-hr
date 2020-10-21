---
title: Prijavite se za pretplate za pretpregled aplikacije Project Operations za scenarije resursa / bez zalihe
description: U ovoj temi nalaze se informacije o načinu pretplate i implementiranja aplikacije Project Operations za scenarije koji se temelje na resursu / bez zalihe.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948792"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Prijavite se za pretplate za pretpregled aplikacije Project Operations za scenarije resursa / bez zalihe

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovoj temi pojašnjava se način pretplate na pretpregled / ponudu partnera i implementaciju okruženja aplikacije Project Operations za scenarije koji se temelje na resursima / bez zaliha.

## <a name="prerequisites"></a>Preduvjeti

- Dobit ćete e-poštu s pozivom da sudjelujete u pretpregledu. Možete zatražiti pretpregled na [Web-mjestu aplikacije Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Korisnik koji uvodi pretpregled mora imati globalna prava administratora za klijent platforme Azure.
- Za implementaciju okruženja aplikacije Finance potrebna je valjana pretplata za platformu Azure koja će se naplaćivati po okruženju. Kako biste započeli, možete upotrijebiti postojeću pretplatu svoje tvrtke ili ustanove ili [probnu verziju platforme Azure](https://azure.microsoft.com/en-us/free/). CDS okruženje bit će besplatno za ograničeno razdoblje od 30 dana.

## <a name="subscribe"></a>Pretplata

Kada se odobri vaš [zahtjeva za pretpregled](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), e-poštom ćete primiti dvije ponude od tvrtke Microsoft. Te ponude omogućuju vam postavljanje pretpregleda aplikacije Project Operations:

- Dynamics 365 Project Operations – Probni pretpregled
- Probni pretpregled aplikacije Dynamics 365 for Finance and Operations

> [!IMPORTANT]
> Samo jedna osoba u tvrtki ili ustanovi, administrator klijenta, mora izvršiti ovaj zadatak. Ako niste pretplatnik na ovo izdanje, pričekajte dok se vaša tvrtka ili ustanova ne prijavi i ne dobijete svoje vjerodajnice.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – probni pretpregled

1. Iskoristite prvu ponudu **Probne aplikacije Dynamics 365 Project Operations** s pomoću URL-adrese navedene u poruci dobrodošlice koju ste dobili e-poštom.

![Prva ponuda](./media/1FirstOffer.png)

2. Provjerite jeste li prijavljeni kao korisnik koji pripada tvrtki ili ustanovi koja će se pretplatiti na uslugu.
3. Nastavite s iskorištavanjem ponude. 
4. Odaberite **Da, dodaj na moj račun**.

![Korištenje ponude](./media/2RedeemFirstOffer.png)

![Potvrda ponude](./media/3ConfirmFirstOffer.png)

![Ponuda iskorištena](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Probni pretpregled aplikacije Dynamics 365 Finance

Ponovite iste korake s drugom ponudom iz e-pošte dobrodošlice.

## <a name="assign-licenses"></a>Dodjela licenci

> [!IMPORTANT]
> Trebat će vam administrativni pristup portalu sustava Office 365 vaše tvrtke ili ustanove za dovršetak sljedećih koraka.

1. Idite do [Centra za administratore sustava Microsoft 365](https://portal.office.com/) kako biste dodijelili licence svojim korisnicima.

![Administratorski portal aplikacije Office](./media/5OfficeAdminPortal.png)

2. Na stranici **Aktivni korisnici** odaberite korisnike kojima želite dodijeliti licencu.

![Dodjela licenci](./media/6AssignLicenses.png)

3. Provjerite je li odabrana licenca za aplikaciju Project Operations i odaberite **Spremi promjene**. 

> [!NOTE]
> Ponudu za probnu aplikaciju Finance ne treba dodijeliti korisniku.

## <a name="start-a-new-project-in-lcs"></a>Pokretanje novog projekta u LCS-u

Stvaranje novog LCS projekta kako je opisano u temi [Pokretanje novog projekta u LCS-u](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Dodavanje pretplate za platformu Azure LCS projektu

Kako biste dovršili ovaj zadatak, slijedite korake u temi [Dodavanje pretplate za platformu Azure u LCS projekt](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implementiranje pokaznog okruženja aplikacije Finance s aplikacijom Project Operations za scenarije resursa / bez zalihe

Slijedite smjernice u temi [Dodjela novog okruženja](resource-provision-new-environment.md) kako biste dovršili implementaciju. Upotrijebite vrstu implementacije [pokaznog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) za pretpregled.

## <a name="install-cds-setup-and-configuration-data"></a>Instalacija postavljanja CDS-a i konfiguracijskih podataka

Instalirajte podatke o postavljanju i konfiguraciji CDS-a na način opisan u temi [Postavljanje i primjena konfiguracijskih podataka na platformi Common Data Service](resource-apply-pro-setup-config-data.md).

