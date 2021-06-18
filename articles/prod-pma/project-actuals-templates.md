---
title: Sinkronizacija stvarnih podataka o projektu izravno iz aplikacije Project Service Automation u dnevnik integracije projekta za objavljivanje na usluzi Finance and Operations
description: U ovoj se temi opisuju predlošci i temeljni zadaci koji se upotrebljavaju za sinkronizaciju stvarnih podataka o projektu izravno iz sustava Microsoft Dynamics 365 Project Service Automation u uslugu Finance and Operations.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: db63413456e4b91d308af9c1103000d5cdc693f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999887"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Sinkronizacija stvarnih podataka o projektu izravno iz aplikacije Project Service Automation u dnevnik integracije projekta za objavljivanje na usluzi Finance and Operations

[!include[banner](../includes/banner.md)]

U ovoj se temi opisuju predlošci i temeljni zadaci koji se upotrebljavaju za sinkronizaciju stvarnih podataka o projektu izravno iz sustava Dynamics 365 Project Service Automation u uslugu Dynamics 365 Finance.

Predložak sinkronizira transakcije iz aplikacije Project Service Automation u izvedbenu tablicu u Financijama. Nakon završetka sinkronizacije, **morate** uvesti podatke iz izvedbene tablice u dnevnik integracije.

> [!NOTE]
> - Integracija stvarnih podataka projekata dostupna je počevši od verzije 8.0.1.
> - Ako upotrebljavate verziju Enterprise Edition 7.3.0, nakon što instalirate zakrpe KB 4132657 i KB 4132660 moći ćete upotrebljavati predloške za integraciju projektnih zadataka, kategorija transakcija izdataka, procjena sati rada, procjena izdataka i stvarnih podataka te za konfiguraciju funkcije zaključavanja. Ako morate vratiti zadane računovodstvene distribucije, preporučujemo da instalirate i zakrpu KB 4131710.
> - Ako upotrebljavate verziju 7.3.0 i transakcije naknada prenosite iz usluge Project Service Automation, morate instalirati zakrpu KB 4345320 kako biste te naknade uključili u fakturu projekta.
> - Ako na vrijeme unosite iznose PDV-a ili u transakcije izdataka u aplikaciju Project Service Automation, morate instalirati ažuriranje 7 aplikacije Project Service Automation. U suprotnom, stvarni porezni podaci neće biti povezani sa stvarnim podacima o vremenu ili izdacima i oni se neće sinkronizirati s Financijama. Za dodatne informacije obratite se Službi podrške.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tijek podataka s usluge Project Service Automation na Financije

Rješenje za integraciju usluge Project Service Automation u Financije upotrebljava značajku Integracija podataka za sinkronizaciju podataka diljem instanci aplikacija Project Service Automation i Financije. Predlošci integracije koji su dostupni sa značajkom Integracija podataka omogućuje protok podataka o stvarnim podacima projekta iz aplikacije Project Service Automation u Financije.

Na slijedećoj slici prikazan je način na koji se podaci sinkroniziraju između usluge Project Service Automation i Financija.

