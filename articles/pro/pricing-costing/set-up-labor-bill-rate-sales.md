---
title: Postavljanje cijena za naplatu rada – jednostavno
description: U ovoj temi nalaze se informacije o postavljanju cijena za naplatu radne snage u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf53f6909ed5fb9b143197118c799b9803699171
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181170"
---
# <a name="set-up-labor-bill-rates---lite"></a>Postavljanje cijena za naplatu rada – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Svaki cjenik ima skup cijena uloga ili cijena radne snage koje su na snazi u kontekstu, a datumu stupanja na snagu uključen u zaglavlje cjenika. Cijene naplate za vrijeme u aplikaciji Dynamics 365 Project Operations mogu se postaviti u samo jednoj valuti, koja je valuta u zaglavlju Cjenika.

1. Kako biste postavili cijene naplate za radnu snagu za prodajni cjenik, stvorite cjenik na temelju zaglavlja cjenika. 
2. Na kartici **Cijene uloga**, u podrešetki, odaberite **+ Nova cijena uloge**. 
3. U oknu **Brzo stvaranje** unesite kombinaciju uloge i organizacijske jedinice za koju trebate postaviti cijenu naplate.

  Sljedeća tablica uključuje polja na kartici **Općenito** i oknu **Brzo stvaranje** retka cjene uloge koju biste trebali imati na umu tijekom izrade cijena uloga na prodajnom cjeniku:

  | Polje | Lokacija | Opis | Utjecaj na niže razine |
  | --- | --- | --- | --- |
  | Uloga | Kartica **Općenito** i okno **Brzo stvaranje** | Odaberite ulogu za koju postavljate cijenu naplate. | Uloga na dolaznoj procjeni ili stvarnoj vrijednosti podudarit će se s ovim retkom kako bi se zadala cijena naplate uloge. |
  | Jedinica za resurse | Kartica **Općenito** i okno **Brzo stvaranje** | Odaberite organizacijsku jedinicu ili sektor tvrtke iz koje je preuzeta uloga. Na primjer, razvojni inženjer iz sektora Robotics tvrtke Fabrikam India ili razvojni inženjer iz sektora softvera tvrtke Fabrikam USA. | Jedinica za određivanje resursa na dolaznoj procjeni ili stvarnoj vrijednosti podudarat će se s ovim retkom kako bi se zadala cijena naplate uloge. |
  | Cijena | Kartica **Općenito** i okno **Brzo stvaranje** | Postavite cijenu naplate za ulogu kombinacije tvrtke za raspodjelu resursa i jedinice za raspodjelu resursa. Na primjer, razvojni inženjer iz tvrtke Fabrikam India ima cijenu naplate 100 USD ili razvojni inženjer iz tvrtke Fabrikam USA ima cijenu naplate 150 USD. | Ta cijena zadana je cijena naplate jedinične cijene dolazne procjene ili retka stvarne vrijednosti za klasu vremenske transakcije. |
  | Valuta | Kartica **Općenito** i okno **Brzo stvaranje**| Prema zadanim postavkama, vrijednost valute dolazi iz valute koja se nalazi u zaglavlju prodajnog cjenika. Na prodajnom se cjeniku valuta ne može nadjačati. | Ova valuta zadana je valuta jedinične cijene retka dolazne stvarne prodajne vrijednosti za klasu vremenske transakcije. |
  | Raspored jedinica | Kartica **Općenito** i okno **Brzo stvaranje** | Ovaj je raspored jedinica zadan je za Vrijeme i ne može se mijenjati na entitetu cijene uloge jer se upotrebljava za izražavanje cijena prema jedinicama vremena. | Ovo polje ne utječe na niže razine. |
  | Jedinica | Kartica **Općenito** i okno **Brzo stvaranje** | Vrijednost jedinice dolazi iz polja **Vremenska jedinica** koje se nalazi u zaglavlju prodajnog cjenika. No, vrijednost se može nadjačati. Na primjer, razvojni inženjer iz tvrtke Fabrikam India ima cijenu za naplatu od 1000 USD po **Danu u Indiji**. Razvojni programer iz tvrtke Fabrikam USA ima cijenu naplate od 1500 USD po **Danu SAD-a**. | Kada je jedinična cijena zadana na retku dolazne procjene ili stvarne vrijednosti, sustav upotrebljava sustav jedinica i pretvorbu u osnovnim jedinicama za izračunavanje jedinične cijene. Na primjer, procjena je za 10 **Dana Indije** vrijedi raditi za razvojnog inženjera iz Indije, a jedinica Dana Indije definirana je kao 10 sati. Pri određivanju cijene retka procjene, aplikacija izračunava jediničnu cijenu na procjeni kao 1000 USD / 10 sati = 100 USD po satu. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Cijene prijenosa ili postavljanje cijene naplate za resurse iz drugih organizacijskih jedinica ili sektora 

Projektne tvrtke upotrebljavaju zaposlenike iz različitih sektora tvrtke za rad na projektima. Projekti se mogu izvršavati iz jednog sektora, dok zaposlenici ili savjetnici dolaze iz istog ili drugog sektora tvrtke. Projekt bi također mogla izraditi kombinacija ljudi iz različitih sektora. U aplikaciji Project Operations, tvrtka koja je vlasnik isporuke projekta naziva se **Ugovorna jedinica**. Svi ostali sektori koji osiguravaju resurse nazivaju se **Jedinice za raspodjelu resursa**. Zbog razlika u troškovima radne snage na različitim zemljopisnim područjima i tržištima rada širom svijeta, cijene naplate rada također se različito postavljaju za različite zemljopisne regije.

Na primjer, razvojnom inženjeru iz tvrtke Fabrikam India, koji radi na američkom projektu, plaća se cijena od 100 USD po satu. Razvojnom inženjeru iz tvrtke Fabrikam US koji radi na projektu US Project plaća se 150 USD po satu.

### <a name="example-set-up-a-bill-rate"></a>Primjer: Postavljanje cijene naplate

1. Stvorite prodajni cjenik pod nazivom *Cijene naplate za Fabrikam US* i postavite datum stupanja na snagu.
2. U prodajni cjenik unesite sljedeće podatke o cijeni:

    | Uloga | Organizacijska jedinica | Stopa naplate |
    | --- | --- | --- |
    | Razvojni programer | Fabrikam India | $100 |
    | Razvojni programer | Fabrikam Philippines | 90 USD |
    | Razvojni programer | Fabrikam US | 150 USD |

3. Priložite prodajni cjenik **Cijene naplate za Fabrikam US** cjeniku ugovora o projektu ili na određenom računu.
