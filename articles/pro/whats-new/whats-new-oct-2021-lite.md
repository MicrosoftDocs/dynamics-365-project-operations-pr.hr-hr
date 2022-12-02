---
title: Što je novo u listopadu 2021. – Osnovna implementacija aplikacije Project Operations
description: U ovom članku nalaze se podaci o ažuriranjima kvalitete dostupnima u izdanju osnovne implementacije aplikacije Project Operations za listopad 2021.
author: sigitac
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7199853bea7e8e99a2a1ce19d6ce88736edb38f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921937"
---
# <a name="whats-new-october-2021---project-operations-lite-deployment"></a>Što je novo u listopadu 2021. – Osnovna implementacija aplikacije Project Operations

_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

  - Project Operations u verziji 4.25.0.91 okruženja platforme Microsoft Dataverse


## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

U ovo izdanje uključene su sljedeće značajke:

[Upravljanje podugovorima](../subcontracting/managing-subcontracts-overview.md): Ova značajka pruža mogućnost stvaranja podugovora s dobavljačem, navođenja svih kupnji kao stavki retka na podugovoru, prilagođavanja cijena i povezivanja kontakata.


## <a name="quality-updates"></a>Ažuriranja kvalitete

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| Naplata i određivanje cijene | 2209402 | Ispravljene su provjere valjanosti koje su sprječavale fakturiranje iznosa zadržavanja nakon potvrde ugovora o projektu. |
|   Upravljanje prilikama | 2227414 | Polja **Proizvod**, **Upiši-u** i **IsProductOverriden** kopiraju se u pojedinosti retka ponude i retka ugovora. |
| Naplata i određivanje cijene | 2338357 | Valutu u zapisa o uporabi materijala obvezno zadaje valuta projekta kada se odabere projekt. |
| Vrijeme i trošak | 2414777 | Mora se omogućiti otkazivanje odobrenja ako unos troška ili vremena ima više od jednog povezanog odobrenja za projekt. |
