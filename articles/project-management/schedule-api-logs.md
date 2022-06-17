---
title: Dnevnici planiranja projekta
description: U ovom se članku navode informacije i uzorci koji će vam pomoći da pomoću zapisnika planiranja projekata pratite nedostatke povezane s uslugom planiranja projekata i API-jevima za planiranje projekata.
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

_**Odnosi se na:** Projektne operacije za scenarije koji se temelje na resursima/ne zalihama, Implementacija Litea - ponuda za fakturiranje_ proforma, _Projekt za web_

Microsoft Dynamics 365 Project Operations koristi [Project za Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) kao primarni mehanizam zakazivanja. Umjesto korištenja standardnih Microsoft Dataverse sučelja za programiranje web-aplikacija (API-ja), Project Operations koristi nove API-jeve za planiranje projekata za stvaranje, ažuriranje i brisanje projektnih zadataka, dodjela resursa, ovisnosti zadataka, grupa projekata i članova projektnih timova. Međutim, kada se operacije stvaranja, ažuriranja ili brisanja programski pokreću na entitetima strukture raščlambe rada (WBS), mogu se pojaviti pogreške. Da bi se pratile te pogreške i povijest operacija, provedena su dva nova administrativna zapisnika: **Skup operacija i** Usluga zakazivanja projekata (PSS) **·**. Da biste pristupili tim zapisnicima, idite na **Postavke** \> **zakaži integraciju.**

Sljedeća ilustracija prikazuje podatkovni model za zapisnike planiranja projekata.

