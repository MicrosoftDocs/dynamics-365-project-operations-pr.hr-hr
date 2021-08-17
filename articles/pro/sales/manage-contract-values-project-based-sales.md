---
title: Pregled redaka ugovora koji se temelje na projektu
description: U ovoj temi nalaze se informacije o radu s redcima ugovora koji se temelji na projektu.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 7da8a7f898e6f0bb46d4cf6de65812e3aabb7416a2fdf2f9d9c8bad07e77cd85
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999037"
---
# <a name="project-based-contract-lines-overview"></a>Pregled redaka ugovora koji se temelje na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Redci ugovora koji se temelje na projektu u aplikaciji Dynamics 365 Project Operations dizajnirani su da drže angažirane ugovore o procjeni i naplati za određene komponente projektnog rada. Struktura retka ugovora koji se temelji na projektu proširena je za procjene projekta i scenarije naplate sa sljedećim konceptima:

- Način naplate
- Mapiranje projekta i zadatka
- Uključene klase transakcije
- Ograničenje koje se ne smije prekoračiti
- Postavka naplativosti
- Procjene s pomoću pojedinosti retka ugovora
- Klijenti retka ugovora

Sljedeća tablica uključuje polja na kartici **Općenito** redaka ugovora koji se temelje na projektu koji pomažu u postavljanju osnove za podrobnu, temeljnu procjenu i aranžmane naplate za posao koji se temelji na projektu.

| Polje | Opis | Utjecaj na niže razine |
| --- | --- | --- |
| **Ime** | Naziv retka ugovora. Ovo identificira određenu komponentu ugovora koja se procjenjuje. Za ugovor o projektu stvoren iz ponude, ova se vrijednost kopira iz odgovarajuće vrijednosti retka ponude koja se temelji na projektu. | Naziv koji se kopira na redak fakture za projekt koji se stvara iz ovog retka kada se stvara faktura. |
| **Način naplate** | U ugovoru o projektu stvorenom iz ponude ova se vrijednost kopira iz odgovarajućeg polja retka ponude. Ovo je skup mogućnosti koji predstavlja dva glavna modela ugovaranja koje podržava aplikacija Project Operations:</br>- **Fiksna cijena**</br>- **Vrijeme i materijal** | Na temelju načina naplate navedenog retka ugovora, obradit će se stvarna transakcija. Ako redak ugovora na koji se odnosi stvarna vrijednost ima način naplate vremena i materijala, stvaraju se stvarni zapisi troška i nenaplaćene prodaje. Ako redak ugovora na koji se poziva stvarni podatak ima način naplate s fiksnom cijenom, stvara se samo stvarni trošak. |
| **Project** | Upotrijebite ovo polje za identificiranje projekta koji će se upotrijebiti za izvođenje posla na ovom angažmanu. | Ova vrijednost koristit će se zajedno sa mogućnostima **Uključeni zadaci** i **Uključeni razredi transakcija** kako bi se razriješila referenca retka ugovora na stvarnom ili procijenjenom zapisu u retku. |
| **Uključeni zadaci** | Označava uključuje li ovaj redak ugovora sve projektne zadatke za odabrani projekt ili samo podskup zadataka. To je skup mogućnosti koji ima sljedeće moguće vrijednosti:</br>- **Svi zadaci projekta**</br>- **Samo odabrani projektni zadaci**. Prazna vrijednost u ovom polju jednaka je odabiru **Svi projektni zadaci**. | Ako se odabere **Samo odabrani zadaci**, možete odabrati određene zadatke i povezati ih s ovim retkom ugovora na kartici **Postavljanje naplate zadatka** na stranici **Projekt**. Ta vrijednost upotrijebit će se zajedno sa klasama **Projekt** i **Uključena transakcija** za rješavanje reference retka ugovora na stvarnom ili procijenjenom zapisu. |
| **Uvrsti vrijeme** | Vrijednost **Da**/**Ne** pokazuje hoće li se vremenske transakcije ili troškovi rada na odabranom projektu uključiti u ovaj redak ugovora. Vrijednost **Ne** znači da vremenske transakcije ili trošak rada neće biti uključeni u ovaj redak ugovora. Vrijednost **Da** označava da hoće. | Ova se vrijednost upotrebljava zajedno s projektom za rješavanje reference retka ugovora na stvarni ili procijenjeni zapis u retku. |
| **Uvrsti trošak** | Vrijednost **Da**/**Ne** označava hoće li se troškovi izdataka na odabranom projektu uključiti u ovaj redak ugovora. Vrijednost **Ne** znači da cijena troška neće biti uključena u ovaj redak ugovora. Vrijednost **Da** označava da hoće. | Ova se vrijednost upotrebljava zajedno s projektom za rješavanje reference retka ugovora na stvarni ili procijenjeni zapis u retku. |
| **Uključi materijale** | Vrijednost **Da**/**Ne** označava hoće li se troškovi materijala na odabranom projektu uključiti u ovaj redak ugovora. Vrijednost **Ne** označava da se troškovi materijala neće uključiti u ovaj redak ugovora. Vrijednost **Da** označava da hoće. | Ova se vrijednost upotrebljava zajedno s projektom za rješavanje reference retka ugovora na stvarni ili procijenjeni zapis u retku. |
| **Uvrsti naknadu** | Vrijednost **Da**/**Ne** označava hoće li se naknade na odabranom projektu uključiti u ovaj redak ugovora. Vrijednost **Ne** znači da naknade neće biti uključene u ovaj redak ugovora. Vrijednost **Da** označava da hoće. | Ova se vrijednost upotrebljava zajedno s projektom za rješavanje reference retka ugovora na stvarni ili procijenjeni zapis u retku. |
| **Ugovoreni iznos** | Na retku ugovora s fiksnom cijenom ovaj je iznos dogovorena vrijednost koja će se fakturirati klijentu za sve komponente posla povezane s ovim retkom ugovora. Na retku ugovora za vrijeme i materijal ovaj je iznos procijenjena vrijednost onoga što će se fakturirati klijentu za sve komponente posla povezane s ovim retkom ugovora. U ugovoru o projektu stvorenom iz ponude ova se vrijednost kopira iz odgovarajućeg polja retka ponude. Kada redak ugovora koji se temelji na projektu ima pojedinosti retka, ovo je polje zaključano za uređivanje i sažeto je od iznosa pojedinosti retka ugovora. | Kada redak ugovora sadrži pojedinosti o retku, ta se vrijednost može izmijeniti promjenom iznosa na pojedinostima retka. Na retku ugovora s fiksnom cijenom, ova se vrijednost upotrebljava za generiranje iznosa prije poreza na periodičnim kontrolnim točkama naplate. |
| **Procijenjeni porez** | Korisnik može urediti ovo polje za unos procijenjenog iznosa poreza u redak ugovora. Kada redak ugovora koji se temelji na projektu ima pojedinosti retka, ovo je polje zaključano za uređivanje i sažeto je od iznosa poreza u pojedinostima retka ugovora. | Kada redak ugovora sadrži pojedinosti o retku, ta se vrijednost može izmijeniti promjenom iznosa poreza na pojedinostima retka. Na retku ugovora s fiksnom cijenom, ova se vrijednost upotrebljava za generiranje poreza na periodičnim kontrolnim točkama naplate. |
| **Ugovoreni iznos nakon poreza** | Iznos retka ugovora nakon poreza. Ovo je polje samo za čitanje i izračunava se kao **Ugovoreni iznos + porez**. | Na retku ugovora s fiksnom cijenom, ova se vrijednost upotrebljava za generiranje periodičnih kontrolnih točaka naplate. |
| **Ograničenje koje se ne smije prekoračiti** | Korisnik može uređivati ovo polje i ono je dostupno samo na redcima ugovora koji se temelje na projektu i imaju način naplate postavljen kao vrijeme i materijal. | Korisnik može uređivati ovo polje. Kada se stvarni podatak o vremenu ili materijalu odnosi na ovaj redak ugovora za vrijeme i materijal, iznos stvarnog podatka procjenjuje se prema ograničenju koje se ne smije prekoračiti u retku ugovora. Ova procjena završava se nakon što se obračunaju već potrošeni i angažirani iznosi. |
| **Proračun klijenta** | Ovo se polje može uređivati i kopira se iz odgovarajućeg polja na retku ponude, ako je ugovor stvoren iz ponude. | Ovo se polje upotrebljava samo za informacije i nema nikakvo daljnje značenje. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Pravila provjere valjanosti mogućnosti na kartici Općenito redaka ugovora koji se temelje na projektu

