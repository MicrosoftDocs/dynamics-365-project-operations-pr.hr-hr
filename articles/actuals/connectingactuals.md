---
title: Transakcijske veze – povezivanje stvarnih vrijednosti različitih vrsta transakcija
description: Ova tema objašnjava kako se transakcijska veza koristi za povezivanje stvarnih vrijednosti različitih vrsta kako bi se pomoglo u praćenju profitabilnosti, zaostataka u naplati i naplaćenih u odnosu na nenaplaćene izračune prihoda.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2e8d75a69e27619e6a21f0fe61e2c656e94017b0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580769"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Transakcijske veze – povezivanje stvarnih vrijednosti različitih vrsta transakcija

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Zapisi o transakcijskoj vezi kreiraju se kako bi povezali stvarne vrijednosti različitih vrsta kao vrijeme, trošak ili korištenje materijala kreće se u njegovom životnom ciklusu od faze ponude ili predprodaje do faze ugovora, odobrenja i/ili opoziva, fakturiranja i potencijalno kreditnog ili korektivnog fakturiranja.

Sljedeći primjer prikazuje tipičnu obradu unosa vremena u životnom ciklusu projekta sustava Project Operations.

> ![Obrada stavki vremena u operacijama projekta.](media/basic-guide-17.png)

Obrada unosa vremena u životnom ciklusu projekta Project Operations slijedi ove korake: 

1. Slanje stavke vremena uzrokuje kreiranje dva retka temeljnice: jedan za trošak i jedan za nenaplaćenu prodaju. 
2. Eventualno odobravanje unosa vremena uzrokuje stvaranje dvije stvarne vrijednosti: jednu za trošak i jednu za nenaplaćenu prodaju. Ove dvije stvarne vrijednosti povezane su pomoću transakcijskih veza.
3. Kada korisnik izradi projektnu fakturu, transakcija retka fakture izrađuje se s pomoću podataka iz nenaplaćenih prodajnih stvarnih podataka.
4. Kada je faktura potvrđena, to stvara dvije nove stvarne vrijednosti: neplaćeni storniranje prodaje i stvarnu prodaju naplaćenu prodaju. Neplaćeni preokret prodaje i izvorni neplaćeni iznos prodaje povezani su pomoću storniranja transakcijskih veza. Naplaćena prodaja i izvorne neplaćene prodajne stvarne vrijednosti također su povezane kako bi se prikazale veze između nekadašnjih zaostataka ili prihoda od rada u tijeku (PUT) s onim što se sada naplaćuje prihod.   

Svaki događaj u tijeku rada obrade pokreće stvaranje zapisa u tablici Povezivanje s **transakcijom**. To pomaže u stvaranju praćenja Odnosi između zapisa kreiranih kroz stavku vremena, retka temeljnice, stvarnih detalja i detalja retka fakture.

Sljedeća tablica prikazuje zapise u entitetu transakcijske **veze** za prethodni tijek rada.

|Događaj                   |Transakcija 1                 |Uloga transakcije 1 |Vrsta transakcije 1       |Transakcija 2          |Uloga transakcije 2 |Vrsta transakcije 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Slanje unosa vremena   |redak u dnevniku (prodaja) GUID     |Nenaplaćena prodaja |msdyn_journalline            |Redak u dnevniku (trošak) GUID     |Trošak            |msdyn_journalline  |
|Odobrenje vremena           |Nenaplaćeni stvarni podaci (prodaja) GUID  |Nenaplaćena prodaja |msdyn_actual                 |Stvarni podaci troška(trošak) GUID       |Trošak            |msdyn_actual       |
|Izrada fakture        |GUID detalji retka fakture      |Naplaćena prodaja   |msdyn_invoicelinetransaction |Nenaplaćena prodaja stvarni podaci GUID   |Nenaplaćena prodaja  |msdyn_actual       |
|Potvrda fakture    |Storniranje stvarnih podataka GUID         |Storniranje      |msdyn_actual                 |Izvorna nenaplaćena prodaja GUID |Izvorna        |msdyn_actual       |
|                        |Naplaćena prodaja GUID             |Naplaćena prodaja   |msdyn_actual                 |Nenaplaćena prodaja stvarni podaci GUID   |Nenaplaćena prodaja  |msdyn_actual       |
|Nacrt ispravka fakture |GUID transakcija retka fakture|Zamjena      |msdyn_invoicelinetransaction |Naplaćena prodaja GUID            |Izvorna        |msdyn_actual       |
|Potvrdi ispravak fakture|Storniranje naplaćene prodaje GUID  |Storniranje      |msdyn_actual                 |Naplaćena prodaja GUID            |Izvorna        |msdyn_actual       |
|                        |Novi neisplaćeni GUID prodaje |Zamjena            |msdyn_actual                 |Naplaćena prodaja GUID            |Izvorna        |msdyn_actual       |


Sljedeća ilustracija prikazuje veze koje se stvaraju između različitih vrsta stvarnih vrijednosti na različitim događajima na primjeru unosa vremena u operacijama projekta.

> ![Kako su stvarne vrijednosti različitih vrsta međusobno povezane u projektnim operacijama.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
