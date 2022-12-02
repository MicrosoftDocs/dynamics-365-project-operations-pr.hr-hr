---
title: Pogreška nepodudaranja valute
description: U ovom se članku navode informacije o rješavanju problema u vezi s pogreškom nepodudaranja valute koja se javlja kada spremite određene vrste zapisa.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914715"
---
# <a name="currency-mismatch-error"></a>Pogreška nepodudaranja valute 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Kada spremite projekt, ugovor, ponudu ili resurs koji se može rezervirati, može vam se pojaviti pogreška **Valuta tvrtke vlasnice ne podudara se s valutom ugovorne jedinice. Odaberite drugu tvrtku vlasnicu ili ugovornu jedinicu da biste nastavili**. Uzrok te pogreške je neusklađenost valute između valute koju ugovorna jedinica upotrebljava za evidenciju i valute tvrtke vlasnice.


## <a name="resolution"></a>Rješenje

Da biste zaobišli ovaj problem, učinite jedno od sljedećeg:
- Provjerite valutu ugovorne jedinice za ovaj zapis. Valutu možete vidjeti otvaranjem zapisa organizacijske jedinice i provjerom vrijednosti na kartici **Općenito** u polju **Valuta**.
- Potvrdite valutu tvrtke vlasnice. Valutu možete vidjeti tako da u evidenciji tvrtke odete na **Povezano** > **Glavne knjige**. Dvaput kliknite zapis glavne knjige koji je povezan s tvrtkom i potvrdite vrijednost na kartici **Općenito** u polju **Računovodstvena valuta**.

Ako se valuta postavljena za ugovornu jedinicu i zapis glavne knjige ne podudaraju, prilagodite konfiguraciju ili odaberite različite vrijednosti kada spremite zapis. Sustav zahtijeva podudaranje tih zapisa kako bi se osigurali ispravni tokovi fakturiranja među tvrtkama. Više informacija o konfiguracijama unutar tvrtke potražite u članku [Izrada transakcija unutar tvrtke](../../project-accounting/create-intercompany-transactions.md).

Ako zapis tvrtke nema povezani zapis glavne knjige, to znači da je prilikom postavljanja okruženja nedostajala konfiguracija. Administrator sustava mora ispraviti konfiguraciju. Administrator sustava mora otići na **Konfiguracije dvostrukog zapisivanja** te zaustaviti i ponovno pokrenuti značajku **Karta dvojnog zapisivanja glavnih knjiga** s početnom sinkronizacijom ove karte i njezinim preduvjetima. Dodatne informacija potražite u odjeljku [Verzije karte s dvostrukim upisivanjem aplikacije Project Operations](../../environment/resource-dual-write-maps.md).
