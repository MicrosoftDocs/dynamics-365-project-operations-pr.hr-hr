---
title: Skupovi odobrenja
description: U ovoj temi objašnjava se način rada sa skupovima odobrenja, zahtjevima i podskupovima tih operacija.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323227"
---
# <a name="approval-sets"></a>Skupovi odobrenja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Skupovi odobrenja grupiraju zahtjeve za odobrenja u manje podskupove operacija. Ovo grupiranje omogućuje da se odobrenja obrađuju po projektu, određenim redoslijedom i omogućuje ponovni pokušaj i sekvencioniranje. Grupiranje zahtjeva za odobrenje poboljšava pouzdanost i sljedivost obrade odobrenja za velike količine odobrenja.

Skupovi odobrenja pokazuju cjelokupno stanje obrade njihovih povezanih zapisa. Kada se zapis o odobrenju obrađuje s pomoću skupa odobrenja, zapis se pomiče iz **Poslano** u **Odobreno** i više nije povezan sa skupom odobrenja. Ako zapis ne uspije kad se pošalje na odobrenje, on ostaje u stanju **Poslan**, a skup odobrenja označava se kao neuspješan. Skup odobrenja zapisuje poruku o pogrešci neuspjeha.

## <a name="processing-approvals-and-approval-sets"></a>Obrada odobrenja i skupova odobrenja
Odobrenja koja su u redu čekanja za obradu vidljiva su u prikazu **Odobrenja za obradu**. Sustav asinkrono obrađuje sve unose više puta, uključujući ponovni pokušaj odobrenja ako prethodni pokušaji nisu uspjeli.

Polje **Vijek trajanja skupa odobrenja** bilježi broj preostalih pokušaja obrade skupa prije nego što se označi kao neuspješan.

## <a name="failed-approvals-and-approval-sets"></a>Neuspjela odobrenja i skupovi odobrenja
Prikaz **Neuspjela odobrenja** prikazuje sva odobrenja za koja je potrebna intervencija korisnika. Otvorite povezane zapisnike skupa odobrenja kako biste identificirali uzrok neuspjeha.
Odabir **Pokušaj ponovno** pridodaje broj vijeka trajanja odobrenja, vraća skup odobrenja natrag u stanje **Obrada u tijeku** i pokušava obraditi preostale zapise.

## <a name="configure-approval-sets"></a>Konfiguriranje skupova odobrenja

### <a name="enable-the-approval-sets-feature"></a>Omogućivanje značajke Skupovi odobrenja
Prije nego što omogućite značajku Skupovi odobrenja, utvrdite da u obradi trenutačno nema odobrenja.

- Idite na stranicu **Parametri projekta** i odaberite **Kontrola značajke** > **Omogući nova odobrenja**.

### <a name="turn-off-the-approval-sets-feature"></a>Isključivanje značajke Skupovi odobrenja
Prije nego što isključite značajku Skupovi odobrenja, utvrdite da u obradi trenutačno nema odobrenja.

- Idite na stranicu **Parametri projekta** i odaberite **Kontrola značajke** > **Onemogući nova odobrenja**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfiguriranje asinkronog praga 
Kada se stvaraju skupovi odobrenja, obrada se pomiče u pozadinu nakon što odabrani broj zapisa za odobrenje premaši naznačeni prag. Upotrijebite polje **Asinkroni prag** kako biste konfigurirali kada obradu odobrenja treba izvoditi sinkrono, a kada asinkrono. Odaberite jednu od sljedećih vrijednosti:

  - Nula: Svi se zahtjevi trebaju obrađivati asinkrono. 
  - Brojevi veći od nule: Odobrenja se obrađuju asinkrono samo kada prijavljeni broj odobrenja premašuje ovu vrijednost.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
