---
title: Zapisnici za planiranje projekata
description: Ovaj tema pruža informacije i uzorke koji će vam pomoći da koristite zapisnike za planiranje projekata za praćenje kvarova povezanih s uslugom zakazivanja projekata i API-jem za planiranje projekata.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1c5632a880fa30d1b863c326b22e3d930c9564dc
ms.sourcegitcommit: 844ec8eacd0fc10d1659b437cc5cbb4480ec9e1e
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/01/2021
ms.locfileid: "7877507"
---
# <a name="project-scheduling-logs"></a>Zapisnici za planiranje projekata

_**Odnosi se na:** Projektne operacije za scenarije temeljene na resursima/zalihama, Lite implementacija - posao do fakturiranja proforma,_ Projekt za _web_

Microsoft Dynamics 365 Project Operations koristi [Project za web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) kao svoj primarni mehanizam za raspoređivanje. Umjesto korištenja standardnih Microsoft Dataverse sučelja za programiranje web-aplikacija (API-je), Project Operations koristi nove API-je za planiranje projekata za stvaranje, ažuriranje i brisanje projektnih zadataka, dodjela resursa, ovisnosti zadataka, grupa projekata i članova projektnih timova. Međutim, kada se operacije kreiranja, ažuriranja ili brisanja programski pokreću na entitetima strukture raščlambe rada (WBS), mogu se pojaviti pogreške. Da biste pratili te pogreške i povijest operacija, implementirana su dva nova administrativna zapisnika: **Skup operacija i Usluga** **zakazivanja projekata (PSS).** Da biste pristupili tim zapisnicima, idite na **Postavke** \> **Zakazivanje integracije**.

Sljedeća ilustracija prikazuje podatkovni model zapisnika zakazivanja projekata.

