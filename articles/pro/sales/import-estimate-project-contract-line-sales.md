---
title: Uvoz procjene u redak ugovora koji se temelji na projektu
description: U ovoj temi nalaze se informacije o uvozu financijskih procjena iz projekta u redak ugovora.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9ac367baba4529e86a42d812b7d9b2550812e297
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4073621"
---
# <a name="importing-an-estimate-to-a-project-based-contract-line"></a>Uvoz procjene u redak ugovora koji se temelji na projektu

_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_

U aplikaciji Dynamics 365 Project Operations možete uvesti procjene iz projekta u redak ugovora koji se temelji na projektu.

1. Provjerite je li popunjeno polje **Projekt** u retku ugovora koji se temelji na projektu.
2. Na kartici **Pojedinosti retka ugovora**, na podrešetki, odaberite mogućnost **Uvoz iz procjene projekta**. Otvara se dijaloška stranica s mogućnostima sažimanja. Dostupne mogućnosti sažimanja su **Klasa transakcije**, **Kategorija**, **Uloga** i **Projektni zadatak**.
3. Na temelju odabira za sažimanje kopiraju se procjene iz projekta za sve klase transakcija i zadatke uključene u ovaj redak ugovora. Kako biste provjerili koje su klase transakcija uključene, na kartici **Općenito** retka ugovora koji se temelji na projektu provjerite vrijednosti u poljima **Uključi vrijeme**, **Uključi troškove** i **Uključi naknade**. 
4. Kako biste vidjeli koji su zadaci uključeni, odaberite karticu **Naplativi zadaci** u retku ugovora. Na temelju povezanih zadataka, koji imaju polje **Uključene klase transakcije** postavljeno na **Da**, sve procjene za te kombinacije zadataka i klasa transakcija uvoze se u redak ugovora.

Kada uvozite procjene, sustav zadaje određivanje cijena na temelju cjenika za projekt priloženih ugovoru i vrste naplate postavljene na retku ugovora. Ako je zadatak ili kategorija postavljena na retku ugovora kao nenaplativa, uvezeni redak procjene bit će nenaplativ i neće se zbrajati s ugovorenom vrijednošću retka ugovora.

Kada redak ugovora ima pojedinosti retka, polja **Vrijednost ugovora** i **Procijenjeni porez** na retku ugovora sažeta su i ne mogu se uređivati.

Kada je odabrano više mogućnosti sažimanja, sustav pokušava sažeti po svim odabranim mogućnostima. Izlaz sažimanja rezultira s više uvezenih redaka ugovora nego ako odaberete samo jednu mogućnost sažimanja.

Na primjer, ako projekt ima sljedeće retke procjene troškova:

| Zadatak | Kategorija | Datum | Količina | Jedinična cijena | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Zrakoplovne karte | 10. 1. 2020. | 4 | 400 | 1600 |
| Zadatak B | Hoteli | 10. 1. 2020. | 4 | 200 | 800 |
| Zadatak C | Hoteli | 11. 1. 2020. | 2 | 200 | 400 |

Kada korisnik odluči sažeti po **Klasi transakcije**, uvest će se sljedeći podaci:

| Zadatak | Kategorija | Datum | Količina | Jedinična cijena | Iznos |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 10. 1. 2020. | 3.34 | 840 | 2800 |

Kada korisnik odluči sažeti po **Klasi transakcije** i **Kategoriji**, uvest će se sljedeći podaci:

| Zadatak | Kategorija | Datum | Količina | Jedinična cijena | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Zrakoplovne karte | 10. 1. 2020. | 4 | 400 | 1600 |
| &nbsp;| Hoteli | 10. 1. 2020. | 6 | 200 | 1200 |

Kada korisnik odabere sažeti po **Klasi transakcije**, **Kategoriji** i **Zadatku lisnog čvora**, uvest će se sljedeći podaci. Vidite kako je ovaj rezultat jednak onome koji je na projektu:

| Zadatak | Kategorija | Datum | Količina | Jedinična cijena | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Zrakoplovne karte | 10. 1. 2020. | 4 | 400 | 1600 |
| Zadatak B | Hoteli | 10. 1. 2020. | 4 | 200 | 800 |
| Zadatak C | Hoteli | 11. 1. 2020. | 2 | 200 | 400 |
