---
title: Dodavanje članova tima iz rešetke članova tima
description: U ovom se članku nalaze informacije o upravljanju resursima članova tima.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3c0c277ca1fe2b709a6ff1c626f5ea7ec63705d6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928561"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Dodavanje članova tima iz rešetke članova tima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations uključuje nadzornu ploču upravitelja resursa koja pruža vizualni pregled potražnje resursa i korištenja na svim razinama ustanove. Grafikone na toj nadzornoj ploči možete koristiti za vizualizaciju sljedećih informacija:

- **Potražnja za resursima**: Grafikon **Zahtjevi za aktivne resurse** prikazuje poslane resurse. Resursi se agregiraju prema ulozi ili projektu.
- **Potražnja za neposlanim resursima**: Grafikon **Potražnja za resursima koji nisu dodijeljeni** prikazuje sve preduvjete resursa koji nisu poslani. Taj grafikon pomaže upraviteljima resursa da pregledaju potražnju koja nije utvrđena i može se poslati putem zahtjeva za resurs.
- **Naplativo korištenje za protekli tjedan**: Grafikon **Iskoristivost po ulozi** prikazuje postotak stvarno naplative iskoristivosti tvrtke ili ustanove po ulozi u odnosu na ciljano naplativo korištenje po ulozi.

    > [!NOTE]
    > Kako bi grafikon **Iskoristivost po ulozi** učinili dostupnim, stvorite posao koji izvodi tijek rada **UpdateRoleUtilization**. Taj ponavljajući posao izvodi se svakih sedam dana radi izračuna naplativog korištenja za prethodnih sedam dana. Rezultati su agregirani po ulozi.

## <a name="manage-project-team-members"></a>Upravljanje članovima projektnog tima

Upravitelji projekata mogu upotrebljavati nadzornu ploču upravitelja resursa za upravljanje resursima u projektima. Na primjer, mogu dodati člana tima izravno u projekt i rezervirati člana tima kako bi se ispunili preduvjeti resursa koje je zabilježio generički resurs.

### <a name="add-a-team-member-directly-to-a-project"></a>Dodavanje člana tima izravno u projekt

Kako biste člana tima dodali izravno u projekt, na obrascu **Projekti** na kartici **Tim** odaberite **Novo**. Prikazat će se dijaloški okvir **Brza izrada: član projektnog tima**. U tom dijaloškom okviru možete izvršiti sljedeće zadatke:

- **Rezerviraj imenovani resurs**: U polju **Resurs koji je moguće rezervirati** odaberite naziv resursa. Zatim odaberite ulogu, postavite razdoblje i odaberite način dodjele. Imenovani resurs koji ste odabrali dodaje se projektu pomoću odabranog načina dodjele i kalendara resursa.
- **Dodaj generički resurs**: Ostavite polje **Resurs koji je moguće rezervirati** prazno, a zatim odaberite ulogu, postavite razdoblje i odaberite željeni način dodjele. Generički resurs dodaje se timu kao rezervirano mjesto. Rezervirano mjesto zadržava obrazac potražnje koji se upotrebljava za rezerviranje imenovanih resursa u timu. Preduvjet se izrađuje prema kalendaru projekta.
- **Dodaj imenovani resurs timu bez potrošnje kapaciteta resursa**: U polju **Resurs koji je moguće rezervirati** odaberite resurs. Odaberite razdoblje pa kao način dodjele odaberite **Ništa**. Resurs se dodaje timu, no kapacitet resursa ne iskorištava se putem rezervacije.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Rezerviranje člana tima radi ispunjavanja preduvjeta resursa za generički resurs

U aplikaciji Project Operations možete rezervirati generički resurs za projektni tim. Također možete odrediti ulogu, potrebni kapacitet i način na koji se taj kapacitet raspoređuje. Za preduvjet resursa možete odrediti atribute koji su povezani s generičkim resursom. Ti atributi uključuju potrebne vještine, željenu organizacijsku jedinicu i željene resurse.

Izvršite ove korake kako biste odredili potrebne vještine razvojnog programera u generičkom resursu.

