---
title: Upravljanje resursima
description: Ova tema pruža informacije o tome kako možete upravljati resursima.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d47be6c11ced70b94b7497dfbc0c67d1a3f631b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274989"
---
# <a name="manage-resources"></a>Upravljanje resursima

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation uključuje nadzornu ploču upravitelja resursa koja pruža vizualni pregled potražnje resursa i korištenja na svim razinama ustanove. Grafikone na toj nadzornoj ploči možete koristiti za vizualizaciju sljedećih informacija:

- **Potražnja za resursima** – grafikon **Zahtjevi za aktivne resurse** prikazuje poslane resurse. Resursi se agregiraju prema ulozi ili projektu.
- **Potražnja za neposlanim resursima** – grafikon **Potražnja za nedodijeljenim resursima** prikazuje sve preduvjete resursa koji nisu poslani. Pomaže upraviteljima resursa da pregledaju potražnju koja nije utvrđena i može se poslati putem zahtjeva za resurs.
- **Naplativo korištenje za protekli tjedan** – grafikon **Korištenje po ulozi** prikazuje postotak stvarnog naplativog korištenja ustanove po ulozi u odnosu na ciljano naplativo korištenje po ulozi.

    > [!NOTE]
    > Da bi grafikon **Korištenje po ulozi** učinili dostupnim, stvorite posao koji izvodi tijek rada UpdateRoleUtilization. Taj ponavljajući posao izvodi se svakih sedam dana radi izračuna naplativog korištenja za prethodnih sedam dana. Rezultati su agregirani po ulozi.

## <a name="manage-project-team-members"></a>Upravljanje članovima projektnog tima

Upravitelji projekata mogu koristiti nadzornu ploču upravitelja resursa za upravljanje resursima u projektima. Na primjer, mogu dodati člana tima izravno u projekt i rezervirati člana tima kako bi se ispunili preduvjeti resursa koje je zabilježio generički resurs.

### <a name="add-a-team-member-directly-to-a-project"></a>Dodavanje člana tima izravno u projekt

Da biste člana tima dodali izravno u projekt, na stranici **Projekti** na kartici **Tim** odaberite **Novo**. Prikazat će se dijaloški okvir **Brza izrada: član projektnog tima**. U tom dijaloškom okviru možete izvršiti sljedeće zadatke:

- **Rezervirajte imenovani resurs** – u polju **Resurs koji je moguće rezervirati** odaberite naziv resursa. Zatim odaberite ulogu, postavite razdoblje i odaberite način dodjele. Imenovani resurs koji ste odabrali dodaje se projektu pomoću odabranog načina dodjele i kalendara resursa.
- **Dodajte generički resurs** – ostavite polje **Resurs koji je moguće rezervirati** prazno, a zatim odaberite ulogu, postavite razdoblje i odaberite željeni način dodjele. Generički se resurs dodaje timu kao rezervirano mjesto radi zadržavanja uzorka potražnje koji se koristi za rezerviranje imenovanih resursa u timu. Preduvjet se izrađuje prema kalendaru projekta.
- **Dodajte imenovani resurs timu bez potrošnje kapaciteta resursa** – u polju **Resurs koji je moguće rezervirati** odaberite resurs. Zatim odaberite razdoblje pa kao način dodjele odaberite **Ništa**. Resurs se dodaje timu, no kapacitet resursa ne iskorištava se putem rezervacije.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Rezerviranje člana tima radi ispunjavanja preduvjeta resursa za generički resurs

U PSA-u možete rezervirati generički resurs u projektnom timu i možete odrediti ulogu, potreban kapacitet i način distribucije tog kapaciteta. U preduvjetu resursa možete odrediti atribute koji su pridruženi generičkom resursu. Ti atributi uključuju potrebne vještine, željenu organizacijsku jedinicu i željene resurse.

Poduzmite ove korake da biste naveli potrebne vještine u generičkom resursu za razvojnog programera.

