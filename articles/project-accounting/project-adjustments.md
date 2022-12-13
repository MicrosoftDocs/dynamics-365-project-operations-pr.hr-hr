---
title: Prilagodbe projekata
description: U ovom se članku nalaze informacije o prilagodbama projekata.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788362"
---
# <a name="project-adjustments"></a>Prilagodbe projekata

_**Odnosi se na:** Project Operations za scenarije koji se temelje na zalihama/proizvodnji_

## <a name="adjustments-overview"></a>Pregled prilagodbi

Microsoft Dynamics 365 Project Operations možete konfigurirati tako da korisnici mogu mijenjati proknjižene transakcije. Projektne transakcije možete prilagoditi pojedinačno ili možete odabrati više transakcija odjednom na popisu svih projektnih transakcija. Prilagodbe projekata koriste se, na primjer, za masovno ažuriranje naplativog statusa, ponovni izračun troškova nakon promjene konfiguracije ili ažuriranje izvora financiranja.

Korisnici mogu pristupiti funkciji prilagodbe projekta na nekoliko načina:

- Korištenjem stranice Prilagodba **transakcija** kojoj se može pristupiti iz **programa Project Management i Accounting** \> **Setup**.
- Pomoću gumba Prilagodba na stranici Proknjižene projektne transakcije **kojima se može pristupiti iz** upravljanja projektima i **računovodstvenih**  transakcija. **·** \> **·**
- Pomoću gumba Prilagodba **na** **stranici Proknjižene projektne transakcije** u kontekstu projekta. Ovoj stranici možete pristupiti iz **project managementa i računovodstva** \> **Svi projekti**.

Da biste omogućili prilagodbe, morate omogućiti jedan ili više statusa transakcija iz **upravljanja projektima i računovodstvenog** \> **upravljanja projektima i računovodstvenih paramatera** na **kartici Općenito** u odjeljku **Dopusti prilagodbu statusa** transakcije. Primjeri statusa transakcija obuhvaćaju proknjižene transakcije, fakturirane transakcije ili eliminirane transakcije. Bilo koji status transakcije postavljen na **Ne** imat će transakcije u tom statusu koje se neće pojaviti unutar postupka prilagodbe kao odabrane za prilagodbu.

Mogućnost konfiguracije pod nazivom **Uvijek stvori transakciju** prilagodbe trenutno je dostupna u parametrima upravljanja projektima i računovodstvu. Ovu mogućnost možete onemogućiti za ažuriranje izvorne transakcije umjesto stvaranja novih transakcija tijekom prilagodbe u podskupini scenarija. Najavljeno je da će ovaj parametar biti amortiziran do 1. ožujka 2023. godine. Nakon 1. ožujka 2023. sustav će se uvijek ponašati kao da je opcija omogućena.

## <a name="adjustments-process-flow"></a>Tijek procesa podešavanja

Sljedeći koraci prikazuju tipičan tijek za obradu prilagodbi.

1.  **Otvorite stranicu Prilagodbe** projekta.
2. Odaberite **Odaberi** da biste potražili transakcije koje zadovoljavaju očekivane kriterije za prilagodbu.
3. Na popisu transakcija odaberite sve transakcije ili podskup transakcija za prilagodbu.
4. Odaberite **Prilagodi** i izmijenite atribute u retku. Alternativno, ako su vrijednosti ručno navedene tijekom unosa transakcije, možete odabrati unos zadanih vrijednosti sustava.
5. Popis transakcija se vraća, a u **stupcu Neriješeno prilagođavanje** pojavljuje se kvačica koja označava gdje su izvršene promjene. Sve prilagodbe koje imaju neriješene promjene prikazane su u donjoj polovici stranice. Tamo možete napraviti dodatne detaljne promjene izvan onoga što je prikazano na prethodnoj stranici.
6. Odaberite **Proknjiži** da biste proknjižili transakcije prilagođavanja.

Ovisno o konfiguraciji, za prilagodbu se obično kreiraju nove transakcije.

- Polje **Status** fakture izvorne transakcije postavljeno je na **Prilagođeno**.
- Kreira se stornirana transakcija da bi se stornirala izvorna transakcija, a **polje Status** postavljeno je na **Prilagođeno**.
- Kreira se nova transakcija koja sadrži promjene izvršene tijekom postupka prilagođavanja.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Odabir više proknjiženih projektnih transakcija odjednom za prilagođavanja i kreditne napomene

