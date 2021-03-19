---
title: Postavljanje cijena za naplatu radne snage
description: U ovoj temi nalaze se informacije o načinu postavljanja cijena za naplatu radne snage u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b4d09f4bf6788f93c028f084965faa6aac41a22d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274809"
---
# <a name="set-up-labor-bill-rates"></a>Postavljanje cijena za naplatu rada

**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha

Svaki cjenik ima skup cijena uloga ili cijena radne snage koje su na snazi u kontekstu, a datumu stupanja na snagu uključen u zaglavlje cjenika. Cijene naplate vremena u aplikaciji Dynamics 365 Project Operations mogu se postaviti u samo jednoj valuti, koja je navedena u zaglavlju Cjenika.

1. Kako biste postavili cijene naplate za radnu snagu za prodajni cjenik, stvorite cjenik na temelju zaglavlja cjenika. 
2. Na kartici **Cijene uloga**, u podrešetki, odaberite **+ Nova cijena uloge**. 
3. U oknu **Brzo stvaranje** unesite kombinaciju uloge i organizacijske jedinice za koju trebate postaviti cijenu naplate.

   Sljedeća tablica uključuje polja na kartici **Općenito** i oknu **Brzo stvaranje** retka cjene uloge koju biste trebali imati na umu tijekom izrade cijena uloga na prodajnom cjeniku:

    | Polje | Lokacija | Opis | Utjecaj na niže razine |
    | --- | --- | --- | --- |
    | Uloga | Kartica **Općenito** i okno **Brzo stvaranje** | Odaberite ulogu za koju postavljate cijenu naplate. | Uloga na dolaznoj procjeni ili stvarnoj vrijednosti podudarit će se s ovim retkom kako bi se zadala cijena naplate uloge. |
    | Tvrtka resursa | Kartica **Općenito** i okno **Brzo stvaranje** | Odaberite tvrtku ili pravnu osobu iz koje je uloga. Na primjer, razvojni inženjer iz tvrtke Fabrikam India ili razvojni inženjer iz tvrtke Fabrikam USA. | Tvrtka za određivanje resursa na dolaznoj procjeni ili stvarnoj vrijednosti podudarat će se s ovim retkom kako bi se zadala cijena naplate uloge. |
    | Jedinica za resurse | Kartica **Općenito** i okno **Brzo stvaranje** | Odaberite organizacijsku jedinicu ili sektor tvrtke iz koje je preuzeta uloga. Na primjer, razvojni inženjer iz sektora Robotics tvrtke Fabrikam India ili razvojni inženjer iz sektora softvera tvrtke Fabrikam USA. | Jedinica za određivanje resursa na dolaznoj procjeni ili stvarnoj vrijednosti podudarat će se s ovim retkom kako bi se zadala cijena naplate uloge. |
    | Cijena | Kartica **Općenito** i okno **Brzo stvaranje** | Postavite cijenu naplate za ulogu kombinacije tvrtke za raspodjelu resursa i jedinice za raspodjelu resursa. Na primjer, razvojni inženjer iz tvrtke Fabrikam India ima cijenu naplate 100 USD ili razvojni inženjer iz tvrtke Fabrikam USA ima cijenu naplate 150 USD. | Ta cijena zadana je cijena naplate jedinične cijene dolazne procjene ili retka stvarne vrijednosti za klasu vremenske transakcije. |
    | Valuta | Kartica **Općenito** i okno **Brzo stvaranje**| Prema zadanim postavkama, vrijednost valute dolazi iz valute koja se nalazi u zaglavlju prodajnog cjenika. Na prodajnom se cjeniku valuta ne može nadjačati. | Ova valuta zadana je valuta jedinične cijene retka dolazne stvarne prodajne vrijednosti za klasu vremenske transakcije. |
    | Raspored jedinica | Kartica **Općenito** i okno **Brzo stvaranje** | Ovaj je raspored jedinica zadan je za Vrijeme i ne može se mijenjati na entitetu cijene uloge jer se upotrebljava za izražavanje cijena prema jedinicama vremena. | Ovo polje ne utječe na niže razine. |
    | Jedinica | Kartica **Općenito** i okno **Brzo stvaranje** | Vrijednost jedinice dolazi iz polja **Vremenska jedinica** koje se nalazi u zaglavlju prodajnog cjenika. No, vrijednost se može nadjačati. Na primjer, razvojni inženjer iz tvrtke Fabrikam India ima cijenu za naplatu od 1000 USD po **Danu u Indiji**. Razvojni programer iz tvrtke Fabrikam USA ima cijenu naplate od 1500 USD po **Danu SAD-a**. | Kada je jedinična cijena zadana na retku dolazne procjene ili stvarne vrijednosti, sustav upotrebljava sustav jedinica i pretvorbu u osnovnim jedinicama za izračunavanje jedinične cijene. Na primjer, procjena je za 10 **Dana Indije** vrijedi raditi za razvojnog inženjera iz Indije, a jedinica Dana Indije definirana je kao 10 sati. Pri određivanju cijene retka procjene, aplikacija izračunava jediničnu cijenu na procjeni kao 1000 USD / 10 sati = 100 USD po satu. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Cijene prijenosa ili postavljanje cijene naplate za resurse iz drugih organizacijskih jedinica ili sektora 

Projektne tvrtke često upotrebljavaju zaposlenike iz različitih pravnih osoba i različitih sektora unutar pravne osobe za rad na projektima. Projekti se mogu izvršavati od određene pravne osobe i odjela, dok zaposlenici ili savjetnici koji rade na projektima mogu poticati iz iste pravne osobe ili odjela ili iz druge. Projekt bi također mogla izraditi kombinacija ljudi iz različitih pravnih osoba i sektora. U aplikaciji Project Operations, pravna osoba koja je vlasnik isporuke projekta naziva se **Tvrtka vlasnik**, a sektor koji je vlasnik isporuke naziva se **Ugovorna jedinica**. Pozvane su sve ostale pravne osobe koje osiguravaju resurse **Tvrtke za raspodjelu resursa**, a sektori koji osiguravaju resurse nazivaju se **Jedinice za raspodjelu resursa**. Zbog razlika u troškovima radne snage na različitim zemljopisnim područjima i tržištima rada širom svijeta, cijene naplate rada također se različito postavljaju za različite zemljopisne regije.

Na primjer, razvojnom inženjeru iz sektora Robotics tvrtke Fabrikam India, koji radi na projektu iz SAD-a, plaća se cijena od 100 USD po satu. Razvojnom inženjeru iz sektora Robotics tvrtke Fabrikam US koji radi na projektu iz SAD-a plaća se 150 USD po satu. 

### <a name="example-set-up-a-bill-rate"></a>Primjer: Postavljanje cijene naplate 

1. Stvorite prodajni cjenik pod nazivom *Cijene naplate za Fabrikam US* i postavite datum stupanja na snagu.
2. U prodajni cjenik unesite sljedeće podatke o cijeni:

    | Uloga | Tvrtka resursa | Jedinica za resurse | Stopa naplate |
    | --- | --- | --- | --- |
    | Razvojni programer | Fabrikam India | Fabrikam India – Robotics | $100 |
    | Razvojni programer | Fabrikam Philippines | Fabrikam Philippines – Robotics | 90 USD |
    | Razvojni programer | Fabrikam US | Fabrikam US – Robotics | 150 USD |

3. Priložite prodajni cjenik **Cijene naplate za Fabrikam US** cjeniku ugovora o projektu ili na određenom računu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]