---
title: Isključivanje dimenzije cijena
description: Ovaj članak pokazuje kako postaviti dimenzije cijena u rješenju Project Service.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 81c3cfaad8dc8d057985b509f20c3ba31de45e3b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913151"
---
# <a name="turn-off-a-pricing-dimension"></a>Isključivanje dimenzije cijena

[!include [banner](../includes/psa-now-project-operations.md)]

Možda ćete morati pregledati i ažurirati svoju strategiju određivanja cijena svakih nekoliko godina. Za ažuriranja koja izvršite možda bude potrebno da isključite postojeću dimenziju cijena i stvorite novu. Na primjer, možda ste prethodno određivali cijenu po dimenziji **Uloga**, ali sada ste odlučili određivati cijenu po dimenziji **Radno iskustvo**. To može zahtijevati da isključite dimenziju **Uloga** kao dimenziju cijena i izradite dimenziju **Radno iskustvo** kao novu dimenziju cijena. 

Isključivanje dimenzije cijena, bez obzira na to je li unaprijed pripremljena ili prilagođena, možete provesti postavljanjem polja **Primjenjivo na trošak** i **Primjenjivo na prodaju** za dimenzije cijena na **Ne**.

No, kada to učinite, možda ćete primiti sljedeću poruku o pogrešci.

![Vjerojatnost pogreške poslovnog procesa kad se isključi dimenzija cijena.](media/Business-Process-Error.png)


Ta poruka o pogrešci ukazuje na to da postoje zapisi cijena koji su prethodno postavljeni za dimenziju koja se isključuje. Svi zapisi u recima **Cijena uloge** i **Provizija cijene uloge** koji se odnose na dimenziju moraju se izbrisati prije postavljanja primjenjivosti dimenzije na **Ne**. Ovo se pravilo odnosi na unaprijed pripremljene dimenzije cijena i na prilagođene dimenzije cijena koje ste izradili. Ova provjera valjanosti provodi se zbog toga što Project Service ima ograničenje da svaki zapis retka **Cijena uloge** mora imati jedinstvenu kombinaciju dimenzija. Na primjer, u cjeniku pod nazivom **Cijene koštanja za SAD, 2018.**, imate sljedeće retke **Cijena uloge**. 

| Radno mjesto – standardno         | Org. jedinica    |Jedinica   |Cijena  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Inženjer sustava|Contoso US|Hour| 100|USD|
| Viši inženjer sustava|Contoso US|Hour| 150| USD|


Kada isključite **Radno mjesto – standardno** kao dimenziju cijena, a modul za određivanje cijena Project Service pretražuje cijenu, upotrebljava se samo vrijednost **Org. jedinica** iz ulaznog konteksta. Ako je **Org. jedinica** ulaznog konteksta „Contoso US”, rezultat će biti neodređen jer se oba retka podudaraju. Da biste to izbjegli, kada stvorite zapise **Cijena uloge**, Project Service provjerava je li kombinacija dimenzija jedinstvena. Ako je dimenzija isključena nakon stvaranja zapisa **Cijena uloge**, ovo ograničenje može biti prekršeno. Stoga je potrebno da prije nego što isključite dimenziju izbrišete sve retke **Cijena uloge** i **Provizija cijene uloge** koji imaju tu vrijednost dimenzije.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
