---
title: Konfiguriranje materijala koji nisu na zalihi i faktura dobavljača na čekanju
description: U ovom se članku objašnjava način omogućivanja materijala koji nije na zalihi i faktura dobavljača na čekanju.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6473ef3510f0d3641a2d61b6a1b1f28980993277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913749"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Konfiguriranje materijala koji nisu na zalihi i faktura dobavljača na čekanju

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

## <a name="minimum-version-requirement"></a>Zahtjevi za minimalnom verzijom

Uporaba materijala koji nije na zalihi i faktura dobavljača na čekanju u aplikaciji Dynamics 365 Project Operations za scenarije koji se temelje na resursima / bez zaliha zahtijevaju sljedeće verzije:

Rješenja aplikacije Dynamics 365 Dataverse:

- Project Operations – 4.9.0.221 ili novije
- Rješenje za organizaciju aplikacije dvostrukog pisanja – 2.2.2.23 ili novije

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) ili novije. Provjerite je li vaše okruženje aplikacije Financije aktualno i primjenjuju li se sva ažuriranja kvalitete kako bi se udovoljilo zahtjevima za minimalnu verziju.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Pokretanje karte s dvostrukim pisanjem za materijale koji nisu na zalihi i integraciju računa dobavljača

Ovaj odjeljak pruža informacije o određenim kartama potrebnim za materijale koji nisu na zalihi i račune dobavljača. Provjerite izvršavaju li se karte preduvjeta navedene u članku [Priprema novog okruženja](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) u vašem okruženju.

1. Idite na uslugu Lifecycle Services (LCS), pomaknite se do svog LCS projekta i idite na stranicu **Pojedinosti okruženja**.
2. U odjeljku **Podaci o okruženju platforme Common Data Service** odaberite **Veza na CDS za aplikacije**. Nakon što odaberete vezu, bit ćete preusmjereni na popis entiteta u mapiranjima.
3. Provjerite rade li sljedeće karte. Ako se ne izvršavaju, pokrenite ih i uključite sve povezane karte tablice.

    - Izdavanje različitih proizvoda (proizvodi) od strane CDS-a
    - Dobavljači v2 (msdyn_vendors)
    - Tablica aplikacije Project Operations za procjene materijala (msdyn_estimatelines)
    - Entitet izvoza fakture dobavljača projekata integracije aplikacije Project Operations (msdyn_projectvendorinvoices)
    - Entitet izvoza retka fakture dobavljača projekata integracije aplikacije Project Operations (msdyn_projectvendorinvoicelines)
    - Stvarni podaci aplikacije Project Operations (msdyn_actuals). Obvezno pokrenite verziju karte 1.0.0.14 ili noviju. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Novu verziju karte možete aktivirati odabirom **Verzija karte tablice**, a zatim spremanjem odabrane verzije.

Ako upotrebljavate standardne pokazne podatke, možda ćete također trebati zaustaviti i ponovo pokrenuti sljedeće mape entiteta uz početnu sinkronizaciju:
  - Dani plaćanja CDS V2 (msdyn_paymentdays)
  - Raspored plaćanja (msdyn_paymentschedules)
  - Uvjeti plaćanja (msdyn_paymentterms)
  - Grupe dobavljača (msdyn_vendorgroups)
  - Jedinice (uom)

> [!NOTE]
> Početna sinkronizacija za grupe i jedinice dobavljača možda neće uspjeti za nekoliko zapisa u postojećem skupu pokaznih podataka. Neuspjehe možete zanemariti jer vas neće spriječiti pri uporabi pokaznih podataka uz aplikaciju Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Konfiguriranje preduvjeta na platformi Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Aktivirajte tijek rada za stvaranje računa na temelju entiteta dobavljača

