---
title: Novosti u veljači 2021. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju aplikacije Project Operations za veljaču 2021. za scenarije koji se temelje na resursu / bez zaliha.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1fe1e59a0a3674752fe62525349a50f00e11089b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029606"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u veljači 2021. – Project Operations za scenarije temeljene na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

- Project Operations u okruženju 4.7.0.95 platforme Dataverse
- Upravljanje projektima i računovodstvo u verziji 10.0.16 okruženja aplikacije Dynamics 365 Finance 

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| **Naplata i određivanje cijene** | 2053736 | Pojedinosti retka fakture sada su dostupne odlaskom na **Faktura** > **Povezane informacije**. |
| **Naplata i određivanje cijene** | 2122613 | Radnje **Aktiviraj** i **Deaktiviraj** uklonjene su iz entiteta združivanja **Cjenik**. |
| **Naplata i određivanje cijene** | 2128606 | Riješen je problem sa **ullReferenceException** u dodatku **GetEstimatesForProject**. |
| **Implementacija i konfiguracija** | 2139346 | Riješen je problem s uvozom neupravljanog rješenja **Dynamics365ProjectOperationsDualWrite**. |
| **Implementacija i konfiguracija** | 2140569 | Projektno rješenje ne mora biti instalirano u okruženju Teams platforme Dataverse. |
| **Implementacija i konfiguracija** | 2086991 | Ograničena je prilagodba lokalizacije web-resursa. |
| **Upravljanje prilikama** | 2136794 | Prikazuje se ispravna poruka o pogrešci kada ne uspije postupak **Potvrdi fakturu** ili **Označi fakturu kao plaćenu**. |
| **Upravljanje prilikama** | 2139330 | Promjena voditelja projekta na projektu ne smije vratiti tvrtku koja je vlasnik natrag na zadanu vrijednost. |
| **Upravljanje prilikama** | 2146376 | Pravilan iznos poreza u nenaplativo stvarnom podatku stvara se iz potvrde fakture. |
| **Planiranje i praćenje projekta** | 2099879 | Implementacija okruženja platforme Dataverse mora stvoriti zadanu kategoriju transakcije sa statičkim ID-om, a ne nasumično generirati jednu po okruženju. |
| **Planiranje i praćenje projekta** | 2128577 | Ispravljena je ovlast korisnika u aplikaciji Project service za ažuriranje kategorije transakcije u dodjeli resursa. |
| **Planiranje i praćenje projekta** | 2164035 | Ispravljeni su problemi s funkcijom **Kopiraj projekt**. |
| **Vremenski unos** | 2129161 | Primjenjuju se stroža ograničenja kako bi se osiguralo da korisnici ne mogu mijenjati i ažurirati vremenski unos koji je poslan ili odobren. |
| **Vremenski unos** | 2103572 | Odobrenje vremena za unose koji se ne odnose na projekt ne smije tražiti ulogu odobravatelja projekta. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u aplikaciji Dynamics 365 Finance 

Dodatne informacije o upravljanju projektima i računovodstvu u aplikaciji Dynamics 365 Finance potražite u odjeljku [Što je novo u siječnju 2021. – Project Operations za scenarije koji se temelje na resursima / bez zaliha](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Ažuriranja propisa

Za informacije o ažuriranjima propisa za aplikacije za financije i operacije pogledajte članak [Ažuriranja propisa](/dynamics365/finance/localizations/regulatory-updates). Drugi način da saznate više o regulatornim ažuriranjima jest prijava na Lifecycle Services (LCS) i pregledavanje planiranih regulatornih ažuriranja s pomoću alata za pretraživanje problema. Pretraživanje izdanja omogućuje vam pretraživanje po zemlji, vrsti značajke i izdanju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]