![Podatkovni model za zapisnike planiranja projekata.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Zapisnik skupa operacija

Zapisnik skupa operacija prati izvršavanje skupa operacija koji se koristi za pokretanje jednog ili više operacija stvaranja, ažuriranja ili brisanja u seriji o projektima, projektnim zadacima, dodjelama resursa, zavisnostima zadataka, grupama projekata ili članovima projektnog tima. Polje **Operacija u statusu** prikazuje cjelokupni status skupa operacija. Pojedinosti o korisnom opterećenju skupa operacija bilježe se u povezanim zapisima o skupu podataka o operaciji.

### <a name="operation-set"></a>Skup operacija

Sljedeća tablica prikazuje polja povezana s entitetom **Skup** operacija.

| Naziv sheme            | Opis                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Datum/vrijeme dovršetka ili neuspjeha skupa operacija.                                                | CompletedOn            |
| msdyn_correlationid   | Vrijednost **I korelacije** zahtjeva.                                                                  | CorrelationId          |
| msdyn_description     | Opis skupa operacija.                                                                        | Opis            |
| msdyn_executedon      | Datum/vrijeme pokretanja zapisa.                                                                       | Izvršeno dana            |
| msdyn_operationsetId  | Jedinstveni identifikator instanci entiteta.                                                                   | OperationSet           |
| msdyn_Project         | Projekt koji se odnosi na skup operacija.                                                            | Project                |
| msdyn_projectid       | Vrijednost **projectId** zahtjeva.                                                                      | ProjectId (zastario) |
| msdyn_projectName     | Nije primjenjivo.                                                                                              | Nije primjenjivo         |
| msdyn_PSSErrorLog     | Jedinstveni identifikator zapisnika pogrešaka servisa za planiranje projekta koji je povezan sa skupom operacija. | Zapisnik pogrešaka PSS-a          |
| msdyn_PSSErrorLogName | Nije primjenjivo.                                                                                              | Nije primjenjivo         |
| msdyn_status          | Stanje skupa operacija.                                                                             | Stanje                 |
| msdyn_statusName      | Nije primjenjivo.                                                                                              | Nije primjenjivo         |
| msdyn_useraadid       | Azure Active Directory ID (Azure AD) objekta korisnika kojem zahtjev pripada.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detalji skupa operacija

Sljedeća tablica prikazuje polja povezana s entitetom Detalji **skupa** operacija.

| Naziv sheme                 | Opis                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Serijalizirana Dataverse polja za zahtjev.                                            | CdsPayload            |
| msdyn_entityname           | Naziv entiteta za zahtjev.                                                     | EntityName            |
| msdyn_httpverb             | Način zahtjeva.                                                                         | HTTPakcija (zastarjelo) |
| msdyn_httpverbName         | Nije primjenjivo.                                                                             | Nije primjenjivo        |
| msdyn_operationset         | Jedinstveni identifikator skupa operacija kojem zapis pripada.                      | OperationSet          |
| msdyn_operationsetdetailId | Jedinstveni identifikator instanci entiteta.                                                  | Pojedinost OperationSet   |
| msdyn_operationsetName     | Nije primjenjivo.                                                                             | Nije primjenjivo        |
| msdyn_operationtype        | Vrsta operacije skupa operacija detaljno.                                             | OperationType         |
| msdyn_operationtypeName    | Nije primjenjivo.                                                                             | Nije primjenjivo        |
| msdyn_psspayload           | Polja Serijalizirana usluga zakazivanja projekata za zahtjev.                           | PssPayload            |
| msdyn_recordid             | Identifikator zapisa zahtjeva.                                                       | ID zapisa             |
| msdyn_requestnumber        | Automatski generiran broj koji identificira narudžbu kojom su zahtjevi zaprimljeni. | Broj zahtjeva        |

## <a name="project-scheduling-service-error-logs"></a>Zapisnici pogrešaka servisa za planiranje projekata

U zapisnicima pogrešaka servisa za planiranje projekata zabilježene su pogreške do kojih dolazi kada servis za planiranje projekata pokuša operaciju Spremanja **ili** Otvaranja **·**. Postoje tri podržana scenarija u kojima se generiraju ti zapisnici:

- Akcije koje je pokrenuo korisnik kritično ne uspijevaju (na primjer, dodjela se ne može stvoriti zbog privilegija koje nedostaju).
- Usluga zakazivanja projekata ne može programski stvarati, ažurirati, brisati ili izvoditi bilo koju drugu kaskadnu operaciju na entitetu.
- Korisnik naiđe na pogreške kada se zapis ne otvori (na primjer, prilikom otvaranja projekta ili ažuriranja informacija o članu tima).

### <a name="project-scheduling-service-log"></a>Zapisnik usluge planiranja projekta

Sljedeća tablica prikazuje polja obuhvaćena zapisnikom servisa za planiranje projekta.

| Naziv sheme          | Opis                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Stog poziva za iznimku.                                               | Stog poziva     |
| msdyn_correlationid | ID korelacije pogreške.                                               | CorrelationId  |
| msdyn_errorcode     | Polje koje se koristi za spremanje koda Dataverse pogreške ili HTTP koda pogreške. | Kod pogreške     |
| msdyn_HelpLink      | Veza na javnu dokumentaciju pomoći.                                       | Veza za pomoć      |
| msdyn_log           | Zapisnik iz usluge zakazivanja projekata.                                   | Zapisnik            |
| msdyn_project       | Projekt koji je povezan s zapisnikom pogrešaka.                             | Project        |
| msdyn_projectName   | Naziv projekta ako će korisni teret skupa operacija biti zadržan. | Nije primjenjivo |
| msdyn_psserrorlogId | Jedinstveni identifikator instanci entiteta.                                     | Zapisnik pogrešaka PSS-a  |
| msdyn_SessionId     | ID projektne sesije.                                                        | ID sesije     |

## <a name="error-log-cleanup"></a>Čišćenje zapisnika pogrešaka

Prema zadanim postavkama, i zapisnici pogrešaka usluge zakazivanja projekata i zapisnik Skupa operacija mogu se očistiti svakih 90 dana. Svi zapisi stariji od 90 dana bit će izbrisani. Međutim, promjenom vrijednosti **polja msdyn_StateOperationSetAge** na **stranici Parametri** projekta administratori mogu prilagoditi raspon čišćenja tako da bude između 1 i 120 dana. Dostupno je nekoliko metoda za promjenu ove vrijednosti:

- **Prilagodite entitet Parametar** projekta stvaranjem prilagođene stranice i dodavanjem polja Postavljena **dob** za ustajale operacije.
- Koristite klijentski kod koji koristi [WebApi komplet za razvoj softvera (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Koristite SDK kod servisa koji koristi Xrm SDK **updateRecord** metodu (referenca klijentskog API-ja) u aplikacijama stvorenim prema modelu. Power Apps uključuje opis i podržane parametre za metodu **updateRecord**.

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
