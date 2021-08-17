---
title: Rasporedi faktura po redcima ponude koji se temelje na projektu
description: U ovoj temi nalaze se informacije o stvaranju rasporeda faktura i kontrolnih točaka za retke ponude.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0d07596b299d71b229487faf80a09e368059575ea37095d2c82d35561d009c96
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988597"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Rasporedi faktura po redcima ponude koji se temelje na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Redak ponude koji se temelji na projektu pruža mogućnost navođenja rasporeda računa. To nije obvezno tijekom faze ponude, jer aplikacija ne podržava fakturiranje projekta kada je vezan za redak ponude. Fakturiranje je dozvoljeno tek nakon prihvaćanja ponude. Jedini utjecaj na niže razine pri stvaranju rasporeda faktura tijekom faze ponude je taj da se ovaj raspored faktura kopira u redak ugovora koji se temelji na projektu. Ako tijekom faze ponude ne stvorite raspored faktura, to ćete moći učiniti na retku ugovora koji se temelji na projektu.

Sveukupno, svrha rasporeda faktura je omogućiti automatsko stvaranje nacrta faktura za redak ugovora koji se temelji na projektu. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Stvaranje rasporeda faktura za vrijeme i materijal za redak ponude koji se temelji na projektu

Kada je način naplate retka ponude koji se temelji na projektu Vrijeme i materijal, sustav generira raspored računa na temelju datuma. Kako biste automatski generirali raspored računa na temelju datuma, poduzmite sljedeće korake.

1. Idite na **Postavke** > **Učestalost faktura** i postavite učestalost faktura.
2. Na stranici **Ponude** otvorite ponudu projekta i na kartici **Sažetak** postavite traženi datum isporuke.
3. Otvorite redak ponude vremena i materijala za koji trebate stvoriti raspored faktura koji se temelji na datumu. 
4. Na kartici **Raspored faktura** odaberite vrijednosti u poljima **Početak naplate** i **Učestalost faktura**. 
5. Na podrešetki odaberite **Generiraj raspored faktura**.
6. Aplikacija generira raspored faktura s poljima **Datum pokretanja fakture**, **Datum presjeka transakcije** i **Status pokretanja** postavljenima na sljedeći način:

    - **Datum pokretanja fakture** postavljen je na datum koji se određuje na temelju učestalosti fakture.
    - **Datum presjeka transakcije** postavljen je na dan prije **Datuma pokretanja fakture**.
    - **Status pokretanja** automatski se postavlja na **Ne pokreći**. Kada se posao automatskog stvaranja fakture odvija za određeni datum pokretanja fakture, ažurirat će ovo polje bilo na **Uspješno pokretanje** ili **Neuspješno pokretanje**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Stvaranje rasporeda faktura nepromjenjive cijene za redak ponude koji se temelji na projektu

Kada redak ponude koji se temelji na projektu ima način naplate **Nepromjenjiv**, sustav stvara raspored faktura na temelju kontrolne točke. Poduzmite sljedeće korake za automatsko generiranje ovog rasporeda za nepromjenjivi skup kontrolnih točaka koje su podjednako raspoređene za kalendarsko razdoblje.

1. Idite na **Postavke** > **Učestalost faktura** i postavite učestalost faktura.
2. Na stranici **Ponude** otvorite ponudu projekta i na kartici **Sažetak** postavite traženi datum isporuke.
3. Otvorite redak ponude s nepromjenjivom cijenom za koji trebate stvoriti raspored kontrolnih točaka. 
4. Na kartici **Raspored faktura** odaberite vrijednosti u poljima **Početak naplate** i **Učestalost faktura**. 
5. Na podrešetki odaberite **Generiraj povremene kontrolne točke**.
6. Aplikacija generira raspored faktura s nazivom, datumom i iznosom kontrolne točke.

    - Naziv kontrolne točke postavljen je na datum koji se određuje na temelju učestalosti fakture.
    - Datum kontrolne točke postavljen je na datum koji se određuje na temelju učestalosti fakture.
    - Iznos kontrolne točke izračunava se dijeljenjem iznosa ponude na retku ponude koji se temelji na projektu s brojem kontrolnih točaka kako je određeno učestalošću te početkom naplate i zatraženim datumima isporuke.
    - Ako redak ponude ima i procijenjeni iznos poreza, ta se vrijednost podjednako dijeli između svake kontrolne točke pri generiranju povremenih kontrolnih točaka.

### <a name="manually-create-milestones"></a>Ručno stvaranje kontrolnih točaka

Kontrolne točke s nepromjenjivom cijenom mogu se generirati i ručno kada se povremeno ne dijele. Za ručno stvaranje kontrolnih točaka, učinite sljedeće:

Otvorite redak ponude s nepromjenjivom cijenom u kojem trebate stvoriti kontrolnu točku. Na kartici **Raspored faktura**, na podrešetki, odaberite **+ Stvori novu kontrolnu točku ponude** i unesite tražene podatke na temelju sljedeće tablice.

| **Polje** | **Mjesto** | **Opis** | **Utjecaj prema dolje** |
| --- | --- | --- | --- |
| Naziv kontrolne točke | Brzo stvaranje | Naziv kontrolne točke. | To se prenosi na kontrolnu točku retka ugovora o projektu i na fakturu |
| Projektni zadatak | Brzo stvaranje | Ako je kontrolna točka vezana uz projektni zadatak, s pomoću ove reference možete dodati prilagođenu logiku koja je postavila status kontrolne točke na temelju statusa zadatka. | Ta referenca aplikacije nema nikakav utjecaj na niže razine u zadatku. |
| Datum kontrolne točke | Brzo stvaranje | Postavite datum na koji bi postupak automatskog stvaranja fakture trebao tražiti status ove kontrolne točke kako bi se uzela u obzir za fakturiranje. | To se prenosi na kontrolnu točku retka ugovora o projektu i na fakturu. |
| Stanje fakturiranja | Brzo stvaranje | Kad se stvori kontrolna točka, taj se status uvijek postavi na **Nije spremno za fakturiranje**. | To se prenosi na kontrolnu točku retka ugovora o projektu i na fakturu. |
| Iznos retka | Brzo stvaranje | Iznos ili vrijednost kontrolne točke koja će se fakturirati klijentu. | To se prenosi na kontrolnu točku retka ugovora o projektu i na fakturu. |
| Porez | Brzo stvaranje | Iznos poreza koji će se primijeniti na kontrolnu točku. | To se prenosi na kontrolnu točku retka ugovora o projektu i na fakturu. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]