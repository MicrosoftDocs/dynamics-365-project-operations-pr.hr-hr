---
title: Primjena pokaznog postavljanja i konfiguracijskih podataka
description: U ovoj temi nalaze se informacije o načinu primjene pokaznih postavki i konfiguracijskih podataka za aplikaciju Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948787"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Primjena pokaznih postavki i konfiguracijskih podataka za uvođenje jednostavne aplikacije Project Operations – od sklapanja posla do predračuna

_Jednostavno uvođenje – od sklapanja posla do predračuna_

1. Preuzmite [Paket glavnih podataka](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Pomaknite se do mape *ProjOpsDemoDataSetupAndMaster – Integrirani CMT* i pokrenite izvršnu datoteku *DataMigrationUtility*.
3. Na 1. stranici Čarobnjaka za migraciju konfiguracije (CMT) platforme Common Data Service odaberite **Uvez podatke** a zatim **Nastavi**.

![Migracija konfiguracije](./media/1ConfigurationMigration.png)

4. Na 2. stranici CMT čarobnjaka odaberite **Office 365** kao **Vrstu uvođenja**.
5. Označite potvrdne okvire **Prikaži popis dostupnih tvrtki ili ustanova** i **Prikaži napredne**.
6. Odaberite regiju svog klijenta, unesite svoje vjerodajnice, a zatim odaberite **Prijava**.

![Konfiguracija prijave](./media/2ConfigurationSignin.png)

7. Na 3. stranici, s popisa tvrtki ili ustanova na klijentu odaberite u koju tvrtku ili ustanovu želite uvesti pokazne podatke, a zatim odaberite **Prijava**.
8. Na 4. stranici odaberite zip datoteku *MasterAndSetupData* iz raspakirane mape *ProjOpsDemoDataSetupAndMaster – Integrirani CMT*.

![Zip datoteka](./media/3ZipFile.png)

![Odaberite datoteku](./media/4SelectAFile.png)

9. Nakon odabira zip datoteke odaberite **Uvezi podatke**.

![Uvoz podataka](./media/5ImportData.png)

10. Uvoz će se izvoditi otprilike dvije do deset minuta, ovisno o brzini vaše mreže. Po završetku izađite iz CMT čarobnjaka. 
11. U svojoj tvrtki ili ustanovi provjerite podatke za sljedećih 20 entiteta:

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
- Pojedinost učestalosti fakture
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
