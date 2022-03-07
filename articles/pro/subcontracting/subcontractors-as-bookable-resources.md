---
title: Postavljanje podizvođača kao resursa koji se mogu rezervirati
description: U ovoj se temi objašnjava način za postavljanje i održavanje resursa podizvođača koje su stvorili korisnici i kontakti u sustavu, tako da se mogu povezati s podugovorima u aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c765e3c423e440f092c92f9bab75304914b0609447f1dc1c014f98801561b7a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994177"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Postavljanje podizvođača kao resursa koji se mogu rezervirati

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

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
