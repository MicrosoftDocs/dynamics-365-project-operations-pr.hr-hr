---
title: Stvaranje procjena po retku ponude
description: U ovom se članku navode informacije o načinu stvaranja procjene na retku ponude za projekt.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9f606ff2c33c46063f7025e8bc58e704d472061b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912553"
---
# <a name="create-estimates-on-a-quote-line"></a>Stvaranje procjena po retku ponude

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Na ponudi koji se temelji na projektu, možete koristiti entitet pojedinost retka ponude za procjenu rada potrebnog za isporuku projekta. Tu procjenu zatim možete podijeliti s klijentom.

Reci ponude koja se temelji na projektu ne moraju imati pojedinosti retka ponude. Alternativno, mogu imati mnogo pojedinosti retka ponude. Pojedinosti retka ponude koriste se za procjenu vremena, troškova ili naknada. Dynamics 365 Project Operations ne dopušta materijalne procjene na pojedinostima retka ponude. Oni se zovu razredi transakcije. Procijenjeni iznosi poreza također se mogu unijeti na razred transakcije.

Uz razrede transakcija, pojedinosti retka ponude imaju vrstu transakcije. Za pojedinosti retka ponude postoje dvije vrste transakcija, **Trošak** i **Ugovor o projektu**.

## <a name="estimate-by-using-a-contract"></a>Procjena korištenjem ugovora

Ako ste tijekom stvaranja ugovora koji se temelji na projektu upotrijebili ponudu aplikacije Project Operations, procjena koju ste izvršili za svaki redak ponude kopira se u ugovor o projektu. Struktura ugovora projekta je kao struktura ponude projekta koja ima retke, pojedinosti retka i rasporede faktura.

Procjene se mogu izvršiti izravno u ugovoru projekta, kao i u ponudi projekta. Za ponudu projekta, procjena se vrši s pomoću redaka ugovora i pojedinosti retka ugovora. Pojedinosti retka ugovora mogu se generirati i iz plana projekta koji je izrađen s pomoću pristupa procjene odozdo prema gore.

Pojedinosti retka ugovora mogu se koristiti za procjenu vremena, troškova ili naknada. Procijenjeni iznosi poreza također se mogu unijeti u pojedinost retka ugovora.

U pojedinostima retka ugovora nisu dozvoljene procjene materijala.

Procesi koji su podržani u ugovoru projekta su izrada fakture i potvrda. Izrada fakture izrađuje skicu fakture koja se temelji na projektu koja uključuje sve stvarne vrijednosti nenaplaćene prodajne do trenutačnog datuma.

Potvrdom se dobiva verzija ugovora koja je samo za čitanje i njezin se status mijenja iz **Skica** u **Potvrđeno**. Nakon što poduzmete ovu radnju, ne možete ju poništiti. Budući da je ova radnja trajna, najbolja je praksa održati ugovor u statusu **Skica**.

Jedine razlike između ugovora sa statusom skice i potvrđenih ugovora jesu njihov status i činjenica da se ugovori sa statusom skice mogu uređivati, dok potvrđeni ugovori ne mogu. Izrada fakture i praćenje stvarnih vrijednosti mogu se izvršiti na ugovorima sa statusom skice i potvrđenim ugovorima.

Nije dozvoljena promjena narudžbi u ugovorima ili projektima.

## <a name="estimating-projects"></a>Procjena projekata

Možete procijeniti vrijeme i troškove projekata, ali ne i materijale ili naknade.

Procjene vremena generiraju se kada izradite zadatak i identificirate atribute generičkog resursa potrebnog za izvršavanje zadatka. Procjene vremena generiraju se iz zadataka rasporeda. Procjene vremena ne izrađuju se ako izradite generičke članove tima izvan konteksta rasporeda.

Procjene troškova unose se u rešetku na stranici **Procjene**.

## <a name="understand-estimation"></a>Objašnjenje procjene

Sljedeću tablicu koristite kao vodič za razumijevanje poslovne logike u fazi procjene.

