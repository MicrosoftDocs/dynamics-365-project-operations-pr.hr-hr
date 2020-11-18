---
title: Upravljanje zaostalim naplatama
description: U ovoj temi nalaze se informacije o načinu prikaza zaostalih naplata i rada s njima u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec77f3911a460b96414a61bc44ea254f1b7da660
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087849"
---
# <a name="manage-the-billing-backlog"></a>Upravljanje zaostalim naplatama

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Dynamics 365 Project Operations ima dva namjenska prikaza koja vam pomažu pri radu sa zaostalim naplatama i upravljanju njima. To su **Kontrolne točke s fiksnom cijenom** i **Zaostale naplate vremena i materijala**. Za odabir prikaza, u lijevom navigacijskom oknu na području aplikacije Project Operations **Prodaja** , odaberite **Naplata**. Veze zaostalih naplata tamo se pohranjuju.

## <a name="fixed-price-milestones"></a>Kontrolne točke fiksne cijene

Ovaj prikaz navodi sve kontrolne točke s fiksnom cijenom u svim redcima ugovora o projektu u sustavu. Iz ovog se prikaza jedna ili više kontrolnih točaka mogu označiti kao **Spremno za fakturiranje** ili **Nije spremno za fakturiranje**. Kada označite kontrolnu točku kao **Spremno za fakturiranje** , ona postaje dostupna za nacrt fakture.

Kada redci ugovora s više klijenata imaju način naplate s nepromjenjivom cijenom, stvara se jedna kontrolna točka za svakog klijenta na retku ugovora. Korisnik stvara kontrolnu točku i ona se dijeli unutar klijenta = specifični interni zapisi kontrolne točke, u skladu s podjelom postotka naplate definiranom za svakog klijenta u retku ugovora. U prikazu **Kontrolne točke s nepromjenjivom cijenom** vidjet ćete pojedinačne zapise kontrolne točke specifične za klijenta. Svaki od ovih zapisa može se označiti kao **Spremno za fakturiranje** odvojeno od ovog prikaza. Kada se jedno ili više povezanih odvajanja kontrolne točke označi kao **Spremno za fakturiranje** , zaglavlje prelazi u status **U tijeku** iz statusa **Nije pokrenuto**. Kada se fakturiraju svi dijelovi kontrolne točke, status zaglavlja kontrolne točke prelazi u **Završeno**.

Kontrolna točka na nacrtu fakture prikazuje se u ovom prikazu sa statusom naplate **Faktura za klijenta stvorena**. Kada se nacrt fakture potvrdi, status naplate na ovom zapisu ažurira se na **Faktura proknjižena**. Ažuriranje ove vrijednosti statusa s pomoću prilagođenog koda ne preporučuje se. Project Operations neće ispravno funkcionirati ako se ove vrijednosti statusa ažuriraju prilagođenim kodom.

## <a name="time-and-material-billing-backlog"></a>Zaostale naplate za vrijeme i materijal

U ovom su prikazu navedene svi stvarni podaci o nenaplaćenim prodajama koje nisu fakturirane u svim ugovorima o projektu diljem sustava. Iz ovog se prikaza jedan ili više stvarnih podataka o nenaplaćenim prodajama mogu označiti kao **Spremno za fakturiranje** ili **Nije spremno za fakturiranje**. Označavanje stvarnog podatka o nefakturiranoj prodaji kao **Spremno za fakturiranje** omogućuje stavljanje na nacrt računa.

Stvarni podaci o nenaplaćenoj prodaji koji imaju status **Ne smije se prekoračiti** stavke **Neuspjelo** ne može se označiti kao **Spremno za fakturiranje**. Ako ove stvarne podatke treba označiti kao takve, poništite status ostalih stvarnih podataka u retku ugovora koji su izvršeni, a zatim procijenite status **Ne smije se prekoračiti**.

U slučaju redaka ugovora s više klijenata koji imaju način naplate Vrijeme i Materijal, kada se odobre vrijeme i troškovi, za svakog klijenta u retku ugovora stvara se stvarni podatak o neplaćenoj prodaji prema podijeljenom postotku naplate definiranom za svakog klijenta u retku ugovora. U prikazu **Zaostala naplata vremena i materijala** vidjet ćete ove pojedinačne stvarne podatke o nefakturiranoj prodaji specifične za klijenta. Svaki od ovih zapisa stvarnih podataka o nefakturiranoj prodaji može se odvojeno od ovog prikaza označiti kao **Spremno za fakturiranje**.

Stvarni podatak o nenaplaćenoj prodaji na nacrtu fakture prikazuje se u ovom prikazu s pomoću **Statusa naplate** **Faktura za klijenta stvorena**. Kada se nacrt fakture potvrdi, status naplate na ovom zapisu ažurira se na **Faktura za klijenta proknjižena**. Ažuriranje ove vrijednosti statusa, kada je u ovom statusu, s pomoću prilagođenog koda ne preporučuje se. Project Operations neće ispravno funkcionirati kada se ove vrijednosti statusa ažuriraju prilagođenim kodom.