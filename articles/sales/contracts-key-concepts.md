---
title: Ugovori o projektu – Osnovni koncepti
description: U ovom se članku navode informacije o osnovnim konceptima ugovora o projektu u aplikaciji Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 016a5d1defacdc6ba5828ca26395c9123e9323d0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926215"
---
# <a name="concepts-unique-to-project-based-contracts"></a>Jedinstveni koncepti za ugovore koji se temelje na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_



U ovom se članku navode ključni koncepti kojih morate biti svjesni prije nego što počnete upotrebljavati ugovore o projektu u aplikaciji Dynamics 365 Project Operations:

## <a name="owning-company"></a>Tvrtka vlasnik

Tvrtka vlasnica pravna je osoba iz modula **Upravljanje projektima i računovodstvo** za aplikaciju Project Operations iz sustava Dynamics 365 Finance. Tvrtka vlasnik pravna je osoba koja će obračunati troškove i prihode koji proizlaze iz posla.

## <a name="contracting-unit"></a>Ugovorna jedinica

Ugovorna jedinica predstavlja odjel ili praksu koja je vlasnik isporuke projekta. Možete postaviti troškove resursa za svaku ugovornu jedinicu. Kada resursu odredite cijenu, moći ćete postaviti i različite cijene koštanja resursa. Ova ugovorna jedinica posuđuje ove resurse od drugih sektora ili praksi unutar poduzeća. Cijene koštanja resursa nazivaju se cijenama prijenosa, posuđivanjem resursa ili cijenama razmjene. Kada postavljate cijene koštanja za posudbu resursa iz drugih sektora, upotrijebite valutu sektora koji posuđuje.

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

## <a name="project-price-lists"></a>Cjenici za projekt

Cjenici za projekt upotrebljavaju se za zadane cijene, a ne cijene koštanja, za vrijeme, trošak i ostale komponente povezane s projektom. Može postojati više cjenika. Svaki cjenik ima svoj datum stupanja na snagu za svaki ugovor o projektu. Project Operations ne podržava preklapanje datuma stupanja na snagu cjenika za projekt.

Kada se ugovor o projektu stvara prihvaćanjem ponude projekta, cjenici za projekt kopiraju se s uključenim nazivom i datumom ugovora. Kopiranje ovih podataka formira prilagođenu cijenu za komponente projekta na ovom ugovoru o projektu.

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

Poslovi s više klijenata imaju više klijenata kojima se fakturira za posao. Uobičajeni primjeri ovoga uključuju sljedeće:

- OEM poduzeća i njihovi partneri: Partneri i preprodavači prodaju proizvod s nekim uslugama kojw imaju dodanu vrijednost, što obično uključuje određeni posao s klijentom. OEM nudi financiranje dijela projekta. 

- Projekti javnog sektora: Više odjela lokalne samouprave pristaje financirati projekt i fakturira im se prema prethodno dogovorenoj raspodjeli. Na primjer, školski okrug i lokalna uprava dogovore se financirati izgradnju bazena.

## <a name="invoice-schedules"></a>Rasporedi fakturiranja

Rasporedi faktura specifični su za svaki redak ugovora i potrebni su za rad automatskog fakturiranja. Rasporedi faktura izrađuju se na temelju određenih datuma početka i završetka te učestalosti faktura. Rasporedi se upotrebljavaju u fazi ugovora kada je konfiguriran automatski postupak stvaranja fakture. Kada se ugovor o projektu stvara iz ponude, raspored faktura kopira se u ugovor o projektu iz ponude.

## <a name="changes-from-dynamics-365-sales-orders"></a>Promjene iz aplikacije Dynamics 365 Sales Orders

Ugovori u aplikaciji Project Operations grade se na narudžbama iz aplikacije Dynamics 365 Sales. Međutim, postoje bitna odstupanja i razlike u funkcionalnosti. Ugovori imaju vlastiti obrazac i elemente korisničkog sučelja, poslovna pravila, poslovnu logiku u dodacima i skripte na strani klijenta što ih čini jedinstvenima iz narudžbi. Iz tih razloga ne trebate naizmjenično upotrebljavati prodajni nalog i ugovor aplikacije Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
