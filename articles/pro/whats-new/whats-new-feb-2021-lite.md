---
title: Novosti u veljači 2021. – osnovna implementacija aplikacije Project Operations
description: U ovoj temi nalaze se informacije o ažuriranjima kvalitete dostupnim u izdanju osnovne implementacije aplikacije Project Operations za veljaču 2021.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: df6490d3d9c28b095efd5ef856064de4b1517055
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272154"
---
# <a name="whats-new-february-2021---project-operations-lite-deployment"></a>Novosti u veljači 2021. – osnovna implementacija aplikacije Project Operations

Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

  - Project Operations na verziji 4.7.0.95 okruženja platforme Dataverse

## <a name="quality-updates"></a>Ažuriranja kvalitete

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| **Naplata i određivanje cijene** | 2053736 | Pojedinosti retka fakture sada su dostupne odlaskom na **Faktura** > **Povezane informacije**. |
| **Naplata i određivanje cijene** | 2122613 | Radnje **Aktiviraj** i **Deaktiviraj** uklonjene su iz entiteta združivanja **Cjenik**. |
| **Naplata i određivanje cijene** | 2128606 | Riješen je problem sa **ullReferenceException** u dodatku **GetEstimatesForProject**. |
| **Implementacija i konfiguracija** | 2140569 | Projektno rješenje ne mora biti instalirano u okruženju Teams platforme Dataverse. |
| **Implementacija i konfiguracija** | 2086991 | Ograničena je prilagodba lokalizacije web-resursa. |
| **Upravljanje prilikama** | 2136794 | Prikazuje se ispravna poruka o pogrešci kada ne uspije postupak **Potvrdite fakturu** ili **Označite fakturu kao plaćenu**. |
| **Upravljanje prilikama** | 2146376 | Pravilan iznos poreza u nenaplativo stvarnom podatku stvara se iz potvrde fakture. |
| **Planiranje i praćenje projekta** | 2099879 | Implementacija okruženja platforme Dataverse mora stvoriti zadanu kategoriju transakcije sa statičkim ID-om, a ne nasumično generirati jednu po okruženju. |
| **Planiranje i praćenje projekta** | 2128577 | Ispravljena je ovlast korisnika u aplikaciji Project service za ažuriranje kategorije transakcije u dodjeli resursa. |
| **Planiranje i praćenje projekta** | 2164035 | Ispravljeni su problemi s funkcijom **Kopiraj projekt**. |
| **Vremenski unos** | 2129161 | Primjenjuju se stroža ograničenja kako bi se osiguralo da korisnici ne mogu mijenjati i ažurirati vremenski unos koji je poslan ili odobren. |
| **Vremenski unos** | 2103572 | Odobrenje vremena za unose koji se ne odnose na projekt ne smije tražiti ulogu odobravatelja projekta. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]