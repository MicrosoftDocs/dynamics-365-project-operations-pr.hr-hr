---
title: Promjenjivo rezerviranje preduvjeta
description: Ova tema pruža informacije o tome kako promjenjivo rezervirati preduvjete.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: bc58c805bfe1a3087600b8d4a6be2d1bcdd18188
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997907"
---
# <a name="soft-book-requirements"></a>Promjenjivo rezerviranje preduvjeta

[!include [banner](../includes/psa-now-project-operations.md)]

Preduvjet resursa može biti fiksno rezerviran. Fiksno rezerviranje stvara prijedlog koji iskorištava kapacitet resursa. Prijedlog se zatim šalje natrag podnositelju zahtjeva na odobrenje. Promjenjivo rezerviranje uvjetno dodaje resurs u projektni tim i ima drugačiji status na ploči s rasporedom, ali ne iskorištava kapacitet resursa. Za promjenjivo rezerviranje resursa na ploči s rasporedom postavite polje **Status rezervacije** na **Promjenjivo**.

![Status rezervacije postavljen je na Promjenjivo](media/Resource-Management-image77.png)

Kada je kartica **Tim** u prikazu **Imenovani članovi tima**, resurs se prikazuje tamo. Promjenjivo rezervirani sati zabilježeni su u stupcu **Promjenjivo rezervirani sati**.

![Promjenjivo rezervirani sati u prikazu Imenovani članovi tima](media/Resource-Management-image78.png)

Promjenjivo rezervirani članovi tima ne mogu biti dodijeljeni zadacima.

![Promjenjivo rezervirani član tima dodijeljen zadatku](media/Resource-Management-image79.png)

Na kartici **Usklađivanje** nema prikazanih rezervacija za promjenjivo rezervirani resurs jer se na kartici **Usklađivanje** bilježe samo fiksne rezervacije.

![Promjenjivo rezervirani resurs bez rezervacija na kartici Usklađivanje](media/Resource-Management-image80.png)

> [!NOTE]
> Ne možete promjenjivo rezervirati resurs iz preduvjeta koji je generiran iz generičkog člana tima.

Na ploči s rasporedom promjenjive rezervacije za resurs označene su drugom bojom.

![Promjenjive rezervacije na ploči s rasporedom](media/Resource-Management-image81.png)

Da biste promjenjivu rezervaciju pretvorili u fiksnu rezervaciju, na ploči s rasporedom kliknite desnom tipkom miša na promjenjivu rezervaciju, a zatim odaberite **Promjena statusa** \> **Fiksna rezervacija** \> **Fiksno**.

![Promjena statusa rezervacije u Fiksno](media/Resource-Management-image82.png)

Rezervacija je promijenjena, a status se mijenja na ploči s rasporedom. Budući da je status rezervacije sada **Fiksno**, resurs se prikazuje kao rezerviran, a njegov kapacitet i dostupnost su prilagođeni.

Pomoću iste metode možete otkazati fiksnu rezervaciju ili promjenjivu rezervaciju na ploči s rasporedom.

Da biste promjenjivo rezervirani resurs pretvorili u fiksno rezervirani resurs na kartici **Tim** projekta, odaberite resurs, a zatim **Potvrdi**.

![Potvrda naredbe](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]