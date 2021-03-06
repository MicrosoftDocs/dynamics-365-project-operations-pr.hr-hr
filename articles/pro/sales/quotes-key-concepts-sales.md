---
title: Osnovni koncepti ponude projekta
description: U ovoj temi nalaze se informacije o načinu uporabe ponuda projekata u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64d2fd9bab9452d71e8cd194fbab70edadf00b93
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896272"
---
# <a name="project-quote-key-concepts"></a>Osnovni koncepti ponude projekta

_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_


Slijede ključni koncepti kojih morate biti svjesni prije nego što počnete upotrebljavati ponude projekata u aplikaciji Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Ugovorna jedinica

Ugovorna jedinica predstavlja odjel ili praksu koja je vlasnik isporuke projekta. Možete postaviti troškove resursa za svaku ugovornu jedinicu. Kada odredite cijenu resursa za resurs u ugovornoj jedinici, moći ćete postaviti različite cijene troškova za resurse kod kojih se ova ugovorna jedinica zadužuje ili drugi odjel ili prakse unutar poduzeća. Nazivaju se cijenama prijenosa, posuđivanjem resursa ili cijenama razmjene. Kada postavljate trošak posudbe resursa iz drugih odjela, možete odabrati i postavljanje tih cijena troškova u valuti odjela koji posuđuje.

## <a name="cost-currency"></a>Valuta troška

Valuta troška u aplikaciji Project Operations valuta je u kojoj se prijavljuju troškovi. Ta je valuta izvedena iz valute koja je pridružena polju **Ugovorna jedinica** na ponudi, ugovoru i projektu. Troškovi se mogu evidentirati u bilo kojoj valuti u odnosu na projekt. Međutim, postoji konverzija valute iz valute u kojoj su zabilježeni troškovi u valutu troškova iz projekta.

Budući da tečajevi na platformi CDS ne mogu biti datumski učinkoviti, ukupni troškovi na zaslonu mogu se s vremenom promijeniti ako ažurirate tečajeve valuta. Međutim, troškovi zabilježeni u bazi ostaju nepromijenjeni jer se iznosi pohranjuju u valuti u kojoj su nastali.

## <a name="sales-currency"></a>Valuta prodaje

Valuta prodaje u aplikaciji Project Operations valuta je u kojoj se bilježe i prikazuju procijenjeni i stvarni iznosi prodaje. To je također valuta u kojoj se klijentu fakturira ugovoreni posao. Na ponudi projekta, valuta prodaje zadana je iz zapisa klijenta ili računa i može se mijenjati kada se stvori cijena. Nakon spremanja ponude, valuta prodaje ne može se mijenjati. Cjenici proizvoda i projekata zadani su na temelju valute prodaje iz ponude.

Za razliku od troškova, vrijednosti prodaje mogu se evidentirati samo u valuti prodaje.

## <a name="billing-method"></a>Način naplate

Projekti obično imaju fiksne modele ugovaranja na temelju naknada i potrošnje. To je u aplikaciji Project Operations predstavljeno kao **Način naplate** i ima dvije vrijednosti, vrijeme i materijal te fiksnu cijenu.

- **Vrijeme i materijal:** Ovo je model ugovora koji se temelji na potrošnji u kojem je svaki nastali trošak poduprt odgovarajućim prihodom. Kako procijenite ili napravite više troškova, odgovarajuća procijenjena i stvarna prodaja također će se povećati. U redcima ponude koji imaju ovaj način naplate možete odrediti ograničenja koja ne smiju premašiti. Ovo će ograničiti stvarni prihod. Ograničenja koja ne smiju premašiti ne utječu na procijenjeni prihod.
- **Fiksna cijena:** Ovo je model ugovora s fiksnom naknadom koji ukazuje da će prodajne vrijednosti biti neovisne o nastalim troškovima. Prodajna je vrijednost fiksna i ne mijenja se kako procijenite ili napravite više troškova.

## <a name="project-price-lists"></a>Cjenici projekta

Cjenici projekata su cjenici koji se upotrebljavaju za zadane cijene, a ne cijene troška, za vrijeme, trošak i ostale komponente povezane s projektom. Cjenika može biti više, a svaki popis može imati svoj datum stupanja na snagu za svaku ponudu projekta. Project Operations ne podržava preklapanje datuma stupanja na snagu cjenika projekata.

## <a name="product-price-lists"></a>Cjenici proizvoda

Cjenici proizvoda su cjenici koji se upotrebljavaju za zadane cijene, a ne za cijene troškova, za retke ponude koji se temelje na proizvodima. Postoji samo jedan cjenik proizvoda po ponudi.

## <a name="transaction-classes"></a>Klase transakcija

Project Operations podržava četiri vrste klasa transakcija:

- Vrijeme
- Izdatak
- Materijal
- Naknada

Vrijednosti troška i prodaje mogu se procijeniti i nastati za klase transakcija Vrijeme, Trošak i Materijal. Naknada je klasa transakcija koja je samo prihod.

## <a name="work-entities-and-billing-entities"></a>Entiteti rada i naplate

Entiteti koji predstavljaju rad su projekti i zadaci. Entiteti koji predstavljaju naplatu su redci ponude i ugovora. Razne entitete rada možete povezati s mogućnostima naplate tako da ih povežete s redcima ponude ili ugovora.

## <a name="multi-customer-deals"></a>Poslovi s više klijenata

Poslovi s više klijenata događaju se kada postoji više klijenata kojima se fakturira. Uobičajeni primjeri ovoga uključuju sljedeće:

- **OEM poduzeća i njihovi partneri:** Partneri i maloprodaje prodaju proizvod s uslugama dodatne vrijednosti. To je obično scenarij u kojem tijekom određenog posla s klijentom OEM nudi financiranje dijela projekta. 

- **Projekti javnog sektora:** Više odjela lokalne samouprave pristaje financirati projekt i fakturira im se prema prethodno dogovorenoj raspodjeli. Na primjer, školski okrug i gradska uprava ili odjel lokalne uprave dogovore se financirati izgradnju bazena.

## <a name="invoice-schedules"></a>Rasporedi fakturiranja

Rasporedi faktura specifični su za svaki redak ponude i također nisu obavezni. Rasporedi faktura izrađuju se na temelju određenih datuma početka i završetka te učestalosti faktura. Rasporedi faktura upotrebljavaju se u fazi ugovora kada je konfiguriran automatski postupak stvaranja fakture. U fazi ponude rasporedi su neobavezni. Kada se rasporedi faktura stvaraju u fazi **Ponude** kopiraju se u ugovor o projektu koji se stvara kada se prihvati ponuda projekta.

## <a name="changes-from-dynamics-365-sales-quote"></a>Promjene iz ponude u aplikaciji Dynamics 365 Sales:

Ponude iz aplikacije Project Operations grade se na ponudama iz aplikacije Dynamics 365 Sales. Međutim, postoje neke važne razlike u funkcionalnosti koje biste trebali znati:

- Radnje **Revidiraj** i **Aktiviraj** nisu podržane.
- Ponude iz aplikacije Project Operations imaju dvije različite vrste redaka. Jedni su za projekte, a druga za proizvode.
- Ponude iz aplikacije Project Operations imaju vlastiti obrazac i elemente korisničkog sučelja, poslovna pravila, poslovnu logiku u dodacima i skripte na strani klijenta što ih čini jedinstvenima u prodajnim ponudama.

Iz tih razloga nije preporučljivo naizmjenično upotrebljavati ponude iz aplikacija Sales i Project Operations.
