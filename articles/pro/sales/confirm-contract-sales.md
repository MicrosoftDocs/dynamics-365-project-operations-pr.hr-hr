---
title: Potvrda ugovora o projektu
description: U ovoj temi nalaze se informacije o načinu potvrde ugovora u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128274"
---
# <a name="confirm-a-project-contract"></a>Potvrda ugovora o projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Ugovor o projektu u aplikaciji Dynamics 365 Project Operations može biti aktivan s razlogom **Potvrđeno** ili zatvoren s razlogom **Izgubljeno**. Kada potvrdite ugovor o projektu, status se ažurira iz **Nacrt** u **Aktivan**, a razlog statusa je **Potvrđeno**. Aktivni ili zatvoreni ugovor ne može se uređivati ili ponovno otvarati. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Financijski učinak potvrde ugovora o projektu

Nakon potvrde ugovora o projektu, aplikacija će preračunati troškove storniranjem starijih stvarnih troškova i stvaranjem novih. Novi stvarni podaci o trošku zatim se obrađuju na temelju načina naplate retka ugovora povezanog projekta. Ako se stvarni podaci o troškovima odnose na redak ugovora za vrijeme i materijal, aplikacija automatski ponovno stvara odgovarajuće nenaplaćene stvarne podatke prodaje. Ako se stvarni podaci o troškovima odnose na redak ugovora s fiksnom cijenom, aplikacija zaustavlja ponovnu obradu stvarnih podataka o troškovima.

Ograničenja koja se ne smiju prekoračiti, postavljanje naplativosti te utvrđivanje cijena i troškova na stvarnim podacima procjenjuju se, a zatim ažuriraju kao dio postupka potvrde.

## <a name="close-a-project-contract-as-lost"></a>Zatvaranje ugovora o projektu kao izgubljenog

Kada ugovor o projektu zatvorite kao izgubljen, status ugovora ažurira se na **Zatvoreno** a razlog statusa je **Izgubljeno**. Ugovor o projektu postaje samo za čitanje. Dijaloški okvir za potvrdu osiguran je prije dovršetka promjena jer ne možete ponovo otvoriti zatvoreni ugovor o projektu.

Ako se ugovor o projektu koji je zatvoren kao izgubljen u svojim redcima poziva na projekt i taj se projekt označava kao zatvoren. Sve se rezervacije resursa od tog dana nadalje otkazuju. Svi stvarni podaci nenaplaćene prodaje iz ugovora o projektu koji još nisu na računu, stornirat će se.

> [!NOTE]
> Zatvaranje ugovora o projektu kao izgubljenog u aplikaciji Dynamics 365 Project Operations, neće utjecati na taj status povezane prilike. Prilika će ostati otvorena i mora se ručno zatvoriti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]