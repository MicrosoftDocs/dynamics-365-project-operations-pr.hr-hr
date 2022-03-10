---
title: Pregledavanje predloženih resursa
description: Ova tema pruža informacije o tome kako predložiti resurse projekta.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b3077f98052fcac9989a81b2fab12fa30d65d970
ms.sourcegitcommit: ebcaec7806ee8aee1323ef532d5b7735d27edd04
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403786"
---
# <a name="review-proposed-resources"></a>Pregledavanje predloženih resursa

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Upravitelji resursa mogu predložiti resurs voditelju projekta pomoću zahtjeva za resurs.

Kako biste pregledali predložene resurse, slijedite ove korake:

1. U rešetki **Zahtjev** ili u samom zahtjevu, odaberite **Pronađi resurse**.
2. Na stranici **Pomoćnik za planiranje** odaberite resurs, a zatim potvrdite da su svi predloženi sati uključeni u predloženu rezervaciju.
3. U oknu **Stvori rezervaciju resursa** polje **Status rezervacije** postavite na **Predloženo**, a zatim odaberite **Rezerviraj**.

    > [!NOTE]
    > Postavljanje stavke **Status rezervacije** na **Predloženo** ne rezervira resurs fiksno i ne zamjenjuje generički resurs imenovanim članom tima.

    Pojavljuju se sljedeća ažuriranja statusa:

    - Na stranici **Pomoćnik za raspored** pokazatelji statusa ažuriraju se kako bi bilo jasno da je rezervacija predložena, a ne fiksno rezervirana.
    - Na zahtjevu za resurs status se mijenja u **Potreban pregled**.
    - Na kartici **Tim** projekta vrijednost **Status zahtjeva** generičkog člana tima mijenja se u **Potreban pregled**.

Voditelj projekta može prihvatiti ili odbaciti prijedlog.

Kada upravitelji resursa obrađuju zahtjeve za resurs, mogu upotrijebiti neki od sljedećih pristupa:

- Predlaganje više resursa kako bi se zadovoljila potražnja ako nije dostupan jedan resurs koji bi odradio potrebne sate. Predloženi sati zatim se dijele na više resursa koji mogu odraditi potrebne sate. U ovom scenariju sati se ne smiju preklapati.
- Predložite manje resursa nego što je potrebno. U ovom scenariju predloženi kapacitet resursa je manji od potrebnih sati koje je odredio podnositelj zahtjeva. Nakon što podnositelj zahtjeva prihvati predložene resurse, stvara neispunjeni zahtjev za resurs koji pokriva preostalu potražnju.
- Rezerviranje više resursa kako bi se zadovoljila potražnja ako nije dostupan jedan resurs koji bi dovršio posao.
- Rezervirajte manje resursa nego što je potrebno. U ovom scenariju rezerviranih je sati manje od potrebnih sati. Sustav vas upućuje da predložite resurse umjesto rezervacija, tako da podnositelj zahtjeva može provjeriti valjanost i pratiti preostalu potražnju.

## <a name="resource-availability"></a>dostupnost resursa

Upravitelji resursa moraju pregledavati dostupnost resursa i ažurirati rezervacije. U nekim slučajevima nema formalne potražnje (zahtjev za resursom). Međutim, upravitelj resursa mora odgovoriti na neplanirani zahtjev koji dolazi putem drugih kanala, poput e-pošte, telefonskih poziva ili trenutačnih poruka. Upravitelji resursa ažuriraju resurse i rezervacije na **Ploči s rasporedom**.

Radno vrijeme resursa upotrebljava se kao osnova za izračun dostupnosti resursa. Rezervacije resursa iskorištavaju kapacitet resursa.

Boje i sjenčanje na **Ploči s rasporedom** upotrebljavaju se za prikaz rezervacija, dostupnosti i prekomjernih rezervacija, kao i statusa rezervacija. Postavka na **Ploči s rasporedom** omogućuje prikaz legende.

Ako se strelica udesno prikazuje pokraj pojedinačnog resursa koji se može rezervirati na **Ploči s rasporedom**, resurs se može proširiti da bi se prikazale pojedinosti posla za koji je resurs rezerviran.

Budući da Dynamics 365 Project Operations upotrebljava modul Universal Resource Scheduling, a ako imate instaliranu značajku Dynamics 365 Field Service, možete pregledati pojedinosti o rezervacijama resursa za projekte, radne naloge i sve druge entitete na koje ste proširili zakazivanje.

Za prikaz dodatnih pojedinosti o pojedinačnom resursu desnom tipkom miša kliknite resurs za otvaranje kartice resursa.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
