---
title: Pregled redaka ponude koji se temelje na projektu
description: U ovom se članku nalaze informacije o korištenju redaka ponuda temeljenih na projektu za projektni rad.
author: rumant
ms.date: 03/30/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 90c5affa25b113476e43f0bbbadd5c9615f9c05c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934449"
---
# <a name="project-based-quote-lines-overview"></a>Pregled redaka ponude koji se temelje na projektu 

_**Primjenjuje se na:** Osnovna implementacija – od dogovora do predračuna, Project Operations za scenarije koji se temelje na resursima / bez zaliha_

Redci ponude koji se temelje na projektu osmišljeni su za pomoć pri procjeni angažiranja rada na projektu. Struktura redaka ponude koji se temelje na projektu proširena je za projektne procjene sa sljedećim konceptima:

- Način naplate
- Mapiranje projekta i zadatka
- Uključene klase transakcija
- Ograničenje koje se ne smije prekoračiti
- Postavka naplativosti
- Procjena s pomoću pojedinosti retka ponude
- Klijenti retka ponude

Tablica u nastavku pruža informacije o poljima na kartici **Općenito** retka ponude koji se temelje na projektu. Ova polja pomažu u postavljanju osnove za podrobnu, temeljitu procjenu rada na projektu.

| **Polje** | **Opis** | **Utjecaj prema dolje** |
| --- | --- | --- |
| Ime | Naziv retka ponude koji vam pomaže prepoznati diskretnu komponentu ponude koja se procjenjuje. | Kopira se u redak ugovora o projektu koji se stvara iz ovog retka ponude kad se prihvati ponuda. |
| Način naplate | U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz odgovarajućeg polja u retku prilike. Ovo polje uključuje dva glavna modela ugovaranja koja podržava aplikacija Dynamics 365 Project Operations:</br>- Fiksna cijena</br>- Vrijeme i materijal.| Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi. |
| Project | Upotrijebite ovo neobvezno polje za identifikaciju projekta koji će se upotrebljavati za izvođenje radova na ovom angažmanu. Kada se projekt preslika u redak ponude, to pomaže pri postavljanju naplativih zadataka, a također i pri donošenju procjene koji se temelji na projektu za redak ponude kao pojedinosti retka ponude. Kada projekt nije mapiran u redak ponude koji se temelji na projektu, procjenu treba stvoriti ručno stvaranjem svake pojedinosti retka ponude. | Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi.|
| Uključeni zadaci | Označava upotrebljava li se ovaj redak ponude za sve ili samo neke projektne zadatke odabranog projekta. Polje ima sljedeće moguće vrijednosti:</br>- Svi projektni zadaci</br>- Samo odabrani projektni zadaci</br>Nepostojanje vrijednosti u ovom polju jednako je mogućnosti **Svi projektni zadaci**. | Kad se na stranici projekta odabere stavka **Samo odabrani projektni zadaci**, kartica **Postavljanje zadatka za naplatu** omogućuje odabir određenih zadataka kako biste ih povezali s ovim retkom ponude. Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi. |
| Uvrsti vrijeme | Vrijednost **Da**/**Ne** pokazuje hoće li se vremenske transakcije ili troškovi rada na odabranom projektu uključiti u procjenu u ovom retku ponude. Vrijednost **Ne** označava da vremenske transakcije ili trošak rada neće biti uključeni u procjenu u ovom retku ponude. Vrijednost **Da** označava da će vremenske transakcije ili trošak rada biti uključeni u procjenu u ovom retku ponude. | Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi. |
| Uvrsti trošak | Vrijednost **Da**/**Ne** označava hoće li se troškovi izdataka na odabranom projektu uključiti u procjenu u ovom retku ponude. Vrijednost **Ne** označava da trošak izdatka neće biti uključen u procjenu u ovom retku ponude. Vrijednost **Da** označava da će trošak izdatka biti uključen u procjenu u ovom retku ponude. | Ova se vrijednost kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi. |
| Uvrsti materijal | Vrijednost **Da**/**Ne** označava hoće li se troškovi materijala na odabranom projektu uključiti u procjenu u ovom retku ponude. Vrijednost **Ne** označava da se troškovi materijala neće uključiti u procjenu u ovom retku ponude. Vrijednost **Da** označava da će se troškovi materijala uključiti u procjenu u ovom retku ponude. | Ova se vrijednost kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi. |
| Uvrsti naknadu | Vrijednost **Da**/**Ne** označava hoće li se naknade na odabranom projektu uključiti u procjenu u ovom retku ponude. Vrijednost **Ne** označava da se naknade neće uključiti u procjenu u ovom retku ponude. Vrijednost **Da** označava da će se naknade uključiti u procjenu u ovom retku ponude. | Ova se vrijednost kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi. |
| Ponuđeni iznos | Ovo je iznos koji će se ponuditi klijentu za sav posao predviđen u ovom retku ponude koja se temelji na projektu. U ponudi stvorenoj iz prilike, ova se vrijednost kopira iz polja **Proračun klijenta** u redak prilike. Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa iz pojedinosti retka ponude. | Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi. |
| Procijenjeni porez | Ovo je polje koje korisnik može uređivati kako bi dodao procijenjeni iznos poreza u redak ponude. Kada redak ponude koji se temelji na projektu sadrži pojedinosti retka, ovo se polje zaključava za uređivanje i sažima se od iznosa poreza iz pojedinosti retka ponude. | Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi. |
| Ponuđeni iznos nakon oporezivanja | Ovo je polje iznos retka ponude nakon oporezivanja i samo je za čitanje. Iznos u ovom polju izračunava se kao *Ponuđeni iznos + porez*. | Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi. |
| Ograničenje koje se ne smije prekoračiti | Ovo se polje može uređivati i dostupno je samo u redcima ponude koji se temelje na projektu i imaju način naplate **Vrijeme i materijal**. | Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi. |
| Proračun klijenta | Ovo se polje može uređivati i kopira se iz odgovarajućeg polja u retku prilike ako je ponuda stvorena iz prilike. | Ova vrijednost se kopira u redak ugovora o projektu koji se stvara iz ovog retka ponude kad ponuda pobijedi. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Pravila provjere valjanosti za polja na kartici Općenito redaka ponude koji se temelje na projektu

