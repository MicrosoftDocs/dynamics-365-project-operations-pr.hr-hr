---
title: Fakturiranje dobavljača - koncept i kreiranje
description: Ovaj tema opisuje koncept faktura dobavljača, scenarije za korištenje i kako kreirati fakture dobavljača u Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc9b3954b237294f52aa0bb74f8008a5dfdf78fd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580539"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Fakturiranje dobavljača - koncept i kreiranje

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Fakturiranje dobavljača u Microsoftu Dynamics 365 Project Operations može se koristiti za bilježenje troškova isporuka usluga i/ili materijala na projektu od strane dobavljača.

Kada se usluge i/ili materijali podugovaraju s dobavljačem, podugovaratelj predstavlja ugovorni ugovor s tim dobavljačem. Kako dobavljač isporučuje usluge ili se materijali primaju i koriste na projektnim zadacima, troškovi se bilježe na projektu. Povremeno dobavljač šalje fakture koje su provjerene i usklađene s troškovima koji su zabilježeni na projektu. Nakon dovršetka postupka provjere faktura dobavljača potvrđuje se i pušta za plaćanje.

## <a name="scenarios-for-use"></a>Scenariji za upotrebu

Fakture dobavljača u operacijama projekta mogu se koristiti za podršku dva različita scenarija.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Korisnici koriste puna iskustva podugovaranja

Iskustva fakture dobavljača pružaju način provjere i podudaranja stavki vremena, upotrebe materijala i stavki troškova koje upućuju na komponente kooperanta s recima fakture dobavljača. Taj se postupak može koristiti za provjeru točnosti redaka fakture dobavljača. Nakon dovršetka postupka provjere i potvrde fakture dobavljača, zatvaranje će stornirati stvarne vrijednosti zabilježene odobrenim zapisnicima o vremenu, troškovima i korištenju materijala te kreirati nove stvarne troškove pomoću redaka fakture dobavljača.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Korisnici ne koriste puna iskustva podugovaranja, ali žele imati jedinstven pregled troškova na projektima u projektnim operacijama

Ako proces podugovaranja pratite u sustavu treće strane, troškove iz tog sustava treće strane možete zabilježiti u Operacije projekta kreiranjem faktura dobavljača koje se ne odnose na kooperante. Na taj način vaši voditelji projekata mogu imati jedinstven, jedinstven uvid u sve troškove na određenom projektu.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Kreiranje faktura dobavljača u operacijama projekta

Fakture dobavljača mogu se kreirati na dva načina:

- Sa stranice popisa faktura dobavljača ili stranice s detaljima za jednu fakturu dobavljača
- Sa stranice popisa kooperanta ili stranice s detaljima za jedan podugovor

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Kreiranje sa stranice popisa faktura dobavljača ili stranice s detaljima

1. Otvorite **Fakture dobavljača za nabavu** \> **·**.
2. Na stranici popisa faktura dobavljača ili stranici s detaljima za jednu fakturu dobavljača odaberite **Novo** da biste kreirali novu fakturu dobavljača.

Tako kreirane fakture dobavljača mogu se odnositi i na kooperant.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Stvaranje sa stranice popisa kooperanta ili stranice s detaljima

1. Otvorite **Nabava** \> **kooperanata.**
2. Odaberite jedan ili više kooperanata.
3. Na stranici popisa kooperanta ili stranici s detaljima za jedan kooperant odaberite **Kreiraj fakturu** dobavljača da biste kreirali novu fakturu dobavljača.

Za svaki odabrani kooperant kreira se nova faktura dobavljača u **statusu Skica**.

Fakture dobavljača koje kreirate na ovaj način uvijek se odnose na kooperant u zaglavlju fakture dobavljača. Svaki redak na kooperantu koji ima način naplate vrijeme i materijal uzrokovat će kreiranje retka na fakturi dobavljača. Svaki redak na kooperantu koji ima način naplate fiksne cijene uzrokovat će kreiranje retka na fakturi dobavljača za svaku prekretnicu retka kooperanta koja ima status Spremno **za fakturiranje**.

Sljedeća polja i srodni zapisi kopirat će se iz kooperanta u zaglavlje fakture dobavljača:

- Prodavač.
- Povezani cjenici kopirat će se na fakturu dobavljača kao cjenike.
- Valuta.
- Ugovorna jedinica.
- Uvjeti plaćanja.

Za retke kooperacije vrijeme i materijal sljedeća polja i povezani zapisi kopirat će se iz retka kooperanta u redak fakture dobavljača:

- Reference redaka podugovaranja i podugovaranja
- Razred transakcije
- Uloga
- Kategorija transakcije
- Polja proizvoda
- Project
- Zadatak
- Resurs koji je moguće rezervirati

Za retke podugovaranja fiksnih cijena sljedeća će se polja kopirati iz retka kooperanta i prekretnice retka kooperacije u redak fakture dobavljača:

- Reference redaka kooperacije i podugovaranja.
- Klasa transakcija. Prema zadanim postavkama vrijednost će biti **Prekretnica**.
- Naziv i iznos ključne etape kopirat će se iz povezane prekretnice retka kooperanta.
- Korisnik će moći odabrati projekt i zadatak u retku fakture dobavljača.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
