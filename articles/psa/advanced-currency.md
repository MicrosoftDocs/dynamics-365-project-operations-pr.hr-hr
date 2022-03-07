---
title: Scenariji višestruke valute (verzija 3.x)
description: Ova tema pruža informacije o scenarijima višestruke valute.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 89a91cf3dbbcf81dbb089ee88c8c177c73afb694914ca7d95eae96776d38abed
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005112"
---
# <a name="multiple-currency-scenarios"></a>Scenariji višestruke valute

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 ima dva koncepta valuta:

- **Valuta transakcije** - Valuta u kojoj se odvija transakcija. 
- **Osnovna valuta** - Valuta instance Dynamics 365. Ova je valuta postavljena kada je dostupna instanca sustava Dynamics 365. Ne može se promijeniti.

Na primjer, Contoso SAD prodao je 100 majica klijentu u Ujedinjenoj Kraljevini za 15 funti (GBP) po komadu. Sljedeća tablica prikazuje kako se ta transakcija zapisuje u entitetu Naručeni proizvod.

| Proizvod | Količina | Jedin. cijena | Valuta | Iznos | Tečaj | Cijena po jedinici (osnova)| Iznos (osnova)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Majica | 100      | 15             | GBP      | 1500   | 0.94          | $17.25               | $1,725       |

Stupac **Valuta** prikazuje valutu transakcije koja je valuta u kojoj se izvršila prodaja. Stupac **Tečaj** je tečaj između valute transakcije i osnovne valute. Osnovna valuta je dolar (USD). Ova osnovna valuta postavljena je kada je dostupna instanca sustava Dynamics 365.
Kako tablica prikazuje, svaka se transakcija zapisuje i u valuti transakcije i u osnovnoj valuti. Dynamics 365 koristi valutni tečaj za izračunavanje iznosa osnovnih valuta.

## <a name="project-service-automation-extensions"></a>Proširenja za Project Service Automation

Dynamics 365 Project Service Automation utječe na valutu transakcije jer poslovne transakcije obično imaju dva aspekta: trošak i prodaju.

Sljedeći entiteti smatraju se poslovnim transakcijama:

- Pojedinost retka ponude
- Pojedinost retka ugovora o projektu
- Redak procjene
- Redak u dnevniku
- Pojedinost retka fakture
- Stvarni rezultat

U svakom od tih entiteta postoji zapis koji predstavlja iznos troška ili iznos prodaje. Što se tiče bilo kojeg entiteta sustava Dynamics 365 koji ima polje **Iznos**, svaki zapis sadrži iznose i u valuti transakcije i u osnovnoj valuti. 

PSA proširuje koncept valute transakcije za trošak i prodaju na sljedeće načine:

- Valuta transakcije troška za vremenske transakcije uvijek dolazi iz valute organizacijske jedinice koja posjeduje ili upravlja projektom. Ova organizacijska jedinica poznata je kao ugovorna jedinica.
- Valuta transakcije prodaje za transakcije vremena i troška uvijek dolazi iz valute ugovora o projektu.
- Valuta transakcije troška za troškove dolazi iz valute u kojoj je izrađena stavka troška.

## <a name="multiple-currency-scenario"></a>Scenarij višestruke valute

U ovom se odjeljku opisuje primjer projekta koji tvrtka Contoso UK dostavlja klijentu pod nazivom Fabrikam iz Japana. Evo kako je scenarij postavljen:

1. GBP i Japanski jen (JPY) postavljeni su pod **Postavke** \> **Poslovno upravljanje** \> **Valute**. 
2. Postavljen je račun klijenta pod nazivom **Fabrikam - Japan**, a JPY je odabran kao valuta na računu.
3. Postavljena je organizacijska jedinica pod nazivom **Contoso UK**, a GBP je odabrana kao valuta.
4. Stvoren je ugovor o projektu gdje je **Contoso UK** naveden kao ugovorna jedinica, a **Fabrikam – Japan** kao klijent.
5. Na temelju aranžmana naplate za različite razrede transakcija na projektu, kao što je naplata za vrijeme u odnosu na naplatu za troškove, izrađeni su reci ugovora o projektu.
6. Stvoren je projekt u kojem je **Contoso UK** naveden kao ugovorna jedinica. Ovaj projekt je izrađen i mapiran u retke ugovora o projektu.


Tijekom procjene koja koristi pojedinost retka ponude, pojedinost retka ugovora o projektu ili u retku procjene rasporeda, dva zapisa uvijek se izrađuju u entitetu. Jedan zapis je za trošak, a drugi zapis je za prodaju.

- Prema zadanim postavkama, valuta transakcije na zapisu o troškovima postavljena je na valutu ugovorne jedinice projekta. U ovom primjeru, valuta je GBP.
- Prema zadanim postavkama, valuta transakcije na zapisu o prodaji postavljena je na valutu ugovora o projektu. U ovom primjeru, valuta je JPY.

Kada se stvaraju stvarne vrijednosti za vrijeme s pomoću unosa vremena ili retka u dnevniku, događa se sljedeće:

- Prema zadanim postavkama, valuta transakcije na zapisu o troškovima postavljena je na valutu ugovorne jedinice projekta.
- Prema zadanim postavkama, valuta transakcije na zapisu o prodaji postavljena je na valutu ugovora o projektu.

Kada se izrađuju stvarne vrijednosti za troškove koristeći unos troška ili redak u dnevniku, događa se sljedeće:

- Iznos troška možete zapisati u bilo kojoj valuti. Odaberite valutu s pomoću birača valute na stranici **Unos troška** ili na stranici **Redak u dnevniku**. Prema zadanim postavkama, valuta transakcije za zapis o troškovima postavljena je na valutu unosa troška. 
- Prema zadanim postavkama, valuta transakcije za zapis o prodaji valuta je ugovora o projektu. Da biste postavili ovu valutu, sustav najprije pretvara iznos transakcije u valuti koju je korisnik unio u osnovnu valutu. Zatim pretvara iznos u valutu ugovora o projektu. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Računanje zbrojeva kada se stvarni rezultati projekta zapisuju u višestrukim valutama transakcije

Dynamics 365 automatski obrađuje zbrojeve iznosa u različitim valutama. Evo primjera.

| Razred transakcije | Vrsta transakcije| Datum   | Resurs | Kategorija transakcije | Količina | Jedinična cijena | Iznos      | Tečaj | Osnovni iznos |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Vrijeme              | Nenaplaćena prodaja   | 14. lip. | Ivan  |                      | 8 h    | 20,000 JPY    | 160,000 JPY | 123           | 1,300.81 USD    |
| Time              | Nenaplaćena prodaja   | 15. lip. | Ivan  |                      | 8 h    | 20,000 JPY    | 160,000 JPY | 123           | 1,300.81 USD    |
| Trošak           | Nenaplaćena prodaja   | 16. lip. | Ivan  | Hoteli                | 1 ea     | 250 EUR      | 250 EUR     | 0.94          | 265.95 USD     |
| Trošak           | Nenaplaćena prodaja   | 17. lip. | Ivan  | Najam automobila           | 1 ea     | 150 EUR      | 150 EUR     | 0.94          | 159.57 USD     |

Da biste izračunali ukupnu vrijednost nenaplaćene prodaje na projektu, možete izraditi polje zbroja za polje **Iznos** na svim povezanim stvarnim vrijednostima nenaplaćene prodaje. Polje zbroja konstrukt je sustava Dynamics 365 koji omogućuje brze formule na povezanim zapisima.


[!INCLUDE[footer-include](../includes/footer-banner.md)]