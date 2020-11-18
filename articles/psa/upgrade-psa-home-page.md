---
title: Nadogradnja početne stranice
description: Ova tema pokazuje gdje pronaći važne informacije o novim i promijenjenim značajkama u sustavu Dynamics 365 Project Service Automation i procesu nadogradnje na najnoviju verziju.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 29e7b519b61e8709c025e9906d04aed0156f65eb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073469"
---
# <a name="upgrade-home-page"></a>Nadogradnja početne stranice

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Nadogradnja aplikacije PSA s verzije 2.x ili 1.x na verziju 3.x

### <a name="new-instances"></a>Nove instance

Od 17. svibnja 2019. godine kada je aplikacija Project Service Automation odabrana tijekom pripreme nove instance, prema zadanim je postavkama instalirana verzija 3.x.

### <a name="existing-instances"></a>Postojeće instance

Klijenti koji su imali instancu PSA verzije 2.x i trebali su se nadograditi na verziju 3.x, što je verzija PSA koja je temeljena na objedinjenom klijentskom sučelju (UCI), ranije su se morali obratiti podršci i pružiti pojedinosti o svojoj instanci, tako da podrška može omogućiti instancu za nadogradnju na verziju 3.x. Od 1. ožujka 2020. klijenti koji imaju instancu PSA verzije 2.x i trebaju je nadograditi na verziju 3.x, moći će nadograditi svoje instance izravno s portala administratora bez potrebe za obraćanjem Microsoftovoj službi za podršku.  

> [!NOTE]
> Verzija 3.x aplikacije PSA uključuje značajne promjene. Izgrađena je na okviru objedinjenog sučelja kako bi pomogla u pružanju poboljšanog korisničkog doživljaja. Redizajnirana aplikacija donosi dosljedno, objedinjeno korisničko sučelje (UI), a slijedi načela responzivnog dizajna za optimalan prikaz na bilo kojoj veličini zaslona ili bilo kojem uređaju. Aplikacija donosi i druge promjene. Neka od područja koja su promijenjena uključuju određivanje cijena, rezervacije i dodjeljivanje resursa, vremena, troškova i odobrenja.

Prije početka postupka nadogradnje preporučujemo da dovršite sljedeće zadatke:

- Provjerite jesu li sustav Dynamics 365 Field Service i aplikacija Project Service Automation instalirani na identificiranoj nstanci. Ako su instalirana oba rješenja, trebali biste planirati nadogradnju prije nego što nastavite uobičajeno korištenje instance.
- Pažljivo pregledajte sljedeće teme. Svijest i razumijevanje promjena između verzija pomoći će vam s postupkom nadogradnje. Te teme pružaju informacije o glavnim promjenama u aplikaciji PSA, zajedno s razmatranjima i preporukama za planiranje nadogradnje na verziju 3.x.

    - [Što je novo ili promijenjeno u aplikaciji Project Service Automation, verzija 3](whats-new-changed-v3.md)
    - [Razmatranja nadogradnje – Project Service Automation, verzija 2.x ili 1.x na verziju 3](upgrade-v3.md)

- Nadogradite instancu za testiranje da biste procijenili promjene u implementaciji prije nadogradnje proizvodne instance.

Nakon što pregledate teme koje su ranije spomenute i spremni ste za nadogradnju aplikacije PSA, verzija 3.x ili verzija temeljena na UCI-ju, pošaljite zahtjev Microsoftovoj podršci da biste nadogradnju učinili dostupnom iz centra za administratore. U zahtjevu navedite pojedinosti o svojoj instanci.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Starije verzije aplikacije PSA (verzija 2.x aplikacije PSA) u novostvorenoj instanci

Od 17. svibnja 2019. godine sve će nove instance imati UCI kao zadani klijent. Verzija 3.x aplikacije PSA i Field Service verzija 8.x za usklađivanje će s ovom promjenom biti dodijeljene prema zadanim postavkama jer su te verzije dizajnirane za rad s klijentskim UCI-jom.

Od 1. ožujka 2020. klijenti sustava Dynamics PSA više neće moći stvarati nova okruženja sa starijim verzijama PSA, na primjer PSA verzije 2.x ili starije. Svako novo okruženje dobit će samo PSA verzije 3.x.

> [!NOTE]
> Za najbolji doživljaj prilikom korištenja starijih verzija aplikacija Field service i PSA, idite na **Postavke sustava** , a za polje **Koristi samo novo objedinjeno sučelje (preporučeno)** , odaberite **Ne** jer ove verzije nisu dizajnirane da se ispravno učitavaju u UCI-ju. Nakon što ste isključili UCI, možete otvoriti i pokrenuti ove verzije aplikacija Field Service i PSA pomoću starog web-klijenta. 