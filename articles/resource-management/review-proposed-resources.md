---
title: Pregledavanje predloženih resursa
description: Ova tema pruža informacije o tome kako predložiti resurse projekta.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
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
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401164"
---
# <a name="review-proposed-resources"></a>Pregledavanje predloženih resursa

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

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

## <a name="resource-availability"></a>dostupnost resursa

Ključno je da upravitelji resursa mogu pregledavati dostupnost resursa i ažurirati rezervacije. U nekim slučajevima ne postoji službena potražnja (zahtjev za resurs), ali upravitelj resursa mora odgovoriti na neplaniranu potražnju koja dolazi putem kanala kao što su e-pošta, telefonski poziv ili izravna poruka. Upravitelji resursa ažuriraju resurse i rezervacije na ploči s rasporedom.

Radno vrijeme resursa koristi se kao osnova za izračun dostupnosti resursa. Rezervacije resursa iskorištavaju kapacitet resursa.

Na ploči s rasporedom boje i sjenčanje označavaju rezervacije, dostupnost i prekomjerne rezervacije, kao i status rezervacija. Postavka u postavkama ploče s rasporedom omogućuje prikaz legende.

Ako se strelica udesno prikazuje pokraj pojedinačnog resursa koji se može rezervirati na ploči s rasporedom, resurs se može proširiti da bi se prikazale pojedinosti posla za koji je resurs rezerviran.

Budući da Dynamics 365 Project Operations upotrebljava modul Universal Resource Scheduling, ako imate instaliranu uslugu Dynamics 365 Field Service, možete pregledati pojedinosti o rezervacijama resursa za projekte, radne naloge i sve druge entitete na koje ste proširili planiranje.

Za prikaz dodatnih pojedinosti o pojedinačnom resursu desnom tipkom miša kliknite resurs za otvaranje kartice resursa.



[!INCLUDE[footer-include](../includes/footer-banner.md)]