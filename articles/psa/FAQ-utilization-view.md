---
title: Prikaži naplativo korištenje za resurse
description: Ova tema pruža informacije o prikazu korištenja resursa.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e1c123854209b3cb5c310e3bbcb242c9219279a8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992825"
---
# <a name="view-chargeable-utilization-for-resources"></a>Prikaži naplativo korištenje za resurse

[!include [banner](../includes/psa-now-project-operations.md)]
 
**Prikaz korištenja** na stranici **Korištenje resursa programa Project Service** prikazuje naplativo korištenje za svaki resurs koji je moguće rezervirati. Budući da se taj prikaz temelji na ploči s rasporedom, pronaći ćete mnoge iste funkcije.

> ![Snimka zaslona prikaza korištenja](media/FAQ-utilization-1.png)
 

Naplativo korištenje izračunava se na sljedeći način:

   Naplativo korištenje = (Naplativi stvarni sati) / (kapacitet resursa)

Ćelije predstavljaju izračunato naplativo korištenje za odabrano razdoblje (dani, tjedni ili mjeseci).

Boje u ćelijama predstavljaju naplativo korištenje za resurs u usporedbi s njegovim ciljnim naplativim korištenjem. 

Ciljno korištenje može se postaviti na zadanu ulogu resursa ili na sam određeni resurs. Izračun prvo uzima u obzir pojedinačni za cilj, a zatim zadanu ulogu resursa.

## <a name="set-target-on-a-resource"></a>Postavi cilj na resurs

1. Otvorite **Resursi** \> **Resursi**. 
2. Odaberite resurs da biste otvorili zapis. 
3. Na kartici **Project Service**, možete postaviti ciljno korištenje resursa.

> ![Snimka zaslona s prikazom postavljanja ciljnog korištenja s pomoću kartice Project Service](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Postavi ciljno korištenje na ulogu

1. Idite na **Resursi** \> **Uloge resursa**. 
2. Odaberite ulogu i otvorite zapis. 
3. Postavite ciljno korištenje za ulogu.

> ![Snimka zaslona s prikazom postavljanja ciljnog korištenja s pomoću Uloga resursa](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Izračunaj naplativo korištenje za resurs

Da biste izračunali naplativo korištenje za resurs, morate ispuniti neke preduvjete. 

### <a name="set-default-role-for-individual-resource"></a>Postavi zadanu ulogu za pojedinačni resurs

Najprije, ciljno korištenje mora se postaviti na pojedinačni resurs ili na uloge resursa. Ako za ciljeve upotrebljavate uloge resursa, svaki pojedinačni resurs mora imati zadanu ulogu. 

1. Da biste to postavili, idite na **Resursi** \> **Resursi**. 
2. Odaberite resurs, otvorite zapis, a zatim odaberite karticu **Project Service**. 
3. U rešetki **Uloga resursa**, provjerite postoji li jedna uloga za resurs i je li **Zadana** postavljena na **Da**.
 
### <a name="change-billing-type-for-resource-role"></a>Promijeni vrstu naplate za ulogu resursa

Uloge resursa moraju se postaviti tako da im je vrsta naplate **Naplativa**. 

1. Idite na **Resursi** \> **Uloge resursa**. 
2. Otvorite zapis koji želite ažurirati, a zatim postavite zadanu postavku vrste naplate na **Naplativa**.

### <a name="set-working-hours-for-resource-role"></a>Postavi radno vrijeme za ulogu resursa
 
Da bi izračun kapaciteta bio moguć, za resurs mora biti postavljeno radno vrijeme. 

1. Otvorite **Resursi** \> **Resursi**. 
2. Odaberite resurs da biste otvorili zapis pa odaberite stavku **Prikaži radno vrijeme**. 
3. Možete skupno ažurirati popis resursa primjenom **Predložak radnog vremena** s prikaza **Popis resursa**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Uklanjanje poteškoća s naplativim stvarnim satima

Naplativi stvarni sati preuzimaju se iz entiteta **Stvarne vrijednosti**. Stvarne vrijednosti s vrstom naplate **Naplativa** uključeni su u izračun i stoga morate imati projekte u kojima su stvarne vrijednosti naplative.

Ako nije prikazano naplativo korištenje, evo nekih stvari koje možete provjeriti:

- je li za kapacitet resursa postavljeno radno vrijeme;
- je li resursu dodijeljen pojedinačno definiran cilj korištenja ili mu je dodijeljena zadana uloga; je li za ulogu definiran cilj korištenja;
- Stvarne vrijednosti imaju vrstu naplate **Naplativa** za razdoblje za koje očekujete izračun korištenja. Provjerite sljedeće ako su prikazane stvarne vrijednosti s drugačijim vrstama naplate od naplative:

  - je li zadana vrsta naplate za ulogu koja je upotrijebljena na stvarnoj vrijednosti drugačija od naplative;
  - je li uloga na retku ugovora projekta koja podržava projekt postavljena na nenaplativa;
  - je li projektu pridružen redak ugovora.



[!INCLUDE[footer-include](../includes/footer-banner.md)]