Pravilo 1: Ako je polje **Uključeni zadaci** prazno ili postavljeno na **Svi projektni zadaci**, svi zadaci projekta uključeni su u redak ugovora.

Pravilo 2: Kada je polje **Uključeni zadaci** prazno ili je izričito postavljeno na **Svi projektni zadaci**, projekt i određena klasa transakcije mogu se uključiti samo u jedan redak ugovora koji se temelji na projektu.

Pravilo 3: Kada je polje **Uključeni zadaci** postavljeno na **Samo odabrani projektni zadaci**, projekt i određena klasa transakcije mogu se uključiti u više redaka ugovora koji se temelji na projektu.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Ugovor</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Redak ugovora</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Uključeni zadaci</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Uvrsti vrijeme</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Uvrsti trošak</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Uključi materijale</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Uvrsti</strong>
                </p>
                <p>
                    <strong>Naknada</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Valjan / nije valjan</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Razlog</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nije valjan </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 2. Vrijeme, trošak, materijali i naknade za projekt P1 uključeni su u retke ugovora i CL1 i CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nije valjan </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 2. Vrijeme, materijali i naknade za projekt P1 uključeni su u retke ugovora i CL1 i CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Valjano </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Vrijeme, materijali i naknade za projekt P1 uključeni su u CL1.
                </p>
                <ul>
                    <li>
Trošak za projekt P1 uključen je u CL2.
                    </li>
                </ul>
                <p>
Nema preklapanja onoga što je uključeno u svaki redak ugovora i stoga vrijedi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Samo odabrani zadaci </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nije valjan </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 2 </p>
                <p>
C1 uključuje vrijeme, materijale, troškove i naknade za podskup zadataka na projektu P1.
                </p>
                <p>
CL2 uključuje vrijeme, materijale, troškove i naknade za cijeli projekt P1 i stoga se preklapa s onim što je uključeno u C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Samo odabrani zadaci </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Valjano </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Prema pravilu #3 </p>
                <p>
C1 uključuje vrijeme, troškove, materijale i naknade za podskup zadataka na projektu P1.
                </p>
                <p>
CL2 uključuje vrijeme, troškove, materijale i naknade za podskup zadataka na projektu P1.
                </p>
                <p>
Jedina dodatna provjera valjanosti odnosi se na podskup zadataka na CL1 koji se razlikuje od podskupa zadataka na CL2 kako bi se osiguralo da nema preklapanja. To čini sustav kada su zadaci povezani.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Samo odabrani zadaci </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="48" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
            <td width="42" valign="top">
                <p>
Jest </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
