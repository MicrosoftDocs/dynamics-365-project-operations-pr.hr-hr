---
title: Financijske procjene troškova na projektima
description: U ovoj temi nalaze se informacije o načinu definiranja ili procjene troškova koji se temelje na projektu.
author: rumant
manager: Annbe
ms.date: 03/19/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad4901b1264289f1da881154bc147fc3f8da698f
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701773"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Financijske procjene troškova na projektima
_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations omogućuje voditeljima projekata da definiraju troškove koji se temelje na projektu za svaki projekt ili zadatak. Svaka stavka troška može se povezati s određenim projektnim zadatkom. Rashodi su kategorizirani u različite kategorije troškova, koje su definirane na organizacijskoj razini. Cijene i troškovi za svaku kategoriju troškova definiraju se cjenikom. 

Poduzmite sljedeće korake za prikaz, dodavanje ili brisanje troška projekta.

1. Idite na mogućnost **Projekti** i odaberite projekt na kojem želite raditi.
2. Odaberite karticu **Procjene projekta** i pogledajte popis troškova projekta.
3. Odaberite **Novi trošak** kako biste dodali trošak. Ili odaberite trošak za brisanje, a zatim odaberite **Izbriši trošak**.

Tablica u nastavku pruža informacije o poljima na stavci **Redak procjene troška** u projektu. 

| **Polje** | **Opis** | **Utjecaj prema dolje** |
| --- | --- | --- |
| Zadatak | Popis projektnih zadataka. To uključuje zadatke sažetka i lisnog čvora. | Odabir zadatka za redak procjene troška utjecati će na procijenjenu cijenu troška i procijenjeni trošak prodaje za zadatak. Ako ovo polje ostane prazno, procjena troškova prati se i zbraja samo na razini projekta. |
| Kategorija | Popis kategorija transakcija koje su u aplikaciji povezale kategorije troškova. | Odabir kategorije pokreće određivanje cijene i troška u retku procjene troška. |
| Datum početka | Predviđeni datum nastanka troška. | Ovo polje ne utječe na niže razine. |
| Grupa jedinica | Zadana vrijednost u ovom polju proizlazi iz grupe jedinica koja je postavljena kao zadana na odabranoj kategoriji. Ovo polje možete ažurirati kako biste odabrali drugu grupu jedinica. | Ovo polje ne utječe na niže razine. |
| Jedinica | Vrijednost u ovom polju zadaje zadanu jedinicu odabrane kategorije. Ovo polje možete ažurirati kako biste odabrali drugu jedinicu. | Promjena jedinice rezultira drugačijom zadanom cijenom i troškom jedinice. |
| Količina | Količina procijenjenih troškova koje ćete imati. | Ovo polje ne utječe na niže razine. |
| Jedinična cijena | Trošak odabrane kombinacije kategorije i jedinice kako je postavljen u mjerodavnom troškovniku | Jedinični trošak uvijek se prikazuje u valuti troška projekta. |
| Jedinična cijena | Cijena odabrane kombinacije kategorije i jedinice kako je postavljena u mjerodavnom prodajnom cjeniku. | Jedinični cijena uvijek se prikazuje u valuti prodaje projekta. |
| Ukupni trošak | Iznos troška koji se izračunava kao količina \* jedinični trošak.| Iznos troška uvijek se prikazuje u valuti troška projekta. |
| Ukupne prodaje | Prodajni iznos koji se izračunava kao količina \* jedinična cijena. | Iznos prodaje uvijek se prikazuje u valuti prodaje projekta. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
