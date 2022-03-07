---
title: Ažuriranje aplikacije Project Operations u vašem okruženju aplikacije Financije
description: U ovoj temi nalaze se informacije o načinu ažuriranja rješenja Project Operations u vašem okruženju aplikacije Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3665bccfa25c759c0f2351c691d24901867c178f7c339f4a524856842666aec5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986752"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Ažuriranje aplikacije Project Operations u vašem okruženju aplikacije Financije

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_


U ovoj temi nalaze se informacije o načinu ažuriranja rješenja Dynamics 365 Project Operations u vašem okruženju aplikacije Dynamics 365 Finance. Tri su postupka potrebna za ažuriranje aplikacije Project Operations na Ažuriranje 5 (UR5):

- [Uvezite paket u pretpregled svojeg projekta](#import)
- [Primjena ažuriranja](#apply)
- [Ažuriranje okruženja svoje platforme Dataverse](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Uvezite paket u svoj projekt LCS

1. Prijavite se na portal [Lifecycle Services (LCS)](https://lcs.dynamics.com/) kao vlasnik projekta ili upravitelj okruženja.
2. S popisa projekata odaberite svoj projekt LCS.
3. Na stranici **Projekt** u grupi **Okruženja** otvorite okruženje koje želite ažurirati.
4. Provjerite radi li okruženje. Ako okruženje nije pokrenuto, pokrenite ga.
5. U odjeljku **Novo izdanje** pod stavkom **Dostupna ažuriranja** odaberite **Prikaži ažuriranje** za 10.0.15.

![Gumb za prikaz ažuriranja.](media/view-update.png)

6. Na stranici **Binarna ažuriranja** odaberite **Spremi paket**.
7. Na stranici **Pregled i spremanje ažuriranja** odaberite **Spremi paket**.
8. U oknu **Spremi paket u biblioteku sredstava** koje se otvori, unesite naziv paketa, a zatim odaberite **Spremi paket**.
9. Kad LCS završi spremanje paketa, omogućuje se gumb **Gotovo**. Odaberite **Gotovo**. LCS će provjeriti paket. Provjera može trajati nekoliko minuta ili do jedan sat.


## <a name="apply-the-package-update"></a><a name="apply"></a>Primjena paketa za ažuriranje

1. Na stranici **Pojedinosti okruženja** u LCS-u, odaberite **Održavaj** > **Primijeni ažuriranja**.
2. S popisa odaberite paket koji ste ranije spremili, a zatim odaberite **Primijeni**.
3. Odaberite **Da** kako biste potvrdili da želite implementirati paket.

![Potvrda dijaloškog okvira za implementaciju paketa.](media/confirm-package-deployment.png)

4. Odaberite **Da** kako biste potvrdili da želite ažurirati aplikaciju.

![Potvrđivanje dijaloškog okvira za ažuriranje aplikacije.](media/confirm-application-update.png)

Započet će implementacija i ažuriranje aplikacije. 

U gornjem desnom kutu stranice **Pojedinosti okruženja** status okoliša ažurirat će se na **Servisiranje**. Ažuriranje će se dovršiti za otprilike dva sata. Podaci o izdanju aplikacije ažurirat će se na **Microsoft Dynamics 365 for Finance and Operations 10.0.15)**, a status okruženja ažurirat će se na **Implementiran**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Ažuriranje okruženja platforme Dataverse

1. Prijavite se u [centar za administratore platforme Power Platform](https://admin.powerplatform.com/).
2. Na popisu pronađite i otvorite okruženje koje ste upotrebljavali za instalaciju aplikacije Project Operations.
3. Na stranici **Okruženja** odaberite **Resurs** > **Aplikacije sustava Dynamics 365**.
4. Na popisu pronađite **Microsoft Dynamics 365 Project Operations** i u stupcu **Status** odaberite **Ažuriranje dostupno**.
5. Odaberite potvrdni okvir **Slažem se s uvjetima pružanja usluge**, a zatim odaberite **Ažuriraj**. Instalirat će se najnovija verzija rješenja.

Nakon završetka instalacije imat ćete instaliranu verziju 4.5.0.134.

## <a name="configure-new-features"></a>Konfiguriranje novih značajki

### <a name="enable-dual-write-mapping"></a>Omogućivanje mapiranja dvostrukog pisanja

Nakon što dovršite ažuriranje aplikacije Financije i okruženja platforme Dataverse možete omogućiti potrebna mapiranja dvostrukog pisanja. Izvršite sljedeće postupke kako biste omogućili mapiranje dvostrukog pisanja:

- [Ažuriranje sigurnosnih postavki u okruženju aplikacije Customer Engagement](#security)
- [Osvježavanje unosa podataka](#refresh)
- [Ažuriranje i pokretanje mapiranja dvostrukog pisanja](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Ažuriranje sigurnosnih postavki u okruženju platforme Dataverse

Sljedeća ažuriranja sigurnosnih ovlasti za entitete potrebna su kao dio ažuriranja UR5.

1. U okruženju svoje platforme Dataverse idite na **Postavke** i u grupi **Sustav** odaberite **Sigurnost**.

![Postavke okruženja platforme Dataverse.](media/Picture21.png)

2. Odaberite mogućnost **Sigurnosna uloga**.
3. S popisa uloga odaberite **korisnik aplikacije dvostrukog ispisa** i odaberite karticu **Prilagođeni entiteti**. 
4. Provjerite ima li uloge **Čitanje** i **Dodaj u** dozvole za:

      - **Vrstu deviznog tečaja valute**
      - **Grafikon računa** 
      - **Fiskalni kalendar** 
      - **Knjiga**

5. Nakon ažuriranja sigurnosne uloge idite na **Postavke** > **Sigurnost** > **Teams**. Provjerite primjenjuje li se uloga **korisnik aplikacije dvostrukog pisanja** na tim. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Osvježite podatkovne jedinice iz ažuriranja

1. U okruženju vaše aplikacije Financije otvorite radni prostor **Upravljanje podacima**, a zatim otvorite stranicu **Parametri okvira**.
2. Na kartici **Postavke entiteta** odaberite **Osvježi popis entiteta**.
3. Odaberite **Zatvori** za potvrdu osvježavanja entiteta.

 > [!NOTE]
 > Za dovršenje ovog postupka treba približno 20 minuta. Kada se osvježavanje završi primit ćete obavijest.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Ažuriranje mapiranja dvostrukog pisanja

1. U radnom prostoru **Upravljanje podacima** odaberite **Dvostruko pisanje**.
2. Odaberite **Primijeniti rješenja**, odaberite oba rješenja s popisa, a zatim odaberite **Primijeni**.
3. Na stranici **Dvostruko pisanje** odaberite sljedeće karte tablice, a zatim odaberite **Zaustavi**.

    - **Stvarni podaci aplikacije Project Operations (msdyn_actuals)**
    - **Kategorije troškova projekta za integraciju aplikacije Project Operations (msdyn_expensecategories)**
    - **Entitet izvoza stvarnih troškova projekta za integraciju aplikacije Project Operations (msdyn_expenses)**

4. Na stranici **Verzija karte tablice** primijenite novu verziju karte na svaki od tri entiteta.
5. Na stranici **Dvostruko pisanje** odaberite Pokreni za ponovno pokretanje karti.
6. S popisa karti odaberite kartu **Knjiga (msdyn_ledgers)** sa svim preduvjetima i odaberite potvrdni okvir **Početna sinkronizacija**. 
7. U polju **Glavni za početnu sinkronizaciju** odaberite **Aplikacije rješenja Finance and Operations**, a zatim odaberite **Pokreni**.
 
 ![Sinkronizacija karte knjige.](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]