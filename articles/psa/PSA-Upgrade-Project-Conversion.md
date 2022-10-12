---
title: Promjene značajki za automatizaciju projektnih usluga u projektne operacije
description: U ovom se članku daje pregled promjena značajki za Microsoft Dynamics 365 Project Service Automation Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621318"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Promjene značajki za automatizaciju projektnih usluga u projektne operacije

Nakon što je projekt uspješno nadograđen s 3.X na Microsoft Dynamics 365 Project Service Automation Lite, uređivanje projektnih zadataka Dynamics 365 Project Operations u strukturi kvara radne mreže zadataka (WBS) nije moguće. Kupci će moći pregledati WBS-ove u mreži za praćenje u kojoj su dodana nova polja kako bi se pružili svi detalji koji se odnose na zadatak. Za projekte u kojima su potrebna uređivanja WBS-a možete selektivno pretvoriti prihvatljive projekte u novi projekt za iskustvo zakazivanja weba.

## <a name="project-conversion-process"></a>Postupak pretvorbe projekta

Da biste pretvorili projekt, slijedite ove korake.

1. Otvorite glavnu stranicu projekta i u oknu akcije odaberite **Pretvori**.
1. U okviru s potvrdnom porukom odaberite **U redu** da biste započeli pretvorbu projekta. Događaju se sljedeće akcije:

    1. Traka za poruke koja se pojavljuje na glavnoj stranici projekta kaže: "Raspored projekta se pretvara. Ne možete mijenjati projekt dok se pretvorba ne dovrši."
    1. Preusmjereni ste na popis projekata.

    Nakon dovršetka pretvorbe projekta događaju se sljedeće akcije:

    1. Dodijeljeni voditelj projekta prima obavijest na desnoj strani aplikacije.
    1. Uklanja se traka za poruke na kojoj se navodi da je pretvorba u tijeku.
    1. Kartica **Raspored** prikazuje novo iskustvo zakazivanja s programom Project za web. Svaki korisnik koji ima odgovarajuće licence i sigurnosne uloge može urediti WBS.
    1. Polje modula **za** zakazivanje ažurira se u **Project za web**.
    1. Gumb **Pretvori** uklanja se iz okna akcije.

> [!IMPORTANT]
> Masovna prenamjena projekata nije dopuštena. Svaki pokušaj ažuriranja velikog broja projekata u isto vrijeme bit će zagušen. Ovo ograničenje pomaže osigurati visoke performanse za sve kupce.

## <a name="manual-tasks-vs-automatic-tasks"></a>Ručni zadaci u odnosu na automatske zadatke

Kada se okruženje nadogradi s automatizacije projektnih usluga na projektne operacije, svi zadaci u WBS-u smatraju se automatski zakazanima. Koncept ručno zakazanih zadataka nije dostupan u programu Project za web. Međutim, željeno ponašanje zakazivanja projekata možete definirati pomoću [postavke načina zakazivanja](/project-management/scheduling-modes.md) prilikom stvaranja novih projekata.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Ograničene operacije za projekte prije pretvorbe

U ovom se odjeljku opisuju funkcionalne razlike koje možete očekivati kada projekti nisu pretvoreni.

### <a name="copy-project"></a>Kopiraj projekt

Operacija Kopiranje **podržana** je samo na pretvorenim projektima. Nadograđene projekte nije moguće kopirati prije pretvorbe.

### <a name="move-project"></a>Premjesti projekt

Promjena datuma početka projekta neće razmjerno pomaknuti početak zadataka ako projekt nije pretvoren.

## <a name="frequently-asked-questions"></a>Najčešća pitanja

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Koje su razlike između pretvorenih projekata i novih projekata koji se stvaraju nakon dovršetka nadogradnje?

Za projekte koji se pretvaraju nakon nadogradnje okruženja postavit će se zastavica koja upućuje raspored da poštuje samo kalendar projekta. To se ponašanje podudara s ponašanjem u automatizaciji usluge projekta. Međutim, zastavica neće biti postavljena za nove projekte stvorene nakon nadogradnje. Stoga će raspored poštivati radno vrijeme resursa kada su dodijeljeni zadatku.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Što trebam učiniti ako se projekt ne uspije pretvoriti?

Ako se vaš projekt ne uspije pretvoriti, prvi korak je pregled zapisnika pogrešaka kako biste identificirali uobičajene probleme povezane s vašim WBS-om. Ako zapisnici ne ukazuju na određenu pogrešku na kojoj možete poduzeti mjere, obratite se korisničkoj podršci kako bi se vaš slučaj mogao dalje pregledati.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Kako se postupa sa zatvaranjem poduzeća u programu Project za web?

Projekt za web ne poštuje zatvaranje poslovanja koje poduzeće definira na razini organizacije. Međutim, poštovat će druge vrste slobodnih dana koje su definirane u određenom predlošku radnog vremena.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Koja su ograničenja projekta za web?

Pročitajte članak [Stvaranje strukture raščlambe](/project-management/create-wbs#project-limitations.md) rada: Ograničenja projekta.

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Mogu li očekivati promjene u procjenama troškova i prodaje?

U rijetkim slučajevima kada se konture dodjele resursa ponovno izračunavaju ili kada padaju na granicu različitog datuma od izvornog projekta, možda ćete vidjeti razlike u procjenama prodaje i troškova. Kao dio postupka nadogradnje, od kupaca se očekuje da testiraju reprezentativni uzorak skupa projekata kako bi mogli razumjeti sve potencijalne promjene rasporeda.
