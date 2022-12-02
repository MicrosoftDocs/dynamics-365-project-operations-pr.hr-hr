---
title: Pregled usklađivanja resursa
description: U ovom članku nalaze se informacije koje će vam pomoći da osigurate usklađivanje rezervacija i zadataka resursa za projekte.
author: ruhercul
ms.date: 01/08/2021
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: eaad9187f08be810d730f5a8ca6411ecee85bbc4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926307"
---
# <a name="resource-reconciliation-overview"></a>Pregled usklađivanja resursa

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Za članove tima rezervacije i dodjele slobodno se uparuju. Drugim riječima, resursi mogu imati zadatke, a ne rezervacije ili pak mogu imati rezervacije, a ne zadatke. U idealnom slučaju rezervacije i dodjele trebaju biti usklađene, tako da resursi imaju potvrđeni kapacitet za izvođenje dodjela zadataka. Međutim, rezervacije se mogu temeljiti na dostupnosti, a vremenski rasporedi zadataka mogu se promijeniti tijekom nastavka projekta. Stoga slobodno uparivanje rezervacija i dodjela pruža fleksibilnost.

Kartica **Usklađivanje** na stranici **Projekti** omogućuje voditeljima projekata usklađivanje rezervacija članova tima s njihovim zadacima za projektne timove.

Kartica **Usklađivanje** prikazuje rezervacije i dodjele na razini dodjele pojedinačnog zadatka za svakog člana tima. Sati se prikazuju u ćelijama koje predstavljaju razdoblja u rasponu od mjeseci do dana. Kartica također prikazuje ukupni neto iznos za projekt, zajedno sa stupcem **Ukupno**.

Za svaki resurs kartica **Usklađivanje** izračunava razliku između rezervacija člana tima i skupne vrijednosti dodijeljenih zadataka članu tima. Ta bi razlika idealno trebala iznositi 0 (nula). Drugim riječima, ne bi trebalo biti razlike između rezervacija i dodjela. Razlike su obojene i zasjenjene kako bi privukle pozornost na dva uvjeta:

- **Nedostatak rezervacija** – nedostatak rezervacija događa se kada resurs ima više dodjela nego rezervacija. Budući da taj kapacitet nije rezerviran, upravitelj projekta možda će htjeti ispraviti taj uvjet produljivanjem rezervacija resursa kako bi se pokrio manjak.
- **Previše rezervacija** – previše se rezervacija pojavljuje kada je resurs rezerviran za projekt, ali nije dodijeljen zadacima. Taj uvjet može biti prihvatljiv u slučajevima kada je resurs rezerviran za projekt prije dodjele zadataka. Međutim, u drugim slučajevima, kada ne postoji plan dodjeljivanja resursa zadacima, voditelj projekta trebao bi razmotriti otkazivanje rezervacija resursa. Na taj se način kapacitet može upotrijebiti za drugi projekt.

U nekim slučajevima, kada pregledate vrijeme na razini koja je viša od dnevne (na primjer, razina mjeseca), možda ćete vidjeti neto razliku u iznosu nula za resurs (drugim riječima, rezervacije su jednake zadacima). Međutim, ako pogledate vrijeme na razini tjedna, možda ćete vidjeti da postoje dodjele od nula sati i rezervacije od 40 sati u prvom tjednu, no dodjele od 40 sati i rezervacije od nula sati u drugom tjednu. Sveukupno, rezervacije i dodjele usklađene su, ali se razlikuju od jednog do drugog tjedna.

Kada pogledate vrijeme na višim razinama, ćelije na kartici **Usklađivanje** imaju pokazatelj koji će vas obavijestiti da postoje razlike na nižim razinama. Dvostrukim dodirom na ćeliju možete povećati prikaz razlike. Zatim možete odabrati i držati (ili kliknite desnom tipkom miša) kako biste prikaz smanjili. Odabirom resursa i korištenjem kontrole **Sljedeća razlika** na alatnoj traci rešetke možete ići na sljedeću razliku između rezervacija i zadataka za taj resurs. Zatim možete koristiti kontrolu **Prethodna razlika** da biste se vratili. Možete i isključiti pokazatelj razlike i ponašanje navigacije u odjeljku **Postavke.**

Ako imate dodjele zadataka za resurs, ali bez rezervacija, odaberite manjak rezervacija na kartici **Usklađivanje** stranice **Projekti**, a zatim odaberite **Produlji rezervaciju**. Prikazat će se dijaloški okvir **Produlji rezervaciju** koji prikazuje rezervacija koja je potrebna za rješavanje manjka resursa. Dijaloški okvir prikazuje i postojeće rezervacije resursa diljem projekata ili drugih entiteta koji se mogu planirati. Ako odaberete **U redu** da biste izradili rezervaciju za resurs, bez obzira na dostupnost tog resursa, može doći do prebukiranosti.

Rezervacije stvorene putem radnje **Produlji rezervaciju** povezane su s primarnim projektnim zahtjevom. Kada se pokreće produljenje, ne može se odrediti posebni zahtjev koji se mora produljiti, jer bi resurs mogao biti povezan s više zahtjeva za projekt.

Voditelj projekta ili upravitelj resursa zatim može upotrijebiti ploču s rasporedom kako bi upravljao svim situacijama u kojima resurs ima prevelik broj rezervacija izvan svog kapaciteta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]