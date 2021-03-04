---
title: Postavljanje cijena koštanja rada – jednostavno
description: U ovoj temi nalaze se informacije o načinu postavljanja troškova radne snage u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2e79dde867833fb952349c073ce8975381029dcf
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180696"
---
# <a name="set-up-labor-cost-rates---lite"></a>Postavljanje cijena koštanja rada – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Svaki cjenik ima skup cijena radne snage (cijena uloge) koje su u skladu sa sadržajem i datumom stupanja na snagu cjenika.

1. Stvorite cjenik i na kartici **Cijena uloge** u podrešetki odaberite **Nova uloga**.
2. Na stranici **Brzo stvaranje**, odaberite ulogu i organizacijsku jedinicu.
3. Unesite sve druge obvezne podatke.

Sljedeća tablica uključuje neka polja koja su bitna za stvaranje cijena radne snage na cjeniku troškova.

| Polje | Lokacija | Opis | Utjecaj na niže razine |
| --- | --- | --- | --- |
| Uloga | Kartica **Općenito** i stranice **Brzo stvaranje** | Odaberite ulogu na koju se troškova primjenjuje. | Uloga na dolaznoj procjeni ili stvarnoj vrijednosti podudarit će se s ovim retkom kako bi se zadala cijena uloge. |
| Jedinica za resurse | Kartica **Općenito** i stranice **Brzo stvaranje** | Odaberite organizacijsku jedinicu ili sektor tvrtke iz koje će se uzeti ta uloga za uporabu. Na primjer, razvojni inženjer iz sektora Robotics tvrtke Fabrikam India ili razvojni inženjer iz sektora softvera tvrtke Fabrikam USA. | Jedinica za određivanje resursa na dolaznoj procjeni ili stvarnoj vrijednosti podudarat će se s ovim retkom kako bi se zadala cijena uloge. |
| Cijena | Kartica **Općenito** i stranice **Brzo stvaranje** | Postavite cijenu koštanja za kombinaciju uloge, tvrtke za raspodjelu resursa i jedinice za raspodjelu resursa. Na primjer, razvojni inženjer iz tvrtke Fabrikam India košta 1000 INR ili razvojni inženjer iz tvrtke Fabrikam USA košta 150 USD. | Cijena je troškova koja zadaje cijenu po jedinici dolazne procjene ili retka stvarne vrijednosti za klasu transakcije **Vrijeme**. |
| Valuta | Kartica **Općenito** i stranice **Brzo stvaranje** | Prema zadanim postavkama, vrijednost valute dolazi iz valute koja se nalazi u zaglavlju cjenika troškova, ali se može nadjačati. Na primjer, razvojni inženjer iz tvrtke Fabrikam India košta 1000 INR. Razvojni inženjer iz tvrtke Fabrikam USA košta 150 USD. | Ova valuta zadana je valuta jedinične cijene retka dolazne stvarne vrijednosti troška za klasu transakcije **Vrijeme**. Na procjeni projekta, vrijednost valute pretvara se u valutu projekta i prikazuje na prikazu vremenskih faza procjene. |
| Raspored jedinica | Kartica **Općenito** i stranice **Brzo stvaranje** | Ovaj je raspored jedinica zadan je za Vrijeme i ne može se mijenjati na entitetu cijene uloge jer se upotrebljava za izražavanje cijena prema jedinicama vremena. | Nema nizvodnog utjecaja. |
| Jedinica | Kartica **Općenito** i stranice **Brzo stvaranje** | Prema zadanim postavkama, vrijednost dolazi iz polja **Vremenska jedinica** koje se nalazi u zaglavlju cjenika troškova. Vrijednost se može nadjačati. Na primjer, razvojni inženjer iz tvrtke Fabrikam India košta 1000 INR po **Danu u Indiji**. Razvojni inženjer iz tvrtke Fabrikam USA košta 150 USD po **Danu u SAD-u**. | Sustav upotrebljava sustav jedinica i pretvorbu u osnovnim jedinicama za izračunavanje jedinične cijene troška za izračun zadane jedinične cijene na retku dolazne procjene ili stvarnog podatka. Na primjer, procjena je za 10 **Indijskih dana** vrijednosti posla za razvojnog inženjera iz Indije, a jedinica **Indijski dan** definirana je kao 10 sati. Kada određuje koštanje tog retka procjene, aplikacija izračunava jedinični trošak na procjeni kao: 1000 INR / 10 sati = 100 INR po satu, što se pretvara u USD i prikazuje kao jedinični trošak na stranici **Procjene projekta**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Prijenos cijene i troškova za resurse izvan svojeg sektora ili pravne osobe