1. Da biste rezervirali generički resurs, na stranici **Projekti** na kartici **Tim** odaberite **Novo**.

    ![Generički resurs rezerviran u timu](media/Resource-Management-image9.png)

2. U prikazu **Svi članovi tima** u stupcu **Preduvjet resursa** odaberite vezu za dodavanje potrebnih vještina za generički resurs.

    ![Veza preduvjeta](media/Resource-Management-image10.png)

3. Da biste dodali potrebne vještine za razvojnog programera, na stranici **Preduvjet resursa** koja se prikaže u rešetki **Vještine** odaberite tri točke (**...**), a zatim odaberite **Dodaj novu značajku preduvjeta**.

    ![Naredba za dodavanje nove značajke uvjeta](media/Resource-Management-image11.png)

4. U dijaloškom okviru **Brza izrada: značajka preduvjeta** koji se prikaže, u polju **Značajka** odaberite potrebnu vještinu. Zatim u polju **Vrijednost ocjene** odaberite razinu stručnosti za tu vještinu. Na kraju u polju **Preduvjet resursa** postavite preduvjet na izvorne resurse iz organizacijskih jedinica ili čak imenovanih resursa. Kada dovršite, odaberite **Spremi**.

    ![Brza izrada: dijaloški okvir Značajka preduvjeta](media/Resource-Management-image12.png)

5. Na stranici **Preduvjet resursa** odaberite **Rezerviraj** da biste ispunili preduvjet resursa.

    ![Gumb Rezerviraj na stranici Preduvjet resursa](media/Resource-Management-image13.png)

    Možete također odabrati generički resurs u rešetki **Svi članovi tima**, a zatim odabrati **Rezerviraj**.

    ![Gumb Rezerviraj iznad rešetke Svi članovi tima](media/Resource-Management-image14.png)

    > [!NOTE]
    > U ovom primjeru navedeno je 40 potrebnih sati, ali nema stvarnih rezerviranih sati jer generički resursi nemaju rezervacije. Osim toga, ne postoje dodijeljeni sati jer je generički resurs izravno dodan timu. Nije dodan pomoću dodjele zadatka.

    Na stranici **Pomoćnik za raspored** možete filtrirati dostupne resurse prema preduvjetima navedenim u preduvjetu resursa. Resursi se sortiraju prema parametrima sortiranja koji su navedeni na ploči s rasporedom.

    ![Stranica Pomoćnik za raspored](media/Resource-Management-image15.png)

    Evo nekih filtara koji se često koriste:

    - **Karakteristike s ocjenom** – filtriranje po vještinama, certifikatima i drugim kvalitetama resursa, uz ocjene stručnosti.
    - **Uloge** – filtriranje po zadanim ulogama koje su dodijeljene resursima koje je moguće rezervirati.
    - **Organizacijske jedinice** – filtriranje resursa koje je moguće rezervirati prema organizacijskim jedinicama kojima su dodijeljeni.

6. Ako niste zadovoljni rezultatima početnog pretraživanja preduvjeta, možete izmijeniti kriterije filtra. Proširite okno **Prikaz filtra** na lijevoj strani, a zatim odaberite **Pretraži** da biste pronašli dodatne resurse.

    ![Okno Prikaz filtra](media/Resource-Management-image16.png)

7. Da biste promijenili način sortiranja rezultata, odaberite **Sortiraj**.

    ![Naredba za sortiranje](media/Resource-Management-image17.png)

8. Odaberite resurse prema potražnji koja je navedena u preduvjetu, kako je naznačeno na vrhu rešetke. Možete ukloniti odabir ćelija u rešetki i ostaviti taj kapacitet resursa otvorenim. Istodobno je moguće odabrati samo jedan resurs kao rezerviran.