1. Kako biste rezervirali generički resurs, na obrascu **Projekti**, na kartici **Tim**, odaberite mogućnost **Novo**.
2. U prikazu **Svi članovi tima** u stupcu **Preduvjet resursa** odaberite vezu za dodavanje potrebnih vještina za generički resurs.
3. Kako biste dodali potrebne vještine razvojnog programera, na obrascu **Preduvjet resursa** u rešetki **Vještine** odaberite tri točke (**...**), a zatim odaberite **Dodaj novu značajku preduvjeta**.
4. U dijaloškom obrascu **Brza izrada: Značajka preduvjeta**, u polju **Značajka** odaberite potrebnu vještinu.
5. U polju **Vrijednost ocjene** odaberite razinu stručnosti za tu vještinu. 
6. U polju **Preduvjet resursa** postavite preduvjet na izvorne resurse iz organizacijskih jedinica ili čak imenovanih resursa. Kada dovršite, odaberite **Spremi**.
7. U obrascu **Preduvjet resursa** odaberite **Rezerviraj** kako biste ispunili preduvjet resursa. Možete također odabrati generički resurs u rešetki **Svi članovi tima**, a zatim odabrati **Rezerviraj**.

    > [!NOTE]
    > U ovom primjeru navedeno je 40 potrebnih sati, ali nema stvarnih rezerviranih sati jer generički resursi nemaju rezervacije. Osim toga, ne postoje dodijeljeni sati jer je generički resurs timu dodan izravno, a ne s pomoću dodjele zadatka.

    Na obrascu **Pomoćnik za raspored** možete filtrirati dostupne resurse prema zahtjevima navedenim u preduvjetu resursa. Resursi se sortiraju prema parametrima sortiranja koji su navedeni na ploči s rasporedom.

   Neki od najčešće upotrijebljenih filtara su sljedeći:

    - **Svojstva s ocjenom**: Filtriranje po vještinama, certifikatima i drugim kvalitetama resursa, uz ocjene stručnosti.
    - **Uloge**: Filtriranje po zadanim ulogama koje su dodijeljene resursima koje je moguće rezervirati.
    - **Organizacijske jedinice**: Filtriranje resursa koje je moguće rezervirati prema organizacijskim jedinicama kojima su dodijeljeni.

8. Ako niste zadovoljni rezultatima početnog pretraživanja preduvjeta, možete izmijeniti kriterije filtra. Proširite okno **Prikaz filtra** na lijevoj strani, a zatim odaberite **Pretraži** da biste pronašli dodatne resurse. Da biste promijenili način sortiranja rezultata, odaberite **Sortiraj**.
9. Odaberite resurse prema potražnji koja je navedena u preduvjetu, kako je naznačeno na vrhu rešetke. Možete ukloniti odabir ćelija u rešetki i ostaviti taj kapacitet resursa otvorenim. Istodobno je moguće odabrati samo jedan resurs kao rezerviran.
10. Odaberite **Rezerviraj** da biste rezervirali odabrani resurs i ostavite ploču s rasporedom otvorenom, tako da možete odabrati dodatne resurse. Ili odaberite **Rezerviraj i izađi** da biste rezervirali odabrani resurs i zatvorite ploču s rasporedom.
11. Vratite se na prikaz **Svi članovi tima**. U rešetki možete vidjeti da je generički resurs zamijenjen imenovanim resursom, a 40 sati navedeno je kao rezervirano za taj resurs.

    > [!NOTE]
    > Dodijeljeni se sati ne prikazuju jer su izravno rezervirani u timu. Nisu rezervirani pomoću dodjele zadatka.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Dodjeljivanje generičkih resursa zadacima i generiranje preduvjeta resursa

U aplikaciji Project Operations možete stvoriti zadatke, a zatim im dodijeliti generičke resurse. Potražnju resursa mogu tada predstavljati rezervirana mjesta dok procjenjujete svoj raspored i financijske brojeve. Zatim možete generirati preduvjete resursa za generičke resurse i ispuniti ih.

1. Na obrascu **Projekti** na kartici **Raspored** odaberite **Dodaj** kako biste izradili zadatak.
2. U polju **Resursi** odaberite simbol **Odabir resursa**. Prikazat će se odabir resursa i postojeći članovi tima za projekt.
3. Unesite naziv novog generičkog resursa, a zatim odaberite **Izradi**.
4. U dijaloškom okviru **Brza izrada: član projektnog tima** koji se prikaže, u polju **Značajka** odaberite ulogu generičkog resursa. 
5. U polju **Jedinica za resurse** odaberite organizacijsku jedinicu za generički resurs. Zatim odaberite **Spremi**. Generički član tima sada je dodijeljen zadatku.

   Na kartici **Tim** vidjet ćete novog generičkog člana tima. Imajte na umu da ima samo dodijeljene sate. Ti su sati zbroj svih zadataka koji su dodijeljeni generičkom članu tima. Generički član tima nema potrebne sate ili preduvjet resursa.