Nova značajka uvedena u izdanje 10.0.30 omogućuje odabir više transakcija za prilagodbu odjednom sa **stranice Proknjižene projektne transakcije** .

Da biste mogli koristiti ovu značajku, ona mora biti omogućena u vašem sustavu. Administratori mogu koristiti **radni prostor za upravljanje** značajkama kako bi provjerili status značajke i omogućili je ako je potrebna.  **U radnom prostoru za upravljanje** značajkama potražite i odaberite **Višestruko odaberite Proknjižene projektne transakcije za prilagođavanja i kreditne bilješke**, a zatim odaberite **Omogući odmah**.

Ova značajka omogućuje sljedeće ključne funkcije:

- Može mu se pristupiti sa stranice proknjižene transakcije unutar projekta pomoću postojećeg **gumba Za prilagodbu** .
- Omogućuje kontrolu odabira u više redaka **na stranici Proknjižene transakcije** projekta. Možete primijeniti filtre na stranicu popisa i odabrati zapise prije početka podešavanja.
- Onemogućuje **gumb Prilagodba** ako se bilo koja pojedinačna transakcija ne može prilagoditi ili ako odaberete kombinaciju kreditnih bilješki i temeljnica zajedno umjesto pojedinačno.
- Zbog dodavanja kontrole odabira u više redaka veza Predani trošak **na** vrpci više nije onemogućena ako je odabrano više redaka.
- Dodaje sljedeću poruku upozorenja: "Odabrali ste više od (odabranih brojeva) zapisa za prilagodbu. Nastavak ove akcije mogao bi potrajati neko vrijeme. Jeste li sigurni da biste željeli nastaviti s ovom akcijom?"

Ova značajka također uklanja korak 2 iz tijeka procesa koji je opisan ranije u ovom članku. Stoga će sve transakcije koje su odabrane prije **otvaranja stranice Prilagodba transakcija biti uključene** u popis transakcija za prilagodbu. Da biste ih potražili, ne morate koristiti gumb **Odaberi** .

> [!NOTE] 
> Čak i ako je ova značajka onemogućena, i dalje možete odabrati više zapisa za prilagodbu. Međutim, samo će *jedan zapis ostati odabran*, a **dijaloški okvir Odabir transakcija** pojavit će se odmah nakon što odaberete otvaranje prilagođavanja.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Prilagodba statusa transakcija koji se mogu omogućiti ili onemogućiti za prilagodbe

Sljedeći statusi mogu se omogućiti ili onemogućiti na kartici **Općenito** na **stranici Parametri** upravljanja projektima i računovodstva:

- Objavljeno
- Prijedlog fakture
- Fakturirano
- Procijenjeno
- Eliminiran
- Početni saldo (sat)

## <a name="adjustment-parameters"></a>Parametri prilagodbe

Ti su parametri navedeni na **stranici Parametri** upravljanja projektima i računovodstva na **kartici Općenito** u **grupi Prilagodba** i izmijenit će ponašanje za način obrade prilagodbi. 

| Naziv parametra | Opis |
|----------------|-------------
| Uvijek kreiraj transakciju prilagođavanja | Ako je ovaj parametar omogućen, postupak prilagodbe uvijek će kreirati novu transakciju storniranja i novu prilagođenu transakciju kada dođe do financijskog ili izvještajnog učinka. Ako je parametar onemogućen, postupak prilagodbe ažurirat će izvornu transakciju umjesto stvaranja storniranja i nove transakcije za scenarij kao što je ažuriranje teksta transakcije. |
| Polje automatskog ažuriranja | Ako je ovaj parametar omogućen, sustav će ponovno izračunati cijenu troškova i prodajnu cijenu. |
| Koristi datum prilagodbe kao novi projekt | Ovaj se parametar koristi za premještanje transakcija u buduću poslovni period prije nego što je sustav podržao ovu funkciju. Ne preporučujemo da ga koristite jer mijenja datum poslovanja transakcije i bit će amortiziran u budućem izdanju. |
| Dopusti zatvorene aktivnosti | Transakcije se obično ne mogu kreirati za zatvorene aktivnosti. Ako je ovaj parametar omogućen, to se ponašanje nadjačava. Stoga se prilagodbe mogu kreirati za zatvorene aktivnosti. |
