---
title: Što je novo u prosincu 2021. - Implementacija projektnih operacija
description: Ovaj tema pruža informacije o ažuriranjima kvalitete koja su dostupna u izdanju project operations lite implementacije u prosincu 2021.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942968"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Što je novo u prosincu 2021. - Implementacija projektnih operacija

_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_

Ovaj tema primjenjuje se na sljedeće Microsoftove komponente i verzije Dynamics 365 Project Operations:

- Projektne operacije u Dataverse okruženju verzije 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

### <a name="subcontract-management"></a>Upravljanje kooperantima 

- [Članovi projektnog tima](../subcontracting/subcontracting-project-team-members.md) kooperanta : voditelj projekta može stvoriti imenovane ili generičke članove tima s kooperantima i podizvođačima kako bi utjecao na osoblje i procjenu.
- [Mogućnosti podugovaranja za članove projektnog tima](../subcontracting/subcon-options.md) : Prilikom odabira osoblja za imenovane ili generičke članove projektnog tima, voditelj projekta može pregledati postojeće podugovaratelje ili stvoriti nove podugovaratelje za jednog ili više članova projektnog tima. 
- [Procjena troškova dodjela resursa kooperanta](../subcontracting/costing-subcon-ra.md) : procjena troškova projekta uzet će u obzir dodjele resursa kooperanta i koštat će ih pomoću cjenika nabave povezanih s kooperantima. 
- [Konfiguriranje ploče rasporeda za prikaz ugovornih radnika i kooperantskog](../subcontracting/configure-sb-subcon.md) kapaciteta : Ploča rasporeda u projektnim operacijama sada se može konfigurirati za traženje i predlaganje vrste resursa koji se mogu rezervirati i kooperantskog kapaciteta ugovora zajedno sa zaposlenicima. Ta se konfiguracija može primijeniti pri traženju resursa u kontekstu osoblja za određeni zahtjev projekta ili pri pretraživanju izvan konteksta zahtjeva projekta.
- [Osoblje projekta s ugovornim radnicima i kooperantskim](../subcontracting/staffing-cw.md) kapacitetom : Ugovorni radnici sada se mogu rezervirati na projektima koji koriste iskustva odbora rasporeda.
- [Bilježenje vremena, troškova i upotrebe materijala na projektima za kooperantske komponente](../subcontracting/recording-subcon-actuals.md) : ugovorni radnici mogu bilježiti vrijeme i troškove, a članovi projektnog tima mogu bilježiti i upotrebu materijala kupljenih podizvođačem na projektu. To će dovesti do bilježenja točnih troškova za projekte koji koriste kupljeni kapacitet ili materijale.
- [Prijelazi države na kooperantu](../subcontracting/subcon-states.md) : Podugovarači se mogu potvrditi za dovršetak pregovora s dobavljačem, zatvoreni kako bi naznačili završetak isporuke ili otkazani kako bi se naznačio raskid ugovora s dobavljačem prije završetka isporuke.

### <a name="task-planning"></a>Planiranje zadatka
- Poboljšano otklanjanje poteškoća za administratore sustava. Kada korisnik ne može otvoriti projekt, administrator može pregledati pogreške koje nisu povezane s licencom generirane iz programa Project za web u [zapisnicima za zakazivanje programa Project](../../project-management/schedule-api-logs.md).
- [Koristite kontrolne liste zadataka u programu Microsoft Project za web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). U programu Microsoft Project za web možete dodati kontrolni popis zadatku da biste pratili određene stavke.

## <a name="quality-updates"></a>Ažuriranja kvalitete

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| Planiranje i praćenje | 2392596 | Zakazivanje API-ja sada omogućuje ažuriranja **preostalih pokušaja**, **dovršenog napora** i % **dovršenja** polja. |
| Planiranje i praćenje | 2478497 | Zakazivanje broja aktivnosti API-ja **i** polja **ID-a** zadatka mogu biti prazna pri unosu jer će ih sustav popuniti automatiziranim numeriranjem.|
| Vrijeme i trošak | 2468135 | Broj odobrenja se smanjuje s pet na tri. |
| Vrijeme i trošak | 2468188 | Riješili ste problem s tekstom zapisnika koji premašuje maksimalnu duljinu **atributa** notnog teksta **entiteta** primjedbe. |
