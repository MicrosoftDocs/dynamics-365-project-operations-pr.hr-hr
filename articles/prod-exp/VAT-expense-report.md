---
title: Povrat PDV-a
description: U ovom se članku objašnjava kako povratiti povrat novca za transakcije poreza na dodanu vrijednost (PDV).
author: saraschi2
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5798c11b4f7a9e49318cdab097746f21c2e81e2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934081"
---
# <a name="vat-recovery"></a>Povrat PDV-a 

Kako bi dobila povrat za prihvatljive transakcije poreza na dodanu vrijednost (PDV), tvrtka ili organizacija mora identificirati, prikupiti, provjeriti i dostaviti točne podatke. Ovaj postupak uključuje više zadataka i, ovisno o veličini vaše tvrtke, može uključivati nekoliko zaposlenika ili uloga.

Za povrat PDV-a s pomoću Upravljanja troškovima moraju se ispuniti sljedeći preduvjeti:

- Za zemlje/regije moraju se stvoriti porezni brojevi koji se raspoređuju u kategorije troškova.
- Za svaki porezni broj mora se stvoriti grupa poreza na promet.
- Za svaku grupu poreza na promet mora se stvoriti porezni broj.

Nakon što se ispune preduvjeti, zaposlenici slijede ove korake za traženje povrata za transakcije s PDV-om.

1. U izvješće o troškovima unesite porezne podatke o transakcijama kreditnom karticom kako biste identificirali prihvatljivi povrat PDV-a.
2. Uvjerite se kako su svi porezni podaci potpuni, a zatim proknjižite izvješće o troškovima.
3. Obradite troškove koji ispunjavaju uvjete za međunarodni povrat PDV-a.
4. Pošaljite podatke o povratu PDV-a neovisnom dobavljaču kako bi podnio međunarodne prijave povrata.
5. Troškovi postupka za povrat domaćeg PDV-a.

Sljedeći odjeljci pružaju primjere koji pokazuju kako zaposlenici tvrtke Contoso-a dovršavaju svaki korak.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>U izvješće o troškovima unesite porezne podatke o transakcijama kreditnom karticom kako biste identificirali prihvatljivi povrat PDV-a

Nancy, prodajna predstavnica tvrtke Contoso sa sjedištem u SAD-u, nedavno se vratila s prodajnog putovanja u Ujedinjenom Kraljevstvu. Tijekom putovanja imala je nekih osobnih troškova za obroke koji su plaćeni kreditnom karticom. Nancy sada mora izraditi izvješće o troškovima kako bi uskladila svoje troškove.

Kad Nancy unese podatke u izvješće o svojim troškovima, ona odabire **Ujedinjeno Kraljevstvo** u polju **Država/regija** na stranici **Uredi izvješće o troškovima**. Popis grupa poreza na promet zatim se filtrira tako da prikazuje samo grupe koje se odnose na Ujedinjeno Kraljevstvo. Nancy odabire grupu poreza na promet **Ujedinjeno Kraljevstvo 001** a zatim odabire stavku grupe poreza na promet **Obroci**. Nadalje, ona dodaje novu transakciju za svoj smještaj. Budući da u Ujedinjenom Kraljevstvu postoji samo jedna grupa poreza na promet i stavka grupe poreza na promet za smještaj, ti se podaci automatski popunjavaju u Nancynom izvješću o troškovima.

Prema pravilniku tvrtke Contoso, svi troškovi moraju imati odgovarajuće račune. Stoga, kada Nancy spremi izvješće o svojim troškovima, ona dobiva poruku u kojoj stoji da mora priložiti račun za svaku transakciju koju je navela u svom izvješću o troškovima. Nancy provjerava je li svom izvješću o troškovima dodala digitalnu sliku svakog računa o transakciji, a zatim svoje izvješće podnosi na odobrenje. Zatim šalje račune u papirnatom obliku pozadinskom timu za obradu. Ovaj će tim poslati podatke o povratu PDV-a neovisnom dobavljaču koji podnosi međunarodne prijave za povrat PDV-a za tvrtku Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Uvjerite se kako su svi porezni podaci potpuni, a zatim proknjižite izvješće o troškovima