9. Odaberite **Rezerviraj** da biste rezervirali odabrani resurs i ostavite ploču s rasporedom otvorenom, tako da možete odabrati dodatne resurse. Ili odaberite **Rezerviraj i izađi** da biste rezervirali odabrani resurs i zatvorite ploču s rasporedom.

    ![Resurs za rezerviranje](media/Resource-Management-image19.png)

    Primit ćete obavijest o rezerviranim satima. Pokazatelji potražnje prikazuju u kojoj je mjeri preduvjet rezervacije ispunjen i koliko je preostalo do ispunjavanja. Možete vidjeti i koliko je kapaciteta odabranog resursa iskorišteno. Odaberite **Proširi** da biste vidjeli više pojedinosti o rezervacijama resursa.

9. Vratite se na prikaz **Svi članovi tima**. U rešetki možete vidjeti da je generički resurs zamijenjen imenovanim resursom, a 40 sati navedeno je kao rezervirano za taj resurs.

    ![Ažurirana rešetka Svi članovi tima](media/Resource-Management-image20.png)

    > [!NOTE]
    > Dodijeljeni se sati ne prikazuju jer su izravno rezervirani u timu. Nisu rezervirani pomoću dodjele zadatka.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Dodjeljivanje generičkih resursa zadacima i generiranje preduvjeta resursa

U PSA-u možete izraditi zadatke, a zatim im dodijeliti generičke resurse. Na taj način potražnju resursa mogu predstavljati rezervirana mjesta dok procjenjujete svoj raspored i financijske brojeve. Zatim možete generirati preduvjete resursa za generičke resurse i ispuniti ih.

1. Na stranici **Projekti** na kartici **Raspored** odaberite **Dodaj** da biste izradili zadatak.

    ![Izrađen je novi zadatak](media/Resource-Management-image21.png)

2. U polju **Resursi** odaberite simbol **Odabir resursa**. Prikazat će se odabir resursa i postojeći članovi tima za projekt.

    ![Odabir resursa](media/Resource-Management-image22.png)

3. Unesite naziv novog generičkog resursa, a zatim odaberite **Izradi**.

    ![Unesen je naziv novog generičkog resursa](media/Resource-Management-image23.png)

4. U dijaloškom okviru **Brza izrada: član projektnog tima** koji se prikaže, u polju **Značajka** odaberite ulogu generičkog resursa. U polju **Jedinica za resurse** odaberite organizacijsku jedinicu za generički resurs. Zatim odaberite **Spremi**.

    ![Dijaloški okvir Brza izrada: član projektnog tima](media/Resource-Management-image24.png)

    Generički član tima sada je dodijeljen zadatku.

    ![Generički član tima dodijeljen zadatku](media/Resource-Management-image25.png)

    Na kartici **Tim** vidjet ćete novog generičkog člana tima. Imajte na umu da ima samo dodijeljene sate. Ti su sati zbroj svih zadataka koji su dodijeljeni generičkom članu tima. Generički član tima još uvijek nema potrebne sate ili preduvjet resursa.

    ![Generički član tima na kartici Tim](media/Resource-Management-image26.png)

5. Sada možete dodijeliti generičkog člana tima drugim zadacima pomoću odabira resursa.

    ![Generički član tima u odabiru resursa](media/Resource-Management-image27.png)

    Kada dovršite dodjeljivanje generičkog resursa zadacima, možete generirati preduvjet resursa za generički resurs.

