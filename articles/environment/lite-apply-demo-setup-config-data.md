---
title: Primjena probnog postavljanja i konfiguracija podataka – jednostavno
description: U ovom se članku nalaze informacije o primjeni podataka o postavljanju demoa i konfiguraciji za operacije projekta.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 68e504dd031596b295b1383a8e81621744cae8d2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922305"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Primjena podataka postavljanja pokazne verzije i konfiguracije za aplikaciju Project Operations – jednostavno 

_**Jednostavna implementacija – od sklapanja posla do predračuna_



## <a name="prerequisites"></a>Preduvjeti

Prije nego započnete konfiguriranje, morate imati okruženje platforme Common Data Service (CDS) pripremljeno za aplikaciju Dynamics 365 Project Operations.


## <a name="instructions"></a>Upute

1. Preuzmite [Paket glavnih podataka](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Dođite do mape *ProjOpsSampleSetupData – CE samo CMT* i pokrenite izvršnu datoteku *DataMigrationUtility*.
3. Na 1. stranici Čarobnjaka za migraciju konfiguracije (CMT) platforme Common Data Service odaberite **Uvez podatke** a zatim **Nastavi**.

    ![Migracija konfiguracije.](./media/1ConfigurationMigration.png)

4. Na 2. stranici CMT čarobnjaka odaberite **Microsoft 365** kao **Vrstu uvođenja**.
5. Označite potvrdne okvire **Prikaži popis dostupnih tvrtki ili ustanova** i **Prikaži napredne**.
6. Odaberite regiju svog klijenta, unesite svoje vjerodajnice, a zatim odaberite **Prijava**.

   ![Konfiguracija prijave.](./media/2ConfigurationSignin.png)

7. Na 3. stranici, s popisa tvrtki ili ustanova na klijentu odaberite u koju tvrtku ili ustanovu želite uvesti pokazne podatke, a zatim odaberite **Prijava**.
8. Na 4. stranici odaberite zip datoteku *SampleSetupAndConfigData* iz raspakirane mape *ProjOpsSampleSetupData – CE samo CMT*.

   ![Zip datoteka.](./media/3ZipFile.png)

   ![Odabir datoteke.](./media/4SelectAFile.png)

9. Nakon odabira zip datoteke odaberite **Uvezi podatke**.

   ![Uvezite podatke.](./media/5ImportData.png)

10. Uvoz će se izvoditi otprilike dvije do deset minuta, ovisno o brzini vaše mreže. Po završetku izađite iz CMT čarobnjaka. 
11. U svojoj tvrtki ili ustanovi provjerite podatke za sljedećih 18 entiteta:

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
