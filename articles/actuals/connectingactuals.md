---
title: Veze transakcije – Povežite stvarne podatke različitih vrsta transakcija
description: U ovom se članku objašnjava kako se veza transakcije koristi za povezivanje stvarnih podataka različitih vrsta kako bi se lakše pratilo profitabilnost, zaostatke u naplati i izračune naplaćenog i nenaplaćenog prihoda.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926077"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Veze transakcije – Povežite stvarne podatke različitih vrsta transakcija

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Zapisi veze transakcije izrađuju se za povezivanje stvarnih podataka različitih vrsta kako se vrijeme, trošak ili potrošnja materijala kreću u svom životnom ciklusu od faze ponude ili pretprodaje do faze ugovora, odobrenja i/ili opoziva, fakturiranja i potencijalno kreditno ili korektivno fakturiranje.

Sljedeći primjer prikazuje tipičnu obradu unosa vremena u životnom ciklusu projekta sustava Project Operations.

> ![Obrada unosa vremena u aplikaciji Project Operations.](media/basic-guide-17.png)

Obrada unosa vremena u životnom ciklusu projekta aplikacije Project Operations slijedi ove korake: 

1. Slanje unosa vremena uzrokuje izradu dvaju redaka u dnevniku: jedan za trošak i jedan za nenaplaćene prodaje. 
2. Eventualno odobrenje unosa vremena uzrokuje izradu dvaju stvarnih podataka: jedan za trošak i jedan za nenaplaćene prodaje. Ta dva stvarna podatka povezana su vezama transakcije.
3. Kada korisnik izradi projektnu fakturu, transakcija retka fakture izrađuje se s pomoću podataka iz nenaplaćenih prodajnih stvarnih podataka.
4. Kada se faktura potvrdi, izrađuju se dva nova stvarna podatka: stvarni podatak storniranja nenaplaćene prodaje i stvarni podatak naplaćene prodaje. Stvarni podatak storniranja nenaplaćene prodaje i stvarni podatak izvorne nenaplaćene prodaje povezani su putem veza transakcije storniranja. Stvarni podatak naplaćene prodaje i stvarni podatak izvorne nenaplaćene prodaje povezani su i kako bi se prikazale veze između prihoda koji se prethodno vodio kao zaostali odnosno kao prihod za djelomično izvršeni posao (WIP, work in progress) i prihoda koji se sada vodi kao naplaćeni prihod.   

Svaki događaj u tijeku rada obrade pokreće izradu zapisa u tablici **Veza transakcije**. Time se olakšava izrada praćenja odnosa između zapisa izrađenih preko vremenskog unosa, retka dnevnika, stvarnog podatka i pojedinostima retka fakture.

U tablici u nastavku prikazani su zapisi u entitetu **Veza transakcije** za prethodni tijek rada.

|Događaj                   |Transakcija 1                 |Uloga transakcije 1 |Vrsta transakcije 1       |Transakcija 2          |Uloga transakcije 2 |Vrsta transakcije 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Slanje unosa vremena   |redak u dnevniku (prodaja) GUID     |Nenaplaćena prodaja |msdyn_journalline            |Redak u dnevniku (trošak) GUID     |Trošak            |msdyn_journalline  |
|Odobrenje vremena           |Nenaplaćeni stvarni podaci (prodaja) GUID  |Nenaplaćena prodaja |msdyn_actual                 |Stvarni podaci troška(trošak) GUID       |Trošak            |msdyn_actual       |
|Izrada fakture        |GUID detalji retka fakture      |Naplaćena prodaja   |msdyn_invoicelinetransaction |Nenaplaćena prodaja stvarni podaci GUID   |Nenaplaćena prodaja  |msdyn_actual       |
|Potvrda fakture    |Storniranje stvarnih podataka GUID         |Storniranje      |msdyn_actual                 |Izvorna nenaplaćena prodaja GUID |Izvorna        |msdyn_actual       |
|                        |Naplaćena prodaja GUID             |Naplaćena prodaja   |msdyn_actual                 |Nenaplaćena prodaja stvarni podaci GUID   |Nenaplaćena prodaja  |msdyn_actual       |
|Nacrt ispravka fakture |GUID transakcija retka fakture|Zamjena      |msdyn_invoicelinetransaction |Naplaćena prodaja GUID            |Izvorna        |msdyn_actual       |
|Potvrdi ispravak fakture|Storniranje naplaćene prodaje GUID  |Storniranje      |msdyn_actual                 |Naplaćena prodaja GUID            |Izvorna        |msdyn_actual       |
|                        |Nova nenaplaćena prodaja GUID |Zamjena            |msdyn_actual                 |Naplaćena prodaja GUID            |Izvorna        |msdyn_actual       |


Na ilustraciji u nastavku prikazane su veze koje se izrađuju između različitih vrsta stvarnih podataka u okviru različitih događaja na primjeru unosa vremena u aplikaciji Project Operations.

> ![Način međusobnog povezivanja različitih vrsta stvarnih podataka u aplikaciji Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