U projektnim je tvrtkama uobičajena uporaba zaposlenika iz različitih pravnih osoba ili sektora za rad na projektima. Projekt može izvršiti jedna pravna osoba, ali zaposlenici ili savjetnici koji rade na projektu mogu dolaziti iz iste pravne osobe ili iz neke druge tj. može se raditi o kombinacije obje. U aplikaciji Dynamics 365 Project Operations, pravna osoba koja je vlasnik isporuke projekta je **Tvrtka vlasnik**, a sektor koji je vlasnik isporuke je **Ugovorna jedinica**. Ostale pravne osobe koje osiguravaju resurse su **Tvrtke za raspodjelu resursa**, a sektori koji osiguravaju resurse su **Jedinice za raspodjelu resursa**. U većini zemalja tvrtke su dužne osigurati da pravna osoba ili sektor za raspodjelu resursa naplaćuju uporabu resursa tvrtki vlasnici i ugovornoj jedinici.

Na primjer, tvrtka Fabrikam mora osigurati da Fabrikam India-Robotics pregovara o kartici cijene troška s Fabrikam US-Robotics ili Fabrikam UK-Robotics.

Razvojni inženjer iz tvrtke Fabrikam India-Robotic košta 100 USD kada je posuđen tvrtki Fabrikam US-Robotics i 150 USD kada je posuđen tvrtki Fabrikam U-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Postavljanje troškova vanjskih resursa

1. Stvorite cjenik troškova pod nazivom, *Cijene troškova za tvrtku Fabrikam US-Robotics* i postavite datumski raspon primjene.
2. U cjeniku troška postavite cijene s pomoću podataka iz sljedeće tablice. 

| Uloga | Tvrtka resursa | Jedinica za resurse | Stopa troška |
| --- | --- | --- | --- |
| Razvojni programer | Fabrikam India | Fabrikam India-Robotics | $100 |
| Razvojni programer | Fabrikam Philippines | Fabrikam Philippines-Robotics | 90 USD |
| Razvojni programer | Fabrikam US | Fabrikam US-Robotics | 150 USD |

3. Priložite ovaj cjenik troškova organizacijskoj jedinici Fabrikam US-Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Postavljanje prijenosa cijene za resurs u odgovarajućoj valuti 

U aplikaciji Project Operations cijene resursa mogu se postaviti u bilo kojoj valuti. Valuta je prema zadanim postavkama navedena u zaglavlju cjenika, ali se može promijeniti.

S pomoću primjera za postavljanje cijene prijenosa podaci bi se mogli promijeniti u sljedeće:

Tvrtka Fabrikam mora osigurati da Fabrikam India-Robotics pregovara o cijeni troška s tvrtkom Fabrikam US-Robotics ili Fabrikam UK-Robotics.

Razvojni inženjer iz tvrtke Fabrikam India-Robotics košta 5000 INR kada je posuđen tvrtki Fabrikam US-Robotics i 5500 INR kada je posuđen tvrtki Fabrikam UK-Robotics.

U cjeniku troškova za tvrtku Fabrikam US-Robotics cijene troška mogu se izraziti kao:

| Uloga | Tvrtka resursa | Cijena |
| --- | --- | --- |
| Razvojni programer | Fabrikam India | 5000 INR |
| Razvojni programer | Fabrikam US | 115 USD |

U cjeniku troškova za tvrtku Fabrikam UK-Robotics cijene troška mogu se izraziti kao:

| Uloga | Tvrtka resursa | Cijena |
| --- | --- | --- |
| Razvojni programer | Fabrikam India | 5500 INR |
| Razvojni programer | Fabrikam UK | 115 GBP |

Cjenik troškova može osigurati cijene radne snage u više valuta. Pri generiranju procjene troškova na projektu, Project Operations pretvorit će ove cijene troškova u valutu projekta i prikazati ih korisniku. Kada se odobri unos vremena i stvori stvarni trošak, cijena stvarnog troška određuje se u valuti retka cijene odgovarajuće uloge na cjeniku troškova. Stvarni troškovi vremena u pojedinom projektu mogu se evidentirati u više valuta. Međutim, prilikom kumuliranja ili sažimanja stvarnih troškova radne snage na razini projekta, Project Operations pretvorit će sve iznose troškova radne snage u valutu projekta, koju korisnik može vidjeti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]