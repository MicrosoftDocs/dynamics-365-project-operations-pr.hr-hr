---
title: Prijavite se za pretplatu na pretpregled – osnovno
description: U ovom se članku navode informacije o tome kako se pretplatiti i uvesti implementaciju lite implementacije Project Operations - deal to proforma fakturiranje.
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

Ovaj članak objašnjava kako se pretplatiti na probnu ponudu i implementirati Dynamics 365 Project Operations lite implementaciju - dogovor o proforma fakturiranju.

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

1. Dodijelite novo okruženje za implementaciju operacija Dataverse projekta slijedeći upute u članku, [Dataverse model implementacije](lite-deployment.md). Kad odaberete vrstu okruženja, obvezno upotrijebite **Probno razdoblje (na temelju pretplate)**.

  ![Novo okruženje.](./media/19CreateEnvironment.png)

2. Odaberite postavku **Omogući aplikacije sustava Dynamics 365** i mogućnost **Automatski postavi ove aplikacije** ostavite praznu.  
3. Odaberite **Spremi** kako biste stvorili okruženje.

  ![Dodaj bazu podataka.](./media/20CreateEnvironment1.png)

4. Nakon stvaranja okruženja, instalirajte rješenje **Microsoft Dynamics 365 Project Operations**. 

![Instalacija rješenja.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Postavljanje demo podataka

Postavite demo podatke slijedeći upute u članku Primijenite [podatke o postavljanju demo zapisa i konfiguraciji](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
