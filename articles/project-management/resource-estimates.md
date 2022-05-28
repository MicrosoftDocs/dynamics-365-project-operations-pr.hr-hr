---
title: Financijske procjene vremena resursa na projektima
description: U ovoj temi nalaze se informacije o načinu izračunavanja financijskih procjena vremena.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: aab5c11a7dc23331c935403a4f96ec7197ec1572
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592545"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Financijske procjene vremena resursa na projektima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Financijske procjene vremena izračunavaju se na temelju tri čimbenika: 

- Vrsta generičkog ili imenovanog člana tima dodijeljenog svakom zadatku lisnog čvora na projektnom planu. 
- Vrsta ili složenost posla.
- Širenje napora za dodjelu resursa na zadatak. 

Prva dva čimbenika utječu na jedinični trošak ili cijenu za naplatu dodjele resursa. Jedinični trošak ili cijena naplate dodjele resursa određuje se atributima dodijeljenog resursa. Ti atributi obuhvaćaju organizacijsku jedinicu kojoj resurs pripada i uobičajenu ulogu resursa. Resursu možete dodati i prilagođene atribute relevantne za vaše poslovanje, poput uobičajenog naslova ili razine iskustva i omogućiti mu da utječe na jedinični trošak ili cijenu za naplatu dodjele.
Osim atributa resursa, atributi rada, poput zadatka, mogu također utjecati na jediničnu cijenu za naplatu ili cijenu koštanja dodjele. Na primjer, kada su određeni zadaci složeniji, dodjela resursa tim specifičnim zadacima dovodi do većeg jediničnog troška ili cijene za naplatu nego što je to slučaj kod manje složenih zadataka.   

Treći čimbenik daje količinu sati po toj cijeni. U slučajevima kada se zadatak proteže na dva cjenovna razdoblja, vjerojatno će se obračun troškova i određivanje cijene za prvi dio dodjele resursa za taj zadatak vršiti drugačije nego za drugi dio zadatka. Procjena rada za svaku dodjelu resursa složena je vrijednost pohranjena s dnevnom raspodjelom rada po danu.

Podrobne upute o načinu postavljanja prilagođenih atributa rada i resursa kao veličina za određivanje cijene i troškova potražite u odjeljku [Pregled veličina za određivanje cijena](../pricing-costing/pricing-dimensions-overview.md).

Financijska procjena za svaku dodjelu resursa izračunava se kao **cijena/sat za zadatak pomnožena s brojem sati.**  Slično procjeni rada, financijska procjena troška i prihoda za svaku dodjelu resursa složena je vrijednost pohranjena s dnevnom raspodjelom novčanog iznosa po danu. 

## <a name="summarizing-financial-estimates-for-time"></a>Zbrajanje financijske procjene za vrijeme
Financijska procjena vremena na zadatku lisnog čvora zbroj je financijskih procjena svih dodjela resursa za taj zadatak.

Financijska procjena vremena na sažetku ili nadređenom zadatku zbroj je financijskih procjena njegovih podređenih zadataka. Ovo je procijenjeni trošak rada na projektu. 

![Procjene resursa.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Zadana cijena koštanja i valuta troška

Zadana cijena koštanja proizlazi iz cjenika koji su priloženi ugovornoj jedinici projekta. Valuta troška projekta uvijek je valuta ugovorne jedinice projekta. Pri dodjeli resursa, financijska procjena troška pohranjuje se u valuti troška projekta. Ponekad se valuta u kojoj je cijena koštanja postavljena u cjeniku razlikuje od valute troška projekta. U tim slučajevima aplikacija pretvara valutu u kojoj je postavljena cijena koštanja u valutu projekta. Sve procjene troškova na rešetki **Procjene** prikazuju se i zbrajaju u valuti troška projekta. 

## <a name="default-bill-rate-and-sales-currency"></a>Zadane cijena naplate i valute prodaje

Zadana prodajna cijena proizlazi iz cjenika projekta koji su priloženi uz povezani ugovor o projektu ako je posao dobiven ili iz povezane ponude projekta ako je posao još uvijek u fazi pretprodaje. Valuta prodaje projekta uvijek je valuta ponude projekta ili ugovorne o projektu. Pri dodjeli resursa, financijska procjena za prodaju pohranjuje se u valuti za prodaju projekta. Za razliku od troška, prodajna cijena koja je postavljena u cjeniku nikada se ne može razlikovati od valute za prodaju projekta. Ne postoji scenarij u kojem je potrebno pretvaranje valuta. Sve procjene prodaje na rešetki **Procjene** prikazuju se i zbrajaju u valuti za prodaju projekta. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