April, koja je koordinator dugovanja tvrtke Contoso, mora unijeti sve porezne podatke koji joj nedostaju u izvješću o troškovima prije nego što se izvješće o troškovima može knjižiti. Ona otvara stranicu **Pojedinosti izvješća o troškovima** i vidi Nancyino odobreno izvješće o troškovima. April tada otvara izvješće o troškovima kako bi pregledala pojedinosti transakcija. Vidi da Nancy nije unijela stavku grupe poreza na promet niti za jednu transakciju. Budući da ove informacije nisu dostavljene, April ne može proknjižiti izvješće o troškovima. Stoga, ona gleda na stranicu **Porezne konfiguracije** u Upravljanju troškovima i pronalazi odgovarajuću grupu poreza na promet stavki za zemlju/regiju i vrstu transakcije. April sada može knjižiti izvješće o troškovima u glavnu knjigu.

Kada April proknjiži izvješće o troškovima, stvara se radna stavka povrata PDV-a. Ova radna stavka dodjeljuje se članu pozadinskog tima za obradu. April prima poruku koja potvrđuje da je knjiženje bilo uspješno. U ovoj se poruci također navodi broj transakcija s PDV-om koje su identificirane za povrat.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Obrađivanje troškova koji ispunjavaju uvjete za međunarodni povrat PDV-a

Arnie, član pozadinskog tima tvrtke Contoso za obradu, odgovoran je za potvrdu da su svi potrebni podaci za povrat PDV-a uključeni u izvješća o troškovima. Otvara stranicu **Povrat poreza za troškove** i odabire izvješće o troškovima koje je Nancy poslala. Zatim Arnie provjerava jesu li priloženi svi potrebni računi te jesu li unijete ispravne grupe poreza na promet i stavka broja poreza na promet.

Kada Arnie dobije papirnate račune od Nancy, provjerava papirnate u odnosu na digitalne račune, a zatim mijenja status izvješća o troškovima u **Spreman za povrat**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Pošaljite podatke o povratu PDV-a neovisnom dobavljaču kako bi podnio međunarodne prijave povrata

Kada je Arnie spreman poslati podatke izvješća o trošku neovisnom dobavljaču koji će podnijeti zahtjev za povrat PDV-a, on otvara stranicu **Povrat poreza za troškove**. Filtrira stranicu tako da prikazuje samo izvješća o troškovima koja su označena kao **Spremna za povrat**. Arnie zatim odabire **Datoteka** &gt; **Izvoz u Excel**. Podaci o PDV-u iz izvješća o troškovima izvoze se u radni list programa Microsoft Excel. Arnie predaje ovaj radni list neovisnom dobavljaču i uključuje poruku u kojoj se navodi da su računi poslani kurirskom službom.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Troškovi postupka za povrat domaćeg PDV-a

Arnie mora provjeriti jesu li transakcije izvješća o troškovima prihvatljive za povrat PDV-a i jesu li digitalni računi priloženi izvješćima. Kako bi počeo obrađivati prihvatljive troškove za domaći povrat, Arnie otvara stranicu **Povrat poreza za troškove** i odabire izvješće o troškovima koje treba provjeriti. Provjerava jesu li računi na ime tvrtke umjesto na zaposlenika. Za povrat PDV-a računi moraju biti na ime tvrtke. Arnie zatim potvrđuje da su primijenjeni ispravna grupa poreza na promet i šifra stavke poreza na promet.

Kad Arnie primi račune u papirnatom obliku, mijenja status izvješća o troškovima u **Spremno za povrat**. Tada prijavu može poslati odgovarajućem poreznom tijelu. U ovom je slučaju odgovarajuće porezno tijelo u SAD-u Služba internih prihoda (IRS, Internal Revenue Service).


[!INCLUDE[footer-include](../includes/footer-banner.md)]