---
title: Upravljanje zaostalim naplatama projekta
description: U ovoj temi nalaze se informacije o raznim prikazima dostupnim za uporabu tijekom upravljanja zaostalom naplatom na projektima.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 25dc9cff6aeb6daed9a27ba843a74b892ca4751c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866987"
---
# <a name="manage-project-billing-backlog"></a>Upravljanje zaostalim naplatama projekta 

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Dynamics 365 Project Operations ima namjenske prikaze koji pomažu pri upravljanju zaostalim naplatama. Kako biste upravljali zaostalim naplatama, odaberite veze u području **Prodaja** pod stavkom **Naplata**. 

Dostupni su sljedeći prikazi:

- Akontacije i predujmovi
- Dostupne akontacije i predujmovi
- Kontrolne točke fiksne cijene
- Zaostale naplate za proizvod
- Zaostale naplate za vrijeme i materijal

## <a name="retainers-and-advances"></a>Akontacije i predujmovi

Prikaz **Akontacije i predujmovi** navodi sve akontacije i predujmove u svim ugovorima o projektu u sustavu. Nakon fakturiranja akontacije ili predujma, iznos predujma postaje dostupan za uporabu.

## <a name="available-retainers-and-advances"></a>Dostupne akontacije i predujmovi

Prikaz **Dostupne akontacije i predujmovi** navodi sve dostupne akontacije i predujmove u svim ugovorima o projektu u sustavu. Nakon fakturiranja akontacije ili predujma, iznos predujma postaje dostupan za uporabu i dodaje se popisu. Nakon što se u potpunosti iskoristi iznos akontacije ili predujma, uklanja se s popisa.

## <a name="fixed-price-milestones"></a>Kontrolne točke fiksne cijene

Prikaz **Kontrolne točke s fiksnom cijenom** navodi sve kontrolne točke s fiksnom cijenom u svim redcima ugovora o projektu u sustavu. Iz ovog se prikaza jedna ili više kontrolnih točaka mogu označiti kao **Spremno za fakturiranje** ili **Nije spremno za fakturiranje**. Označavajući kontrolnu točku kao **Spremno za fakturiranje** omogućuje stavljanje na nacrt fakture.

Kada redci ugovora s više klijenata imaju način naplate s fiksnom cijenom, stvara se kontrolna točka za svakog klijenta na retku ugovora. Kontrolna točka može se stvoriti, a zatim podijeliti u pojedinačne zapise kontrolne točke specifične za klijenta. Ovo je dijeljenje interno i u skladu s dijeljenjem postotka naplate definiranim za svakog klijenta u retku ugovora. U prikazu **Kontrolne točke s fiksnom cijenom** vidjet ćete pojedinačne zapise kontrolne točke specifične za klijenta. Svaki od ovih zapisa može se označiti kao **Spremno za fakturiranje** odvojeno od ovog prikaza. Kada se jedno ili više povezanih razdvajanja kontrolnih točki označi kao **Spremno za fakturiranje**, status zaglavlja ažurira se na **U tijeku** iz **Nije pokrenuto**. Kada se fakturiraju sve podjele kontrolnih točaka, status kontrolne točke zaglavlja ažurira se na **Dovršeno**.

Kontrolna točka na nacrtu fakture prikazuje se u ovom prikazu sa statusom naplate **Faktura za klijenta stvorena**. Kada se potvrdi nacrt fakture, status naplate na zapisu ažurira se na **Faktura klijenta proknjižena**. Nemojte ažurirati ovu vrijednost statusa s pomoću prilagođenog koda. Project Operations ne funkcioniraju ispravno kada se ove vrijednosti statusa ažuriraju prilagođenim kodom.

## <a name="product-billing-backlog"></a>Zaostale naplate za proizvod

Prikaz **Zaostale naplate proizvoda** navodi sve retke ugovora koji se temelje na proizvodu u svim ugovorima o projektu u sustavu. Iz ovog se prikaza jedan ili više redaka ugovora koji se temelje na proizvodu mogu označiti kao **Spremno za fakturiranje** ili **Nije spremno za fakturiranje**. Označavajući redak ugovora koji se temelji na proizvodu kao **Spremno za fakturiranje** omogućuje njegovo stavljanje na nacrt fakture.

Redak ugovora koji se temelji na proizvodu koji se nalazi na nacrtu fakture prikazan je u ovom prikazu sa statusom naplate **Faktura za klijenta stvorena**. Kada se nacrt fakture potvrdi, status naplate na ovom zapisu ažurira se na **Faktura za klijenta proknjižena**. Nemojte ažurirati ovu vrijednost statusa s pomoću prilagođenog koda. Project Operations ne funkcioniraju ispravno kada se ove vrijednosti statusa ažuriraju prilagođenim kodom.

## <a name="time-and-material-billing-backlog"></a>Zaostale naplate za vrijeme i materijal

Prikaz **Zaostale naplate vremena i materijala** navodi sve nenaplaćene stvarne podatke o prodaji u svim ugovorima o projektu u sustavu koje nisu fakturirane. Iz ovog se prikaza jedan ili više stvarnih podataka o nenaplaćenim prodajama mogu označiti kao **Spremno za fakturiranje** ili **Nije spremno za fakturiranje**. Označavanje stvarnog podatka o nefakturiranoj prodaji kao **Spremno za fakturiranje** omogućuje stavljanje na nacrt računa.

Nenaplaćene stvarne podatke o prodaji sa statusom **Ne smije se prekoračiti** od **Neuspjelo** ne može se označiti kao **Spremno za fakturiranje**. Ako stvarne podatke treba označiti kao **Spremno za fakturiranje**, vratite zadani status drugih stvarnih podataka na redak ugovora na kojem su izvršene. i ponovno ocijenite status **Ne smije se prekoračiti**.

Ako redci ugovora za više klijenata imaju način naplate vremena i materijala, kada se odobre vrijeme i troškovi, stvara se jedna nefakturirana stvarna prodaja za svakog kupca u retku ugovora prema razdijeljenom postotku naplate utvrđenom za svakog klijenta. U prikazu **Zaostale naplate vremena i materijala** vidjet ćete ove pojedinačne stvarne podatke o nenaplaćenoj prodaji. Svaki od ovih zapisa stvarnih podataka o nefakturiranoj prodaji može se odvojeno od ovog prikaza označiti kao **Spremno za fakturiranje**.

Nenaplaćeni stvarni podatak o prodaji koji se nalazi na nacrtu fakture prikazan je u ovom prikazu sa statusom naplate **Faktura za klijenta stvorena**. Kada se nacrt fakture potvrdi, status naplate na ovom zapisu ažurira se na **Faktura za klijenta proknjižena**. Nemojte ažurirati ovu vrijednost statusa s pomoću prilagođenog koda. Project Operations ne funkcioniraju ispravno kada se ove vrijednosti statusa ažuriraju prilagođenim kodom.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