6. Sada možete dodijeliti generičkog člana tima drugim zadacima pomoću odabira resursa.

   Kada dovršite dodjeljivanje generičkog resursa zadacima, možete generirati preduvjet resursa za generički resurs.

7. Na kartici **Tim** odaberite generički resurs, a zatim odaberite **Generiraj preduvjet**. Kada se preduvjet generira, generički član tima imat će potrebne sate i vezu na preduvjet resursa.

  Nakon što rezervirate imenovani resurs, generički resurs uklanja se iz tima i zamjenjuje imenovanim resursom. Na kartici **Raspored** dodjele generičkih resursa uklonjene su i zamijenjene imenovanim resursom.

  > [!NOTE]
  > To se događa samo kada je imenovani resurs u potpunosti rezerviran za preduvjet generičkog resursa. Kada imenovani resurs djelomično zamjenjuje generički preduvjet resursa ili više imenovanih resursa zamjenjuje preduvjet generičkog resursa, generički resurs ostaje dodijeljen zadatku.

Project Operations ne dodjeljuje oba resursa zadatku jer bi to ponašanje rezultiralo manje predvidivim rasporedom. U ovom jednostavnom primjeru lako je podijeliti sate jednako između dva resursa. Međutim, u složenijim scenarijima koji uključuju više zadataka i više resursa, PSA bi morao donijeti pretpostavke o tome kako bi trebao dodijeliti rezervacije koje su primljene za više resursa u više zadataka.

Stoga je u tim scenarijima upravitelj projekta odgovoran za raščlanjivanje više rezervacija i njihovo dodjeljivanje po potrebi. Kako bi dodijelio rezervacije, upravitelj projekta dodjeljuje zadatke iz generičkih resursa imenovanom resursu i zatim koristi prikaz **Usklađivanje** kako bi se osiguralo da dodjela funkcionira s rezervacijama.

### <a name="edit-a-resource-requirement"></a>Uređiivanje preduvjeta resursa

Nakon izrade preduvjeta resursa upravitelj projekta ili upravitelj resursa možda će htjeti urediti pojedinosti kako bi precizirao kriterije pretraživanja pri uporabi ploče s rasporedom. Da biste uredili preduvjet resursa, poduzmite ove korake.

1. Na obrascu **Projekti** na kartici **Tim** odaberite vezu na neki preduvjet generičkog resursa.
2. Na obrascu **Preduvjet resursa** koji se prikaže, unesite potrebne podatke o polju

   Na obrascu **Preduvjet resursa**, voditelj projekta ili resursa također mogu definirati vještine, uloge, postavke resursa i željenu organizacijsku jedinicu.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Ažuriranje rezervacija resursa nakon što su rezervirane u projektu

Nakon što dodate generički ili imenovani resurs u projektni tim, možete promijeniti rezervacije resursa.

1. Na obrascu **Projekti**, na kartici **Tim**, odaberite člana tima, a zatim odaberite **Zadrži rezervacije**.
 
   Prikazuju se ploča s rasporedom i rezervacije člana projektnog tima. Proširite zapis člana tima da biste vidjeli sate koji su rezervirane za taj projekt i druge projekte koji koriste kapacitet člana tima.

2. Odaberite i povucite rezervaciju da biste je produljili ili skratili. Prikazuje se dijaloški okvir **Izrada rezervacije resursa** koji vam omogućuje prilagodbu rezervacije.
3. Desnom tipkom miša kliknite rezervaciju. Zatim možete koristiti izbornik prečaca da biste dovršili sljedeće radnje:

    - Izmjena statusa rezervacije
    - Uredite rezervaciju
    - Zamjena resursa u projektnom timu.

### <a name="change-the-booking-status"></a>Izmjena statusa rezervacije

Možete izmijeniti bilo koji zadani ili prilagođeni status rezervacije.

Project Operations obuhvaća sljedeće statuse:

