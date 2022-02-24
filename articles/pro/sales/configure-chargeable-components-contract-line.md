---
title: Konfiguriranje naplative komponente retka ugovora koji se temelji na projektu
description: U ovoj temi nalaze se informacije o načinu dodavanja naplatnih komponenti u retke ugovora u projektnim operacijama.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858464"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfiguriranje naplative komponente retka ugovora koji se temelji na projektu

_**Primjenjuje se na:** Osnovna implementacija – od dogovora do predračuna, Project Operations za scenarije koji se temelje na resursima / bez zaliha_

Redak ugovora koji se temelji na projektu ima *naplative* komponente i *naplative* komponente.

Uključene komponente, komponente su koje podliježu:

  - Način naplate i podjele klijenta
  - Ograničenja koja se ne smiju prekoračiti 
  - Postavke učestalosti fakture definirane u retku ugovora koji se temelji na projektu

Podskup uključenih komponenti može se označiti kao naplativ s pomoću polja **Vrsta naplate**. Polje **Vrsta naplate** skup je mogućnosti koji dopušta sljedeće vrijednosti u kontekstu retka ugovora:

  - Naplativo
  - Nenaplativo

Komponente koje se naplaćuju mogu se definirati u zadacima, ulogama i kategorijama transakcija.

Mogućnost naplate definirana je na zadacima za redak ugovora o projektu i primjenjuje se na sve klase transakcija uključene u redak. Ako je polje **Uključi zadatke** u retku ugovora prazno ili postavljeno na **Cijeli projekt**, kartica **Naplativi zadaci** neće biti dostupna.

Mogućnost naplate definirana u ulogama za redak ugovora o projektu odnosi se samo na klasu transakcije **Vrijeme**. Ako je polje **Uključi vrijeme** u retku ugovora o projektu postavljeno na **Ne**, kartica **Naplative uloge** neće biti dostupna.

Mogućnost naplate definirana je u kategorijama transakcije za redak ugovora o projektu i primjenjuje se samo na klasu transakcije **Trošak**. Ako je polje **Uključi troškove** postavljeno na **Ne**, kartica **Naplative kategorije** neće biti dostupna.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Ažuriranje projektnog zadatka kao naplativog ili nenaplativog

Projektni zadatak može biti naplativ ili nenaplativ u određenom retku ugovora koji omogućuje sljedeće postavljanje:

Ako redak ugovora koji se temelji na projektu uključuje **Vrijeme** i određeni zadatak, **T1** povezan je s njim kao naplativ. Ako postoji drugi redak ugovora koji uključuje stavku **Trošak**, možete povezati zadatak T1 s retkom ugovora kao nenaplativ. Rezultat je da se svo vrijeme zabilježeno na zadatku naplaćuje, dok su svi troškovi nenaplativi.

Vrsta naplate zadatka može se konfigurirati na kartici **Naplativi zadaci** retka ugovora ažuriranjem polja **Vrsta naplate** u podrešetki zadataka retka ugovora. Umjesto toga, možete ažurirati polje **Vrsta naplate** na podrešetki postavke naplate zadatka projekta koja prikazuje retke povezane sa zadatkom.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Ažuriranje uloge kao naplative ili nenaplative

Uloga može biti naplativa ili nenaplativa u određenom retku ugovora.

Vrsta naplate za ulogu može se konfigurirati na kartici **Naplative uloge** retka ugovora. Kako biste to učinili, ažurirajte polje **Vrsta naplate** u podrešetki **Naplative uloge**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Ažuriranje kategorije transakcije kao naplativa ili nenaplativa

Kategorije transakcije može biti naplativa ili nenaplativa na određenom retku ugovora.

Vrsta naplate transakcije može se konfigurirati na kartici **Naplative kategorije** retka ugovora koji se temelji na projektu. Kako biste to učinili, ažurirajte polje **Vrsta naplate** u podrešetki **Naplative kategorije**.

### <a name="resolve-chargeability"></a>Rješavanje naplativosti

Procjena ili stvarni podatak stvoren za vrijeme smatra se naplativim samo ako je:

   - **Vrijeme** uključeno u redak ugovora.
   - **Uloga** konfigurirana kao naplativa u retku ugvora.
   - Mogućnost **Uključeni zadaci** postavljena na **Odabrani zadaci** u retku ugovora.
 
 Ako su ove tri stvari točne, zadatak je konfiguriran kao naplativ. 

Procjena ili stvarni podatak stvoren za trošak smatra se naplativim samo ako je:

   - **Trošak** uključeno u redak ugovora
   - **Kategorija transakcije** konfigurirana kao naplativa u retku ugovora
   - Mogućnost **Uključeni zadaci** postavljena na **Odabrani zadatak** u retku ugovora
  
 Ako su ove tri stvari točne, **Zadatak** je konfiguriran kao naplativ. 

Procjena ili stvarni podatak stvoren za materijal smatra se naplativim samo ako je:

   - Stavka **Materijali** uključena u redak ugovora
   - Mogućnost **Uključeni zadaci** postavljena na **Odabrani zadaci** u retku ugovora

Ako su ove dvije stvari točne, **Zadatak** je konfiguriran kao naplativ. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Uključuje Vrijeme</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Uključuje Trošak</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Obuhvaća materijale</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Uključeni zadaci</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Uloga</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategorija</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Zadatak</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Učinak naplativosti</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jest </p>
            </td>
            <td width="78" valign="top">
                <p>
Jest </p>
            </td>
            <td width="63" valign="top">
                <p>
Jest </p>
            </td>
            <td width="75" valign="top">
                <p>
Cijeli projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="70" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće postaviti </p>
            </td>
            <td width="350" valign="top">
                <p>
