---
title: Kako mogu „promjenjivo rezervirati” resurse u verziji aplikacije 2.x?
description: U ovom članku je opisano kako promjenjivo rezervirati članove projektnog tima putem aplikacije Project Service.
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
ms.openlocfilehash: d7eb9e3baea3c3f696845905a2522940d14bba8a8d42917f8fe1b90c7c443747
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993907"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Kako mogu promjenjivo rezervirati resurse u web-aplikaciji (aplikaciji Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Možete uvjetno zakazati ili „promjenjivo rezervirati” resurs za projektni tim da biste pokazali da planirate dodijeliti resurs projektu. Promjenjive rezervacije ne troše dostupni kapacitet resursa. Promjenjivo rezervirani članovi tima ne mogu biti dodijeljeni projektnim zadacima. Samo resursi s fiksno rezerviranim statusom i dodijeljenom vrstom izvršavanja mogu biti dodijeljeni zadacima (pod uslovom da imaju dovoljno fiksno rezerviranih sati za pokrivanje truda dodjele).

Promjenjivo rezervirani članovi tima se prikazuju na rešetki Članovi tima, a njihovi promjenjivo rezervirani sati se prikazuju u stupcu Promjenjive rezervacije. Također se prikazuju na ploči s rasporedom. I u ovom slučaju ne pokazuju nikakvo trošenje kapaciteta budući da promjenjive rezervacije ne troše kapacitet resursa.

Postoje tri načina promjenjive rezervacije člana tima za projekat pomoću verzije 2.x aplikacije Project Service. Promjenjivo rezervirati možete pomoću ploče s rasporedom, koristeći značajku Zadrži rezervacije ili stvaranjem generičkog resursa. Ove metode su opisane u nastavku.

## <a name="soft-book-with-the-schedule-board"></a>Promjenjiva rezervacija na ploči s rasporedom

Za promjenjive rezervacije pomoću ploče s rasporedom, slijedite sljedeći postupak: 
1. Otvorite ploču s rasporedom.
2. Odaberite karticu Projekat na dnu panela Preduvjeti rezervacije na ploči s rasporedom.
3. Pronađite projekat za koji želite promjenjivo rezervirati resurs. Ako imate mnogo projekata, kliknite na zaglavlje stupca projekta, a zatim koristite filtar za pronalazak vašeg projekta.
4. Kliknite na projekat, a zatim ga povucite i ispustite na vremenskoj rešetki resursa.
5. Ovim će se na desnoj strani otvoriti panel Stvori rezervaciju za resurs. Prilagodite datum početka i završetka, za Status rezervacije odaberite Promjenjiva i postavite sate. 
6. Kliknite Rezerviraj.
7. Resurs će se sada u projektu prikazati kao član tima s promjenjivo rezerviranim satima u stupcu Promjenjive rezervacije.

Imajte na umu da ih ne možete dodijeliti zadacima u strukturnoj analizi rada (SAR-u) budući da resursi moraju biti fiksno rezervirani u timu da bi se mogli dodijeliti.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Promjenjiva rezervacija pomoću značajke Zadrži rezervacije

Za promjenjive rezervacije pomoću značajke Zadrži rezervacije, slijedite sljedeći postupak:
1. Kliknite Novo na rešetki članova tima.
2. Odaberite resurs koji se može rezervirati, ulogu i datume od i do.
3. Odaberite bilo koju metodu dodjele osim Ništa:
- Puni kapacitet
- Postotni kapacitet
- Raspodijeli ravnomjerno po satima
- Umetanje sprijeda po satima
4. Kliknite Spremi. Resurs ćete vidjeti na rešetki tima, a njegovi sati će biti označeni kao Fiksni.
5. Zadržite rezervacije resursa klikom na Zadrži rezervacije.
6. Kada se ploča s rasporedom otvori, proširite resurs za prikaz njegovih rezervacija. Rezervacija će biti označena kao Fiksna.
7. Desnom klikom kliknite na rezervaciju pod stavkom Promijeni status, a zatim odaberite Promjenjiva rezervacija, te Promjenjiva. Status rezervacije je sada Promjenjiva.
8. Nakon zatvaranja ploče s rasporedom, vidjet ćete da su se na rešetki članova tima sati resursa promijenili sa Fiksni na Promjenjivi.
Imajte na umu da ako fiksno rezervirate resurs za tim, a zatim mu dodijelite zadatke u SAR-u, kada koristite značajku Zadrži rezervacije za promjenu statusa sa Fiksni na Promjenjivi, dodjele zadataka za taj resurs će biti uklonjene budući da se zadacima mogu dodijeliti samo fiksno rezervirani resursi.

## <a name="soft-book-by-creating-a-generic-resource"></a>Promjenjiva rezervacija stvaranjem generičkog resursa

Promjenjivu rezervaciju možete stvoriti generiranjem generičkog resursa člana tima, ispunjavanjem pomoću ploče s rasporedom ili Zahtjeva resursa i promjenom vrste tijekom rezervacije.
Slijedite sljedeću proceduru kako biste to uradili:

1. U SAR-u projekta dodijelite uloge zadacima za koje želite generirati generičke članove tima.
2. Kliknite Generiraj projektni tim.
3. Na rešetki članova projektnog tima odaberite generički resurs i kliknite Rezerviraj.
4. Na ploči s rasporedom odaberite resurs koji želite rezervirati.
5. Na panelu Stvori rezervaciju za resurs ploče s rasporedom promijenite Status rezervacije u Promjenjiva.
6. Kliknite Rezerviraj ili Rezerviraj i zatvori.

Nakon zatvaranja ploče s rasporedom, vidjet ćete odabrani resurs koji je dodan timu s promjenjivo rezerviranim satima, kao i dodijeljenim satima. Vidjet ćete i da je generički resurs i dalje u timu, što pokazuje da su zadaci dodijeljeni promjenjivo rezerviranom članu tima.

Kada budete spremni za promjenu promjenjivo rezerviranog resursa člana tima u fiksno rezerviranog člana tima kako biste ga mogli dodijeliti zadacima, uradite sljedeće:

1. Odaberite taj resurs i kliknite Zadrži rezervacije.
2. Kada se ploča s rasporedom otvori, proširite resurs za prikaz njegovih rezervacija. Rezervacija će biti označena kao Promjenjiva.
3. Desnom klikom kliknite na rezervaciju pod stavkom Promijeni status, a zatim odaberite Fiksna rezervacija, te Fiksna. Status rezervacije je sada Fiksna.
4. Nakon zatvaranja ploče s rasporedom, vidjet ćete da su se na rešetki članova tima sati resursa promijenili sa Promjenjivi u Fiksni. Sada možete dodijeliti resurs zadacima (pod uvjetom da su fiksno rezervirani sati usklađeni s satima rada zadatka za dodjelu). Imajte na umu da ako ste slijedili korake generičkog resursa iz 3. stavke koja je navedena ranije, kada promjenite status resursa kojeg je moguće rezervirati sa promjenjivog u fiksni, generički član tima će biti uklonjen iz tima.


[!INCLUDE[footer-include](../includes/footer-banner.md)]