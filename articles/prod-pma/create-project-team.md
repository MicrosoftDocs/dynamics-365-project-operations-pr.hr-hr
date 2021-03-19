---
title: Stvaranje projektnog tima
description: U ovoj se temi nalaze informacije o načinu izrade projektnih timova i upravljanja njima.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 121a007d91c2da4f3b9951901781757b8bcca8fe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270849"
---
# <a name="create-a-project-team"></a>Stvaranje projektnog tima

[!include [banner](../includes/banner.md)]

Kako bi se upotrebljavale uloge koje su prethodno postavljene u projektu, voditelj projekta mora povezati uloge s projektom. Za projekt se može dodijeliti više uloga. Kako bi se spriječila zabuna, ove se uloge automatski označavaju tijekom rezervacije. Na primjer, ako voditelj projekta zahtijeva tri softverska inženjera, oznake tri uloge softverskog inženjera **softverski inženjer 1**, **softverski inženjer 2** i **softverski inženjer 3** automatski se generiraju. Ako su svojstva uloge prethodno postavljena za ulogu, ona se primjenjuju kao filtar tijekom pretraživanja resursa. Dodatna svojstva mogu se prema potrebi dodati za daljnje sužavanje pretraživanja.

Postavke prikaza također se mogu prilagoditi kako bi pružile bolji prikaz dostupnosti resursa. Postoje mogućnosti prikazivanja dostupnosti po satu, dnevno, tjedno, mjesečno, tromjesečno i godišnje. Također postoji mogućnost prikaza dostupnog i preostalog kapaciteta na resursima. Ova je mogućnost korisna za upravljanje vremenom kada procjenjujete dostupno vrijeme za aktivnosti ili dostupnost resursa.

Voditelj projekta može odabrati ulogu na stranici, a zatim, ako postoji dostupan resurs koji udovoljava zahtjevu, odabrati resurs kako bi ga rezervirao za popunjavanje uloge. Imajte na umu kako resurse u fazi planiranja u ovom trenutku nije potrebno rezervirati. Kada stvarate WBS uloge možete zamijeniti resursima osoblja za projekt. Ako se uloge u WBS-u zamijene resursima s osobljem, postavka resursa automatski ažurira popis i raspored projektnog tima.

[![Popis projektnog tima koji uključuje i uloge i stvarne resurse](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Voditelj projekta ima razne mogućnosti za rezerviranje resursa za projekt, kao što su **Preostali kapacitet**, **Puni kapacitet**, **Postotak kapaciteta** i **Navođenje sati rada**. Ove mogućnosti rezervacije mogu se otkazati u bilo kojem trenutku ako se zadaci resursa promijene. Podržane su dvije vrste rezervacija:

- **Fiksna rezervacija** – Rezervacija resursa je odobrena i potvrđena za rad s određenim vremenom angažmana.
- **Uvjetna rezervacija** – Rezervacija resursa uvjetno je potvrđena za rad s određenim vremenom angažmana.

U sljedećem postupku objašnjava se način stvaranja projektnog tima.

## <a name="create-a-project-team"></a>Stvaranje projektnog tima

1. Na stranici s popisom **Svi projekti** odaberite projekt, a zatim odaberite **Uredi**.
2. Na kartici **Projektni tim i planiranje** u polju **Planiraj datum završetka** unesite datum koji nastupa mjesec dana nakon datuma početka rasporeda. Na primjer, ako je datum početka rasporeda 24. lipnja 2017. (24.6.2017.), unesite **24.07.2017.**.
3. Odaberite **Dodaj**.
4. U oknu **Dodaj uloge projektu** u polju **Uloga**, odaberite **Voditelj projekta višeg ranga**.
5. Odaberite **Potrebne kompetencije**.
6. Svojstva koja ste prethodno postavili za ulogu voditelja projekta višeg ranga , na stranici **Odaberi svojstva** odabiru se prema zadanim postavkama. Odaberite **U redu**.
7. Na stranici **Dodaj uloge projektu** u polje **Broj resursa** unesite **1**.
8. U polju **Resurs** pretraživanje prikazuje sve resurse koji imaju potrebne kompetencije. Odaberite **Daniel Petek**, a zatim odaberite **Stvori**.
9. Na stranici **Projekt** odaberite **Dodaj**.
10. U oknu **Dodaj uloge projektu** u polju **Uloga**, odaberite **Član tima**. U polje **Broj resursa** unesite **5**.
11. Kliknite **Stvori**.
12. Na stranici **Projekti** odaberite **Popuni resurs**.

## <a name="monitor-project-teams"></a>Nadzirite projektne timove
1. Na stranici **Svi projekti** odaberite vezu **Projekt ID** za projekt **2. faza nadogradnje XYZ**.
2. Na Brzoj kartici **Projektni tim i planiranje** provjerite jesu li navedeni resursi projekta točni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]