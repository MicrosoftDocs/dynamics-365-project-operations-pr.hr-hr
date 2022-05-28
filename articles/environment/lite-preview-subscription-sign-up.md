---
title: Prijava za pretplatu na pretpregled – jednostavno
description: U ovoj temi nalaze se informacije o načinu pretplate i implementacije jednostavne aplikacije Project Operations – od sklapanja posla do predračuna.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3b06ac29e8021967490534d3aefc8b5ce733413b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587991"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Prijavite se za pretplatu na pretpregled – osnovno 

U ovoj se temi objašnjava način na koji se vrši pretplata na probnu ponudu i implementacija osnovne verzije aplikacije Dynamics 365 Project Operations – od sklapanja posla do predračuna.

> [!NOTE]
> Ovaj će se postupak promijeniti u predstojećim izdanjima aplikacije Project Operations.

## <a name="prerequisites"></a>Preduvjeti
- Korisnik koji uvodi pretpregled mora imati globalna prava administratora za klijent platforme Azure. Klijenta možete stvoriti tijekom iskorištavanja prve ponude.

> [!IMPORTANT]
> Samo jedna osoba u tvrtki ili ustanovi, administrator klijenta, mora izvršiti ovaj zadatak. Ako niste pretplatnik na ovo izdanje, pričekajte dok se vaša tvrtka ili ustanova ne prijavi i ne dobijete svoje vjerodajnice.
> 
> Probne verzije na klijentu upotrebljavaju se jednokratno. Probnu verziju možete pokrenuti samo jednom. Preporučujemo vam da u svrhu probne verzije stvorite novog klijenta.

### <a name="dynamics-365-project-operations-trial"></a>Probna verzija usluge Dynamics 365 Project Operations 

Prije nego što započnete, provjerite jeste li prijavljeni u preglednik s korisničkim radnim računom na klijentu u kojem želite pretpregled aplikacije Project Operations.

1. Idite na [Probnu verziju aplikacije Project Operations](https://aka.ms/try-po) kako biste iskoristili kôd prve ponude, **Dynamics 365 Project Operations**.
2. Potvrdite svoj nalog.

  Vidjet ćete da je ponuda o potvrdi uspješno iskorištena.

## <a name="assign-licenses"></a>Dodjela licenci

> [!IMPORTANT]
> Trebat će vam administrativni pristup portalu sustava Microsoft 365 vaše tvrtke ili ustanove za dovršetak sljedećih koraka.


1. Idite u [Microsoft 365 centar](https://portal.office.com/) za administratore da biste korisnicima dodijelili licence.
2. Na stranici **Aktivni korisnici** odaberite korisnike kojima želite dodijeliti licencu.
3. Provjerite je li odabrana licenca **Dynamics 365 Project Operations**. 
4. Odaberite **Spremi promjene**.

## <a name="create-a-new-dataverse-environment"></a>Izrada novog okruženja usluge Dataverse

1. Pripremite novo okruženje za implementaciju aplikacije Project Operations Dataverse slijedeći upute u temi, [Model implementacije aplikacije Dataverse](lite-deployment.md). Kad odaberete vrstu okruženja, obvezno upotrijebite **Probno razdoblje (na temelju pretplate)**.

  ![Novo okruženje.](./media/19CreateEnvironment.png)

2. Odaberite postavku **Omogući aplikacije sustava Dynamics 365** i mogućnost **Automatski postavi ove aplikacije** ostavite praznu.  
3. Odaberite **Spremi** kako biste stvorili okruženje.

  ![Dodaj bazu podataka.](./media/20CreateEnvironment1.png)

4. Nakon stvaranja okruženja, instalirajte rješenje **Microsoft Dynamics 365 Project Operations**. 

![Instalacija rješenja.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instaliranje CDS konfiguracije i postavljanje pokaznih podataka

Instalirajte CDS konfiguraciju i postavite pokazne podatke slijedeći upute u temi [Primjena pokaznih postavki i konfiguracijskih podataka](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