5. Na kartici **Tim** odaberite generički resurs, a zatim odaberite **Generiraj preduvjet**.

    ![Naredba za generiranje preduvjeta](media/Resource-Management-image28.png)

    Kada se preduvjet generira, generički član tima imat će potrebne sate i vezu na preduvjet resursa.

    ![Veza na preduvjet resursa](media/Resource-Management-image29.png)

    Nakon što rezervirate imenovani resurs, generički resurs uklanja se iz tima i zamjenjuje imenovanim resursom.

    ![Generički resurs zamijenjen je imenovanim resursom](media/Resource-Management-image30.png)

    Na kartici **Raspored** dodjele generičkih resursa uklonjene su i zamijenjene imenovanim resursom.

    ![Dodjele generičkih resursa zamijenjene imenovanim resursom na kartici Raspored](media/Resource-Management-image31.png)

    > [!NOTE]
    > To se događa samo kada je imenovani resurs u potpunosti rezerviran za preduvjet generičkog resursa. Kada imenovani resurs djelomično zamjenjuje generički uvjet resursa ili više imenovanih resursa zamjenjuje preduvjet generičkog resursa, generički resurs ostaje dodijeljen zadatku.

    Na sljedećoj ilustraciji 80-satni zadatak planiran je za trajanje od pet dana (16 sati dnevno tijekom pet dana) i dodijeljen generičkom resursu koji naziva **Funkcionalno**.

    ![80-satni, petodnevni zadatak dodijeljen generičkom resursu naziva Funkcionalno](media/Resource-Management-image32.png)

    Kada generirate preduvjet, on se odnosi na 80 sati tijekom pet dana.

    ![Preduvjet generiran za 80 sati tijekom pet dana](media/Resource-Management-image33.png)

    Budući da dostupni resursi funkcioniraju samo osam sati dnevno, za ispunjavanje preduvjeta potrebna su dva resursa.

    ![Drugi resurs](media/Resource-Management-image35.png)

    Na kartici **Tim** sada možete vidjeti da generički resurs nema potrebne sate, ali dodijeljeni sati i dalje se prikazuju s dva imenovana resursa koji su potrebni za ispunjavanje preduvjeta.

    ![Dva imenovana resursa na kartici Tim](media/Resource-Management-image36.png)

    Na kartici **Raspored** generički resurs ostaje dodijeljen zadatku.

    ![Generički resursi na kartici Raspored](media/Resource-Management-image37.png)

PSA ne dodjeljuje oba resursa zadatku jer bi to ponašanje rezultiralo manje predvidljivim rasporedom. U ovom jednostavnom primjeru lako je podijeliti sate jednako između dva resursa. Međutim, u složenijim scenarijima koji uključuju više zadataka i više resursa, PSA bi morao donijeti pretpostavke o tome kako bi trebao dodijeliti rezervacije koje su primljene za više resursa u više zadataka.

Stoga je u tim scenarijima upravitelj projekta odgovoran za raščlanjivanje više rezervacija i njihovo dodjeljivanje po potrebi. Da bi dodijelio rezervacije, upravitelj projekta dodjeljuje zadatke iz generičkih resursa imenovanom resursu i zatim koristi prikaz **Usklađivanje** kako bi se osiguralo da dodjela funkcionira s rezervacijama.

### <a name="edit-a-resource-requirement"></a>Uređiivanje preduvjeta resursa

Nakon izrade preduvjeta resursa upravitelj projekta ili upravitelj resursa možda će htjeti urediti pojedinosti kako bi precizirao kriterije pretraživanja pri upotrebi ploče s rasporedom. Da biste uredili preduvjet resursa, poduzmite ove korake.

1. Na stranici **Projekti** na kartici **Tim** odaberite vezu na bilo koji preduvjet generičkog resursa.
2. Na stranici **Preduvjet resursa** koja se prikaže možete ažurirati nekoliko atributa. Evo nekoliko primjera:

    - naziv
    - Od datuma
    - Do datuma
    - Trajanje
    - Vrsta resursa

Na stranici **Preduvjet resursa** upravitelj projekta ili upravitelj resursa može definirati i sljedeće podatke:

- Vještine
- Uloge
- Preference resursa
- Željena organizacijska jedinica

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Ažuriranje rezervacija resursa nakon što su rezervirane u projektu

Nakon što dodate generički ili imenovani resurs u projektni tim, možete promijeniti rezervacije resursa.

