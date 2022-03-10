---
title: Uvoz procjena za projekt u redak ponude projekta
description: U ovoj temi nalaze se informacije o uvozu procjena iz projekta u redak ponude projekta.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a9ac27b7694927f9cea88b49310f3106fbc6542cc0f7f1756744b970358c1057
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993502"
---
# <a name="import-estimates-for-a-project-to-a-project-quote-line"></a>Uvoz procjena za projekt u redak ponude projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_


Ako se projekt stvara tijekom faze pretprodaje, možete odabrati uvoz financijske procjene iz projekta u redak ponude koji se temelji na projektu.

1. Pazite da redak ponude koji se temelji na projektu sadrži podatke o projektu u polju **Projekt**.
2. Na kartici **Pojedinosti retka ponude** odaberite **Uvoz iz procjene projekta**.
3. U dijaloškom okviru otvara se stranica na kojoj odaberite jednu od sljedećih mogućnosti sažimanja:

  - **Razred transakcije**
  - **Kategorija**
  - **Uloga** 
  - **Projektni zadatak**

Na temelju vašeg odabira kopiraju se procjene iz projekta za sve klase transakcija uključene u ovaj redak ponude. Kako biste provjerili koje su klase transakcija uključene, odaberite karticu **Općenito** na retku ponude koji se temelji na projektu i provjerite vrijednosti za **Uključi vrijeme**, **Uključi troškove** i **Uključi naknade**.

Kada uvozite procjene, sustav će zadati određivanje cijena na temelju cjenika za projekt priloženih ponudi i vrste naplate postavljene na retku ponuda koji se temelji na projektu. Ako je uloga ili kategorija postavljena na retku ponude koji se temelji na projektu kao nenaplativa, uvezeni redak procjene postavit će se kao nenaplativ i neće se zbrajati s ponuđenom vrijednošću retka ponude.

Kada redak ponude ima pojedinosti retka, polja **Vrijednost ponude** i **Procijenjeni porez** na ponudi sažeta su i ne mogu se uređivati.

Kada je odabrano više mogućnosti sažimanja, sustav pokušava sažeti po svim odabranim mogućnostima. Rezultat je da će izlaz uvezenih redaka ponude biti veći nego ako ste odabrali samo jednu mogućnost sažimanja.

Na primjer, ako projekt ima sljedeće retke procjene troškova.

| Zadatak | Kategorija | Datum | Količina | Jedinična cijena | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Zrakoplovne karte | 10. 1. 2020. | 4 | 400 | 1600 |
| Zadatak B | Hoteli | 10. 1. 2020. | 4 | 200 | 800 |
| Zadatak C | Hoteli | 11. 1. 2020. | 2 | 200 | 400 |

Kada korisnik odluči sažeti po klasi transakcije, uvest će se sljedeći podaci.

| Zadatak | Kategorija | Datum | Količina | Jedinična cijena | Iznos |
| --- | --- | --- | --- | --- | --- |
| | | 10. 1. 2020. | 3.34 | 840 | 2800 |

Kada korisnik odluči sažeti po klasi transakcije i kategoriji, uvest će se sljedeći podaci.

| Zadatak | Kategorija | Datum | Količina | Jedinična cijena | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Zrakoplovne karte | 10. 1. 2020. | 4 | 400 | 1600 |
| | Hoteli | 10. 1. 2020. | 6 | 200 | 1200 |

Kada korisnik odluči sažeti po klasi transakcije, kategoriji i zadatku lisnog čvora, uvest će se sljedeći podaci. Vidite kako je ovaj rezultat jednak onome koji je bio na projektu.

| Zadatak | Kategorija | Datum | Količina | Jedinična cijena | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Zrakoplovne karte | 10. 1. 2020. | 4 | 400 | 1600 |
| Zadatak B | Hoteli | 10. 1. 2020. | 4 | 200 | 800 |
| Zadatak C | Hoteli | 11. 1. 2020. | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
