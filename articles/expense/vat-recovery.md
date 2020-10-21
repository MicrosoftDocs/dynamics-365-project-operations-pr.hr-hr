---
title: Povrat PDV-a u upravljanju troškovima
description: U ovoj temi objašnjava se način povrata za prihvatljive transakcije poreza na dodanu vrijednost (PDV).
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 2c20e4a7fa9748e03bf1729fc2f7bdbfc2f292d1
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907968"
---
# <a name="vat-recovery-in-expense-management"></a>Povrat PDV-a u upravljanju troškovima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Kako bi dobila povrat za prihvatljive transakcije poreza na dodanu vrijednost (PDV), tvrtka ili organizacija mora identificirati, prikupiti, provjeriti i dostaviti točne podatke. Ovaj postupak uključuje više zadataka i, ovisno o veličini vaše tvrtke, može uključivati nekoliko zaposlenika ili uloga.

Za povrat PDV-a, u modulu **Upravljanje troškovima** moraju se ispuniti sljedeći preduvjeti:

- Za zemlje/regije moraju se stvoriti porezni brojevi koji se raspoređuju u kategorije troškova.
- Za svaki porezni broj mora se stvoriti grupa poreza na promet.
- Za svaku grupu poreza na promet mora se stvoriti porezni broj.

Nakon što se ispune preduvjeti, moraju se poduzeti sljedeći koraci za traženje povrata za transakcije s PDV-om.

1. U izvješće o troškovima unesite porezne podatke o transakcijama kreditnom karticom kako biste identificirali prihvatljivi povrat PDV-a.
2. Provjerite jesu li svi porezni podaci potpuni, a zatim proknjižite izvješće o troškovima.
3. Obradite troškove koji ispunjavaju uvjete za međunarodni povrat PDV-a.
4. Pošaljite podatke o povratu PDV-a neovisnom dobavljaču kako bi podnio međunarodne prijave povrata.
5. Troškovi postupka za povrat domaćeg PDV-a.

Sljedeći odjeljci pružaju primjere koji pokazuju kako zaposlenici tvrtke Contoso-a dovršavaju svaki korak.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Unesite porezne podatke o transakcijama kreditnom karticom kako biste identificirali prihvatljivi povrat PDV-a.

Nancy, prodajna predstavnica tvrtke Contoso sa sjedištem u SAD-u, nedavno se vratila s prodajnog putovanja u Ujedinjenom Kraljevstvu. Tijekom putovanja Nancy je imala nekih osobnih troškova za obroke koji su plaćeni kreditnom karticom. Nancy sada mora izraditi izvješće o troškovima kako bi uskladila troškove.

Kad Nancy unese podatke u izvješće o troškovima, ona odabire **Ujedinjeno Kraljevstvo** u polju **Država/regija** na stranici **Uredi izvješće o troškovima**. Popis grupa poreza na promet zatim se filtrira tako da prikazuje samo grupe koje se odnose na Ujedinjeno Kraljevstvo. Nancy odabire grupu poreza na promet **Ujedinjeno Kraljevstvo 001** a zatim odabire stavku grupe poreza na promet **Obroci**. Nadalje, Nancy dodaje novu transakciju za smještaj. Budući da u Ujedinjenom Kraljevstvu postoji samo jedna grupa poreza na promet i jedna stavka grupe poreza na promet za smještaj, ti se podaci automatski popunjavaju u Nancyinom izvještaju o troškovima.

Prema pravilniku tvrtke Contoso, svi troškovi moraju imati odgovarajuće račune. Stoga, kada Nancy spremi izvješće o troškovima, ona dobiva poruku u kojoj stoji da mora priložiti račun za svaku transakciju koju je navela u svom izvješću o troškovima. Nancy provjerava je li svom izvješću o troškovima dodala digitalnu sliku svakog računa o transakciji, a zatim svoje izvješće podnosi na odobrenje. Zatim šalje račune u papirnatom obliku pozadinskom timu za obradu. Ovaj će tim poslati podatke o povratu PDV-a neovisnom dobavljaču koji podnosi međunarodne prijave za povrat PDV-a za tvrtku Contoso.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Provjera valjanosti poreznih podataka i knjiženje izvješća o troškovima

