---
title: Faktura za povremena plaćanja ili plaćanje unaprijed
description: U ovom se članku navode informacije o fakturiranju akontacije ili predujma u operacijama projekta.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 044186d5c7759866dec3883103acec19cb571c11
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914439"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Faktura za povremena plaćanja ili plaćanje unaprijed

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations podržava ugovore koji se temelje na akontacijama. Na ugovor o projektu možete zabilježiti raspored akontacija ili jednokratnih predujmova. Međutim, bilježenje na razini ugovora o projektu ne osigurava odmah uporabu akontacije ili predujma. Kako biste upotrebljavali akontaciju ili predujam na računu kojim se stvarno tereti klijenta, prvo se mora fakturirati akontacija ili predujam.

Poduzmite sljedeće korake za fakturiranje akontacije ili predujma.

1. Odaberite **Prodaja** > **Naplata** > **Akontacije i predujmovi**. 
2. Na stranici **Predujmovi i akontacije** upotrijebite filtar za odabir određene akontacije ili predujma za fakturiranje i označite ih kao **Spremno za fakturiranje**.
3. Stvorite račun bilo ručno iz popisa **Ugovor o projektu** ili stranice s pojedinostima. Akontacija ili predujam prikazan je na nacrtu fakture u odjeljku **Predujmovi i akontacije** na stranici **Faktura**.
4. Potvrdite fakturu. To će akontaciju ili predujam učiniti dostupnim za uporabu. Valjanost računa možete provjeriti na stranici s popisom **Akontacije i predujmovi**. Za fakturirani predujam ili akontaciju, dostupni iznos prikazuje se u rešetki.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Stvaranje akontacije ili predujma iz rešetke računa

Akontaciju ili predujam možete stvoriti izravno na računu.

1. Na nacrtu fakture, na podrešetki **Predujmovi i akontacije**, odaberite **Novo** za stvaranje nove akontacije ili predujma. 
2. Na stranici **Brzo stvaranje** dodajte nužne podatke, a zatim odaberite **Spremi**. Akontacija ili predujam stvaraju se na ugovoru o projektu koji je povezan s računom. Akontacija ili predujam automatski se označavaju kao **Spremno za fakturiranje** i potom se dodaju podrešetki **Predujmovi i akontacije** na stranici **Faktura**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Usklađivanje fakturirane akontacije ili predujma

Nakon što se akontacija ili predujam fakturira, mogu se upotrebljavati na računu s vremenom, troškovima, kontrolnim točkama ili drugim projektnim troškovima. Klijent će vidjeti iznos svoje fakture umanjen za akontaciju ili predujam upotrijebljen na toj fakturi.

Na svakoj fakturi koja se generira za ugovor o projektu koji ima fakturirane akontacije ili predujmove, Project Operation automatski na fakturu primjenjuje akontaciju ili predujam.

To se može vidjeti u rešetki **Primijenjene akontacije i predujmovi** na stranici **Faktura**. Sljedeća tablica pruža informacije o poljima na rešetki **Primijenjene akontacije i predujmovi** stranice **Faktura za projekt**.

| Polje | Lokacija | Opis | Utjecaj na niže razine |
| --- | --- | --- | --- |
| Opis | Rešetka **Primijenjene akontacije i predujmovi** na stranici **Faktura za projekt** |Ovo je polje samo za čitanje i pruža opis akontacije ili predujma koji se upotrebljava na ovoj fakturi. Ta se vrijednosti ne može promijeniti na fakturi. Ova se vrijednost može ažurirati na podrešetki, na stranici **Ugovor o projektu**. | Ovo se polje može prikazati klijentu na ispisanom računu kako bi se naznačilo koja se akontacija ili predujam primjenjuje na računu. |
| Isporučeno | Rešetka **Primijenjene akontacije i predujmovi** na stranici **Faktura za projekt**  | Ovo je polje samo za čitanje i osigurava datum fakture akontacije ili predujma koji se upotrebljava na ovoj fakturi. Ta se vrijednosti ne može promijeniti na fakturi. Ova se vrijednost može ažurirati na podrešetki, na stranici **Ugovor o projektu**. | Ovo se polje može prikazati klijentu na ispisanom računu kako bi se naznačio datum na koji je akontacija ili predujam prvi put fakturiran klijentu. |
| Iznos | Rešetka **Primijenjene akontacije i predujmovi** na stranici **Faktura za projekt**  | Ovo je polje samo za čitanje i pruža iznos akontacije ili predujma koji se upotrebljava na ovoj fakturi. Ta se vrijednosti ne može promijeniti na fakturi. Ova se vrijednost može ažurirati na podrešetki, na stranici **Ugovor o projektu**. | Ovo se polje može prikazati klijentu na ispisanom računu kako bi se naznačio izvorni iznos akontacije ili predujma koji je klijent platio. |
| Iskorišteni iznos | Rešetka **Primijenjene akontacije i predujmovi** na stranici **Faktura za projekt**  | Ovo je polje samo za čitanje i daje izračunanu vrijednost koja sažima koliko je akontacije ili predujma upotrijebljeno. | Ovo se polje može prikazati klijentu na ispisanom računu kako bi se naznačio iznos iz te akontacije ili predujma koji je već upotrijebljen. |
| Prošireni iznos | Rešetka **Primijenjene akontacije i predujmovi** na stranici **Faktura za projekt**  | Ovo se polje može uređivati i pruža iznos akontacije ili predujma koji je upotrijebljen na ovoj fakturi za projekt. Ovaj iznos ne može biti veći od onoga što je dostupan na predujmu. Sustav to automatski izračunava kao razliku između polja **Iznos** i **Upotrijebljeni iznos** na rešetki. Možete smanjiti ovaj iznos kako biste upotrijebili manje od onoga što je dostupno, ali ne možete povećati iznos kako biste upotrebljavali više od onoga što je dostupno. | Ovo se polje može prikazati klijentu na ispisanom računu kako bi se naznačio iznos iz te akontacije ili predujma koji se upotrebljavao na fakturi. |
| Iznos salda akontacije. | Rešetka **Primijenjene akontacije i predujmovi** na stranici **Faktura za projekt**  | Ovo je polje samo za čitanje i pruža vrijednost preostalog dijela akontacije ili predujma nakon potvrde fakture. | Ovo se polje može prikazati klijentu na ispisanom računu kako bi se naznačio iznos koji će preostati iz te akontacije ili predujma nakon što se faktura potvrdi i plati. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]