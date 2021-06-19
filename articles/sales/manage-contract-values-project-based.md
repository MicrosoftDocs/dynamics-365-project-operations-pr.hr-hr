---
title: Rad s redcima ugovora koji se temelje na projektu
description: U ovoj temi nalaze se informacije o redcima ugovora koji se temelje na projektu.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2072692296308a08756ec3e0f381c792745dd3e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011497"
---
# <a name="work-with-projectbased-contract-lines"></a>Rad s redcima ugovora koji se temelje na projektu

Redci ugovora koji se temelje na projektu u aplikaciji Dynamics 365 Project Operations dizajnirani su da drže angažirane ugovore o procjeni i naplati za određene komponente projektnog rada. Struktura retka ugovora koji se temelji na projektu proširena je za procjene projekta i scenarije naplate sa sljedećim konceptima:

- Način naplate
- Mapiranje projekta i zadatka
- Uključene klase transakcije
- Ograničenje koje se ne smije prekoračiti
- Postavka naplativosti
- Procjene s pomoću pojedinosti retka ugovora
- Klijenti retka ugovora

Sljedeća su polja uključena u karticu **Općenito** redaka ugovora koji se temelje na projektu. Ta polja pomažu pri postavljanju osnove za podrobnu, temeljnu procjenu i aranžmane naplate za posao koji se temelji na projektu .

| Polje | Opis | Utjecaj na niže razine |
| --- | --- | --- |
| **Ime** | Naziv retka ugovora koji identificira određenu komponentu ugovora koja se procjenjuje. Za ugovor o projektu stvoren iz ponude, ova se vrijednost kopira iz odgovarajuće vrijednosti retka ponude koja se temelji na projektu. | Vrijednost ovog polja kopira se u redak fakture za projekt koji se stvara iz ovog retka ugovora kada se stvara faktura. |
| **Način naplate** | U ugovoru o projektu stvorenom iz ponude ova se vrijednost kopira iz odgovarajućeg polja retka ponude. Ovo je skup mogućnosti koji predstavlja dva glavna modela ugovaranja koje podržava aplikacija Project Operations:</br>- **Fiksna cijena**</br>- **Vrijeme i materijal** | Na temelju načina naplate navedenog retka ugovora, obradit će se stvarna transakcija. Ako redak ugovora na koji se odnosi stvarna vrijednost ima način naplate vremena i materijala, stvara se stvarni zapis troška i nenaplaćene prodaje. Ako redak ugovora na koji se poziva stvarni podatak ima način naplate s fiksnom cijenom, stvara se samo stvarni trošak. |
| **Project** | Upotrijebite ovo polje za identificiranje projekta koji će se upotrijebiti za izvođenje posla na ovom angažmanu. | Vrijednost u ovom polju upotrebljava se zajedno s poljima **Uključeni zadaci** i **Uključene klase transakcija** za rješavanje reference retka ugovora na stvarnom ili procijenjenom zapisu. |
| **Uvrsti vrijeme** | Zastavica označava jesu li vremenske transakcije ili troškovi rada na odabranom projektu uključeni u taj redak ugovora. Vrijednost **Ne** znači da vremenske transakcije ili troškovi rada neće biti uključeni u ovaj redak ugovora. Vrijednost **Da** označava da hoće. | Ova vrijednost polja upotrebljava se zajedno s projektom za rješavanje reference retka ugovora na stvarnom ili procijenjenom zapisu. |
| **Uvrsti trošak** | Zastavica označava hoće li cijena troška na odabranom projektu biti uključeni u taj redak ugovora. Vrijednost **Ne** znači da cijena troška neće biti uključena u ovaj redak ugovora. Vrijednost **Da** označava da hoće. | Ova vrijednost polja upotrebljava se zajedno s projektom za rješavanje reference retka ugovora na stvarnom ili procijenjenom zapisu. |
| **Uvrsti naknadu** | Zastavica označava hoće li naknade na odabranom projektu biti uključene u taj redak ugovora. Vrijednost **Ne** znači da naknade neće biti uključene u ovaj redak ugovora. Vrijednost **Da** označava da hoće. | Ova vrijednost polja upotrebljava se zajedno s projektom za rješavanje reference retka ugovora na stvarnom ili procijenjenom zapisu. |
| **Ugovoreni iznos** | Na retku ugovora s fiksnom cijenom ovo je dogovorena vrijednost koja će se fakturirati klijentu za sve komponente posla povezane s ovim retkom ugovora. Na retku ugovora za vrijeme i materijal ovaj je iznos procijenjena vrijednost onoga što će se fakturirati klijentu za sve komponente posla povezane s ovim retkom ugovora. U ugovoru o projektu stvorenom iz ponude ova se vrijednost kopira iz odgovarajućeg polja retka ponude. Kada redak ugovora koji se temelji na projektu ima pojedinosti retka, ovo je polje zaključano za uređivanje i sažeto je od iznosa pojedinosti retka ugovora. | Kada redak ugovora sadrži pojedinosti o retku, ta se vrijednost može izmijeniti promjenom iznosa na pojedinostima retka. Na retku ugovora s fiksnom cijenom, ova se vrijednost upotrebljava za generiranje iznosa prije poreza na periodičnim kontrolnim točkama naplate. |
| **Procijenjeni porez** | Korisnik može urediti ovo polje za unos procijenjenog iznosa poreza u redak ugovora. Kada redak ugovora koji se temelji na projektu ima pojedinosti retka, ovo je polje zaključano za uređivanje i sažeto je od iznosa poreza u pojedinostima retka ugovora. | Kada redak ugovora sadrži pojedinosti o retku, ta se vrijednost može izmijeniti promjenom iznosa poreza na pojedinostima retka. Na retku ugovora s fiksnom cijenom, ova se vrijednost upotrebljava za generiranje poreza na periodičnim kontrolnim točkama naplate. |
| **Ugovoreni iznos nakon poreza** | Iznos retka ugovora nakon poreza. Ovo je polje samo za čitanje i izračunava se kao **Ugovoreni iznos + porez**. | Na retku ugovora s fiksnom cijenom, ova se vrijednost upotrebljava za generiranje periodičnih kontrolnih točaka naplate. |
| **Ograničenje koje se ne smije prekoračiti** | Korisnik može uređivati ovo polje i ono je dostupno samo na redcima ugovora koji se temelje na projektu i imaju način naplate vremena i materijala. | Korisnik može uređivati ovo polje. Kada se stvarno vrijeme ili trošak odnosi na ovaj redak ugovora za vrijeme i materijal, iznos na stvarnoj vrijednosti procjenjuje se prema ograničenju koje se ne smije premašiti u ovom retku ugovora nakon obračunavanja već potrošenih i angažiranih iznosa. |
| **Proračun klijenta** | Ovo se polje može uređivati i kopira se iz odgovarajućeg polja na retku ponude, ako je ugovor stvoren iz ponude. | Ovo se polje upotrebljava samo za informacije i nema nikakvo daljnje značenje. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Pravilo provjere valjanosti mogućnosti na kartici Općenito redaka ugovora koji se temelje na projektu

