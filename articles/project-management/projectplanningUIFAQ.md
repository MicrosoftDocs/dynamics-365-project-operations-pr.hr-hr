---
title: Rješavanje problema s radom u rešetki sa zadacima
description: U ovom se članku nalaze informacije o otklanjanju poteškoća potrebne za rad u rešetki zadatka.
author: ruhercul
ms.date: 07/22/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 208ed55abf4cdf0ad2b035bd923e183ff3cae660
ms.sourcegitcommit: e91136d3335ee03db660529eccacd48907774453
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/22/2022
ms.locfileid: "9188222"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Rješavanje problema s radom u rešetki sa zadacima 


_**Odnosi se na:** Project Operations za scenarije koji se temelje na resursima/bez zaliha, osnovna implementacija – od sklapanja posla do predračuna, Project for the Web_

Rešetka zadatka koju Dynamics 365 Project Operations koristi je hostirani iframe unutar sustava Microsoft Dataverse. Kao rezultat ove uporabe, moraju biti ispunjeni specifični zahtjevi kako bi se osigurala provjera autentičnosti i ispravno funkcioniranje autorizacije. U ovom se članku opisuju uobičajeni problemi koji mogu utjecati na mogućnost prikazivanja rešetke ili upravljanja zadacima u strukturi raščlambe rada (WBS).

Uobičajeni problemi uključuju:

- Kartica **Zadatak** na rešetki zadataka prazna je.
- Prilikom otvaranja projekta, projekt se ne učitava, a korisničko sučelje (UI, engl. user interface) zaglavilo se na rotoru.
- Upravljanje privilegijima za **Project for the Web**.
- Promjene se ne spremaju kada zadatak stvorite, ažurirate ili izbrišete.

## <a name="issue-the-task-tab-is-empty"></a>Problem: Kartica Zadatak prazna je

### <a name="mitigation-1-enable-cookies"></a>Ublažavanje 1: Omogućivanje kolačića

Project Operations zahtjeva da kolačići trećih strana budu omogućeni za prikazivanje strukturne analize rada. Kada kolačići drugih proizvođača nisu omogućeni, umjesto da vidite zadatke, vidjet ćete praznu stranicu kada odaberete karticu **Zadaci** na **stranici Projekt**.

Postupci u nastavku opisuju način ažuriranja postavki preglednika Microsoft Edge ili Google Chrome kako biste omogućili kolačiće treće strane.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Otvorite preglednik Edge.
2. U gornjem desnom kutu odaberite **tri točke** (...), a zatim odaberite mogućnost **Postavke**.
3. Pod stavkom **Kolačići i dozvole web-mjesta** odaberite **Kolačići i podaci o web mjestu**.
4. Isključite **Blokiraj kolačiće treće strane**.
5. Osvježite preglednik. 

#### <a name="google-chrome"></a>Google Chrome

1. Otvorite preglednik Chrome.
2. U gornjem desnom kutu odaberite tri uspravne točke, a zatim odaberite mogućnost **Postavke**.
3. Pod stavkom **Privatnost i sigurnost** odaberite **Kolačići i ostali podaci o web mjestu**.
4. Odaberite **Dopusti sve kolačiće**.
5. Osvježite preglednik. 

> [!NOTE]
> Ako blokirate kolačiće treće strane, blokirat će se svi kolačići i podaci o web-mjestu s drugih web-mjesta, čak i ako je web-mjesto dopušteno na vašem popisu iznimaka.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Ublažavanje 2: Potvrđivanje da je Krajnja točka PEX ispravno konfigurirana

Project Operations zahtijeva da parametar projekta upućuje na krajnju točku PEX. Ovaj krajnja točka potrebna je za komunikaciju s uslugom koja se upotrebljava za prikazivanje strukturne analize rada. Ako parametar nije omogućen, prikazat će se pogreška "Parametar projekta nije valjan". Kako biste ažurirali Krajnju točku PEX, poduzmite sljedeće korake.

1. Dodajte polje **Krajnja točka PEX** na stranicu **Parametri projekta**.
2. Identificirajte vrstu proizvoda koju koristite. Ova se vrijednost upotrebljava kada je postavljena krajnja točka PEX-a. Nakon preuzimanja, vrsta proizvoda već je definirana u krajnjoj točki PEX-a. Zadržite tu vrijednost.
3. Ažurirajte polje sljedećim vrijednostima: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Sljedeća tablica daje parametre vrste koja se treba upotrebljavati ovisno o vrsti proizvoda.

      | **Vrsta proizvoda**                     | **Parametar vrste** |
      |--------------------------------------|--------------------|
      | Project for the Web u zadanoj organizaciji   | vrsta=0             |
      | Project for the Web u organizaciji imenovanoj na platformi CDS | vrsta=1             |
      | Project Operations                   | vrsta=2             |

4. Uklonite polje sa stranice **Parametri projekta**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Ublažavanje 3: prijavite se u project.microsoft.com

U pregledniku otvorite novu karticu, idite na project.microsoft.com i prijavite se s korisničkom ulogom koju koristite za pristup operacijama programa Project. Važno je da se samo jedan korisnik prijavi na Microsoftov proizvod u pregledniku. Poruka o pogrešci "login.microsoftonline.com odbio povezati" najčešće se pojavljuje kada je prijavljeno više korisnika, kao što je prikazano na sljedećoj slici.

