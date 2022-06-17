---
title: Pogreška nepodudarnosti valute
description: U ovom se članku nalaze informacije o otklanjanju poteškoća s pogreškom u nepodudarnosti valute do koje dolazi prilikom spremanja određenih vrsta zapisa.
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
# <a name="currency-mismatch-error"></a>Pogreška nepodudarnosti valute 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Kada spremite projekt, ugovor, ponudu ili resurs koji se može rezervirati, možda ćete primijetiti pogrešku, **Valuta vlasnika poduzeća ne odgovara valuti ugovorne jedinice. Za nastavak odaberite drugo poduzeće ili ugovornu jedinicu**. To je zato što postoji nepodudarnost valute između valute ugovorne jedinice za zapis i valute vlasničkog poduzeća.


## <a name="resolution"></a>Rješenje

Da biste zaobišli taj problem, učinite sljedeće:
- Provjerite valutu ugovorne jedinice za ovaj zapis. Valutu možete vidjeti tako da otvorite zapis organizacijske jedinice i potvrdite vrijednost na **kartici Općenito** u **polju Valuta**.
- Provjerite valutu vlastitog poduzeća. Valutu možete vidjeti tako da u zapisu poduzeća otvorite **Povezane** > **knjige**. Dvokliknite zapis analitike povezan s poduzećem i provjerite vrijednost na **kartici Općenito** u **polju Obračunska valuta**.

Ako se valuta postavljena u ugovornoj jedinici i zapisu analitike ne podudaraju, prilagodite konfiguraciju ili odaberite različite vrijednosti prilikom spremanja zapisa. Sustav zahtijeva da se ti zapisi podudaraju kako bi se osigurali ispravni tokovi međukompanijskog fakturiranja. Dodatne informacije o međukompanijskim konfiguracijama potražite u članku [Stvaranje međukompanijskih](../../project-accounting/create-intercompany-transactions.md) transakcija.

Ako zapis o poduzeću nema pridruženi zapis o glavnoj knjizi, to znači da prilikom postavljanja okruženja nedostaje konfiguracija. Konfiguraciju mora ispraviti administrator sustava. Administrator sustava mora otići na **konfiguracije dvostrukog pisanja** i zaustaviti i ponovno pokrenuti **mapu dvostrukog pisanja** Ledgers s početnom sinkronizacijom ove karte i to su preduvjeti. Dodatne informacija potražite u odjeljku [Verzije karte s dvostrukim upisivanjem aplikacije Project Operations](../../environment/resource-dual-write-maps.md).
