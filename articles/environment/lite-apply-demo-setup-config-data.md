---
title: Primjena probnog postavljanja i konfiguracija podataka – jednostavno
description: U ovom se članku navode informacije o načinu primjene pokaznih postavki i konfiguracijskih podataka za aplikaciju Project Operations.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811016"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Primjena podataka postavljanja pokazne verzije i konfiguracije za aplikaciju Project Operations – jednostavno 

_**Jednostavna implementacija – od sklapanja posla do predračuna_



## <a name="prerequisites"></a>Preduvjeti

Prije nego započnete konfiguriranje, morate imati okruženje platforme Dataverse pripremljeno za aplikaciju Dynamics 365 Project Operations.


## <a name="instructions"></a>Upute

1. Preuzmite paket instalacijskih [podataka](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Dođite do mape *ProjOpsSampleSetupData – CE samo CMT* i pokrenite izvršnu datoteku *DataMigrationUtility*.
1. Na 1. stranici Čarobnjaka za migraciju konfiguracije (CMT) platforme Common Data Service odaberite **Uvez podatke** a zatim **Nastavi**.

    ![Migracija konfiguracije.](./media/1ConfigurationMigration.png)

1. Na 2. stranici CMT čarobnjaka odaberite **Microsoft 365** kao **Vrstu uvođenja**.
1. Označite potvrdne okvire **Prikaži popis dostupnih tvrtki ili ustanova** i **Prikaži napredne**.
1. Odaberite regiju svog klijenta, unesite svoje vjerodajnice, a zatim odaberite **Prijava**.

   ![Konfiguracija prijave.](./media/2ConfigurationSignin.png)

1. Na 3. stranici, s popisa tvrtki ili ustanova na klijentu odaberite u koju tvrtku ili ustanovu želite uvesti pokazne podatke, a zatim odaberite **Prijava**.
1. Na 4. stranici odaberite zip datoteku *SampleSetupAndConfigData* iz raspakirane mape *ProjOpsSampleSetupData – CE samo CMT*.

   ![Zip datoteka.](./media/3ZipFile.png)

   ![Odabir datoteke.](./media/4SelectAFile.png)

1. Nakon odabira zip datoteke odaberite **Uvezi podatke**.

   ![Uvezite podatke.](./media/5ImportData.png)

1. Uvoz će se izvoditi otprilike dvije do deset minuta, ovisno o brzini vaše mreže. Po završetku izađite iz CMT čarobnjaka. 
1. U svojoj tvrtki ili ustanovi provjerite podatke za sljedećih 18 entiteta:

    -   Valuta
    -   Kupac
    -   Organizacijska jedinica
    -   Kontakt
    -   Jedinica
    -   Grupa jedinica
    -   Cjenik
    -   Cjenik parametara projekta 
    -   Učestalost fakturiranja
    -   Kategorija resursa koji je moguće rezervirati
    -   Kategorija transakcije
    -   Kategorija troška
    -   Cijena uloge
    -   Cijena kategorije transakcije
    -   Značajka
    -   Resurs koji je moguće rezervirati
    -   Dodjela kategorije resursa kojeg je moguće rezervirati
    -   Značajka kategorije resursa koji je moguće rezervirati

    ![Dovrši uvoz.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
