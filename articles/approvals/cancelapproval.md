---
title: Otkazivanje odobrenja za prethodno odobrene unose
description: U ovom se članku objašnjava kako voditelj projekta može otkazati odobrenje prethodno odobrenih unosa vremena, troškova ili upotrebe materijala.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930447"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Otkazivanje odobrenja za prethodno odobrene unose

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Voditelj projekta ili odobravatelj koji je prethodno odobrio unose vremena, troškova ili upotrebe materijala može otkazati svoje odobrenje tih unosa. 

Slijedite ove korake da biste otkazali odobrenje ranije odobrenih unosa vremena, troškova ili upotrebe materijala.

1. Idi na **Projekti** \> **Moj posao** \> **Odobrenja**.
2. Stranica s popisom **Odobrenja** prikazuje sve unose vremena koji čekaju odobrenje. Prikaz prebacite na **Moja prošla odobrenja**.
3. Odaberite odobrenja vremena, troškova ili materijala koja želite otkazati. Zatim u oknu radnji odaberite **Otkaži odobrenje**.
4. U okviru potvrdne poruke koja se pojavi odaberite **U redu** da biste potvrdili radnju

> [!IMPORTANT]
> Odobrenje prethodno odobrenog unosa vremena, troška i upotrebe materijala koji je već fakturiran kupcu ne možete poništiti. Ako pokušate, dobit ćete poruku da se odobrenje ne može poništiti jer je već fakturirano. U tom slučaju možete poništiti odobrenje samo ako se korektivna faktura koristi za izdavanje punog kredita ili povrata kupcu na originalnoj fakturi.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Utjecaj otkazivanja odobrenja prethodno odobrenog unosa

Kada se odobrenje poništi, učinak je i operativni i financijski.

### <a name="operational-impact"></a>Operativni učinak

Ako se odobrenje unosa poništeni, zapis odobrenja označit će se s **Poslano**. Status unosa mijenja se u **Poslano**. U ovoj fazi, član projektnog tima može opozvati unos bez podnošenja zahtjeva za opoziv.

Odobravatelj može promijeniti vrijednosti **Naplativa količina** i **Vrsta naplate**, a zatim još jednom odobriti unos.

### <a name="financial-impact"></a>Financijski učinak

Ako se odobrenje nekog unosa otkaže, odgovarajući stvarni podaci za troškove i prodaju ažuriraju se na sljedeći način:

- Polje **Status prilagodbe** ažurira se na **Prilagođeno**.
- Polje **Status naplate** ažurira se na **Prilagođeno**.

Zatim, izrađuju se unosi preokreta u tablici Stvarne vrijednosti. Da biste izradili unose preokreta, sustav kopira vrijednosti polja iz izvornih stvarnih vrijednosti. Jedine vrijednosti koje se ne kopiraju su vrijednosti količine. Te su vrijednosti umjesto toga preokreću. Preokrenute stvarne vrijednosti izrađuju se za stvarne vrijednosti **Troškova** i **Nenaplaćene prodaje**. Polje **Status prilagodbe** u poništenim stvarnim podacima postava se na **Nije moguće prilagoditi**, a polje **Status naplate** postavlja se na **Otkazano**. Zbog tih promjena zabilježena potrošnja i zaostatak prihoda na projektu više neće pravdati iznose koje ti stvarni podaci predstavljaju.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
