---
title: Konfiguriranje naplative komponente retka ponude
description: U ovoj temi nalaze se informacije o postavljanju naplativih i nenaplativih komponenti na retku ponude koji se temelji na projektu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003757"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Konfiguriranje naplative komponente retka ponude 

_**Primjenjuje se na:** Osnovna implementacija – od dogovora do predračuna, Project Operations za scenarije koji se temelje na resursima / bez zaliha_

Redak ponude koji se temelji na projektu ima koncept *uključenih* komponenti i *naplativih* komponenti.

Uključene komponente podliježu:

  - Način naplate i podjele klijenta
  - Ograničenja koja se ne smiju prekoračiti 
  - Postavke učestalosti fakture definirane u retku ponude koji se temelji na projektu

Podskup uključenih komponenti može se označiti kao naplativ s pomoću polja **Vrsta naplate**. Polje **Vrsta naplate** skup je mogućnosti koji dopušta sljedeće vrijednosti u kontekstu retka ponude:

  - Naplativo
  - Nenaplativo

Komponente koje se naplaćuju mogu se definirati u zadacima, ulogama i kategorijama transakcija.

Mogućnost naplate definirana je na zadacima za redak ponude i primjenjuje se na sve klase transakcija uključene u taj redak. Ako je polje **Uključi zadatke** postavljeno na **Cijeli projekt** ili je ostavljeno prazno, kartica **Naplativi zadaci** nije dostupna.

Mogućnost naplate definirana je u ulogama za redak ponude i primjenjuje se samo na klasu transakcije **Vrijeme**. Ako je polje **Uključi vrijeme** postavljeno na **Ne** u retku ponude projekta, kartica **Naplative uloge** nije dostupna.

Mogućnost naplate definirana je u kategorijama transakcije za redak ponude i primjenjuje se samo na klasu transakcije **Trošak**. Ako je polje **Uključi troškove** postavljeno na **Ne** u retku ponude projekta, kartica **Naplative kategorije** nije dostupna.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Ažuriranje projektnog zadatka kako bi bio naplativ ili nenaplativ

Projektni zadatak može biti naplativ ili nenaplativ u kontekstu određenog retka ponude koji se temelji na projektu, što omogućuje sljedeće postavljanje.

Ako redak ponude koji se temelji na projektu uključuje **Vrijeme** i zadatak **T1**, zadatak je povezan s retkom ponude kao naplativ. Ako postoji drugi redak ponude koji uključuje stavku **Troškovi**, možete povezati zadatak **T1** s retkom ponude kao nenaplativ. Rezultat je da se svo vrijeme zabilježeno na zadatku naplaćuje, dok se svi troškovi zabilježeni na zadatku ne naplaćuju.

Vrsta naplate zadatka može se konfigurirati na kartici **Naplativi zadaci** retka ponude koji se temelji na projektu ažuriranjem polja **Vrsta naplate** u podrešetki **Zadaci retka ponude**. Umjesto toga, možete ažurirati vrstu naplate za projektni zadatak u polju **Vrsta naplate** na podrešetki, na postavci naplate zadatka projekta koja prikazuje retke ponude povezane sa zadatkom.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Ažuriranje uloge kako bi bila naplativa ili nenaplativa

Uloga može biti naplativa ili nenaplativa u kontekstu određenog retka ponude koji se temelji na projektu.

Vrsta naplate uloge može se konfigurirati na kartici **Naplative uloge** retka ponude ažuriranjem polja **Vrsta naplate** u podrešetki **Naplative uloge**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Ažuriranje kategorije transakcije kako bi bila naplativa ili nenaplativa

Kategorije transakcije može biti naplativa ili nenaplativa na određenom retku ponude.

Vrsta naplate transakcije može se konfigurirati na kartici **Naplative kategorije** retka ponude ažuriranjem polja **Vrsta naplate** u podrešetki **Naplative kategorije**.

### <a name="resolve-chargeability"></a>Rješavanje naplativosti
Procjena ili stvarni podatak stvoren za vrijeme smatrat će se naplativim samo ako je:

   - **Vrijeme** uključeno u redak ponude.
   - **Uloga** konfigurirana kao naplativa u retku ponude.
   - Mogućnost **Uključeni zadaci** postavljena na **Odabrani zadaci** u retku ponude. 

Ako su ove tri stvari točne, **Zadatak** je također konfiguriran kao naplativ. 

Procjena ili stvarni podatak stvoren za trošak smatra se naplativim samo ako je: 

   - **Trošak** uključen u redak ponude.
   - **Kategorija transakcije** konfigurirana kao naplativa u retku ponude.
   - Mogućnost **Uključeni zadaci** postavljena na **Odabrani zadaci** u retku ponude.

Ako su ove tri stvari točne, **Zadatak** je također konfiguriran kao naplativ. 

Procjena ili stvarni podatak stvoren za materijal smatrat će se naplativim samo ako je:

   - **Materijal** uključen u redak ponude.
   - Mogućnost **Uključeni zadaci** postavljena na **Odabrani zadaci** u retku ponude.

Ako su ove dvije stvari točne, **Zadatak** bi također trebao biti konfiguriran kao naplativ. 


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
Naplata za stvarno vrijeme: Naplativo </p>
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
Naplativo </p>
            </td>
            <td width="350" valign="top">
                <p>
Naplata za stvarno vrijeme: Naplativo </p>
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
