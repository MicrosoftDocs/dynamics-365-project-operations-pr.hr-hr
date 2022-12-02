---
title: Financijske procjene materijala na projektima
description: U ovom se članku navode informacije o definiranju ili procjeni materijala koji se temelji na projektu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eb33c8e2ead2a558bf53256095645011212ff343
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925677"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Financijske procjene materijala na projektima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations omogućuje voditeljima projekata da definiraju troškove materijala koji se temelje na projektu za svaki projekt ili zadatak. Svaka procjena materijala može se povezati s određenim projektnim zadatkom. Materijali koji se koriste na projektima mogu biti upisani proizvodi ili proizvodi iz kataloga proizvoda. Za svaku kombinaciju proizvoda i jedinice može se definirati cijena u cjenicima projekta za prodaju i cjenicima projekta za trošak.  

Poduzmite sljedeće korake za prikaz, dodavanje ili brisanje procjene materijala za projekt.

1. Idite na **Projekti** i odaberite projekt koji želite ažurirati.
2. Na kartici **Procjene materijala** pogledajte popis procjena materijala za projekt.
3. Odaberite **Nova procjena materijala** kako biste stvorili novu procjenu materijala. Ili odaberite procjenu materijala koja za brisanje, a zatim odaberite **Izbriši procjenu materijala**.

Tablica u nastavku pruža informacije o poljima na stavci **Redak procjene materijala** u projektu. 

| **Polje** | **Opis** | **Utjecaj prema dolje** |
| --- | --- | --- |
| Zadatak | Popis projektnih zadataka. To uključuje zadatke sažetka i lisnog čvora. | Kada odaberete zadatak za redak procjene materijala, to utječe na procijenjeni trošak materijala i procijenjenu prodaju materijala za zadatak. Ako je ovo polje prazno, procjena materijala prati se i zbraja samo na razini projekta. |
| Odabir proizvoda |  Možete navesti kako je ovo redak procjene za postojeći (kataloški) ili umetnut proizvod. | Ovo polje određuje hoćete li proizvod odabrati iz kataloga ili ga umetnuti. |
| Proizvod | ID proizvoda iz kataloga proizvoda. Kada odaberete ID proizvoda, vrijednost polja **Odaberi proizvod** automatski se ažurira na **Postojeći proizvod**. ID se upotrebljava za dohvaćanje cijena koštanja i prodajnih cijena iz cjenika. | Ovo polje ne utječe na niže razine. |
| Opis proizvoda koji se umeće | Tekstno polje za upisivanje naziva proizvoda. Ovo bi se polje trebalo upotrebljavati nakon odabira mogućnost **Umetni** u polju **Odaberi proizvod**.| Ovo polje ne utječe na niže razine. |
| Datum početka | Predviđeni datum za očekivanu uporabu materijala. | Ovo polje ne utječe na niže razine. |
| Grupa jedinica | Zadana vrijednost u ovom polju proizlazi iz zadane grupe jedinica na kataloškom proizvodu. Ovo polje možete ažurirati kako biste odabrali drugu grupu jedinica. | Ovo polje ne utječe na niže razine. |
| Jedinica | Vrijednost u ovom polju proizlazi iz zadane jedinice odabranog proizvoda. Ovo polje možete ažurirati kako biste odabrali drugu jedinicu. | Promjena jedinice rezultira drugačijom zadanom cijenom i troškom jedinice. |
| Količina | Procijenjena količina proizvoda koji će se upotrebljavati na projektu. | Ovo polje ne utječe na niže razine. |
| Jedinična cijena | Jedinični trošak odabranog proizvoda i kombinacije jedinica kako su postavljeni u mjerodavnom troškovniku. | Jedinični trošak uvijek se prikazuje u valuti troška projekta. Ako u cjeniku nije postavljen jedinični trošak za postavku kombinacije proizvoda i jedinice, jedinični trošak zadat će se na 0,00. |
| Jedinična cijena | Cijena odabrane kombinacije proizvoda i jedinice kako je postavljena u mjerodavnom prodajnom cjeniku. | Jedinični cijena uvijek se prikazuje u valuti prodaje projekta. Ako u cjeniku nije postavljena jedinična cijena za postavku kombinacije proizvoda i jedinice, tada će se jedinični trošak zadati na 0,00.|
| Ukupni trošak | Iznos troška koji se izračunava kao količina \* jedinični trošak.| Iznos troška uvijek se prikazuje u valuti troška projekta. |
| Ukupne prodaje | Prodajni iznos koji se izračunava kao količina \* jedinična cijena. | Iznos prodaje uvijek se prikazuje u valuti prodaje projekta. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
