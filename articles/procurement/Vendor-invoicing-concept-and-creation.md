---
title: Izrada faktura dobavljača
description: U ovom članku je opisan koncept faktura dobavljača i objašnjeno kako ih izraditi u aplikaciji Microsoft Dynamics 365 Project Operations.
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
# <a name="create-vendor-invoices"></a>Izrada faktura dobavljača

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Da biste koristili funkcionalnost opisanu u ovom članku, morate omogućiti značajku **Omogućivanje obrade stvarnih podataka podugovora pomoću aplikacije Project Operations za scenarije temeljene na resursima** u radnom prostoru **Upravljanje značajkama**.

Fakturiranje dobavljača u aplikaciji Microsoft Dynamics 365 Project Operations može se koristiti za bilježenje troškova isporuka usluga i/ili materijala na projektu koji su dovršili dobavljači.

Kada se usluge i/ili materijali podugovore s dobavljačem, podugovor predstavlja ugovor s tim dobavljačem. Kako dobavljač isporučuje usluge ili kako se materijali primaju i koriste na projektnim zadacima, bilježe se troškovi na projektu. Dobavljač tada povremeno šalje fakture. Te se fakture provjeravaju i usklađuju s troškovima koji su zabilježeni na projektu. Nakon završetka postupka provjere faktura dobavljača se potvrđuje i izdaje za plaćanje.

## <a name="scenarios-for-use"></a>Scenariji upotrebe

Fakture dobavljača u aplikaciji Project Operations mogu se koristiti za podršku dva različita scenarija:

- Klijenti koriste potpuna iskustva podugovaranja.
- Klijenti ne koriste potpuna iskustva podugovaranja, ali žele imati objedinjeni pregled troškova na projektima u aplikaciji Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klijenti se koriste svim iskustvima podugovaranja

Iskustva fakturiranja dobavljača pružaju način za provjeru unosa vremena, iskorištenost materijala i unosa troškova koji se odnose na podugovorene komponente i njihovo usklađivanje s redcima fakture dobavljača. Ovaj se postupak može upotrijebiti za provjeru točnosti redaka fakture dobavljača. Nakon dovršetka postupka provjere i potvrde fakture dobavljača, sustav poništava stvarne podatke koje su zabilježili zapisnici za odobreno vrijeme, troškove i iskorištenost materijala, a zatim stvara nove stvarne podatke o troškovima pomoću redaka fakture dobavljača.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klijenti koji se ne svim iskustvima podugovaranja, ali žele imati objedinjeni prikaz troškova projekata u aplikaciji Project Operations

Ako pratite proces podugovaranja u sustavu treće strane, možete zabilježiti troškove iz tog sustava u aplikaciji Project Operations kreiranjem faktura dobavljača koje ne upućuju na podugovore. Na taj način vaši voditelji projekta mogu imati jedinstveni, objedinjeni prikaz svih troškova na određenom projektu.

## <a name="create-vendor-invoices-in-project-operations"></a>Stvaranje faktura dobavljača u aplikaciji Project Operations

Fakture dobavljača stvaraju se u sustavu Dynamics 365 Finance pomoću modula **Dugovanja**. Ne možete izraditi fakture dobavljača izravno na platformi Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Postavljanje provjere fakture dobavljača

Ako je faktura dobavljača namijenjena podugovoru na platformi Dataverse, morate omogućiti parametar **Potrebna je ručna provjera voditelja projekta**. Postavka opcije određuje hoće li se faktura dobavljača automatski potvrditi na platformi Dataverse ili zahtijeva ručnu potvrdu. Zaglavlje svake fakture dobavljača projekta uključuje opciju istog naziva. Prema zadanim postavkama, opcija u zaglavlju svih faktura dobavljača projekta postavljena je na vrijednost koju ste postavili ovdje. Međutim, prema potrebi možete ažurirati vrijednost u zaglavlju pojedinačnih faktura dobavljača.

Ako je opcija postavljena na **Da**, faktura dobavljača koja se izrađuje u aplikaciji Finance i sinkronizira s platformom Dataverse ima status **Skica**. Fakturu zatim mora provjeriti voditelj projekta, te potvrditi, prije nego što se obradi i objavi na određenom projektu i računima glavne knjige u aplikaciji Finance.

Ako je opcija postavljena na **Ne**, faktura dobavljača se potvrđuje automatski. Daljnje radnje nisu potrebne.

Slijedite ove korake za postavljanje provjere fakture dobavljača.

