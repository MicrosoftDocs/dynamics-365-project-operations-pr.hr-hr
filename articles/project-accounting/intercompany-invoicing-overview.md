---
title: Pregled fakturiranja unutar tvrtke
description: U ovoj temi nalaze se informacije i primjeri o načinu fakturiranja projekata unutar tvrtke.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42af89105f8325f1c94df6d2133d2c329facf2b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002632"
---
# <a name="intercompany-invoicing-overview"></a>Pregled fakturiranja unutar tvrtke

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Vaša tvrtka ili ustanova može imati više sektora, podružnica i drugih pravnih osoba koje međusobno prenose proizvode i usluge za projekte. Pravna osoba koja osigurava uslugu ili proizvod naziva se *pravna osoba koja kreditira*. Pravna osoba koja prima uslugu ili proizvod naziva se *pravna osoba koja se zadužuje*.

Na sljedećoj se ilustraciji prikazuje tipični scenarij kada dvije pravne osobe, Contoso Robotics SAD (pravna osoba koja se zadužuje) i Contoso Robotics UK (pravna osoba koja pozajmljuje), dijele resurse za isporuku projekta za klijenta Adventure works. Za ovaj scenarij, Contoso Robotics SAD unajmljen je za isporuku posla tvrtki Adventure Works.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]