---
title: Skupovi odobrenja
description: U ovoj temi nalaze se informacije o skupu odobrenja, zahtjevima i podskupovima tih operacija.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116862"
---
# <a name="approval-sets"></a>Skupovi odobrenja

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Skupovi odobrenja grupiraju zahtjeve za odobrenja u manje podskupove operacija. Ovo grupiranje omogućuje obradu odobrenja redoslijedom po projektu i omogućuje ponovni pokušaj i redoslijed. Grupiranje poboljšava pouzdanost i sljedivost obrade odobrenja za velike količine odobrenja.

Skupovi odobrenja pokazuju cjelokupno stanje obrade njihovih povezanih zapisa. Kada se zapis o odobrenju obrađuje s pomoću skupa odobrenja, zapis se pomiče iz stanja **Poslan** u stanje **Odobren** i prekida mu se veza iz skupa odobrenja. Ako zapis ne uspije kad se pošalje na odobrenje, on ostaje u stanju **Poslan**, a skup odobrenja označava se kao neuspješan. Skup odobrenja zapisuje poruku o pogrešci neuspjeha.

## <a name="processing-approvals-and-approval-sets"></a>Obrada odobrenja i skupova odobrenja
Odobrenja koja su u redu čekanja za obradu vidljiva su u prikazu **Odobrenja za obradu**. Sustav pokušava sinkronizirano više puta obraditi sve unose, uključujući ponovni pokušaj odobrenja ako prethodni pokušaji nisu uspjeli.

Polje **Vijek trajanja skupa odobrenja** bilježi broj preostalih pokušaja obrade skupa prije nego što se označi kao neuspješan.

## <a name="failed-approvals-and-approval-sets"></a>Neuspjela odobrenja i skupovi odobrenja
Prikaz **Neuspjela odobrenja** navodi sva odobrenja koja zahtijevaju intervenciju korisnika. Otvorite povezane zapisnike skupa odobrenja kako biste identificirali uzrok neuspjeha.
Odabir **Pokušaj ponovno** pridodaje broj vijeka trajanja odobrenja, vraća skup odobrenja natrag u stanje **Obrada u tijeku** i pokušava obraditi preostale zapise.

## <a name="configure-approval-sets"></a>Konfiguriranje skupova odobrenja

###  <a name="enable-the-approval-sets-feature"></a>Omogućivanje značajke Skupovi odobrenja
Prije nego što omogućite značajku Skupovi odobrenja, utvrdite da u obradi trenutačno nema odobrenja.

- Idite na stranicu **Parametri projekta** i odaberite **Kontrola značajke** > **Omogući nova odobrenja**.

### <a name="turn-off-the-approval-sets-feature"></a>Isključivanje značajke Skupovi odobrenja
Prije nego što isključite značajku Skupovi odobrenja, utvrdite da u obradi trenutačno nema odobrenja.

- Idite na stranicu **Parametri projekta** i odaberite **Kontrola značajke** > **Onemogući nova odobrenja**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfiguriranje asinkronog praga 
Kada se stvaraju skupovi odobrenja, obrada se pomiče u pozadinu nakon što odabrani broj zapisa za odobrenje premaši naznačeni prag. Upotrijebite polje **Asinkroni prag** kako biste konfigurirali kada obradu odobrenja treba izvoditi sinkrono, a kada asinkrono.
Valjane vrijednosti su:

  - Nula: Svi se zahtjevi trebaju obrađivati asinkrono. 
  - Brojevi veći od nule: Odobrenja se obrađuju asinkrono samo kada prijavljeni broj odobrenja premašuje ovu vrijednost.

[!INCLUDE[footer-include](../includes/footer-banner.md)]