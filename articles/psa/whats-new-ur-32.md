---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 32, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 3ad87eceb90a48997aadf00803b8d14c5108eb83
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580079"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 32, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 32. Ova verzija ima broj međuverzije V3.10.53.108 i općenito je dostupna putem samostalnog ažuriranja u lipnju 2021. godine.

## <a name="update-release-32"></a>Izdanje ažuriranja 32

### <a name="bug-fixes"></a>Ispravke pogrešaka

#### <a name="general"></a>Općenito

- Kada glavna nadogradnja ne uspije, treba blokirati samo glavne ulazne točke aplikacije kako bi se osiguralo da dijeljeni entiteti i dalje budu dostupni.

#### <a name="time-and-expense"></a>Vrijeme i trošak

Popravljeni su sljedeći problemi:

- **TimeEntriesImportFromResourceAssignment** ne održava vrijeme početka i završetka isječka konture za dodjelu resursa.
- Kad odaberete **Otvoreni unos** na rešetki **Vemenski unos**, možda nećete moći odabrati druge obrasce.
- Dok uvozite zadatke u vremenske unose, upit kôda klijenta mogao bi generirati dugačku URL-adresu koja ne uspijeva u upitu.
- U rešetki **Vremenski unos**, nakon što se vrijednost izbriše iz ćelije, fokus ne ostaje u rešetki.
- Gumb **Odbaci** uklonjen je s prikaza **Obrada odobrenja** za nova odobrenja.
- Na stabilnost i izvedbu skupnog odobravanja vremenskog unosa utječu zastoji i neuspješno rukovanje prilagodbama, koje su povezane s entitetom **Vremenski unos**, na odgovarajući način.

#### <a name="project-planning"></a>Planiranje projekta

- Iznimka nulte reference generira se kada ažurirate projekt koji ima nultu vrijednost u polju **Ugovorna jedinica**.
- **Osvježi ukupne vrijednosti projekata** pogrešno izračunava preostali trošak i preostalu prodaju na projektu.
- Izračuni prekomjerne cijene utječu na učinkovitost povezanu s ažuriranjima na konturama dodjele resursa.

#### <a name="resource-management"></a>Upravljanje resursima

Popravljen je sljedeći profil:

- Kada je kalendarski kapacitet resursa koji možete rezervirati veći od 1, Project Service Automation pogrešno prepoznaje kapacitet kao 0 (nula). Stoga se u prikazu rasporeda prikazuje beskonačna petlja.

#### <a name="sales"></a>Prodaje

Popravljeni su sljedeći problemi:

- Kada se stvori redak dnevnika koji ima prilagođenu vrstu transakcije, prikazuje se sljedeći izuzetak nulte reference: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType (TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Prije kopiranja ponude ne biste trebali dodavati uloge i kategorije koje su neaktivne u uloge koje se naplaćuju i kategorije novokopirane ponude.
- Datumi dokumenta i obračuna nisu usklađeni s datumom početka koji je naveden u pojedinosti retka fakture i koji stvoren izravno na nacrtu fakture.
- Iznimke nulte reference generiraju se u scenarijima koji su povezani s naktivacijom uloga i kategorija prije kopiranja ponude.
- Radnja **Ažuriraj cijene** na stranici **Projekti** ne ažurira procjene troškova i materijala.
