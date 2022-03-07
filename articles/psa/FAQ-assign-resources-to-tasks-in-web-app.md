---
title: Kako mogu resurs koji se može rezervirati dodijeliti zadatku u web-aplikaciji
description: Pregled načina na koje možete dodijeliti resurse koji se mogu rezervirati.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 25cf017c53d7db23e467b3b610e2990e56e95cb56bdf9820e427dfeeeb979637
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987697"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Kako da zadatku dodijelim resurs koji se može rezervirati u web-aplikaciji (aplikaciji Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Postoje dva načina za dodjelu resursa zadatku u aplikaciji Project Service. Možete rezervirati resurs kao član tima, a zatim ga dodijeliti zadatku. Ili možete stvoriti generičkog člana tima putem dodjele uloge u zadacima, generirati tim, a zatim ispuniti dodatne preduvjete s imenovanim resursom.

Imajte na umu da ako zadatku želite dodijeliti resurs koji se može rezervirati, član tima tog resursa mora imati dovoljno dostupnih rezervacija. Status rezervacije mora biti Vrsta izvršavanja: fiksna rezervacija i Status izvršen. Ako nema dovoljno rezervacija za određeni resurs, aplikacija Project Service uklanja dodjelu i prikazuje sljedeću poruku o pogrešci:

*Nije moguće dodijeliti resurs zadatku - Sljedeći resurs/i nema/ju dovoljno rezerviranih sati za projekat*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Rezervirajte resurs kao član tima, a zatim ga dodijelite zadatku

Pomoću ove metode možete dodati resurs projektnom timu, a zatim dodijeliti zadatake tom resursu u projektnom rasporedu. Evo kako da to uradite:
1.  Na rešetki član tima dodajte novog člana tima odabirom **Novo**.
2.  Na ekranu za brzo stvaranje člana tima izaberite ime za resurs koji je moguće rezervirati i postavite ulogu.
3.  Odaberite **od** i **do** datume.

    > [!div class="mx-imgBorder"] 
    > ![Snimka zaslona dodavanja člana tima.](media/FAQ-Resources-to-Tasks2-1.png "Snimka zaslona dodavanja člana tima")
 
4.  Izaberite jednu od sljedećih metoda dodjeljivanja za rezervaciju resursa:
    - **Puni kapacitet** rezervira puni kapacitet resursa za odabrane datume od i do.
    - **Postotni kapacitet** rezervira određeni postotak kapaciteta resursa za odabrane datume od i do.
    - **Ravnomjerna raspodjela po satima** rezervira resurs na određeni broj sati, ravnomjerno ga raspoređujući svakog dana za vrijeme određenog razdoblja.
    - **Punjenje sprijeda po satima** rezervira resurs na određeni broj sati, umečući sprijeda sate svakog dana za vrijeme određenog razdoblja.

    Nemojte odabrati **Ništa** jer bi se time resurs dodao timu, ali ne bi se stvarile nikakve rezervacije koje troše kapacitet resursa.
5.  Odaberite **Spremi**.

    Imajte na umu da sati rezervacije moraju biti dovoljni da pokriju sate rada i datumske raspone za zadatke kojima dodijelite taj resurs. Ako oni nisu usklađeni, nećete moći dodijeliti resurs tom zadatku.

6.  U strukturnoj analizi rada (SAR-u) za taj zadatak, kliknite na padajući izbornik ćelije resursa. Zatim: 

    1. Odaberite **Dodaj**.
    2. Odaberite padajući izbornik pod **Resursi** i odaberite člana tima kojeg ste dodali gore.
    3. Odaberite **U redu**. Taj član tima sada je dodijeljen zadatku.

    > [!div class="mx-imgBorder"] 
    > ![Snimka zaslona dodavanja resursa sa SAR-om.](media/FAQ-Resources-to-Tasks2-2.png "Snimka zaslona dodavanja resursa sa SAR-om")
 
Na rešetki član tima pod Dodijeljeni sati vidjet ćete agregat dodijeljenih sati resursa. Bit će jednak ili manji od rezerviranih sati resursa. 

> [!div class="mx-imgBorder"] 
> ![Snimka zaslona dodijeljenih sati za resurs.](media/FAQ-Resources-to-Tasks2-3.png "Snimka zaslona dodijeljenih sati za resurs")
 
