---
title: Redci podugovora za kategorije troška
description: U ovom se članku objašnjava kako zabilježiti retke kooperacije za trošak i pomoću polja zabilježiti nabavu vremena od dobavljača.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7166642abc2187a53f7019639df6f0d7124f4765
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261831"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Redci podugovora za kategorije troška

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Podugovor u aplikaciji Dynamics 365 Project Operations može imati redak za kategorije troška. Redci podugovora za kategorije troška omogućuju voditelju projekta da od dobavljača kupi kategorije usluga ili proizvoda koje mogu naplatiti projektu.

Kako biste stvorili redak podugovora za kategorije troška u aplikaciji Project Operations, poduzmite sljedeće korake.

1. U navigacijskom oknu odaberite **Podugovori** i otvorite podugovor na kojem želite raditi.
2. Na kartici **Retci podugovora** odaberite **Novi** kako biste stvorili novi redak.
3. Na stranici **Brzo stvaranje**, u polju **Klasa transakcije**, odaberite **Trošak** i unesite ili odaberite odaberite neki drugi obvezni podatak o polju.

U tablici u nastavku nalaze se podaci o poljima na stranici s pojedinostima **Redak podugovora** i stranici **Brzo stvaranje**.

| **Polje** | **Opis** | **Funkcionalni utjecaj** |
| --- | --- | --- |
| Ime/naziv | Naziv retka podugovora za pomoć pri identifikaciji. | To će se prikazati kao prvi stupac u svim pretraživanjima koja se temelje na redcima podugovara. |
| Opis | Kratak opis kategorija troškova koje se nabavljaju na retku podugovora. | Nijedno |
|Vrsta retka | Ovo polje ima zadanu vrijednost stavke **Na temelju količine**. |Nijedno |
| Način naplate | Ovo je skup mogućnosti koji predstavlja dva glavna modela ugovaranja podržana aplikacijom Project Operations: **Fiksna cijena** i **Vrijeme i materijal**. | Raspored faktura koji se temelji na kontrolnim točkama dostupan je za retke podugovora ako je odabran način naplate s fiksnom cijenom. |
| Razred transakcije | Ovo polje ima zadanu vrijednost stavke **Vrijeme**. Za stvaranje redaka podugovora za kupnju proizvoda, polje **Klasa transakcije** postavite na **Trošak**.  | To ukazuje da se redak podugovora upotrebljava za evidentiranje kupnje kategorije troškova koji će se upotrebljavati za projekte. |
| Kategorija transakcije | Prikazuje popis aktivnih kategorija transakcija u sustavu. |Nijedno |
| Zatraženi početak | Unesite datum kada dobavljač mora omogućiti dostupnost kategorija za nabavu. | Traženi početak upotrebljava se za odabir cjenika projekta iz cjenika projekta priloženog podugovoru. Trošak kategorije na retku podugovora dolazi iz tog cjenika. |
| Traženi završetak | Unesite datum kada kategorije nabave više neće biti potrebne. | To će se upotrebljavati za prikaz upozorenja kada voditelj projekta povezuje taj redak podugovora s određenim procjenama troškova na projektu koji su potrebni nakon tog datuma. |
| Naručena količina | Količina kategorije koja se nabavlja od dobavljača. | To će se upotrebljavati za prikaz upozorenja kada voditelj projekta previše crpi tu količinu.|
| Grupa jedinica | Zadana vrijednost temelji se na zadanoj grupi jedinica postavljenoj za odabranu kategoriju. |Nijedno |
| Jedinica | Zadana vrijednost temelji se na zadanoj jedinici postavljenoj za odabranu kategoriju.  | Kombinacija **Kategorija** i **Jedinica** upotrebljavat će se kao zadana vrijednost ili će se izračunati za jediničnu cijenu retka podugovora.  |
| Jedinična cijena | Zadana vrijednost upotrebljava kombinaciju **Kategorija** i **Jedinica** iz cijena kategorije povezanih s cjenikom za projekt, koji se primjenjuje za traženi početak retka podugovora. |Nijedno |
| Podzbroj | Ovo je polje samo za čitanje koje se izračunava kao Količina X Jedinična cijena, ako se unesu vrijednosti i količine i jedinične cijene. Ako su jedno ili oba polja prazna, možete unijeti vrijednost u ovo polje. |Nijedno |
| Porez na promet | Unesite iznos poreza na prodaju. |Nijedno |
| Ukupni iznos | Ukupni iznos retka podugovora, uključujući porez. Ovo polje izračunava se kao međuzbroj + porez na promet. |Nijedno |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
