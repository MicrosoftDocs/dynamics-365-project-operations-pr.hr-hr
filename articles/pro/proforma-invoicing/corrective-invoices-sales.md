---
title: Krediti i ispravljene fakture
description: U ovoj temi nalaze se informacije o ispravljenim fakturama u rješenju Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2187627439d42b37222dce0a491c62dafc358d5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073499"
---
# <a name="credits-and-corrected-invoices"></a>Krediti i ispravljene fakture

_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_

Potvrđena faktura za projekt može se ispraviti kako bi se obradile promjene ili krediti prema dogovoru s klijentom i upraviteljem projekta.

Kako biste izvršili uređivanje potvrđene fakture, otvorite potvrđenu fakturu i odaberite **Ispravi ovu fakturu**. 

> [!NOTE]
> Ovaj odabir nije dostupan ako se faktura za projekt ne potvrdi.

Iz potvrđene fakture stvara se novi nacrt fakture. Sve pojedinosti retka fakture iz prethodno potvrđene fakture kopiraju se u novi nacrt. Slijede neke od ključnih točaka koje treba razumjeti o pojedinostima retka na novoj ispravljenoj fakturi:

- Sve količine se ažuriraju na nulu. Aplikacija pretpostavlja da se sve fakturirane stavke u potpunosti duguju. Ako je potrebno, ove količine možete ručno ažurirati tako da odražavaju količinu koja se fakturira, a ne količinu koja se duguje. Na temelju količine koju unesete, aplikacija izračunava količinu koja se duguje. Taj se iznos odražava u stvarnim podacima koji se stvaraju nakon potvrde ispravljene fakture. Ako mijenjate iznos poreza, morate unijeti točan iznos poreza, a ne iznos poreza koji se duguje.
- Prethodno potvrđeni redci ugovora koji se temelje na proizvodu ne kopiraju se. Obrada ispravaka na fakturi za projekt koja se temelji na proizvodu nije podržana.
- Ispravci kontrolnih točaka uvijek se obrađuju kao puna dugovanja.
- Iznos akontacije ili predujma može se ispraviti ako je klijentu fakturiran netočan iznos.
- Usklađivanje iznosa akontacija i predujmova mogu se ispraviti ako se upotrebljavao netočan iznos za usklađivanje sa zaračunanim iznosima na prethodno potvrđenoj fakturi.

> [!IMPORTANT]
> Pojedinosti retka fakture koje predstavljaju ispravke za ostale već fakturirane troškove imaju polje **Ispravak** postavljeno na **Da**. Fakture koje su ispravile pojedinosti retka fakture imaju polje koje se naziva **Ima ispravaka** koje je također postavljeno na **Da**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Stvarni podaci stvoreni na potvrdi korektivne fakture:

Ispod su stvarni podaci koje je stvorila aplikacija za potvrdu ispravka na temelju operacija izvršenih na nacrtu korektivne fakture prije potvrde.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Scenarij</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Stvarni podaci stvoreni potvrdom</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Potvrdite ispravak fakturiranog predujma ili akontacije.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje akontacije ili predujma koji je stvoren za usklađivanje. Ovaj je iznos pozitivan jer se želi poništiti negativan iznos stvoren pri fakturiranju akontacije ili predujma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Stvarni podatak o storniranju naplaćene prodaje stvara se za iznos akontacije ili predujme za storniranje izvorno zaračunane prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o naplaćenoj prodaji stvara se za ispravljeni iznos na retku ispravljene fakture koji se temelji na akontaciji ili predujmu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Stvarni podatak o nenaplaćenoj prodaji negativnog iznosa retka fakture koji se temelji na akontaciji ili predujmu, koji će se upotrebljavati za usklađivanje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Potvrda ispravka prethodno usklađene akontacije ili predujma.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje akontacije ili predujma koji je stvoren za usklađivanje. Ovaj je iznos pozitivan i namijenjen je poništenju negativnog iznosa stvorenog pri prethodnom usklađenju.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Stvarni podatak o storniranoj naplati prodaje za iznos na prethodnoj fakturi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o naplaćenoj prodaji za ispravljeni iznos akontacije koji se prikazuje na ispravljenoj fakturi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Stvarni podatak o nenaplaćenoj prodaji s negativnim iznosom ispravljenog ostatka akontacije ili predujma, koji će se upotrebljavati za usklađivanje u kasnijim fakturama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturiranje cjelokupnog duga prethodno fakturirane transakcije vremena.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za sate i iznos na izvornoj pojedinosti retka fakture za vrijeme.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o naplaćenoj prodaji za sate i iznos na izvornoj pojedinosti retka fakture za vrijeme.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturiranje djelomičnog duga za transakciju vremena.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za sate i iznos fakturirane na izvornoj pojedinosti retka fakture za vrijeme.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koja se naplaćuje za sate i iznos za pojedinosti retka uređene fakture, storniranje istog i ekvivalentna stvarnom podatku naplaćene prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za preostale sate i iznos nakon odbijanja ispravljenih podataka u pojedinosti retka računa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturiranje cjelokupnog duga prethodno fakturirane transakcije troška.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za trošak.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za trošak.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturiranje djelomičnog duga prethodno fakturirane transakcije troška.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za količinu i iznos naplaćen na izvornoj pojedinosti retka fakture za trošak.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koja se naplaćuje za količinu i iznos za pojedinosti retka ispravljene fakture, storniranje istog i ekvivalentna stvarnom podatku naplaćene prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za preostalu količinu i iznos nakon odbijanja ispravljenih podataka u pojedinosti retka računa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturiranje cjelokupnog duga prethodno fakturirane transakcije naknade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za naknadu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za naknadu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturiranje djelomičnog duga iz prethodno fakturirane transakcije naknade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za naknadu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koja se naplaćuje za količinu i iznos za pojedinost retka uređene ispravljene fakture, storniranje istog i ekvivalentna stvarnom podatku naplaćene prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturiranje cjelokupnog duga prethodno fakturirane kontrolne točke.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za sate i iznos na izvornoj pojedinosti retka za kontrolnu točku.
                </p>
                <p>
Status fakture za kontrolnu točku ili naplate za redak ugovora o projektu ažurira se na **Spremno za fakturiranje**.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturiranje djelomičnog duga prethodno fakturirane kontrolne točke.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nije podržano </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Dugovi i ispravci prethodno fakturiranog retka ugovora koji se temelji na proizvodu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nije podržano </p>
            </td>
        </tr>
    </tbody>
</table>
