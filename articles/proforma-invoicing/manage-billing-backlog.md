---
title: Upravljanje zaostalim naplatama
description: U ovoj temi nalaze se informacije o načinu prikaza zaostalih naplata i rada s njima u aplikaciji Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2e839c1f32248fff6d97271796666b5031f66490ccd98574045b770100bf379f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991072"
---
# <a name="manage-billing-backlog"></a>Upravljanje zaostalim naplatama

**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha

Dynamics 365 Project Operations ima namjenske prikaze koji pomažu pri upravljanju zaostalim naplatama. Kako biste upravljali zaostalim naplatama, odaberite veze u području **Prodaja** pod stavkom **Naplata**. 

Dostupni su sljedeći prikazi:

- Zadržavanja i predujmovi
- Dostupna zadržavanja i predujmovi
- Kontrolne točke fiksne cijene
- Zaostale naplate za vrijeme i materijal

## <a name="retainers-and-advances"></a>Zadržavanja i predujmovi

Na prikazu **Akontacije i predujmovi** navode se akontacije i predujmovi u svim ugovorima o projektu. Nakon fakturiranja akontacije ili predujma, iznos predujma postaje dostupan za uporabu.

## <a name="available-retainers-and-advances"></a>Dostupne akontacije i predujmovi

Na prikazu **Dostupne akontacije i predujmovi** navode se sve dostupne akontacije i predujmovi u svim ugovorima o projektu. Nakon fakturiranja akontacije ili predujma, iznos predujma postaje dostupan za uporabu i dodaje se popisu. Nakon što se u potpunosti iskoristi iznos akontacije ili predujma, uklanjaju se s popisa.

## <a name="fixed-price-milestones"></a>Kontrolne točke fiksne cijene

Na prikazu **Kontrolne točke fiksne cijene** navedene su sve kontrolne točke fiksne cijene u svim redcima ugovora o projektu. Iz ovog se prikaza pojedinačne ili višestruke kontrolne točke mogu označiti kao **Spremno za fakturiranje** ili **Nije spremno za fakturiranje**. Označavajući kontrolnu točku kao **Spremno za fakturiranje** omogućuje stavljanje na nacrt fakture.

Kada redci ugovora s više klijenata imaju način naplate s fiksnom cijenom, stvara se kontrolna točka za svakog klijenta na retku ugovora. Kontrolna točka može se stvoriti, a zatim podijeliti u pojedinačne zapise kontrolne točke specifične za klijenta. Ovo je dijeljenje interno i u skladu s dijeljenjem postotka naplate definiranim za svakog klijenta u retku ugovora. U prikazu **Kontrolne točke s fiksnom cijenom** vidjet ćete pojedinačne zapise kontrolne točke specifične za klijenta. Svaki od ovih zapisa može se označiti kao **Spremno za fakturiranje** odvojeno od ovog prikaza. Kada se jedna ili više povezanih podjela kontrolne točke označi kao **Spremno za fakturiranje**, stanje zaglavlja ažurira se na **U tijeku** iz **Nije pokrenuto**. Kada se fakturiraju sve podjele kontrolne točke, stanje kontrolne točke zaglavlja ažurira se na **Dovršeno**.

Kontrolna točka na nacrtu fakture prikazuje se u ovom prikazu sa statusom naplate **Faktura za klijenta stvorena**. Kada se potvrdi nacrt fakture, status naplate na zapisu ažurira se na **Faktura klijenta proknjižena**. 

> [!NOTE] 
> Nemojte ažurirati ovu vrijednost stanja s pomoću prilagođenog kôda. Project Operations ne funkcioniraju ispravno kada se ove vrijednosti statusa ažuriraju prilagođenim kodom.

## <a name="time-and-material-billing-backlog"></a>Zaostale naplate za vrijeme i materijal

Prikaz **Zaostale naplate vremena i materijala** navodi sve nenaplaćene stvarne podatke o prodaji u svim ugovorima o projektu u sustavu koje nisu fakturirane. Iz ovog se prikaza jedan ili više stvarnih podataka o nenaplaćenim prodajama mogu označiti kao **Spremno za fakturiranje** ili **Nije spremno za fakturiranje**. Označavanje stvarnog podatka o nefakturiranoj prodaji kao **Spremno za fakturiranje** omogućuje stavljanje na nacrt računa.

Nenaplaćene stvarne podatke o prodaji sa statusom **Ne smije se prekoračiti** od **Neuspjelo** ne može se označiti kao **Spremno za fakturiranje**. Ako stvarne podatke treba označiti kao **Spremno za fakturiranje**, vratite stanje na drugim stvarnim podacima na retku ugovora koje su se dogodili, a zatim ponovno procijenite stanje **Ne smije se prekoračiti**.

Ako redci ugovora za više klijenata imaju način naplate vremena i materijala, kada se odobre vrijeme i troškovi, stvara se jedna nefakturirana stvarna prodaja za svakog kupca u retku ugovora prema razdijeljenom postotku naplate utvrđenom za svakog klijenta. U prikazu **Zaostale naplate vremena i materijala** vidjet ćete ove pojedinačne stvarne podatke o nenaplaćenoj prodaji. Svaki od ovih zapisa stvarnih podataka o nefakturiranoj prodaji može se odvojeno od ovog prikaza označiti kao **Spremno za fakturiranje**.

Nenaplaćena stvarna prodaja koja se nalazi na skici fakture prikazuje se na ovom prikazu sa stanjem naplate **Faktura za kupca stvorena**. Kada se nacrt fakture potvrdi, status naplate na ovom zapisu ažurira se na **Faktura za klijenta proknjižena**. 

> [!NOTE] 
> Nemojte ažurirati ovu vrijednost stanja s pomoću prilagođenog kôda. Project Operations ne funkcioniraju ispravno kada se ove vrijednosti statusa ažuriraju prilagođenim kodom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