Rješenje združenog dvostrukog pisanja osigurava [Glavnu integraciju dobavljača](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Kao preduvjet za ovu značajku, podaci o dobavljaču moraju se stvoriti u entitetu **Računi**. Aktivirajte postupak tijeka rada predloška za stvaranje dobavljača u tablici **Računi** kako je opisano u članku [Prebacivanje između dizajna dobavljača](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Postavljanje proizvoda koji će se stvoriti kao aktivni

Materijali koji nisu na zalihi u aplikaciji Financije moraju biti konfigurirani kao **Objavljeni proizvodi**. Rješenje združenog dvostrukog pisanja osigurava gotovu [Integraciju proizvoda objavljenih u katalogu proizvoda platforme Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Prema zadanim postavkama, proizvodi iz aplikacije Financije sinkroniziraju se s platformom Dataverse u stanju skice. Kako biste proizvod sinkronizirali u aktivno stanje, tako da se može izravno upotrebljavati u dokumentima o uporabi materijala ili na fakturama dobavljača na čekanju, idite na **Sustav** > **Administracija** > **Administracija sustava** > **Postavke sustava** i na kartici **Prodaja** mogućnost **Stvori proizvode u aktivnom stanju** postavite na **Da**.

## <a name="configure-prerequisites-in-finance"></a>Konfiguriranje preduvjeta u aplikaciji Financije

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Omogućivanje tipke značajke za fakture dobavljača na čekanju

Poduzmite sljedeće korake kako biste omogućili funkcionalnost za dodavanje pojedinosti projekta na retke faktura dobavljača na čekanju.

1. U aplikaciji Financije, idite na radni prostor **Upravljanje značajkama**.
2. Na popisu značajki pronađite značajku **Omogući fakture dobavljača na čekanju u aplikaciji Project Operations za scenarije koji se temelje na resursima / bez zaliha** i odaberite **Omogući**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Definiranje grupa kategorija i kategorija projekata za stavke

Konfigurirajte barem jednu grupu kategorija za vrstu transakcije **Stavka** i najmanje jednu kategoriju projekta koja upotrebljava ovu grupu. Dodatne informacije potražite u članku [Konfiguracija kategorija projekata](../project-accounting/configure-project-categories.md#category-groups).

Pregledajte profile troškova i prihoda projekta i konfigurirajte postavke računovodstvenog knjiženja za transakcije stavki. Dodatne informacija potražite u članku [Konfiguriranje računovodstva za naplative projekte](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Postavljanje upisanog proizvoda

U aplikaciji Project Operations možete bilježiti procjene i uporabu materijala za kataloške proizvode koji su konfigurirani u objavljenom katalogu proizvoda i za upisane proizvode. Uporaba upisanih proizvoda zahtijeva jedan objavljeni proizvod koji je u tu svrhu konfiguriran u aplikaciji Financije. Poduzmite sljedeće korake za konfiguriranje upisanih proizvoda. Ponovite ove korake u svakoj pravnoj osobi koja upotrebljava aplikaciju Project Operations za scenarije resursa / bez zalihe.

1. U aplikaciji Financije idite na **Upravljanje informacijama o proizvodu** > **Proizvodi** > **Objavljeni proizvodi** i odaberite **Novi**.
2. U polju **Vrsta proizvoda** odaberite **Stavka** i u polju **Podvrsta proizvoda** odaberite **Proizvod**.
3. Unesite broj proizvoda (UPISAN) i naziv proizvoda (upisani proizvod).
4. Odaberite grupu modela stavke. Provjerite ima li odabrana grupa modela stavke polje **Pravila o zalihama proizvoda na zalihi** postavljeno na **Netočno**.
5. Odaberite vrijednosti u poljima **Grupa predmeta**, **Grupa za veličinu pohrane** i **Grupa za veličinu praćenja**. Upotrijebite mogućnost **Veličina prostora za pohranu** samo za stavku **Web-mjesto** i u polju **Veličine koje se prate** odaberite **Nijedna**.
6. Odaberite vrijednosti u poljima **Jedinica zalihe**, **Jedinica nabave** i **Jedinica prodaje**, a zatim spremite promjene.
7. U kartici **Planiranje** postavite zadane postavke redoslijeda, a na kartici **Zalihe** postavite zadano mjesto i skladište.
8. Idite na **Upravljanje projektima i računovodstvo** > **Postavke** > **Upravljanje projektom i računovodstveni parametri** i otvorite **Project Operations u aplikaciji Dynamics 365 Dataverse**. 
9. Na kartici **Materijali**, u polju **Upisni proizvod**, odaberite proizvod koji ste stvorili.
10. U mapi web-mjesta vašeg okruženja platforme Dataverse otvorite entitet **Proizvodi** i pronađite zapis o upisu proizvoda. 
11. Otvorite pojedinosti o zapisu i stanje proizvoda postavite na **Povučeno iz uporabe**. Ovo stanje proizvoda sprječava da netko slučajno upotrebljava ovaj zapis izravno u procjenama materijala i dokumentima o uporabi.

### <a name="set-up-a-procurement-integration-account"></a>Postavljanje računa za integraciju nabave

Račun za integraciju nabave upotrebljava se kao račun za obračun pri knjiženju fakture dobavljača na čekanju s linijama dodijeljenim projektu.

Kada sustav knjiži fakturu dobavljača na čekanju, ovaj se račun upotrebljava za iznos troškova projekta. Pojedinosti o fakturi dobavljača obrađuju se na platformi Dataverse i stvara se odgovarajući stvarni projekt. Podaci iz stvarnog projekta dodaju se u dnevniku integracije aplikacije Project Operations. Kada objavite dnevnik integracije, iznos se briše s računa integracije nabave i bilježi na trošak projekta.

1. Kako biste postavili račun za integraciju nabavite, idite na **Upravljanje projektima i računovodstvo** > **Postavke** > **Upravljanje projektom i računovodstveni parametri** i otvorite **Project Operations u aplikaciji Dynamics 365 Dataverse**. 
2. Odaberite karticu **Materijali** i odaberite vrijednost u polju **Račun za integraciju nabave**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Postavljanje zadane kategorije projekta za stavku

1. U aplikaciji Financije, idite na **Upravljanje projektima i računovodstvo** > **Postavke** > **Upravljanje projektom i računovodstveni parametri** i otvorite **Project Operations u aplikaciji Dynamics 365 Dataverse**. 
2. Na kartici **Zadane postavke kategorije projekta**, u polju **Stavka**, odaberite vrijednost. Ova kategorija projekta upotrebljava se za materijalne transakcije ako kategorija projekta nije postavljena u zapis stvarnih podataka o projektu.