Naplata za stvarno vrijeme: <strong>Naplativo</strong>
                </p>
                <p>
Vrsta naplate stvarnog troška: <strong>Naplativo</strong>
                </p>
                <p>
Vrsta naplate stvarnog materijala: <strong>Naplativo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jest </p>
            </td>
            <td width="78" valign="top">
                <p>
Jest </p>
            </td>
            <td width="63" valign="top">
                <p>
Jest </p>
            </td>
            <td width="75" valign="top">
                <p>
Samo odabrani zadaci </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="70" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="350" valign="top">
                <p>
Naplata za stvarno vrijeme: <strong>Naplativo</strong>
                </p>
                <p>
Vrsta naplate stvarnog troška: <strong>Naplativo</strong>
                </p>
                <p>
Vrsta naplate stvarnog materijala: <strong>Naplativo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jest </p>
            </td>
            <td width="78" valign="top">
                <p>
Jest </p>
            </td>
            <td width="63" valign="top">
                <p>
Jest </p>
            </td>
            <td width="75" valign="top">
                <p>
Samo odabrani zadaci </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="350" valign="top">
                <p>
Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </p>
                <p>
Vrsta naplate na stvarnom trošku: Naplativo </p>
                <p>
Vrsta naplate stvarnog materijala: Naplativo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jest </p>
            </td>
            <td width="78" valign="top">
                <p>
Jest </p>
            </td>
            <td width="63" valign="top">
                <p>
Jest </p>
            </td>
            <td width="75" valign="top">
                <p>
Samo odabrani zadaci </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="70" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </p>
                <p>
Vrsta naplate stvarnog troška: <strong>Nenaplativo</strong>
                </p>
                <p>
Vrsta naplate stvarnog materijala: <strong>Nenaplativo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jest </p>
            </td>
            <td width="78" valign="top">
                <p>
Jest </p>
            </td>
            <td width="63" valign="top">
                <p>
Jest </p>
            </td>
            <td width="75" valign="top">
                <p>
Samo odabrani zadaci </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </p>
                <p>
Vrsta naplate stvarnog troška: <strong>Nenaplativo</strong>
                </p>
                <p>
Vrsta naplate stvarnog materijala: <strong> Nenaplativo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jest </p>
            </td>
            <td width="78" valign="top">
                <p>
Jest </p>
            </td>
            <td width="63" valign="top">
                <p>
Jest </p>
            </td>
            <td width="75" valign="top">
                <p>
Samo odabrani zadaci </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="350" valign="top">
                <p>
Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </p>
                <p>
Vrsta naplate stvarnog troška: <strong>Nenaplativo</strong>
                </p>
                <p>
Vrsta naplate stvarnog materijala: Naplativo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Jest </p>
            </td>
            <td width="63" valign="top">
                <p>
Jest </p>
            </td>
            <td width="75" valign="top">
                <p>
Cijeli projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće postaviti </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Naplativo</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće postaviti </p>
            </td>
            <td width="350" valign="top">
                <p>
Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </p>
                <p>
Vrsta naplate na stvarnom trošku: Naplativo </p>
                <p>
Vrsta naplate stvarnog materijala: Naplativo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Jest </p>
            </td>
            <td width="63" valign="top">
                <p>
Jest </p>
            </td>
            <td width="75" valign="top">
                <p>
Cijeli projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće postaviti </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće postaviti </p>
            </td>
            <td width="350" valign="top">
                <p>
Naplata stvarnog vremena: <strong>Nenaplativo</strong>
                </p>
                <p>
Vrsta naplate stvarnog troška: <strong> Nenaplativo</strong>
                </p>
                <p>
Vrsta naplate stvarnog materijala: Naplativo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jest </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Jest </p>
            </td>
            <td width="75" valign="top">
                <p>
Cijeli projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="70" valign="top">
                <p>
Nije moguće postaviti </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće postaviti </p>
            </td>
            <td width="350" valign="top">
                <p>
Naplata za stvarno vrijeme: Naplativo </p>
                <p>
Vrsta naplate stvarnog troška:<strong> Nenaplativo</strong>
                </p>
                <p>
Vrsta naplate stvarnog materijala: Naplativo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jest </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Jest </p>
            </td>
            <td width="75" valign="top">
                <p>
Cijeli projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Nije moguće postaviti </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće postaviti </p>
            </td>
            <td width="350" valign="top">
                <p>
Naplata stvarnog vremena: <strong>Nenaplativo </strong>
                </p>
                <p>
Vrsta naplate stvarnog troška:<strong> Nenaplativo</strong>
                </p>
                <p>
Vrsta naplate stvarnog materijala: Naplativo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jest </p>
            </td>
            <td width="78" valign="top">
                <p>
Jest </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Cijeli projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="70" valign="top">
                <p>
Naplativo </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće postaviti </p>
            </td>
            <td width="350" valign="top">
                <p>
Naplata za stvarno vrijeme: Naplativo </p>
                <p>
Vrsta naplate na stvarnom trošku: Naplativo </p>
                <p>
Vrsta naplate stvarnog materijala: <strong> Nenaplativo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Jest </p>
            </td>
            <td width="78" valign="top">
                <p>
Jest </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Cijeli projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nenaplativo</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Nije moguće postaviti </p>
            </td>
            <td width="350" valign="top">
                <p>
Naplata stvarnog vremena: <strong>Nenaplativo </strong>
                </p>
                <p>
Vrsta naplate stvarnog troška: <strong> Nenaplativo</strong>
                </p>
                <p>
Vrsta naplate stvarnog materijala: <strong> Nenaplativo</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
