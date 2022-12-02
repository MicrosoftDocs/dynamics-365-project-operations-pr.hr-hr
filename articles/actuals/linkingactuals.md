---
title: Porijeklo transakcije – Povežite stvarne podatke s njihovim izvorom
description: U ovom se članku objašnjava kako se koncept porijekla transakcije upotrebljava za povezivanje stvarnih podataka s izvornim zapisima, poput unosa vremena, unosa troškova ili zapisnika o uporabi materijala.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921293"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Porijeklo transakcije – Povežite stvarne podatke s njihovim izvorom

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Zapisi o porijeklu transakcije izrađuju se za povezivanje stvarnih podataka s njihovim izvorom, kao što su unosi vremena, unosi troškova, zapisnici upotrebe materijala i fakture za projekte.

Sljedeći primjer prikazuje tipičnu obradu unosa vremena u životnom ciklusu projekta sustava Project Operations.

> ![Obrada unosa vremena u aplikaciji Project Operations.](media/basic-guide-17.png)
 
1. Slanje unosa vremena uzrokuje izradu dvaju redaka u dnevniku: jedan za trošak i jedan za nenaplaćene prodaje.
2. Eventualno odobrenje unosa vremena uzrokuje izradu dvaju stvarnih podataka: jedan za trošak i jedan za nenaplaćene prodaje.
3. Kada korisnik izradi projektnu fakturu, transakcija retka fakture izrađuje se s pomoću podataka iz nenaplaćenih prodajnih stvarnih podataka.
4. Kada je faktura potvrđena, stvaraju se dva nova stvarna podatka: nenaplaćena stornirana prodaja i fakturirani prodajni stvarni podatak.

Svaki događaj u tom tijeku rada obrade pokreće izradu zapisa u entitetima Porijeklo transakcije kako bi se pomoglo izgraditi trag odnosa između tih zapisa koji su izrađeni u unosu vremena, retku u dnevniku, stvarnim podacima i pojedinostima retka fakture.

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


Sljedeća ilustracija prikazuje veze koje se izrađuju između stvarnih podataka i njihovih izvora u okviru različitih događaja na primjeru unosa vremena u aplikaciji Project Operations.

> ![Način na koji su stvarni podaci povezuju s izvornim zapisima u aplikaciji Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
