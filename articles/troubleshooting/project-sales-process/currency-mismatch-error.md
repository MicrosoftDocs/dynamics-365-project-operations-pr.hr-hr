---
title: Pogreška nepodudarnosti valute
description: Ovaj tema pruža informacije o otklanjanju poteškoća s nepodudarnosti valute do koje dolazi prilikom spremanja određenih vrsta zapisa.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903641"
---
# <a name="currency-mismatch-error"></a>Pogreška nepodudarnosti valute 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Kada spremite projekt, ugovor, ponudu ili resurs koji se može rezervirati, možda ćete primiti pogrešku, **valuta vlasnika tvrtke ne odgovara valuti ugovorne jedinice. Odaberite drugo poduzeće ili ugovorna jedinica za nastavak**. To je zato što postoji nepodudaranje valute između valute ugovorne jedinice za zapis i valute poduzeća vlasnika.


## <a name="resolution"></a>Rješenje

Da biste zaobišli taj problem, učinite sljedeće:
- Provjerite valutu ugovorne jedinice za ovaj zapis. Valutu možete vidjeti otvaranjem zapisa organizacijske jedinice i provjerom vrijednosti na **kartici Općenito** u polju **Valuta**.
- Provjerite valutu vlasnika tvrtke. Valutu možete vidjeti tako **da** > **odete u Povezane knjige** u zapisu poduzeća. Dvokliknite zapis analitike povezan s poduzećem i provjerite vrijednost na **kartici Općenito** u polju **Računovodstvena** valuta.

Ako se valuta postavljena u jedinici ugovaranja i zapisu analitike ne podudaraju, prilagodite konfiguraciju ili odaberite različite vrijednosti prilikom spremanja zapisa. Sustav zahtijeva da se ti zapisi podudaraju kako bi se osigurali ispravni međukompanijski tokovi fakturiranja. Dodatne informacije o međukompanijskim konfiguracijama potražite u [članku Kreiranje međukompanijskih transakcija](../../project-accounting/create-intercompany-transactions.md).

Ako zapis poduzeća nema pridruženi zapis analitike, to znači da prilikom postavljanja okruženja nedostaje konfiguracija. Konfiguraciju mora ispraviti administrator sustava. Administrator sustava mora otići u **konfiguracije dvostrukog pisanja** i zaustaviti i ponovno pokrenuti **mapu dvostrukog pisanja Ledgers** s početnom sinkronizacijom ove karte i preduvjetima. Dodatne informacija potražite u odjeljku [Verzije karte s dvostrukim upisivanjem aplikacije Project Operations](../../environment/resource-dual-write-maps.md).