1. Na stranici **Projekti** na kartici **Tim** odaberite člana tima, a zatim odaberite **Zadrži rezervacije**.

    ![Ploča s rasporedom otvorena za odabranog člana tima](media/Resource-Management-image40.png)

    Prikazuju se ploča s rasporedom i rezervacije člana projektnog tima. Proširite zapis člana tima da biste vidjeli sate koji su rezervirane za taj projekt i druge projekte koji koriste kapacitet člana tima.

2. Odaberite i povucite rezervaciju da biste je produljili ili skratili. Prikazuje se dijaloški okvir **Izrada rezervacije resursa** koji vam omogućuje prilagodbu rezervacije.

    ![Dijaloški okvir Izrada rezervacije resursa](media/Resource-Management-image41.png)

3. Desnom tipkom miša kliknite rezervaciju. Zatim možete koristiti izbornik prečaca da biste dovršili sljedeće radnje:

    - Izmijenite status rezervacije.
    - Uredite rezervaciju.
    - Zamijenite resurs u projektnom timu.

### <a name="change-the-booking-status"></a>Izmjena statusa rezervacije

Možete izmijeniti bilo koji zadani ili prilagođeni status rezervacije.

![Naredba za status izmjene](media/Resource-Management-image42.png)

PSA obuhvaća sljedeće statuse:

- **Otkazano** – ovaj status poništava rezervaciju resursa i oslobađa kapacitet resursa.
- **Fiksna rezervacija** – ovaj status koristi kapacitet resursa. Rezervacija obično ima taj status kada otvorite **Zadržavanje rezervacija** iz rešetke **Svi članovi tima** na stranici **Projekti**.
- **Promjenjiva rezervacija** – ovaj status dodaje resurs timu, ali ne koristi kapacitet resursa. To označava da je resurs rezerviran za potencijalni rad, ali još uvijek ima kapacitet ako je potreban za druge poslove. U prikazu ukupne dostupnosti resursa promjenjive rezervacije imaju različit status od fiksnih rezervacija.
- **Predloženo** – ovaj status predstavlja prijedlog upravitelja resursa ili upravitelja projekta za resurs. Prijedlozi ne koriste kapacitet resursa, a resurs nije dodan u projektni tim. Da biste fiksno rezervirali resurs u timu, upravitelj projekta mora prihvatiti prijedlog.

### <a name="submit-resource-requests"></a>Pošalji zahtjeve za resurs

Zahtjevi za resurse koriste se za prijenos potražnje (preduvjet resursa) koji upravitelj resursa mora ispuniti. Za generički resurs koji je već u timu možete izravno poslati zahtjev za resurs. Zahtjev za resurs može se ispuniti na dva načina:

- Upravitelj resursa izravno ispunjava zahtjev. U tom slučaju generički resurs zamjenjuje se fiksnom rezervacijom koja sadrži imenovani resurs.
- Upravitelj resursa predlaže resurs upravitelju projekta, a upravitelj projekta odobrava ili odbacuje predloženi resurs.

#### <a name="direct-fulfillment-of-resource-requests"></a>Izravno ispunjavanje zahtjeva za resurse

Kada se generira preduvjet resursa, upravitelj projekta može poslati zahtjev za resurs za generički resurs tako da odabere resurs, a zatim **Pošalji zahtjev**.

![Gumb Pošalji zahtjev](media/Resource-Management-image45.png)

Komentari o resursu mogu se pružiti upravitelju resursa koji ispunjava zahtjev. Nakon podnošenja zahtjeva polje **Status** za člana tima mijenja se u **Poslano.**

![Unos neobaveznih komentara](media/Resource-Management-image46.png)

Kada upravitelj resursa ispuni zahtjev, generički član tima zamjenjuje se imenovanim resursom u rešetki **Svi članovi tima**.

