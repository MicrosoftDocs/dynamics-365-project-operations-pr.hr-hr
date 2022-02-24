---
title: Opoziv odobrenih unosa vremena ili troškova
description: Ova tema pruža informacije o tome kako opozvati prethodno odobreno vrijeme ili transakciju troškova.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f9bb25ac9ef7b400063c5f958311e475de6f6506
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147824"
---
# <a name="recall-approved-time-or-expense-entries"></a>Opoziv odobrenih unosa vremena ili troškova

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Član projektnog tima ili druga osoba koja pošalje Unos vremena ili troškova može opozvati taj Unos vremena ili troškova nakon što se odobri. Postupak opoziva odobrenog unosa vremena ili troškova obuhvaća dva koraka:

1. Pošiljatelj zahtijeva opoziv.
2. Odobravatelj odobrava opoziv.

## <a name="request-a-recall"></a>Zahtjev za opoziv

Poduzmite ove korake da biste zatražili opoziv odobrenog unosa vremena ili troškova.

1. Za vremenske unose idite na **Projekti** \> **Moj posao** \> **Unos vremena**.

    –ili–

    Za unose troškova idite na **Projekti** \> **Moj posao** \> **Troškovi**.

2. Za vremenske unose odaberite sve vremenske unose za određenu kombinaciju projekta i zadatka. Ili u rešetki odaberite pojedinačne ćelije za vrijeme na određeni datum za određeni projekt.

    –ili–

    Za unose troškova odaberite redak za unos troškova za opoziv.

3. Odaberite **Opozovi**. Prikazat će se dijaloški okvir za potvrdu. Ako su odabrani unosi vremena ili troškova već odobreni, od vas će se zatražiti da unesete razlog za opoziv.
4. Unesite razlog za opoziv, a zatim odaberite **U redu** da biste potvrdili operaciju. Sustav šalje osobi koja je odobrila unose zahtjev za odobravanje opoziva.

> [!NOTE]
> Iako se odobreni unosi vremena ili troškova mogu opozvati, ako su odobreno vrijeme ili trošak već fakturirani klijentu, nije moguće stvoriti zahtjev za opoziv. Korisnik koji pokuša stvoriti zahtjev za opoziv primit će poruku u kojoj se navodi da vrijeme ili trošak nije moguće opozvati jer su već fakturirani.

## <a name="approve-or-reject-a-recall-request"></a>Odobravanje ili odbacivanje zahtjeva za opoziv

Poduzmite ove korake da biste odobrili ili odbacili zahtjev za opoziv.

1. Idi na **Projekti** \> **Moj posao** \> **Odobrenja**.
2. Na stranici popisa **Odobrenja** promijenite prikaz u **Zahtjevi za opoziv za odobrenje**. Prikazat će se popis poslanih zahtjeva za opoziv.
3. Odaberite jedan ili više unosa, a zatim odaberite **Odobri** ili **Odbaci**.
4. Ako ste odabrali **Odobri**, primit ćete poruku upozorenja koja objašnjava učinak odobrenja. Odaberite **U redu** da biste potvrdili operaciju. Zahtjev za opoziv odobren je.

    –ili–

    Ako ste odabrali **Odbaci**, zahtjev za opoziv odbacuje se.

> [!NOTE]
> Kao kada se zatraži opoziv, kada se opoziv odobri, sustav provjerava postoje li aktivnosti fakturiranja u vezi s unosima vremena ili troškova. Ako je unos već fakturiran ili je naveden u skici fakture, odobravatelj će primiti poruku o pogrešci u kojoj se navodi da se vrijeme ili trošak ne mogu odobriti za opoziv jer su već fakturirani.

## <a name="impact-of-a-recall-request"></a>Učinak zahtjeva za opoziv

Kada se odobrenje opozove, postoji operativni i financijski učinak.

### <a name="operational-impact"></a>Operativni učinak

Ako se zahtjev za opoziv odobri, zapis odobravanja dobiva oznaku **Odbačeno**. Status unosa mijenja se u **Vraćeno** ili **Odbačeno**, ovisno o tome je li riječ o unosu vremena ili troška.

Član projektnog tima može pregledati, urediti i zatim ponovno poslati unose ili ih u cijelosti izbrisati.

Ako se zahtjev za opoziv odbaci, status unosa ostaje **Odobreno**, a član projektnog tima ili odobravatelj za projekt ne može uređivati unos.

### <a name="financial-impact"></a>Financijski učinak

Ako se zahtjev za opoziv odobri, odgovarajući stvarni podaci za troškove i prodaju ažuriraju se na sljedeći način:

- Polje **Status prilagodbe** ažurira se na **Prilagođeno**.
- Polje **Status naplate** ažurira se na **Prilagođeno**.

Zatim, izrađuju se unosi preokreta u tablici Stvarne vrijednosti. Da biste izradili unose preokreta, sustav kopira vrijednosti polja iz izvornih stvarnih vrijednosti. Jedine vrijednosti koje se ne kopiraju su vrijednosti količine. Te su vrijednosti umjesto toga preokreću. Preokrenute stvarne vrijednosti izrađuju se za stvarne vrijednosti **Troškova** i **Nenaplaćene prodaje**. Polje **Status prilagodbe** u poništenim stvarnim podacima postava se na **Nije moguće prilagoditi**, a polje **Status naplate** postavlja se na **Otkazano**. Zbog tih promjena zabilježena potrošnja i zaostatak prihoda na projektu više neće pravdati iznose koje ti stvarni podaci predstavljaju.

Ako se zahtjev za opoziv odbaci, ne postoji financijski učinak na projekt.

## <a name="changes-to-time-entry-records"></a>Promjene zapisa unosa vremena

Sljedeća ilustracija prikazuje promjene do kojih dolazi prilikom opoziva odobrenih vremenskih unosa.

![Prijelazi stanja unosa vremena](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Promjene zapisa unosa troškova

Sljedeća ilustracija prikazuje promjene do kojih dolazi prilikom opoziva odobrenih unosa troškova.

![Prijelazi stanja unosa troškova](media/ExpenseEntryStateTransitions.png)
