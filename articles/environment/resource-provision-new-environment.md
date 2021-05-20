---
title: Priprema novog okruženja
description: U ovoj temi nalaze se informacije o načinu pripreme novog okruženja aplikacije Project Operations.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ee9e4c31d1972e3a75ad214071b31527f0ca826
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950525"
---
# <a name="provision-a-new-environment"></a>Priprema novog okruženja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

U ovoj temi nalaze se informacije o načinu omogućivanja novog okruženja aplikacije Dynamics 365 Project Operations za scenarije koji se temelje na resursu / bez zaliha.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Omogućivanje automatiziranu pripremu aplikacije Project Operations u LCS projektu

Poduzmite sljedeće korake kako biste omogućili automatizirani tijek pripreme za LCS projekt.

1. Idite na [LCS](https://lcs.dynamics.com/v2) i odaberite pločicu **Pregled upravljanja značajkama**.
2. U popisu **Značajka pregleda** odaberite **Značajka aplikacije Project Operations** i zatim odaberite **Omogućena značajka pregleda** kako biste omogućili aplikaciju Project Operations.

> [!NOTE]
> Ovaj korak izvodi se samo jedanput po LCS projektu.

## <a name="provision-a-project-operations-environment"></a>Priprema okruženja aplikacije Project Operations

1. Otvorite novo Dynamics 365 Finance [probno okruženje](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ili implementaciju [sigurnosne ograde / proizvodnog okruženja](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
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

7. Neobvezno – Primijenite pokazne podatke na okruženje. Idite na **Napredne postavke**, odaberite **Prilagodi konfiguraciju baze podataka SQL** i postavite mogućnost **Navedi skup podataka za bazu podataka aplikacije** na **Pokazno**.

8. Ispunite preostala potrebna polja u čarobnjaku i potvrdite implementaciju. Vrijeme pripreme okruženja razlikuje se ovisno o vrsti okruženja. Priprema može potrajati do šest sati.

  Nakon što se implementacija uspješno dovrši, okruženje će se prikazati kao **Implementirano**.

9. Kako biste potvrdili da se okruženje uspješno implementiralo, odaberite **Prijava** i prijavite se u okruženje radi potvrde.

![Pojedinosti  okruženja](./media/3EnvironmentDetails.png)

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

5. Odaberite oba rješenja, **Karta entiteta aplikacije Dynamics 365 Finance and Operations za dvostruko upisivanje** i **Karte entiteta aplikacije Dynamics 365 Project Operations za dvostruko upisivanje**, a zatim odaberite mogućnost **Primijeni**.

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

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Ažuriranje sigurnosnih postavki aplikacije Project Operations na platformi Dataverse

1. Idite na aplikaciju Project Operations u okruženju svoje platforme Dataverse. 
2. Idite na **Postavke** > **Sigurnost** > **Sigurnosne uloge**. 
3. S popisa uloga na stranici **Sigurnosne uloge**, odaberite **korisnik aplikacije za dvostruko pisanje** i odaberite karticu **Prilagođeni entiteti**.  
4. Provjerite ima li uloga dozvole **Čitanje** i **Dodaj na** za:
      
      - **Vrstu deviznog tečaja valute**
      - **Grafikon računa**
      - **Fiskalni kalendar**
      - **Knjiga**

5. Nakon ažuriranja sigurnosne uloge idite na **Postavke** > **Sigurnost** > **Teams** i odaberite zadani tim u timskom prikazu **Vlasnik lokalne tvrtke**.
6. Odaberite **Upravljanje ulogama** i provjerite primjenjuje li se sigurnosna ovlast **korisnik aplikacije za dvostruko pisanje** na ovaj tim.

## <a name="run-project-operations-dual-write-maps"></a>Pokretanje mapa dvostrukog zapisivanja aplikacije Project Operations

1. U svom LCS projektu idite na stranicu **Pojedinosti okruženja**.
2. Pod stavkom **Informacije o okruženju platforme Common Data Service** odaberite mogućnost **Veza na CDS za aplikacije**. Nakon što odaberete vezu, bit ćete preusmjereni na popis entiteta u mapiranjima.
3. Pokrenite mape na način opisan u sljedećoj tablici. Svakako slijedite redoslijed kako je naveden.

| **Karta entiteta** | **Osvježi entitet** | **Početna sinkronizacija** | **Glavni za početnu sinkronizaciju** | **Pokreni preduvjete** | **Početna sinkronizacija preduvjeta** |
| --- | --- | --- | --- | --- | --- |
| **Uloge aplikacije Project Resource za sve tvrtke (kategorije resursa koji se mogu rezervirati)** | No | Jest | Common Data Service | No | Nije dostupno |
| **Pravne osobe (cdm\_companies)** | No | Jest | Aplikacije Finance and Operations | No | Nije dostupno |
| **Glavna knjiga (msdyn_ledgers)** | No | Jest | Aplikacije Finance and Operations | Jest | Da, aplikacije Finance and Operations |
| **Stvarni podaci o integraciji aplikacije Project Operations (msdyn\_actuals)** | No | No | Nije dostupno | Jest | No |
| **Redci ugovora o projektu (pojedinosti prodajnog naloga)** | No | No | Nije dostupno | No | No |
| **Entitet integracije za odnose projektne transakcije (msdyn\_transactionconnections)** | No | No | Nije dostupno | No | Nije dostupno |
| **Kontrolne točke retka ugovora za integraciju aplikacije Project Operations (msdyn\_contractlinesscheduleofvalues)** | No | No | Nije dostupno | No | Nije dostupno |
| **Entitet za integraciju aplikacije Project Operations za procjene troškova (msdyn\_estimateslines)** | No | No | Nije dostupno | No | Nije dostupno |
| **Entitet izvoza kategorija troškova projekta za integraciju aplikacije Project Operations (msdyn\_expensecategories)** | No | No | Nije dostupno | No | Nije dostupno |
| **Entitet izvoza troškova projekta za integraciju aplikacije Project Operations (msdyn\_expenses)** | Jest | No | Nije dostupno | No | Nije dostupno |
| **Entitet za integraciju aplikacije Project Operations za procjene sati (msdyn\_resourceassignments)** | Jest | No | Nije dostupno | No | Nije dostupno |


4. Kako biste osvježili entitet, odaberite naziv mape, a zatim odaberite **Osvježi entitete**. 


![Osvježavanje mape](./media/20RefreshMapping.png)

5. Nakon završetka osvježavanja pokrenite mapu. Prije nego što omogućite sljedeću mapu, provjerite je li mapa u tablici u stanju **Izvodi se**. Izvođenje mapa s većim brojem preduvjeta može potrajati.

Kako biste pokrenuli mapu s preduvjetima, omogućite preklopni gumb **Prikaži povezane mape entiteta**. Ako je u tablici navedeno kako **Početna sinkronizacija preduvjeta** ima vrijednost **Ne**, prije pokretanja provjerite je li zastavica **Početna sinkronizacija** postavljena na **Isključeno** na svim mapama s preduvjetima.

![Pokretanje mape](./media/21RunMap.png)

6. Provjerite jesu li sve mape povezane s projektom u stanju aktivnosti.

![Sve mape rade](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Primjena konfiguracijskih podataka na platformi CDS za aplikaciju Project Operations (neobvezno)

Ako ste primijenili pokazne podatke u okruženju aplikacije Finance, pogledajte odjeljak [Postavljanje i primjena podataka na platformi Common Data Service za aplikaciju Project Operations](resource-apply-pro-setup-config-data.md) kako biste pokazne podatke primijenili na okruženje platforme CDS.


Vaše okruženje Project Operations sada je pripremljeno i konfigurirano. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]