---
title: Koncepti financijske procjene
description: U ovoj temi nalaze se informacije o financijskim procjenama projekata u aplikaciji Project Operations.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 74b2499cc706e03658cadeb088df154100051cbc7cce386b2e4d50dbdb5c197f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989182"
---
# <a name="financial-estimation-concepts"></a>Koncepti financijske procjene

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Financijska procjena projekta u aplikaciji Dynamics 365 Project Operations odvija se u dvije faze: 
1. Tijekom faze pretprodaje, prije dobivanja posla. 
2. Tijekom faze izvršenja, nakon izrade ugovora o projektu. 

Možete stvoriti financijsku procjenu za rad na projektu s pomoću neke od sljedeće 3 stranice:
- Stranice **Ponuda**, s pomoću pojedinosti retka ponude.  
- Stranice **Redak ugovora o projektu**, s pomoću pojedinosti retka ugovora. 
- Stranice **Projekt**, s pomoću stranica kartice **Zadaci** ili **Procjene troškova**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Uporaba ponude za projekt za stvaranje procjene
U ponudi koja se temelji na projektu možete upotrebljavati entitet **Pojedinost retka ponude** za procjenu rada potrebnog za isporuku projekta. Tu procjenu zatim možete podijeliti s klijentom.

Redci ponude koja se temelji na projektu ne moraju imati nijednu pojedinost retka ponude, a mogu ih imati puno. Pojedinosti retka ponude koriste se za procjenu vremena, troškova ili naknada. Microsoft Dynamics 365 Project Operations ne dopušta materijalne procjene na pojedinostima retka ponude. Oni se zovu razredi transakcije. Procijenjeni iznosi poreza također se mogu unijeti na razred transakcije.

Uz razrede transakcija, pojedinosti retka ponude imaju vrstu transakcije. Za pojedinosti retka ponude podržane su dvije vrste transakcija: **Trošak** i **Ugovor o projektu**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Uporaba ugovora o projektu za stvaranje procjene

Ako ste tijekom stvaranja ugovora koji se temelji na projektu upotrijebili ponudu, procjena koju ste izvršili za svaki redak ponude kopira se u ugovor o projektu. Struktura ugovora projekta je kao struktura ponude projekta koja ima retke, pojedinosti retka i rasporede faktura.

Procjene se mogu izvršiti izravno u ugovoru projekta, kao i u ponudi projekta. Za ponudu projekta, procjena se vrši s pomoću redaka ugovora i pojedinosti retka ugovora. Pojedinosti retka ugovora mogu se generirati i iz plana projekta koji je izrađen s pomoću pristupa procjene odozdo prema gore.

Pojedinosti retka ugovora mogu se koristiti za procjenu vremena, troškova ili naknada. Procijenjeni iznosi poreza također se mogu unijeti u pojedinost retka ugovora.

U pojedinostima retka ugovora nisu dozvoljene procjene materijala.

## <a name="use-a-project-to-create-an-estimate"></a>Uporaba projekta za stvaranje procjene 

Možete procijeniti vrijeme i troškove projekata. Project Operations ne podržava procjene materijala ili naknada za projekte.

Procjene vremena generiraju se kada izradite zadatak i identificirate atribute generičkog resursa potrebnog za izvršavanje zadatka. Procjene vremena generiraju se iz zadataka rasporeda. Procjene vremena ne izrađuju se ako izradite generičke članove tima izvan konteksta rasporeda.

Procjene troškova unose se u rešetku na stranici **Procjene troškova**.

Stvaranje procjene za projekt smatra se najboljom praksom, jer možete izraditi podrobne procjene rada ili vremena i troškova od dna naviše za svaki zadatak u projektnom planu. Zatim ovu podrobnu procjenu možete upotrijebiti za izradu procjena za svaki redak ponude i za klijenta izraditi vjerodostojniju ponudu. Kada uvozite ili stvarate podrobnu procjenu na retku ponude s pomoću projektnog plana, Project Operations uvozi prodajne vrijednosti i vrijednosti troška iz tih procjena. Nakon uvoza možete vidjeti mjerne podatke profitabilnosti, marže i izvedivosti na ponudi projekta.

## <a name="understanding-estimates"></a>Razumijevanje procjena

Tablicu u nastavku upotrebljavajte kao vodič za razumijevanje poslovne logike u fazi procjene.

