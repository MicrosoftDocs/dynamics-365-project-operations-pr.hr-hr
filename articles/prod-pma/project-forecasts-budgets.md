---
title: Predviđanja i proračuni projekata
description: Microsoft Dynamics 365 Finance omogućuje predviđanja i proračune projekata za upravljanje projektima i nadzor nad njima.
author: Yowelle
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f99c00effbb0678f1f55e5068a7128cbfb86f5ce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073501"
---
# <a name="project-forecasts-and-budgets"></a>Predviđanja i proračuni projekata

[!include [banner](../includes/banner.md)]

Dva su načina za upravljanje projektima i nadzor nad njima: predviđanja i proračuni projekata. 

Predviđanje za projekt upotrebljavajte ako vaša tvrtka ili ustanova ima operativnu perspektivu i ako je usredotočena na prihode i troškove koji proizlaze iz određenih transakcija. Ako se vaša tvrtka ili ustanova više usredotočuje na financijske iznose, upotrijebite izradu proračuna za projekt. 

I predviđanja i proračuni projekata upotrebljavaju modele predviđanja kako bi zadržali predviđene iznose transakcija. 

Svaki način ima svoje prednosti. Prije nego što odaberete način za svoju tvrtku ili ustanovu, trebali biste razmotriti sljedeće točke.

|   Način dodjele       |           Predviđanje projekta            |        Izrada proračuna za projekt                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Dodjela razdoblja**     | Ne možete izričito dodijeliti transakcije tijekom fiskalnog razdoblja. Umjesto toga, predviđanje i nadzor predviđanja temelje se na životnom vijeku projekta. Budući da se predviđanja temelje na određenom datumu, morate prosuditi razdoblje od datuma. | Ne možete izričito dodijeliti transakcije tijekom cijelog projekta ili fiskalnog razdoblja. Ako dodjeljujete tijekom razdoblja, neupotrijebljene iznose možete prenijeti u sljedeće fiskalno razdoblje. |
| **Pregled transakcija**  | Transakcije možete pregledavati u obrascima za predviđanje, gdje vidite predviđanja za cijelu tvrtku i za sve projekte, bez obzira na hijerarhiju. Kako biste se usredotočili na određeni projekt, morate filtrirati podatke.                                       | Možete pregledati proračunske transakcije za jednu hijerarhiju projekta. Stoga možete pogledati pojedinosti transakcije za nadređeni projekt ili njegove potprojekte.                 |
| **Varijable transakcije** | Kada unosite predviđene transakcije, možete upotrebljavati svaki postojeći atribut za stvarnu transakciju. To omogućuje više pojedinosti u predviđanju. Na primjer, možete unijeti pojedinosti za količine, radnike, stavke ili svojstva retka.         | Kada unesete pojedinosti proračuna, možete upotrijebiti samo iznose, kategorije i aktivnosti.                    |
| **Sigurnost**              | Predviđanje se temelji na transakcijama koje unesete u obrasce za predviđanje i ne uključuje mehanizam nadzora procesa. Svaki radnik koji ima dozvolu za obrazac za predviđanje može revidirati podatke bez odobrenja.                                        | Pri izradi proračuna upotrebljava se sustav tijeka posla, koji omogućuje upravljanje promjenama i dozvoljava vam zadržavanje povijesti promjena.         |
| **Vrste unosa**           | Unosi predviđenih transakcija temelje se na broju jedinica te na trošku i cijenama prodajnih jedinica.  | Pojedinosti proračuna temelje se na iznosima koji se dijele između troškova i prihoda.                                          |
| **Modeli predviđanja**       | Budući da svako predviđanje mora biti povezano s modelom, možete stvoriti više modela predviđanja i također postaviti podmodele.           | Izrada proračuna za projekt ograničava modele predviđanja koji se upotrebljavaju za izradu proračuna. Manji broj modela predviđanja može pomoći pri povećanju dosljednosti u projekcijama.                           |
| **Prekoračenje troška**         | Unos transakcija koje će dovesti do prekoračenja troškova možete dozvoliti ili zabraniti.   | Izrada proračuna za projekt pruža korisnicima dodatne mogućnosti nadzora. Možete dozvoliti upozorenja i prekoračenja.                    |
| **Kontrola**               | Nadzor predviđanja vrši se smanjenjem predviđanja. Stvarni iznosi oduzimaju se od predviđenih salda transakcija bez ikakvog traga nadzora. To može otežati praćenje mjesta događanja stvarnih transakcija.                   | U nadzoru proračuna projekta, stvarni se iznosi oduzimaju od iznosa u preostalom proračunu. To omogućuje jasniji trag nadzora.                                   |

## <a name="project-forecasts"></a>Predviđanja projekata
Kada upotrebljavate predviđanje projekta, možete unijeti predviđene transakcije u obrasce za predviđanje za svaku vrstu transakcije. Svaki atribut koji je dostupan za stvarnu transakciju može se upotrijebiti za predviđenu transakciju – na primjer, profitabilnost retka, atributi retka, radnici ili opisi. Također možete predvidjeti nakon koliko ćete vremena od nastanka troška isti fakturirati klijentu. 

