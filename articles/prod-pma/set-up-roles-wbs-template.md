---
title: Postavljanje uloga na predlošcima strukturne analize rada
description: U ovom se članku nalaze informacije o postavljanju informacija o ulozi u predlošcima strukture raščlambe rada.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8721c5e5798c2b80c6f3eb65cef118d1ade5e680
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920787"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Postavljanje uloga na predlošcima strukturne analize rada

[!include [banner](../includes/banner.md)]

Upravitelji projekata mogu postaviti predloške strukturne analize rada (WBS, Work breakdown structure) koje mogu primijeniti tijekom stvaranja WBS-a za nove projekte. Kada stvaraju predložak voditelji projekata mogu dodati uloge. Upotrijebite sljedeći postupak za dodjeljivanje uloge WBS predlošku.

1. Odaberite **Upravljanje projektima i računovodstvo** > **Postavke** > **Projekti** > **Predlošci strukturne analize rada**.
2. Odaberite **Pojedinosti** za odabrani WBS predložak.
3. Na popisu odaberite zadatak, a zatim u polju **Uloga**, odaberite ulogu koju ćete dodijeliti zadatku.

## <a name="work-with-a-wbs"></a>Rad s WBS-om

Možete stvoriti novi WBS ili ga kopirati iz postojećeg WBS predloška. Voditelj projekta može lako upravljati resursima dodjeljivanjem uloga novim zadacima na WBS-u. Uloge se mogu zamijeniti, ili nakon stjecanja resursa ili nakon identificiranja potvrđenog resursa za rad na zadatku. Ova fleksibilnost omogućuje voditeljima projekata izvršavanje sljedećih zadataka:

- Određivanje broja resursa potrebnih za radne pakete WBS-a.
- Procjenu troškova projekta.
- Određivanje pripremnog proračuna.
- Procjenu trajanja aktivnosti na temelju uloga i resursa.
- Razvijanje nekih planova upravljanja projektom na temelju dostupnih informacija o projektu.

Dodatne mogućnosti dodane su u WBS radi bolje uporabe funkcionalnosti resursa.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Mogućnost</th>
<th>Opis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dodjele resursa</td>
<td>Pregledajte dodijeljene resurse, datume, broj radnih sati i vrstu rezervacije za zadatke na WBS-u.</td>
</tr>
<tr class="even">
<td>Automatsko generiranje tima</td>
<td>Automatski dodajte planirane resurse s pomoću uloga povezanih sa zadatkom. Financije automatski predlažu planirane resurse s pomoću višekriterijske analize odluke koja se temelji na ulogama. Nakon što su uloge i rad (sati) postavljeni za zadatke u WBS-u i nakon što je objavljena struktura, odaberite mogućnost <strong>Automatski generiraj tim</strong>. Potreban broj planiranih resursa dodaje se WBS-u i kartici <strong>Planiranje projekata i tima</strong>.</td>
</tr>
<tr class="odd">
<td>Resurs (padajući popis)</td>
<td>Na stranici <strong>Pokretanje dodjele resursa</strong> možete odabrati resurse za fiksnu ili uvjetnu rezervaciju na temelju određenog trajanja. Možete prilagoditi postavke prikaza kako biste vidjeli i postavili trajanje aktivnosti resursa. Možete odabrati i dodijeliti resurse na razini radnog paketa s pomoću sljedećih mogućnosti:
<ul>
<li><strong>Prihvati</strong> – Potvrdite promjene resursa dodijeljenog zadatku.</li>
<li><strong>Odustani</strong> – Odustanite od promjena resursa dodijeljenog zadatku.</li>
<li><strong>Dodijeli automatski</strong> - Dostupni resurs osoblja koji ima podudarnu ulogu automatski se odabire i dodjeljuje odabranom zadatku.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na stranici **Svi projekti** odaberite projekt **XYZ nadogradnja 2. faze**.
2. Odaberite **Planiraj** > **Aktivnosti** > **Strukturna analiza rada**.
3. Odaberite **Novo** kako biste WBS-u dodali sljedeće aktivnosti prve razine:

    - Pokretanje
    - Planiranje
    - Izvršavanje
    - Upravljanje i nadzor
    - Zatvaranje

4. Postavite datume i rad (sate) na način prikazan na sljedećoj slici.

    [![Postavljanje datuma i rada.](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Odaberite redak zadatka **Pokretanje**, a zatim u polju **Uloga** odaberite **Voditelj projekta višeg ranga**.
6. Odaberite **Objavi**.
7. U istom retku, u polju **Resurs** odaberite **Daniel Petek**, a zatim odaberite **Prihvati**.
8. Odaberite redak zadatka **Planiranje**, a zatim u polju **Uloga** odaberite **Poslovni analitičar**.
9. Odaberite **Objavi**, a zatim odaberite **Automatski generiraj tim**.
10. U okviru poruke koji se prikazuje odaberite **Da**.
11. U polju **Resurs** provjerite postoji li vrijednost **Poslovni analitičar 1**.
12. Za resurs **Poslovni analitičar 1**, otvorite pretragu i odaberite **Pokreni dodjele resursa**. Zatim odaberite radnika za zadatak.
13. Odaberite **Uvjetna dodjela** &gt; **Puni kapacitet**.

    > [!NOTE] 
    > Nećete dobiti upozorenje da je navedeni resurs sada 2, jer broj resursa ostaje 1.

14. Na stranici **Strukturna analiza rada** potvrdite dodjelu resursa na WBS-u, a zatim odaberite **Spremi**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]