---
title: Dodjela resursa zadatku
description: Ova tema pruža informacije o tome kako dodijeliti resurse zadacima.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: b1ad011b2d78dd85023be7cf380ce19c3b2b8441
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149984"
---
# <a name="assign-a-resource-to-a-task"></a>Dodjela resursa zadatku

[!include [banner](../includes/psa-now-project-operations.md)]

Postoje tri načina za dodjelu resursa zadatku u aplikaciji Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Rezervirajte resurs kao član tima, a zatim ga dodijelite zadatku

Možete dodati resurs projektnom timu i zatim ga dodijeliti zadacima u projektnom rasporedu.

1. Na kartici **Član tima** dodajte novog člana tima odabirom **Novo**. 

2. Otvora se panel **Brza izrada člana tima** na kojem možete odabrati naziv za resurs koji je moguće rezervirati i postaviti ulogu. 

    Odaberite jednu od sljedećih načina dodjeljivanja za rezervaciju resursa:

    - **Puni kapacitet** rezervira puni kapacitet resursa za odabrane datume od i do.
    - **Postotni kapacitet** rezervira određeni postotak kapaciteta resursa za odabrane datume od i do.
    - **Ravnomjerna raspodjela po satima** rezervira resurs na određeni broj sati, ravnomjerno ih raspoređujući svakog dana za vrijeme određenih od i do datuma.
    - **Punjenje sprijeda po satima** rezervira resurs na određeni broj sati, umečući sprijeda sate svakog dana za vrijeme određenog razdoblja.
    - **Ništa** dodaje resurs timu, ali ne stvara nikakve rezervacije koje bi trošile njegov kapacitet.

3. Na rešetki **Raspored** za zadatak, odaberite ikonu **Resurs** u ćeliji resursa, a zatim pod **Članovi tima** odaberite člana tima kojeg ste upravo dodali. 

> [!NOTE]
> Na karticama **Članovi tima** i **Usklađivanje**, resurs pokazuje rezervirane i dodijeljene sate. Sati bi trebali biti isti, ali ne moraju biti, budući da rezervacije i zadaci nisu usko povezani. Kartica **Usklađivanje** pruža vam pojedinosti kada su različite, na primjer, kada dodijelite resursu više sati nego što ste rezervirali. Po potrebi, možete ispraviti informacije produljivanjem rezervacija resursa ili izmjenom zadatka.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Izrada generičkog člana tima putem dodjele zadatka

Kada izrađujete generičkog člana tima putem dodjele zadatka, izrađujete rezervirano mjesto ili generički resurs koji opisuje karakteristike imenovanog resursa za kojeg u konačnici želite da radi na zadacima. Zatim generirate uvjet (ili šaljete zahtjev koristeći uvjet) koji se koristi za pretraživanje i rezervaciju imenovanog resursa.

1. Na rešetki **Raspored** za zadatak, odaberite ikonu **Resurs** u ćeliji resursa.

2. Upišite naziv koji će služiti kao naziv rezerviranog mjesta resursa. Na primjer, upravitelj programa.

3. Odaberite **Izradi** i u polju **Brza izrada projektnog člana tima** postavite ulogu za generički resurs.

4. Možete nastaviti dodjeljivati zadatke tom rezerviranom mjestu resursa odabirom resursa na **Biraču resursa** za taj zadatak. Navedeni su pod stavkom **Članovi tima**.

5. Kada završite s dodjelom generičkog resursa, odaberite ga na kartici **Tim**, a zatim odaberite **Generiraj preduvjet** da biste izradili preduvjet resursa za generički resurs.

6. Odaberite **Rezerviraj** za generički resurs. Zatim možete koristiti Ploču s rasporedom za pronalazak i rezerviranje pravog resursa. Možete poslati i zahtjev za ispunjenje od strane upravitelja resursa.

7. Kada se generički resurs ispuni imenovanim resursom, tada se uklanja iz tima i dodjele zadataka generičkog resursa se dodjeljuju imenovanom resursu koji je ispunio preduvjet generičkog resursa za resursom.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Dodijeli imenovani resurs s popisa svih resursa koje je moguće rezervirati

Možete koristiti okvir za pretraživanje u **Biraču resursa** za pretraživanje resursa koje je moguće rezervirati i za njihovo dodjeljivanje zadatku.

Resursi dodijeljeni na taj način dodaju se timu bez rezervacija. To je slično dodavanju člana tima i odabiru Nijedan kao načina dodjele. Resurs je prikazan na karticama **Tim** i **Usklađivanje** kao resursi koji imaju samo zadatke i koji imaju manjak rezervacija. Rezervirajte ih ako želite da iskoristite njihovu dostupnost.

1. Na rešetki **Raspored** za zadatak, odaberite ikonu **Resurs** u ćeliji resursa.

2. Počnite tipkati naziv. Rezultati pretraživanja za naziv prikazuju se u **Biraču resursa** pod stavkom **Ostali resursi**.

3. Odaberite resurs koji želite dodijeliti zadatku.