**Pravilo 1**: Ako je polje **Uključeni zadaci** prazno ili ako je postavljeno na **Svi projektni zadaci**, projekt je uključen u redak ponude.

**Pravilo 2**: Ako je polje **Uključeni zadaci** prazno ili je postavljeno na **Svi projektni zadaci**, projekt i određena klasa transakcija mogu se uključiti samo u jedan redak ponude koji se temelji na projektu.

**Pravilo 3**: Ako je polje **Uključeni zadaci** postavljeno na **Svi projektni zadaci**, projekt i određena klasa transakcija mogu se uključiti u više redaka ponude koji se temelji na projektu.

**Pravilo 4**: Ako prilika ima više ponuda, mogu postojati redci ponude iz različitih ponuda koji se svi odnose na isti projekt i uključuju istu klasu transakcije.

**Pravilo 5**: Ako ponude ne pripadaju istoj prilici, ne mogu obuhvaćati isti projekt i klasu transakcije.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Prilika</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Ponuda</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Redak ponude</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Uključeni zadaci</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Uvrsti vrijeme</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Uvrsti trošak</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Uvrsti materijal</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Uvrsti</strong>
                </p>
                <p>
                    <strong>Naknada</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Valjan / nije valjan</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Razlog</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Jest </p>
            </td>
            <td width="46" valign="top">
                <p>
Jest </p>
            </td>
            <td width="43" valign="top">
                <p>
Jest </p>
            </td>
            <td width="41" valign="top">
                <p>
Jest </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nije valjan </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 2. Vrijeme, trošak i naknade za projekt P1 uključeni su u retke ponude QL1 i QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Jest </p>
            </td>
            <td width="46" valign="top">
                <p>
Jest </p>
            </td>
            <td width="43" valign="top">
                <p>
Jest </p>
            </td>
            <td width="41" valign="top">
                <p>
Jest </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Jest </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Jest </p>
            </td>
            <td width="41" valign="top">
                <p>
Jest </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nije valjan </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 2. Vrijeme, materijal i naknade za projekt P1 uključeni su u retke ponude QL1 i QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Jest </p>
            </td>
            <td width="46" valign="top">
                <p>
Jest </p>
            </td>
            <td width="43" valign="top">
                <p>
Jest </p>
            </td>
            <td width="41" valign="top">
                <p>
