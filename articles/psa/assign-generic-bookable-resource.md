---
title: Dodijeli generičke resurse koji se mogu rezervirati za zadatak i projektni tim
description: Ova tema pruža informacije o rezerviranju generičkih resursa za zadatke i projektne timove.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073403"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Dodijeli generičke resurse koji se mogu rezervirati zadatku i generiraj zahtjeve resursa 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Osim rezerviranja i dodjele imenovanih ili stvarnih resursa vašem projektu, možete dodijeliti generičke resurse projektnim zadacima. Ti resursi mogu poslužiti kao rezervirana mjesta za imenovane resurse dok ne budete spremni za popunjavanje projekta s imenovanim resursima. 

1. U programu Project Service Automation (PSA), otvorite stranicu **Projekt** i na kartici **Raspored** , unesite naziv položaja generičkog resursa u ćeliji **Resurs** rasporeda. Ili kliknite ikonu **Resurs** u ćeliji da biste otvorili birača resursa, a zatim unesite naziv generičkog resursa koji želite izraditi.

![Izrada i dodjela generičkog člana tima](media/RM-how-to-9.png)

Time će se otvoriti panel **Brza izrada: Član projektnog tima**. 

2. Unesite ulogu i organizacijsku jedinicu člana tima generičkog resursa, a zatim kliknite **Spremi**.

![Brza izrada generičkog člana tima](media/RM-how-to-10.png)

3. Nakon što ste izradili novi član tima generičkog resursa, dodijeljen je zadatku. Možete nastaviti dodjeljivati taj generički resurs drugim zadacima u rasporedu zadataka.

![Dodjela postojećeg generičkog člana tima zadacima](media/RM-how-to-11.png)

4. Nakon što ste dodijelili generički resurs, možete generirati zahtjev resursa i ispuniti ga izravnim rezerviranjem ili slanjem zahtjeva resursa upravitelju resursa.

![Generiranje zahtjeva za generički član tima](media/RM-how-to-12.png)

Na rešetki člana tima, osim što imate mogućnost koristiti birača resursa kao što je navedeno gore, možete izravno dodati generičke resurse. Resursi se dodaju zahtjevom resursa koji se temelji na datumima početka/završetka i načinu dodjele navedenim na panelu **Brza izrada: Član projektnog tima**.

Možete vidjeti razliku ako izravno dodate generički član tima, a zatim dodijelite više zadataka generičkom resursu nego što imaju potrebnih sati za pokrivanje. Kliknite **Generiraj zahtjev** za ponovno generiranje zahtjeva da biste uskladili potrebne sate i zadatke.

Možete kliknuti i vezu **Zahtjev resursa** u rešetki tima da biste otvorili zahtjev i dodali vještine, preferirane resurse, itd.

![Zahtjev resursa](media/RM-how-to-13.png)
