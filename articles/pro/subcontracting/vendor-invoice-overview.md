---
title: Fakturiranje dobavljača – Koncept i stvaranje
description: U ovom se članku opisuje koncept faktura dobavljača i scenariji njihove upotrebe te se objašnjava kako navedene fakture izraditi u aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261925"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Fakturiranje dobavljača – Koncept i stvaranje

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Fakturiranjem u aplikaciji Microsoft Dynamics 365 Project Operations dobavljači mogu upotrebljavati za bilježenje troškova isporuka usluga i/ili materijala za projekt.

Kada se usluge i/ili materijali podugovore s dobavljačem, podugovor predstavlja ugovor s tim dobavljačem. Kako dobavljač isporučuje usluge ili kako se materijali primaju i upotrebljavaju za projektne zadatke, bilježe se troškovi na projektu. Dobavljač povremeno šalje provjerene fakture i one se usklađuju s troškovima zabilježenima na projektu. Nakon završetka postupka provjere faktura dobavljača se potvrđuje i izdaje za plaćanje.

## <a name="scenarios-for-use"></a>Scenariji upotrebe

Fakture dobavljača izrađene u aplikaciji Project Operations mogu se upotrijebiti u dvama različitim scenarijima:

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klijenti se koriste svim iskustvima podugovaranja

Iskustva fakturiranja dobavljača pružaju način za provjeru i usklađivanje vremena unosa, utrošenog materijala i unosa troškova koji se odnose na podugovorene komponente s redcima fakture dobavljača. Ovaj se postupak može upotrijebiti za provjeru točnosti redaka fakture dobavljača. Nakon dovršetka postupka provjere i potvrde fakture dobavljača aplikacija će poništiti stvarne podatke spremljene za odobreno vrijeme, zapisnike o troškovima i iskorištenosti materijala te kreirati nove stvarne podatke o troškovima koristeći retke fakture dobavljača.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klijenti koji se ne svim iskustvima podugovaranja, ali žele imati objedinjeni prikaz troškova projekata u aplikaciji Project Operations

Ako pratite proces podugovaranja u sustavu treće strane, možete zabilježiti troškove iz tog sustava u aplikaciji Project Operations kreiranjem faktura dobavljača koje ne upućuju na podugovore. Na taj način vaši voditelji projekta mogu imati jedinstveni, objedinjeni prikaz svih troškova danog projekta.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Kreiranje faktura dobavljača u aplikaciji Project Operations

Fakturu dobavljača možete kreirati na dva načina:

- Na stranici s popisom faktura dobavljača ili stranici s pojedinostima za jednu fakturu dobavljača
- Na stranici s popisom podugovora ili stranici s pojedinostima za pojedinačni podugovor

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Kreiranje fakture na stranici s popisom faktura dobavljača ili stranici s pojedinostima

1. Idite na **Nabava** \> **Fakture dobavljača**.
2. Na stranici s popisom faktura dobavljača ili stranici s pojedinostima za jednu fakturu dobavljača odaberite **Nova** za kreiranje nove fakture dobavljača.

Fakture dobavljača koje se kreiraju na ovaj način također mogu upućivati na podugovor.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Kreiranje fakture na stranici s popisom podugovora ili stranici s pojedinostima

1. Idite na **Nabava** \> **Podugovori**.
2. Odaberite jedan ili više podugovora.
3. Na stranici s popisom podugovora ili stranici s pojedinostima za jedan podugovor odaberite **Kreiranje fakture dobavljača** za kreiranje nove fakture dobavljača.

Nova faktura dobavljača sa statusom **Skica** kreira se za svaki podugovor koji odaberete.

Fakture dobavljača koje kreirate na ovaj način uvijek upućuju na podugovor u zaglavlju fakture dobavljača. Zbog svakog retka u podugovoru koji ima način naplate vremena i materijala stvorit će se redak na fakturi dobavljača. Svaki redak u podugovoru s načinom naplate po fiksnoj cijeni uzrokovat će stvaranje retka na fakturi dobavljača za svaku ključnu točku retka podugovora koji ima status **Spremno za fakturiranje**.

Sljedeća polja i povezani zapisi kopirat će se iz podugovora u zaglavlje fakture dobavljača:

- Dobavljač.
- Povezani će se cjenici kopirati na fakturu dobavljača kao cjenici.
- Valuta.
- Ugovorna jedinica.
- Uvjeti plaćanja.

Za retke podugovora o vremenu i materijalu sljedeća će se polja i povezani zapisi kopirati iz retka podugovora u redak fakture dobavljača:

- Upućivanja podugovora i retka podugovora
- Razred transakcije
- Uloga
- Kategorija transakcije
- Polja proizvoda
- Project
- Zadatak
- Resurs koji je moguće rezervirati

Za retke podugovora o nepromjenjivoj cijeni sljedeća će se polja kopirati iz retka podugovora i ključne točke retka podugovora u redak fakture dobavljača:

- Upućivanja podugovora i retka podugovora.
- Razred transakcije. Prema zadanim postavkama vrijednost će biti **Ključna točka**.
- Naziv i iznos ključne točke kopirat će se iz povezane ključne točke retka podugovora.
- Korisnik će moći odabrati projekt i zadatak na retku fakture dobavljača.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
