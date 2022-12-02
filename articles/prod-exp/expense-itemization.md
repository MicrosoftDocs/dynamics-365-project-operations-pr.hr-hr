---
title: Organizacija troškova
description: U ovom se članku objašnjava kako specificirati troškove koristeći se novodizajniranim radnim prostorom Expense.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920925"
---
# <a name="expense-itemization"></a>Organizacija troškova

[!include [banner](../includes/banner.md)]

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Organizacije često zahtijevaju od zaposlenika da podnesu detaljnu raščlambu troškova nastalih tijekom putovanja. Na primjer, račun hotela može sadržavati nekoliko redaka s pojedinostima za cijenu sobe, porez, parkiranje i druge razne troškove nastale svakog dana tijekom boravka. Moguće je i da se za trošak obroka mora navesti preciznija raščlamba za doručak, ručak ili večeru. Bez obzira na potrebe organizacije, svaka kategorija troškova može se postaviti tako da odražava potkategorije ili stavke retka koje čine trošak. Iako je specificiranje uvijek bilo podržano u **Upravljanje troškovima**, **novodizajnirani radni prostor troška** omogućuje učinkovitiju specificiranje kada je značajka **Mogućnost brzog specificiranja ponavljajućih troškova** omogućena.  

## <a name="enable-quick-itemization"></a>Omogućivanje brzog specificiranja 

Značajku **Mogućnost brzog specificiranja ponavljajućih troškova** možete upotrijebiti da biste brzo specificirali ponavljajuće troškove bez da morate unositi dnevne troškove svaki put tijekom boravka. Poduzmite sljedeće korake da biste omogućili brzo specificiranje.

1. Idite na radni prostor **Upravljanje značajkama** i na popisu značajki pronađite i odaberite **Ponovno osmišljena izvješća o troškovima**. 
2. Odaberite **Omogući odmah**. 
3. Na popisu značajki pronađite i odaberite **Mogućnost brzog specificiranja ponavljajućih troškova**.
4. Odaberite **Omogući odmah**. 

## <a name="itemization-grid"></a>Rešetka za specificiranje 

Ako kategorija troškova ima potkategorije ili različite komponente koje čine taj trošak, može se specificirati. Da biste specificirali trošak, odaberite redak troška u izvješću o trošku te u oknu **Pojedinosti troška** odaberite **Radnje** > **Specificiraj**. Klizač **Specificiranje** otkriva rešetku s poljima. U sljedećoj tablici navodi se primjer svakog polja u rešetki i načina na koji se polje prikazuje u izvješću o troškovima. 

|     Polje          |     Opis                                                                                  |     Primjer              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Potkategorija    |     Popis potkategorija konfiguriranih pod vrstom kategorije troškova **Hotel**.             |     Dnevna cijena sobe      |
|     Datum početka     |     Datum kada je stavka troška prvi put nastala.                                           |     13. 9. 2021.           |
|     Dnevna stopa     |     Iznos koji je nastao za stavku troška.                                                    |     200                  |
|     Količina       |     Broj ponavljanja troška tijekom kontinuiranog razdoblja.                       |     3                    |

![Specificiraj trošak.](media/Itemization%20screen%201.png)

Kada spremite specifikaciju, vidjet ćete pojedinačni specificiran redak za količinu navedenu u rešetki za specificiranje. Svaki redak počinje na datum koji je naveden u mreži.

![Izvješće sa specifikacijama](media/Itemization%20screen%202.png)

