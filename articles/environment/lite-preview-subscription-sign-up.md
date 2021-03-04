---
title: Prijava za pretplatu na pretpregled – jednostavno
description: U ovoj temi nalaze se informacije o načinu pretplate i implementacije jednostavne aplikacije Project Operations – od sklapanja posla do predračuna.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6f4360b7febab57b97df0776ef9148d2a38f16a7
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175882"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Prijava za pretplatu na pretpregled – jednostavno 

U ovoj temi pojašnjava se način pretplate na pretpregled ponude partnera i implementacije jednostavne aplikacije Dynamics 365 Project Operations – od sklapanja posla do predračuna.

> [!NOTE]
> Ovaj će se postupak promijeniti u predstojećim izdanjima aplikacije Project Operations.

## <a name="prerequisites"></a>Preduvjeti

- Dobit ćete e-poštu s pozivom da sudjelujete u pretpregledu. Možete zatražiti pretpregled na [Web-mjestu aplikacije Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Korisnik koji uvodi pretpregled mora imati globalna prava administratora za klijent platforme Azure.
- Pregledajte sve uvjete i odredbe.

## <a name="subscribe"></a>Pretplata

Kada primite odobrenje [zahtjeva za pretpregled](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), e-poštom ćete primiti dvije ponude od tvrtke Microsoft. Te ponude omogućuju vam postavljanje pretpregleda aplikacije Project Operations:

- Dynamics 365 Project Operations (CRM) – Probni pretpregled
- Office 365 Project Operations –Probni pretpregled

> [!IMPORTANT]
> Samo jedna osoba u tvrtki ili ustanovi, administrator klijenta, mora izvršiti ovaj zadatak. Ako niste pretplatnik na ovo izdanje, pričekajte dok se vaša tvrtka ili ustanova ne prijavi i ne dobijete svoje vjerodajnice.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – Probni pretpregled 

Prije nego što započnete, provjerite jeste li prijavljeni u preglednik s korisničkim radnim računom na klijentu u kojem želite pretpregled aplikacije Project Operations.

1. Iskoristite kod iz prvu ponude, **Dynamics 365 Project Operations (CRM) – Probni pretpregled** tako da ga zalijepite u URL-adresu preglednika.

![Korištenje ponude](./media/16RedeemFirstOfferNew.png)

2. Potvrdite svoj nalog.
![Potvrda naloga](./media/17ConfirmOrderNew.png)

Vidjet ćete da je nalog potvrde uspješno iskorišten.

![Potvrda](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations –Probni pretpregled

Ponovite iste korake kao i s prvim kodom ponude. Obvezno dodajte kod iz druge ponude s pomoću istog korisničkog računa koji je upotrebljavan s kodom iz prve ponude.

## <a name="assign-licenses"></a>Dodjela licenci

> [!IMPORTANT]
> Trebat će vam administrativni pristup portalu sustava Microsoft 365 vaše tvrtke ili ustanove za dovršetak sljedećih koraka.


1. Idite do [Centra za administratore sustava Microsoft 365](https://portal.office.com/) kako biste dodijelili licence svojim korisnicima.

![Početna stranica Centra za administratore](./media/14AdminPortal.png)

2. Na stranici **Aktivni korisnici** odaberite korisnike kojima želite dodijeliti licencu.

![Dodjela licenci](./media/15AssignLicenses.png)

3. Provjerite jesu li odabrane licence **Pretpregled aplikacije Dynamics 365 Project Operations (CRM)** i **Office 365 Projektne operacije – Pretpregled**. 
4. Odaberite **Spremi promjene**.

## <a name="create-a-new-cds-environment"></a>Stvaranje novog CDS okruženja

1. Pripremite novo okruženje za implementaciju CDS-a aplikacije Project Operations slijedeći upute u temi [Model implementacije CDS-a](lite-deployment.md). Kad odaberete vrstu okruženja, obvezno upotrijebite **Probno razdoblje (na temelju pretplate)**.
![Novo okruženje](./media/19CreateEnvironment.png)

2. Odaberite postavku **Omogući aplikacije sustava Dynamics 365** i mogućnost **Automatski postavi ove aplikacije** ostavite praznu.  
3. Odaberite **Spremi** kako biste stvorili okruženje.

![Dodaj bazu podataka](./media/20CreateEnvironment1.png)

4. Nakon stvaranja okruženja, instalirajte rješenje **Microsoft Dynamics 365 Project Operations** . 

![Instalacija rješenja](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instaliranje CDS konfiguracije i postavljanje pokaznih podataka

Instalirajte CDS konfiguraciju i postavite pokazne podatke slijedeći upute u temi [Primjena pokaznih postavki i konfiguracijskih podataka](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]