Pravilo: Projekt i određena klasa transakcije mogu biti uključeni samo u jedan redak ugovora koji se temelji na projektu u ugovoru.

| Ugovor | Redak ugovora | Project | Uvrsti vrijeme | Uvrsti trošak | Uvrsti naknadu | Valjan / nije valjan | Razlog                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Jest          | Jest             | Jest         | Nije valjan       | Krši pravilo. Vrijeme, trošak i naknade za projekt P1 uključeni su u oba retka ugovora, CL1 i CL2.                                                                                       |
| C1       | CL2           | P1      | Jest          | Jest             | Jest         | Nije valjan       | Krši pravilo. Vrijeme, trošak i naknade za projekt P1 uključeni su u oba retka ugovora, CL1 i CL2.                                                                                       |
| C1       | CL1           | P1      | Jest          | No              | Jest         | Nije valjan       | Krši pravilo. Vrijeme i naknade za projekt P1 uključeni su u oba retka ugovora, CL1 i CL2.                                                                                                   |
| C1       | CL2           | P1      | Jest          | Jest             | Jest         | Nije valjan       | Krši pravilo. Vrijeme i naknade za projekt P1 uključeni su u oba retka ugovora, CL1 i CL2.                                                                                                   |
| C1       | CL1           | P1      | Jest          | No              | Jest         | Valjano           | Vrijeme i naknade za projekt P1 uključeni su u CL1. Trošak za projekt P1 uključen je u CL2. </br>   Nema preklapanja onoga što je uključeno u svaki redak ugovora i stoga je valjano.  |
| C1       | CL2           | P1      | No           | Jest             | No          | Valjano           | Vrijeme i naknade za projekt P1 uključeni su u CL1. Trošak za projekt P1 uključen je u CL2. </br>   Nema preklapanja onoga što je uključeno u svaki redak ugovora i stoga je valjano.  |
| C1       | CL1           | P1      | Jest          | Jest             | Jest         | Nije valjan       | Krši pravilo. Vrijeme, trošak i naknade za projekt P1 uključeni su u retke dva ugovora.                                                                                               |
| CL2      | CL2           | P1      | Jest          | Jest             | Jest         | Nije valjan       | Krši pravilo. Vrijeme, trošak i naknade za projekt P1 uključeni su u retke dva ugovora.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]