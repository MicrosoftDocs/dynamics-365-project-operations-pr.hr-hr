---
title: Obrada računa za troškove
description: U ovoj se temi nalaze informacije o obradi optičkog prepoznavanja znakova (OCR, optical character recognition) za račune. Ova je funkcija dizajnirana za poboljšanje korisničkog iskustva kada je izvješće o troškovima stvoreno u aplikaciji Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 64901610144f9dfe274bd4c2294ab32659743a1a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960283"
---
# <a name="expense-receipt-processing"></a>Obrada računa za troškove

Unos troškova poboljšan je uvođenjem optičkog prepoznavanja znakova (OCR) za obradu računa. Ova je funkcija dizajnirana za poboljšanje korisničkog iskustva kada je stvoreno izvješće o troškovima.

## <a name="key-features"></a>Glavne značajke

- Ime trgovca, datum i ukupan iznos izdvojeni su iz računa.
- Značajka će pokušati povezati nevezane račune s nevezanim transakcijama troškova.
- Iz računa korisnici mogu stvoriti ručno unesene transakcije troškova.

## <a name="usage-examples"></a>Primjeri uporabe

Kako biste tijekom stvaranja izvješća o troškovima automatski priložili račune koji obuhvaćaju transakcije kreditnom karticom, napravite sljedeće:

  1. Otvorite radni prostor **Upravljanje troškovima**.
  2. Na kartici **Računi** provjerite postoje li nepovezani računi. Račune možete prenijeti i na karticu **Računi**.
  3. Na kartici **Troškovi** provjerite postoje li nepovezani troškovi. Administrator troškova uobičajeno uvozi te troškove od davatelja usluge kreditnih kartica.
  4. Odaberite **Novo izvješće o troškovima**. Primjećujete kako troškove i račune sada možete uključiti tijekom stvaranja izvješća o troškovima. Ako dodate i troškove i račune, aktivirat će se automatsko podudaranje računa i troškova.

Kako biste stvorili trošak ili uskladili trošak s računa, napravite sljedeće:

  1. Na izvješću o troškovima, na kartici **Računi**, račun priložite odabirom mogućnosti **Dodaj račune**.
  2. Ispod prenesene slike računa prikazuju se mogućnosti **Stvori** i **Uskladi**.

      - Odaberite mogućnost **Stvori** za stvaranje ručno unesene transakcije troškova i popunjavanje vrijednosti izvučenih iz računa.
      - Ako odaberete **Uskladi**, sustav pokušava postojeći trošak uskladiti s računom.

## <a name="installation"></a>Instalacija

Ova značajka radi u kombinaciji sa značajkom **Izmijenjena izvješća o trošku** za pojednostavljivanje iskustva s troškom. Ova je značajka dostupna samo za Razinu 2+ okruženja, a to su Sigurnosna ograda i Proizvodnja.

Kako biste upotrijebili ove napredne mogućnosti troškova, instalirajte dodatak Usluga upravljanja troškovima za Microsoft Dynamics 365 Finance i uključite značajke u svojoj instanci. Dodatku možete pristupiti iz svog projekta u aplikaciji Microsoft Dynamics Lifecycle Services(LCS).

1. Prijavite se na LCS i otvorite željeno okruženje.
2. Idite na **Potpune pojedinosti**.
3. Odaberite **Održavaj** ili se pomaknite dolje do Brze kartice **Dodaci za okruženje**.
4. Odaberite **Instaliraj novi dodatak**.
5. Odaberite **Usluga upravljanja troškovima**.
6. Slijedite vodič za instalaciju i prihvatite uvjete i odredbe.
7. Odaberite **Instaliraj**.

U radnom prostoru **Upravljanje značajkama** uključite sljedeće značajke:

- Izmijenjena izvješća o trošku
- Automatsko podudaranje i stvaranje troška iz računa

Kada uključite ove značajke, događaju se sljedeće radnje:

- Postojeći radni prostor **Upravljanje troškovima** zamjenjuje se novim radnim prostorom.
- Dodana je nova stavka izbornika za vidljivost polja troška.
- Još uvijek možete otvoriti prethodnu stranicu **Izvješća o troškovima** odlaskom na **Upravljanje troškovima > Moji troškovi > Izvješća o troškovima**.
- Tijekovi rada i sva odobrenja i dalje vas vode na postojeću stranicu izvješća o troškovima.
- Računi će se obrađivati putem aplikacije Microsoft Azure Cognitive Services, a izdvojit će se i dodati metapodaci.
- Dodana je mogućnost koja vam omogućuje stvaranje izvješća o troškovima koji obuhvaćaju podudarne nepovezane račune.
- Mogućnost koja se dodaje izvješćima o troškovima omogućuje vam stvaranje retka troška iz računa ili pokušaj usklađivanja postojećeg računa s postojećim retkom troška.

Dodatne informacija o izmijenjenoj značajci izvješća o troškovima potražite u odjeljku [Izmijenjena izvješća o troškovima](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Najčešća pitanja

**Koristi li Microsoft moje podatke za svoje modele?**

Ne, za svoju uslugu obrade računa Microsoft je stvorio opći model strojnog učenja. Ovaj se model ne temelji na računima koje ste prenijeli.

**Gdje je ova značajka dostupna i obrađena?**

Trenutačno je podržan SAD.

**Kamo idu moji računi?**

Financije će kontaktirati uslugu Cognitive Services radi izdvajanja podataka s terena. Cognitive Services zadržat će kopiju vašeg računa do 24 sata dok traje obrada. Nakon završetka obrade, Cognitive Services uklonit će račun. Računi se i dalje čuvaju u Financijama.

Dodatne informacije potražite u članku [Omogućivanje razumijevanja računa s novom mogućnosti prepoznavanja obrazaca](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]