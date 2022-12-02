---
title: Skupovi odobrenja
description: U ovom se članku objašnjava način rada sa skupovima odobrenja, zahtjevima i podskupovima tih operacija.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524907"
---
# <a name="approval-sets"></a>Skupovi odobrenja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Skupovi odobrenja grupiraju zahtjeve za odobrenja u manje podskupove operacija. Ovo grupiranje omogućuje da se odobrenja obrađuju po projektu, određenim redoslijedom i omogućuje ponovni pokušaj i sekvencioniranje. Grupiranje zahtjeva za odobrenje poboljšava pouzdanost i sljedivost obrade odobrenja za velike količine odobrenja.

Skupovi odobrenja pokazuju cjelokupno stanje obrade njihovih povezanih zapisa. Kada se zapis o odobrenju obrađuje s pomoću skupa odobrenja, zapis se pomiče iz **Poslano** u **Odobreno** i više nije povezan sa skupom odobrenja. Ako zapis ne uspije kad se pošalje na odobrenje, on ostaje u stanju **Poslan**, a skup odobrenja označava se kao neuspješan. Skup odobrenja zapisuje poruku o pogrešci neuspjeha.

## <a name="processing-approvals-and-approval-sets"></a>Obrada odobrenja i skupova odobrenja
Odobrenja koja su u redu čekanja za obradu vidljiva su u prikazu **Odobrenja za obradu**. Sustav asinkrono obrađuje sve unose više puta, uključujući ponovni pokušaj odobrenja ako prethodni pokušaji nisu uspjeli.

Polje **Vijek trajanja skupa odobrenja** bilježi broj preostalih pokušaja obrade skupa prije nego što se označi kao neuspješan.

Skupovi odobrenja obrađuju se kroz periodičku aktivaciju na temelju **toka oblaka** nazvanog **Project Service – Zakažite skupove odobrenja projekta u ponavljanju**. Nalazi se u **rješenju** naziva **Project operations**. 

Provjerite je li tok aktiviran dovršavanjem sljedećih koraka.

1. Kao administrator se prijavite na [flow.microsoft.com](https://powerautomate.microsoft.com).
2. U gornjem desnom kutu prijeđite na okruženje kojim se koristite za Dynamics 365 Project Operations.
3. Odaberite **Rješenja** za popis rješenja koja su instalirana u okruženju.
4. Na popisu rješenja odaberite **Project Operations**.
5. Promijenite filtar iz **Svi** u **Tok oblaka**.
6. Provjerite je li tok **Project Service – Zakažite skupove odobrenja projekta u ponavljanju** postavljen na **Uključeno**. Ako nije, odaberite tok, a zatim odaberite **Uključi**.
7. Provjerite odvija li se obrada svakih pet minuta pregledom popisa **Poslovi sustava** u području **Postavke** unutar Project Operations Dataverse okruženja.

## <a name="failed-approvals-and-approval-sets"></a>Neuspjela odobrenja i skupovi odobrenja
Prikaz **Neuspjela odobrenja** prikazuje sva odobrenja za koja je potrebna intervencija korisnika. Otvorite povezane zapisnike skupa odobrenja kako biste identificirali uzrok neuspjeha.
Odabir **Pokušaj ponovno** pridodaje broj vijeka trajanja odobrenja, vraća skup odobrenja natrag u stanje **Obrada u tijeku** i pokušava obraditi preostale zapise.

## <a name="configure-approval-sets"></a>Konfiguriranje skupova odobrenja

### <a name="enable-the-approval-sets-feature"></a>Omogućivanje značajke Skupovi odobrenja
Prije nego što omogućite značajku Skupovi odobrenja, utvrdite da u obradi trenutačno nema odobrenja. Nakon što se ova značajka omogući, više se ne može onemogućiti.

- Idite na stranicu **Parametri projekta** i odaberite **Kontrola značajke** > **Omogući nova odobrenja**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfiguriranje asinkronog praga 
Kada se stvaraju skupovi odobrenja, obrada se pomiče u pozadinu nakon što odabrani broj zapisa za odobrenje premaši naznačeni prag. Upotrijebite polje **Asinkroni prag** kako biste konfigurirali kada obradu odobrenja treba izvoditi sinkrono, a kada asinkrono. Odaberite jednu od sljedećih vrijednosti:

  - Nula: Svi se zahtjevi trebaju obrađivati asinkrono. 
  - Brojevi veći od nule: Odobrenja se obrađuju asinkrono samo kada prijavljeni broj odobrenja premašuje ovu vrijednost.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
