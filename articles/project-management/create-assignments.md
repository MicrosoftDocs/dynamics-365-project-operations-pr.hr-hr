---
title: Stvaranje dodjela resursa
description: U ovoj temi nalaze se informacije o stvaranju generičkih i imenovanih dodjela resursa.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 610d9f7abbe7bc2eea8cc9a238dd7cfa1c626787
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006952"
---
# <a name="create-resource-assignments"></a>Stvaranje dodjela resursa

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_


Dodjela resursa izravna je povezanost člana projektnog tima sa zadatkom lisnog čvora. U ovoj temi nalaze se informacije o različitim načinima za dodjelu resursa.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Izrada generičkog člana tima putem dodjele zadatka


Kada stvarate generičkog člana tima putem dodjele zadatka, stvarate rezervirano mjesto ili generički resurs. Taj generički resurs koji opisuje svojstva imenovanog resursa za kojeg u konačnici želite da radi na zadacima. Zatim generirate uvjet, ili šaljete zahtjev koristeći uvjet, koji se koristi za pretraživanje i rezervaciju imenovanog resursa.

1. Na rešetki Raspored za zadatak, odaberite ikonu Resurs u ćeliji **Resurs**.
2. Upišite naziv koji će služiti kao naziv rezerviranog mjesta resursa. Na primjer, upravitelj programa.
3. Odaberite **Izradi** i u polju **Brza izrada projektnog člana tima** postavite ulogu za generički resurs.
4. Prema potrebi, dodijelite zadatke tom resursu rezerviranog mjesta odabirom resursa na **Biraču resursa** za taj zadatak. Resursi navedeni pod stavkom **Članovi tima**.
5. Kada završite s dodjelom generičkog resursa, na kartici **Tim** odaberite generički resurs, a zatim odaberite **Generiraj preduvjet** kako biste stvorili preduvjet resursa za generički resurs.
6. Odaberite **Rezerviraj** za generički resurs, a zatim možete upotrijebiti ploču s rasporedom za pronalaženje i rezerviranje stvarnog resursa. Možete poslati i zahtjev za ispunjenje od strane upravitelja resursa.
7. Kada je generički resurs u potpunosti ispunjen (djelomično ispunjenje preduvjeta resursa neće rezultirati dodjelom resursa) imenovanim resursom, generički resurs se uklanja iz tima. Dodjele zadatka za generički resurs dodjeljuju se imenovanom resursu koji je ispunio preduvjet resursa za generički resurs.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Dodijeli imenovani resurs s popisa svih resursa koje je moguće rezervirati

Možete upotrijebiti okvir za pretraživanje u **Biraču resursa** za pretraživanje svih aktivnih resursa koje je moguće rezervirati i dodijeliti ih svakom zadatku lisnog čvora. Resursi dodijeljeni na taj način dodaju se timu bez rezervacija. To je slično dodavanju člana tima i odabiru mogućnosti **Nijedan** kao načina dodjele. Resurs se prikazuje na karticama **Tim**, **Dodjela resursa** i **Usklađivanje** kao resursi koji imaju samo zadatke i manjak rezervacija. Rezervirajte ih ako želite da iskoristite njihovu dostupnost.

1. Iz rešetke zadatka, ploče ili vremenske trake pomaknite se na stranicu **Dodijeljeno za**.
2. U okvir za pretraživanje počnite upisivati naziv. Rezultati pretraživanja za naziv prikazuju se u **Biraču resursa** pod stavkom **Ostali resursi**.
3. Odaberite resurs koji želite dodijeliti zadatku ili odaberite naziv resursa pod stavkom **Ostali resursi tima**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]