---
title: Što je novo u studenome 2022. – Osnovna implementacija aplikacije Project Operations
description: U ovom se članku nalaze informacije o kvalitetnim ažuriranjima koja su dostupna u izdanju implementacije sustava Microsoft Dynamics 365 Project Operations Lite u studenome 2022.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: ed61f8c03c4ab1960aaf97712b3d46dc298ce96a
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831129"
---
# <a name="whats-new-november-2022---project-operations-lite-deployment"></a>Što je novo u studenome 2022. – Osnovna implementacija aplikacije Project Operations

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.58.0.119


## <a name="quality-updates"></a>Ažuriranja kvalitete

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2781818 | Pogreška prilikom zadane cijene za zapisnik korištenja materijala nije pronađena ključem. |
| Naplata i određivanje cijene | 2922373 | Nije moguće povezati redak ponude s projektom koji je zatvoren kao izgubljena ponuda. |
| Naplata i određivanje cijene | 2943206 | **Polje Redak** ugovora u entitetu projekta mora biti neobavezno. |
| Naplata i određivanje cijene | 2953182 | Poboljšajte poruku o pogrešci za korektivne fakture.|
| Naplata i određivanje cijene | 2959500 | Nije moguće povezati redak ponude s projektnim zadatkom koji je već povezan s izgubljenom ponudom.|
| Naplata i određivanje cijene | 2959560 | Poruka "Ovaj kupac je već na ugovoru o projektu" primljena je tijekom zatvaranja ponude kao osvojene u određenim regionalnim shemama. |
| Naplata i određivanje cijene | 3031727 | Dodjele resursa ne uspijevaju s pogreškom Obavezno polje 'msdyn_Company'. |
| Naplata i određivanje cijene | 3036905 | Posjedovanje tvrtke nikada nije inicijalizirano na ProjectTeamMember. |
| Upravljanje prilikama | 2763519 | Pogreška Null Reference u odjeljku EnsureProjectContractAllowsUpdates. |
| Upravljanje prilikama | 2783798 | Prilikom uvoza procjena projekta u redak ponude nedostaju opisi zadataka za procjene troškova i materijala.|
| Upravljanje prilikama | 2988635 | Poboljšajte msg opis pogreške prilikom brisanja kupca na ponudi. |
| Upravljanje prilikama | 3001191 | Nije moguće stvoriti ponudu iz prilike u kojoj je način naplate naveden kao null. |
| Nadogradnja | 3012324 | Pretvorba projekta nije uspjela na projektu s kontrolnim znakovima kao što je Tab u nazivu. || Planiranje i praćenje projekta | 2790384 | Prekoračenje vremena skupa operacija na čekanju je prekratko. |
| Planiranje i praćenje projekta | 3044275 | Nedostaje lokalizacija za: nedostajeProjectSchedulerErrorMessage. |
| Planiranje i praćenje projekta | 3044277 | Rešetka izviđača projekta ne učitava se kada je planer neiskorišten.|
| Upravljanje resursima | 2943153 | Ažuriraj karticu Praćenje da bi se prikazala dva decimalna mjesta za Trajanje.|
| Podugovaranje | 2932774 | Pogreška u neispravnom odbacivanju retka fakture Za čitanje samo bacanje. |
| Podugovaranje | 2939556 | Status zaglavlja fakture dobavljača ne bi trebao biti postavljen na Skica internetskog brisanja ako nije aktivna. |
| Vrijeme i trošak | 2939998 | Iskoristite novu TESA verziju u ProjOpsu. |
