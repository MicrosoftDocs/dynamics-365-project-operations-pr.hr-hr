---
title: Projektne potpore
description: U ovoj se temi objašnjava način stvaranja ili izmjene potpore.
author: RadhikaRS
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: c58a051b8129cadbde491751a946b75a75cb85118c7f0c7d25a06d322ffea596
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995752"
---
# <a name="project-grants"></a>Projektne potpore

[!include [banner](../includes/banner.md)]

Potpora je novčani poklon za određenu svrhu ili projekt. Obično postoje ograničenja za trošenje potpore. U Upravljanju projektima i računovodstvu možete unijeti i pratiti potpore i definirati njihove odnose s projektima i ugovorima o projektima. Na primjer, možete provesti sljedeće scenarije:

- Povežite potpore s projektima i izvorima financiranja putem veza na stranice **Projekt** i **Pojedinosti ugovora o projektu**.
- Unesite i pratite promjene u potpori kako se ona premješta iz jednog statusa u drugi.
- Unesite i pratite troškove, tražene i dodijeljene iznose.
- Stvorite glavne potpore i povežite s njima podpotpore.

Potporu možete stvoriti unosom svih pojedinosti u novi zapis ili možete kopirati pojedinosti iz postojeće potpore i zatim ih ažurirati.

## <a name="create-a-new-grant"></a>Stvaranje nove potpore

1. Idite na **Upravljanje projektima i računovodstvo** \> **Potpore** \> **Potpore**.
2. Odaberite **Novo** \> **Potpora**.
3. Na stranici s pojedinostima potpore, na Brzoj kartici **Općenito**, u polje **ID potpora**, unesite alfanumerički identifikator za potporu.
4. U polje **Naziv potpore** unesite naziv potpore.
5. U polje **Opis** dodajte pojedinosti o novoj potpori.

    Većina ostalih polja na stranici nisu obvezna i možete unijeti onoliko podataka koliko želite.

    Sljedeći popis opisuje podatke koji su navedeni na svakoj Brzoj kartici stranice pojedinosti o potpori:

    - **Općenito** – Unesite naziv potpore, status, opis, svrhu i iznos.
    - **Podaci o kontaktu** – Unesite pojedinosti o članovima osoblja, odjelu koji upravlja potporama i klijentu potpore ili organizacijskom izvoru potpore. Također možete naznačiti i je li vaša tvrtka ili ustanova prolazni entitet koji prima potporu, a zatim je prosljeđuje drugom primatelju. Odaberite **Dodaj** kako biste dodali podatke o kontaktu poput telefonskih brojeva i adresa e-pošte za tvrtku ili ustanovu koja daje potporu.
    - **Datumi i rokovi** – Unesite datume koji se odnose na potporu i zahtjev za potporu. Primjeri uključuju datum dospijeća zahtjeva, datum slanja i datum kada je potpora odobrena ili odbijena.
    - **Povezani projekti i ugovori o projektu** – Na ovu Brzu karticu možete unijeti podatke samo ako je polje **Status potpore** na Brzoj kartici **Općenito** postavljen na **Aktivno** ili **Dodijeljeno**. Odaberite jednu od sljedećih mogućnosti kako biste dovršili povezani zadatak:

        - **Dodaj izvor financiranja** – Dodajte novi izvor financiranja za potporu. Odmah možete unijeti sve pojedinosti ili možete upotrijebiti zadane podatke, a zatim ih kasnije ažurirati.
        - **Dodaj ugovor o projektu** – Dodajte ili ažurirajte podatke ugovora o projektu.
        - **Dodaj projekt** – Dodajte ili ažurirajte pojedinosti projekta.

    - **Postavi** – Unesite pojedinosti o odgovarajućim sredstvima financiranja, ako su ti podaci potrebni. Mnoge tvrtke ili ustanove koje dodjeljuju potpore zahtijevaju da primatelji potroše određeni iznos vlastitog novca ili resursa, koji bi se podudarali s iznosom dodijeljene potpore. U polje **Lokalni projekt ili ID praćenja** možete unijeti identifikator koji se razlikuje od identifikatora projekta.

        > [!NOTE]
        > Ako se dio potpore dodjeljuje drugoj tvrtki ili ustanovi, mogućnost **Podpotpora** postavite na **Da**. Za potpore koje se dodjeljuju u SAD-u možete odrediti hoće li se potpora dodijeliti u skladu s državnim ili saveznim propisom.

    - **Pojedinosti o povlačenju sredstava** – Dodajte ili ažurirajte podatke o tome koliko često se sredstva potpore mogu povući, naplatiti ili potrošiti.

## <a name="create-a-new-grant-from-a-copy"></a>Stvaranje nove potpore iz kopije

1. Idite na **Upravljanje projektima i računovodstvo** \> **Potpore** \> **Potpore**.
2. Odaberite **Novo** \> **Kopiraj iz potpore**.
3. Unesite alfanumerički identifikator i naziv nove potpore, a zatim odaberite **U redu**.
4. Na stranici s pojedinostima potpore pregledajte pojedinosti kopirane potpore i unesite sve potrebne promjene. Većina polja na stranici nisu obvezna.

## <a name="view-or-modify-grant-details"></a>Prikaz ili izmjena pojedinosti potpore

1. Idite na **Upravljanje projektima i računovodstvo** \> **Potpore** \> **Potpore**.
2. Odaberite potporu za izmjenu.
3. U Oknu radnje, na kartici **Potpora**, u grupi **Održavaj**, kliknite mogućnost **Uredi**.
4. Pregledajte pojedinosti potpore i unesite sve potrebne promjene.


[!INCLUDE[footer-include](../includes/footer-banner.md)]