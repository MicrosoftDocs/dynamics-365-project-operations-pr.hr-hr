---
title: Sinkroniziranje ugovora o projektu i projekata izravno iz aplikacije Project Service Automation u aplikaciju Financije
description: U ovoj se temi opisuje predložak i temeljni zadaci koji se upotrebljavaju za sinkronizaciju ugovora o projektu i projekata izravno iz sustava Microsoft Dynamics 365 Project Service Automation u uslugu Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 1a470fd86ceccd7b6058da6972399a6d6be2a991
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764810"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Sinkroniziranje ugovora o projektu i projekata izravno iz aplikacije Project Service Automation u aplikaciju Financije 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

U ovoj se temi opisuje predložak i temeljni zadaci koji se upotrebljavaju za sinkronizaciju ugovora o projektu i projekata izravno iz sustava Dynamics 365 Project Service Automation u uslugu Dynamics 365 Finance.

> [!NOTE] 
> Ako upotrebljavate verziju Enterprise Edition 7.3.0, morate instalirati zakrpu KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tijek podataka s usluge Project Service Automation na Financije

> [!NOTE]
> Prije nego što budete mogli upotrebljavati rješenje integracije iz usluge Project Service Automation na Financije, trebali biste se upoznati sa značajkom integracije podataka sustava Dynamics 365.

Rješenje za integraciju usluge Project Service Automation u Financije upotrebljava značajku Integracija podataka za sinkronizaciju podataka diljem instanci aplikacija Project Service Automation i Financije. Predložak integracije koji je dostupan uz značajku Integracija podataka omogućuje tijek podataka o ugovorima o projektu, projektima, redcima ugovora o projektu i kontrolnim točkama redaka ugovora o projektu iz usluge Project Service Automation u Financije.

Na slijedećoj slici prikazan je način na koji se podaci sinkroniziraju između usluge Project Service Automation i Financija.

