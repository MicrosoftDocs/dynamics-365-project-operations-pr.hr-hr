---
title: Postavljanje i primjena konfiguracijskih podataka na platfomi Microsoft Dataverse
description: U ovom članku nalaze se informacije o načinu postavljanja i primjene konfiguracijskih podataka u aplikaciji Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b09d3ea7348082a0467fd7b47918c9e00d1f1e8c
ms.sourcegitcommit: 8edd24201cded2672cec16cd5dc84c6a3516b6c2
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2022
ms.locfileid: "9230228"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Postavljanje i primjena konfiguracijskih podataka na platfomi Common Data Service 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_



## <a name="prerequisites"></a>Preduvjeti

Prije nego što počnete konfigurirati podatke u aplikaciji Microsoft Dataverse, moraju se ispuniti sljedeći preduvjeti:

1.  Pružite okruženje platforme Dataverse i sustava Dynamics 365 Finance za aplikaciju Project Operations.
2.  Dijeljenje podataka o pravnoj osobi sustava Dynamics 365 Finance s okruženjem platforme Dataverse. To znači da entitet **Tvrtka** na platformi Dataverse ima sljedeće zapise o poduzeću:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Instalacija postavljanja i konfiguracijskih podataka

1. Preuzmite, deblokirajte i raspakirajte [Paket podataka za postavljanje i konfiguraciju](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).
2. Pomaknite se do raspakirane mape i pokrenite izvršnu datoteku *DataMigrationUtility*.
3. Na 1. stranici Čarobnjaka za migraciju konfiguracije (CMT) platforme Common Data Service odaberite **Uvez podatke** a zatim **Nastavi**.

![Migracija konfiguracije.](./media/1ConfigurationMigration.png)

4. Na 2. stranici CMT čarobnjaka odaberite **Microsoft 365** kao **Vrstu uvođenja**.
5. Označite potvrdne okvire **Prikaži popis dostupnih tvrtki ili ustanova** i **Prikaži napredne**.
6. Odaberite regiju svog klijenta, unesite svoje vjerodajnice, a zatim odaberite mogućnost **Prijava**.

![Konfiguracija prijave.](./media/2ConfigurationSignin.png)

7. Na 3. stranici, s popisa tvrtki ili ustanova na klijentu, odaberite u koju tvrtku ili ustanovu želite uvesti pokazne podatke, a zatim odaberite **Prijava**.
8. Na 4. stranici odaberite zip datoteku *SampleSetupAndConfigData* iz raspakirane mape.

![Odabir zip datoteke.](./media/3ZipFile.png)

![Odabir datoteke.](./media/4SelectAFile.png)

9. Nakon odabira zip datoteke odaberite **Uvezi podatke**.

![Uvezi podatke.](./media/5ImportData.png)

10. Uvoz će se izvoditi otprilike dvije do deset minuta, ovisno o brzini vaše mreže. Po završetku uvoza izađite iz CMT čarobnjaka. 
11. U svojoj tvrtki ili ustanovi provjerite podatke za sljedećih 26 entiteta:

  - Valuta
  - Grafikon računa
  - Fiskalni kalendar
  - Vrste deviznih tečajeva
  - Dan plaćanja
  - Raspored plaćanja
  - Uvjet plaćanja
  - Organizacijska jedinica
  - Kontakt
  - Porezna grupa
  - Grupa klijenata
  - Grupa dobavljača
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

![Dovrši uvoz.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Ažuriranje konfiguracija aplikacije Project Operations

1. Pomaknite se do CE okruženja. Možete ga pronaći otvaranjem [Centra za administratore aplikacije Power Platform](https://admin.powerplatform.microsoft.com/environments), odabirom okruženja i potom mogućnosti **Otvori okruženje**. 

![Otvaranje okruženja.](./media/7OpenEnvironment.png)

2. Idite na **Projekti** > **Resursi**, a zatim odaberite **Novi** kako biste svojem korisniku stvorili resurs koji se može rezervirati.

![Resursi koji se mogu rezervirati.](./media/8BookableResources.png)

3. Na kartici **Općenito** odaberite svog korisnika administratora. Provjerite podudara li se vremenska zona s onom u kojoj se nalazite. 

![Novi resurs koji se može rezervirati.](./media/9NewBookableResource.png)

4. Na kartici **Planiranje**, u polju **Tvrtka**, odaberite tvrtku **USPM**, a zatim odaberite **Spremi**. 

![Kartica planiranja.](./media/10SchedulingTab.png)

5. Odaberite karticu **Radno vrijeme**.  

![Radni sati.](./media/11WorkHours.png)

6. Dvaput kliknite neku vrijednost u kalendaru i odaberite **Uredi** > **Svi događaji u nizu**. 

![Radni kalendar.](./media/12WorkCalendar.png)

7. Promijenite radno vrijeme u osmosatni (8) radni dan, obilježite vikende kao neradne dane i pobrinite se da se vremenska zona poklapa s vašom. 
8. Odaberite **Spremi i zatvori**.

![Ažuriranje kalendara.](./media/13UpdateCalendar.png)

9. Idite na **Postavke** > **Predlošci kalendara** i odaberite **Novi**.
 
 ![Predlošci kalendara.](./media/14CalendarTemplates.png)
 
 10. Unesite naziv, odaberite resurs predloška koji ste stvorili, a zatim odaberite **Spremi**. 
 
 ![Spremanje predloška kalendara.](./media/15SaveCalendarTemplate.png)
 
 11. Idite na stavku **Parametri** i dvaput kliknite zapis. 
 
 ![Parametri projekta.](./media/16ProjectParameters.png)
 
12. Ažurirajte sljedeća polja:

 - **Zadana tvrtka**: USPM
 - **Zadana organizacijska jedinica** : Contoso Robotics Global
 - **Učestalost faktura**: Sedmi i posljednji dan
 - **Predložak radnog vremena**: Zamijenite s predloškom koji ste stvorili.

13. Odaberite **Spremi**. 

![Ažuriranje parametara projekta.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
