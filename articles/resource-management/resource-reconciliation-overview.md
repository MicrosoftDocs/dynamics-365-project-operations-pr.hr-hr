---
title: Pregled usklađivanja resursa
description: U ovoj se temi nalaze informacije o osiguravanju usklađenosti rezervacija i dodjela resursa za projekte.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 574afac3bf5d1f6e5e13d8c61aa1ace6188f4008
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125709"
---
# <a name="resource-reconciliation-overview"></a>Pregled usklađivanja resursa

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Za članove tima rezervacije i dodjele slobodno se uparuju. Drugim riječima, resursi mogu imati dodjele, ali ne i rezervacije ili pak mogu imati rezervacije, ali ne i dodjele. U idealnom slučaju rezervacije i dodjele trebaju biti usklađene, tako da resursi imaju potvrđeni kapacitet za izvođenje dodjela zadataka. Međutim, rezervacije se mogu temeljiti na dostupnosti, a vremenski rasporedi zadataka mogu se promijeniti tijekom nastavka projekta. Stoga slobodno uparivanje rezervacija i dodjela pruža fleksibilnost.

Kartica **Usklađivanje** na obrascu **Projekt** upraviteljima projekata omogućuje usklađivanje rezervacija članova tima i njihovih zadataka za projektne timove.

Kartica **Usklađivanje** također prikazuje rezervacije i dodjele na razini dodjele pojedinačnog zadatka za svakog člana tima. Sati se prikazuju u ćelijama koje predstavljaju vremensko razdoblje od mjeseci do dana.

Kartica također prikazuje ukupni neto iznos za projekt, zajedno sa stupcem **Ukupno**.

Za svaki resurs kartica izračunava razliku između rezervacija člana tima i skupnu vrijednost dodjela zadataka člana tima. Ta bi razlika idealno trebala iznositi 0 (nula). Drugim riječima, ne bi trebalo biti razlike između rezervacija i dodjela. Razlike su obojene i zasjenjene kako bi privukle pozornost na dva uvjeta:

- **Nedostatak rezervacija** – nedostatak rezervacija događa se kada resurs ima više dodjela nego rezervacija. Budući da taj kapacitet nije rezerviran, upravitelj projekta možda će htjeti ispraviti taj uvjet produljivanjem rezervacija resursa kako bi se pokrio manjak.
- **Previše rezervacija** – previše se rezervacija pojavljuje kada je resurs rezerviran za projekt, ali nije dodijeljen zadacima. Taj uvjet može biti prihvatljiv u slučajevima kada je resurs rezerviran za projekt prije dodjele zadataka. Međutim, u drugim slučajevima resurs nije planiran za dodjelu zadacima. U tim slučajevima upravitelj projekta trebao bi razmotriti otkazivanje rezervacija resursa, tako da se kapacitet može koristiti za drugi projekt.

U nekim slučajevima, kada pregledate vrijeme na razini koja je viša od dnevne (na primjer, razina mjeseca), možda ćete vidjeti neto razliku u iznosu nula za resurs (drugim riječima, rezervacije = dodjele). Međutim, ako pogledate vrijeme na razini tjedna, možda ćete vidjeti da postoje dodjele od nula sati i rezervacije od 40 sati u prvom tjednu, no dodjele od 40 sati i rezervacije od nula sati u drugom tjednu. Sveukupno, rezervacije i dodjele usklađene su, ali se razlikuju od jednog do drugog tjedna.

Kada pogledate vrijeme na višim razinama, ćelije na kartici **Usklađivanje** imaju pokazatelj koji će vas obavijestiti da postoje razlike na nižim razinama. Dvostrukim klikom na ćeliju možete povećati prikaz razlike. Zatim desnom tipkom miša možete pritisnuti gumb da biste smanjili prikaz. Odabirom resursa i korištenjem kontrole **Sljedeća razlika** na alatnoj traci rešetke možete ići na sljedeću razliku između rezervacija i dodjela za taj resurs. Zatim možete koristiti kontrolu **Prethodna razlika** da biste se vratili. Možete i isključiti pokazatelj razlike i ponašanje navigacije u odjeljku **Postavke.**


Ako imate dodjele zadataka za resurs, ali bez rezervacija, na stranici **Projekti** na kartici **Usklađivanje** odaberite manjak rezervacija, a zatim odaberite **Produlji rezervaciju**. Prikazat će se dijaloški okvir **Produlji rezervaciju** produljivanje rezervacije i rezervacija koju je potrebna za rješavanje manjka resursa. Prikazuju se i postojeće rezervacije resursa u svim projektima ili drugim entitetima koji se mogu zakazati. Ako odaberete **U redu** da biste izradili rezervaciju za resurs, bez obzira na dostupnost tog resursa, može doći do prebukiranosti.

Upravitelj projekta ili upravitelj resursa zatim može koristiti ploču s rasporedom kako bi upravljao svim situacijama u kojima je resurs prebukiran izvan svog kapaciteta.