![Podatkovni model za zapisnike zakazivanja projekata.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Zapisnik skupa operacija

Zapisnik skupa operacija prati izvršavanje skupa operacija koji se koristi za pokretanje jedne ili više operacija stvaranja, ažuriranja ili brisanja u seriji o projektima, projektnim zadacima, dodjelama resursa, ovisnostima o zadacima, projektnim grupama ili članovima projektnog tima. **Polje Operacija u** statusu prikazuje cjelokupno stanje skupa operacija. Detalji o teretu skupa operacija zabilježeni su u povezanim zapisima o detaljima skupa operacija.

### <a name="operation-set"></a>Skup operacija

Sljedeća tablica prikazuje polja povezana s **entitetom Skup** operacija.

| Naziv sheme            | Opis                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Datum/vrijeme dovršetka ili neuspjeha skupa operacija.                                                | CompletedOn            |
| msdyn_correlationid   | Vrijednost **korelacijeId** zahtjeva.                                                                  | CorrelationId          |
| msdyn_description     | Opis skupa operacija.                                                                        | Opis            |
| msdyn_executedon      | Datum/vrijeme izvođenja zapisa.                                                                       | Izvršeno            |
| msdyn_operationsetId  | Jedinstveni identifikator instanci entiteta.                                                                   | OperationSet           |
| msdyn_Project         | Projekt koji je povezan sa skupom operacija.                                                            | Project                |
| msdyn_projectid       | Vrijednost **ID projekta** zahtjeva.                                                                      | ProjectId (zastario) |
| msdyn_projectName     | Nije primjenjivo.                                                                                              | Nije primjenjivo         |
| msdyn_PSSErrorLog     | Jedinstveni identifikator zapisnika pogrešaka usluge zakazivanja projekata koji je povezan sa skupom operacija. | Zapisnik pogrešaka PSS-a          |
| msdyn_PSSErrorLogName | Nije primjenjivo.                                                                                              | Nije primjenjivo         |
| msdyn_status          | Stanje skupa operacija.                                                                             | Stanje                 |
| msdyn_statusName      | Nije primjenjivo.                                                                                              | Nije primjenjivo         |
| msdyn_useraadid       | ID objekta Azure Active Directory (Azure AD) korisnika kojem zahtjev pripada.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detalji skupa operacija

Sljedeća tablica prikazuje polja povezana s **entitetom Skup detalja** operacije.

| Naziv sheme                 | Opis                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Serijalizirana polja Dataverse za zahtjev.                                            | CdsPayload            |
| msdyn_entityname           | Naziv entiteta za zahtjev.                                                     | EntityName            |
| msdyn_httpverb             | Način zahtjeva.                                                                         | HTTPakcija (zastarjelo) |
| msdyn_httpverbName         | Nije primjenjivo.                                                                             | Nije primjenjivo        |
| msdyn_operationset         | Jedinstveni identifikator skupa operacija kojem zapis pripada.                      | OperationSet          |
| msdyn_operationsetdetailId | Jedinstveni identifikator instanci entiteta.                                                  | Pojedinost OperationSet   |
| msdyn_operationsetName     | Nije primjenjivo.                                                                             | Nije primjenjivo        |
| msdyn_operationtype        | Vrsta operacije detalja skupa operacija.                                             | OperationType         |
| msdyn_operationtypeName    | Nije primjenjivo.                                                                             | Nije primjenjivo        |
| msdyn_psspayload           | Polja Serijalizirana usluga zakazivanja projekata za zahtjev.                           | PssPayload            |
| msdyn_recordid             | Identifikator zapisa zahtjeva.                                                       | ID zapisa             |
| msdyn_requestnumber        | Automatski generirani broj koji identificira redoslijed u kojem su zahtjevi primljeni. | Broj zahtjeva        |

## <a name="project-scheduling-service-error-logs"></a>Zapisnici pogrešaka servisa za planiranje projekata

Pogreška servisa za planiranje projekata bilježi pogreške pri snimanju koje se događaju kada servis za planiranje projekata pokuša **operaciju spremanja** ili **otvaranja**. Postoje tri podržana scenarija u kojima se generiraju ti dnevnici:

- Akcije koje je pokrenuo korisnik kritično ne uspijevaju (na primjer, dodjela se ne može stvoriti zbog nedostajućih privilegija).
- Usluga zakazivanja projekata ne može programski stvarati, ažurirati, brisati ili izvoditi bilo koju drugu kaskadnu operaciju na entitetu.
- Korisnik naići na pogreške kada se zapis ne otvori (na primjer, kada se projekt otvori ili se ažuriraju informacije o članu tima).

### <a name="project-scheduling-service-log"></a>Zapisnik servisa za planiranje projekata

Sljedeća tablica prikazuje polja obuhvaćena zapisnikom servisa za planiranje projekata.

| Naziv sheme          | Opis                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Stog poziva za iznimku.                                               | Stog poziva     |
| msdyn_correlationid | ID korelacije pogreške.                                               | CorrelationId  |
| msdyn_errorcode     | Polje koje se koristi za spremanje šifre pogreške Dataverse ili HTTP šifre pogreške. | Kod pogreške     |
| msdyn_HelpLink      | Veza na dokumentaciju javne pomoći.                                       | Veza za pomoć      |
| msdyn_log           | Zapisnik iz usluge zakazivanja projekata.                                   | Zapisnik            |
| msdyn_project       | Projekt povezan s zapisnikom pogrešaka.                             | Project        |
| msdyn_projectName   | Naziv projekta ako će se teret skupa operacija nastaviti. | Nije primjenjivo |
| msdyn_psserrorlogId | Jedinstveni identifikator instanci entiteta.                                     | Zapisnik pogrešaka PSS-a  |
| msdyn_SessionId     | ID sesije projekta.                                                        | ID sesije     |

## <a name="error-log-cleanup"></a>Čišćenje zapisnika pogrešaka

Prema zadanim postavkama i zapisnici pogrešaka servisa za planiranje projekata i zapisnik skupa operacija mogu se čistiti svakih 90 dana. Svi zapisi stariji od 90 dana bit će izbrisani. Međutim, promjenom vrijednosti **polja msdyn_StateOperationSetAge na** **stranici Parametri projekta** administratori mogu prilagoditi raspon čišćenja tako da bude između 1 i 120 dana. Dostupno je nekoliko metoda za promjenu ove vrijednosti:

- Prilagodite **entitet Parametar projekta** stvaranjem prilagođene stranice i dodavanjem **polja Vrijeme skupa ustajalih** operacija.
- Koristite klijentski kod koji koristi [WebApi komplet za razvoj softvera (SDK).](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord)
- Koristite Kod Service SDK koji koristi Xrm SDK **updateRecord** metodu (referenca klijentskog API-ja) u aplikacijama utemeljenim na modelu. Power Apps sadrži opis i podržane parametre za **metodu** updateRecord.

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
