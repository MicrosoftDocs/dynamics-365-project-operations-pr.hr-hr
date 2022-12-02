---
title: Vanjsko planiranje
description: U ovom se članku navode informacije o vanjskom planiranju.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736982"
---
# <a name="external-scheduling"></a>Vanjsko planiranje

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Način rada vanjskog planiranja omogućuje vam nativno izrađivanje, ažuriranje i brisanje entiteta povezanih sa strukturnom analizom rada (WBS; work breakdown structure), no bez trenutačnih ograničenja koje nameće rješenje Microsoft Project for the Web. Također pruža ograničenu provjeru valjanosti. Ovaj način rada trebaju koristiti samo sljedeći korisnici:

- Korisnici koji imaju alate koji su potrebni za definiranje WBS-a izvan logike planiranja koju pruža aplikacija Project Operations
- Klijenti koji moraju upravljati hijerarhijom rasporeda, ovisnostima ili trajanjem zadatka

> [!IMPORTANT]
> Podaci koji nisu ispravno uneseni u entitete povezane s WBS-om možda se neće prikazati u mreži usklađivanja resursa, mreži procjena, mreži praćenja ili mreži dodjele resursa.

## <a name="configuration"></a>Konfiguracija

Ova je značajka omogućena prema zadanim postavkama. Međutim, na gotovoj glavnoj stranici za projekte, povezano polje nije vidljivo prema zadanim postavkama. Da biste omogućili polje, na portalu Maker Portal otvorite glavnu stranicu za entitet projekta, odaberite polje **Modul za planiranje**, a zatim promijenite polje u **Vidljivo prema zadanim postavkama**. Ako se ne koristite gotovom glavnom stranicom za projekte, uredite svoju postojeću stranicu i dodajte joj polje **Modul za planiranje**.

## <a name="settings"></a>Postavke

Da biste se koristili načinom rada vanjskog planiranja, prvo morate izraditi novi projekt i na padajućem izborniku na glavnoj stranici projekta odabrati modul planiranja **Planirano izvana**. Nakon što je ovaj način rada postavljen za projekt, ne može se promijeniti.

## <a name="viewing-the-wbs"></a>Pregledavanje WBS-a

Ako je projekt planiran izvana, pristup rješenju Project for the Web ograničen je za taj projekt. Da biste vidjeli WBS, morate otići na rešetku praćenja, gdje je prikazan cijeli WBS.

## <a name="creating-and-editing-the-wbs"></a>Izrada i uređivanje WBS-a

Ako je za projekt omogućeno vanjsko planiranje, morate definirati podatke za sve entitete povezane s WBS-om, uključujući zadatke, članove tima, dodjele resursa i ovisnosti.

Sljedeća ilustracija prikazuje podatkovni model za planiranje projekta.

![Podatkovni model planiranja projekta.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Funkcionalna ograničenja

Sljedeće operacije nisu dopuštene na projektima planiranima izvana.

### <a name="project-planning"></a>Planiranje projekta

- **Kopiraj projekt** – ova radnja nije podržana na projektima planiranima izvana.
- **Premjesti projekt** – promjene datuma početka projekta neće pomaknuti početak zadataka ili dodjele resursa u WBS-u.
- **Ažuriranje voditelja projekta** – promjenama voditelja projekta na glavnoj stranici projekta neće se automatski izraditi novi član projektnog tima sve dok se projekt ne pretvori.
- **Ažuriranje predloška radnog sata projekta** – promjene predloška radnog sata projekta neće ponovno izračunati raspored projekta.
- **Konture dodjele resursa** – izrada dodjela resursa neće automatski ažurirati polje **mdyn\_PlannedWork**. Ovo se polje upotrebljava za pohranjivanje kontura za rad dodjele resursa. Ako prikazujete vremenski razrađeni rad u rešetki dodjele resursa ili mreži usklađivanja resursa, morate definirati valjane konture dodjele resursa. Te konture moraju biti ispravno formatirane tako da pokreću i izračun kontura troškova i izračun kontura prodajne cijene. Preporučujemo da izradite testni projekt planiran za rješenje Project for the Web te da zatim pregledate povezane podatke kako biste potvrdili zahtjeve i formatiranje.

### <a name="resource-management"></a>Upravljanje resursima

- **Ispunjenje generičkog resursa** – ispunjenje generičkih resursa nije podržano za vanjski planirane projekte. Pokušaji ispunjenja aktivnih otvorenih zahtjeva izradit će nove članove projektnog tima, no neće izbrisati generičkog člana tima niti zamijeniti generičkog člana tima na bilo kojem postojećem dodjeljivanju resursa.
- **Izbriši člana tima** – brisanje člana tima neće automatski izbrisati dodjele resursa.

### <a name="quoting-and-contracting"></a>Sastavljanje ponuda i ugovaranje

- **Uvoz pojedinosti retka ponude i retka ugovora** – kada se pojedinosti retka ponude ili retka ugovora uvoze iz projekta, ispitana je mogućnost aplikacije da podrži maksimalno samo 500 zadataka u WBA-u, na temelju ograničenja od 20 dodjela po zadatku.

### <a name="actuals-and-invoicing"></a>Stvarni podaci i fakturiranje

- Iako nema promjena u postojećim provjerama valjanosti između WBS-a i financijskih transakcija, važno je da se uskladite s gotovim podatkovnim modelom kako biste se pobrinuli da se sve transakcije niže razine izvršavaju prema očekivanjima.
