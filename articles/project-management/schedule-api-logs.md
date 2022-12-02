---
title: Dnevnici planiranja projekta
description: U ovom se članku navode informacije i uzorci koji će vam pomoći pri uporabi zapisnika planiranja projekta za praćenje kvarova koji su povezani s uslugom za planiranje projekta i API-jima za planiranje projekta.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923686"
---
# <a name="project-scheduling-logs"></a>Dnevnici planiranja projekta

_**Odnosi se na:** Project Operations za scenarije koji se temelje na resursima / bez zaliha, osnovnu implementaciju – od sklapanja posla do predračuna_, _Project for the Web_

Microsoft Dynamics 365 Project Operations upotrebljava [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) kao primarni modul planiranja. Umjesto uporabe standardnih Microsoft Dataverse programskih sučelja za web aplikacije (API), Project Operations upotrebljava nove API-je za planiranje projekta za izradu, ažuriranje i brisanje projektnih zadataka, dodjelu resursa, ovisnosti zadataka, grupe projekata i članove timova projekta. Međutim, može doći do pogreške prilikom programskog izvršavanja operacija izrađivanja, ažuriranja ili brisanja na entitetima strukture raščlambe rada (SAR). Za praćenje ovih pogrešaka i povijesti operacija implementirana su dva nova administrativna zapisnika: **Skup operacija** i **Usluga planiranja projekta (UPP)**. Za pristup tim zapisnicima idite na **Postavke** \> **Integracija rasporeda**.

Sljedeća ilustracija prikazuje podatkovni model za zapisnike planiranja projekta.

