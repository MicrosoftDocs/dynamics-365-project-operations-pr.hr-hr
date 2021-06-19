---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 17, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 17, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 364a64e0ea501ac5b7faaf254c7af3648cfe1f9b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006682"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation, izdanje ažuriranja 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti.  Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji PSA V3, izdanje ažuriranja 17. Ova verzija ima broj međuverzije V3.10.6.34 i općenito je dostupna putem samostalnog ažuriranja iz ožujka 2020.


## <a name="update-release-17"></a>Izdanje ažuriranja 17

### <a name="bug-fixes"></a>Ispravke pogrešaka

**Općenito**

- Popravljeno: Ažurirajte rješenje Project Service Automation kako biste primijenili licence za članove tima (Središte resursa projekta uključuje metapodatke 3.x plana usluge za člana tima)
 
**Vrijeme i trošak**

- Popravljeno: Procjenu rashoda nije moguće promijeniti s vrijednosti koja nije jednaka nuli na nulu (0). Promjena se zanemaruje.

**Upravljanje projektom**

- Popravljeno: U naziv položaja člana tima dodana je provjera za nulte vrijednosti.
- Popravljeno: Polje **msdyn_userresourceid** entiteta **msdyn_resourceassignment** je zastarjelo.
- Popravljeno: Nadogradnja s verzije 2.x na verziju 3.x sada obrađuje prazne konture rada na dodijeljenim zadacima.

**Sales**

- Popravljeno: **Invoice.PreValidateInvoiceUpdate** sada obrađuje scenarij pravilne preraspodjele vlasnicima zapisa.
- Popravljeno: Kad je klasa transakcije **Vrijeme**, stavka **UnitGroup** ne može se uređivati za sve subjekte, uključujući stavke **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** i **ContractLineDetails**. Međutim, **Unit** ne može se uređivati samo za stavke **JournalLine** i **InvoiceLineDetails**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]