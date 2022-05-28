---
title: Potvrda predračuna za projekt
description: U ovoj temi nalaze se informacije o potvrđivanju predračuna za projekt u aplikaciji Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 276f54936ad9fd72fdc7e85196b43463572e6d3e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600273"
---
# <a name="confirm-a-proforma-project-invoice"></a>Potvrda predračuna za projekt 

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_


Nakon potvrde predračuna status fakture za projekt ažurira se na **Potvrđeno**. Kad se faktura potvrdi, postaje samo za čitanje. Ubuduće se faktura može ispraviti samo ako postoje ispravke ili krediti koje je pokrenuo klijent.

Sljedeća tablica navodi stvarne podatke koje je stvorio sustav. Ti se stvarni podaci stvaraju kada se izvrše određene radnje na nacrtu fakture za projekt prije nego što se ona potvrdi.

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
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturiranje predujma ili akontacije </p>
            </td>
            <td width="408" valign="top">
                <p>
Stvarni podatak o naplati prodaje vrste <strong>Akontacija</strong> stvara se za iznos predujma ili akontacije.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Stvarni podatak o nenaplaćenoj prodaji negativnog iznosa akontacije ili predujma, koji će se upotrebljavati za usklađivanje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Nakon potpunog usklađenja akontacije ili predujma na računu.
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
Stvarni podatak o naplati prodaje za iznos na toj fakturi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Nakon djelomičnog usklađenja akontacije ili predujma na računu.
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
Stvarni podatak o naplati prodaje za iznos na toj fakturi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Negativni stvarni podatak o nenaplaćenoj prodaji preostalog iznosa akontacije ili predujma, koji će se upotrebljavati za usklađivanje na budućim fakturama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturiranje transakcije vremena bez ikakvih uređivanja nacrta fakture.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za sate i iznos na izvornom odobrenju vremena.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Stvarni podatak o naplaćenoj prodaji za sate i iznos na izvornom odobrenju vremena.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturiranje transakcije vremena koja je uređena za smanjenje količine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za sate i iznos na izvornom odobrenju vremena.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za sate i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o prodaji i ekvivalent stvarnom podatku naplaćene prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koji se ne naplaćuje za preostale sate i iznos nakon odbijanja ispravljenih brojki u pojedinosti retka uređene fakture, storniranje stvarnog podatka o prodaji i ekvivalent stvarnom podatku naplaćene prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturiranje transakcije vremena koja je uređena za povećanje količine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za sate i iznos na izvornom odobrenju vremena.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za sate i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturiranje transakcije troška bez ikakvih uređivanja nacrta fakture.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za količinu i iznos na izvornom odobrenju troška.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Stvarni podatak naplaćene prodaje za količinu i iznos na izvornom odobrenju troška </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturiranje transakcije troška koja je uređena za smanjenje količine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za količinu i iznos na izvornom odobrenju troška.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za količinu i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koji se ne naplaćuje za preostalu količinu i iznos nakon odbijanja ispravljenih brojki u pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturiranje transakcije troška koja je uređena za povećanje količine.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za količinu i iznos na izvornom odobrenju troška.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za količinu i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturiranje transakcije materijala bez ikakvih izmjena na skici fakture.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za utrošeni materijal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Naplaćena stvarna prodaja za količinu i iznos na originalnom odobrenju za utrošeni materijal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturiranje transakcije materijala koja je uređena kako bi se smanjila količina.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju vremena.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za količinu i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koji se ne naplaćuje za preostalu količinu i iznos nakon odbijanja ispravljenih brojki u pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturiranje transakcije materijala koja je uređena kako bi se povećala količina.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za utrošeni materijal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za količinu i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturiranje naknade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za iznos naknade na izvornom retku dnevnika.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Stvarni podatak naplaćene prodaje za količinu i iznos na izvornom retku dnevnika naknade.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturiranje kontrolne točke.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Stvarni podatak naplaćene prodaje za iznos kontrolne točke na izvornoj kontrolnoj točki retka ugovora o projektu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturiranje retka ugovora koji se temelji na proizvodu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Stvarni podatak naplaćene prodaje za redak proizvoda s količinom i iznosom koji dolaze iz retka ugovora koji se temelji na proizvodu.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
