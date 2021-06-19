---
title: Usklađivanje rezervacija i dodjela
description: Ova tema pruža informacije o stvarnim podacima.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 73cbc89ae4350cbd568f1bb978825ff53da07afb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008887"
---
# <a name="reconcile-bookings-and-assignments"></a>Usklađivanje rezervacija i dodjela

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Rezervacije projekta člana projeknog tima i dodjele projektnih zadataka slobodno se uparuju. Stoga resurs može imati dodjele zadataka koje ne odgovaraju rezervacijama i rezervacije koje ne odgovaraju dodjelama zadataka. U idealnom slučaju rezervacije i dodjele projekta usklađene su, tako da resursi imaju potvrđeni kapacitet za izvođenje dodjela zadataka. Međutim, u stvarnosti se rezervacije mogu pojavljivati na temelju dostupnosti, a vremenski rasporedi zadataka mogu se mijenjati tijekom životnog ciklusa projekta. Stoga slobodno uparivanje omogućuje fleksibilnost.

Zbog slobodnog uparivanja rezervacija i dodjela zadataka projekta kartica **Usklađivanje** uključena je u entitet projekta. Ta kartica upraviteljima projekta omogućuje usklađivanje rezervacija članova tima i njihovih dodjela za projektni tim.

Za svaki imenovani tim kartica **Usklađivanje** prikazuje rezervacije i dodjele na razini dodjele pojedinačnog zadatka. Prikazuje sate u ćelijama koje predstavljaju razdoblja od mjeseci do dana.

U polju **Vremensko mjerilo** možete odabrati **Mjesec**, **Tjedan** ili **Dan**. Prema zadanim postavkama odabrana je mogućnost **Tjedan**. Međutim, zadanu vrijednost možete promijeniti odabirom gumba **Postavke**. Kada se otvori kartica **Usklađivanje**, prikazuje se trenutačni datum, no možete koristiti kontrolu kalendara za pomicanje naprijed ili natrag u vremenu. Ako projekt ima datum početka u budućnosti, kartica prikazuje taj datum prilikom otvaranja. Kontrola kalendara također sadrži mogućnosti koje vam omogućuju pomicanje datuma početka i završetka projekta.

Možete koristiti kontrole proširivača za svaki resurs da bi se prikazale pojedinosti o rezervacijama tog resursa. Možete također proširiti dodjele svakog resursa na razinu pojedinačnog zadatka.

Dno kartice **Usklađivanje** prikazuje ukupni neto iznos za projekt, a kartica sadrži i stupac ukupne vrijednosti. Za svaki resurs kartica uzima u obzir razliku između rezervacija člana projektnog tima i skupne vrijednosti dodjela zadataka tog člana tima. Ta bi razlika idealno trebala iznositi 0 (nula). Drugim riječima, ne bi trebalo biti razlike između broja rezervacija resursa i dodjela zadataka. Sve razlike označene su bojom i sjenčanjem kako bi se pozvala dva uvjeta:

- **Nedostatak rezervacija** – nedostatak rezervacija pojavljuje se kada resurs ima više dodjela nego rezervacija. Budući da taj kapacitet nije rezerviran, upravitelj projekta to stanje može ispraviti produljivanjem rezervacija resursa kako bi se pokrio nedostatak.
- **Previše rezervacija** – previše se rezervacija pojavljuje kada je resurs rezerviran za projekt, ali nije dodijeljen zadacima. To stanje može biti prihvatljivo ako je, primjerice, resurs bio rezerviran prije dodjele zadatka. Međutim, u drugim slučajevima resurs možda nije planiran za dodjelu. U tim slučajevima upravitelj projekta trebao bi razmotriti otkazivanje rezervacija resursa, tako da se kapacitet može koristiti za drugi projekt.

> [!NOTE]
> Legenda za navedene uvjete može biti skrivena kako bi ostalo više prostora za rešetku. U tom slučaju legendu možete učiniti vidljivom tako da odaberete gumb **Postavke**.

U nekim slučajevima, kada je polje **Vremensko mjerilo** postavljeno na razinu koja je viša od razine **Dan**, razlike se mogu izračunati kao 0 (nula). Na primjer, na razini **Mjesec** neto razlika za resurs može biti 0 (nula) kako bi se naznačilo da je broj ukupnih rezervacija jednak broju dodjela. Međutim, ako pogledate vrijeme na razini **Tjedan**, možda ćete vidjeti da postoje dodjele od 0 (nula) sati i rezervacije od 40 sati u prvom tjednu mjeseca te dodjele od 40 sati i rezervacije od 0 (nula) sati u drugom tjednu mjeseca. Iako je broj ukupnih rezervacija i dodjela za mjesec jednak, razlikuje se po tjednu.

Kada pogledate vrijeme na višim razinama, na kartici **Usklađivanje** prikazuje se pokazatelj ćelija koji će vas obavijestiti da postoje razlike na nižim razinama. Na primjer, na sljedećoj ilustraciji pokazatelj ćelije prikazuje se u ćeliji za mjesec listopad 2018. za resurs naziva Klara Čeh. Stoga možete vidjeti da, iako je broj ukupnih rezervacija i dodjela za resurs jednak kada se zbroji na razini **Mjesec**, ti se brojevi ne podudaraju na nižim razinama.