![Podatkovni model za zapisnike planiranja projekta.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Zapisnik skupa operacija

Zapisnik skupa operacija prati izvršavanje skupa operacija koji se upotrebljava za pokretanje jedne ili više operacija grupne izrade, ažuriranja ili brisanja na projektima, projektnim zadacima, dodjelama resursa, ovisnostima zadataka, grupama projekata ili članovima tima projekta. Polje **Status operacije** prikazuje ukupni status skupa operacija. Pojedinosti korisnih podataka skupa operacija obuhvaćene su povezanim zapisima o pojedinostima skupa operacija.

### <a name="operation-set"></a>Skup operacija

Sljedeća tablica prikazuje polja koja su povezana s entitetom **Skup operacija**.

| Naziv sheme            | Opis                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Datum i vrijeme kad je skup operacija dovršen ili nije uspio.                                                | CompletedOn            |
| msdyn_correlationid   | Vrijednost **correlationId** zahtjeva.                                                                  | CorrelationId          |
| msdyn_description     | Opis skupa operacija.                                                                        | Opis            |
| msdyn_executedon      | Datum/vrijeme kad je zapis izvršen.                                                                       | Izvršeno dana            |
| msdyn_operationsetId  | Jedinstveni identifikator instance entiteta.                                                                   | OperationSet           |
| msdyn_Project         | Projekt koji je povezan sa skupom operacija.                                                            | Project                |
| msdyn_projectid       | Vrijednost **projectId** zahtjeva.                                                                      | ProjectId (zastario) |
| msdyn_projectName     | Nije primjenjivo.                                                                                              | Nije primjenjivo         |
| msdyn_PSSErrorLog     | Jedinstveni identifikator zapisnika grešaka usluge planiranja projekta koji je povezan sa skupom operacija. | Zapisnik pogrešaka PSS-a          |
| msdyn_PSSErrorLogName | Nije primjenjivo.                                                                                              | Nije primjenjivo         |
| msdyn_status          | Status skupa operacija.                                                                             | Stanje                 |
| msdyn_statusName      | Nije primjenjivo.                                                                                              | Nije primjenjivo         |
| msdyn_useraadid       | ID objekta Azure Active Directory (Azure AD) korisnika kojem pripada ovaj zahtjev.                     | UserAADID              |

### <a name="operation-set-detail"></a>Pojedinost skupa operacija

Sljedeća tablica prikazuje polja koja su povezana s entitetom **Pojedinosti skupa operacija**.

| Naziv sheme                 | Opis                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Serijalizirana polja Dataverse za zahtjev.                                            | CdsPayload            |
| msdyn_entityname           | Naziv entiteta za zahtjev.                                                     | EntityName            |
| msdyn_httpverb             | Metoda zahtjeva.                                                                         | HTTPakcija (zastarjelo) |
| msdyn_httpverbName         | Nije primjenjivo.                                                                             | Nije primjenjivo        |
| msdyn_operationset         | Jedinstveni identifikator skupa operacija kojem pripada ovaj zapisnik.                      | OperationSet          |
| msdyn_operationsetdetailId | Jedinstveni identifikator instance entiteta.                                                  | Pojedinost OperationSet   |
| msdyn_operationsetName     | Nije primjenjivo.                                                                             | Nije primjenjivo        |
| msdyn_operationtype        | Vrsta operacije pojedinosti skupa operacije.                                             | OperationType         |
| msdyn_operationtypeName    | Nije primjenjivo.                                                                             | Nije primjenjivo        |
| msdyn_psspayload           | Serijalizirana polja usluge za planiranje projekta za zahtjev.                           | PssPayload            |
| msdyn_recordid             | Identifikator zapisa zahtjeva.                                                       | ID zapisa             |
| msdyn_requestnumber        | Automatski generirani broj koji identificira redoslijed primljenih zahtjeva. | Broj zahtjeva        |

## <a name="project-scheduling-service-error-logs"></a>Zapisnik pogrešaka usluge planiranja projekta

Zapisnici pogrešaka usluge planiranja projekta bilježe pogreške koje se javljaju kad usluga planiranja projekta pokuša izvršiti operaciju **Spremi** ili **Otvori**. Postoje tri podržana scenarija pri kojima se ovi zapisnici generiraju:

- Radnje koje pokreće korisnik kritično ne uspijevaju (na primjer, dodjela se ne može izraditi zbog nedostatka privilegija).
- Usluga planiranja projekta ne može programski izrađivati, ažurirati, brisati niti izvoditi bilo koju drugu kaskadnu operaciju na entitetu.
- Korisnik nailazi na pogreške kad se zapis ne uspije otvoriti (na primjer, kad se otvori projekt ili ažuriraju informacije člana tima).

### <a name="project-scheduling-service-log"></a>Zapisnik usluge planiranja projekta

Sljedeća tablica prikazuje polja koja su uključena u zapisnik usluge planiranja projekta.

| Naziv sheme          | Opis                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Stog poziva za iznimku.                                               | Stog poziva     |
| msdyn_correlationid | Korelacijski ID pogreške.                                               | CorrelationId  |
| msdyn_errorcode     | Polje koje se upotrebljava za pohranu Dataverse koda pogreške ili HTTP koda pogreške. | Kod pogreške     |
| msdyn_HelpLink      | Veza javne dokumentacije za pomoć.                                       | Veza za pomoć      |
| msdyn_log           | Zapisnik iz usluge planiranja projekta.                                   | Zapisnik            |
| msdyn_project       | Projekt koji je povezan sa zapisnikom pogreške.                             | Project        |
| msdyn_projectName   | Naziv projekta ako su korisni podaci skupa operacija postojani. | Nije primjenjivo |
| msdyn_psserrorlogId | Jedinstveni identifikator instance entiteta.                                     | Zapisnik pogrešaka PSS-a  |
| msdyn_SessionId     | ID sesije projekta.                                                        | ID sesije     |

## <a name="error-log-cleanup"></a>Čišćenje zapisnika pogrešaka

Prema zadanim postavkama, zapisnici pogrešaka usluge planiranja projekta i zapisnik skupa operacija mogu se očistiti svakih 90 dana. Obrisat će se svi zapisi stariji od 90 dana. Međutim, administratori mogu prilagoditi raspon čišćenja od 1 do 120 dana promjenom vrijednosti polja **msdyn_StateOperationSetAge** na stranici **Parametri projekta**. Dostupno je nekoliko metoda za promjenu ove vrijednosti:

- Prilagodite entitet **Parametar projekta** tako što ćete izraditi prilagođenu stranicu i dodati polje **Postavljena starost zastarjelih operacija**.
- Upotrijebite kod klijenta koji upotrebljava [Komplet za razvoj softvera WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Upotrijebite kod usluge SDK koji upotrebljava metodu Xrm SDK **updateRecord** (referenca na API klijenta) u aplikacijama stvorenim prema modelu. Power Apps uključuje opis i podržane parametre za metodu **updateRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