![Generički član tima zamijenjen imenovanim resursom u rešetki Svi članovi tima](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Upotreba prijedloga resursa za zahtjeve za resurse

Umjesto izravnog rezerviranja resursa u zahtjevu resursa, upravitelj resursa može predložiti resurs upravitelju projekta. Upravitelj resursa može koristiti ovu mogućnost kada točno podudaranje za zahtjeve nije dostupno. Kada upravitelj resursa predloži resurs, upravitelj projekta vidi da se polje **Status** za generičkog člana tima izmijenilo u **Potreban pregled**.

![Status generičkog člana tima izmijenjen u Potreban pregled](media/Resource-Management-image48.png)

Za prikaz predloženog resursa zajedno s vizualizacijom učinka rezervacije prijedloga dvaput kliknite člana tima koji ima status pregleda **Potreban pregled**. Zatim odaberite karticu **Predloženi resursi**.

![Kartica Predloženi resursi](media/Resource-Management-image49.png)

Odaberite **Prihvati sve prijedloge** kako biste prihvatili sve predložene resurse ili **Odbaci sve prijedloge** kako biste ih odbacili. Ako prihvatite predložene resurse, oni se fiksno rezerviraju u projektu kao članovi tima i zamjenjuju generičke resurse.

> [!NOTE]
> Morate prihvatiti ili odbaciti sve predložene resurse. Ne možete ih djelomično prihvatiti ili odbaciti.

### <a name="substitute-a-resource-on-the-project-team"></a>Zamjena resursa u projektnom timu.

Ponekad upravitelj projekta mora zamijeniti rezerviranog člana tima na projektu.

1. Na stranici **Projekti** na kartici **Tim** odaberite resurs koji je potrebno zamijeniti, a zatim odaberite **Zadrži rezervacije**.
2. Proširite resurs da biste vidjeli projekte kojima je dodijeljen.

    ![Resurs proširen za prikaz dodijeljenih projekata](media/Resource-Management-image50.png)

3. Desnom tipkom miša kliknite projekt, a zatim odaberite **Zamijeni resurs**.
4. Ako znate kojim resursom želite želite zamijeniti trenutačni resurs, odaberite ili unesite naziv, a zatim odaberite **Ponovno dodijeli**.

    ![Određivanje zamjenskog resursa](media/Resource-Management-image51.png)

    Umjesto toga, poduzmite ove korake da biste pretražili resurs:

    1. Odaberite **Pronađi zamjenu**.

        ![Pretraživanje zamjenskog resursa](media/Resource-Management-image52.png)

        Pomoćnik za raspored vraća popis dostupnih zamjena. U pomoćniku za raspored možete dodatno filtrirati dostupne resurse kako biste pronašli odgovarajuću zamjenu.

        ![Popis dostupnih zamjena](media/Resource-Management-image53.png)

    2. Da biste zamijenili resurs, odaberite željeni resurs, a zatim odaberite **Zamijeni**.

        ![Zamjenski resurs odabran](media/Resource-Management-image54.png)

    Rezervacije i dodjele zamjenjuju se novim resursom.

    ![Rezervacije i dodjele zamijenjene novim resursom](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Usklađivanje rezervacija i dodjela člana tima

Za članove tima rezervacije i dodjele slobodno se uparuju. Drugim riječima, resursi mogu imati dodjele, ali ne i rezervacije ili pak mogu imati rezervacije, ali ne i dodjele. U idealnom slučaju rezervacije i dodjele trebaju biti usklađene, tako da resursi imaju potvrđeni kapacitet za izvođenje dodjela zadataka. Međutim, rezervacije se mogu temeljiti na dostupnosti, a vremenski rasporedi zadataka mogu se promijeniti tijekom nastavka projekta. Stoga slobodno uparivanje rezervacija i dodjela pruža fleksibilnost.

PSA ima karticu **Usklađivanje** koja upraviteljima projekata omogućuje usklađivanje rezervacija članova tima i njihovih zadataka za projektne timove.

![Kartica Usklađivanje](media/Resource-Management-image56.png)

Kartica **Usklađivanje** prikazuje rezervacije i dodjele na razini dodjele pojedinačnog zadatka za svakog člana tima. Prikazuje sate u ćelijama koje predstavljaju vremensko razdoblje od mjeseci do dana.

Kartica također prikazuje ukupni neto iznos za projekt, zajedno sa stupcem ukupne vrijednosti.

Za svaki resurs kartica izračunava razliku između rezervacija člana tima i skupnu vrijednost dodjela zadataka člana tima. Ta bi razlika idealno trebala iznositi 0 (nula). Drugim riječima, ne bi trebalo biti razlike između rezervacija i dodjela. Razlike su obojene i zasjenjene kako bi privukle pozornost na dva uvjeta:

- **Nedostatak rezervacija** – nedostatak rezervacija događa se kada resurs ima više dodjela nego rezervacija. Budući da taj kapacitet nije rezerviran, upravitelj projekta možda će htjeti ispraviti taj uvjet produljivanjem rezervacija resursa kako bi se pokrio manjak.
- **Previše rezervacija** – previše se rezervacija pojavljuje kada je resurs rezerviran za projekt, ali nije dodijeljen zadacima. Taj uvjet može biti prihvatljiv u slučajevima kada je resurs rezerviran za projekt prije dodjele zadataka. Međutim, u drugim slučajevima resurs nije planiran za dodjelu zadacima. U tim slučajevima upravitelj projekta trebao bi razmotriti otkazivanje rezervacija resursa, tako da se kapacitet može koristiti za drugi projekt.

U nekim slučajevima, kada pregledate vrijeme na razini koja je viša od dnevne (na primjer, razina mjeseca), možda ćete vidjeti neto razliku u iznosu nula za resurs (drugim riječima, rezervacije = dodjele). Međutim, ako pogledate vrijeme na razini tjedna, možda ćete vidjeti da postoje dodjele od nula sati i rezervacije od 40 sati u prvom tjednu, no dodjele od 40 sati i rezervacije od nula sati u drugom tjednu. Sveukupno, rezervacije i dodjele usklađene su, ali se razlikuju od jednog do drugog tjedna.

Kada pogledate vrijeme na višim razinama, ćelije na kartici **Usklađivanje** imaju pokazatelj koji će vas obavijestiti da postoje razlike na nižim razinama. Dvostrukim klikom na ćeliju možete povećati prikaz razlike. Zatim desnom tipkom miša možete pritisnuti gumb da biste smanjili prikaz. Odabirom resursa i korištenjem kontrole **Sljedeća razlika** na alatnoj traci rešetke možete ići na sljedeću razliku između rezervacija i dodjela za taj resurs. Zatim možete koristiti kontrolu **Prethodna razlika** da biste se vratili. Možete i isključiti pokazatelj razlike i ponašanje navigacije u odjeljku **Postavke.**

![Pokazatelj razlike](media/Resource-Management-image57.png)

Ako imate dodjele zadataka za resurs, ali bez rezervacija, na stranici **Projekti** na kartici **Usklađivanje** odaberite manjak rezervacija, a zatim odaberite **Produlji rezervaciju**. Prikazat će se dijaloški okvir **Produlji rezervaciju** produljivanje rezervacije i rezervacija koju je potrebna za rješavanje manjka resursa. Prikazuju se i postojeće rezervacije resursa u svim projektima ili drugim entitetima koji se mogu zakazati. Ako odaberete **U redu** da biste izradili rezervaciju za resurs, bez obzira na dostupnost tog resursa, može doći do prebukiranosti.

![Dijaloški okvir Produlji rezervaciju](media/Resource-Management-image58.png)

Upravitelj projekta ili upravitelj resursa zatim može koristiti ploču s rasporedom kako bi upravljao svim situacijama u kojima je resurs prebukiran izvan svog kapaciteta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]