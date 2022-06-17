---
title: Raspored izdataka upita za savezne nagrade
description: Ovaj članak pruža informacije o rasporedu izdataka saveznih nagrada.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: johnmichalak
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 00f9e97b9a6b3e8fe5e9cf9143e670612869b84c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916647"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Raspored izdataka upita za savezne nagrade

[!include [banner](../includes/banner.md)]

Prema Uredu za upravljanje i proračunskoj uputi A-133, agencije koje primaju savezna sredstva podliježu zahtjevima revizije, koji su poznati i kao pojedinačne revizije. Postupak revizije upotrebljava se za redovito izvješćivanje o prihodima i rashodima saveznih potpora. Dio jedinstvenog revizorskog izvješća uključuje Raspored izdataka za savezne nagrade (SEFA).

Raspored izdataka upita za savezne nagrade uključuje naziv i broj Kataloga savezne domaće pomoći (CFDA), broj potpore, godinu dodjele, naziv savezne agencije koja osigurava sredstva i naziv prolaznog entiteta. Upit se odnosi na određeno razdoblje. Uobičajeno je da je to razdoblje isto kao i razdoblje financijskog izvješća, koje je poslovna godina.

Upit uključuje potpore koje imaju datume predviđanja u odabranom datumskom rasponu. Stupac upita **Agencija za davanje potpore** prikazuje klijenta za potporu ili, za prolaznu potporu, agenciju za davanje potpore. Za prolazne potpore, stupac **Prolazna agencija** prikazuje klijenta potpore. Ako potpora nije prolazna potpora, stupac **Prolazna agencija** je prazan.

## <a name="set-up-the-cfda-clusters"></a>Postavljanje CFDA klastera

Morate postaviti CFDA klastere koji se mogu povezati s CFDA brojevima u Rasporedu izdataka upita za savezne nagrade.

1. Idite na **Upravljanje projektima i računovodstvo \> Postavljanje \> Potpore \> Katalog klastera savezne domaće pomoći**.
2. Odaberite **Novo** za stvaranje CFDA clustera.
3. Unesite naziv klastera.
4. Odaberite **Spremi** da biste spremili izmjene.

## <a name="set-up-cfda-numbers"></a>Postavljanje CFDA brojeva

Morate postaviti CFDA brojeve koji se mogu dodati potporama i uključiti u Rasporedu izdataka upita za savezne nagrade.

1. Idite na **Upravljanje projektima i računovodstvo \> Postavljanje \> Potpore \> Katalog brojeva savezne domaće pomoći**.
2. Odaberite **Novi** kako biste stvorili CFDA broj.
3. U stupac **Broj** unesite CFDA broj.
4. Pritisni tipku **Tab**.
5. U stupac **Opis** unesite CFDA naslov.
6. Pritisni tipku **Tab**.
7. Neobvezno: U polje **Programski klaster** dodajte odgovarajući CFDA klaster.
8. Odaberite **Spremi** da biste spremili izmjene.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Postavljanje potpora na izvješće za Raspored izdataka upita za savezne nagrade

1. Idite na **Upravljanje projektima i računovodstvo \> Potpore \> Potpore** i odaberite postojeću potporu.
2. Na Brzoj kartici **Postavljanje**, u polju **Katalog savezne domaće pomoći**, dodijelite CFDA broj. CFDA broj na potpori određuje CFDA klaster za izvješćivanje.
3. Na Brzoj kartici **Podaci za kontakt** unesite podatke o davatelju potpore slijedeći ove korake:

    1. U polje **Klijent potpore** unesite klijenta koji je odgovoran za potporu. Za postojeću potporu ovi su podaci možda već unijeti.
    2. Navedite je li klijent potpore donator. Ako je klijent potpore donator, potvrdni okvir **Prolazni** ostavite prazan. Ako je drugi klijent donator, a klijent potpore odgovoran je za trošenje i praćenje novca, odaberite potvrdni okvir **Prolazni**.

4. Ako ste u prethodnom koraku odabrali potvrdni okvir **Prolazni**, u polju **Agencija za davanje potpore** unesite klijenta koji je dao potporu. Agencija za davanje potpore i klijent ne mogu biti isti klijent.

Evo primjera prolazne potpore:

Savezna vlada financirala je infrastrukturni projekt za državu. Savezna vlada dala je novac državi da ga potroši. U ovom slučaju, savezna vlada je agencija davatelj potpore, a država je klijent potpore.

> [!NOTE] 
> Kada prvi put uključite značajku, početni CFDA brojevi unosit će se s pomoću postojećih brojeva u potporama.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Isključite potpore iz SEFA izvješća koje se temelji na vrsti potpore

1. Idite na **Upravljanje projektima i računovodstvo \> Postavljanje \> Potpore \> Vrste potpora**.
2. Na Brzoj kartici **Zadane informacije** odaberite potvrdni okvir **Izuzeti iz rasporeda izdataka za savezne nagrade**.
3. Odaberite **Spremi** da biste spremili izmjene.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Pokretanje Rasporeda izdataka upita za savezne nagrade

1. Idite na **Upravljanje projektima i računovodstvo \> Upiti i izvješća \> Upit za potporu \> Raspored izdataka za federalne nagrade**.
2. U odjeljku **Parametri** slijedite ove korake:

    1. U polju **Datumski interval** odaberite kod za datumski interval. Alternativno, u poljima **Od datuma** i **Do datuma** definirajte datumski interval.
    2. Neobvezno: Kako biste u upit uključili samo naplaćene transakcije kao prihod, postavite mogućnost **Uključi samo naplaćene prihode** na **Da**.

## <a name="columns"></a>Stupci

Raspored izdataka upita za savezne nagrade uključuje sljedeće stupce:

- Katalog naziva klastera savezne domaće pomoći
- Agencija za davanje potpora
- Prolazna agencija
- Naziv potpore
- ID potpore
- ID aplikacije potpore
- Katalog savezne domaće pomoći
- Potvrde
- Izdaci


[!INCLUDE[footer-include](../includes/footer-banner.md)]