[![Tijek podataka za integraciju usluge Project Service Automation s aplikacijom Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Stvarni podaci o projektu iz aplikacije Project Service Automation

### <a name="template-and-tasks"></a>Predlošci i zadaci

Kako biste pristupili dostupnim predlošcima, u centru za administratore platforme Microsoft Power Apps odaberite **Projekti**, a zatim u gornjem desnom kutu odaberite **Novi projekt** za odabir javnih predložaka.

Predložak u nastavku i temeljni zadaci upotrebljavaju se za sinkronizaciju stvarnih podataka o projektu iz usluge Project Service Automation u Financije:

- **Naziv predloška u Integraciji podataka:** Stvarni podaci o projektu (PSA u Fin i Ops)
- **Naziv zadataka u projektu:**

    - Ostvarenja
    - TransactionConnections

### <a name="entity-set"></a>Postavljanje entiteta

| Project Service Automation | Financije                                   |
|----------------------------|----------------------------------------------------------|
| Ostvarenja                    | Entitet integracije za stvarne podatke o projektu                   |
| Veze transakcija    | Entitet integracije za odnose transakcije projekta |

### <a name="entity-flow"></a>Tijek entiteta

Stvarnim podacima o projektu upravlja se u usluzi Project Service Automation, a sinkroniziraju se s dnevnikom integracije projekta u Financijama. Računovodstvo će se primijeniti na temelju zadanih financijskih dimenzija i postavki knjiženja.

### <a name="prerequisites"></a>Preduvjeti

Prije nego što dođe do sinkronizacije stvarnih podataka, morate konfigurirati parametre integracije aplikacije Project Service Automation i sinkronizirati kategorije projekata, projektnih zadataka i transakcija troškova projekta.

### <a name="power-query"></a>Power Query

U predlošku stvarnih podataka o projektu morate upotrijebiti uslugu Microsoft Power Query za Excel kako biste izvršili ove zadatke:

- Transformirali vrstu transakcije iz aplikacije Project Service Automation u ispravnu vrstu transakcije u Financijama. Ta je transformacija već definirana u predlošku stvarnih podataka o projektu (PSA u Fin i Ops).
- Transformirali vrstu naplate iz aplikacije Project Service Automation u ispravnu vrstu naplate u Financijama. Ta je transformacija već definirana u predlošku stvarnih podataka o projektu (PSA u Fin i Ops). Zatim se vrsta naplate mapira u svojstvo retka, na temelju konfiguracije na stranici **Parametri za integraciju aplikacije Project Service Automation**.
- Filtrirajte do određenih organizacijskih jedinica resursa koje se moraju sinkronizirati s ovim predloškom.
- Ako će se stvarni podaci o vremenu unutar tvrtke ili o izdacima unutar tvrtke sinkronizirati s Financijama, morate pretvoriti ugovornu organizacijsku jedinicu u ispravnu pravnu osobu u Financijama. U predlošku Stvarni podaci o projektu (PSA u Fin i Ops) uvjetni je stupac definiran na temelju pokaznih podataka. Morate ažurirati zadnji umetnuti uvjetni stupac na ispravne pravne osobe. U suprotnom, može se dogoditi integracijska pogreška ili se u Financije mogu uvesti netočne stvarne transakcije.
- Ako se stvarni podaci za vrijeme ili izdatke unutar tvrtki neće sinkronizirati s Financijama, morate iz svog predloška izbrisati uvjetni stupac koji ste posljednji umetnuli. U suprotnom, može se dogoditi integracijska pogreška ili se u Financije mogu uvesti netočne stvarne transakcije.

#### <a name="contract-organizational-unit"></a>Ugovorne organizacijskih jedinica
Kako biste u predlošku ažurirali umetnuti uvjetni stupac, kliknite strelicu **Mapiraj** kako biste otvorili mapiranje. Odaberite vezu **Napredni upit i filtriranje** kako biste otvorili modul Power Query.

- Ako upotrebljavate zadani predložak stvarni podaci o projektu (PSA u Fin i Ops), u modulu Power Query odaberite posljednji **Umetnuti uvjet** iz odjeljka **Primijenjeni koraci**. U unosu **Funkcija** zamijenite **USSI** nazivom pravne osobe koji bi se trebao upotrijebiti s integracijom. Dodajte dodatne uvjete u unos **Funkcija** prema vašem zahtjevu i ažurirajte uvjet **drugo** iz **USMF** ispravnoj pravnoj osobi.
- Ako stvarate novi predložak, morate dodati stupac za podršku vremenu i izdacima unutar tvrtke. Odaberite **Dodaj uvjetni stupac** i unesite naziv novog stupca, kao što je **LegalEntity**. Unesite uvjet za stupac, gdje, ako **msdyn\_contractorganizationalunitid.msdyn\_name** je \<organizational unit\>, onda je \<enter the legal entity\>; inače je prazno.

### <a name="template-mapping-in-data-integration"></a>Mapiranje predloška u integraciji podataka

Sljedeće slike prikazuju primjer mapiranja zadataka predloška u Integraciji podataka. Mapiranje prikazuje podatke polja koji će se sinkronizirati iz aplikacije Project Service Automation u Financije.

[![Mapiranje predloška – Stvarni podaci](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Mapiranje predloška – Transakcijske veze](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Uvoz iz izvedbene tablice nakon integracije iz aplikacije Project Service Automation

Nakon sinkronizacije stvarnih podataka iz aplikacije Project Service Automation u Financije, mora se pokrenuti uvoz iz povremenog postupka izvedbene tablice. Ovim će se postupkom uvesti projektne transakcije iz izvedbene tablice u dnevnik integracije aplikacije Project Service Automation, gdje se primjenom računovodstva uvezene transakcije mogu knjižiti. Preporučujemo da ovaj postupak pokrenete u skupnom načinu; po želji se može postaviti da se izvršava kao skupno ponavljanje.

## <a name="update-actuals-from-finance"></a>Ažuriranje stvarnih podataka iz Financija

### <a name="template-and-tasks"></a>Predlošci i zadaci

Sljedeći predložak i temeljni zadaci upotrebljavaju se za sinkronizaciju broja kupona i PDV-a za proknjižene projektne transakcije iz Financija u aplikaciju Project Service Automation:

- **Naziv predloška u Integraciji podataka:** Ažuriranje stvarnih podataka o projektu (Fin i Ops u PSA)
- **Naziv zadataka u projektu:**

    - Ostvarenja 
    - TransactionConnections

### <a name="entity-set"></a>Postavljanje entiteta

| Financije                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Entitet integracije za stvarne podatke o projektu                   | Ostvarenja                    |
| Entitet integracije za odnose transakcije projekta | Veze transakcija    |

### <a name="entity-flow"></a>Tijek entiteta

Stvarnim podacima o projektu upravlja se u usluzi Project Service Automation, a sinkroniziraju se s dnevnikom integracije projekta u Financijama. Nakon što se stvarni podaci proknjiže u Financijama, ažurirat će se u aplikaciji Project Service Automation s pomoću broja kupona iz Financija. Ako se u Financijama doda PDV, novi stvarni porezni podaci stvaraju se u aplikaciji Project Service Automation.

### <a name="power-query"></a>Power Query

U predlošku za ažuriranje stvarnih podataka o projektu morate upotrijebiti modul Power Query kako biste izvršili ove zadatke:

- Transformirali vrstu transakcije u Financijama u ispravnu vrstu transakcije u aplikaciji Project Service Automation. Ta je transformacija već definirana u predlošku za ažuriranje stvarnih podataka o projektu (Fin Ops u PSA).
- Transformirali vrstu naplate u Financijama u ispravnu vrstu naplate u aplikaciji Project Service Automation. Ta je transformacija već definirana u predlošku za ažuriranje stvarnih podataka o projektu (Fin Ops u PSA).

### <a name="template-mapping-in-data-integration"></a>Mapiranje predloška u integraciji podataka

Sljedeće slike prikazuju primjer mapiranja zadataka predloška u Integraciji podataka. Mapiranje prikazuje podatke polja koji će se sinkronizirati iz Financija u aplikaciju Project Service Automation.

[![Mapiranje predloška – Ažuriranje stvarnih podataka](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Mapiranje predloška – Ažuriranje transakcije](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]