Jest </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Jest </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Jest </p>
            </td>
            <td width="41" valign="top">
                <p>
Jest </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Valjano </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Vrijeme, materijal i naknade za projekt P1 uključeni su u QL1 <br>
Trošak za projekt P1 uključen je u QL2 <br>
Nema preklapanja onoga što je uključeno u svaki redak ponude i stoga vrijedi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Jest </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Samo odabrani zadaci </p>
            </td>
            <td width="45" valign="top">
                <p>
Jest </p>
            </td>
            <td width="46" valign="top">
                <p>
Jest </p>
            </td>
            <td width="43" valign="top">
                <p>
Jest </p>
            </td>
            <td width="41" valign="top">
                <p>
Jest </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nije valjan </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 2 </p>
                <p>
Q1 uključuje vrijeme, materijal, troškove i naknade za podskup zadataka na projektu P1 </p>
                <p>
QL2 uključuje vrijeme, troškove i naknade za cijeli projekt P1 i stoga se preklapa s onim što je uključeno u Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Jest </p>
            </td>
            <td width="46" valign="top">
                <p>
Jest </p>
            </td>
            <td width="43" valign="top">
                <p>
Jest </p>
            </td>
            <td width="41" valign="top">
                <p>
Jest </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Samo odabrani zadaci </p>
            </td>
            <td width="45" valign="top">
                <p>
Jest </p>
            </td>
            <td width="46" valign="top">
                <p>
Jest </p>
            </td>
            <td width="43" valign="top">
                <p>
Jest </p>
            </td>
            <td width="41" valign="top">
                <p>
Jest </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Valjano </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Prema pravilu br. 3, </p>
                <p>
Q1 uključuje vrijeme, materijal, troškove i naknade za podskup zadataka na projektu P1.
                </p>
                <p>
QL2 uključuje vrijeme, materijal, troškove i naknade za podskup zadataka na projektu P1.
                </p>
                <p>
Jedina dodatna provjera valjanosti odnosi se na podskup zadataka na QL1 koji se razlikuje od podskupa zadataka na QL2 kako bi se osiguralo da nema preklapanja. To čini sustav kada su zadaci povezani.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Samo odabrani zadaci </p>
            </td>
            <td width="45" valign="top">
                <p>
Jest </p>
            </td>
            <td width="46" valign="top">
                <p>
Jest </p>
            </td>
            <td width="43" valign="top">
                <p>
Jest </p>
            </td>
            <td width="41" valign="top">
                <p>
Jest </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Svi ili prazni projektni zadaci </p>
            </td>
            <td width="45" valign="top">
                <p>
Jest </p>
            </td>
            <td width="46" valign="top">
                <p>
Jest </p>
            </td>
            <td width="43" valign="top">
                <p>
Jest </p>
            </td>
            <td width="41" valign="top">
                <p>
Jest </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Valjano </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Prema pravilu br. 5, Q1 i Q2 dvije su ponude u istoj prilici, tako da oboje mogu procijeniti iste komponente projekta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
2. tromj. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Svi ili prazni projektni zadaci </p>
            </td>
            <td width="45" valign="top">
                <p>
Jest </p>
            </td>
            <td width="46" valign="top">
                <p>
Jest </p>
            </td>
            <td width="43" valign="top">
                <p>
Jest </p>
            </td>
            <td width="41" valign="top">
                <p>
Jest </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Svi ili prazni projektni zadaci </p>
            </td>
            <td width="45" valign="top">
                <p>
Jest </p>
            </td>
            <td width="46" valign="top">
                <p>
Jest </p>
            </td>
            <td width="43" valign="top">
                <p>
Jest </p>
            </td>
            <td width="41" valign="top">
                <p>
Jest </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nije valjan </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Prema pravilu br. 4, Q1 i Q2 dvije su ponude u različitim prilikama, tako da oboje ne mogu procijeniti iste komponente istog projekta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. tromj. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Svi ili prazni projektni zadaci </p>
            </td>
            <td width="45" valign="top">
                <p>
Jest </p>
            </td>
            <td width="46" valign="top">
                <p>
Jest </p>
            </td>
            <td width="43" valign="top">
                <p>
Jest </p>
            </td>
            <td width="41" valign="top">
                <p>
Jest </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
