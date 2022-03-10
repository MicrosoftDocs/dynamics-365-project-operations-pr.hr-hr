---
title: Rješavanje problema s radom u rešetki sa zadacima
description: U ovoj temi nalaze se informacije o rješavanju problema potrebne za rad u rešetki sa zadacima.
author: ruhercul
ms.date: 09/22/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 67136229d84a09886fffe9677b10f671aea3c393
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547190"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Rješavanje problema s radom u rešetki sa zadacima 


_**Odnosi se na:** Project Operations za scenarije koji se temelje na resursima/bez zaliha, osnovna implementacija – od sklapanja posla do predračuna, Project for the Web_

Rešetka zadataka koju je aplikacija Dynamics 365 Project Operations upotrebljavala hostirani je iframe unutar platforme Microsoft Dataverse. Kao rezultat ove uporabe, moraju se ispuniti posebni zahtjevi kako bi se osiguralo ispravno funkcioniranje provjere autentičnosti i autorizacije. U ovoj temi navode se uobičajeni problemi koji mogu utjecati na mogućnost prikazivanja rešetke ili upravljanja zadacima u strukturnoj analizi rada (WBS, engl. work breakdown structure).

Uobičajeni problemi uključuju:

- Kartica **Zadatak** na rešetki zadataka prazna je.
- Prilikom otvaranja projekta, projekt se ne učitava, a korisničko sučelje (UI, engl. user interface) zaglavilo se na rotoru.
- Upravljanje privilegijima za **Project for the Web**.
- Promjene se ne spremaju kada zadatak stvorite, ažurirate ili izbrišete.

## <a name="issue-the-task-tab-is-empty"></a>Problem: Kartica Zadatak prazna je

### <a name="mitigation-1-enable-cookies"></a>Ublažavanje 1: Omogućivanje kolačića

Project Operations zahtjeva da kolačići trećih strana budu omogućeni za prikazivanje strukturne analize rada. Kada kolačići trećih strana nisu omogućeni, umjesto da vidite zadatke, vidjet ćete praznu stranicu kada odaberete karticu **Zadaci** na stranici **Projekt**.

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

Project Operations zahtijeva da parametar projekta upućuje na krajnju točku PEX. Ovaj krajnja točka potrebna je za komunikaciju s uslugom koja se upotrebljava za prikazivanje strukturne analize rada. Ako parametar nije omogućen, dobit ćete pogrešku „Parametar projekta nije valjan”. Kako biste ažurirali Krajnju točku PEX, poduzmite sljedeće korake.

1. Dodajte polje **Krajnja točka PEX** na stranicu **Parametri projekta**.
2. Odredite vrstu proizvoda koju upotrebljavate. Ova se vrijednost upotrebljava kada je postavljena krajnja točka PEX-a. Nakon preuzimanja, vrsta proizvoda već je definirana u krajnjoj točki PEX-a. Zadržite tu vrijednost.
3. Ažurirajte polje sljedećim vrijednostima: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Sljedeća tablica daje parametre vrste koja se treba upotrebljavati ovisno o vrsti proizvoda.

      | **Vrsta proizvoda**                     | **Parametar vrste** |
      |--------------------------------------|--------------------|
      | Project for the Web u zadanoj organizaciji   | vrsta=0             |
      | Project for the Web u organizaciji imenovanoj na platformi CDS | vrsta=1             |
      | Project Operations                   | vrsta=2             |

4. Uklonite polje sa stranice **Parametri projekta**.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problem: Projekt se ne učitava, a korisničko sučelje je zaglavilo na rotoru

U svrhu provjere autentičnosti, skočni prozori moraju biti omogućeni za učitavanje Rešetke zadataka. Ako skočni prozori nisu omogućeni, zaslon će se zaglaviti na rotoru za učitavanje. Slika u nastavku prikazuje URL-adresu s blokiranom skočnom oznakom u traci za adresu što dovodi do zaglavljivanja rotora pri pokušaju učitavanja stranice. 

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

Project Operations oslanja se na vanjsku uslugu planiranja. Usluga zahtijeva da korisnik ima nekoliko dodijeljenih uloga koje mu omogućuju čitanje i pisanje entitetima povezanim s WBS-om. Ti entiteti uključuju projektne zadatke, dodjele resursa i ovisnosti zadataka. Ako korisnik ne može prikazati WBS tijekom kretanja do kartice **Zadaci**, to je vjerojatno zato što **Projekt** za **Project Operations** nije omogućen. Korisnik može dobiti pogrešku sigurnosne uloge ili pogrešku povezanu s uskraćivanjem pristupa.

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
