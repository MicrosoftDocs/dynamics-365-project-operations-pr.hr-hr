---
title: Konfiguriranje automatskog stvaranja predračuna
description: U ovoj temi nalaze se informacije o konfiguriranju automatskog stvaranja predračuna.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e146dd510b3795d52d164fc6acf8e5400ba11310
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073297"
---
# <a name="configure-automated-proforma-invoice-creation"></a>Konfiguriranje automatskog stvaranja predračuna

_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_

Možete konfigurirati automatsko stvaranje faktura u programu Dynamics 365 Project Operations. Sustav stvara nacrt predračuna na temelju rasporeda faktura za svaki ugovor o projektu i redak ugovora. Rasporedi faktura konfigurirani su na razini retka ugovora. Svaki redak ugovora može imati različit raspored faktura ili isti raspored faktura može biti uključen u svaki redak ugovora.

Kada stvarate fakturu, sustav uvijek stvara barem jednu fakturu po ugovoru o projektu. U nekim slučajevima može biti stvoreno više faktura.

Na primjer, ako ugovor ima više klijenata, stvorit će se onoliki broj računa koliko ima klijenata koji imaju naplative transakcije za fakturiranje na tom ugovoru o projektu.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Razumijevanje načina uključivanja transakcija u račun 

Ponekad svaki redak ugovora koji se temelji na projektu navodi zaseban raspored faktura. Na primjer, usluge implementacije iz ugovora Adatum imaju sljedeće retke ugovora:

- Prototip rada koji je fiksna cijena s dvije ručno stvorene kontrolne točke.
- Posao implementacije koji uključuje Vrijeme i koji će se naplaćivati ponedjeljkom svaka dva tjedna.
- Nastali troškovi koji se trebaju naplaćivati mjesečno prvog ponedjeljka u mjesecu.

Rasporedi faktura definirani za svaku od ove dvije stavke retka izgledaju kao sljedeća tablica:

| Redak ugovora | Datum izrade fakture | Datum završetka transakcije | Datum kontrolne točke | Iznos kontrolne točke |
| --- | --- | --- | --- | --- |
| Prototip rada | Ponedjeljak, 5. listopada | - | Ponedjeljak, 5. listopada | 5000 USD |
| - | Utorak, 3. studenog | - | Utorak, 3. studenog | 12,000 USD |
| Rad na implementaciji | Ponedjeljak, 5. listopada | Nedjelja, 4. listopada | - | - |
| - | Ponedjeljak, 19. listopada | Nedjelja, 18. listopada | - | - |
| - | Ponedjeljak, 2. studenog | Nedjelja, 1. studeni | - | - |
| - | Ponedjeljak, 16. studeni | Nedjelja, 15. studeni | - | - |
| Nastali troškovi | Ponedjeljak, 5. listopada | Nedjelja, 4. listopada | - | - |
| - | Ponedjeljak, 2. studenog | Nedjelja, 1. studeni | - | - |

U ovom primjeru, kada se automatsko fakturiranje pokreće dana:

- **4. listopada ili neki datum prije** : Za ovaj se ugovor ne generira faktura jer tablica **Raspored fakture** za svaki od ovih redaka ugovora ne poziva 4. listopada, nedjelju kao datum pokretanja fakture.
- **Ponedjeljak, 5. listopada** : Generira se jedna faktura za:

    - Prototip rada koji uključuje kontrolnu točku, ako je označena kao **Spremno za fakturiranje**.
    - Rad na implementaciji koji uključuje sve vremenske transakcije stvorene prije datuma presijecanja transakcija, nedjelja, 4. listopada, koji je označen kao **Spremno za fakturiranje**.
    - Nastali trošak koji uključuje sve transakcije troškova stvorenih prije datuma presijecanja transakcija, nedjelja, 4. listopada, koji je označen kao **Spremno za fakturiranje**.
  
