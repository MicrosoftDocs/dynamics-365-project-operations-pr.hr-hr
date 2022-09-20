---
title: Kreiranje faktura dobavljača
description: U ovom se članku opisuje koncept faktura dobavljača i objašnjava kako ih stvoriti u Microsoftu Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475459"
---
# <a name="create-vendor-invoices"></a>Kreiranje faktura dobavljača

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Da biste koristili funkcionalnost opisanu u ovom članku, morate omogućiti **značajku Omogući obradu stvarnih kooperanata s projektnim operacijama za scenarije temeljene** na resursima u **radnom prostoru za upravljanje** značajkama.

Fakturiranje dobavljača u Microsoftu Dynamics 365 Project Operations može se koristiti za bilježenje troškova isporuka usluga i/ili materijala na projektu koji dovršavaju dobavljači.

Kada se usluge i/ili materijali podugovaraju s dobavljačem, podugovaratelj predstavlja ugovorni ugovor s tim dobavljačem. Kako dobavljač isporučuje usluge ili kako se materijali primaju i koriste na projektnim zadacima, troškovi se bilježe na projektu. Dobavljač zatim povremeno šalje fakture. Te se fakture provjeravaju i usklađuju s troškovima koji su zabilježeni na projektu. Nakon dovršetka postupka provjere faktura dobavljača potvrđuje se i pušta za plaćanje.

## <a name="scenarios-for-use"></a>Scenariji za upotrebu

Fakture dobavljača u operacijama projekta mogu se koristiti za podršku dva različita scenarija:

- Kupci koriste puna iskustva podugovaranja.
- Korisnici ne koriste potpuna iskustva podugovaranja, ali žele imati jedinstven pregled troškova na projektima u projektima u projektnim operacijama.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Korisnici koriste puna iskustva podugovaranja

Iskustva fakture dobavljača pružaju način provjere stavki vremena, upotrebe materijala i stavki troškova koje se odnose na komponente kooperanta i podudaraju ih s recima fakture dobavljača. Taj se postupak može koristiti za provjeru točnosti redaka fakture dobavljača. Nakon dovršetka postupka provjere i potvrde fakture dobavljača, sustav stornira stvarne vrijednosti zabilježene odobrenim zapisnicima o vremenu, troškovima i korištenju materijala, a zatim kreira nove stvarne troškove pomoću redaka fakture dobavljača.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Korisnici ne koriste puna iskustva podugovaranja, ali žele imati jedinstven pregled troškova na projektima u projektnim operacijama

Ako proces podugovaranja pratite u sustavu treće strane, troškove iz tog sustava treće strane možete zabilježiti u Operacije projekta kreiranjem faktura dobavljača koje se ne odnose na kooperante. Na taj način vaši voditelji projekata mogu imati jedinstven, jedinstven pogled na sve troškove na određenom projektu.

## <a name="create-vendor-invoices-in-project-operations"></a>Kreiranje faktura dobavljačima u operacijama projekta

Fakture dobavljača kreiraju se u Dynamics 365 Finance pomoću modula **Računi koji se** plaćaju. Fakture dobavljača ne možete kreirati izravno u sustavu Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Postavljanje provjere fakture dobavljača

Ako je faktura dobavljača namijenjena kooperatu u sustavu, morate omogućiti parametar Ručna provjera prema PM-u Dataverse **.** Postavka mogućnosti određuje treba li fakturu dobavljača automatski potvrditi u sustavu Dataverse ili je potrebna ručna potvrda. Zaglavlje svake fakture dobavljača projekta uključuje istoimenu mogućnost. Po zadanome, mogućnost u zaglavlju svih faktura dobavljača projekta postavljena je na vrijednost koju ste ovdje postavili. Međutim, vrijednost možete obnoviti prema potrebi u zaglavlju pojedinačnih faktura dobavljača.

Ako je mogućnost postavljena na **Da**, faktura dobavljača kreirana u odjeljku Financije i sinkronizirana s Dataverse ima **status Skica**. Račun zatim voditelj projekta mora provjeriti i provjeriti te potvrditi fakturu prije nego što se obradi i proknjiži na određene račune projekta i analitike u financijskim financijama.

Ako je mogućnost postavljena na **Ne**, faktura dobavljača automatski se potvrđuje. Daljnje radnje nisu potrebne.

Da biste postavili provjeru fakture dobavljača, slijedite ove korake.

