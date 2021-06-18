---
title: Primjena probnog postavljanja i konfiguracija podataka – jednostavno
description: U ovoj temi nalaze se informacije o načinu primjene pokaznih postavki i konfiguracijskih podataka za aplikaciju Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997142"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Primjena podataka postavljanja pokazne verzije i konfiguracije za aplikaciju Project Operations – jednostavno 

_**Jednostavna implementacija – od sklapanja posla do predračuna_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Preduvjeti

Prije nego započnete konfiguriranje, morate imati okruženje platforme Common Data Service (CDS) pripremljeno za aplikaciju Dynamics 365 Project Operations.


## <a name="instructions"></a>Upute

1. Preuzmite [Paket glavnih podataka](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Dođite do mape *ProjOpsSampleSetupData – CE samo CMT* i pokrenite izvršnu datoteku *DataMigrationUtility*.
3. Na 1. stranici Čarobnjaka za migraciju konfiguracije (CMT) platforme Common Data Service odaberite **Uvez podatke** a zatim **Nastavi**.

    ![Migracija konfiguracije](./media/1ConfigurationMigration.png)

4. Na 2. stranici CMT čarobnjaka odaberite **Microsoft 365** kao **Vrstu implementacije**.
5. Označite potvrdne okvire **Prikaži popis dostupnih tvrtki ili ustanova** i **Prikaži napredne**.
6. Odaberite regiju svog klijenta, unesite svoje vjerodajnice, a zatim odaberite **Prijava**.

   ![Konfiguracija prijave](./media/2ConfigurationSignin.png)

7. Na 3. stranici, s popisa tvrtki ili ustanova na klijentu odaberite u koju tvrtku ili ustanovu želite uvesti pokazne podatke, a zatim odaberite **Prijava**.
8. Na 4. stranici odaberite zip datoteku *SampleSetupAndConfigData* iz raspakirane mape *ProjOpsSampleSetupData – CE samo CMT*.

   ![Zip datoteka](./media/3ZipFile.png)

   ![Odabir datoteke](./media/4SelectAFile.png)

9. Nakon odabira zip datoteke odaberite **Uvezi podatke**.

   ![Uvoz podataka](./media/5ImportData.png)

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

    ![Dovrši uvoz](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
