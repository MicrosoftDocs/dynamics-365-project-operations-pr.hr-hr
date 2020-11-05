---
title: Isključivanje dimenzije cijena
description: Ova tema pokazuje kako postaviti dimenzije cijena u rješenju Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073473"
---
# <a name="turn-off-a-pricing-dimension"></a>Isključivanje dimenzije cijena

Možda ćete morati pregledati i ažurirati svoju strategiju određivanja cijena svakih nekoliko godina. Za ažuriranja koja izvršite možda bude potrebno da isključite postojeću dimenziju cijena i stvorite novu. Na primjer, možda ste prethodno određivali cijenu po dimenziji **Uloga** , ali sada ste odlučili određivati cijenu po dimenziji **Radno iskustvo**. To može zahtijevati da isključite dimenziju **Uloga** kao dimenziju cijena i izradite dimenziju **Radno iskustvo** kao novu dimenziju cijena. 

Isključivanje dimenzije cijena, bez obzira na to je li unaprijed pripremljena ili prilagođena, možete provesti postavljanjem polja **Primjenjivo na trošak** i **Primjenjivo na prodaju** za dimenzije cijena na **Ne**.

No, kada to učinite, možda ćete primiti sljedeću poruku o pogrešci.

![Vjerojatnost pogreške poslovnog procesa kad se isključi dimenzija cijena](media/Business-Process-Error.png)


Ta poruka o pogrešci ukazuje na to da postoje zapisi cijena koji su prethodno postavljeni za dimenziju koja se isključuje. Svi zapisi u recima **Cijena uloge** i **Provizija cijene uloge** koji se odnose na dimenziju moraju se izbrisati prije postavljanja primjenjivosti dimenzije na **Ne**. Ovo se pravilo odnosi na unaprijed pripremljene dimenzije cijena i na prilagođene dimenzije cijena koje ste izradili. Ova provjera valjanosti provodi se zbog toga što Project Service ima ograničenje da svaki zapis retka **Cijena uloge** mora imati jedinstvenu kombinaciju dimenzija. Na primjer, u cjeniku pod nazivom **Stope troška za SAD, 2018.** , imate sljedeće retke **Cijena uloge**. 

| Radno mjesto – standardno         | Org. jedinica    |Jedinica   |Cijena  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Inženjer sustava|Contoso US|Hour| 100|USD|
| Viši inženjer sustava|Contoso US|Hour| 150| USD|


Kada isključite **Radno mjesto – standardno** kao dimenziju cijena, a modul za određivanje cijena Project Service pretražuje cijenu, upotrebljava se samo vrijednost **Org. jedinica** iz ulaznog konteksta. Ako je **Org. jedinica** ulaznog konteksta „Contoso US”, rezultat će biti neodređen jer se oba retka podudaraju. Da biste to izbjegli, kada stvorite zapise **Cijena uloge** , Project Service provjerava je li kombinacija dimenzija jedinstvena. Ako je dimenzija isključena nakon stvaranja zapisa **Cijena uloge** , ovo ograničenje može biti prekršeno. Stoga je potrebno da prije nego što isključite dimenziju izbrišete sve retke **Cijena uloge** i **Provizija cijene uloge** koji imaju tu vrijednost dimenzije.

