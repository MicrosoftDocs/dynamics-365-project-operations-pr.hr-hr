---
title: Otkazivanje odobrenja prethodno odobrenih stavki
description: Ova tema objašnjava kako voditelj projekta može otkazati odobravanje prethodno odobrenih stavki vremena, troškova ili korištenja materijala.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584771"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Otkazivanje odobrenja prethodno odobrenih stavki

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Voditelj projekta ili odobravatelj koji je prethodno odobrio stavke vremena, troška ili korištenja materijala može otkazati odobrenje tih stavki. 

Slijedite ove korake da biste poništili odobravanje prethodno odobrenog vremena, troška ili stavke korištenja materijala.

1. Idi na **Projekti** \> **Moj posao** \> **Odobrenja**.
2. Stranica popisa Odobrenja **prikazuje** sve stavke vremena koje čekaju odobrenje. Promijenite prikaz **u Moja prošla odobrenja**.
3. Odaberite vrijeme, trošak ili materijalna odobrenja koja želite otkazati. Zatim u oknu akcije odaberite **Odustani od odobravanja**.
4. U okviru s potvrdnom porukom koji će se pojaviti odaberite **U redu** da biste potvrdili operaciju.

> [!IMPORTANT]
> Ne možete otkazati odobravanje prethodno odobrene stavke vremena, troška i korištenja materijala koja je već fakturirana kupcu. Ako pokušate, primit ćete poruku u kojoj se navodi da se odobrenje ne može otkazati jer je već fakturirano. U tom slučaju odobrenje možete otkazati samo ako se korektivna faktura koristi za izdavanje punog kredita ili povrata novca kupcu na izvornoj fakturi.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Utjecaj otkazivanja odobrenja prethodno odobrenog unosa

Kada se odobrenje poništi, učinak je i operativni i financijski.

### <a name="operational-impact"></a>Operativni učinak

Ako je odobrenje stavke otkazano, zapis o odobrenju označen je kao **Poslano**. Status unosa mijenja **se u Poslano**. U ovoj fazi član projektnog tima može opozvati unos bez podnošenja zahtjeva za opoziv.

Odobravatelj može promijeniti vrijednosti količine **za naplatu** i **vrste** naplate, a zatim još jednom odobriti stavku.

### <a name="financial-impact"></a>Financijski učinak

Ako je odobrenje stavke otkazano, odgovarajuće stvarne vrijednosti troškova i prodaje obnavljaju se na sljedeći način:

- Polje **Status prilagodbe** ažurira se na **Prilagođeno**.
- Polje **Status naplate** ažurira se na **Prilagođeno**.

Zatim, izrađuju se unosi preokreta u tablici Stvarne vrijednosti. Da biste izradili unose preokreta, sustav kopira vrijednosti polja iz izvornih stvarnih vrijednosti. Jedine vrijednosti koje se ne kopiraju su vrijednosti količine. Te su vrijednosti umjesto toga preokreću. Preokrenute stvarne vrijednosti izrađuju se za stvarne vrijednosti **Troškova** i **Nenaplaćene prodaje**. Polje **Status prilagodbe** u poništenim stvarnim podacima postava se na **Nije moguće prilagoditi**, a polje **Status naplate** postavlja se na **Otkazano**. Zbog tih promjena zabilježena potrošnja i zaostatak prihoda na projektu više neće pravdati iznose koje ti stvarni podaci predstavljaju.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
