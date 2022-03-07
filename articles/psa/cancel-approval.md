---
title: Poništi prethodno odobrene unose vremena i troškova
description: Ova tema pruža informacije o tome kako poništiti odobreno vrijeme projekta i transakciju troškova.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 09b85ea302ac46171afbd531a551aa5fbf5492a3644cba3448be03009840228c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987427"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Poništi prethodno odobrene unose vremena ili troškova

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

U posljednjoj verziji sustava Dynamics 365 Project Service Automation, odobravatelji mogu poništiti unose vremena ili troškova koje su prethodno odobrili.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Poništi prethodno odobreni unos vremena ili troškova

Slijedite ove korake da biste poništili unos vremena ili troškova koji ste prethodno odobrili.

1. Idi na **Projekti** \> **Moj posao** \> **Odobrenja**.
2. Na stranici popisa **Odobrenja** promijenite prikaz u **Moja prošla odobrenja**. Prikazuje se popis unosa vremena i troškova koje ste prethodno odobrili.
3. Odaberite jednu ili više unosa, a zatim odaberite **Otkaži odobrenje**. Primit ćete poruku upozorenja.
4. Odaberite **U redu** da biste poništili odobrenje.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Razumijevanje učinka poništavanja odobrenja za unos vremena ili troškova

Kada se odobrenje poništi, učinak je i operativni i financijski.

### <a name="operational-impact"></a>Operativni učinak

S operativne strane, kada se odobrenje poništi, status zapisa vraća se na **Skica**, a odobrenje se više ne pojavljuje u prikazu **Moja prošla odobrenja**. Umjesto toga, poništeno odobrenje pojavljuje se u prikazu **Unosi vremena za odobrenje** ili **Unosi troškova za odobrenje**, ovisno o tome je li to bio unos vremena ili izdatka. Osim toga, status povezanog unosa vremena ili unosa troškova mijenja se u **Poslano**, tako da je povezani unos u skladu s odobrenjima koja imaju status **Skica**.

Kao odobravatelj, možete urediti neka polja odobrenja koja ima status **Skica**. Ta polja uključuju **Vrsta naplate** i **Naplativi sati za unose vremena**. Nakon što izvršite promjene, ponovno možete odobriti zapis. Alternativno, možete odbiti unos. Ako odbijete odobrenje unosa vremena, status unosa mijenja se u **Vraćeno**. Ako odbijete odobrenje unosa troškova, status se mijenja u **Odbijeno**. S funkcionalne strane, i vraćeni i odbijeni unosi ponašaju se isto kao i unos koji ima status **Skica**. Član tima projekta može izvršiti bilo kakve potrebne promjene unosa, a zatim ga ponovno poslati na odobrenje ili u cijelosti izbrisati unos.

### <a name="financial-impact"></a>Financijski učinak

Projekt je također zahvaćen financijski kada se poništava odobrenje. Najprije, odgovarajuće stvarne vrijednosti za troškove i prodaju ažuriraju se na sljedeći način:

- Status prilagodbe postavlja se na **Prilagođeno**.
- Status naplate postavlja se na **Poništeno**.

Zatim, izrađuju se unosi preokreta u tablici Stvarne vrijednosti. Da biste izradili unose preokreta, sustav kopira vrijednosti polja iz izvornih stvarnih vrijednosti. Jedine vrijednosti koje se ne kopiraju su vrijednosti količine. Te su vrijednosti umjesto toga preokreću. Preokrenute stvarne vrijednosti izrađuju se za stvarne vrijednosti **Troškova** i **Nenaplaćene prodaje**. Polje **Status prilagodbe** na preokrenutim stvarnim vrijednostima postavlja se na **Nepodesivo**, a status naplate postavlja se na **Poništeno**.

Nakon što su te promjene izvršene, iznos koji je zapisan kao potrošen na projektu i zaostatak prihoda na projektu duže će pravdati iznose koje te stvarne vrijednosti predstavljaju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]