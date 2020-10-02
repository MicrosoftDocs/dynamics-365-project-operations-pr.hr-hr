---
title: Usklađivanje računa i troška s pomoću OCR-a
description: U ovoj se temi nalaze informacije o obradi optičkog prepoznavanja znakova (OCR, optical character recognition) za račune.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896992"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a>Usklađivanje računa i troška s pomoću OCR-a

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Unos troškova poboljšan je uvođenjem optičkog prepoznavanja znakova (OCR) za obradu računa. Ova je funkcija dizajnirana za poboljšanje korisničkog iskustva tijekom izrade izvješća o troškovima.

## <a name="key-features"></a>Glavne značajke

- Sustav iz računa izdvaja ime trgovca, datum i ukupan iznos.
- Sustav će pokušati povezati nevezane račune s nevezanim transakcijama troškova.
- Iz računa možete stvoriti ručno unesene transakcije troškova.

## <a name="attach-receipts-to-an-expense-report"></a>Računi priloženi izvješću o troškovima

Kako biste tijekom stvaranja izvješća o troškovima automatski priložili račune koji obuhvaćaju transakcije kreditnom karticom, izvršite sljedeće korake.

  1. Otvorite radni prostor **Upravljanje troškovima**.
  2. Na kartici **Računi** provjerite postoje li nepovezani računi. Račune možete prenijeti i na karticu **Računi**.
  3. Na kartici **Troškovi** provjerite postoje li nepovezani troškovi. Administrator troškova uobičajeno uvozi te troškove od davatelja usluge kreditnih kartica.
  4. Odaberite **Novo izvješće o troškovima**. Primjećujete kako troškove i račune sada možete uključiti tijekom stvaranja izvješća o troškovima. Ako dodate i troškove i račune, aktivirat će se automatsko podudaranje računa i troškova.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Stvaranje i podudaranje računa s izvješćem o troškovima
Kako biste stvorili trošak ili uskladili trošak s računa, poduzmite sljedeće korake.

  1. Na izvješću o troškovima, na kartici **Računi**, račun priložite odabirom mogućnosti **Dodaj račune**.
  2. Ispod prenesene slike računa prikazuju se mogućnosti **Stvori** i **Uskladi**.

      - Odaberite mogućnost **Stvori** za stvaranje ručno unesene transakcije troškova i popunjavanje vrijednosti izvučenih iz računa.
      - Ako odaberete **Uskladi**, sustav pokušava postojeći trošak uskladiti s računom.

## <a name="installation"></a>Instalacija

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

## <a name="frequently-asked-questions"></a>Najčešća pitanja

**Koristi li Microsoft moje podatke za svoje modele?**

Ne, za svoju uslugu obrade računa Microsoft je stvorio opći model strojnog učenja. Ovaj se model ne temelji na računima koje ste prenijeli.

**Gdje je ova značajka dostupna i obrađena?**

Trenutačno je podržan SAD.

**Kamo idu moji računi?**

Financije će kontaktirati uslugu Cognitive Services radi izdvajanja podataka s terena. Cognitive Services zadržat će kopiju vašeg računa do 24 sata dok traje obrada. Nakon završetka obrade, Cognitive Services uklonit će račun. Računi se i dalje čuvaju u Financijama.

Dodatne informacije potražite u članku [Omogućivanje razumijevanja računa s novom mogućnosti prepoznavanja obrazaca](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
