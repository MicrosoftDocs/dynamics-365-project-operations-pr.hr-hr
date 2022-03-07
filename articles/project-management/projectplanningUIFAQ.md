---
title: Rješavanje problema s radom u rešetki sa zadacima
description: U ovoj temi nalaze se informacije o rješavanju problema potrebne za rad u rešetki sa zadacima.
author: ruhercul
ms.date: 08/02/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 07e7bd42db48842edee17fdfdd22fdcd8207644c1751f453ec29c3194aac625e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989092"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Rješavanje problema s radom u rešetki sa zadacima 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U ovoj temi opisuje se način rješavanja problema s kojima biste se mogli susresti tijekom rada na upravljanju troškovima.

## <a name="enable-cookies"></a>Omogućivanje kolačića

Project Operations zahtijeva da se omoguće kolačići treće strane kako bi se prikazala strukturna analiza rada. Kada kolačići trećih strana nisu omogućeni, umjesto da vidite zadatke, vidjet ćete praznu stranicu kada odaberete karticu **Zadaci** na stranici **Projekt**.

![Prazna kartica kada kolačići treće strane nisu omogućeni.](media/blankschedule.png)


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

1. Dodajte polje **Krajnja točka PEX** na stranicu **Parametri projekta**.
2. Odredite vrstu proizvoda koju upotrebljavate. Ova se vrijednost upotrebljava kada je postavljena krajnja točka PEX-a. Nakon preuzimanja, vrsta proizvoda već je definirana u krajnjoj točki PEX-a. Zadržite tu vrijednost. 
   
    ![Polje krajnje točke PEX-a na parametru projekta.](media/pex-endpoint.png)

3. Ažurirajte polje sljedećim vrijednostima: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`.

   
   | Vrsta proizvoda                         | Parametar vrste |
   |--------------------------------------|----------------|
   | Project for the Web u zadanoj organizaciji   | vrsta=0         |
   | Project for the Web u organizaciji imenovanoj na platformi CDS | vrsta=1         |
   | Project Operations                   | vrsta=2         |
   
4. Uklonite polje sa stranice **Parametri projekta**.

## <a name="privileges-for-project-for-the-web"></a>Ovlasti za projekt za web

Project Operations oslanja se na vanjsku uslugu planiranja. Usluga zahtijeva da korisnik ima nekoliko uloga dodijeljenih za čitanje i pisanje u entitete povezane sa strukturnom analizom rada. Ti entiteti uključuju projektne zadatke, dodjele resursa i ovisnosti zadataka. Ako korisnik ne može prikazati strukturnu analizu rada kad ode na karticu **Zadaci**, to je vjerojatno zato što Project za aplikaciju Project Operations nije omogućen. Korisnik može dobiti pogrešku sigurnosne uloge ili pogrešku povezanu s uskraćivanjem pristupa.


## <a name="workaround"></a>Zaobilazno rješenje

1. Idite na **Postavke > Sigurnost > Korisnici > Korisnici aplikacije**.  

   ![Alat za čitanje aplikacije.](media/applicationuser.jpg)
   
2. Dvaput kliknite korisnički zapis aplikacije kako biste provjerili sljedeće:

 - Korisnik ima pristup projektu. Ova se provjera obično vrši osiguravanjem da korisnik ima sigurnosnu ulogu **Voditelj projekta**.
 - Korisnik aplikacije Microsoft Project postoji i ispravno je konfiguriran.
 
3. Ako taj korisnik ne postoji, možete stvoriti novi korisnički zapis. Odaberite **Novi korisnici**. Promijenite obrazac za unos u **Korisnik aplikacije**, a zatim dodajte **ID aplikacije**.

   ![Pojedinosti o korisniku aplikacije.](media/applicationuserdetails.jpg)

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
