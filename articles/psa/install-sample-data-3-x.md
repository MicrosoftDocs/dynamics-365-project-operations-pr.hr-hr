---
title: Instalacija uzorka podataka
description: U ovoj temi nalaze se informacije o načinu instaliranju uzoraka podataka u aplikaciju Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 01e2f1f6b29e040d5c72af402031e13a867736405c4ee161e49b74a30e4b506e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985537"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Instalacija oglednih podataka za aplikaciju Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

Da biste mogli izraditi vlastita demonstracijska okruženja, Microsoft vam omogućuje da preuzmete pakete oglednih podataka pomoću kojih ćete vidjeti mogućnosti svojih aplikacija. Postoje dvije vrste paketa oglednih podataka:
- referentni podaci / podaci za postavljanje
- pokazni podaci (referentni podaci / podaci za postavljanje i transakcijski podaci kao što su radni nalozi i projekti)

Paketi oglednih **referentnih** podataka mogu se preuzeti u trima različitim paketima, pa možete instalirati samo podatke za Project Service ili samo za Field Service ili pak možete istodobno instalirati ogledne podatke za obje aplikacije.

Paketi oglednih podataka za postavljanje / referentnih podataka su sljedeći:

- [**V902PSMasterData** – samo verzija 3.x za Project Service](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** – samo verzija 8.x za Field Service](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x i Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Najnoviji paket **pokaznih** podataka je sljedeći:

 - [**FPSDemoData** – Field Service 8.x i Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Upute za instalaciju malo se razlikuju u odjeljku korisnika za stvaranje i konfiguriranje, ali ostatak je isti kao u prethodnoj [**objavi na blogu**](https://aka.ms/fpsdemodatablog). Ovaj paket sadrži smanjeni skup pokaznih podataka i njegova instalacija traje približno 3 sata.

Ti paketi oglednih podataka dostupni su samo na engleskom.

> [!IMPORTANT]
> **Ogledne podatke nije moguće deinstalirati.** Pakete biste trebali instalirati samo na probnim ili testnim sustavima te sustavima za procjenu i obuku. Napominjemo i da nije podržano instaliranje jednog pojedinačnog paketa, a zatim instaliranje još jednog pojedinačnog paketa. (Drugim riječima, ne možete instalirati **FSMasterData**, a nakon toga **PSMasterData** ili obrnuto.) Ako mislite da bi vam u budućnosti mogli zatrebati ogledni podaci za obje aplikacije, instalirajte paket **v902FPSMasterData**.

Pri instaliranju bilo kojeg paketa oglednih podataka postupak instalacije izvodi sljedeće radnje:

- Stvara ili postavlja zadane parametre za korištenje aplikacije Project Service, Field Service ili obje aplikacije (ako je to primjenjivo).

- Uvozi ogledne podatke za aplikacije, kao što su resursi koji se mogu rezervirati, uloge za određenu aplikaciju, prodajne popise i cjenike, organizacijske jedinice, zapise o prodajnim procesima i druge entitete koji prikazuju ključne mogućnosti aplikacije.  

U paketu **pokaznih podataka** dobivate sve gore navedene i dodatne transakcijske podatke kao što su radni nalozi i projekti.

Pitate se koje mogućnosti možete demonstrirati uz pomoć oglednih podataka? Pogledajte izmišljeni scenarij za Fabrikam Robotics u [tehničkim napomenama](#technical-notes).

Ako imate pitanja o instaliranju tih paketa oglednih podataka, [pošaljite nam poruku e-pošte na adresu fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com)

## <a name="requirements"></a>Uvjeti

Instalacijski protokol pretpostavlja sljedeće o vašoj ciljnoj instanci (organizaciji):

- Osnovni jezik je engleski, a osnovna valuta američki dolar (USD, $).

- Tvrtka ili ustanova nema već podatke za Field Service ili Project Service ili su to samo osnovni zadani podaci koji dolaze u svaku novu tvrtku ili ustanovu.

- Već je instalirana ispravna verzija poslovne aplikacije:
       
    - **Za FPSDemoData ili v902FPSMasterData:** za tvrtku ili ustanovu instalirane su aplikacije Field Service, verzija 8.x i Project Service, verzija 3.x.

    - **Za v902PSMasterData:** za organizaciju je instalirana aplikacija Project Service verzija 3.x.

    - **Za v902FSMasterData:** za organizaciju je instalirana aplikacija Field Service verzija 8.x.

> [!NOTE]
> Ako ogledne podatke morate instalirati preko postojećeg probnog ili pokaznog okruženja za Project Service i Field Service koje već sadrži podatke (ne preporučuje se), morat ćete obustaviti sigurnosne predprovjere koje izvodi instalacijski program. Dodatne informacije potražite u tehničkim napomenama u nastavku.

## <a name="prepare-for-installation"></a>Priprema za instalaciju

Morate pokrenuti instalacijski program na računalu s najnovijom verzijom sustava Windows (Windows 10 Preferirani).

Trebate planirati da računalo ostane povezano s mrežom te da instalacija **podataka za postavljanje / referentnih podataka** traje do **jednog sata**. (Instalacija paketa **FPSMasterData** obično traje oko 30 minuta, a taj paket sadrži ogledne podatke za obje aplikacije.) Instalacija paketa **FPSDemoData** trajat će oko **3 sata**.

Na računalu mora biti isključena funkcija čuvara zaslona. U suprotnom se vjerodajnice sesije za instalaciju mogu izgubiti kada se aktivira čuvar zaslona (osim ako sesija aktivna cijelo vrijeme).

> [!div class="mx-imgBorder"]
> ![Snimka zaslona s prikazom postavki čuvara zaslona s isključenim čuvarom zaslona.](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Preuzimanje i raspakiravanje

Instalacijski program za ogledne podatke aplikacija Project Service i Field Service distribuira se kao izvršna datoteka s automatskim izdvajanjem. Nazivi datoteka mogu se razlikovati ovisno o paketu oglednih podataka, ali inače su koraci isti bez obzira na to koji paket instalirate.

Nakon preuzimanja paketa pokrenite .exe datoteku, a zatim prihvatite ugovorne odredbe i uvjete da biste raspakirali komprimiranu zip datoteku. Potom morate izdvojiti sadržaj te datoteke u mapu na računalu.

Ovisno o operacijskom sustavu i sigurnosnim postavkama, možda ćete morati izvršiti sljedeće korake nakon raspakiravanja zip datoteke:

1. Pronađite i desnom tipkom miša kliknite datoteku **FPSDemoData.dll** u mapi **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Odaberite **Deblokiraj**.

3. Odaberite **Primijeni**.

4. Odaberite **U redu**.


## <a name="create-or-configure-users"></a>Stvaranje ili konfiguriranje korisnika

Za paket **FPSDemoData** potrebno je šest korisnika, a za paket **FPSMasterData** jedan korisnik. Potražite odgovarajući za svoj paket oglednih podataka.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Stvaranje ili konfiguriranje korisnika – paketi podataka za postavljanje / referentnih podataka

Pri instalaciji paketa **FPSMasterData** bit će potrebno odabrati korisnika Spencer Low i za njega koristiti ovdje opisane postavke. Da biste ispravno instalirali paket, trebate stvoriti (ili privremeno preimenovati) korisnike u svom okruženju tako da odgovaraju konfiguraciji ulaznih oglednih podataka.

Da biste stvorili ili konfigurirali korisnike, idite na **Postavke** > **Sigurnost** > **Korisnici**, a zatim učinite sljedeće:

1. Korisniku UserFullname="Spencer Low" s korisničkim imenom „spencerl” (**mala slova**) dodijelite ulogu voditelja projekta i upravitelja prakse.

2. Odaberite korisnika **Spencer Low** , a zatim odaberite **Upravljanje ulogama**. Pronađite i odaberite ulogu **Administrator sustava**, a zatim odaberite **U redu** da biste dodijelili potpuna administratorska prava Spenceru Lowu. Taj je korak potreban kako bi se osiguralo da stvoreni ogledni zapisi imaju ispravno korisničko vlasništvo te da se prikazi ispravno popune.

3. U preuzetom paketu morate ažurirati datoteku za mapiranje podataka adresama e-pošte zadanog korisničkog konteksta. Kako biste to učinili, otvorite mapu **PkgFolder**, a zatim pronađite i otvorite datoteku **ImportUserMapFile.xml** u programu Notepad (alatu Visual Studio ili nekom drugom XML uređivaču). Postavite polje **DefaultUserToMapTo =** na adresu e-pošte korisnika Spencera Lowa.

4. Ako za korisnika niste odabrali Spencera Lowa s korisničkim imenom **spencerl**, morate ažurirati dodatnu datoteku. Otvorite datoteku **DemoDataPreImportConfig.xml**, a zatim pronađite oznaku **userstocreateandconfigure**. Ažurirajte oznaku **\<login\>** korisničkim imenom korisnika Tome Debeljaka. Dodatne pojedinosti potražite u [tehničkim napomenama](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Stvaranje ili konfiguriranje korisnika – paket pokaznih podataka

Za paket pokaznih podataka potrebno je šest korisnika. Da bi se paket pravilno instalirao, učinite sljedeće:

 1. Stvorite nove korisnike ili privremeno preimenujte postojeće tako da odgovaraju ulaznoj konfiguraciji oglednih podataka. To možete učiniti u odjeljku **Postavke** > **Sigurnost** > **Korisnici**.
 
    Te su uloge potrebne samo za pokazne programe koji se temelje na osobama.  
    - Ime i prezime korisnika = „David So” kao tehničar za upravljanje terenskom uslugom (Field Service)   
    - Ime i prezime korisnika = „Reding Jamie” kao Otpremnik službe za korisnike (Customer Service) i Otpremnik terenske usluge (Field Service)   
    - Ime i prezime korisnika = „Molly Clark” kao Upraviteljica računa   
    - Ime i prezime korisnika = „Spencer Low” kao Upravitelj vježbi i Voditelj projekta  
    - Ime i prezime korisnika = „Veronica Quek” kao član tima   
    - Ime i prezime korisnika=„William Contoso”
  
2. U svrhe uvoza pokaznih podataka dodijelite šest korisnika s ulogom iznad uloge administratora da bi se uzorci zapisa pravilno uvezli. 

3. Otvorite mapu **PkgFolder** i zatim pronađite i otvorite datoteku **ImportUserMapFile.xml**. Ažurirajte polja **Novo=** tako da sadrže adrese e-pošte odgovarajućih korisnika u vašem sustavu.

   > [!div class="mx-imgBorder"]
   > ![Snimka zaslona s prikazom datoteke UserMapFile.](media/sample-data-7.png)

4. Ako vaš korisnik s imenom i prezimenom „Spencer Low” ima drugačiji korisnički ID od **"spencerl**, morate ažurirati dodatnu datoteku. Otvorite datoteku **DemoDataPreImportConfig.xml** pa pronađite oznaku **userstocreateandconfigure**. Ažurirajte oznaku **\<login\>** s pomoću ID-a za prijavu (razlikovanje velikih i malih slova). 

5. Kalendar prvog korisnika (u oznaci **userstocreateandconfigure**) upotrebljava se za ispunjavanje radnog vremena za sve resurse koje je moguće rezervirati pri uvozu pokaznih podataka. Idite na **Postavke** > **Sigurnost** > **Korisnici**, pronađite svojeg korisnika „Spencer Low” i otvorite mogućnost „Radno vrijeme”. Uredite postojeće radno vrijeme uz odabir mogućnosti **Cijeli tjedni raspored koji se ponavlja od početka do kraja**. Provjerite je li **radno vrijeme postavljeno na 8 – 17 sati (9 sati), od ponedjeljka do petka, s vremenskom zonom Pacifičko vrijeme (SAD i Kanada)**. To je potrebno kako biste osigurali pravilan prikaz ploče projekta i rasporeda.

**Preporuka:** bilo bi dobro da odmah stvorite sigurnosnu kopiju svoje organizacije u slučaju da se morate vratiti na početnu točku ako nešto ne bude u redu tijekom instalacije oglednih podataka. Dodatne informacije potražite u članku [Sigurnosno kopiranje i vraćanje instanci](/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Pokrenite Package Deployer

1. Pronađite i pokrenite datoteku **PackageDeployer.exe** u mapi **v902FPSMasterData** ILI **PackageDeployer_FPSDemoData**.

2. Prihvatite uvjete i odredbe.

3. Na sljedećem prozoru:

   a. Odaberite vrstu implementacije sustava **Office 365**.

   b. Koristite korisničko ime i lozinku administratora sustava konfiguriranog u odjeljku „Stvaranje ili konfiguriranje korisnika” („Spencer Low” s korisničkim imenom „spencerl”).

   c. Provjerite je li odabrana opcija **Prikaži popis dostupnih organizacija**.

      > [!div class="mx-imgBorder"]
      > ![Snimka zaslona s prikazom prozora aplikacije Package Deployer s odabranom mogućnošću „Prikaži popis dostupnih tvrtki ili ustanova”](media/sample-data-2.png)

4. Odaberite tvrtku ili ustanovu u koju želite instalirati ogledne podatke.

5. Odaberite **Sljedeće** dok se ne prikaže dijaloški okvir **Postavljanje demo podataka**.

   > [!div class="mx-imgBorder"]
   > ![Snimka zaslona prozora statusa instalacijskog programa za demo podatke.](media/sample-data-3.png)

6. Prije nastavka napominjemo da instaliranje oglednih podataka može potrajati do jedan sat (obično ~10 minuta). Morate se pobrinuti da računalo ostane uključeno i povezano s mrežom tijekom cijelog postupka instalacije te da vaša sesija ostane aktivna.   

7. Kada ste spremni, kliknite **Sljedeće** da biste pokrenuli postupak instalacije oglednih podataka. Nakon što se ogledni podaci učitaju, pritisnite **Završi**.

## <a name="verify-the-sample-data-installation"></a>Provjera instalacije oglednih podataka

Da biste provjerili je li sve u redu, pogledajte izgleda li broj zapisa i vrsta entiteta navedenih u izmišljenom scenariju za Fabrikam Robotics kako treba.

Nakon što se ogledni podaci potpuno učitaju, prijavite se kao korisnik Spencer Low i potvrdite sljedeće:

- Ako je instalirana aplikacija Project Service, idite na **Project Service** > **Postavke** > **Cjenici**. Potvrdite jesu li u skupu podataka navedene stope naplate i troškova u odgovarajućoj valuti za svaku zemlju/regiju.

- Ako je instalirana aplikacija Project Service, idite na stavku **Universal Resource Scheduling** > **Postavke** > **Organizacijska jedinica**. Potvrdite da je cjenik u odgovarajućoj valuti povezan sa svakom organizacijskom jedinicom (osim unosa gradova). Ako bilo koji nedostaje, pronađite i povežite ispravni cjenik.

- Ako je instalirana aplikacija Field Service, idite na **Project Service** > **Postavke** > **Cjenici**. Potvrdite jesu li navedene stope naplate i troškova. Idite na **Field Service** > **Postavke** > **Cjenici** i provjerite jesu li u skupu podataka navedene stope naplate i troškova u odgovarajućoj valuti za svaku zemlju/regiju.

  > [!div class="mx-imgBorder"]
  > ![Snimka zaslona aktivnih cjenika.](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Snimka zaslona aktivnih organizacijskih jedinica.](media/sample-data-5.png)

## <a name="technical-notes"></a>Tehničke napomene

U nastavku potražite više tehničkih podataka o instalaciji ovih podataka.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Instalacija oglednih podataka preko postojećih podataka (ne preporučuje se)

Ako ogledne podatke morate instalirati preko postojećeg probnog ili demonstracijskog okruženja za Project Service i Field Service koje već sadrži podatke (ne preporučuje se), morat ćete zaustaviti sigurnosne provjere koje izvodi instalacijski program.

Da biste to učinili, u mapi **PkgFolder** pronađite i otvorite datoteku **DemoDataPreImportConfig.xml** u programu Notepad (ili drugom XML uređivaču).

Pronađite sljedeću vrijednost, a zatim promijenite postavku iz true u false:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Zbog te promjene instalacijski program zaobilazi neke važne sigurnosne provjere kojima se između ostalog potvrđuje sljedeće:

- aktivan je samo jedan zapis **Organizacijska jedinica** koji je potom potrebno preimenovati u **Fabrikam US**

- aktivan je samo jedan zapis **Radni predložak**

- aktivan je samo jedan zapis **Projektni parametar** koji je potom potrebno preimenovati u **Parametri**.

### <a name="configuration-components"></a>Komponente konfiguracije

Postoji niz drugih komponenti konfiguracije u ovoj konfiguracijskoj datoteci za preduvoz. Za tehničke korisnike neke od tih komponenti uključuju sljedeće:

- **\<RequiredSolutions\>** navodi preduvjete instalacija rješenja i brojeve njihovih verzija.

- **\<InstallSampleData\>** kontrolira jesu li instalirani gotovi ogledni podaci za aplikacije.

    - false – preskače instalaciju ovih ugrađenih podataka (koji se mogu ukloniti)

    - true – instalira ugrađene podatke istodobno s instalacijom oglednih podataka za FS i PSA

- **\<PreImportDataCollection\>** navodi mape podataka s plošnim podacima i povezane zapise koji će se uvesti prije instalacije glavnih oglednih podataka.

- **\<EntitiesToEnableScheduling\>** navodi koje bi entitete trebalo omogućiti za rezervaciju u sustavu Microsoft Dynamics Scheduling (poznatom i kao Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** navodi resurse koje je moguće rezervirati, a koji će se stvoriti (ako već ne postoje) prije nego što se izvrši uvoz oglednih podataka. Imajte na umu da se ime i prezime (FullName) i podaci za prijavu svakog resursa (koji se može rezervirati) oglednih podataka izvornog sustava podudaraju s imenom i prezimenom i podacima za prijavu zapisa resursa (koji se može rezervirati) ciljnog sustava. Stoga NIJE moguće promijeniti nazive u toj predkonfiguracijskoj datoteci, osim ako najprije ne uvezete ogledne podatke u ciljni sustav pomoću tih imena, a zatim preimenujete resurse koje je moguće rezervirati u željeni skup naziva zajedno sa zapisima omogućenog korisnika te potom ponovno izvezete podatke u konačni odredišni sustav (ažurirajući na odgovarajući način stare i nove unose za **ImportUserMapFile.xml**).

- **\<PluginsToDisable\>** navodi točne dodatke stavke retka koje je potrebno onemogućiti tijekom uvoza oglednih podataka, a zatim kasnije ponovno omogućiti.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Izmišljeni scenarij za Fabrikam Robotics

Paketi referentnih podataka za Field Service i Project Service instaliraju **rješenje Fabrikam Manufacturing Master Data (v3.0.0.0)** zajedno s približno 4000 zapisa i približno 40 različitih entiteta. Zasebni paketi oglednih podataka za Field Service ili Project Service sadrži podskup oglednih podataka **v902FPSMasterData** za tu aplikaciju. Paket **Pokazni podaci** instalira **rješenje Fabrikam Manufacturing Demo Data (v3.0.0.7)** s približno 22.000 zapisa u 148 entiteta.

Izmišljena tvrtka Fabrikam Robotics proizvođač je robota za pokretne trake za sastavljanje elektroničkih uređaja i poznata je po kvaliteti svojih proizvoda, inovacija te dobroj službi za korisnike, uključujući planiranje instalacija, implementaciju i trajne usluge održavanja. Fabrikam ima sjedište u Sjedinjenim Američkim Državama (Fabrikam US) i projektne servisne operacije u Francuskoj, Indiji, Ujedinjenom Kraljevstvu i Švicarskoj.

Terenske operacije najzastupljenije su u Sjedinjenim Američkim Državama, uglavnom na širem području Seattlea. Tvrtka nastoji povezivanjem interneta stvari (IoT) pratiti performanse sredstava klijenata i pružati proaktivnije usluge na lokaciji klijenta.

Detaljni pregled oglednih podataka je sljedeći:

- uobičajeni elementi oglednih podataka (uključeno za obje aplikacije)

    - 1 korisnik

    - 71 račun

    - 137 kontakata

    - različite vrste i kategorije transakcija

    - 50 proizvoda s jednim cjenikom

    - 14 cjenika/troškovnika

    - 31 karakteristika (vještine resursa) u 2 modela ocjenjivanja s 3 razine (vrijednosti ocjenjivanja)

- Project Service

    - 8 organizacijskih jedinica

    - 6 razina korištenja za određene uloge

    - više od 2800 specifikacija cijene uloge

- Field Service

    - 4 teritorija

    - 5 vrsta radnih naloga

    - 22 sredstva klijenta

    - 9 vrsta incidenta s rasponom povezanih karakteristika resursa (9), usluga (13) i servisnih zadataka (13)
   
Paket **Pokazni podaci** instalira približno 179 radnih naloga, 12 projekata i povezane transakcijske podatke. 

### <a name="change-the-work-hours-for-sample-resources"></a>Promjena radnih sati za ogledne resurse

Prema zadanim postavkama, svi resursi koje je moguće rezervirati imaju kalendar s 24 radna sata.

Ako morate promijeniti radne sate za ogledne resurse koje je moguće rezervirati, idite na **Universal Resource Scheduling** > **Planiranje** > **Resursi**.

Odaberite korisnika (na primjer, Spencer Low) i promijenite radne sate za Spencera u sate koje želite primijeniti na više korisnika. Idite na **Universal Resource Scheduling** > **Postavke** > **Predlošci radnih sati** i uredite zapis **Zadani radni predložak**. U polju **Resurs predloška** odaberite korisnika s radnim satima koje želite primijenite na druge resurse. Idite na **Universal Resource Scheduling** > **Planiranje** > **Resursi** > **Aktivni resursi koje je moguće rezervirati**. Odaberite resurse koje želite promijeniti, a zatim odaberite **Postavi kalendar**. Na padajućem popisu **Radni predložak** odaberite predložak **Zadani radni sat** ili drugi predložak s ispravnim resursom predloška. Kada otvorite ploču s rasporedom, morali biste moći vidjeti da su resursi u međuvremenu ažurirali radne sate.

> [!div class="mx-imgBorder"]
> ![Snimka zaslona aktivnih resursa koje je moguće rezervirati.](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]