---
title: Rješavanje problema s radom u rešetki sa zadacima
description: U ovoj temi nalaze se informacije o rješavanju problema potrebne za rad u rešetki sa zadacima.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031528"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Rješavanje problema s radom u rešetki sa zadacima 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U ovoj temi opisuje se način rješavanja problema s kojima biste se mogli susresti tijekom rada na upravljanju troškovima.

## <a name="enable-cookies"></a>Omogućivanje kolačića

Project Operations zahtijeva da se omoguće kolačići treće strane kako bi se prikazala strukturna analiza rada. Kada kolačići trećih strana nisu omogućeni, umjesto da vidite zadatke, vidjet ćete praznu stranicu kada odaberete karticu **Zadaci** na stranici **Projekt**.

![Prazna kartica kada kolačići treće strane nisu omogućeni](media/blankschedule.png)


### <a name="workaround"></a>Zaobilazno rješenje
Postupci u nastavku opisuju način ažuriranja postavki preglednika Microsoft Edge ili Google Chrome kako biste omogućili kolačiće treće strane.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Otvorite preglednik Edge.
2. U gornjem desnom kutu odaberite **tri točke** (...), a zatim odaberite mogućnost **Postavke**.
3. Pod stavkom **Kolačići i dozvole web-mjesta** odaberite **Kolačići i podaci o web mjestu**.
4. Isključite **Blokiraj kolačiće treće strane**.

#### <a name="google-chrome"></a>Google Chrome

1. Otvorite preglednik Chrome.
2. U gornjem desnom kutu odaberite tri uspravne točke, a zatim odaberite mogućnost **Postavke**.
3. Pod stavkom **Privatnost i sigurnost** odaberite **Kolačići i ostali podaci o web mjestu**.
4. Odaberite **Dopusti sve kolačiće**.

> [!IMPORTANT]
> Ako blokirate kolačiće treće strane, blokirat će se svi kolačići i podaci o web-mjestu s drugih web-mjesta, čak i ako je web-mjesto dopušteno na vašem popisu iznimaka.

## <a name="pex-endpoint"></a>Krajnja točka PEX-a

Project Operations zahtijeva da parametar projekta upućuje na krajnju točku PEX. Ovaj krajnja točka potrebna je za komunikaciju s uslugom koja se upotrebljava za prikazivanje strukturne analize rada. Ako parametar nije omogućen, dobit ćete pogrešku „Parametar projekta nije valjan”. 

### <a name="workaround"></a>Zaobilazno rješenje
 ![Polje krajnje točke PEX na parametru projekta](media/projectparameter.png)

1. Dodajte polje **Krajnja točka PEX** na stranicu **Parametri projekta**.
2. Ažurirajte polje sljedećim vrijednostima: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Uklonite polje sa stranice **Parametri projekta**.

## <a name="privileges-for-project-for-the-web"></a>Ovlasti za projekt za web

Project Operations oslanja se na vanjsku uslugu planiranja. Usluga zahtijeva da korisnik ima nekoliko uloga dodijeljenih za čitanje i pisanje u entitete povezane sa strukturnom analizom rada. Ti entiteti uključuju projektne zadatke, dodjele resursa i ovisnosti zadataka. Ako korisnik ne može prikazati strukturnu analizu rada kad ode na karticu **Zadaci**, to je vjerojatno zato što Project za aplikaciju Project Operations nije omogućen. Korisnik može dobiti pogrešku sigurnosne uloge ili pogrešku povezanu s uskraćivanjem pristupa.


## <a name="workaround"></a>Zaobilazno rješenje

1. Idite na **Postavke > Sigurnost > Korisnici > Korisnici aplikacije**.  

   ![Alat za čitanje aplikacije](media/applicationuser.jpg)
   
2. Dvaput kliknite korisnički zapis aplikacije kako biste provjerili sljedeće:

 - Korisnik ima pristup projektu. Ova se provjera obično vrši osiguravanjem da korisnik ima sigurnosnu ulogu **Voditelj projekta**.
 - Korisnik aplikacije Microsoft Project postoji i ispravno je konfiguriran.
 
3. Ako taj korisnik ne postoji, možete stvoriti novi korisnički zapis. Odaberite **Novi korisnici**. Promijenite obrazac za unos u **Korisnik aplikacije**, a zatim dodajte **ID aplikacije**.

   ![Pojedinosti o korisniku aplikacije](media/applicationuserdetails.jpg)

4. Provjerite je li korisniku dodijeljena ispravna licenca i je li usluga omogućena u pojedinostima licencnih planova usluga.
5. Provjerite može li korisnik otvoriti project.microsoft.com.
6. Provjerite kroz parametre projekta usmjerava li sustav na ispravu krajnju točku projekta.
7. Provjerite je li stvoren korisnik projektne aplikacije.
8. Primijenite sljedeće sigurnosne uloge na korisnika:

  - Korisnik rješenja Dataverse
  - Sustav aplikacije Project Operations
  - Sustav projekta

## <a name="error-when-updating-the-work-breakdown-structure"></a>Pogreška tijekom ažuriranja strukturne analize rada

Kada se izvrši jedno ili više ažuriranja strukturne analize rada, promjene na kraju ne uspiju i ne spremaju se. Dolazi do pogreške u rešetki rasporeda uz napomenu da „Nije bilo moguće spremiti promjenu koju ste nedavno unijeli.”

### <a name="workaround"></a>Zaobilazno rješenje

1. Provjerite je li korisniku dodijeljena ispravna licenca i je li usluga omogućena u pojedinostima licencnih planova usluga.
2. Provjerite može li korisnik otvoriti project.microsoft.com.
3. Provjerite usmjerava li sustav na ispravu krajnju točku projekta.
4. Provjerite je li stvoren korisnik projektne aplikacije.
5. Primijenite sljedeće sigurnosne uloge na korisnika:
  
  - Korisnik ili osnovni korisnik platforme Dataverse
  - Sustav aplikacije Project Operations
  - Sustav projekta
  - Sustav dvostrukog pisanja aplikacije Project Operations (ova je uloga potrebna ako za aplikaciju Project Operations postavljate scenarij temeljen na resursima / bez zaliha.)