![Odaberite stranicu za prijavu na račun koja pokazuje da su prijavljena dva korisnika.](media/MULTIPLE_USERS_LOGGED_IN.png)

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problem: Projekt se ne učitava, a korisničko sučelje je zaglavilo na rotoru

U svrhu provjere autentičnosti, skočni prozori moraju biti omogućeni za učitavanje Rešetke zadataka. Ako skočni prozori nisu omogućeni, zaslon će se zaglaviti na rotoru za učitavanje. Sljedeća grafika prikazuje URL s blokiranom skočnom naljepnicom u adresnoj traci, što rezultira zaglavljivanjem spinnera pokušavajući učitati stranicu. 

   ![Zaglavljeni rotor i skočni blok.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Ublažavanje 1: Omogućivanje skočnih prozora

Kad se projekt zaglavi na rotoru, moguće je da se skočni prozori ne omoguće.

#### <a name="microsoft-edge"></a>Microsoft Edge

Postoje dva načina za omogućivanje skočnih prozora u pregledniku Edge.

1. U gornjem desnom kutu pregledniku Edge odaberite obavijest.
2. Odaberite **Uvijek dopusti skočne prozore i preusmjeravanja s njih** specifično okruženje platforme Dataverse.
 
     ![Skočni prozori blokiraju prozor.](media/enablepopups.png)

Umjesto toga možete poduzeti sljedeće korake.

1. Otvorite preglednik Edge.
2. U gornjem desnom kutu odaberite **Tri točke** (...), a zatim odaberite **Postavke** > **Dozvole web- mjesta** > **Skočni prozori i preusmjeravanja**.
3. Isključite mogućnost **Skočni prozori i preusmjeravanja** za blokirane skočne prozore ili uključite kako biste omogućili skočne prozore na svom uređaju.
4. Nakon što omogućite skočne prozore, osvježite preglednik. 

#### <a name="google-chrome"></a>Google Chrome
1. Otvorite preglednik Chrome.
2. Idite na stranicu na kojoj su skočni prozori blokirani.
3. U adresnoj traci odaberite **Blokirani skočni prozor**.
4. Odaberite vezu za skočni prozor koji želite vidjeti.
5. Nakon što omogućite skočne prozore, osvježite preglednik. 

> [!NOTE]
> Kako biste uvijek vidjeli skočne prozore za web-mjesto, odaberite **Uvijek dozvoli skočne prozore i preusmjeravanja s [web-mjesta]** a zatim odaberite **Gotovo**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problem 3: Upravljanje privilegijima za Project for the Web

Project Operations oslanja se na vanjsku uslugu planiranja. Usluga zahtijeva da korisnik ima nekoliko dodijeljenih uloga koje mu omogućuju čitanje i pisanje entitetima povezanim s WBS-om. Ti entiteti uključuju projektne zadatke, dodjele resursa i ovisnosti zadataka. Ako korisnik ne može prikazati WBS kada prijeđe na karticu **Zadaci**, to je vjerojatno zato **što Project** for **Project Operations** nije omogućen. Korisnik može dobiti pogrešku sigurnosne uloge ili pogrešku povezanu s uskraćivanjem pristupa.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Ublažavanje 1: Provjera valjanosti sigurnosnih uloga korisnika aplikacije i krajnjeg korisnika

1. Idite na **Postavke** > **Sigurnost** > **Korisnici** > **Korisnici aplikacije**.  

   ![Alat za čitanje aplikacije.](media/applicationuser.jpg)
   
2. Dvaput kliknite zapis korisnika aplikacije kako biste provjerili:

     - Korisnik ima pristup projektu. To možete učiniti provjerom ima li korisnik sigurnosnu ulogu **Voditelj projekta**.
     - Korisnik aplikacije Microsoft Project postoji i ispravno je konfiguriran.
 
3. Ako ovaj korisnik ne postoji, izradite novi zapis o korisniku. 
4. Odaberite **Novi korisnici**, promijenite obrazac za prijavu u **Korisnik aplikacije**, a zatim dodajte **ID aplikacije**.

   ![Pojedinosti o korisniku aplikacije.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problem 4: Promjene se ne spremaju kada zadatak stvorite, ažurirate ili izbrišete

Kada izvršite jedno ili više ažuriranja WBS-a, promjene ne uspijevaju i ne spremaju se. Dolazi do pogreške u rešetki rasporeda uz poruku „Nedavna promjena koju ste unijeli nije se mogla spremiti”.

### <a name="mitigation-1-validate-the-license-assignment"></a>Ublažavanje 1: Potvrda dodjele licence

1. Provjerite je li korisniku dodijeljena ispravna licenca i je li usluga omogućena u pojedinostima licencnih planova usluga.  
2. Provjerite može li korisnik otvoriti **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Ublažavanje 2: Konfiguracija provjere valjanosti korisnika Projektne aplikacije
1. Provjerite je li stvoren korisnik projektne aplikacije.
2. Primijenite sljedeće sigurnosne uloge na korisnika:
  
  - Korisnik ili osnovni korisnik platforme Dataverse
  - Sustav aplikacije Project Operations
  - Sustav projekta
  - Sustav dvostrukog zapisivanje aplikacije Project Operations. Ta je uloga potrebna za scenarij implementacije koji se temelji na resursu / bez zaliha aplikacije Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