![Neusklađene rezervacije i zadaci na mjesečnoj razini](media/reconcile-assignments-01.JPG)

Dvokliknite ćeliju da biste smanjili prikaz na sljedeću nižu razinu i pogledali razliku. Na primjer, ako dvokliknete razliku za listopad 2018. za Klaru Čeh, pretražujete kroz razine naniže na razinu **Tjedan**. Zatim možete vidjeti da resurs ima rezervacije od 16 sati, ali nema dodjela u prva dva tjedna listopada i 16 sati dodjela, ali nema rezervacija u trećem tjednu listopada.

![Neusklađene rezervacije i zadaci na tjednoj razini](media/reconcile-assignments-02.JPG)

Možete desnom tipkom miša kliknuti ćeliju da biste smanjili prikaz sljedeće više razine. Pokazatelj ćelije možete isključiti i odabirom gumba **Postavke**. 

Također možete koristiti gumbe **Prethodno** i **Sljedeće** iznad rešetke da biste se pomicali razlikama u projektu. Da biste koristili te gumbe, najprije morate odabrati resurs. Odaberite **Sljedeće** da biste otvorili sljedeću razliku između rezervacija i dodjela za taj resurs. Da biste otvorili prethodnu razliku, odaberite **Prethodno**.

U situacijama kada imate dodjele zadataka za resurs bez rezervacija, možete odabrati nedostatak rezervacija, a zatim odabrati **Proširi rezervaciju**. Zatim možete vidjeti rezervaciju potrebnu za rješavanje nedostatka resursa. Možete također pregledati rezervacije resursa u trenutačnom projektu i drugim projektima. Odaberite **U redu** da biste stvorili rezervaciju za resurs bez obzira na trenutačnu dostupnost. Upravitelj projekta ili upravitelj resursa zatim može koristiti ploču s rasporedom kako bi upravljao situacijama u kojima je resurs prebukiran izvan kapaciteta jer su rezervacije produljene.

## <a name="managing-with-time-zones"></a>Upravljanje vremenskim zonama
Dva su osnovna preduvjeta koja moraju biti zadovoljena kako bi se pri uporabi značajke Produlji rezervaciju osigurali točni i predvidljivi rezultati:  

- Korisnik mora konfigurirati vremensku zonu svojeg uređaja tako da bude podudarna s vremenskom zonom određenom u postavkama personalizacije vašeg sustava.
 
  ![Postavke vremenske zone u programu Windows 10](media/reconcile-assignments-03.png)

  ![Postavke vremenske zone u personaliziranim postavkama](media/reconcile-assignments-04.png)
 
- Resurs koji se može rezervirati mora imati najmanje jednu minutu radnog vremena koje se preklapa s konturama koje se upotrebljavaju za određivanje traženog produljenja. Primjerice, naredni primjer prikazuje resurse za pregled s radnim vremenom između 9:00 i 19:00. 

  ![Usporedba kontura resursa](media/reconcile-assignments-05.png)

Tablice u nastavku prikazuju:

- Predložak kalendara projekta.
- Resurs A: Ovaj resurs ima isti kalendar i nalazi se u istoj vremenskoj zoni kao i projekt. Vrijeme početka rezervacija bit će 9:00.
- Resursi B: Ovaj se resurs ne nalazi u istoj vremenskoj zoni s projektom i zato počinje u 7:00 u njegovoj vremenskoj zoni. Međutim, rezervacije će započeti u 9:00, jer je to najranije vrijeme početka konture dodjele.
- Resursi C i D: Resursi se također nalaze u različitim vremenskim zonama, i međusobno i od projekta, a njihove rezervacije ne započinju prije njihovih odgovarajućih dostupnih vremena početka.

|Entitet  |Kalendar  |
|-|-|
|Predložak kalendara projekta   | ![kalendar projekta](media/reconcile-assignments-06.png) |
|Resurs A  | ![Kalendar resursa A](media/reconcile-assignments-06.png) |
|Resurs B  |  ![Kalendar resursa B](media/reconcile-assignments-07.png) |
|Resurs C  |  ![Kalendar resursa C](media/reconcile-assignments-08.png) |
|Resurs D  | ![Kalendar resursa D](media/reconcile-assignments-09.png)  |
 
Kada se pomaknete do prikaza usklađivanja, prikazat će se dodjele resursa i povezani nedostaci rezervacija.
 ![Prikaz usklađivanja prije produljena](media/reconcile-assignments-10.png)

Nakon što se funkcionalnost značajke Produlji rezervaciju izvrši na svakom resursu, rezervacije se uspješno produljuju za svaki resurs. To je zato što se radno vrijeme svakog resursa preklopilo s konturama nedostatka.
 ![Prikaz usklađivanja nakon produljena rezervacije](media/reconcile-assignments-11.png) 

Međutim, pobliži uvid u pojedinosti rezervacija pokazao je razlike u vremenu početka rezervacija. Rezervacije neće započeti prije vremena početka konture dodjele i dostupnog vremena početka resursa.
 ![Nove rezervacije resursa u ploči s rasporedom](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]