---
title: Novosti u prosincu 2021. – implementacija lite projekata projektnih operacija
description: Ovaj tema pruža informacije o ažuriranjima kvalitete koja su dostupna u izdanju u prosincu 2021. uvođenja lite projekta Project Operations.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1ff0a14bf6cb445913bcba11f83234826014857
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585369"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Novosti u prosincu 2021. – implementacija lite projekata projektnih operacija

_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_

Ovaj tema odnosi se na sljedeće microsoftove Dynamics 365 Project Operations komponente i verzije :

- Operacije projekta u verziji okruženja Dataverse 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

### <a name="subcontract-management"></a>Upravljanje kooperantima 

- [Članovi](../subcontracting/subcontracting-project-team-members.md) projektnog tima za podugovaranje: Voditelj projekta može stvoriti imenovane ili generičke članove tima s podugovarateljima i linijama podugovaranja kako bi utjecao na osoblje i procjenu.
- [Mogućnosti podugovaranja za članove](../subcontracting/subcon-options.md) projektnog tima: Prilikom odabira osoblja imenovanih ili generičkih članova projektnog tima, voditelj projekta može pregledati postojeće podugovarate ili stvoriti nove podugovarate za jednog ili više članova projektnog tima. 
- [Procjena troškova dodjela kooperantskih resursa: Procjena troškova](../subcontracting/costing-subcon-ra.md) projekta uzet će u obzir dodjele resursa kooperanta i koštat će ih pomoću popisa nabavnih cijena povezanih s kooperantima. 
- [Konfigurirajte ploču za raspored tako da prikazuje ugovorne radnike i kapacitet](../subcontracting/configure-sb-subcon.md) kooperanta: Ploča za raspored u projektnim operacijama sada se može konfigurirati za traženje i predlaganje vrste resursa koji se mogu rezervirati i kapaciteta ugovornog radnika zajedno sa zaposlenicima. Ta se konfiguracija može primijeniti pri traženju resursa u kontekstu osoblja za određeni zahtjev projekta ili pri pretraživanju izvan konteksta zahtjeva projekta.
- [Kadroviranje projekta s ugovornim radnicima i kapacitetom](../subcontracting/staffing-cw.md) podugovaratelja: Ugovorni radnici sada se mogu rezervirati na projektima koji koriste iskustva s rasporedom odbora.
- [Bilježenje vremena, troškova i korištenja materijala na projektima za komponente](../subcontracting/recording-subcon-actuals.md) podugovaratelja: Ugovorni radnici mogu bilježiti vrijeme i troškove, a članovi projektnog tima također mogu zabilježiti upotrebu materijala kupljenih pomoću podugovaratelja na projektu. To će rezultirati bilježenjem točnih troškova projekata koji koriste kupljeni kapacitet ili materijale.
- [Prijelazi države na podugovaranju](../subcontracting/subcon-states.md): Kooperanti se mogu potvrditi da dovrše pregovore s dobavljačem, zatvoreni kako bi se naznačio završetak isporuke ili otkazani kako bi se naznačio raskid ugovora s dobavljačem prije završetka isporuke.

### <a name="task-planning"></a>Planiranje zadataka
- Poboljšano otklanjanje poteškoća za administratore sustava. Kada korisnik ne može otvoriti projekt, administrator može pregledati pogreške koje nisu povezane s licencom generirane iz programa Project za web u [zapisnicima zakazivanja projekata](../../project-management/schedule-api-logs.md).
- [Koristite kontrolne popise zadataka u programu Microsoft Project za web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). U programu Microsoft Project za web možete dodati kontrolni popis zadatku da biste pratili određene stavke.

## <a name="quality-updates"></a>Ažuriranja kvalitete

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| Planiranje i praćenje | 2392596 | Zakazivanje API-ja sada dopušta ažuriranja **polja Preostali napor**, **Dovršeni** napori i **% dovršenosti**. |
| Planiranje i praćenje | 2478497 | Zakazivanje API-ja **Broj** aktivnosti i **ID** zadatka polja mogu biti prazna na ulazu jer će ih sustav popuniti pomoću automatiziranog numeriranja.|
| Vrijeme i trošak | 2468135 | Broj ponovnih pokušaja odobrenja smanjuje se s pet na tri. |
| Vrijeme i trošak | 2468188 | Riješen je problem s tekstom zapisnika koji premašuje maksimalnu duljinu **u atributu notetext** entiteta **primjedbe**. |