[![Tijek podataka za integraciju usluge Project Service Automation s Financijama](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Predlošci i zadaci

Kako biste pristupili dostupnim predlošcima, u centru za administratore platforme Microsoft Power Apps odaberite **Projekti**, a zatim u gornjem desnom kutu odaberite **Novi projekt** za odabir javnih predložaka.

Predlošci u nastavku i temeljni zadaci upotrebljavaju se za sinkronizaciju ugovora o projektu i projekata iz usluge Project Service Automation u Financije:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integriranje s aplikacijom Dynamics 365 Project Service Automation v2.x
- **Naziv predloška u Integraciji podataka:** Projekti i ugovori (Project Service Automation u Financije)
- **Naziv zadataka u projektu:**

    - Ugovori o projektu iz aplikacije Project Service Automation u aplikaciju Financije
    - Projekti iz aplikacije Project Service Automation u aplikaciju Financije
    - Redci ugovora o projektu iz aplikacije Project Service Automation u aplikaciju Financije
    - Kontrolne točke redaka ugovora o projektu iz aplikacije Project Service Automation u aplikaciju Financije
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integriranje s aplikacijom Dynamics 365 Project Service Automation v3.x
U aplikaciji Project Service Automation dolazi do promjene sheme koja utječe na predložak kontrolne točke retka ugovora o projektu, a za integraciju aplikacije Project Service Automation v3.x sa sustavom Dynamics 365 potrebna je uporaba v2 verzije predloška.

- **Naziv predloška u Integraciji podataka:** Projekti i ugovori (Project Service Automation 3.x u Financije) – v2
- **Naziv zadataka u projektu:**

    - Ugovori o projektu iz aplikacije Project Service Automation u aplikaciju Financije
    - Projekti iz aplikacije Project Service Automation u aplikaciju Financije
    - Redci ugovora o projektu iz aplikacije Project Service Automation u aplikaciju Financije
    - Kontrolne točke redaka ugovora o projektu iz aplikacije Project Service Automation u aplikaciju Financije

Prije nego što dođe do sinkronizacije ugovora o projektu i projekata, morate sinkronizirati račune.

## <a name="entity-set"></a>Postavljanje entiteta

| Project Service Automation       | Financije                                                |
|----------------------------------|--------------------------------------------------------|
| Narudžbe                           | Entitet integracije za ugovor o projektu                |
| Projekti                         | Entitet integracije za projekt                         |
| Reci narudžbe                      | Entitet integracije za redak ugovora o projektu           |
| Kontrolne točke retka ugovora o projektu | Entitet integracije za kontrolnu točku retka ugovora o projektu |

## <a name="entity-flow"></a>Tijek entiteta

Ugovorima o projektu upravlja se u usluzi Project Service Automation, a sinkroniziraju se s Financijama kao ugovori o projektu. Kao dio predloška integracije, za projektni ugovor možete postaviti izvor integracije u Financijama.

Vremenom, materijalom i projektima s fiksnom cijenom upravlja se u aplikaciji Project Service Automation i sinkroniziraju se s aplikacijom Financije kao projekti. Kao dio integracije predloška, možete postaviti izvor integracije za projekt u aplikaciji Financije. Trenutačno su podržani samo projekti vremena i materijala te projekti s fiksnom cijenom.


Redcima ugovora o projektu upravlja se u usluzi Project Service Automation, a sinkroniziraju se s Financijama kao pravila za naplatu ugovora o projektu. Ako se način naplate razlikuje od zadane vrste projekta, sinkronizacija ažurira vrstu projekta za redak ugovora o projektu i grupu projekta.

Kontrolnim točkama redaka ugovora o projektu upravlja se u usluzi Project Service Automation, a sinkroniziraju se s Financijama kao kontrolne točke pravila za naplatu ugovora o projektu.

## <a name="project-service-automation-to-finance-integration-solution"></a>Rješenje za integraciju usluge Project Service Automation s Financijama

Polje **ID ugovora o projektu** dostupno je na stranici **Ugovori o projektu**. Ovo je područje napravljeno kao prirodni i jedinstveni ključ za podršku integraciji.

Kada se stvori novi ugovor o projektu, ako vrijednost **ID ugovora o projektu** već ne postoji, automatski se generira s pomoću niza brojeva. Vrijednost se sastoji od pokrate **ORD** nakon čega slijedi dodatak s nizom brojeva, a zatim sufiks od šest znakova. Evo primjera: **ORD-01022-Z4M9Q0**.

Polje **Broj projekta** dostupno je na stranici **Projekti**. Ovo je područje napravljeno kao prirodni i jedinstveni ključ za podršku integraciji.

Kada se stvori novi projekt, ako vrijednost **Broj projekta** već ne postoji, automatski se generira s pomoću niza brojeva. Vrijednost se sastoji od pokrate **PRJ** nakon čega slijedi dodatak s nizom brojeva, a zatim sufiks od šest znakova. Evo primjera: **PRJ-01049-CCNID0**.

Kada se primijeni rješenje integracije aplikacije Project Service Automation u Financije, skripta za nadogradnju postavlja polje **ID ugovora o projektu** za postojeće ugovore o projektu i polje **Broj projekta** za postojeće projekte u aplikaciji Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Preduvjeti i postavljanje mapiranja

- Prije nego što dođe do sinkronizacije ugovora o projektu i projekata, morate sinkronizirati račune.
- U svoj skup za povezivanje dodajte mapiranje polja integracijskog ključa za **msdyn\_organizationalunits** na **msdyn\_name \[Name\]**. Najprije ćete možda trebati dodati projekt u skup veza. Dodatne informacije potražite u članku [Integriranje podataka s platformom Common Data Service za aplikacije](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- U svoj skup za povezivanje dodajte mapiranje polja integracijskog ključa za **msdyn\_projects** na **msdynce\_projectnumber \[Project Number\]**. Najprije ćete možda trebati dodati projekt u skup veza. Dodatne informacije potražite u članku [Integriranje podataka s platformom Common Data Service za aplikacije](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** za ugovore o projektu i projekte se može se ažurirati na drugu vrijednost ili ukloniti iz mapiranja. Zadana vrijednost predloška je **Project Service Automation**.
- Mapiranje stavke **Uvjeti plaćanja** mora se ažurirati tako da u Financijama odražava valjane uvjete plaćanja. Također možete ukloniti mapiranje iz projektnog zadatka. Zadana karta vrijednosti ima zadane vrijednosti za pokazne podatke. Sljedeća tablica prikazuje vrijednosti u aplikaciji Project Service Automation.

    | Value | Opis   |
    |-------|---------------|
    | 1     | Neto 30        |
    | 2     | 2 % 10, neto 30 |
    | 3     | Neto 45        |
    | 4     | Neto 60        |

## <a name="power-query"></a>Power Query

Upotrijebite aplikaciju Microsoft Power Query za Excel kako biste filtrirali podatke ako su ispunjeni sljedeći uvjeti:

- Imate prodajne naloge u aplikaciji Dynamics 365 Sales.
- Imate više organizacijskih jedinica u aplikaciji Project Service Automation, a te će se organizacijske jedinice biti mapirati u više pravnih osoba u Financijama.

Ako morate upotrijebiti modul Power Query, slijedite ove smjernice:

- Predložak Projekti i ugovori (PSA u Fin i Ops) ima zadani filtar koji uključuje samo prodajne naloge vrste **Stavka posla (msdyn\_ordertype = 192350001)**. Ovaj filtar jamči da se ugovori o projektu ne stvaraju za prodajne naloge u Financijama. Ako stvorite vlastiti predložak, morate dodati ovaj filtar.
- Stvorite filtar aplikacije Power Query koji uključuje samo ugovorne tvrtke ili ustanove koje bi trebale biti sinkronizirane s pravnom osobom skupa integracijskih veza. Na primjer, ugovori o projektu koje imate s ugovornom organizacijskom jedinicom Contoso US trebali bi se sinkronizirati s pravnom osobom USSI, ali ugovori o projektu koje imate s ugovornom organizacijskom jedinicom Contoso Global trebali bi se sinkronizirati s pravnom osobom USMF. Ako ne dodate ovaj filtar u mapiranje zadataka, svi ugovori o projektu sinkronizirat će se s pravnom osobom koja je definirana za skup veza, bez obzira na organizacijsku jedinicu iz ugovora.

## <a name="template-mapping-in-data-integration"></a>Mapiranje predloška u integraciji podataka

> [!NOTE] 
> Polja **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** i **AddressZipCode** nisu uključena u zadano mapiranje za ugovore o projektu. Mapiranja možete dodati ako želite da se ti podaci sinkroniziraju za ugovore o projektu.
>
> Polja **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, i **ProjectType** nisu uključena u zadano mapiranje za projekte. Mapiranja možete dodati ako želite da se ti podaci sinkroniziraju za projekte.

Sljedeće slike prikazuju primjer mapiranja zadataka predloška u Integraciji podataka. Mapiranje prikazuje podatke polja koji će se sinkronizirati iz aplikacije Project Service Automation u Financije.

[![Mapiranje predloška ugovora o projektu](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Mapiranje predloška projekta](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Mapiranje predloška redaka ugovora o projektu](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Mapiranje predloška kontrolne točke redka ugovora o projektu](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Mapiranje kontrolnih točaka retka ugovora o projektu u projektima i ugovorima (PSA 3.x za Dynamics) – predložak v2:

[![Mapiranje kontrolne točke redka ugovora o projektu s pomoću verzije dva predloška](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]