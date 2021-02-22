---
title: Pregled fakturiranja unutar tvrtke
description: U ovoj temi nalaze se informacije i primjeri o načinu fakturiranja projekata unutar tvrtke.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595439"
---
# <a name="intercompany-invoicing-overview"></a>Pregled fakturiranja unutar tvrtke

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Vaša tvrtka ili ustanova može imati više sektora, podružnica i drugih pravnih osoba koje međusobno prenose proizvode i usluge za projekte. Pravna osoba koja osigurava uslugu ili proizvod naziva se *pravna osoba koja kreditira*. Pravna osoba koja prima uslugu ili proizvod naziva se *pravna osoba koja se zadužuje*.

Sljedeća ilustracija prikazuje uobičajeni scenarij u kojem dvije pravne osobe, Contoso Robotics USA (pravna osoba koja se zadužuje) i Contoso Robotics UK (pravna osoba koja kreditira) dijele resurse kako bi se isporučio projekt kupcu, Adventure works. Za ovaj scenarij unajmljena je tvrtka Contoso Robotics USA da posao isporuči tvrtki Adventure Works.

![Fakturiranje unutar tvrtke](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations upotrebljava sljedeći tijek za obradu transakcija unutar tvrtke:

1. Resursi iz pravne osobe koja kreditira bilježe transakcije vremena ili troška unutar tvrtke rezervirajući vrijeme i trošak za projekte u pravnoj osobi koja se zadužuje.
2. Troškovi vremena i koštanja zapisuju se u tvrtku koja kreditira s pomoću cjenika troškova jedinice tvrtke koja se zadužuje.
3. Prodajne transakcije nenaplaćene unutar tvrtke evidentiraju se u tvrtku koja kreditira s pomoću cjenika troškova jedinice tvrtke koja se zadužuje.
4. Nenaplaćeni prihod evidentira se u tvrtki koja se zadužuje s pomoću prodajnog cjenika ugovora o projektu. Klijentu se može naplatiti kada se evidentira nefakturirani prihod. Klijent ne mora čekati završetak obrade fakture unutar tvrtke.
5. Fakture za klijenta unutar tvrtke stvaraju se periodično u tvrtki koja kreditira. Fakture se stvaraju ručno ili uporabom periodičnog automatiziranog postupka. Za svaku pravnu osobu koja se zadužuje može se stvoriti pojedinačna faktura ili projekt može stvoriti zasebne fakture.
6. Kada se račun za klijenta unutar tvrtke knjiži u pravnoj osobi koja kreditira, u pravnoj osobi koja se zadužuje stvara se odgovarajuća faktura dobavljača na čekanju. Troškovi na fakturi dobavljača na čekanju evidentirat će se u sporednoj knjizi projekta kada se faktura proknjiži.

Sljedeći dijagram ilustrira fakturiranje unutar tvrtke koje se odnosi na računovodstvene događaje i očekivana knjiženja u glavnu knjigu.

![Tijek rada unutar tvrtke](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Dodatni resursi

- [Konfiguriranje fakturiranja unutar tvrtke](configure-intercompany-invoicing.md)
- [Bilježenje transakcija unutar tvrtke](create-intercompany-transactions.md)
- [Stvaranje faktura klijenta i dobavljača unutar tvrtke](create-intercompany-customer-vendor-invoices.md)