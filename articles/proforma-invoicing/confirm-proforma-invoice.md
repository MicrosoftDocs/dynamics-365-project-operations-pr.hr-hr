---
title: Potvrda predračuna
description: U ovoj temi nalaze se informacije o potvrđivanju predračuna.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128094"
---
# <a name="confirm-a-proforma-invoice"></a>Potvrda predračuna

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Nakon potvrde predračuna status fakture za projekt ažurira se na **Potvrđeno**. Kad se faktura potvrdi, postaje samo za čitanje. Ubuduće se faktura može ispraviti samo ako postoje ispravke ili dugovanja koje je pokrenuo klijent ili ako je označena kao plaćena.

Sljedeća tablica navodi stvarne podatke koje je stvorio sustav. Ti se stvarni podaci stvaraju kada se izvrše određene radnje na nacrtu fakture za projekt prije nego što se ona potvrdi.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Scenarij</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Stvarni podaci stvoreni potvrdom</strong>
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
Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za sate i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koji se ne naplaćuje za preostalo radno vrijeme i iznos nakon odbijanja ispravljenih brojki u pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.
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
Stvarni podatak o naplaćenoj prodaji za količinu i iznos na izvornom odobrenju troška.
                </p>
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
    </tbody>
</table>
