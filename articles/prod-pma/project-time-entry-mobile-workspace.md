---
title: Radni prostor Unosa vremena za projekt
description: U ovoj se temi nalaze informacije o Radnom prostoru Unosa vremena za projekt. Ovaj radni prostor omogućuje korisnicima unos i uštedu vremena u odnosu na projekt s pomoću mobilnog uređaja.
author: Yowelle
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 23a5a9f25cfdd6df74257b3500c7a035d711b5f6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073369"
---
# <a name="project-time-entry-mobile-workspace"></a>Radni prostor Unosa vremena za projekt

[!include [banner](../includes/banner.md)]

U ovoj se temi nalaze informacije o mobilnom radnom prostoru **Unos vremena za projekt**. Ovaj radni prostor omogućuje korisnicima unos i uštedu vremena u odnosu na projekt s pomoću mobilnog uređaja.

Ovaj mobilni radni prostor namijenjen je uporabi s mobilnom aplikacijom Dynamics 365 Unified Ops. 

## <a name="overview"></a>Pregled
Kao dio svog svakodnevnog posla, projektni resursi često su na licu mjesta ili putuju. Mobilni radni prostor **Unos vremena za projekt** omogućuje korisnicima da unose svoje naplativo ili nenaplativo vrijeme u odnosu na projekt na mobilnom uređaju po svojem odabiru. Stoga projektni resursi mogu bilježiti unose vremena uvijek i svugdje. Također mogu pregledati unose vremena koji su već zabilježeni. 

Točnije, u mobilnom radnom prostoru **Unos vremena za projekt** korisnici mogu izvršavati ove zadatke:

-   Za svaki odabrani datum unesite broj sati koje ste potrošili na određeni zadatak.
-   Pretražite prema nazivu projekta ili klijenta kako biste pronašli projekt za koji ćete unijeti vrijeme.
-   Navedite kategoriju i aktivnost za vrijeme koje ste potrošili.
-   Zabilježite vrijeme za projekt kao naplativo ili nenaplativo.
-   Neobvezno unesite neke vanjske ili interne komentare.

## <a name="prerequisites"></a>Preduvjeti
Preduvjeti se razlikuju, ovisno o verziji sustava Microsoft Dynamics 365 koji je postavljen za vašu tvrtku ili ustanovu.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Preduvjeti ako upotrebljavate aplikaciju Dynamics 365 Finance
Ako su Financije postavljene za vašu tvrtku ili ustanovu, administrator sustava mora objaviti mobilni radni prostor **Unos vremena za projekt**. Upute potražite u odjeljku [Objavljivanje mobilnog radnog prostora](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Preduvjeti ako upotrebljavate verziju 1611 s ažuriranjem platforme 3 ili novijom
Ako je za vašu tvrtku ii ustanovu postavljena verzija 1611 s ažuriranjem platforme 3 ili novijom, administrator sustava mora ispuniti sljedeće preduvjete. 

<table>
<thead>
<tr class="header">
<th>Preduvjet</th>
<th>Uloga</th>
<th>Opis</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implementirati zakrpu KB 4018050.</td>
<td>Administrator sustava</td>
<td>Zakrpa KB 4018050 ažuriranje je za X++ ili hitni popravak metapodataka koji sadrži mobilni radni prostor <strong>Unos vremena za projekt</strong>. Kako biste implementirali zakrpu KB 4018050, vaš administrator sustava mora slijediti ove korake.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Preuzeti hitni popravak metapodataka s usluge Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instalirati hitni popravak metapodataka</a>,</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Stvoriti paket za raspoređivanje</a> koji sadrži modele <strong>ApplicationSuite</strong> i <strong>ProjectMobile</strong>, a zatim na LCS prenijeti paket koji se može rasporediti.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Primijeniti paket koji se može rasporediti</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Objaviti mobilni radni prostor <strong>Unos vremena za projekt</strong>.</td>
<td>Administrator sustava</td>
<td>Pogledajte <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Objavljivanje mobilnog radnog prostora</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Preuzimanje i instaliranje mobilnu aplikaciju

Preuzimanje i instaliranje mobilne aplikacije Finance and Operations:

-   [Za telefone s operacijskim sustavom Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Za iPhon uređaje](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Prijava u mobilnu aplikaciju
1.  Pokrenite aplikaciju na mobilnom uređaju.
2.  Unesite URL-adresu svojeg sustava Dynamics 365.
3.  Kad se prvi put prijavite, od vas će se zatražiti korisničko ime i lozinka. Unesite vjerodajnice.
4.  Nakon što se prijavite, prikazuju se dostupni radni prostori za vašu tvrtku. Imajte na umu kako ćete morati osvježiti popis mobilnih radnih prostora ako vaš administrator sustava kasnije objavi novi radni prostor.

[![Povucite za osvježavanje](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Unesite vrijeme s pomoću mobilnog radnog prostora za Unos vremena za projekt
1.  Na mobilnom uređaju odaberite radni prostor **Unos vremena za projekta**.
2.  Odaberite **Unos vremena**. Prikazani su datumi kalendara za trenutačni tjedan.
3.  Za odabrani datum odaberite **Radnje** &gt; **Novi unos**.
4.  Unesite broj sati koji se bilježe.
5.  Odaberite projekt za Unos vremena. Popis prikazuje projekte koji su učitani u vašu aplikaciju za izvanmrežnu uporabu. Prema zadanim postavkama učitano je 50 stavki, ali razvojni inženjer može promijeniti taj broj. Dodatne informacije potražite u odjeljku [Mobilna platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Ako vaš projekt nije na popisu, odaberite **Traži**. Pretražujte po imenu ili se prebacite na pretraživanje po nazivu projekta ili klijentu.
7.  Odaberite kategoriju. Popis prikazuje kategorije koje su učitane u vašu aplikaciju za izvanmrežnu uporabu. Prema zadanim postavkama učitano je 50 stavki, ali razvojni inženjer može promijeniti taj broj. Dodatne informacije potražite u odjeljku [Mobilna platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Ako vaša kategorija nije na popisu, odaberite **Traži**. Pretražujte po kategoriji ili se prebacite na pretraživanje po nazivu kategorije.
9.  Odaberite aktivnost. Popis prikazuje aktivnosti koje su učitane u vašu aplikaciju za izvanmrežnu uporabu. Prema zadanim postavkama učitano je 50 stavki, ali razvojni inženjer može promijeniti taj broj. Dodatne informacije potražite u odjeljku [Mobilna platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Ako vaša aktivnost nije na popisu, odaberite **Traži**. Pretražujte prema broju aktivnosti ili se prebacite na pretraživanje prema namjeni.

11. Odaberite svojstvo retka.
12. Neobvezno: Unesite neke vanjske ili interne komentare.
13. Odaberite **Gotovo**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]