Ako zadatak kojeg pokušavate dodijeliti resursu počinje nakon datuma završetka rezervacija resursa, taj resurs se neće prikazati u padajućem izborniku.

Imajte na umu da možete dodijeliti resurs većem broju sati od njegovih rezerviranih sati ako ima nešto preostalog nedodijeljenog kapaciteta. U tom slučaju resurs će biti samo djelomično dodijeljen do njihovih rezervacija. Dodavanjem stupca Sati bez djelatnika strukturnoj analizi rada možete vidjeti te preostale nedodijeljene sate zadatka.

Ako su resursi dodijeljeni njihovim rezerviranim satima (njihovi rezervirani sati su jednaki njihovim dodijeljenim satima), vidjet ćete sljedeću poruku o pogrešci kada im pokušate dodijeliti još zadataka:

*Nije moguće dodijeliti resurs zadatku - Sljedeći resurs/i nema/ju dovoljno rezerviranih sati za projekat.*

Uz to, član tima koji je zadani upravitelj projekta i koji je dodan timu kada stvorite projekat dodaje se bez ikakvih rezervacija i ne može biti dodijeljen nijednom zadatku. On se neće pojaviti u padajućem izborniku resursa za zadatke.

Ako želite dodijeliti ovaj resurs, morate ukloniti tog člana iz tima i zatim ga ponovno dodati pomoću bilo koje metode dodjele osim metode Ništa. Taj član je dodan timu pri stvaranju projekta da bi projekat imao barem jednog zadanog projektnog odobravatelja.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Stvorite generičkog člana tima putem dodjele uloge za zadatke

Zahvaljujući ovoj metodi svaki resurs ima dovoljno rezervacija za zadatke. Prvo ćete generiranjem tima nakon dodjele uloga zadacima stvoriti rezervirano mjesto ili generički resurs koji opisuje karakteristike imenovanog resursa za kojeg u konačnici želite da radi na zadacima. Evo kako da to uradite:

1. Odaberite zadatak u strukturnoj analizi rada.
2. Odaberite padajuću ikonu **Dodijeljena uloga** u ćeliji resursa.
3. Odaberite padajući izbornik **Uloga**, a zatim odaberite ulogu za generičkog resursa.
4. Odaberite **U redu**.

    > [!div class="mx-imgBorder"] 
    > ![Snimka zaslona uporabe SAR-a za dodavanja resursa.](media/FAQ-Resources-to-Tasks2-4.png "Snimka zaslona uporabe SAR-a za dodavanja resursa")
 
Nakon dovršetka dodjele uloga zadacima u SAR-u, odaberite **Generiranje projektnog tima**. Aplikacija Project Service stvara najmanji broj generičkih članova tima na temelju uloga, organizacijskih jedinica za resurse i projektnog kalendara agregirajući dodjele zadataka.

> [!div class="mx-imgBorder"] 
> ![Snimka zaslona generiranja projektnog tima.](media/FAQ-Resources-to-Tasks2-5.png "Snimka zaslona generiranja projektnog tima")
 
Na rešetki član tima vidjet ćete resurse generičkog tipa s nazivom uloge i položaja. Ako su dva resursa potrebna za određenu ulogu da dovrši rad, značajka Generiranje tima će stvoriti dva člana tima i koristit će naziv položaja da ih razlikuje.

> [!div class="mx-imgBorder"] 
> ![Snimka zaslona dodavanja dva generička resursa.](media/FAQ-Resources-to-Tasks2-6.png "Snimka zaslona dodavanja dva generička resursa")
 
Možete otvoriti dodatni preduvjet resursa za generičkog člana tima odabirom veze pod stavkom Preduvjet resursa.

> [!div class="mx-imgBorder"] 
> ![Snimka zaslona otvaranja dodatnog preduvjeta resursa.](media/FAQ-Resources-to-Tasks2-7.png "Snimka zaslona otvaranja dodatnog preduvjeta resursa")

Odaberite **Rezerviraj** za generički resurs, a zatim možete koristiti ploču s rasporedom za pronalaženje i rezerviranje pravog resursa. Možete poslati i zahtjev za ispunjenje od strane upravitelja resursa odabirom **Pošalji zahtjev**.

Kada se generički resurs ispuni imenovanim resursom, tada se uklanja iz tima i dodjele zadataka generičkog resursa se dodjeljuju imenovanom resursu koji je ispunio preduvjet generičkog resursa za resursom.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]