| Situacija                                                                                                                                                                                                                                                                                                                                          | Zapis entiteta                                                                                                                                                                                                       | Vrsta transakcije | Razred transakcije | Dodatne informacije                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Kada trebate procijeniti prodajnu vrijednost vremena na ponudi                                                                                                                                                                                                                                                                                    | Izrađena je pojedinost retka ponude (QLD)                                                                                                                                                                               | Ugovor projekta | Time        | Polje porijeklo transakcije u pojedinosti retka ponude na strani prodaje upućuje na pojedinost retka ponude na strani troškova |
|                                                                                                                                                                                                                                                                                     | Drugi zapis pojedinosti retka ponude izrađuje se s pomoću sustava za pohranjivanje odgovarajućih vrijednosti troškova. Sva polja koja nisu novac kopiraju se iz pojedinosti retka ponude za prodaju u pojedinost retka ponude za troškove od strane sustava.                                                                                                                                                                               | Trošak | Time        | Polje porijeklo transakcije u pojedinosti retka ponude na strani prodaje upućuje na pojedinost retka ponude na strani troškova |
| Kada trebate procijeniti prodajnu vrijednost vremena na ugovoru                                                                                                                                                                                                                                                                                 | Izrađena je pojedinost retka ugovora projekta (CLD)                                                                                                                                                                    | Ugovor projekta | Time        | Polje porijeklo transakcije u pojedinosti retka ugovora projekta na strani prodaje upućuje na pojedinost retka ugovora projekta na strani troškova      |
|                                                                                                                                                                                                                                                                                  | Drugi zapis pojedinosti retka ugovora projekta izrađuje se s pomoću sustava za pohranjivanje odgovarajućih vrijednosti troškova. Sva polja koja nisu novac kopiraju se iz prodaje CLD-a na trošak CLD od strane sustava.                                                                                                                                                                    | Trošak | Time        | Polje porijeklo transakcije u pojedinosti retka ugovora projekta na strani prodaje upućuje na pojedinost retka ugovora projekta na strani troškova      |
| Kada korisnik opisuje resurs na projektnom zadatku                                                                                                                                                                                                                                                                                            | Zapis retka procjene za prikaz vrijednosti prodaje zadatka izrađuje se prilikom izrade zadatka sa svim potrebnim dimenzijama određivanja cijena. Uloga i organizacijske jedinice dimenzije su određivanja cijena | Ugovor o projektu | Vrijeme        |                                                                                   |
|     | Zapis retka procjene za prikaz vrijednosti troškova zadatka izrađuje se prilikom izrade zadatka sa svim potrebnim dimenzijama određivanja cijena. Sva polja koja nisu novac kopiraju se iz retka procjene prodaje u redak procjene troškova od strane sustava. Uloga i organizacijska jedinica dimenzije su određivanja cijena za cijene koštanja i naplate.                                                                                                                                                                                                                | Cijena             | Vrijeme           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Prilagodba entiteta pojedinost retka ponude i pojedinost retka ugovora

Ako ste dodali prilagođeno polje u pojedinost retka ponude i želite da sustav unese vrijednost polja kao zadanu vrijednost na povezani redak troškova koji izradi, upotrijebite dodatak PreOperationContractLineDetailUpdate i PreOperationQuoteLineDetailUpdate alata za registraciju. Ti se dodaci moraju ponovno registrirati nakon što se pojedinost retka ponude ili pojedinost retka ugovora promijeni. Da biste dovršili proces, slijedite ove korake:

1. Otvorite PluginRegistrationTool i povežite se s mrežnom instancom.
2. Odaberite **Pretraži** i potražite dodatak za ažuriranje.
3. Odaberite dodatak, a zatim na glavnoj stranici odaberite **Odaberi**.
4. Odaberite korak dodatka za ažuriranje, kliknite desnom tipkom miša, a zatim odaberite **Ažuriraj**.
5. U dijaloškom okviru **Ažuriraj postojeći korak** u polju **Atributi filtriranja** odaberite gumb trotočke (**...**):
6. U dijaloškom okviru **Odaberi atribute** odaberite potvrdne okvire za prilagođene atribute.
7. Odaberite **U redu** da biste zatvorili dijaloški okvir, a zatim odaberite **Ažuriraj korak**.
8. Ponovite korake od 1 do 7 za drugi dodatak.
9. Zatvorite alat za registraciju dodataka.


[!INCLUDE[footer-include](../includes/footer-banner.md)]