| Scenarij                                                                                                                                                                                                                                                                                                                                          | Zapis entiteta                                                                                                                                                                                                       | Vrsta transakcije | Razred transakcije | Dodatne informacije                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Kada trebate procijeniti prodajnu vrijednost vremena na ponudi                                                                                                                                                                                                                                                                                    | Izrađena je pojedinost retka ponude (QLD)                                                                                                                                                                               | Ugovor projekta | Time        | Polje porijeklo transakcije u pojedinosti retka ponude na strani prodaje upućuje na pojedinost retka ponude na strani troškova |
|                                                                                                                                                                                                                                                                                     | Drugi zapis pojedinosti retka ponude izrađuje se s pomoću sustava za pohranjivanje odgovarajućih vrijednosti troškova. Sva polja koja nisu novac kopiraju se iz pojedinosti retka ponude za prodaju u pojedinost retka ponude za troškove od strane sustava.                                                                                                                                                                               | Trošak | Time        | Polje porijeklo transakcije u pojedinosti retka ponude na strani prodaje upućuje na pojedinost retka ponude na strani troškova |
| Kada trebate procijeniti prodajnu vrijednost vremena na ugovoru                                                                                                                                                                                                                                                                                 | Izrađena je pojedinost retka ugovora projekta (CLD)                                                                                                                                                                    | Ugovor projekta | Time        | Polje porijeklo transakcije u pojedinosti retka ugovora projekta na strani prodaje upućuje na pojedinost retka ugovora projekta na strani troškova      |
|                                                                                                                                                                                                                                                                                  | Drugi zapis pojedinosti retka ugovora projekta izrađuje se s pomoću sustava za pohranjivanje odgovarajućih vrijednosti troškova. Sva polja koja nisu novac kopiraju se iz prodaje CLD-a na trošak CLD od strane sustava.                                                                                                                                                                    | Trošak | Time        | Polje porijeklo transakcije u pojedinosti retka ugovora projekta na strani prodaje upućuje na pojedinost retka ugovora projekta na strani troškova      |
| Kada korisnik opisuje resurs na projektnom zadatku                                                                                                                                                                                                                                                                                            | Zapis retka procjene za prikaz vrijednosti prodaje zadatka izrađuje se prilikom izrade zadatka sa svim potrebnim dimenzijama određivanja cijena. Uloga i organizacijske jedinice dimenzije su određivanja cijena | Ugovor o projektu | Vrijeme        |                                                                                   |
|     | Zapis retka procjene za prikaz vrijednosti troškova zadatka izrađuje se prilikom izrade zadatka sa svim potrebnim dimenzijama određivanja cijena. Sva polja koja nisu novac kopiraju se iz retka procjene prodaje u redak procjene troškova od strane sustava. Uloga i organizacijska jedinica dimenzije su određivanja cijena za cijene koštanja i naplate.                                                                                                                                                                                                                | Cijena             | Vrijeme           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Prilagodba entiteta pojedinost retka ponude i pojedinost retka ugovora

Ako ste dodali prilagođeno polje u pojedinost retka ponude i želite da sustav unese vrijednost polja kao zadanu vrijednost na povezani redak troškova koji stvara, upotrijebite dodatke **PreOperationContractLineDetailUpdate** i **PreOperationQuoteLineDetailUpdate** alata za registraciju. Ti se dodaci moraju ponovno registrirati nakon što se pojedinost retka ponude ili pojedinost retka ugovora promijeni. Da biste dovršili proces, slijedite ove korake:

1. Otvorite PluginRegistrationTool i povežite se s mrežnom instancom.
2. Odaberite **Pretraži** i potražite dodatak za ažuriranje.
3. Odaberite dodatak, a zatim na glavnoj stranici kliknite **Odaberi**.
4. Odaberite korak dodatka za ažuriranje, kliknite desnom tipkom miša, a zatim odaberite **Ažuriraj**.
5. U dijaloškom okviru **Ažuriraj postojeći korak** u polju **Atributi filtriranja** odaberite gumb trotočke (**...**):
6. U dijaloškom okviru **Odaberi atribute** odaberite potvrdne okvire za prilagođene atribute.
7. Odaberite **U redu** da biste zatvorili dijaloški okvir, a zatim odaberite **Ažuriraj korak**.
8. Ponovite korake od 1 do 7 za drugi dodatak.
9. Zatvorite dodatak **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