- **Otkazano**: Poništava rezervaciju resursa i oslobađa kapacitet resursa.
- **Fiksne rezervacije**: Troše kapacitet resursa. Rezervacija obično ima taj status kada otvorite **Zadržavanje rezervacija** iz rešetke **Svi članovi tima** na obrascu **Projekti**.
- **Promjenjiva rezervacija**: Dodaje resurs timu, ali ne upotrebljava kapacitet resursa. Taj status označava da je resurs rezerviran za potencijalni rad, ali još uvijek ima kapacitet za druge poslove, ako je potreban. U prikazu ukupne dostupnosti resursa promjenjive rezervacije imaju različit status od fiksnih rezervacija.
- **Predloženo**: Predstavlja prijedlog upravitelja resursa ili upravitelja projekta za resurs. Prijedlozi ne koriste kapacitet resursa, a resurs nije dodan u projektni tim. Kako biste fiksno rezervirali resurs u timu, upravitelj projekta mora prihvatiti prijedlog.

### <a name="submit-resource-requests"></a>Slanje zahtjeva za resurse

Zahtjevi za resurse upotrebljavaju se za prijenos potražnje ili preduvjet resursa, koji upravitelj resursa mora ispuniti. Za generički resurs koji je već u timu možete izravno poslati zahtjev za resurs. Zahtjev za resurs može se ispuniti na dva načina:

- Upravitelj resursa izravno ispunjava zahtjev. U tom slučaju generički resurs zamjenjuje se fiksnom rezervacijom koja sadrži imenovani resurs.
- Upravitelj resursa predlaže resurs upravitelju projekta, a upravitelj projekta odobrava ili odbacuje predloženi resurs.

#### <a name="direct-fulfillment-of-resource-requests"></a>Izravno ispunjavanje zahtjeva za resurse

Kada se generira preduvjet resursa, upravitelj projekta može poslati zahtjev za resurs za generički resurs tako da odabere resurs, a zatim **Pošalji zahtjev**. Komentari o resursu mogu se dati upravitelju resursa koji ispunjava zahtjev. Nakon podnošenja zahtjeva polje **Status** za člana tima mijenja se u **Poslano.** Kada upravitelj resursa ispuni zahtjev, generički član tima zamjenjuje se imenovanim resursom u rešetki **Svi članovi tima**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Upotreba prijedloga resursa za zahtjeve za resurse

Umjesto izravnog rezerviranja resursa u zahtjevu resursa, upravitelj resursa može predložiti resurs upravitelju projekta. Upravitelj resursa može upotrijebiti ovu mogućnost kada točno podudaranje za zahtjeve nije dostupno. Kada upravitelj resursa predloži resurs, upravitelj projekta vidi da se polje **Status** za generičkog člana tima izmijenilo u **Potreban pregled**.

Predloženi resurs možete pregledati zajedno s vizualizacijom učinka rezervacije prijedloga. 

1. Dvaput kliknite člana tima koji ima status **Potreban pregled**. 
2. Odaberite karticu **Predloženi resursi**.
3. Odaberite **Prihvati sve prijedloge** kako biste prihvatili sve predložene resurse ili **Odbaci sve prijedloge** kako biste ih odbacili. Ako prihvatite predložene resurse, oni se fiksno rezerviraju u projektu kao članovi tima i zamjenjuju generičke resurse.

> [!NOTE]
> Morate prihvatiti ili odbaciti sve predložene resurse. Ne možete ih djelomično prihvatiti ili odbaciti.

### <a name="substitute-a-resource-on-the-project-team"></a>Zamjena resursa u projektnom timu.

Ponekad upravitelj projekta mora zamijeniti rezerviranog člana tima na projektu.

1. Na obrascu **Projekti** na kartici **Tim** odaberite resurs koji je potrebno zamijeniti, a zatim odaberite **Zadrži rezervacije**.
2. Proširite resurs da biste vidjeli projekte kojima je dodijeljen.
3. Desnom tipkom miša kliknite projekt, a zatim odaberite **Zamijeni resurs**.
4. Ako znate kojim resursom želite zamijeniti trenutačni resurs, odaberite ili unesite naziv, a zatim odaberite **Ponovno dodijeli**.

Ili. Ako trebate potražiti resurs, poduzmite sljedeće korake.

1. Odaberite **Pronađi zamjenu**.

   Pomoćnik za raspored vraća popis dostupnih zamjena. U pomoćniku za raspored možete dodatno filtrirati dostupne resurse kako biste pronašli odgovarajuću zamjenu.

2. Da biste zamijenili resurs, odaberite željeni resurs, a zatim odaberite **Zamijeni**.   

   Rezervacije i dodjele zamjenjuju se novim resursom.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Usklađivanje rezervacija i dodjela člana tima

