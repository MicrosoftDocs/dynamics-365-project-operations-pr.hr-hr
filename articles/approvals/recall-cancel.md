---
title: Opoziv prethodno odobrenih unosa
description: U ovom članku objašnjeno je kako član projektnog tima može zatražiti opoziv prethodno podnesenih i odobrenih zapisa o vremenu, trošku i utrošenom materijalu te kako voditelj projekta može odobriti ili odbiti zahtjeve za opoziv.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930355"
---
# <a name="recall-previously-approved-entries"></a>Opoziv prethodno odobrenih unosa

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Član projektnog tima koji podnese unos vremena, troška ili utrošenog materijala može u potpunosti opozvati taj unos nakon što je on odobren. Postupak opoziva sastoji se od dva glavna koraka:

1. Pošiljatelj zahtijeva opoziv.
2. Odobritelj odobrava zahtjev za opoziv.

## <a name="request-a-recall"></a>Zahtjev za opoziv

Pratite sljedeće korake kako biste zatražili opoziv odobrenih unosa vremena, troška ili utrošenog materijala.

1. Slijedite jedan od ovih koraka, ovisno o vrsti unosa koji želite opozvati:

    - Za vremenske unose idite na **Projekti** \> **Moj posao** \> **Unos vremena** i odaberite sve unose vremena za određenu kombinaciju projekta i zadatka. Ili u rešetki odaberite pojedinačne ćelije za vrijeme na određeni datum za određeni projekt.
    - Za unose troškova idite na **Projekti** \> **Moj posao** \> **Troškovi** i odaberite redak unosa troška koji želite opozvati.
    - Za unose upotrebe materijala idite na **Projekti** \> **Moj posao** \> **Zapisnik o utrošenom materijalu** i odaberite unos utrošenog materijala koji želite opozvati.

2. Odaberite **Storniraj**. Prikazat će se dijaloški okvir za potvrdu. Ako su odabrani unosi vremena, troška ili utrošenog materijala već odobreni, prikazat će se odzivnik za unos razloga opoziva.
3. Unesite razlog za opoziv, a zatim odaberite **U redu** da biste potvrdili operaciju. Sustav šalje osobi koja je odobrila unose zahtjev za odobravanje opoziva.

> [!IMPORTANT]
> Zahtjev za opoziv ne možete stvoriti za odobreni unos vremena, troška ili utrošenog materijala koji je već fakturiran klijentu. Ako to pokušate učiniti, dobit ćete poruku u kojoj je navedeno da se unos vremena, troška ili utrošenog materijala ne može poništiti jer je već fakturiran. U tom slučaju opoziv unosa možete zatražiti samo ako se korektivna faktura upotrebljava za izdavanje punog kredita ili povrata kupcu na originalnoj fakturi.

## <a name="approve-or-reject-a-recall-request"></a>Odobravanje ili odbacivanje zahtjeva za opoziv

Poduzmite ove korake da biste odobrili ili odbacili zahtjev za opoziv.

1. Idi na **Projekti** \> **Moj posao** \> **Odobrenja**.
2. Na stranici popisa **Odobrenja** promijenite prikaz u **Zahtjevi za opoziv za odobrenje**. Prikazat će se popis poslanih zahtjeva za opoziv.
3. Odaberite jedan ili više unosa, a zatim odaberite **Odobri** ili **Odbaci**.
4. Ako ste odabrali **Odobri**, primit ćete poruku upozorenja koja objašnjava učinak odobrenja. Odaberite **U redu** da biste potvrdili operaciju. Zahtjev za opoziv odobren je.

    –ili–

    Ako ste odabrali **Odbaci**, zahtjev za opoziv odbacuje se.

> [!IMPORTANT]
> Kad se opoziv odobri, kao i kada se zatraži, sustav će provjeriti sve aktivnosti fakturiranja za unose vremena, troška ili utrošenog materijala. Ako je unos već fakturiran ili je naveden u skici fakture, odobravatelj će dobiti poruku o pogrešci u kojoj se navodi da se ne može odobriti opoziv vremena ili troška jer su već fakturirani. U tom slučaju odobravatelj može odobriti opoziv samo ako se korektivna faktura upotrebljava za izdavanje punog kredita ili povrata kupcu na originalnoj fakturi.

## <a name="impact-of-a-recall-request"></a>Učinak zahtjeva za opoziv

Kada se odobrenje opozove, postoji operativni i financijski učinak.

### <a name="operational-impact"></a>Operativni učinak

Ako se zahtjev za opoziv odobri, zapis odobravanja dobiva oznaku **Odbačeno**. Status unosa mijenja se u **Vraćeno** ili **Odbačeno**, ovisno o tome je li riječ o unosu vremena, troška ili materijala.

Član projektnog tima može pregledati, urediti i zatim ponovno poslati unose ili ih u cijelosti izbrisati.

Ako se zahtjev za opoziv odbaci, status unosa ostaje **Odobreno**, a član projektnog tima ili odobravatelj za projekt ne može uređivati unos.

### <a name="financial-impact"></a>Financijski učinak

Ako se zahtjev za opoziv odobri, odgovarajući stvarni podaci za troškove i prodaju ažuriraju se na sljedeći način:

- Polje **Status prilagodbe** ažurira se na **Prilagođeno**.
- Polje **Status naplate** ažurira se na **Prilagođeno**.

Zatim, izrađuju se unosi preokreta u tablici Stvarne vrijednosti. Da biste izradili unose preokreta, sustav kopira vrijednosti polja iz izvornih stvarnih vrijednosti. Jedine vrijednosti koje se ne kopiraju su vrijednosti količine. Te su vrijednosti umjesto toga preokreću. Preokrenute stvarne vrijednosti izrađuju se za stvarne vrijednosti **Troškova** i **Nenaplaćene prodaje**. Polje **Status prilagodbe** u poništenim stvarnim podacima postava se na **Nije moguće prilagoditi**, a polje **Status naplate** postavlja se na **Otkazano**. Zbog tih promjena zabilježena potrošnja i zaostatak prihoda na projektu više neće pravdati iznose koje ti stvarni podaci predstavljaju.

Ako se zahtjev za opoziv odbaci, ne postoji financijski učinak na projekt.

## <a name="changes-to-time-entry-records"></a>Promjene zapisa unosa vremena

Na sljedećoj ilustraciji prikazane su promjene do kojih dolazi pri opozivu odobrenih unosa vremena i odgovarajućih zapisa odobrenja.

![Prijelazi stanja unosa vremena.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Promjene zapisa unosa troška i utrošenog materijala

Na sljedećoj ilustraciji prikazane su promjene do kojih dolazi pri opozivu odobrenih unosa troška i utrošenog materijala te odgovarajućih zapisa odobrenja.

![Prijelazi stanja unosa troška.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