1. U odjeljku Financije idite na **Upravljanje projektima i računovodstvene parametre upravljanja projektima i računovodstva za** \> **upravljanje projektima i računovodstvo.** \> **·**
1. **Na kartici Financije** postavite opciju Ručna **provjera od strane PM-a potrebna** je opcija **Da** ako pravila tvrtke zahtijevaju provjeru faktura dobavljača kooperanta. Ako provjera od strane voditelja projekta nije potrebna u Dataverse sustavu, ostavite skup mogućnosti **broju**. Prema zadanim postavkama postavka će se koristiti na stranici Faktura **dobavljača na čekanju**.

> [!NOTE]
> Fakture dobavljača kreirane za kooperante u sustavu Dataverse mogu se ispravno obraditi samo ako **je potrebna** mogućnost Ručna provjera putem PM-a postavljena na **Da**. Iznose troškova vremena, materijala i troškova koje kreiraju kooperanti upravitelj projekta može ručno uskladiti s recima fakture dobavljača samo ako je ta mogućnost postavljena na **Da**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Postavljanje računa integracije nabave za fakture dobavljača

Kada se faktura dobavljača proknjiži u odjeljku Financije za projektne operacije – integrirano okruženje (nekontarno), financije se knjiže na račun integracije nabave. Sustav generira stvarne u sustavu Dataverse za proknjiženu fakturu. Te se stvarne vrijednosti knjiže u Finance pomoću temeljnice integracija projekta. Knjiženjem temeljnice integracije s projektom knjiži se stvarni trošak i stornira račun integracije nabave.

Da biste postavili račun integracije s nabavom za fakture dobavljača, slijedite ove korake.

1. U odjeljku Financije idite na **Upravljanje projektima i računovodstvene parametre upravljanja projektima i računovodstva za** \> **upravljanje projektima i računovodstvo.** \> **·**
1. Na kartici **Projektne operacije na kartici Angažman** korisnika sustava Dynamics 365 odaberite **Račun** integracije nabave materijala \>**·**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Kreiranje i knjiženje faktura dobavljača kooperanta

Kada službenik koji plaća račune primi fakturu od podizvođača, u financiranju se kreira nova faktura.

1. U odjeljku Financije otvorite **Fakture** \> **dugovanja na čekanju na fakturama** \> **dobavljača**.
1. U oknu **akcije** odaberite **Novo** da biste kreirali fakturu dobavljača.
1. U zaglavlju fakture u polju Račun **fakture** odaberite **Kooperant**.
1. Odaberite datum fakture.
1. Na kartici **Zaglavlje** postavite mogućnost Ručna **provjera prema PM-u na** **Da**. Zadana postavka ove opcije dolazi sa **stranice Parametri upravljanja projektima i računovodstva**. Međutim, može se promijeniti na razini fakture dobavljača.
1. Na BrzojKartici **Redak** fakture odaberite **Dodaj redak** da biste kreirali redak fakture dobavljača.
1. Odaberite kategoriju nabave kreiranu za retke kooperacije i unesite jediničnu cijenu, jedinicu mjerenja i količinu.
1. U odjeljku Reci fakture dobavljača na **kartici Projekt** odaberite projekt s kojim kooperant dijeli fakturu kooperanta.
1. Odaberite kategoriju projekta. Može biti bilo koje vrste artikla, troškova **·**, **materijala** ili **sati**. **·**
1. Odaberite ulogu samo ako je **odabrana kategorija projekta vrste Sat**.
1. Odaberite **Proknjiži** da biste proknjižili fakturu dobavljača.

Možete i kreirati fakturu dobavljača tako da odete na **Fakture za plaćanje** \> **Računi Otvorite fakture** \> **dobavljača** i odaberete **Novo.**

Kada se faktura dobavljača proknjiži, ona postaje dostupna za provjeru i obradu voditelja Dataverse projekta.

## <a name="vendor-invoice-processing-in-dataverse"></a>Obrada fakture dobavljača u Dataverse

U fakturi dobavljača kreiranoj u Dataverse sustavu neke vrijednosti polja dolaze iz fakture dobavljača koja je zabilježena u odjeljku Financije. Ostale vrijednosti su zadane vrijednosti koje dolaze iz podugovaratelja.

Sljedeća polja i srodni zapisi kopirat će se iz kooperanta u zaglavlje fakture dobavljača:

- Valuta
- Ugovorna jedinica
- Uvjeti plaćanja

U recima fakture dobavljača operacije projekta koriste sljedeće vrijednosti polja da bi unijele zadanu referencu retka kooperanta i kooperanta:

- Razred transakcije
- Uloga
- Kategorija transakcije
- Polja proizvoda
- Project
- Zadatak

> [!NOTE]
> Reci podugovaratelja s fiksnom cijenom nisu podržani u operacijama projekta.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
