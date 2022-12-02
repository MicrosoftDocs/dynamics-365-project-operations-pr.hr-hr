---
title: Pregled stvarnih podataka
description: U ovom se članku navode informacije o stvarnim podacima projekta.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: overview
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 35282e6c51fff28dbbb0a5a7de760788416ed0e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929067"
---
# <a name="actuals-overview"></a>Pregled stvarnih podataka

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Stvarne vrijednosti su količina dovršenog posla na projektu. Stvarne vrijednosti projekta mogu se pratiti natrag do njihovih izvornih dokumenata. Ti izvorni dokumenti uključuju unose vremena, izdataka i dnevnika, a također i faktura.

![Kako se stvarne vrijednosti projekta prate do izvornih dokumenata.](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Slanje unosa vremena

U aplikaciji PSA, kada se šalje unos vremena za projekt koji je mapiran u redak ugovora vremena i materijala, izrađuju se dva retka u dnevniku. Jedan redak je za trošak, a drugi redak je za nenaplaćenu prodaju. Kada se unos vremena šalje za projekt koji je mapiran u redak ugovora fiksne cijene, redak u dnevniku izrađuje se samo za trošak. 

Logika za unos zadanih cijena temelji se na retku u dnevniku. Sve vrijednosti polja iz unosa vremena kopiraju se u redak u dnevniku. Ta polja uključuju datum transakcije, redak ugovora u koji je projekt mapiran i rezultat valute na odgovarajućem cjeniku. 

Polja koja utječu na zadane cijene, kao što su **Uloga** i **Org jedinica** uzrokuju odgovarajuću cijenu koja se prema zadanim postavkama unosi u redak u dnevniku. Ako u unos vremena dodate prilagođeno polje, a želite da se vrijednost polja propagira do stvarnih vrijednosti, izradite polje u entitetu Stvarne vrijednosti i koristite mapiranja polja da biste kopirali polje iz unosa vremena u stvarnu vrijednost.

## <a name="submitting-an-expense-entry"></a>Slanje unosa izdatka

U aplikaciji PSA, kada se šalje unos izdatka za projekt koji je mapiran u redak ugovora vremena i materijala, izrađuju se dva retka u dnevniku. Jedan redak je za trošak, a drugi redak je za nenaplaćenu prodaju. Kada se šalje unos izdatka za projekt koji je mapiran u redak ugovora fiksne cijene, izrađuje se redak u dnevniku samo za trošak.

Logika za unos zadanih cijena za izdatke temelji se na kategoriji troška koja se odabire na stranici **Unos izdataka**. Datum transakcije, redak ugovora u kojem je projekt mapiran i valuta koriste se za određivanje odgovarajućeg cjenika. Međutim, za samu cijenu, iznos koji je korisnik unio postavljen je izravno na povezane retke u dnevniku za izdatak i prodaju prema zadanim postavkama.

U trenutačnoj verziji aplikacije PSA, unos zadanih cijena po jedinici koji se temelji na kategoriji u unosima troška nije dostupan.

## <a name="using-entry-journals-to-record-costs"></a>Uporaba dnevnika unosa za zapis troškova

U aplikaciji PSA, dnevnici unosa služe za zapis troškova ili prihoda u razredima materijala, naknade, vremena, troška ili porezne transakcije. Dnevnik ima zaglavlje, retke i radnju **Potvrdi**. Evo nekih scenarija u kojima biste mogli koristiti dnevnik:

- Morate zapisati stvarne troškove materijala i prodaju na projektu.
- Morate premještati stvarne vrijednosti transakcije iz drugog sustava u aplikaciju PSA.
- Morate zapisati troškove koji su se pojavili u drugom sustavu, kao što su troškovi nabave ili podugovaranja.

> [!IMPORTANT]
> Uporabu dnevnika unosa za stvaranje stvarnih podataka trebao bi napraviti samo korisnik koji je u potpunosti svjestan računovodstvenog utjecaja koje stvarni podaci imaju na projekt. To je zato što aplikacija ne provjerava valjanost vrste retka u dnevniku ili povezanu cijenu koja je unesena u redak dnevnika. Zbog utjecaja ovog tipa dnevnika, budite dovoljno oprezni kada drugima omogućujete pristup stvaranju dnevnika unosa.     


## <a name="recording-actuals-based-on-project-events"></a>Zapis stvarnih vrijednosti na temelju projektnih događaja

PSA zapisuje financijske transakcije koje se odvijaju tijekom projekta. Te se transakcije zapisuju kao **stvarne vrijednosti**. Sljedeće tablice prikazuju različite vrste stvarnih vrijednosti koje se izrađuju, ovisno o tome radi li se o projektu s vremenom i materijalima ili o projektu s fiksnom cijenom, o projektu u fazi pretprodaje ili o internom projektu.

**Resurs pripada istoj organizacijskoj jedinici kao i ugovorna jedinica projekta**

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

**Resurs pripada organizacijskoj jedinici koja se razlikuje od ugovorne jedinice projekta**

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
