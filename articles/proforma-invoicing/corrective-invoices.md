---
title: Korektivne fakture koje se temelje na projektu
description: U ovoj temi nalaze se informacije o načinu stvaranja i potvrđivanja korektivnih faktura koje se temelje na projektu u aplikaciji Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 71bf10518c22ce2ad6aa43b710c68d0d46f93e77
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594615"
---
# <a name="corrective-project-based-invoices"></a>Korektivne fakture koje se temelje na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Potvrđena faktura za projekt može se ispraviti kako bi se obradile promjene ili krediti prema dogovoru s klijentom i upraviteljem projekta.

Kako biste izvršili uređivanje potvrđene fakture, otvorite potvrđenu fakturu i odaberite **Ispravi ovu fakturu**. 

> [!NOTE]
> Ovaj odabir nije dostupan osim ako je faktura projekta potvrđena ili ako faktura koja se temelji na projektu sadrži predujmove ili akontacije tj. usklađivanje predujmova ili akontacija.

Iz potvrđene fakture stvara se novi nacrt fakture. Sve pojedinosti retka fakture iz prethodno potvrđene fakture kopiraju se u novi nacrt. Slijede neke od ključnih točaka koje treba razumjeti o pojedinostima retka na novoj ispravljenoj fakturi:

- Sve količine se ažuriraju na nulu. Dynamics 365 Project Operations pretpostavlja da su sve fakturirane stavke u cijelosti knjižene u korist. Ako je potrebno, ove količine možete ručno ažurirati tako da odražavaju količinu koja se fakturira, a ne količinu koja se duguje. Na temelju količine koju unesete, aplikacija izračunava količinu koja se duguje. Taj se iznos odražava u stvarnim podacima koji se stvaraju nakon potvrde ispravljene fakture. Ako mijenjate iznos poreza, morate unijeti točan iznos poreza, a ne iznos poreza koji se duguje.
- Ispravci kontrolnih točaka uvijek se obrađuju kao puna dugovanja.


> [!IMPORTANT]
> Za pojedinosti retka fakture koje su ispravci za druge već fakturirane troškove, polje **Ispravak** postavljeno je na **Da**. Za pojedinosti koje imaju ispravljene pojedinosti retka fakture, polje **Ima ispravke** postavljeno je na **Da**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Stvarni podaci koji su stvoreni kada se potvrdi korektivna faktura

Tablica u nastavku navodi stvarne podatke koji se stvaraju nakon potvrde korektivne fakture.

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
Fakturiranje punog kredita prethodno fakturirane transakcije materijala.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplate prodaje za količinu i iznos na originalnoj pojedinosti retka fakture za materijal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o naplati prodaje za količinu i iznos na originalnoj pojedinosti retka fakture za materijal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturiranje djelomičnog kredita za transakciju materijala.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplate prodaje za količinu i iznos fakturirane na originalnoj pojedinosti retka fakture za materijal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni podatak o nenaplaćenoj prodaji koji se može naplatiti za količinu i iznos na pojedinosti uređenog retka fakture, storniranje istog i ekvivalentni stvarni podatak o naplaćenoj prodaji.
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
Stanje fakture kontrolne točke ažurira se sa <b>Faktura za klijenta proknjižena</b> na <b>Spremno za fakturiranje</b>.
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
Ovaj scenarij nije podržan.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
