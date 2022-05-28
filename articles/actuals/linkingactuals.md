---
title: Podrijetlo transakcije - Povežite stvarne podatke s njihovim izvorom
description: Ova tema objašnjava kako se koncept podrijetla transakcije koristi za povezivanje stvarnih vrijednosti s izvornim izvornim zapisima, kao što su stavka vremena, stavka troškova ili zapisnici o korištenju materijala.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 908f78f7d58ec4b18f37d03b6fa7c4e2295491fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584817"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Podrijetlo transakcije - Povežite stvarne podatke s njihovim izvorom

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Zapisi o podrijetlu transakcije kreiraju se da bi povezali stvarne podatke s njihovim izvorom, kao što su stavke vremena, stavke troškova, zapisnici korištenja materijala i fakture projekta.

Sljedeći primjer prikazuje tipičnu obradu unosa vremena u životnom ciklusu projekta sustava Project Operations.

> ![Obrada vremenskih cjelina u projektnim operacijama.](media/basic-guide-17.png)
 
1. Slanje stavke vremena uzrokuje kreiranje dva retka temeljnice: jedan za trošak i jedan za nenaplaćenu prodaju.
2. Eventualno odobravanje unosa vremena uzrokuje stvaranje dvije stvarne vrijednosti: jednu za trošak i jednu za nenaplaćenu prodaju.
3. Kada korisnik izradi projektnu fakturu, transakcija retka fakture izrađuje se s pomoću podataka iz nenaplaćenih prodajnih stvarnih podataka.
4. Kada je faktura potvrđena, stvaraju se dva nova stvarna podatka: nenaplaćena stornirana prodaja i fakturirani prodajni stvarni podatak.

Svaki događaj u ovom tijeku rada obrade pokreće stvaranje zapisa u entitetu Porijeklo transakcije kako bi pomogao u stvaranju praćenja Odnosi između tih zapisa koji se kreiraju kroz stavku vremena, redak temeljnice, stvarne detalje i detalje retka fakture.

Sljedeća tablica prikazuje zapise u entitetu Porijeklo transakcije za prethodni tijek rada.

| Događaj                        | Porijeklo                   | Vrsta porijekla                       | Transakcija                       | Vrsta transakcije         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Slanje unosa vremena        | GUID zapis unosa vremena   | Unos vremena                        | GUID zapis retka u dnevniku (trošak)   | Redak u dnevniku             |
| GUID zapis unosa vremena       | Unos vremena               | GUID zapis retka u dnevniku (prodaja)  | Redak u dnevniku                      |                          |
| Odobrenje vremena                | GUID zapis retka u dnevniku | Redak u dnevniku                      | GUID zapis nenaplaćene prodaje        | Stvarna vrijednost                   |
| GUID zapis unosa vremena       | Unos vremena               | GUID zapis nenaplaćene prodaje        | Stvarna vrijednost                            |                          |
| GUID zapis retka u dnevniku     | Redak u dnevniku             | GUID zapis stvarne vrijednosti troškova           | Stvarna vrijednost                            |                          |
| GUID zapis unosa vremena       | Unos vremena               | GUID zapis stvarne vrijednosti troškova           | Stvarna vrijednost                            |                          |
| Izrada fakture             | GUID zapis unosa vremena   | Unos vremena                        | GUID transakcija retka fakture     | Transakcija retka fakture |
| GUID zapis retka u dnevniku     | Redak u dnevniku             | GUID transakcija retka fakture     | Transakcija retka fakture          |                          |
| Potvrda fakture         | GUID redak fakture        | Redak fakture                      | GUID zapis naplaćene prodaje          | Stvarni posao                   |
| GUID faktura                 | Faktura                  | GUID zapis naplaćene prodaje          | Stvarni posao                            |                          |
| GUID detalji retka fakture     | Pojedinost retka fakture      | GUID zapis naplaćene prodaje          | Stvarni posao                            |                          |
| GUID zapis unosa vremena       | Unos vremena               | GUID zapis naplaćene prodaje          | Stvarni posao                            |                          |
| GUID zapis retka u dnevniku     | Redak u dnevniku             | GUID zapis naplaćene prodaje          | Stvarni posao                            |                          |
| GUID zapis unosa vremena       | Unos vremena               | GUID povrat nenaplaćene prodaje      | Stvarni posao                            |                          |
| GUID zapis retka u dnevniku     | Redak u dnevniku             | GUID povrat nenaplaćene prodaje      | Stvarni posao                            |                          |
| Nacrt ispravka fakture     | Stari ILD GUID             | Transakcija retka fakture          | Ispravak ILD GUID               | Transakcija retka fakture |
| Stari IL GUID                  | Redak fakture             | Ispravak ILD GUID               | Transakcija retka fakture          |                          |
| Stara GUID faktura             | Faktura                  | Ispravak ILD GUID               | Transakcija retka fakture          |                          |
| GUID zapis unosa vremena       | Unos vremena               | Ispravak ILD GUID               | Transakcija retka fakture          |                          |
| GUID zapis retka u dnevniku     | Redak u dnevniku             | Ispravak ILD GUID               | Transakcija retka fakture          |                          |
| Potvrđeni ispravak fakture | Stari ILD GUID             | Transakcija retka fakture          | GUID stvarni podaci povrata naplaćene prodaje | Stvarni posao                   |
| Stari IL GUID                  | Redak fakture             | GUID stvarni podaci povrata naplaćene prodaje | Stvarni posao                            |                          |
| Stara GUID faktura             | Faktura                  | GUID stvarni podaci povrata naplaćene prodaje | Stvarni posao                            |                          |
| GUID zapis unosa vremena       | Unos vremena               | GUID stvarni podaci povrata naplaćene prodaje | Stvarni posao                            |                          |
| GUID zapis retka u dnevniku     | Redak u dnevniku             | GUID stvarni podaci povrata naplaćene prodaje | Stvarni posao                            |                          |
| Stari ILD GUID                 | Transakcija retka fakture | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarni posao                            |                          |
| Stari IL GUID                  | Redak fakture             | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarni posao                            |                          |
| Stara GUID faktura             | Faktura                  | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarni posao                            |                          |
| GUID zapis unosa vremena       | Unos vremena               | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarni posao                            |                          |
| GUID zapis retka u dnevniku     | Redak u dnevniku             | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarni posao                            |                          |
| Ispravak ILD GUID          | Transakcija retka fakture | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarni posao                            |                          |
| Ispravak IL GUID           | Redak fakture             | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarni posao                            |                          |
| Ispravak GUID faktura      | Faktura                  | Novi GUID stvarni podaci nenaplaćene prodaje    | Stvarno                            |                          |


Sljedeća ilustracija prikazuje veze koje se stvaraju između stvarnih i njihovih izvora na različitim događajima na primjeru unosa vremena u operacijama projekta.

> ![Kako su stvarne stvari povezane s izvornim zapisima u operacijama projekta.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
