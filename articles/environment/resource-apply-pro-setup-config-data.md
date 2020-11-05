---
title: Postavljanje i primjena konfiguracijskih podataka na platformi Common Data Service za aplikaciju Project Operations
description: U ovoj temi nalaze se informacije o načinu postavljanja i primjene konfiguracijskih podataka u aplikaciji Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073261"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a>Postavljanje i primjena konfiguracijskih podataka na platformi Common Data Service za aplikaciju Project Operations

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

## <a name="install-setup-and-configuration-data"></a>Instalacija postavljanja i konfiguracijskih podataka

1. Preuzmite, deblokirajte i raspakirajte [Paket podataka za postavljanje i konfiguraciju](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Pomaknite se do raspakirane mape i pokrenite izvršnu datoteku *DataMigrationUtility*.
3. Na 1. stranici Čarobnjaka za migraciju konfiguracije (CMT) platforme Common Data Service odaberite **Uvez podatke** a zatim **Nastavi**.

![Migracija konfiguracije](./media/1ConfigurationMigration.png)

4. Na 2. stranici CMT čarobnjaka odaberite **Microsoft 365** kao **Vrstu implementacije**.
5. Označite potvrdne okvire **Prikaži popis dostupnih tvrtki ili ustanova** i **Prikaži napredne**.
6. Odaberite regiju svog klijenta, unesite svoje vjerodajnice, a zatim odaberite mogućnost **Prijava**.

![Konfiguracija prijave](./media/2ConfigurationSignin.png)

7. Na 3. stranici, s popisa tvrtki ili ustanova na klijentu, odaberite u koju tvrtku ili ustanovu želite uvesti pokazne podatke, a zatim odaberite **Prijava**.
8. Na 4. stranici odaberite zip datoteku *SampleSetupAndConfigData* iz raspakirane mape.

![Odabir zip datoteke](./media/3ZipFile.png)

![Odaberite datoteku](./media/4SelectAFile.png)

9. Nakon odabira zip datoteke odaberite **Uvezi podatke**.

![Uvoz podataka](./media/5ImportData.png)

10. Uvoz će se izvoditi otprilike dvije do deset minuta, ovisno o brzini vaše mreže. Po završetku uvoza izađite iz CMT čarobnjaka. 
11. U svojoj tvrtki ili ustanovi provjerite podatke za sljedećih 19 entiteta:

  - Valuta
  - Organizacijska jedinica
  - Kontakt
  - Porezna grupa
  - Grupa klijenata
  - Jedinica
  - Grupa jedinica
  - Cjenik
  - Cjenik parametara projekta
  - Učestalost fakturiranja
  - Kategorija resursa koji je moguće rezervirati
  - Kategorija transakcije
  - Kategorija troška
  - Cijena uloge
  - Cijena kategorije transakcije
  - Značajka
  - Resurs koji je moguće rezervirati
  - Dodjela kategorije resursa kojeg je moguće rezervirati
  - Značajka kategorije resursa koji je moguće rezervirati

![Dovrši uvoz](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Ažuriranje konfiguracija aplikacije Project Operations

1. Pomaknite se do CE okruženja. Možete ga pronaći otvaranjem [Centra za administratore aplikacije Power Platform](https://admin.powerplatform.microsoft.com/environments), odabirom okruženja i potom mogućnosti **Otvori okruženje**. 

![Otvaranje okruženja](./media/7OpenEnvironment.png)

2. Idite na **Projekti** > **Resursi** , a zatim odaberite **Novi** kako biste svojem korisniku stvorili resurs koji se može rezervirati.

![Resursi koje je moguće rezervirati](./media/8BookableResources.png)

3. Na kartici **Općenito** odaberite svog korisnika administratora. Provjerite podudara li se vremenska zona s onom u kojoj se nalazite. 

![Novi resurs koji se može rezervirati](./media/9NewBookableResource.png)

4. Na kartici **Planiranje** , u polju **Tvrtka** , odaberite tvrtku **USPM** , a zatim odaberite **Spremi**. 

![Kartica planiranja](./media/10SchedulingTab.png)

5. Odaberite karticu **Radno vrijeme**.  

![Radno vrijeme](./media/11WorkHours.png)

6. Dvaput kliknite neku vrijednost u kalendaru i odaberite **Uredi** > **Svi događaji u nizu**. 

![Radni kalendar](./media/12WorkCalendar.png)

7. Promijenite radno vrijeme u osmosatni (8) radni dan, obilježite vikende kao neradne dane i pobrinite se da se vremenska zona poklapa s vašom. 
8. Odaberite **Spremi i zatvori**.

![Ažuriranje kalendara](./media/13UpdateCalendar.png)

9. Idite na **Postavke** > **Predlošci kalendara** i odaberite **Novi**.
 
 ![Predlošci kalendara](./media/14CalendarTemplates.png)
 
 10. Unesite naziv, odaberite resurs predloška koji ste stvorili, a zatim odaberite **Spremi**. 
 
 ![Spremanje predloška kalendara](./media/15SaveCalendarTemplate.png)
 
 11. Idite na stavku **Parametri** i dvaput kliknite zapis. 
 
 ![Parametri projekta](./media/16ProjectParameters.png)
 
12. Ažurirajte sljedeća polja:

 - **Zadana tvrtka** : USPM
 - **Zadana organizacijska jedinica** : Contoso Robotics Global
 - **Učestalost faktura** : Sedmi i posljednji dan
 - **Predložak radnog vremena** : Zamijenite s predloškom koji ste stvorili.

13. Odaberite **Spremi**. 

![Ažuriranje parametara projekta](./media/17UpdatedProjectParameters.png)
