---
title: Pregledavanje predloženih resursa
description: Ova tema pruža informacije o tome kako predložiti resurse projekta.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073355"
---
# <a name="review-proposed-resources"></a>Pregledavanje predloženih resursa

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Upravitelji resursa mogu predložiti resurs voditelju projekta pomoću zahtjeva za resurs.

1. Odaberite **Pronađi resurse** u rešetki zahtjeva ili u samom zahtjevu.
2. Na stranici **Pomoćnik za raspored** odaberite resurs, a zatim u oknu **Stvaranje rezervacije resursa** u polju **Status rezervacije** odaberite **Rezerviraj**.

Pojavljuju se sljedeća ažuriranja statusa:

- Na stranici **Pomoćnik za raspored** pokazatelji statusa ažuriraju se kako bi bilo jasno da je rezervacija predložena, a ne fiksno rezervirana.
- Na zahtjevu za resurs status se mijenja u **Potreban pregled**.
- Na kartici **Tim** projekta vrijednost **Status zahtjeva** člana generičkog tima mijenja se u **Potreban pregled**.

Voditelj projekta može prihvatiti ili odbaciti prijedlog.

Kada upravitelji resursa obrađuju zahtjeve za resurs, mogu upotrijebiti neki od sljedećih pristupa:

- Predlaganje više resursa kako bi se zadovoljila potražnja ako nije dostupan jedan resurs koji bi odradio potrebne sate. Predloženi sati zatim se dijele na više resursa koji mogu odraditi potrebne sate. U ovom scenariju sati se ne smiju preklapati.
- Predložite manje resursa nego što je potrebno. U ovom scenariju predloženi kapacitet resursa je manji od potrebnih sati koje je odredio podnositelj zahtjeva. Zbog toga se, kad podnositelj zahtjeva prihvati predložene resurse, stvara neispunjeni zahtjev za resurs koji pokriva preostalu potražnju.
- Rezerviranje više resursa kako bi se zadovoljila potražnja ako nije dostupan jedan resurs koji bi dovršio posao.
- Rezervirajte manje resursa nego što je potrebno. U ovom scenariju rezerviranih je sati manje od potrebnih sati. Sustav vas upućuje da predložite resurse umjesto rezervacija, tako da podnositelj zahtjeva može provjeriti valjanost i pratiti preostalu potražnju.

## <a name="billable-utilization"></a>Naplativa upotreba

Resursi mogu imati ciljanu naplativu upotrebu. Ova ciljana upotreba definira se kao atribut u zadanoj ulozi resursa ili je postavljena na zapisu pojedinačnog resursa koji se može rezervirati. Izračuni upotrebe temelje se na stvarnim satima koje su resursi prijavili pomoću odobrenih vremenskih unosa.

Formule u nastavku služe za izračun upotrebe:

- Naplativa upotreba = naplativi stvarni sati ÷ kapacitet resursa
- Nenaplativa upotreba = stvarno vrijeme s ID-om vrste naplate = nenaplativo, besplatno ili nije dostupno ÷ kapacitet resursa
- Interno = stvarno vrijeme bez prodajnog ugovora ÷ kapacitet resursa
- Kapacitet resursa = radno vrijeme resursa – izvan ureda – neradni dani

Prikaz **Upotreba resursa** možete pronaći u oknu **Resursi**.

Svaka ćelija u rešetki predstavlja postotak naplative upotrebe resursa u razdoblju, kao što je dan, tjedan ili mjesec. Formule u nastavku služe za označavanje ćelija bojom:

- **Zelena:** naplativa upotreba \>= ciljna upotreba resursa
- **Žuta:** ciljna upotreba – 20 \<= naplativa upotreba \< ciljna upotreba
- **Crvena:** naplativa upotreba \< ciljna upotreba – 20

Budući da se prikaz **Upotreba resursa** temelji na ploči s rasporedom, možete filtrirati rezultate pomoću mogućnosti filtriranja na ploči s rasporedom.

U rešetki je potrebno postaviti ciljnu upotrebu za svaku ulogu ili pojedinačni resurs. Da biste to učinili, otvorite **Resursi** \> **Uloge resursa**.

Osim toga, svakom resursu koji se može rezervirati potrebno je dodijeliti zadanu ulogu. Otvorite **Resursi** \> **Resursi**. Na kartici **Project Service** provjerite je li definirana uloga resursa i je li polje **Zadano je** postavljeno na **Da**. Možete dodati dodatne uloge ako je polje **Zadano je = Ne**. Uloga u kojoj se koristi polje **Zadano je = Da** služi za procjenu upotrebe resursa u odnosu na cilj za tu ulogu.

Na kartici **Project Service** možete postaviti i pojedinačnu ciljnu upotrebu za resurs. Izračun upotrebe zatim upotrebljava ciljnu upotrebu da bi se procijenio cilj resursa, a ne cilj zadane uloge resursa.

Upotreba se prikazuje za resurs samo ako taj resurs ima odobreno naplativo vrijeme tijekom razdoblja koje je prikazano u rešetki.

## <a name="resource-availability"></a>dostupnost resursa

Ključno je da upravitelji resursa mogu pregledavati dostupnost resursa i ažurirati rezervacije. U nekim slučajevima ne postoji službena potražnja (zahtjev za resurs), ali upravitelj resursa mora odgovoriti na neplaniranu potražnju koja dolazi putem kanala kao što su e-pošta, telefonski poziv ili izravna poruka. Upravitelji resursa ažuriraju resurse i rezervacije na ploči s rasporedom.

Radno vrijeme resursa koristi se kao osnova za izračun dostupnosti resursa. Rezervacije resursa iskorištavaju kapacitet resursa.

Na ploči s rasporedom boje i sjenčanje označavaju rezervacije, dostupnost i prekomjerne rezervacije, kao i status rezervacija. Postavka u postavkama ploče s rasporedom omogućuje prikaz legende.

Ako se strelica udesno prikazuje pokraj pojedinačnog resursa koji se može rezervirati na ploči s rasporedom, resurs se može proširiti da bi se prikazale pojedinosti posla za koji je resurs rezerviran.

Budući da Dynamics 365 Project Operations upotrebljava modul Universal Resource Scheduling, ako imate instaliranu uslugu Dynamics 365 Field Service, možete pregledati pojedinosti o rezervacijama resursa za projekte, radne naloge i sve druge entitete na koje ste proširili planiranje.

Za prikaz dodatnih pojedinosti o pojedinačnom resursu desnom tipkom miša kliknite resurs za otvaranje kartice resursa.