Prije nego što April, koja je koordinator dugovanja tvrtke Contoso, proknjiži izvješće o troškovima, mora unijeti sve porezne podatke koji joj nedostaju. Ona otvara stranicu **Pojedinosti izvješća o troškovima** i vidi Nancyino odobreno izvješće o troškovima. April tada otvara izvješće o troškovima kako bi pregledala pojedinosti transakcija. Vidi da Nancy nije unijela stavku grupe poreza na promet niti za jednu transakciju. Budući da ove informacije nisu dostavljene, April ne može proknjižiti izvješće o troškovima. Stoga, ona gleda na stranicu **Porezne konfiguracije** u Upravljanju troškovima i pronalazi odgovarajuću grupu poreza na promet stavki za zemlju/regiju i vrstu transakcije. April sada može knjižiti izvješće o troškovima u glavnu knjigu.

Kada April proknjiži izvješće o troškovima, stvara se radna stavka povrata PDV-a. Ova radna stavka dodjeljuje se članu pozadinskog tima za obradu. April prima poruku koja potvrđuje da je knjiženje bilo uspješno. U ovoj se poruci također navodi broj transakcija s PDV-om koje su identificirane za povrat.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Obrađivanje troškova koji ispunjavaju uvjete za međunarodni povrat PDV-a

Arnie, član pozadinskog tima tvrtke Contoso za obradu, odgovoran je za provjeru jesu li svi potrebni podaci za povrat PDV-a uključeni u izvješća o troškovima. Otvara stranicu **Povrat poreza za troškove** i odabire izvješće o troškovima koje je Nancy poslala. Zatim Arnie provjerava jesu li priloženi svi potrebni računi te jesu li unijete ispravne grupe poreza na promet i stavka broja poreza na promet.

Kada Arnie dobije papirnate račune od Nancy, provjerava ih u odnosu na digitalne račune, a zatim mijenja status izvješća o troškovima u **Spreman za povrat**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Slanje podataka o povratu PDV-a neovisnom dobavljaču

Kada je Arnie spreman poslati podatke izvješća o trošku neovisnom dobavljaču koji će podnijeti zahtjev za povrat PDV-a, on otvara stranicu **Povrat poreza za troškove**. Filtrira stranicu tako da prikazuje samo izvješća o troškovima koja su označena kao **Spremna za povrat**. Arnie zatim odabire **Datoteka** &gt; **Izvoz u Excel**. Podaci o PDV-u iz izvješća o troškovima izvoze se u radni list programa Microsoft Excel. Arnie predaje ovaj radni list neovisnom dobavljaču i uključuje poruku u kojoj se navodi da su računi poslani kurirskom službom.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Troškovi postupka za povrat domaćeg PDV-a

Arnie mora provjeriti jesu li transakcije izvješća o troškovima prihvatljive za povrat PDV-a i jesu li digitalni računi priloženi izvješćima. Kako bi počeo obrađivati prihvatljive troškove za domaći povrat, Arnie otvara stranicu **Povrat poreza za troškove** i odabire izvješće o troškovima koje treba provjeriti. Provjerava jesu li računi na ime tvrtke umjesto na zaposlenika. (Za povrat PDV-a računi moraju biti naslovljeni na naziv tvrtke). Zatim Arnie provjerava jesu li priloženi svi potrebni računi te jesu li unijete ispravne grupe poreza na promet i stavka broja poreza na promet.

Kad Arnie primi račune u papirnatom obliku, mijenja status izvješća o troškovima u **Spremno za povrat**. Tada prijavu može poslati odgovarajućem poreznom tijelu. U ovom je slučaju odgovarajuće porezno tijelo u SAD-u Služba internih prihoda (IRS, Internal Revenue Service).
