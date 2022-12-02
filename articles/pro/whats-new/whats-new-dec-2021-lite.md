---
title: Što je novo u prosincu 2021. – Osnovna implementacija aplikacije Project Operations
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju osnovne implementacije aplikacije Project Operations za prosinac 2021. godine.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914071"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Što je novo u prosincu 2021. – Osnovna implementacija aplikacije Project Operations

_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

### <a name="subcontract-management"></a>Upravljanje podugovorima 

- [Članovi projektnog tima za podugovaranje](../subcontracting/subcontracting-project-team-members.md): voditelj projekata može stvoriti imenovane ili generičke članove tima s podugovorima i recima podugovora kako bi utjecao na zapošljavanje i procjenu.
- [Mogućnosti podugovaranja za članove projektnog tima](../subcontracting/subcon-options.md): prilikom odabira osoblja za imenovane ili generičke članove projektnog tima, voditelj projekata može pregledati postojeće podugovore ili stvoriti nove podugovore za jednog ili više članova projektnog tima. 
- [Procjena troškova dodjele podugovorenih resursa](../subcontracting/costing-subcon-ra.md): procjena troškova projekta uzet će u obzir dodjele podugovorenih resursa i izračunat će ih korištenjem nabavnih cjenika povezanih s podugovorima. 
- [Konfigurirajte ploču rasporeda za prikaz ugovornih radnika i podugovorenih kapaciteta](../subcontracting/configure-sb-subcon.md): ploča s rasporedom u aplikaciji Project Operations sada se može konfigurirati za traženje i predlaganje vrste ugovornog radnika za resurse koji se mogu rezervirati i podugovorenih kapaciteta zajedno sa zaposlenicima. Ova se konfiguracija može primijeniti kada se traže resursi unutar konteksta zapošljavanja za određeni projektni zahtjev ili kada se traži izvan konteksta projektnog zahtjeva.
- [Osoblje na projektu s ugovornim radnicima i podugovorenim kapacitetima](../subcontracting/staffing-cw.md): ugovorni radnici sada mogu biti angažirani na projektima koristeći iskustva ploče za raspored.
- [Bilježenje vremena, troškova i upotrebe materijala na projektima za podugovorene komponente](../subcontracting/recording-subcon-actuals.md): ugovorni radnici mogu bilježiti vrijeme i troškove, a članovi projektnog tima također mogu bilježiti upotrebu materijala nabavljenih putem podugovora na projektu. To će rezultirati bilježenjem točnih troškova na projektima koji koriste nabavljeni kapacitet ili materijale.
- [Prijelazi stanja na podugovor](../subcontracting/subcon-states.md): podugovori se mogu potvrditi kako bi se završili pregovori s dobavljačem, zatvoriti kako bi se označio završetak isporuke ili otkazati kako bi se označio raskid ugovora s dobavljačem prije završetka isporuke.

### <a name="task-planning"></a>Planiranje zadataka
- Poboljšano otklanjanje poteškoća za administratore sustava. Kada korisnik ne može otvoriti projekt, administrator može pregledati pogreške koje nisu povezane s licencom generirane iz aplikacije Project for the web u [Dnevnicima planiranja projekta](../../project-management/schedule-api-logs.md).
- [Koristite kontrolne popise zadataka u aplikaciji Microsoft Project for the web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). U aplikaciji Microsoft Project for the web možete dodati kontrolni popis u zadatak kako biste pratili određene stavke.

## <a name="quality-updates"></a>Ažuriranja kvalitete

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| Planiranje i praćenje | 2392596 | API-ji za raspored sada dopuštaju ažuriranja za polja **Preostali napor**, **Napor dovršen** i **% dovršeno**. |
| Planiranje i praćenje | 2478497 | Polja API-ja za raspored **Broj aktivnosti** i **ID zadatka** mogu biti prazna pri unosu jer će ih sustav popuniti s pomoću automatskog numeriranja.|
| Vrijeme i trošak | 2468135 | Broj ponovnih pokušaja odobrenja smanjen je s pet na tri. |
| Vrijeme i trošak | 2468188 | Riješen je problem s tekstom zapisnika koji premašuje maksimalnu duljinu u atributu **tekst bilješke** entiteta **anotacija**. |