Za članove tima rezervacije i dodjele slobodno se uparuju. Drugim riječima, resursi mogu imati dodjele, ali ne i rezervacije ili pak mogu imati rezervacije, ali ne i dodjele. U idealnom slučaju rezervacije i dodjele trebaju biti usklađene, tako da resursi imaju potvrđeni kapacitet za izvođenje dodjela zadataka. Međutim, rezervacije se mogu temeljiti na dostupnosti, a vremenski rasporedi zadataka mogu se promijeniti tijekom nastavka projekta. Stoga slobodno uparivanje rezervacija i dodjela pruža fleksibilnost.

Project Operations ima karticu **Usklađivanje** koja upraviteljima projekata omogućuje usklađivanje rezervacija članova tima i njihovih zadataka za projektne timove.

Kartica **Usklađivanje** prikazuje rezervacije i dodjele na razini dodjele pojedinačnog zadatka za svakog člana tima. Prikazuje sate u ćelijama koje predstavljaju vremensko razdoblje od mjeseci do dana.

Kartica također prikazuje ukupni neto iznos za projekt, zajedno sa stupcem ukupne vrijednosti.

Za svaki resurs kartica izračunava razliku između rezervacija člana tima i skupnu vrijednost dodjela zadataka člana tima. Ta bi razlika idealno trebala iznositi 0 (nula). Drugim riječima, ne bi trebalo biti razlike između rezervacija i dodjela. Razlike su obojene i zasjenjene kako bi privukle pozornost na dva uvjeta:

- **Nedostatak rezervacija**: Događa se kada resurs ima više dodjela nego rezervacija. Budući da taj kapacitet nije rezerviran, upravitelj projekta možda će htjeti ispraviti taj uvjet produljivanjem rezervacija resursa kako bi se pokrio manjak.
- **Previše rezervacija**: Pojavljuje se kada je resurs rezerviran za projekt, ali nije dodijeljen zadacima. Taj uvjet može biti prihvatljiv u slučajevima kada je resurs rezerviran za projekt prije dodjele zadataka. Međutim, u drugim slučajevima resurs nije planiran za dodjelu zadacima. U tim slučajevima upravitelj projekta trebao bi razmotriti otkazivanje rezervacija resursa, tako da se kapacitet može upotrijebiti za drugi projekt.

U nekim slučajevima, kada pogledate vrijeme na razini koja je viša od dnevne, na primjer, razina mjeseca, možda ćete vidjeti neto razliku u iznosu nula za resurs. Drugim riječima, rezervacije = zadaci. Međutim, ako pogledate vrijeme na razini tjedna, možda ćete vidjeti da postoje dodjele od nula sati i rezervacije od 40 sati u prvom tjednu, no dodjele od 40 sati i rezervacije od nula sati u drugom tjednu. Sveukupno, rezervacije i dodjele usklađene su, ali se razlikuju od jednog do drugog tjedna.

Kada pogledate vrijeme na višim razinama, ćelije na kartici **Usklađivanje** imaju pokazatelj koji će vas obavijestiti da postoje razlike na nižim razinama. Dvostrukim klikom na ćeliju za povećavanje prikaza razlike. Zatim desnom tipkom miša možete pritisnuti gumb kako biste smanjili prikaz. Odabirom resursa i zatim odabirom kontrole **Sljedeća razlika** na alatnoj traci rešetke možete ići na sljedeću razliku između rezervacija i dodjela za taj resurs. Kako biste se vratili natrag odaberite mogućnost **Prethodna razlika**. Možete i isključiti pokazatelj razlike i ponašanje navigacije u odjeljku **Postavke.**

Ako imate dodjele zadataka za resurs, ali bez rezervacija, na obrascu **Projekti**, na kartici **Usklađivanje**, odaberite manjak rezervacija, a zatim odaberite **Produlji rezervaciju**. Prikazat će se dijaloški okvir **Produlji rezervaciju** produljivanje rezervacije i rezervacija koju je potrebna za rješavanje manjka resursa. Dijaloški okvir prikazuje i postojeće rezervacije resursa diljem projekata ili drugih entiteta koji se mogu planirati. Ako odaberete **U redu** da biste izradili rezervaciju za resurs, bez obzira na dostupnost tog resursa, može doći do prebukiranosti.

Upravitelj projekta ili upravitelj resursa zatim može upotrijebiti ploču s rasporedom kako bi upravljao svim situacijama u kojima resurs ima prevelik broj rezervacija izvan svog kapaciteta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]