---
title: Proces pretvorbe planiranja projekta Project Service Automation u Project Operations
description: U ovom članku nalazi se pregled promjena značajki za nadogradnju Microsoft Dynamics 365 Project Service Automation na Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642559"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Proces pretvorbe planiranja projekta Project Service Automation u Project Operations

Nakon što se projekt uspješno s Microsoft Dynamics 365 Project Service Automation 3.X nadogradi na Dynamics 365 Project Operations Lite, uređivanje projektnih zadataka u strukturnoj analizi rada (WBS) u rešetki zadataka neće biti moguće. Korisnici će moći pregledati WBS-ove u rešetki za praćenje gdje su dodana nova polja kako bi se pružile sve pojedinosti koje se odnose na zadatak. Za projekte za koje je potrebno urediti WBS možete sve prikladne projekte selektivno pretvoriti u novo iskustvo planiranja Project for the Web.

## <a name="project-conversion-process"></a>Proces pretvorbe projekta

Za pretvorbu projekta pratite sljedeće korake.

1. Otvorite glavnu stranicu projekta i u oknu Akcija odaberite **Pretvori**.
1. U okviru potvrdne poruke koji će se prikazati odaberite **U redu** kako biste pokrenuli pretvorbu projekta. Izvršit će se sljedeće akcije:

    1. U traci za poruke koja se prikazuje na glavnoj stranici projekta navedeno je „Raspored projekta se pretvara. Ne možete mijenjati projekt dok se pretvorba ne završi.”
    1. Preusmjerit ćete se na popis projekata.

    Kad pretvorba projekta bude gotova, doći će do sljedećih akcija:

    1. Dodijeljeni voditelj projekta dobit će obavijest na desnoj strani aplikacije.
    1. U traci za poruke navedeno je da je pretvorba koja je u tijeku uklonjena.
    1. Na kartici **Raspored** prikazuje prikazuje se novo iskustvo planiranja sa značajkom Project for the Web. Svaki korisnik koji ima odgovarajuće licence i sigurnosne uloge može uređivati WBS.
    1. Polje **Modul planiranja** ažurirat će se na **Project for the Web**.
    1. Gumb **Pretvori** uklonjen je iz okna Akcija.

> [!IMPORTANT]
> Skupna konverzija projekata nije dopuštena. Svaki pokušaj ažuriranja mnogo projekata odjednom bit će usporen. To ograničenje omogućuje osiguravanje visokih performansi za sve klijente.

## <a name="manual-tasks-vs-automatic-tasks"></a>Ručni zadaci naspram automatskih zadataka

Kada se okruženje s Project Service Automation nadogradi na Project Operations, svi zadaci u WBS-u smatraju se automatski planiranima. Koncept ručno planiranih  zadataka nije dostupan u značajki Project for the Web. Međutim, željeno ponašanje planiranja za svoje projekte možete kada stvarate nove projekte definirati s pomoću postavke [načina planiranja](/project-management/scheduling-modes.md).

## <a name="restricted-operations-for-pre-conversion-projects"></a>Ograničene operacije za projekte prije pretvorbe

U ovom odjeljku opisane su funkcionalne razlike koje možete očekivati kad projekti još nisu pretvoreni.

### <a name="copy-project"></a>Kopiranje projekta

Operacija **Kopiraj** podržana je samo za pretvorene projekte. Ažurirani projekti ne mogu se kopirati prije pretvorbe.

### <a name="move-project"></a>Premještanje projekta

Promjena datuma početka projekta neće proporcionalno pomaknuti početak zadataka ako projekt nije pretvoren.

## <a name="frequently-asked-questions"></a>Najčešća pitanja

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Koje su razlike između pretvorenih projekata i novih projekata koji se stvaraju nakon dovršetka nadogradnje?

Za projekte koji se pretvaraju nakon nadogradnje okruženja postavit će se oznaka koja rasporedu nalaže da se pridržava samo projektnog kalendara. To ponašanje odgovara ponašanju u Project Service Automation. Međutim, zastavica se neće postaviti za nove projekte koji su stvoreni nakon nadogradnje. Stoga će se raspored pridržavati radnog vremena resursa kad su oni dodijeljeni zadatku.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Što trebam učiniti ako pretvorba mojeg projekta ne uspije?

Ako se projekt ne uspije pretvoriti, prvi je korak pregledati zapisnike pogrešaka kako bi se prepoznali bilo kakvi uobičajeni problemi koji su povezani s vašim WBS-om. Ako u zapisniku nije navedena specifična pogreška za koju nešto možete poduzeti, obratite se korisničkoj podršci kako bi se vaš slučaj mogao dodatno istražiti.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Kako se u Project for the Web rješava zatvaranje poduzeća?

Project for the Web ne pridržava se zatvaranja poduzeća koja tvrtka definira na razini organizacije. Pridržavat će se, međutim svih drugih vrsta slobodnih dana koji su definirani u odgovarajućem predlošku radnog vremena.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Koja su ograničenja značajke Project for the Web?

Pogledajte [Stvaranje strukturne analize rada: ograničenja projekta](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Mogu li očekivati promjene procjene troškova i prodaje?

U rijetkim slučajevima može doći do razlika u procjenama prodaje i troškova pri ponovnom izračunu kontura dodjele resursa ili kad one padnu na različitu datumsku granicu od one izvornog projekta. U sklopu procesa nadogradnje od klijenata se očekuje da testiraju reprezentativni uzorak skupa projekata kako bi razumjeli sve potencijalne promjene rasporeda.
