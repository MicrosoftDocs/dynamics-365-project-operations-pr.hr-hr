---
title: Osnovni koncepti ugovora o projektu
description: U ovoj temi nalaze se informacije o osnovnim konceptima ugovora o projektima.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 66d6b72b19a90ecc9161cd16ce9d4dd22798803b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073294"
---
# <a name="key-concepts-of-project-contracts"></a>Osnovni koncepti ugovora o projektu

_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_

U ovoj temi nalaze se osnovni koncepti kojih morate biti svjesni prije nego što počnete upotrebljavati ugovore o projektima u aplikaciji Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Ugovorena jedinica

Ugovorna jedinica predstavlja odjel ili praksu koja je vlasnik isporuke projekta. Možete postaviti troškove resursa za svaku ugovornu jedinicu. Kada resursu odredite cijenu, moći ćete postaviti i različite cijene troška za resurse. Ova ugovorna jedinica posuđuje ove resurse od drugih sektora ili praksi unutar poduzeća. Cijene troška resursa nazivaju se cijenama prijenosa, posuđivanjem resursa ili cijenama razmjene. Kada postavljate cijene troška za posudbu resursa iz drugih sektora, upotrijebite valutu sektora koji posuđuje.

## <a name="cost-currency"></a>Valuta troška

Valuta troška valuta je u kojoj se prijavljuju troškovi na zaslonu. Ta je valuta izvedena iz valute koja je priložena polju **Ugovorna jedinica** na ugovoru i projektu. Troškovi se mogu evidentirati u bilo kojoj valuti u odnosu na projekt. Međutim, postoji konverzija valute iz valute u kojoj su zabilježeni troškovi u valutu troškova iz projekta u kojem se prikazuju na zaslonu.

Budući da tečajevi na platformi Common Data Service (CDS) ne mogu biti datumski učinkoviti, ukupni troškovi na zaslonu mogu se s vremenom promijeniti ako ažurirate tečajeve valuta. Međutim, troškovi kako su zabilježeni u bazi ostaju nepromijenjeni jer se iznosi pohranjuju u valuti u kojoj su nastali.

## <a name="sales-currency"></a>Valuta prodaje

Valuta prodaje u aplikaciji Project Operations valuta je u kojoj se bilježe i prikazuju procijenjeni i stvarni iznosi prodaje. Valuta prodaje je i valuta u kojoj se klijentu fakturira ugovoreni posao. Na ugovoru o projektu, valuta prodaje zadana je iz zapisa klijenta ili računa i može se mijenjati tijekom stvaranja ugovora. Kada se ugovor stvara zatvaranjem ponude kao prihvaćene, valutu na ugovoru zadaje valute iz ponude.

Kada stvarate ugovor o projektu od početka, polje **Valuta prodaje** ne može se uređivati. Cjenici proizvoda i projekta zadani su na temelju te valute iz ugovora.

Za razliku od troškova, vrijednosti prodaje mogu se evidentirati samo u valuti prodaje.

## <a name="billing-method"></a>Način naplate

Obično postoje dvije vrste modela ugovaranja projekata, fiksna naknada i na temelju potrošnje. Ovi su modeli predstavljeni u aplikaciji Project Operations kao načini naplate s dvije moguće vrijednosti:

- Vrijeme i materijal: Model ugovaranja koji se temelji na potrošnji u kojem je svaki nastali trošak poduprt odgovarajućim prihodom. Kako procjenjujete ili pravite više troškova, povećavaju se i odgovarajuće procijenjena i stvarna prodaja. Navedite ograničenja koja se ne smiju prekoračiti za retke ugovora koji imaju ovaj način naplate koji ograničava stvarni prihod. Ograničenja koja ne smiju premašiti ne utječu na procijenjeni prihod.
- Fiksna cijena: Model ugovaranja s fiksnom naknadom koji ukazuje da će prodajne vrijednosti biti neovisne o nastalim troškovima. Prodajna je vrijednost fiksna i ne mijenja se kako procijenite ili napravite više troškova.

## <a name="project-price-lists"></a>Cjenici projekta

Cjenici projekta upotrebljavaju se za zadane cijene, a ne cijene troška, za vrijeme, trošak i ostale komponente povezane s projektom. Može postojati više cjenika. Svaki cjenik ima svoj datum stupanja na snagu za svaki ugovor o projektu. Project Operations ne podržava preklapanje datuma stupanja na snagu cjenika projekta.

Kada se ugovor o projektu stvara prihvaćanjem ponude projekta, cjenici projekta kopiraju se s uključenim nazivom i datumom ugovora. Kopiranje ovih podataka formira prilagođenu cijenu za komponente projekta na ovom ugovoru o projektu.

## <a name="product-price-lists"></a>Cjenici proizvoda

Cjenici proizvoda upotrebljavaju se za zadane cijene, a ne za cijene troškova, za retke ugovora koji se temelje na proizvodima. Postoji samo jedan cjenik proizvoda po ugovoru.

## <a name="transaction-classes"></a>Klase transakcija

Project Operations podržava četiri vrste klasa transakcija:

- Vrijeme
- Izdatak
- Materijal
- Naknada

Vrijednosti troška i prodaje mogu se procijeniti i nastati za klase transakcija Vrijeme, Trošak i Materijal. Naknada je klasa transakcija koja je samo prihod.

## <a name="work-entities-and-billing-entities"></a>Entiteti rada i naplate

Entiteti koji predstavljaju rad su projekti i zadaci. Entiteti koji predstavljaju aspekte naplate su redci ponude. Razne entitete rada možete povezati s mogućnostima naplate tako da ih povežete s redcima ugovora.

## <a name="multi-customer-deals"></a>Poslovi s više klijenata

Poslovi s više klijenata imaju više klijenata kojima se fakturira za posao. Zajednički primjeri obuhvaćaju:

- OEM poduzeća i njihovi partneri: Partneri i preprodavači prodaju proizvod s nekim uslugama kojw imaju dodanu vrijednost, što obično uključuje određeni posao s klijentom. OEM nudi financiranje dijela projekta. 

- Projekti javnog sektora: Više odjela lokalne samouprave pristaje financirati projekt i fakturira im se prema prethodno dogovorenoj raspodjeli. Na primjer, školski okrug i lokalna uprava dogovore se financirati izgradnju bazena.

## <a name="invoice-schedules"></a>Rasporedi fakturiranja

Rasporedi faktura specifični su za svaki redak ugovora i potrebni su za rad automatskog fakturiranja. Rasporedi faktura izrađuju se na temelju određenih datuma početka i završetka te učestalosti faktura. Rasporedi se upotrebljavaju u fazi ugovora kada je konfiguriran automatski postupak stvaranja fakture. Kada se ugovor o projektu stvara iz ponude, raspored faktura kopira se u ugovor o projektu iz ponude.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Promjene iz ugovora u aplikaciji Dynamics 365 Sales

Ugovori u aplikaciji Project Operations grade se na ugovorima iz aplikacije Dynamics 365 Sales. Međutim, postoje neka bitna odstupanja i razlike u funkcionalnosti koje biste trebali znati:

- Ugovori u aplikaciji Project Operations imaju dvije različite vrste redaka, jednu za projekte, a drugu za proizvode.
- Ugovori iz aplikacije Project Operations imaju vlastiti obrazac i elemente korisničkog sučelja, poslovna pravila, poslovnu logiku u dodacima i skripte na strani klijenta što ih čini jedinstvenima u ugovorima o prodaji.

Iz tih razloga ne biste trebali upotrebljavati ugovor o prodaji i ugovor o projektu naizmjenično.