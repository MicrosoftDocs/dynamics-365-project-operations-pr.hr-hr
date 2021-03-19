---
title: Postavljanje troškova i prodajnih cijena za troškove
description: U ovoj temi nalaze se informacije o načinu postavljanja troškova i prodajnih cijena za kategorije transakcije i troškova.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee52daae18c5f9f0b630e54359021fffe1759274
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274899"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Postavljanje troškova i prodajnih cijena za troškove

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U aplikaciji Dynamics 365 Project Operations možete postaviti cijene i prodajne cijene za kategorije transakcija. Budući da su cijene koštanja i prodajne cijene oblikovane za troškove, svaka kategorija transakcije koja ih uključuje također mora biti postavljena kao kategorija troškova. Ova postavka osigurava točnost u nizvodnoj funkcionalnosti. Cijene koštanja i prodajne cijene za kategorije transakcija mogu se navesti samo u jednoj valuti, koja mora biti valuta u zaglavlju cjenika.

Kako biste postavili cijene koštanja i prodajne cijene za kategorije transakcija, poduzmite sljedeće korake. 

1. Stvorite cjenik na temelju zaglavlja cjenika. 
2. U mogućnosti **Cijene kategorije**, na izborniku podrešetke, odaberite **+ Nova cijena kategorije**. 
3. Na stranici **Brzo stvaranje** unesite kategoriju transakcije i jedinicu za koju stvarate novu cijenu.

Sljedeća tablica prikazuje polja na kartici **Općenito** i stranici **Brzo stvaranje** retka cjenovne kategorije koju biste trebali imati na umu tijekom izrade cijena kategorija na prodajnom cjeniku ili cjeniku koštanja.

| Polje | Lokacija | Opis | Utjecaj na niže razine |
| --- | --- | --- | --- |
| Kategorija transakcije | Kartica **Općenito** i stranice **Brzo stvaranje** | Odaberite kategoriju transakcije za koju stvarate prodajnu cijenu ili cijenu troška. | Kategorija transakcije na dolaznoj procjeni ili stvarnoj vrijednosti troškova podudarat će se s ovim retkom kako bi se zadali troškova ili prodajna cijena kategorije transakcije. |
| Raspored jedinica | Kartica **Općenito** i stranice **Brzo stvaranje** | Raspored jedinica zadan je iz rasporeda jedinica kategorije transakcije. | Iz ovog polja nema utjecaja na niže razine. |
| Jedinica | Kartica **Općenito** i stranice **Brzo stvaranje** | Odaberite jedinicu za koju se postavljaju cijene. | Jedinica na dolaznoj procjeni ili stvarnoj vrijednosti usklađuje se s jedinicom na ovom retku kako bi se zadala cijena na procjeni troškova ili njihovoj stvarnoj vrijednosti. |
| Način određivanja cijena | Kartica **Općenito** i stranice **Brzo stvaranje** | Moguće vrijednosti polja **Način određivanja cijene** su **Cijena po jedinici**, **Po trošku** i **Marža na trošak**. | Tijekom postavljanja cijene, odabirom mogućnosti **Cijena po jedinici** zaključava se polje **Postotak** na retku cijene kategorije. Ako se odabere **Po trošku**, u prodajnom se cjeniku zaključavaju polja **Cijena** i **Postotak**. Odabirom mogućnosti **Marža na trošak** zaključava se polje **Cijena** na prodajnom cjeniku. Način određivanja cijene **Po trošku** ili **Marža na trošak** na dolaznom retku stvarne vrijednosti troška rezultira time da se odgovarajućem nenaplaćenom prodajnom retku dodjeljuje cijena koja je jednaka stvarnoj cijeni koštanja ili se izračunava kao marža na cijenu. |
| Cijena | Kartica **Općenito** i stranice **Brzo stvaranje** | Postavite cijenu po jedinici za kategoriju transakcije i kombinaciju jedinica. Na primjer, cijena prijeđenih kilometara je 10 USD po milji i 8 USD po kilometru. | Cijena prijeđenih kilometara bit će cijena koja zadaje cijenu po jedinici ili trošak dolazne procjene ili retka stvarne vrijednosti za klasu transakcije troškova.|
| Postotak | Kartica **Općenito** i stranice **Brzo stvaranje** | Postavite postotak na trošak za kategoriju transakcije i kombinaciju jedinica. Na primjer, prodajna cijena zrakoplovnih karata trebala bi biti viša za 10 posto u odnosu na cijenu nastalih zrakoplovnih troškova. | Taj postotak na trošak primjenjiv je samo za prodajni cjenik kada je za određivanje cijene odabran način **Marža na trošak**. |
| Valuta | Kartica **Općenito** i stranice **Brzo stvaranje** | Prema zadanim postavkama, ova vrijednost dolazi iz valute u zaglavlju cjenika. Za određivanje cijene kategorije transakcije valutu nije moguće poništiti. | Ova valuta zadaje jedinična cijena retka dolazne stvarne vrijednosti za klasu troškova transakcije za trošak i prodaju. |

## <a name="pricing-methods-for-expenses"></a>Načini određivanja cijene koštanja

Kada postavljate cijene kategorija koje su relevantne samo u kontekstu određivanja troškova, možete upotrebljavati jedan od sljedeća tri načina određivanja cijena:

- **Jedin. cijena**
- **Uz trošak**
- **Marža na trošak**

### <a name="price-per-unit"></a>Jedin. cijena
Kada je ovaj način određivanja cijene odabran na retku cijene kategorije koja je povezana s prodajnim cjenikom, cijena je zadana za kombinaciju kategorije i jedinice i u procjeni i u stvarnoj vrijednosti. Procjena se odnosi na retke procjene projekta za troškove, na pojedinosti retka ponude i pojedinosti retka ugovora za troškove.

### <a name="at-cost"></a>Uz trošak
Kada je ovaj način određivanja cijene odabran na retku cijene kategorije koja je povezana s prodajnim cjenikom, cijena je zadana za kombinaciju kategorije i jedinice samo za stvarnu vrijednost troška. Na primjer, nenaplaćene stvarne prodajne vrijednosti za klasu transakcije troška. Jedinična cijena se postavlja na nenaplaćenu stvarnu prodajnu vrijednost iz jedinične cijene stvarne vrijednosti troška za taj trošak. Cijena koja je zadana na temelju troškova nije napravljena na temelju projektnih procjena za troškove ili pojedinosti retka ponude i retka ugovora za troškove.

### <a name="markup-over-cost"></a>Marža na trošak
Kada je ovaj način određivanja cijene odabran na retku cijene kategorije koja je povezana s prodajnim cjenikom, cijena je zadana za kombinaciju kategorije i jedinice samo za stvarnu vrijednost troška. Na primjer, nenaplaćene stvarne prodajne vrijednosti za klasu transakcije troška. Ova jedinična cijena postavlja se na stvarnoj vrijednosti nenaplaćene prodaje na izračunanu vrijednost iz jedinične cijene na stvarnoj vrijednosti troška za taj trošak, nakon što se primijeni definirani postotak marže. Cijena koja je zadana na temelju troškova nije napravljena na temelju projektnih procjena za troškove ili pojedinosti retka ponude i retka ugovora za troškove.


[!INCLUDE[footer-include](../includes/footer-banner.md)]