Transakcije predviđanja projekata temelje se na jedinicama i iznosima. 

Svako predviđanje projekta morate povezati s modelom predviđanja. Kada unesete predviđenu transakciju, automatski se predlaže model predviđanja. Model predviđanja djeluje kao spremnik za predviđene transakcije. 

Modele predviđanja možete naznačiti kao podmodele modela. To vam omogućuje predviđanje po regiji, vremenskom razdoblju ili odjelu. Predviđene transakcije možete kopirati u model kako biste stvorili novi model, a transakcije možete također prenijeti u glavnu knjigu. Budući da postoji odnos jedan-na-jedan između predviđanja i modela, svaki model predviđanja čini zasebni proračun za projekt. 

Modeli predviđanja mogu upotrebljavati smanjenje predviđanja kao nadzorni mehanizam za projekte. U smanjenju predviđanja, stvarne transakcije smanjuju salda predviđenih transakcija. Međutim, budući da se smanjenje predviđanja primjenjuje na najviši projekt u hijerarhiji, ono daje ograničen prikaz promjena u predviđanju. Na primjer, ako je radnik povezan s potprojektom, stvarne transakcije za radnika knjiže se u nadređeni projekt. To može otežati praćenje promjena jer ne možete lako odrediti koja je transakcija u kojem potprojektu uzrokovala smanjenje predviđenog iznosa. Stoga je dobra ideja stvoriti kopiju modela predviđanja za smanjenje predviđanja koja će se upotrebljavati. Tada možete upotrebljavati izvješća za prikaz onoga što je izvorno predviđeno. 

Možete revidirati, kopirati, izbrisati ili prenijeti predviđanja projekata u proračun glavne knjige. Međutim, ne postoji nadzor procesa. Svaki radnik koji ima dozvolu za obrazac za predviđanje može izvršiti izmjene podataka bez provjere.

-   **Revidiraj** – Možete revidirati predviđenu transakciju u istim obrascima u kojima su izvršeni izvorni unosi.
-   **Kopiraj ili izbriši** – Kada kopirate predviđene transakcije, kopirate retke transakcija iz jednog modela predviđanja u drugi. Kada izbrišete predviđanje, brišete predviđene transakcije iz modela predviđanja. Kako biste ograničili predviđene transakcije koje se kopiraju ili brišu, odaberite određene vrste transakcija i datume. To vam omogućuje kopiranje ili brisanje samo određenih dijelova predviđanja.
-   **Prijenos** – Kada prenosite predviđanje projekta u proračun glavne knjige, prenosite predviđene transakcije modela predviđanja u proračun glavne knjige. Sve transakcije prethodno prenesene u proračun glavne knjige, na koji prenosite predviđanje projekta, možete prebrisati.

## <a name="project-budgets"></a>Proračuni za projekt
Izrada proračuna za projekt jednostavnija je metoda od predviđanja, iako se integrira s modelima predviđanja. Upotrebljava jedan obrazac unosa za pojedinosti i revizije izvornog proračuna te omogućuje predviđanja koja se temelje samo na iznosu, kategoriji ili aktivnosti. 

Pri izradi proračuna za projekt, svi izvorni proračuni i revizije moraju se poslati na odobrenje tijeku rada projekta. Tijekovi rada omogućuju vam povećani nadzor nad postupkom i stvaraju zapis povijesti promjena. 

Izrada proračuna za projekt nalikuje izradi proračuna za glavnu knjigu, ali se brže i jednostavnije postavlja. Mnoge mogućnosti u proračunu glavne knjige, poput nizova brojeva ili valute, ne moraju se zasebno postavljati za projekte.

Proračuni projekata automatski se povezuju s dva modela predviđanja, jednim za izvorni proračun i drugim za preostali proračun. Stoga izvješća koja se temelje na modelima predviđanja mogu upotrebljavati proračunske podatke. Kada je izrađen proračun projekta, sustav stvara predviđene transakcije na temelju povezanih modela, koji se upotrebljavaju u svrhu izvješćivanja i nadzora.

## <a name="forecast-models"></a>Modeli predviđanja
Modeli predviđanja imaju jednoslojnu hijerarhiju. To znači da jedno predviđanje projekta mora biti povezano s jednim modelom predviđanja.

Ako upotrebljavate predviđanje projekata, modele možete prepoznati kao podmodele. Tada možete stvoriti predviđanja po odjelima, vremenskim razdobljima ili regijama. Na primjer, možete stvoriti model predviđanja za godinu dana, a zatim stvoriti podmodele za regionalna predviđanja za sjeveroistok, jugoistok, sjeverozapad i jugozapad koje šalju regionalni voditelji. Odabirom različitih mogućnosti u dostupnim izvješćima možete pregledati podatke prema ukupnom predviđanju ili prema podmodelu.





[!INCLUDE[footer-include](../includes/footer-banner.md)]