---
title: Uvoz procjena za projekt u redak ponude koji se temelji na projektu – jednostavno
description: U ovoj temi nalaze se informacije o načinu uvoza procjena iz projekta u redak ponude.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0aedaa2ec77bb54031fccd0db2872e0aa5fea5e0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858239"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Uvoz procjena za projekt u redak ponude koji se temelji na projektu 

_**Primjenjuje se na:** Osnovna implementacija – od dogovora do predračuna, Project Operations za scenarije koji se temelje na resursima / bez zaliha_

Ako se projekt stvara tijekom faze pretprodaje, možete odabrati uvoz financijske procjene iz projekta u redak ponude koji se temelji na projektu.

1. Pazite da redak ponude koji se temelji na projektu sadrži podatke o projektu u polju **Projekt**.
2. Na kartici **Pojedinosti retka ponude** odaberite **Uvoz iz procjene projekta**.
3. U dijaloškom okviru otvara se stranica na kojoj odaberite jednu od sljedećih mogućnosti sažimanja.

  - **Razred transakcije**
  - **Kategorija**
  - **Uloga** 
  - **Projektni zadatak**

Na temelju vašeg odabira kopiraju se procjene iz projekta za sve klase transakcija uključene u ovaj redak ponude. Kako biste provjerili koje su klase transakcija uključene, odaberite karticu **Općenito** u retku ponude koji se temelji na projektu i provjerite vrijednosti za **Uključi vrijeme**, **Uključi troškove**, **Uključite materijale** i **Uključi naknade**.  Kako biste provjerili koji su zadaci uključeni, odaberite karticu **Naplativi zadaci** u retku ponude.

Ovisno o povezanim Zadacima i Uključenim klasama transakcija, procjene za te kombinacije zadataka i klasa transakcija uvoze se u redak ponude.

Kada uvozite procjene, sustav će zadati određivanje cijena na temelju cjenika za projekt priloženih ponudi i vrste naplate postavljene na retku ponuda koji se temelji na projektu. Ako je zadatak ili kategorija postavljena na retku ponude koji se temelji na projektu kao nenaplativa, uvezeni redak procjene postavit će se kao nenaplativ i neće se zbrajati s ponuđenom vrijednošću retka ponude.

Kada redak ponude ima pojedinosti retka, polja **Vrijednost ponude** i **Procijenjeni porez** na ponudi sažeta su i ne mogu se uređivati.

Kada je odabrano više mogućnosti sažimanja, sustav pokušava sažeti po svim odabranim mogućnostima. Rezultat je da će izlaz uvezenih redaka ponude biti veći nego ako ste odabrali samo jednu mogućnost sažimanja.

Na primjer, ako je projekt imao sljedeće retke procjene troškova.

| Zadatak | Kategorija | Datum | Količina | Jedinična cijena | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Zrakoplovne karte | 10. 1. 2020. | 4 | 400 | 1600 |
| Zadatak B | Hoteli | 10. 1. 2020. | 4 | 200 | 800 |
| Zadatak C | Hoteli | 11. 1. 2020. | 2 | 200 | 400 |

Kada korisnik odluči sažeti po klasi transakcije, uvest će se sljedeći podaci.

| Zadatak | Kategorija | Datum | Količina | Jedinična cijena | Iznos |
| --- | --- | --- | --- | --- | --- |
|||10. 1. 2020. | 3.34 | 840 | 2800 |

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