- **6. listopada ili neki datum prije 19. listopada** : Za ovaj se ugovor ne generira faktura jer tablica **Raspored faktura** za svaki od ovih redaka ugovora ne poziva 6. listopada ili neki datum prije 19. listopada kao datum pokretanja fakture.
- **19. listopad, ponedjeljak** : Jedna je faktura generirana za rad na implementaciji koji uključuje sve vremenske transakcije stvorene prije datuma presijecanja transakcija, 18. listopada, nedjelja, koji je označen kao **Spremno za fakturiranje**.
- **Ponedjeljak, 2. listopada** : Generira se jedna faktura za:

    - Rad na implementaciji koji uključuje sve vremenske transakcije stvorene prije datuma presijecanja transakcija, nedjelja, 1. studeni, koji je označen kao **Spremno za fakturiranje**.
    - Nastali trošak koji uključuje sve transakcije troškova stvorenih prije datuma presijecanja transakcija, nedjelja, 1. studeni, koji je označen kao **Spremno za fakturiranje**.

- **Utorak, 3. studenog** : Generira se jedna faktura za rad na prototipu koji uključuje kontrolnu točku za 12.000 USD, ako je označena kao **Spremno za fakturiranje**.

## <a name="configure-automatic-invoicing"></a>Konfiguriranje automatskog fakturiranja

Poduzmite sljedeće korake za konfiguraciju automatskog pokretanja faktura.

1. U stavci **Projektne operacije** idite na **Postavke** > **Ponavljanje postavljanja fakture**.
2. Stvorite skupni posao i dodijelite mu naziv **Fakture stvorene u aplikacije Project Operations**. Naziv skupnog posla mora sadržavati riječi „stvaranje faktura”.
3. U polju **Vrsta posla** odaberite **Ništa**. Prema zadanim postavkama polja **Dnevna učestalost** i **Aktivno je** postavljena su na **Da**.
4. Odaberite **Pokreni tijek rada**. U dijaloškom okviru **Pretraživanje zapisa** vidjet ćete tri tijeka rada:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Odaberite **ProcessRunCaller** , a zatim **Dodaj**.
6. U sljedećem dijaloškom okviru odaberite **U redu**. Nakon tijeka rada **Sleep** slijedi tijek rada **Process**. 

> [!NOTE]
> U petom koraku možete odabrati i **ProcessRunner**. Zatim, kada odaberete **U redu** , nakon tijeka rada **Process** slijedi tijek rada **Sleep**.

Tijekovi rada **ProcessRunCaller** i **ProcessRunner** stvaraju fakture. **ProcessRunCaller** poziva **ProcessRunner**. **ProcessRunner** jest tijek rada koji stvara fakture. Radni tijek prolazi kroz sve retke ugovora za koje je potrebno stvoriti fakture i stvara fakture za te retke. Da bi se odredili reci ugovora za koje je potrebno stvoriti fakture, posao traži datume stvaranja faktura za retke ugovora. Ako reci ugovora koji pripadaju jednom ugovoru imaju isti datum stvaranja fakture, transakcije se kombiniraju u jednu fakturu koja ima dva retka fakture. Ako nema transakcija za stvaranje faktura, posao preskače stvaranje fakture.

Nakon pokretanja funkcije **ProcessRunner** poziva se **ProcessRunCaller** , navodi se vrijeme završetka i funkcija se zatvara. **ProcessRunCaller** zatim pokreće mjerač vremena koji se izvodi 24 sata od navedenog vremena završetka. Po završetku izvođenja mjerača vremena funkcija **ProcessRunCaller** zatvara se.

Skupni postupak stvaranja faktura ponavljajući je posao. Ako se taj skupni postupak izvodi više puta, stvaraju se višestruke instance posla koje uzrokuju pogreške. Stoga biste trebali pokrenuti skupni postupak samo jednom i zatim ga ponovno pokrenuti samo ako se prestane izvoditi.

> [!NOTE]
> Skupno fakturiranje u aplikaciji Project Operations izvršava se samo za retke ugovora o projektu koji su konfigurirani prema rasporedu faktura. Ugovorni redci s načinom naplate fiksne cijene moraju imati konfigurirane prekretnice. Redak projektnog ugovora s vremenskim i materijalnim načinom naplate treba imati postavku rasporeda računa na temelju datuma.