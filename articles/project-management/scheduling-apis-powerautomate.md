---
title: Uporaba API-ja rasporeda projekta s aplikacijom Power Automate
description: U ovom se članku nalazi ogledni tijek koji koristi sučelja za programiranje aplikacija za planiranje projekta (API-je).
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 2527375ff3f3d631f3bb3de1458abb3b8838db54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916325"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Uporaba API-ja rasporeda projekta s aplikacijom Power Automate

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U ovom se članku opisuje ogledni tijek koji pokazuje kako stvoriti cijeli plan projekta pomoću Microsoft Power Automate programa, kako stvoriti skup operacija i kako ažurirati entitet. Primjer pokazuje kako stvoriti projekt, člana projektnog tima, skupove operacija, projektne zadatke i dodjele resursa. U ovom se članku objašnjava i kako ažurirati entitet i izvršiti skup operacija.

Slijedi potpuni popis koraka koji su dokumentirani u oglednom toku u ovom članku:

1. [Stvaranje okidača PowerApps](#1)
2. [Stvori projekt](#2)
3. [Inicijalizacija varijable za člana tima](#3)
4. [Stvaranje generičkog člana tima](#4)
5. [Stvaranje skupa operacija](#5)
6. [Stvaranje grupe projekata](#6)
7. [Inicijalizacija varijable za stanje veze](#7)
8. [Inicijalizacija varijable za broj zadataka](#8)
9. [Inicijalizacija varijable za ID projektnog zadatka](#9)
10. [Učinite dok](#10)
11. [Postavljanje projektnog zadatka](#11)
12. [Stvaranje projektnog zadatka](#12)
13. [Stvaranje dodjele resursa](#13)
14. [Smanjenje varijable](#14)
15. [Preimenovanje projektnog zadatka](#15)
16. [Pokretanje skupa operacija](#16)

## <a name="assumptions"></a>Pretpostavke

Ovaj članak pretpostavlja da imate osnovno znanje o platformi, tokovima oblaka Dataverse i sučelju za programiranje aplikacija project schedule (API). Dodatne informacije potražite u [odjeljku Reference](#references) u nastavku ovog članka.

## <a name="create-a-flow"></a>Stvori tok

### <a name="select-an-environment"></a>Odaberi okruženje

Možete stvoriti protok u Power Automate svom okruženju.

1. Idite na <https://flow.microsoft.com>, i koristite administratorske vjerodajnice za prijavu.
2. U gornjem desnom kutu odaberite **Okruženja**.
3. Na popisu odaberite okruženje u kojem Dynamics 365 Project Operations je instalirano.

### <a name="create-a-solution"></a>Izrada rješenja

Slijedite ove korake da biste stvorili tijek [koji je](/power-automate/overview-solution-flows) svjestan rješenja. Stvaranjem protoka koji je svjestan rješenja možete lakše izvesti protok da biste ga kasnije koristili.

1. U navigacijskom oknu odaberite **Rješenja**.
2. **Na stranici Rješenja** odaberite **Novo rješenje**.
3. **U dijaloškom okviru Novo rješenje** postavite obavezna polja, a zatim odaberite **Stvori**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> Prvi korak: stvaranje okidača PowerApps

1. **Na stranici Rješenja** odaberite rješenje koje ste stvorili, a zatim odaberite **Novo**.
2. U lijevom oknu odaberite **Trenutno strujanje oblaka** \> **Automatizacijski** \> **protok** \> **oblaka.**
3. U polje Naziv **tijeka** unesite **Pokazni tijek zakaženja API-ja**.
4. **Na popisu Odabir načina pokretanja ovog toka** odaberite **Power Apps**. Kada stvorite Power Apps okidač, logika ovisi o vama kao autoru. U ovom članku ostavite ulazne parametre prazne u svrhu testiranja.
5. Kliknite **Stvori**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Korak 2: Stvaranje projekta

Slijedite ove korake da biste stvorili ogledni projekt.

1. U tijeku koji ste stvorili odaberite **Novi korak**.

    ![Dodavanje novog koraka.](media/newstep.png)

2. **U dijaloškom okviru Odabir operacije** u polje za pretraživanje unesite izvedi **slobodnu akciju**. Zatim na kartici **Akcije** odaberite operaciju na popisu rezultata.

    ![Odabir operacije.](media/chooseactiontab.png)

3. U novom koraku odaberite trotočje (**...), a zatim Preimenuj** **.**

![Preimenovanje koraka.](media/renamestep.png)

4. Preimenujte korak **Stvaranje projekta**.
5. **U polju Naziv** akcije odaberite **msdyn\_ CreateProjectV1**.
6. **U polju msdyn\_ predmeta** odaberite **Dodaj dinamički sadržaj**.
7. Na kartici **Izraz** u polje funkcije unesite **Naziv projekta - utcNow()**.
8. Odaberite **U redu**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> Treći korak: inicijalizacija varijable za člana tima

1. U tijeku odaberite **Novi korak**.
2. **U dijaloškom okviru Odabir operacije** u polje za pretraživanje unesite **varijablu** inicijalizacije. Zatim na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite trotočje (**...), a zatim Preimenuj** **.**
4. Preimenujte korak **Član** init tima.
5. **U polje Naziv** unesite **TeamMemberAction**.
6. **U polju Vrsta** odaberite **Niz**.
7. **U polje Vrijednost** unesite **msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> Četvrti korak: Stvaranje generičkog člana tima

1. U tijeku odaberite **Novi korak**.
2. **U dijaloškom okviru Odabir operacije** u polje za pretraživanje unesite izvedi **slobodnu akciju**. Zatim na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite trotočje (**...), a zatim Preimenuj** **.**
4. Preimenujte korak **Stvaranje člana** tima.
5. **Za polje Naziv** akcije u dijaloškom okviru Dinamički **sadržaj** odaberite **TeamMemberAction**.
6. **U polje Parametri akcije** unesite sljedeće informacije o parametru.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Evo objašnjenja parametara:

    - **\@\@ odata.type** – Naziv entiteta. Na primjer, unesite **"Microsoft.Dynamics.CRM.msdyn\_ projectteam"**.
    - **msdyn\_ projectteamid** – Primarni ključ ID projektnog tima. Vrijednost je globalno jedinstveni identifikacijski (GUID) izraz.   ID se generira s kartice izraza.

    - **msdyn\_ projekt\@ odata.bind** – ID projekta vlastitog projekta. Vrijednost će biti dinamičan sadržaj koji proizlazi iz odgovora koraka "Stvori projekt". Provjerite jeste li unijeli cijeli put i dodali dinamički sadržaj između zagrada. Potrebni su navodnici. Na primjer, unesite **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ ime** - Ime člana tima. Na primjer, unesite **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> Peti korak: stvaranje skupa operacija

1. U tijeku odaberite **Novi korak**.
2. **U dijaloškom okviru Odabir operacije** u polje za pretraživanje unesite izvedi **slobodnu akciju**. Zatim na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite trotočje (**...), a zatim Preimenuj** **.**
4. Preimenujte korak **Stvaranje skupa** operacija.
5. **U polju Naziv** akcije odaberite prilagođenu akciju **msdyn\_ CreateOperationSetV1** Dataverse.
6. **U polje Opis** unesite **ScheduleAPIDemoOperationSet**.
7. **U polje Projekt** unesite **/msdyn\_ projects(**.
8. U dijaloškom okviru Dinamički **sadržaj** odaberite **msdyn\_ CreateProjectV1Response ProjectId**.
9. **U polje Projekt** unesite **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> Šesti korak: stvaranje grupe projekata

1. U tijeku odaberite **Novi korak**.
2. **U dijaloškom okviru Odabir operacije** u polje za pretraživanje unesite **dodaj novi redak**. Zatim na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite trotočje (**...), a zatim Preimenuj** **.**
4. Preimenujte korak **Stvaranje grupe**.
5. U polju Naziv **tablice** odaberite **Grupe projekata**.
6. **U polje Naziv** unesite **ScheduleAPIDemoBucket1**.
7. **Za polje Projekt** odaberite **msdyn\_ CreateProjectV1Response ProjectId** u dijaloškom okviru Dinamički sadržaj.**·**

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> Sedmi korak: inicijalizacija varijable za status veze

1. U tijeku odaberite **Novi korak**.
2. **U dijaloškom okviru Odabir operacije** u polje za pretraživanje unesite **varijablu** inicijalizacije. Zatim na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite trotočje (**...), a zatim Preimenuj** **.**
4. Preimenujte korak **Init linkstatus**.
5. **U polje Naziv** unesite **linkstatus**.
6. **U polju Vrsta** odaberite **Cijeli broj**.
7. **U polje Vrijednost** unesite **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> Korak 8: Inicijalizacija varijable za broj zadataka

1. U tijeku odaberite **Novi korak**.
2. **U dijaloškom okviru Odabir operacije** u polje za pretraživanje unesite **varijablu** inicijalizacije. Zatim na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite trotočje (**...), a zatim Preimenuj** **.**
4. Preimenujte korak **Init Broj zadataka**.
5. **U polje Naziv** unesite **broj zadataka**.
6. **U polju Vrsta** odaberite **Cijeli broj**.
7. **U polje Vrijednost** unesite **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> Deveti korak: inicijalizacija varijable za ID projektnog zadatka

1. U tijeku odaberite **Novi korak**.
2. **U dijaloškom okviru Odabir operacije** u polje za pretraživanje unesite **varijablu** inicijalizacije. Zatim na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite trotočje (**...), a zatim Preimenuj** **.**
4. Preimenujte korak **Init ProjectTaskID**.
5. **U polje Naziv** unesite **broj zadataka**.
6. **U polju Vrsta** odaberite **Niz**.
7. **Za polje Vrijednost** unesite **GUID()** u sastavljač izraza.

## <a name="step-10-do-until"></a><a id="10"></a> Korak 10: Učinite dok

1. U tijeku odaberite **Novi korak**.
2. **U dijaloškom okviru Odabir operacije** u polje za pretraživanje unesite **učini dok.** Zatim na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. Postavite prvu vrijednost u uvjetnoj izjavi na **broj varijabilnih zadataka** iz dijaloškog okvira Dinamički **sadržaj**.
4. Postavite uvjet na **manje nego jednako**.
5. Postavite drugu vrijednost u uvjetnom izvodu na **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> Prvi korak: postavljanje projektnog zadatka

1. U tijeku odaberite **Novi korak**.
2. **U dijaloškom okviru Odabir operacije** u polje za pretraživanje unesite **postavljenu varijablu**. Zatim na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite trotočje (**...), a zatim Preimenuj** **.**
4. Preimenujte korak **Postavi projektni zadatak**.
5. **U polju Naziv** odaberite **msdyn\_ projecttaskid**.
6. **Za polje Vrijednost** unesite **GUID()** u sastavljač izraza.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> 12. korak: stvaranje projektnog zadatka

Slijedite ove korake da biste stvorili projektni zadatak koji ima jedinstveni ID koji pripada trenutnom projektu i grupi projekta koju ste stvorili.

1. U tijeku odaberite **Novi korak**.
2. **U dijaloškom okviru Odabir operacije** u polje za pretraživanje unesite izvedi **slobodnu akciju**. Zatim na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U koraku odaberite trotočje (**...), a zatim Preimenuj** **.**
4. Preimenujte korak **Stvaranje projektnog zadatka**.
5. **U polju Naziv** akcije odaberite **msdyn\_ PssCreateV1**.
6. **U polje Entitet** unesite sljedeće informacije o parametru.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Evo objašnjenja parametara:

    - **\@\@ odata.type** – Naziv entiteta. Na primjer, unesite **"Microsoft.Dynamics.CRM.msdyn\_ projecttask"**.
    - **msdyn\_ projecttaskid** – Jedinstveni ID zadatka. Vrijednost treba postaviti na dinamičku varijablu iz **msdyn\_ projecttaskid**.
    - **msdyn\_ projekt\@ odata.bind** – ID projekta vlastitog projekta. Vrijednost će biti dinamičan sadržaj koji proizlazi iz odgovora koraka "Stvori projekt". Provjerite jeste li unijeli cijeli put i dodali dinamički sadržaj između zagrada. Potrebni su navodnici. Na primjer, unesite **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ predmet** – bilo koji naziv zadatka.
    - **msdyn\_ projectbucket\@ odata.bind** – Kanta projekta koja sadrži zadatke. Vrijednost će biti dinamičan sadržaj koji proizlazi iz odgovora koraka "Create Bucket". Provjerite jeste li unijeli cijeli put i dodali dinamički sadržaj između zagrada. Potrebni su navodnici. Na primjer, unesite **"/msdyn\_ projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ start** – Dinamički sadržaj za početni datum. Na primjer, sutra će biti predstavljeno kao **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduledstart** – zakazani datum početka. Na primjer, sutra će biti predstavljeno kao **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduleend** – zakazani datum završetka. Odaberite datum u budućnosti. Na primjer, navedite **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** – Status veze. Na primjer, unesite **"192350000"**.

7. **Za polje OperationSetId** odaberite **msdyn\_ CreateOperationSetV1Response** u **dijaloškom okviru Dinamički sadržaj**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> 13. korak: stvaranje dodjele resursa

1. U tijeku odaberite **Novi korak**.
2. **U dijaloškom okviru Odabir operacije** u polje za pretraživanje unesite izvedi **slobodnu akciju**. Zatim na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U koraku odaberite trotočje (**...), a zatim Preimenuj** **.**
4. Preimenujte korak **Stvaranje dodjele**.
5. **U polju Naziv** akcije odaberite **msdyn\_ PssCreateV1**.
6. **U polje Entitet** unesite sljedeće informacije o parametru.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. **Za polje OperationSetId** odaberite **msdyn\_ CreateOperationSetV1Response** u **dijaloškom okviru Dinamički sadržaj**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> Korak 14: Smanjenje varijable

1. U tijeku odaberite **Novi korak**.
2. **U dijaloškom okviru Odabir operacije** u polje za pretraživanje unesite **varijablu** smanjenja. Zatim na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. **U polju Naziv** odaberite **broj zadataka**.
4. **U polje Vrijednost** unesite **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> Korak 15: preimenovanje projektnog zadatka

1. U tijeku odaberite **Novi korak**.
2. **U dijaloškom okviru Odabir operacije** u polje za pretraživanje unesite izvedi **slobodnu akciju**. Zatim na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U koraku odaberite trotočje (**...), a zatim Preimenuj** **.**
4. Preimenujte korak **Preimenuj projektni zadatak**.
5. **U polju Naziv** akcije odaberite **msdyn\_ PssUpdateV1**.
6. **U polje Entitet** unesite sljedeće informacije o parametru.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. **Za polje OperationSetId** odaberite **msdyn\_ CreateOperationSetV1Response** u **dijaloškom okviru Dinamički sadržaj**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> Korak 16: pokretanje skupa operacija

1. U tijeku odaberite **Novi korak**.
2. **U dijaloškom okviru Odabir operacije** u polje za pretraživanje unesite izvedi **slobodnu akciju**. Zatim na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U koraku odaberite trotočje (**...), a zatim Preimenuj** **.**
4. Preimenujte korak **Skup operacija izvršavanja**.
5. **U polju Naziv** akcije odaberite **msdyn\_ ExecuteOperationSetV1**.
6. **Za polje OperationSetId** odaberite **msdyn\_ CreateOperationSetV1Response OperationSetId** u **dijaloškom okviru Dynamid sadržaj**.

## <a name="references"></a>Reference

- [Pregled kako integrirati tokove s Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Uporaba API-ja rasporeda projekta za izvođenje operacija s entitetima planiranja](schedule-api-preview.md)
- [Pregled tokova oblaka - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Pregled tokova koji su svjesni rješenja - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
