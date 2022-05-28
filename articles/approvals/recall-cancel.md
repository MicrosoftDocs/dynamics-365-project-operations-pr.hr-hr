---
title: Opoziv prethodno odobrenih unosa
description: Ovaj tema objašnjava kako član projektnog tima može zatražiti opoziv prethodno dostavljenih i odobrenih zapisa o vremenu, troškovima i korištenju materijala te kako voditelj projekta može odobriti ili odbiti zahtjeve za opoziv.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586565"
---
# <a name="recall-previously-approved-entries"></a>Opoziv prethodno odobrenih unosa

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Član projektnog tima koji pošalje unos vremena, troškova ili korištenja materijala može se sjetiti tog unosa nakon što je odobren. Postupak opoziva ima dva glavna koraka:

1. Pošiljatelj zahtijeva opoziv.
2. Odobravatelj odobrava zahtjev za opoziv.

## <a name="request-a-recall"></a>Zahtjev za opoziv

Slijedite ove korake da biste zatražili opoziv odobrenih stavki vremena, troškova ili upotrebe materijala.

1. Slijedite jedan od ovih koraka, ovisno o vrsti unosa koji želite opozvati:

    - Stavke vremena potražite u odjeljku **Projicira** \> **stavku** mog radnog \>**vremena** i odaberite sve vremenske unose za određenu kombinaciju projekta i zadatka. Ili u rešetki odaberite pojedinačne ćelije za vrijeme na određeni datum za određeni projekt.
    - Stavke troškova potražite u odjeljku **Projekti** \> **moji troškovi** rada \>**i** odaberite redak za stavku troškova za opoziv.
    - Stavke upotrebe materijala potražite u odjeljku **Projekti** \> **moj evidencija** korištenja radnog \>**materijala** i odaberite redak za stavku korištenja materijala koju želite opozvati.

2. Odaberite **Storniraj**. Prikazat će se dijaloški okvir za potvrdu. Ako su odabrane stavke vremena, troška ili upotrebe materijala već odobrene, od vas će se zatražiti da unesete razlog za opoziv.
3. Unesite razlog za opoziv, a zatim odaberite **U redu** da biste potvrdili operaciju. Sustav šalje osobi koja je odobrila unose zahtjev za odobravanje opoziva.

> [!IMPORTANT]
> Ne možete kreirati zahtjev za opoziv za odobreno vrijeme, trošak ili stavku upotrebe materijala koja je već fakturirana kupcu. Ako pokušate, primit ćete poruku u kojoj se navodi da se vrijeme, trošak ili unos upotrebe materijala ne mogu opozvati jer je već fakturirana. U tom slučaju možete zatražiti opoziv stavke samo ako se korektivni račun koristi za izdavanje punog kredita ili povrata novca kupcu na izvornom računu.

## <a name="approve-or-reject-a-recall-request"></a>Odobravanje ili odbacivanje zahtjeva za opoziv

Poduzmite ove korake da biste odobrili ili odbacili zahtjev za opoziv.

1. Idi na **Projekti** \> **Moj posao** \> **Odobrenja**.
2. Na stranici popisa **Odobrenja** promijenite prikaz u **Zahtjevi za opoziv za odobrenje**. Prikazat će se popis poslanih zahtjeva za opoziv.
3. Odaberite jedan ili više unosa, a zatim odaberite **Odobri** ili **Odbaci**.
4. Ako ste odabrali **Odobri**, primit ćete poruku upozorenja koja objašnjava učinak odobrenja. Odaberite **U redu** da biste potvrdili operaciju. Zahtjev za opoziv odobren je.

    –ili–

    Ako ste odabrali **Odbaci**, zahtjev za opoziv odbacuje se.

> [!IMPORTANT]
> Kada je opoziv odobren, baš kao i kada se zatraži, sustav provjerava ima li aktivnosti fakturiranja u vezi s vremenom, troškovima ili unosima u upotrebi materijala. Ako je stavka već fakturirana ili se nalazi na skici fakture, odobravatelj prima poruku o pogrešci u kojoj se navodi da se vrijeme ili trošak ne mogu odobriti za opoziv jer su već fakturirani. U tom slučaju odobravatelj može odobriti opoziv samo ako se za izdavanje punog kredita ili povrata novca kupcu na izvornom računu koristi korektivni račun.

## <a name="impact-of-a-recall-request"></a>Učinak zahtjeva za opoziv

Kada se odobrenje opozove, postoji operativni i financijski učinak.

### <a name="operational-impact"></a>Operativni učinak

Ako se zahtjev za opoziv odobri, zapis odobravanja dobiva oznaku **Odbačeno**. Status stavke mijenja **se u Vraćeno** ili **Odbijeno**, ovisno o tome radi li se o vremenskoj stavci ili stavci troškova ili materijalne upotrebe.

Član projektnog tima može pregledavati unose, uređivati, a zatim ponovno slati unose ili u potpunosti izbrisati unose.

Ako se zahtjev za opoziv odbaci, status unosa ostaje **Odobreno**, a član projektnog tima ili odobravatelj za projekt ne može uređivati unos.

### <a name="financial-impact"></a>Financijski učinak

Ako se zahtjev za opoziv odobri, odgovarajući stvarni podaci za troškove i prodaju ažuriraju se na sljedeći način:

- Polje **Status prilagodbe** ažurira se na **Prilagođeno**.
- Polje **Status naplate** ažurira se na **Prilagođeno**.

Zatim, izrađuju se unosi preokreta u tablici Stvarne vrijednosti. Da biste izradili unose preokreta, sustav kopira vrijednosti polja iz izvornih stvarnih vrijednosti. Jedine vrijednosti koje se ne kopiraju su vrijednosti količine. Te su vrijednosti umjesto toga preokreću. Preokrenute stvarne vrijednosti izrađuju se za stvarne vrijednosti **Troškova** i **Nenaplaćene prodaje**. Polje **Status prilagodbe** u poništenim stvarnim podacima postava se na **Nije moguće prilagoditi**, a polje **Status naplate** postavlja se na **Otkazano**. Zbog tih promjena zabilježena potrošnja i zaostatak prihoda na projektu više neće pravdati iznose koje ti stvarni podaci predstavljaju.

Ako se zahtjev za opoziv odbaci, ne postoji financijski učinak na projekt.

## <a name="changes-to-time-entry-records"></a>Promjene zapisa unosa vremena

Sljedeća ilustracija prikazuje promjene koje se događaju za odobrene stavke vremena i odgovarajuće zapise odobravanja prilikom opoziva.

![Prijelazi stanja unosa vremena.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Promjene zapisa stavki troškova i korištenja materijala

Sljedeća ilustracija prikazuje promjene koje se događaju za odobrene stavke troškova i korištenja materijala te odgovarajuće zapise odobravanja prilikom opoziva.

![Prijelazi države unosa troškova.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
