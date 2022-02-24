---
title: Stvarni podaci
description: U ovoj temi nalaze se informacije o radu sa stvarnim podacima u aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852535"
---
# <a name="actuals"></a>Stvarni podaci 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Stvarni podaci predstavljaju pregledani i odobreni financijski napredak i napredak rasporeda na projektu. Stvoreni su kao rezultat odobravanja unosa vremena, troškova, utrošenog materijala te unosa i faktura dnevnika.

## <a name="journal-lines-and-time-submission"></a>Redci temeljnice i prijavljivanje vremena

Dodatne informacije o unosu vremena potražite u odjeljku [Pregled unosa vremena](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Vrijeme i materijali

Kada je poslani unos vremena povezan s projektom koji je mapiran u redak ugovora za vrijeme i materijal, sustav stvara dva retka temeljnice, jedan za troškove i drugi za nenaplaćenu prodaju.

### <a name="fixed-price"></a>Fiksna cijena

Kada je poslani unos vremena povezan s projektom koji je mapiran u redak ugovora s nepromjenjivom cijenom, sustav stvara jedan redak u temeljnici za trošak.

### <a name="default-pricing"></a>Zadano određivanje cijene

Logika za stvaranje zadanih cijena temelji se na retku temeljnice. Vrijednosti polja iz unosa vremena kopiraju se u redak temeljnice. Te vrijednosti uključuju datum transakcije, redak ugovora u koji je projekt mapiran i rezultat valute na odgovarajućem cjeniku.

Polja koja utječu na zadane cijene, kao što su **Uloga** i **Jedinica resursa** upotrebljavaju se za određivanje odgovarajuće cijene u redak u dnevniku. Na unos vremena možete dodati prilagođeno polje. Ako želite da se vrijednost polja proširi na stvarne podatke, stvorite polje u tablicama **Stvarni podaci** i **Redak dnevnika**. Upotrijebite prilagođeni kôd za širenje odabrane vrijednosti polja iz Vremenskog unosa u Stvarne podatke putem retka dnevnika s pomoću izvora transakcija. Dodatne informacija o izvorima transakcija i vezama potražite u odjeljku [Povezivanje stvarnih podataka s izvornim zapisima](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Redci temeljnice i slanje osnovnih troškova

Dodatne informacije o unosu troška potražite u odjeljku [Pregled unosa troška](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Vrijeme i materijali

Kada je poslani unos osnovnog troška povezan s projektom koji je mapiran u redak ugovora za vrijeme i materijal, sustav stvara dva retka temeljnice, jedan za troškove i drugi za nenaplaćenu prodaju.

### <a name="fixed-price"></a>Fiksna cijena

Kada je prijavljeni osnovni unos troška povezan s projektom koji je mapiran u redak ugovora s fiksnom cijenom, sustav stvara jedan redak u dnevniku za trošak.

### <a name="default-pricing"></a>Zadano određivanje cijene

Logika unošenja zadanih cijena za troškove temelji se na kategoriji troškova. Datum transakcije, redak ugovora u kojem je projekt mapiran i valuta koriste se za određivanje odgovarajućeg cjenika. Polja koja utječu na zadane cijene, kao što su **Kategorija transakcije** i **Jedinica** upotrebljavaju se za određivanje odgovarajuće cijene u redak u dnevniku. Međutim, to djeluje samo kada je način određivanja cijene u cjeniku **Cijena po jedinici**. Ako je način određivanja cijene **Prema trošku** ili **Provizija povrh troška**, cijena unesena kada se stvorio unos troška upotrebljava se za trošak, a cijena u retku dnevnika prodaje izračunava se na temelju načina za određivanje cijena. 

Na unos troška možete dodati prilagođeno polje. Ako želite da se vrijednost polja proširi na stvarne podatke, stvorite polje u tablicama **Stvarni podaci** i **Redak dnevnika**. Upotrijebite prilagođeni kôd za širenje odabrane vrijednosti polja iz Vremenskog unosa u Stvarne podatke putem retka dnevnika s pomoću izvora transakcija. Dodatne informacija o izvorima transakcija i vezama potražite u odjeljku [Povezivanje stvarnih podataka s izvornim zapisima](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Redci dnevnika i slanje zapisnika o utrošenom materijalu

Dodatne informacije o unosu troškova potražite u odjeljku [Zapisnik o utrošenom materijalu](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Vrijeme i materijali

Kada je prijavljeni zapisnik o utrošenom materijalu povezan s projektom koji je mapiran na redak ugovora o vremenu i materijalima, sustav stvara dva retka dnevnika, jedan za trošak i jedan za nenaplaćenu prodaju.

### <a name="fixed-price"></a>Fiksna cijena

Kada je prijavljeni unos zapisnika o utrošenom materijalu povezan s projektom koji je mapiran u redak ugovora s fiksnom cijenom, sustav stvara jedan redak u dnevniku za trošak.

### <a name="default-pricing"></a>Zadano određivanje cijene

Logika unošenja zadanih cijena materijala temelji se na kombinaciji proizvoda i jedinice. Datum transakcije, redak ugovora u kojem je projekt mapiran i valuta koriste se za određivanje odgovarajućeg cjenika. Polja koja utječu na zadane cijene, kao što su **ID proizvoda** i **Jedinica** upotrebljavaju se za određivanje odgovarajuće cijene u redak u dnevniku. Međutim, ovo vrijedi samo za kataloške proizvode. Za proizvode koji se umeću, cijena unesena kada se stvarao unos zapisnika o utrošenom materijalu upotrebljava se za cijenu troška i prodajnu cijenu u redcima dnevnika. 

Na unos **Zapisnik o utrošenom materijalu** možete dodati prilagođeno polje. Ako želite da se vrijednost polja proširi na stvarne podatke, stvorite polje u tablicama **Stvarni podaci** i **Redak dnevnika**. Upotrijebite prilagođeni kôd za širenje odabrane vrijednosti polja iz Vremenskog unosa u Stvarne podatke putem retka dnevnika s pomoću izvora transakcija. Dodatne informacija o izvorima transakcija i vezama potražite u odjeljku [Povezivanje stvarnih podataka s izvornim zapisima](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Uporaba temeljnica za unos za bilježenje troškova

Temeljnice za unos možete upotrebljavati za bilježenje troška ili prihoda u razredima materijala, naknade, vremena, troška ili porezne transakcije. Temeljnice se mogu upotrebljavati u sljedeće svrhe:

- Premjestite stvarne vrijednosti transakcije iz drugog sustava u aplikaciju Microsoft Dynamics 365 Project Operations.
- Bilježite troškove koji su se dogodili u drugom sustavu. Ti troškovi mogu uključivati troškove nabave ili podugovaranja.

> [!IMPORTANT]
> Aplikacija ne provjerava valjanost vrste retka temeljnice ili povezanog određivanja cijene koje se unosi u redak temeljnice. Stoga bi samo korisnik koji je potpuno svjestan računovodstvenog utjecaja koji stvarni podaci imaju na projekt trebao upotrebljavati temeljnice unosa za stvaranje stvarnih podataka. Zbog utjecaja ove vrste temeljnice, trebali biste pažljivo odabrati tko ima pristup za stvaranje temeljnica za unos.

## <a name="record-actuals-based-on-project-events"></a>Bilježenje stvarnih podataka na temelju projektnih događaja

Project Operations bilježi financijske transakcije koje se odvijaju tijekom projekta. Te se transakcije zapisuju kao stvarne vrijednosti. Sljedeće tablice prikazuju različite vrste stvarnih vrijednosti koje se izrađuju, ovisno o tome radi li se o projektu s vremenom i materijalima ili o projektu s fiksnom cijenom, o projektu u fazi pretprodaje ili o internom projektu.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Resurs pripada istoj organizacijskoj jedinici kao i ugovorna jedinica projekta

<table>
<thead>
<tr>
<th rowspan="3">Događaj</th>
<th colspan="4">Naplativi ili prodani projekt</th>
<th rowspan="3">Projekt u fazi pretprodaje</th>
<th rowspan="3">Interni projekt</th>
</tr>
<tr>
<th colspan="2">Vrijeme i materijali</th>
<th colspan="2">Fiksna cijena</th>
</tr>
<tr>
<th>Stvarne vrijednosti</th>
<th>Valuta transakcije</th>
<th>Fiksna cijena</th>
<th>Valuta transakcije</th>
</tr>
</thead>
<tbody>
<tr>
<td>Stvoren je unos vremena.</td>
<td colspan="6">Nema aktivnosti u entitetu Stvarne vrijednosti</td>
</tr>
<tr>
<td>Poslan je unos vremena.</td>
<td colspan="6">Nema aktivnosti u entitetu Stvarne vrijednosti</td>
</tr>
<tr>
<td rowspan="2">Vrijeme je odobreno i nema promjene ili povećanja u naplativim satima tijekom odobravanja.</td>
<td>Stvarna vrijednost troškova</td>
<td>Valuta ugovorne jedinice</td>
<td rowspan="2">Stvarna vrijednost troškova</td>
<td rowspan="2">Valuta ugovorne jedinice
<td rowspan="2">Stvarna vrijednost troškova</td>
<td rowspan="2">Stvarna vrijednost troškova</td>
</tr>
<tr>
<td>Stvarna vrijednost nenaplaćene prodaje – Naplativa</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td rowspan="3">Vrijeme je odobreno i dolazi do smanjenja u naplativim satima tijekom odobravanja.</td>
<td>Stvarna vrijednost troškova</td>
<td>Valuta ugovorne jedinice</td>
<td rowspan="3">Stvarna vrijednost troškova</td>
<td rowspan="3">Valuta ugovorne jedinice</td>
<td rowspan="3">Stvarna vrijednost troškova</td>
<td rowspan="3">Stvarna vrijednost troškova</td>
</tr>
<tr>
<td>Stvarna vrijednost nenaplaćene prodaje – Naplativa za novu količinu</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td>Stvarna vrijednost nenaplaćene prodaje – Nenaplativa za razliku</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td rowspan="2">Faktura je potvrđena i nema promjene ili povećanja u naplativim satima.</td>
<td>Preokret nenaplaćene prodaje</td>
<td>Valuta ugovora projekta</td>
<td rowspan="2">Naplaćena prodaja za ključnu točku</td>
<td rowspan="2">Valuta ugovora projekta</td>
<td rowspan="2">Nije primjenjivo</td>
<td rowspan="2">Nije primjenjivo</td>
</tr>
<tr>
<td>Naplaćena prodaja</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td rowspan="3">Faktura je potvrđena i dolazi do smanjenja u naplativim satima.</td>
<td>Preokret nenaplaćene prodaje</td>
<td>Valuta ugovora projekta</td>
<td rowspan="3">Nije primjenjivo</td>
<td rowspan="3">Nije primjenjivo</td>
<td rowspan="3">Nije primjenjivo</td>
<td rowspan="3">Nije primjenjivo</td>
</tr>
<tr>
<td>Naplaćena prodaja – Naplativa za novu količinu</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td>Naplaćena prodaja – Nenaplativa za razliku</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td rowspan="2">Faktura je ispravljena da bi se povećala naplativa količina.</td>
<td>Naplaćena prodaja – Preokret</td>
<td>Valuta ugovora projekta</td>
<td rowspan="5">
<ul>
<li>Preokret naplaćene prodaje za ključnu točku</li>
<li>Promjena statusa ključne točke iz <strong>Fakturirano</strong> u <strong>Spremno za fakturiranje</strong></li>
</ul>
</td>
<td rowspan="5">Valuta ugovora projekta</td>
<td rowspan="5">Nije primjenjivo</td>
<td rowspan="5">Nije primjenjivo</td>
</tr>
<tr>
<td>Naplaćena prodaja</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td rowspan="3">Faktura je ispravljena da bi se smanjila naplativa količina.</td>
<td>Naplaćena prodaja – Preokret</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td>Naplaćena prodaja za novu količinu</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td>Nenaplaćena prodaja – Naplativa za razliku</td>
<td>Valuta ugovora projekta</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Resurs pripada organizacijskoj jedinici koja se razlikuje od ugovorne jedinice projekta

<table>
<thead>
<tr>
<th rowspan="3">Događaj</th>
<th colspan="4">Naplativi ili prodani projekt</th>
<th rowspan="3">Projekt u fazi pretprodaje</th>
<th rowspan="3">Interni projekt</th>
</tr>
<tr>
<th colspan="2">Vrijeme i materijali</th>
<th colspan="2">Fiksna cijena</th>
</tr>
<tr>
<th>Stvarne vrijednosti</th>
<th>Valuta transakcije</th>
<th>Fiksna cijena</th>
<th>Valuta transakcije</th>
</tr>
</thead>
<tbody>
<tr>
<td>Stvoren je unos vremena.</td>
<td colspan="6">Nema aktivnosti u entitetu Stvarne vrijednosti</td>
</tr>
<tr>
<td>Poslan je unos vremena.</td>
<td colspan="6">Nema aktivnosti u entitetu Stvarne vrijednosti</td>
</tr>
<tr>
<td rowspan="4">Vrijeme je odobreno i nema promjene ili povećanja u naplativim satima tijekom odobravanja.</td>
<td>Stvarna vrijednost troškova</td>
<td>Valuta ugovorne jedinice</td>
<td rowspan="4">Stvarna vrijednost troškova</td>
<td rowspan="4">Valuta ugovorne jedinice</td>
<td rowspan="4">Stvarna vrijednost troškova</td>
<td rowspan="4">Stvarna vrijednost troškova</td>
</tr>
<tr>
<td>Stvarna vrijednost nenaplaćene prodaje – Naplativa</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td>Jedinična cijena resursa</td>
<td>Valuta resursne jedinice</td>
</tr>
<tr>
<td>Međuorganizacijska prodaja</td>
<td>Valuta ugovorne jedinice</td>
</tr>
<tr>
<td rowspan="5">Vrijeme je odobreno i dolazi do smanjenja u naplativim satima tijekom odobravanja.</td>
<td>Stvarna vrijednost troškova</td>
<td>Valuta ugovorne jedinice</td>
<td rowspan="5">Stvarna vrijednost troškova</td>
<td rowspan="5">Valuta ugovorne jedinice</td>
<td rowspan="5">Stvarna vrijednost troškova</td>
<td rowspan="5">Stvarna vrijednost troškova</td>
</tr>
<tr>
<td>Jedinična cijena resursa</td>
<td>Valuta resursne jedinice</td>
</tr>
<tr>
<td>Međuorganizacijska prodaja</td>
<td>Valuta ugovorne jedinice</td>
</tr>
<tr>
<td>Stvarna vrijednost nenaplaćene prodaje – Naplativa za novu količinu</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td>Stvarna vrijednost nenaplaćene prodaje – Nenaplativa za razliku</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td rowspan="2">Faktura je potvrđena i nema promjene ili povećanja u naplativim satima.</td>
<td>Preokret nenaplaćene prodaje</td>
<td>Valuta ugovora projekta</td>
<td rowspan="2">Naplaćena prodaja za ključnu točku</td>
<td rowspan="2">Valuta ugovora projekta</td>
<td rowspan="2">Nije primjenjivo</td>
<td rowspan="2">Nije primjenjivo</td>
</tr>
<tr>
<td>Naplaćena prodaja</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td rowspan="3">Faktura je potvrđena i dolazi do smanjenja u naplativim satima.</td>
<td>Preokret nenaplaćene prodaje</td>
<td>Valuta ugovora projekta</td>
<td rowspan="3">Nije primjenjivo</td>
<td rowspan="3">Nije primjenjivo</td>
<td rowspan="3">Nije primjenjivo</td>
<td rowspan="3">Nije primjenjivo</td>
</tr>
<tr>
<td>Naplaćena prodaja – Naplativa za novu količinu</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td>Naplaćena prodaja – Nenaplativa za razliku</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td rowspan="2">Faktura je ispravljena da bi se povećala naplativa količina.</td>
<td>Naplaćena prodaja – Preokret</td>
<td>Valuta ugovora projekta</td>
<td rowspan="5">
<ul>
<li>Preokret naplaćene prodaje za ključnu točku</li>
<li>Promjena statusa ključne točke iz <strong>Fakturirano</strong> u <strong>Spremno za fakturiranje</strong></li>
</ul>
</td>
<td rowspan="5">Valuta ugovora projekta</td>
<td rowspan="5">Nije primjenjivo</td>
<td rowspan="5">Nije primjenjivo</td>
</tr>
<tr>
<td>Naplaćena prodaja</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td rowspan="3">Faktura je ispravljena da bi se smanjila naplativa količina.</td>
<td>Naplaćena prodaja – Preokret</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td>Naplaćena prodaja za novu količinu</td>
<td>Valuta ugovora projekta</td>
</tr>
<tr>
<td>Nenaplaćena prodaja – Naplativa za razliku</td>
<td>Valuta ugovora projekta</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
