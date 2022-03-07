---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 30, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 30, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010417"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 30, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution.md).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 30. Ova verzija ima broj međuverzije V3.10.51.61 i uglavnom je dostupna putem samostalnog ažuriranja u travnju 2021. godine.

## <a name="update-release-30"></a>Izdanje ažuriranja 30

### <a name="bug-fixes"></a>Ispravke pogrešaka

**Vrijeme i trošak**

Popravljeni su sljedeći problemi:

- Do pogreške dolazi kada stvorite i spremite vremenski unos na stranici **Brzo stvaranje** ako je uklonjeno polje **Uloga**.
- Filtar Unos vremena primjenjuje pogrešni operator filtra.
- Kopirane vremenske tablice ne prikazuju se automatski kada odaberete **Kopiraj tjedan** na kontroli vremenskog unosa.

**Upravljanje resursima**

Popravljeni su sljedeći problemi:

- Kada produžujete rezervaciju, stanje rezervacije dodijeljeno fiksnoj rezervaciji nije ispravno. Produljenjem rezervacije poštuje se stanje rezervacije definirano kao **Izvršeno** u metapodacima postavki rezervacije.
- Kada nije navedeno valjano stanje rezervacije, poruka o pogrešci nije pravilno lokalizirana.

**Upravljanje projektom**

Popravljeni su sljedeći problemi:

- Projekti se ne mogu stvarati u jednoj valuti, a da obuhvaćaju povezane zadatke u drugoj valuti.

**Prodaja**

Popravljeni su sljedeći problemi:

- Kada se cjenik kopira, cijene se ne ažuriraju.
- Zatvaranje ponude kao prihvaćene ne uspijeva kada pojedinost troška ima vrijednost za original.
- U entitetu **Zadatak projekta**, **Procijenjeni trošak** preimenovan je u **Planirani trošak (osnovni)**.
- Izuzetak nulte reference generira se kad se fakture stvore ili izbrišu.
