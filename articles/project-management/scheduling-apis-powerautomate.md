---
title: Uporaba API-ja rasporeda projekta s aplikacijom Power Automate
description: U ovom se članku prikazuje ogledni tok koji upotrebljava programska sučelja aplikacije (API-je) za raspored projekta.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404452"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Uporaba API-ja rasporeda projekta s aplikacijom Power Automate

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U članku se opisuje ogledni tok koji pokazuje kako stvoriti potpuni plan projekta uz pomoć aplikacije Microsoft Power Automate, kako stvoriti skup operacija i kako ažurirati entitet. Na primjeru je prikazano kako stvoriti projekt, člana projektnog tima, skupove operacija, projektne zadatke i dodjele resursa. U članku se također objašnjava kako ažurirati neki entitet i izvršiti skup operacija.

U nastavku je prikazan popis svih koraka dokumentiranih u oglednom toku u ovom članku:

1. [Stvaranje okidača za PowerApps](#1)
2. [Stvaranje projekta](#2)
3. [Inicijalizacija varijable za člana tima](#3)
4. [Stvaranje generičkog člana tima](#4)
5. [Stvaranje skupa operacija](#5)
6. [Stvaranje grupe projekata](#6)
7. [Inicijalizacija varijable za status veze](#7)
8. [Inicijalizacija varijable za broj zadataka](#8)
9. [Inicijalizacija varijable za ID projektnog zadatka](#9)
10. [Izvrši do](#10)
11. [Postavljanje projektnog zadatka](#11)
12. [Stvaranje projektnog zadatka](#12)
13. [Stvaranje dodjele resursa](#13)
14. [Umanjenje varijable](#14)
15. [Preimenovanje projektnog zadatka](#15)
16. [Pokretanje skupa operacija](#16)

## <a name="assumptions"></a>Pretpostavke

U članku se pretpostavlja da imate osnovno znanje o platformi Dataverse, tokovima oblaka i programskom sučelju aplikacije (API) za raspored projekta. Dodatne informacije potražite u odjeljku [Reference](#references) u nastavku ovog članka.

## <a name="create-a-flow"></a>Stvaranje toka

### <a name="select-an-environment"></a>Odabir okruženja

U svom okruženju možete stvoriti tok aplikacije Power Automate.

1. Otvorite <https://flow.microsoft.com> i prijavite se s svojim administratorskim vjerodajnicama.
2. U gornjem desnom kutu odaberite **Okruženja**.
3. Na popisu odaberite okruženje u kojem je instaliran Dynamics 365 Project Operations.

### <a name="create-a-solution"></a>Stvaranje rješenja

Da biste stvorili [tok ovisan o rješenju](/power-automate/overview-solution-flows), slijedite ove korake. Stvaranje toka ovisnog o rješenju omogućuje vam jednostavniji izvoz toka za naknadnu upotrebu.

1. U navigacijskom oknu odaberite **Rješenja**.
2. Na stranici **Rješenja** odaberite **Novo rješenje**.
3. U dijaloškom okviru **Novo rješenje** postavite obavezna polja, a zatim odaberite **Stvori**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>1. korak: Stvaranje okidača aplikacije PowerApps

1. Na stranici **Rješenja** odaberite rješenje koje ste stvorili, a zatim odaberite **Novo**.
2. U lijevom oknu odaberite **Tokovi oblaka** \> **Automatizacija** \> **Tok oblaka** \> **Trenutno**.
3. U polju **Naziv toka** unesite **Zakaži demo tok API-ja**.
4. Na popisu **Odabir načina pokretanja ovog toka** odaberite **Power Apps**. Nakon stvaranja okidača aplikacije Power Apps logika je na vama kao autoru. U ovom članku ostavite parametre unosa prazne u svrhu testiranja.
5. Odaberite **Stvori**.

## <a name="step-2-create-a-project"></a><a id="2"></a>2. korak: Stvaranje projekta

Poduzmite ove korake da biste stvorili ogledni projekt.

1. U stvorenom toku odaberite **Novi korak**.

    ![Dodavanje novog koraka.](media/newstep.png)

2. U dijaloškom okviru **Odabir operacije** unesite **izvrši neograničenu akciju** u polje za pretraživanje. Potom na kartici **Akcije** odaberite operaciju na popisu rezultata.

    ![Odabir operacije.](media/chooseactiontab.png)

3. U novom koraku odaberite elipsu (**...**), a zatim **Preimenuj**.

![Preimenovanje koraka.](media/renamestep.png)

4. Preimenujte korak **Stvaranje projekta**.
5. U polju **Naziv akcije** odaberite **msdyn\_CreateProjectV1**.
6. U polju **msdyn\_subject** odaberite **Dodavanje dinamičkog sadržaja**.
7. Na kartici **Izraz** u polju funkcije unesite **Naziv projekta – utcNow()**.
8. Odaberite **U redu**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>3. korak: Inicijalizacija varijable za člana tima

1. U toku odaberite **Novo**.
2. U dijaloškom okviru **Odabir operacije** unesite **inicijalizacija varijable** u polje za pretraživanje. Potom na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite elipsu (**...**), a zatim **Preimenuj**.
4. Preimenujte korak **Inicijalizacija člana tima**.
5. U polje **Naziv** unesite **TeamMemberAction**.
6. U polju **Vrsta** odaberite **Niz**.
7. U polje **Vrijednost** unesite **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>4. korak: Stvaranje generičkog člana tima

1. U toku odaberite **Novo**.
2. U dijaloškom okviru **Odabir operacije** unesite **izvrši neograničenu akciju** u polje za pretraživanje. Potom na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite elipsu (**...**), a zatim **Preimenuj**.
4. Preimenujte korak **Stvaranje člana tima**.
5. Za polje **Naziv akcije** odaberite **TeamMemberAction** u dijaloškom okviru **Dinamični sadržaj**.
6. U polje **Parametri akcije** unesite sljedeće informacije o parametrima.

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

    Parametri su objašnjeni u nastavku:

    - **\@\@odata.type** – naziv entiteta. Primjerice, unesite **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – primarni ključ ID-ja projektnog tima. Vrijednost je izraz globalnog jedinstvenog identifikatora (GUID).   ID se generira s kartice izraza.

    - **msdyn\_project\@odata.bind** – ID projekta projekta vlasnika Vrijednost će biti dinamički sadržaj koji nastaje odgovorom koraka „Stvaranje projekta”. Obavezno unesite cijelu putanju i dodajte dinamički sadržaj između zagrada. Navodnici su obvezni. Primjerice, unesite **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_name** – naziv člana tima. Primjerice, unesite **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>5. korak: Stvaranje skupa operacija

1. U toku odaberite **Novo**.
2. U dijaloškom okviru **Odabir operacije** unesite **izvrši neograničenu akciju** u polje za pretraživanje. Potom na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite elipsu (**...**), a zatim **Preimenuj**.
4. Preimenujte korak **Stvaranje skupa operacija**.
5. U polju **Naziv akcije** odaberite prilagođenu akciju **msdyn\_CreateOperationSetV1** Dataverse.
6. U polje **Opis** unesite **ScheduleAPIDemoOperationSet**.
7. U polje **Projekt** unesite **/msdyn\_projects(**.
8. U dijaloškom okviru **Dinamički sadržaj** odaberite **msdyn\_CreateProjectV1Response ProjectId**.
9. U polje **Projekt** unesite **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>6. korak: Stvaranje grupe projekata

1. U toku odaberite **Novo**.
2. U dijaloškom okviru **Odabir operacije** unesite **dodavanje novog retka** u polje za pretraživanje. Potom na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite elipsu (**...**), a zatim **Preimenuj**.
4. Preimenujte korak **Stvaranje grupe**.
5. U polju **Naziv tablice** odaberite **Grupe projekta**.
6. U polje **Naziv** unesite **ScheduleAPIDemoBucket1**.
7. Za polje **Projekt** odaberite **msdyn\_CreateProjectV1Response ProjectId** u dijaloškom okviru **Dinamički sadržaj**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>7. korak: Inicijalizacija varijable za status veze

1. U toku odaberite **Novo**.
2. U dijaloškom okviru **Odabir operacije** unesite **inicijalizacija varijable** u polje za pretraživanje. Potom na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite elipsu (**...**), a zatim **Preimenuj**.
4. Preimenujte korak **Inicijalizacija za linkstatus**.
5. U polje **Naziv** unesite **linkstatus**.
6. U polju **Vrsta** odaberite **Cijeli broj**.
7. U polje **Vrijednost** unesite **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>8. korak: Inicijalizacija varijable za broj zadataka

1. U toku odaberite **Novo**.
2. U dijaloškom okviru **Odabir operacije** unesite **inicijalizacija varijable** u polje za pretraživanje. Potom na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite elipsu (**...**), a zatim **Preimenuj**.
4. Preimenujte korak **Inicijalizacija broja zadataka**.
5. U polje **Naziv** unesite **broj zadataka**.
6. U polju **Vrsta** odaberite **Cijeli broj**.
7. U polje **Vrijednost** unesite **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>9. korak: Inicijalizacija varijable za ID projektnog zadatka

1. U toku odaberite **Novo**.
2. U dijaloškom okviru **Odabir operacije** unesite **inicijalizacija varijable** u polje za pretraživanje. Potom na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite elipsu (**...**), a zatim **Preimenuj**.
4. Preimenujte korak **Inicijalizacija za ProjectTaskID**.
5. U polje **Naziv** unesite **broj zadataka**.
6. U polju **Vrsta** odaberite **Niz**.
7. Za polje **Vrijednost** unesite **guid()** u sastavljač izraza.

## <a name="step-10-do-until"></a><a id="10"></a>10. korak: Izvrši do

1. U toku odaberite **Novo**.
2. U dijaloškom okviru **Odabir operacije** unesite **izvrši do** u polje za pretraživanje. Potom na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. Postavite prvu vrijednost u uvjetnoj naredbi na varijablu **broj zadataka** iz dijaloškog okvira **Dinamički sadržaj**.
4. Postavite uvjet na **manje od jednako**.
5. Postavite drugu vrijednost u uvjetnoj naredbi na **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>11. korak: Postavljanje projektnog zadatka

1. U toku odaberite **Novo**.
2. U dijaloškom okviru **Odabir operacije** unesite **postavljanje varijable** u polje za pretraživanje. Potom na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U novom koraku odaberite elipsu (**...**), a zatim **Preimenuj**.
4. Preimenujte korak **Postavljanje projektnog zadatka**.
5. U polju **Naziv** odaberite **msdyn\_projecttaskid**.
6. Za polje **Vrijednost** unesite **guid()** u sastavljač izraza.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>12. korak: Stvaranje projektnog zadatka

Slijedite ove korake za stvaranje projektnog zadatka koji ima jedinstveni ID koji pripada trenutnom projektu i grupi projekata koju ste stvorili.

1. U toku odaberite **Novo**.
2. U dijaloškom okviru **Odabir operacije** unesite **izvrši neograničenu akciju** u polje za pretraživanje. Potom na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U tom koraku odaberite elipsu (**...**), a zatim odaberite **Preimenuj**.
4. Preimenujte korak **Stvaranje projektnog zadatka**.
5. U polju **Naziv akcije** odaberite **msdyn\_PssCreateV1**.
6. U polje **Entitet** unesite sljedeće podatke o parametrima.

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

    Parametri su objašnjeni u nastavku:

    - **\@\@odata.type** – naziv entiteta. Primjerice, unesite **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – jedinstveni ID zadatka. Vrijednost bi trebala biti postavljena na dinamičku varijablu iz **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – ID projekta projekta vlasnika Vrijednost će biti dinamički sadržaj koji nastaje odgovorom koraka „Stvaranje projekta”. Obavezno unesite cijelu putanju i dodajte dinamički sadržaj između zagrada. Navodnici su obvezni. Primjerice, unesite **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_subject** – bilo koji naziv zadatka.
    - **msdyn\_projectbucket\@odata.bind** – grupa projekata koja sadrži zadatke. Vrijednost će biti dinamički sadržaj koji nastaje odgovorom koraka „Stvaranje grupe”. Obavezno unesite cijelu putanju i dodajte dinamički sadržaj između zagrada. Navodnici su obvezni. Primjerice, unesite **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_start** – dinamički sadržaj za datum početka. Primjerice, sutra se prikazuje kao **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – zakazani datum početka. Primjerice, sutra se prikazuje kao **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – zakazani datum završetka. Odaberite datum u budućnosti. Na primjer, zadajte **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – status veze. Primjerice, unesite **"192350000"**.

7. Za polje **OperationSetId** odaberite **msdyn\_CreateOperationSetV1Response** u dijaloškom okviru **Dinamički sadržaj**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>13. korak: Stvaranje dodjele resursa

1. U toku odaberite **Novo**.
2. U dijaloškom okviru **Odabir operacije** unesite **izvrši neograničenu akciju** u polje za pretraživanje. Potom na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U tom koraku odaberite elipsu (**...**), a zatim odaberite **Preimenuj**.
4. Preimenujte korak **Stvaranje dodjele**.
5. U polju **Naziv akcije** odaberite **msdyn\_PssCreateV1**.
6. U polje **Entitet** unesite sljedeće podatke o parametrima.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Za polje **OperationSetId** odaberite **msdyn\_CreateOperationSetV1Response** u dijaloškom okviru **Dinamički sadržaj**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>14. korak: Umanjenje varijable

1. U toku odaberite **Novo**.
2. U dijaloškom okviru **Odabir operacije** unesite **umanjenje varijable** u polje za pretraživanje. Potom na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U polju **Naziv** odaberite **broj zadataka**.
4. U polje **Vrijednost** unesite **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>15. korak: Preimenovanje projektnog zadatka

1. U toku odaberite **Novo**.
2. U dijaloškom okviru **Odabir operacije** unesite **izvrši neograničenu akciju** u polje za pretraživanje. Potom na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U tom koraku odaberite elipsu (**...**), a zatim odaberite **Preimenuj**.
4. Preimenujte korak **Preimenovanje projektnog zadatka**.
5. U polju **Naziv akcije** odaberite **msdyn\_PssUpdateV1**.
6. U polje **Entitet** unesite sljedeće podatke o parametrima.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Za polje **OperationSetId** odaberite **msdyn\_CreateOperationSetV1Response** u dijaloškom okviru **Dinamički sadržaj**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>16. korak: Pokretanje skupa operacija

1. U toku odaberite **Novo**.
2. U dijaloškom okviru **Odabir operacije** unesite **izvrši neograničenu akciju** u polje za pretraživanje. Potom na kartici **Akcije** odaberite operaciju na popisu rezultata.
3. U tom koraku odaberite elipsu (**...**), a zatim odaberite **Preimenuj**.
4. Preimenujte korak **Izvođenje skupa operacija**.
5. U polju **Naziv akcije** odaberite **msdyn\_ExecuteOperationSetV1**.
6. Za polje **OperationSetId** odaberite **msdyn\_CreateOperationSetV1Response OperationSetId** u dijaloškom okviru **Dinamički sadržaj**.

## <a name="references"></a>Reference

- [Pregled načina integracije tokova s platformom Dataverse – Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Uporaba API-ja rasporeda projekta za izvođenje operacija s entitetima planiranja](schedule-api-preview.md)
- [Pregled tokova oblaka – Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Pregled tokova koji ovise o rješenjima – Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
