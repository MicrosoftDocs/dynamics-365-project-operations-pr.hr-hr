---
title: Prijavite se za pretplatu na pretpregled – osnovno
description: U ovom se članku navode informacije o načinu pretplate i implementacije jednostavne aplikacije Project Operations – od sklapanja posla do predračuna.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 29bf31cd1bc9c1c5ac757de989154b4c7acc53fe
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410002"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Prijavite se za pretplatu na pretpregled – osnovno 

U ovom se članku objašnjava način na koji se vrši pretplata na probnu ponudu i implementacija osnovne verzije aplikacije Dynamics 365 Project Operations – od sklapanja posla do predračuna.

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


1. Idite do [Centra za administratore sustava Microsoft 365](https://portal.office.com/) kako biste dodijelili licence svojim korisnicima.
2. Na stranici **Aktivni korisnici** odaberite korisnike kojima želite dodijeliti licencu.
3. Provjerite je li odabrana licenca **Dynamics 365 Project Operations**. 
4. Odaberite **Spremi promjene**.

## <a name="create-a-new-dataverse-environment"></a>Izrada novog okruženja usluge Dataverse

1. Pripremite novo okruženje za implementaciju aplikacije Project Operations Dataverse slijedeći upute u članku [Model implementacije aplikacije Dataverse](lite-deployment.md). Kad odaberete vrstu okruženja, obvezno upotrijebite **Probno razdoblje (na temelju pretplate)**.

  ![Novo okruženje.](./media/19CreateEnvironment.png)

2. Odaberite postavku **Omogući aplikacije sustava Dynamics 365** i mogućnost **Automatski postavi ove aplikacije** ostavite praznu.  
3. Odaberite **Spremi** kako biste stvorili okruženje.

  ![Dodaj bazu podataka.](./media/20CreateEnvironment1.png)

4. Nakon stvaranja okruženja, instalirajte rješenje **Microsoft Dynamics 365 Project Operations**. 

![Instalacija rješenja.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Postavljanje pokaznih podataka

Postavite pokazne podatke slijedeći upute u članku [Primjena pokaznih postavki i konfiguracijskih podataka](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