1. U aplikaciji Finance idite na **Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Parametri upravljanja projektom i računovodstva**.
1. Na kartici **Financijski** postavite mogućnost **Potrebna je ručna provjera voditelja projekta** na **Da** ako pravila tvrtke zahtijevaju provjeru faktura dobavljača podizvođača. Ako nije potrebna provjera od strane voditelja projekta na platformi Dataverse, ostavite mogućnost postavljenu na **Ne**. Prema zadanom, postavka će se koristiti na stranici **Faktura dobavljača na čekanju**.

> [!NOTE]
> Fakture dobavljača koje su stvorene za podugovore na platformi Dataverse mogu se pravilno obraditi samo ako je opcija **Potrebna je ručna provjera voditelja projekta** postavljena na **Da**. Stvarne cijene vremena, materijala i troškova koje stvaraju podizvođači voditelj projekta može ručno uskladiti s redcima fakture dobavljača samo ako je ova opcija postavljena na **Da**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Postavljanje računa za integraciju nabave za fakture dobavljača

Kada se faktura dobavljača knjiži u aplikaciji Finance za Project Operations – integrirano okruženje (bez zaliha), financije se knjiže na račun integracije nabave. Sustav generira stvarne podatke na platformi Dataverse za proknjiženu fakturu. Ovi stvarni podaci knjiže se u aplikaciji Finance pomoću dnevnika integracije projekta. Knjiženjem dnevnika integracije projekta knjiži se stvarni trošak i poništava račun integracije nabave.

Slijedite ove korake za postavljanje računa za integraciju nabave za fakture dobavljača.

1. U aplikaciji Finance idite na **Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Parametri upravljanja projektom i računovodstva**.
1. Na kartici **Project operations u Dynamics 365 customer engagement** odaberite **Materijali** \> **Račun integracije nabave**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Stvaranje i knjiženje faktura dobavljača podugovora

Kada službenik za dugovanja primi fakturu od podizvođača, u aplikaciji Finance se stvara nova faktura.

1. U aplikaciji Finance idite na **Dugovanja** \> **Fakture** \> **Fakture dobavljača na čekanju**.
1. U **Oknu akcije** odaberite **Novo** za izradu fakture dobavljača.
1. Na zaglavlju fakture, u polju **Račun fakture**, odaberite **Podizvođač**.
1. Odaberite datum fakture.
1. Na kartici **Zaglavlje** postavite mogućnost **Potrebna je ručna provjera voditelja projekta** na **Da**. Zadana postavka ove opcije dolazi sa stranice **Parametri upravljanja projektom i računovodstva**. Međutim, može se promijeniti na razini fakture dobavljača.
1. Na brzoj kartici **Redak fakture** odaberite **Dodaj redak** za stvaranje retka fakture dobavljača.
1. Odaberite kategoriju nabave koja je stvorena za retke podugovora te unesite jediničnu cijenu, mjernu jedinicu i količinu.
1. U odjeljku redaka fakture dobavljača, na kartici **Projekt**, odaberite projekt za koji podizvođač dijeli fakturu za podugovor.
1. Odaberite kategoriju projekta. Može biti bilo koji vrste **Stavka**, **Trošak**, **Materijali** ili **Sati**.
1. Odaberite ulogu samo ako je odabrana kategorija projekta vrste **Sat**.
1. Odaberite **Uknjiži** za knjiženje fakture dobavljača.

Umjesto toga, možete izraditi fakturu dobavljača tako da odete na **Dugovanja** \> **Fakture** \> **Otvorene fakture dobavljača** i odaberete **Novo**.

Kada se uknjiži faktura dobavljača, postaje dostupna voditelju projekta za provjeru i obradu na platformi Dataverse.

## <a name="vendor-invoice-processing-in-dataverse"></a>Obrada fakture dobavljača na platformi Dataverse

U fakturi dobavljača koja je stvorena na platformi Dataverse, neke vrijednosti polja dolaze iz fakture dobavljača koja je zabilježena u aplikaciji Finance. Ostale vrijednosti su zadane vrijednosti koje dolaze iz podugovora.

Sljedeća polja i povezani zapisi kopirat će se iz podugovora u zaglavlje fakture dobavljača:

- Valuta
- Ugovorna jedinica
- Uvjeti plaćanja

Na redcima fakture dobavljača, Project Operations koristi sljedeće vrijednosti polja za unos zadanog podugovora i reference retka podugovora:

- Razred transakcije
- Uloga
- Kategorija transakcije
- Polja proizvoda
- Project
- Zadatak

> [!NOTE]
> Redci podugovora s fiksnom cijenom nisu podržani u aplikaciji Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
