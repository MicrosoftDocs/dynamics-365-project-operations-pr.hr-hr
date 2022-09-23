---
title: Postavljanje podizvođača kao resursa koji se mogu rezervirati
description: U ovom se članku objašnjava kako postaviti i održavati resurse kooperanta stvorene od korisnika i kontakata u sustavu, tako da se mogu povezati s podugovarateljima u Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 727508c41c190c3703e9cd1420066fa0e551f147
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522692"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Postavljanje podizvođača kao resursa koji se mogu rezervirati

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Slijedite ove korake za postavljanje podizvođača kao resursa koji se mogu rezervirati u aplikaciji Microsoft Dynamics 365 Project Operations.

1. Idite na **Projekt** \> **Resursi** i odaberite **Novi**.
2. Na stranici **Novi resurs koji se može rezervirati**, u polju **Vrsta resursa**, odaberite jednu od sljedećih mogućnosti:

    - **Korisnik** – Odaberite ovu vrstu resursa ako podizvođač mora pristupiti rješenju Project Operations za unos vremena ili troškova. Ako odaberete **Korisnik**, podizvođač treba valjanu licencu za pristup sustavu.
    - **Kontakt** ili **Račun** – Odaberite jednu od ovih vrsta resursa ako podizvođač ne treba pristup rješenju Project Operations, ali mora biti dostupan za dodjelu zadataka ili rezervacija na projektima. Nijedna od ovih vrsta resursa ne pruža pristup sustavu. Izaberite **Račun** za prikaz tvrtke dobavljača kao resursa koji se može rezervirati. Izaberite **Kontakt** za prikaz pojedinih zaposlenika dobavljača.

3. Ovisno o vrsti resursa koju ste odabrali, od vas će se tražiti da odaberete odgovarajući zapis korisnika, računa ili kontakta.
4. U polju **Vrsta radnika**, odaberite stavku „Ugovorni radnik” za postavljanje podizvođača kao resursa koji se može rezervirati.

    > [!NOTE]
    > Ako polje **Vrsta radnika** ostavite prazno, resurs koji se može rezervirati smatrat će se zaposlenikom.

5. Ako ste kao vrstu radnika odabrali **Radnik po ugovoru**, odaberite dobavljača za kojeg resurs radi.
6. Odaberite vremensku zonu resursa, a zatim odaberite **Spremi**. Kako biste resursu koji se može rezervirati dodijelili predložak radnog vremena, možete odabrati **Postavi kalendar** na stranici popisa **Resurs koji se može rezervirati**.

Kako bi se resurs koji se može rezervirati povezao s retkom podugovora, on mora zadovoljiti ove uvjete:

- Resurs koji se može rezervirati mora biti radnik po ugovoru.
- Resurs vrste resursa **Kontakt**, koji se može rezervirati, mora biti povezan s računom dobavljača kao kontakt. Resurs vrste resursa **Korisnik**, koji se može rezervirati, ne mora biti povezan s računom dobavljača kao kontakt.
- Vrijednost polja **Dobavljač** resursa koji se može rezervirati mora se poklapati s vrijednosti polja **Dobavljač** polja za podugovor.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Ažuriranje vrste mapiranja radnika i dobavljača za resurse koji se mogu rezervirati

Polje **Vrsta radnika** za resurs koji se može rezervirati određuje je li resurs koji se može rezervirati radnik po ugovoru ili zaposlenik. Polje **Dobavljač** definira račun dobavljača s kojim je povezan resurs koji se može rezervirati. Povezivanjem resursa koji se može rezervirati s dobavljačem kao kontaktom naznačujete da je kontakt zaposlenik tvrtke dobavljača.

Ako se mijenjaju polja **Vrsta radnika** i **Dobavljač** za resurs koji se može rezervirati, promjene utječu na sve buduće provjere valjanosti novih zapisa koje stvara resurs koji se može rezervirati, kao što su vremenski unosi. Međutim, promjene ne poništavaju valjanost postojećih zapisa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
