---
title: Redci ponude utemeljeni na projektu
description: U ovoj temi nalaze se informacije o uporabi redaka ponude koji se temelje na projektu za rad na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906107"
---
# <a name="project-based-quote-lines"></a>Redci ponude utemeljeni na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Redci ponude koji se temelje na projektu osmišljeni su za pomoć pri procjeni angažiranja rada na projektu. Struktura redaka ponude koji se temelje na projektu proširena je za projektne procjene sa sljedećim konceptima:

- Način naplate
- Mapiranje projekta
- Uključene klase transakcija
- Ograničenje koje se ne smije prekoračiti
- Postavka naplativosti
- Procjena s pomoću pojedinosti retka ponude
- Klijenti retka ponude

Tablica u nastavku pruža informacije o poljima na kartici **Općenito** retka ponude koji se temelje na projektu. Ova polja pomažu u postavljanju osnove za podrobnu, temeljitu procjenu rada na projektu.

| **Polje** | **Relevantnost, svrha i smjernice** | **Utjecaj na niže razine** |
| --- | --- | --- |
| Ime | Naziv retka ponude koji bi vam trebao pomoći pri prepoznavanju diskretne komponente ponude koja se procjenjuje. | Kopira se u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda. |
| Način naplate | U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz odgovarajućeg polja u retku prilike. Ovo polje uključuje dva glavna načina ugovaranja koje podržava aplikacija Dynamics 365 Project Operations:</br>- Fiksna cijena</br>- Vrijeme i materijal.| Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda. |
| Project | Upotrijebite ovo neobvezno polje za identifikaciju projekta koji će se upotrebljavati za izvođenje radova na ovom angažmanu. Kada se projekt preslika u redak ponude, to pomaže pri postavljanju naplativih zadataka, a također i pri donošenju procjene koji se temelji na projektu za redak ponude kao pojedinosti retka ponude. Kada projekt nije mapiran u redak ponude koji se temelji na projektu, procjenu treba stvoriti ručno stvaranjem svake pojedinosti retka ponude. | Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda. |
| Uvrsti vrijeme | Zastavica **Da**/**Ne** označava hoće li vremenske transakcije ili troškovi rada na odabranom projektu biti uključeni u procjenu u ovom retku ponude. Vrijednost **Ne** označava da vremenske transakcije ili trošak rada neće biti uključeni u procjenu u ovom retku ponude. Vrijednost **Da** označava da će vremenske transakcije ili trošak rada biti uključeni u procjenu u ovom retku ponude. | Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda. |
| Uvrsti trošak | Zastavica **Da**/**Ne** označava hoće li troškovi izdataka na odabranom projektu biti uključeni u procjenu u ovom retku ponude. Vrijednost **Ne** označava da trošak izdatka neće biti uključen u procjenu u ovom retku ponude. Vrijednost **Da** označava da će trošak izdatka biti uključen u procjenu u ovom retku ponude. | Ta se vrijednost polja kopira preko retka ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda. |
| Uvrsti naknadu | Zastavica **Da**/**Ne** označava hoće li naknade na odabranom projektu biti uključene u procjenu u ovom retku ponude. Vrijednost **Ne** označava da naknade neće biti uključene u procjenu u ovom retku ponude. Vrijednost **Da** označava da će naknade biti uključene u procjenu u ovom retku ponude. | Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda. |
| Ponuđeni iznos | To je iznos koji će se ponuditi klijentu za sav posao predviđen u ovom retku ponude koji se temelji na projektu. U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz polja **Proračun klijenta** u redak prilike. Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa iz pojedinosti retka ponude. | Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda. |
| Procijenjeni porez | Ovo je polje koje korisnik može uređivati kako bi dodao procijenjeni iznos poreza u redak ponude. Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa poreza iz pojedinosti retka ponude. | Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda. |
| Ponuđeni iznos nakon oporezivanja | Ovo je polje iznos retka ponude nakon oporezivanja i samo je za čitanje. Iznos u ovom polju izračunava se kao *Ponuđeni iznos + porez*. | Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda. |
| Ograničenje koje se ne smije prekoračiti | Ovo se polje može uređivati i dostupno je samo u redcima ponude koji se temelje na projektu i imaju način naplate **Vrijeme i materijal**. | Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda. |
| Proračun klijenta | Ovo se polje može uređivati i kopira se iz odgovarajućeg polja u retku prilike ako je ponuda stvorena iz prilike. | Ta se vrijednost polja kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Pravila provjere valjanosti za polja na kartici Općenito redaka ponude koji se temelje na projektu

**Pravilo 1**: Određena klasa transakcije na odabranom projektu može se uključiti samo u jedan redak ponude koji se temelji na projektu.

**Pravilo 2**: Ako prilika ima više ponuda, mogu postojati redci ponude iz različitih ponuda koji se svi odnose na isti projekt i uključuju istu klasu transakcije.

**Pravilo 3**: Ako ponude ne pripadaju istoj prilici, ne mogu obuhvaćati isti projekt i klasu transakcije.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Prilika</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Ponuda</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Redak ponude</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
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
                    <strong>Uvrsti</strong>
                </p>
                <p>
                    <strong>naknada</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Valjan / nije valjan</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Razlog</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Nije valjan </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 1. Vrijeme, trošak i naknade za projekt P1 uključeni su u oba retka ponude, QL1 i QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Nije valjan </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 1. Vrijeme i naknade za projekt P1 uključeni su u oba retka ponude, QL1 i QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Valjano </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
Vrijeme i naknade za projekt P1 uključeni su u QL1.
Trošak za projekt P1 uključen je u QL2.
Nema preklapanja onoga što je uključeno u svaki redak ponude, tako da je valjan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Nije valjan </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kršenje gornjeg pravila br. 1 </p>
                <p>
Q1 uključuje vrijeme, troškove i naknade za cijeli projekt P1.
                </p>
                <p>
QL2 uključuje vrijeme, troškove i naknade za cijeli projekt P1 i preklapa se s onim što je uključeno u Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
                <p>
Valjano </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Na temelju pravila br. 2, Q1 i Q2 dvije su ponude u istoj prilici, tako da obje mogu procijeniti iste komponente projekta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
2. tromj. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 u Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
                <p>
Valjano </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Na temelju pravila br. 3, Q1 i Q2 dvije su ponude u različitim prilikama, tako da ne mogu procijeniti iste komponente istog projekta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
                <p>
Nije valjan </p>
            </td>
        </tr>
    </tbody>
</table>

