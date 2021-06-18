---
title: Upravljanje vremenskim zonama
description: Kada se stvori projekt, njegova vremenska zona temelji se na vremenskoj zoni definiranoj u primijenjenom predlošku radnog vremena.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1480d68105be1041e791de567b180178b330d71e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997727"
---
# <a name="manage-time-zones"></a>Upravljanje vremenskim zonama

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_


## <a name="projects"></a>Projekti

Kada se stvori projekt, vremenska zona temelji se na vremenskoj zoni definiranoj u primijenjenom predlošku radnog vremena. Na obrascu **Projekt** datumi su uvijek u odnosu s vremenskom zonom korisnika koji je prijavljen na svakoj kartici, osim kartice **Zadatak**. Kada pogledate strukturnu analizu rada, datumi će se uvijek prikazivati u vremenskoj zoni projekta.

## <a name="tasks"></a>Zadaci

Kada se stvori zadatak, vrijeme početka, vrijeme završetka i sati/dan kontroliraju se radnim vremenom projekta. Na primjer, ako je zadatak stvoren s projektom čija je vremenska zona – 8 PST i ima sljedeće radno vrijeme: 9:00 do 17:00, od ponedjeljka do petka, svaki zadatak stvoren bez dodjele poštivat će vrijeme početka i vrijeme završetka kalendara projekta.

## <a name="manage-resources-with-time-zones"></a>Upravljanje resursima s pomoću vremenskih zona

Za točne i predvidljive rezultate tijekom uporabe mogućnosti **Produlji rezervaciju**, dva su ključna preduvjeta koja se moraju ispuniti:  

- Korisnik mora konfigurirati vremensku zonu svog uređaja tako da odgovara vremenskoj zoni definiranoj u stavci **Postavke personalizacije** sustava.
 
  ![Postavke vremenske zone u programu Windows 10](media/reconcile-assignments-03.png)

  ![Postavke vremenske zone u personaliziranim postavkama](media/reconcile-assignments-04.png)
 
- Resurs koji se može rezervirati mora imati najmanje jednu minutu radnog vremena koje se preklapa s konturama koje se upotrebljavaju za određivanje traženog produljenja. Na primjer, sljedeći resursi s radnim vremenom koje pada između 9:00 i 19:00 sati. 

  ![Usporedba kontura resursa](media/reconcile-assignments-05.png)

Tablice u nastavku prikazuju:

- Predložak kalendara projekta
- Resurs A: Ovaj resurs ima isti kalendar i nalazi se u istoj vremenskoj zoni kao i projekt. Vrijeme početka rezervacija bit će 9:00.
- Resurs B: Ovaj se resurs nalazi u različitoj vremenskoj zoni od projekta i započinje u 7:00 u svojoj vremenskoj zoni. Međutim, rezervacije će započeti u 9:00, jer je to najranije vrijeme početka konture dodjele.
- Resursi C i D: Resursi se nalaze u različitim vremenskim zonama koje se razlikuju i međusobno i od projekta, a njihove rezervacije započinju najranije od odgovarajućih dostupnih vremena početka.

|Entitet  |Kalendar  |
|-|-|
|Predložak kalendara projekta   | ![kalendar projekta](media/reconcile-assignments-06.png) |
|Resurs A  | ![Kalendar resursa A](media/reconcile-assignments-06.png) |
|Resurs B  |  ![Kalendar resursa B](media/reconcile-assignments-07.png) |
|Resurs C  |  ![Kalendar resursa C](media/reconcile-assignments-08.png) |
|Resurs D  | ![Kalendar resursa D](media/reconcile-assignments-09.png)  |
 
Kada prijeđete na prikaz **Usklađivanje**, prikazuju se dodjele resursa i pridruženi nedostaci rezervacija.

![Prikaz usklađivanja prije produljena](media/reconcile-assignments-10.png)

Nakon što se za svaki resurs upotrijebi funkcija produljenog rezerviranja, rezervacije se uspješno produljuju za svaki resurs, jer se radno vrijeme svakog resursa preklapa s konturama nedostatka.

![Prikaz usklađivanja nakon produljena rezervacije](media/reconcile-assignments-11.png) 

Vidjet ćete kako podrobniji uvid u pojedinosti rezervacije pokazuje razlike u vremenu početka rezervacija. Rezervacije započinju najranije s vremenom početka kontura dodjele i ne prije dostupnog vremena početka resursa.

![Nove rezervacije resursa u ploči s rasporedom](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]