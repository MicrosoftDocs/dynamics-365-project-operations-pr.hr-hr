---
title: Priprema novog okruženja
description: U ovoj temi nalaze se informacije o načinu pripreme novog okruženja aplikacije Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949353"
---
# <a name="provision-a-new-environment"></a>Priprema novog okruženja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovoj temi nalaze se informacije o načinu pripreme okruženja aplikacije Dynamics 365 Project Operations za scenarije koji se temelje na resursu / bez zalihe.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Omogućivanje automatiziranu pripremu aplikacije Project Operations u LCS projektu

Poduzmite sljedeće korake kako biste omogućili automatizirani tijek pripreme za LCS projekt.

1. Idite na [LCS](https://lcs.dynamics.com/v2) i odaberite pločicu **Pregled upravljanja značajkama**.
2. U popisu **Značajka pregleda** odaberite **Project Operations** i odabrani **Omogućena značajka pregleda** kako biste omogućili aplikaciju Project Operations.

> [!NOTE]
> Ovaj korak izvodi se samo jedanput po LCS projektu.

## <a name="provision-a-project-operations-environment"></a>Priprema okruženja aplikacije Project Operations

1. Otvorite novo Dynamics 365 Finance [probno okruženje](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ili implementaciju [sigurnosne ograde / proizvodnog okruženja](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Upoznajte se s radom čarobnjaka **Priprema okruženja**. 

> [!IMPORTANT]
> Provjerite je li odabrana verzija aplikacije 10.0.13 ili novija.

3. Za pripremu aplikacije Project Operations, pod stavkom **Napredne postavke** odaberite **Common Data Service**. 
4. Omogućite **Postavljanje platforme Common Data Service** odabirom mogućnosti **Da** a zatim u obvezna polja unesite podatke:

  - Ime
  - Regija
  - Jezik
  - Valuta
 
5. U polju **Predložak platforme Common Data Service** odaberite **Project Operations** 

6. Odaberite vrstu okruženja za implementaciju. Probno razdoblje koje se temelji na pretplati omogućit će vam postavljanje CDS okruženja na 30 dana. 

![Postavke implementacije](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Odaberite **Slažem se** kako biste se potvrdili uvjete usluge i zatim odaberite **Gotovo** za povratak na postavke implementacije.

![Pristanak za implementaciju](./media/2DeploymentConsent.png)

7. Ispunite preostala potrebna polja u čarobnjaku i potvrdite implementaciju. Vrijeme pripreme okruženja razlikuje se ovisno o vrsti okruženja. Priprema može potrajati do šest sati.

  Nakon što se implementacija uspješno dovrši, okruženje će se prikazati kao **Implementirano**.

8. Kako biste potvrdili da je okruženje uspješno implementirano, odaberite mogućnost **Prijava** i prijavite se u okruženje kako biste to potvrdili.

![Pojedinosti  okruženja](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Primjena pokaznih podataka aplikacije Project Operations Finance (neobvezni korak)

Primijenite pokazne podatke aplikacije Project Operations Finance na izdanje usluge Okruženje hostirano u oblaku 10.0.13 na način opisan u [ovom članku](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Primjena ažuriranja na okruženje aplikacije Finance.

Project Operations zahtijeva okruženje aplikacije Finance verzije **10.0.13 (10.0.569.20009)** ili više.

Možda ćete trebati primijeniti kvalitativna ažuriranja u svom okruženju aplikacije Finance kako biste primili ovu verziju.

1. Na stranici **Pojedinosti okruženja** LSC-a, u odjeljku **Dostupna ažuriranja**, odaberite **Pogledajte ažuriranje**.

![Prikaz ažuriranja](./media/5ViewUpdates.png)

2. Na stranici **Binarna ažuriranja** odaberite **Spremi paket**.

![Spremanje paketa](./media/6SavePackage.png)

3. Kliknite **Odberi sve** i zatim odaberite **Spremi paket**.

![Pregled i spremanje ažuriranja](./media/7ReviewAndSaveUpdates.png)

4. Unesite ime i opis paketa, a zatim odaberite **Spremi**. Ovisno o internetskoj vezi, ovaj postupak može potrajati.

![Prenesite paket u biblioteku Sredstva](./media/8UploadPackageToAssetsLibrary.png)

5. Nakon spremanja paketa odaberite **Gotovo** i spremite ovaj paket u biblioteku Sredstava svojeg LCS projekta.

Spremanje i provjera valjanosti paketa može potrajati oko 15 minuta.

6. Kako biste primijenili ažuriranje, pomaknite se na stranicu **Pojedinosti okruženja** u LCS-u i odaberite **Održavaj** > **Primijeni ažuriranja**.

![Održavanje okruženja](./media/9MaintainEnvironment.png)

7. Na popisu ažuriranja odaberite paket koji ste stvorili, a zatim **Prijava**.

![Primjena ažuriranja](./media/10ApplyUpdates.png)

Održavanje okruženja potrajat će neko vrijeme. Nakon završetka, okruženje će se vratiti u implementirano stanje.

![Okruženje implementirano](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Uspostavljanje veze dvostrukog zapisivanja 

1. U svom LCS projektu idite na stranicu **Pojedinosti okruženja**.
2. Pod stavkom **Informacije o okruženju platforme Common Data Service** odaberite mogućnost **Veza na CDS za aplikacije**.
3. Nakon dovršetka veze ponovno odaberite mogućnost **Veza na CDS za aplikacije**. Bit ćete preusmjereni na dvostruko zapisivanje u aplikaciji Finance.

![Veza na CDS](./media/12LinktoCDS.png)

4. Odaberite **Primjeni rješenje** kako biste pristupili entitetima koji će biti mapirani u integraciju.

![Primjena rješenja](./media/13ApplySolutions.png)

5. Odaberite oba rješenja, **Dvostruko zapisivanje mape entiteta aplikacije Dynamics 365 Finance and Operations** i **Dvostruko zapisivanje mapa entiteta aplikacije Dynamics 365 Project Operations**, a zatim odaberite**Prijava**.

![Potvrda rješenja](./media/14ConfirmSolutions.png)

Nakon primjene rješenja, entiteti dvostrukog zapisivanja primjenjuju se na okruženje.

![Primjena rješenja](./media/15ApplyingSolutions.png)

Nakon primjene entiteta, sva raspoloživa mapiranja navedena su u okruženju.

![Mape dvostrukog zapisivanja](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Osvježavanje podatkovnih entiteta nakon ažuriranja

1. U aplikaciji Finance, idite na radni prostor **Upravljanje podacima**.

![Radni prostor upravljanja podacima](./media/16DataManagement.png)

2. Odaberite pločicu **Parametri okvira**.

![Parametri okvira](./media/17FrameworkParameters.png)

3. Na stranici **Postavke entiteta**, odaberite mogućnost **Osvježi popis entiteta**.

![Osvježavanje popisa entiteta](./media/18RefreshEntityList.png)

Osvježavanje će potrajati otprilike 20 minuta. Kada bude dovršeno dobit ćete upozorenje.

![Potvrda osvježavanja](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Pokretanje mapa dvostrukog zapisivanja aplikacije Project Operations

1. U svom LCS projektu idite na stranicu **Pojedinosti okruženja**.
2. Pod stavkom **Informacije o okruženju platforme Common Data Service** odaberite mogućnost **Veza na CDS za aplikacije**. Nakon što odaberete vezu, bit ćete preusmjereni na popis entiteta u mapiranjima.
3. Pokrenite mape na način opisan u sljedećoj tablici. Svakako slijedite redoslijed kako je naveden.

| **Karta entiteta** | **Osvježi entitet** | **Početna sinkronizacija** | **Glavni za početnu sinkronizaciju** | **Pokreni preduvjete** | **Početna sinkronizacija preduvjeta** |
| --- | --- | --- | --- | --- | --- |
| **Uloge aplikacije Project Resource za sve tvrtke (kategorije resursa koji se mogu rezervirati)** | No | Jest | Common Data Service | No | Nije dostupno |
| **Pravne osobe (cdm\_companies)** | No | Jest | Aplikacije Finance and Operations | No | Nije dostupno |
| **Stvarni podaci o integraciji aplikacije Project Operations (msdyn\_actuals)** | No | No | Nije dostupno | Jest | No |
| **Redci ugovora o projektu (pojedinosti prodajnog naloga)** | No | No | Nije dostupno | No | No |
| **Entitet integracije za odnose projektne transakcije (msdyn\_transactionconnections)** | No | No | Nije dostupno | No | Nije dostupno |
| **Kontrolne točke retka ugovora za integraciju aplikacije Project Operations (msdyn\_contractlinesscheduleofvalues)** | No | No | Nije dostupno | No | Nije dostupno |
| **Entitet za integraciju aplikacije Project Operations za procjene troškova (msdyn\_estimateslines)** | No | No | Nije dostupno | No | Nije dostupno |
| **Entitet za integraciju aplikacije Project Operations za procjene sati (msdyn\_resourceassignments)** | No | No | Nije dostupno | No | Nije dostupno |
| **Entitet izvoza troškova projekta za integraciju aplikacije Project Operations (msdyn\_expenses)** | Jest | No | Nije dostupno | No | Nije dostupno |
| **Entitet za integraciju aplikacije Project Operations za procjene sati (msdyn\_resourceassignments)** | Jest | No | Nije dostupno | No | Nije dostupno |

4. Kako biste osvježili entitet, odaberite naziv mape, a zatim odaberite **Osvježi entitete**. 
5. Nakon završetka osvježavanja nastavite s izvođenjem mape.

![Osvježavanje mape](./media/20RefreshMapping.png)

Prije nego što omogućite sljedeću mapu, provjerite je li mapa u tablici u stanju **Izvodi se**. Izvođenje mapa s većim brojem preduvjeta može potrajati.

Kako biste pokrenuli mapu s preduvjetima, omogućite preklopni gumb **Prikaži povezane mape entiteta**. Ako je u tablici navedeno kako **Početna sinkronizacija preduvjeta** ima vrijednost **Ne**, prije pokretanja provjerite je li zastavica **Početna sinkronizacija** postavljena na **Isključeno** na svim mapama s preduvjetima.

![Pokretanje mape](./media/21RunMap.png)

6. Provjerite jesu li sve mape povezane s projektom u stanju aktivnosti.

![Sve mape rade](./media/22AllMapsRunning.png)

Vaše okruženje Project Operations sada je pripremljeno i konfigurirano.
