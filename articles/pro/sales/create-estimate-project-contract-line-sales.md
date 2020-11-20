---
title: Procjena retka ugovora koji se temelji na projektu – osnovna
description: Ovaj tema pruža informacije o procjeni retka ugovora koji se temelji na projektu.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2d0d8309fcb4300e33ed2f5933259f99ad7e0d6a
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180408"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Procjena retka ugovora koji se temelji na projektu – osnovna

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

U aplikaciji Dynamics 365 Project Operations, redak ugovora koji se temelji na projektu sadrži pojedinosti koje pomažu pri procjeni troškova i potencijalnog prihoda od posla koji se odnosi na isporuku retka ugovora.

Kako biste procijenili redak ugovora koji se temelji na projektu, idite na karticu **Pojedinosti retka ugovora** na **Retku ugovora** koji se temelji na projektu.  Postoje dva načina za stvaranje procjene na retku ugovora koji se temelji na projektu:

   - Stvorite procjenu izravno na retku ugovora ručnim dodavanjem pojedinosti retka ugovora.
   - Stvorite projekt i projektni plan, a zatim projekt i zadatke povežite s retkom ugovora o projektu. To omogućuje postupak kojim možete uvesti procjenu plana projekta u redak ugovora koji se temelji na komponentama uključenim u redak ugovora.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Stvaranje procjene izravno na retku ugovora koji se temelji na projektu

1. Idite na redak ugovora i odaberite karticu **Pojedinosti retka ugovora**. Redci koje stvarate na ovoj kartici sažeti su i prikazani kao **Ugovorena vrijednost** za ovaj **Redak ugovora**. 
2. U podrešetki **Pojedinosti retka ugovora** odaberite **+ Nova pojedinost retka ugovora**. Otvara se klizač za brzo stvaranje. Sljedeća su polja dostupna na obrascu **Pojedinosti retka ugovora**:

| Polje | Lokacija | Opis | Utjecaj na niže razine |
| --- | --- | --- | --- |
| **Opis** | **Brzo stvaranje** | Opis specifične procjene. | Ovo polje zadaje pojedinosti povezanog retka ugovora za troškove koji se automatski stvaraju. |
| **Razred transakcije** | **Brzo stvaranje** | Ovaj padajući popis, popis je klasa transakcija uključenih u karticu **Općenito** retka ugovora koji se temelji na projektu. | Ovo polje zadaje pojedinosti povezanog retka ugovora za troškove koji se automatski stvaraju. |
| **Uloga** | **Brzo stvaranje** | Uloga osobe koja obavlja ovaj posao ili ima taj trošak. | Ovo polje zadaje pojedinosti povezanog retka ugovora za troškove koji se automatski stvaraju. |
| **Kategorija** | **Brzo stvaranje** | Kategorija posla ili troška. | Ovo polje zadaje pojedinosti povezanog retka ugovora za troškove koji se automatski stvaraju. |
| **Datum početka** | **Brzo stvaranje** | Datum početka posla. | Ovo polje zadaje pojedinosti povezanog retka ugovora za troškove koji se automatski stvaraju. |
| **Datum završetka** | **Brzo stvaranje** | Datum završetka posla. | Ovo polje zadaje pojedinosti povezanog retka ugovora za trošak koji se automatski stvara. |
| **Jedinica za resurse** | **Brzo stvaranje** | Jedinica za resurse koja snosi taj trošak i osigurava resurs da radi na tome. | Ovo polje zadaje pojedinosti povezanog retka ugovora za troškove koji se automatski stvaraju. Ovo se polje također upotrebljava za pronalaženje cijene koštanja. |
| **Raspored jedinice** | **Brzo stvaranje** | Grupa jedinica posla ili troška. Jedinice koje pripadaju rasporedu jedinice ili grupi jedinica. Na primjer, *milje* i *kilometri (km)* jedinice su koje pripadaju skupini jedinica koje opisuju udaljenost. | Ovo polje zadaje pojedinosti povezanog retka ugovora za troškove koji se automatski stvaraju. |
| **Jedinica** | **Brzo stvaranje** | Grupa jedinica posla ili troška. | Ovo polje zadaje pojedinosti povezanog retka ugovora za troškove koji se automatski stvaraju. |
| **Količina** | **Brzo stvaranje** | Količina posla ili troška. | Ovo polje zadaje pojedinosti povezanog retka ugovora za troškove koji se automatski stvaraju. |
| **Jedinična cijena** | **Brzo stvaranje** | Cijena naplate uloge koja obavlja posao ili prodajna cijena kategorije troška. Ovo polje zadaje vrijednost za **Vrijeme** koje se temelji na ulozi i kombinaciji resursne jedinice na cjeniku projekta koji vrijedi za datum početka. Za troškove, ovo se polje zadaje iz postavke cijene za kategoriju transakcije u cjeniku za projekt koja vrijedi za datum početka. Ako način određivanja cijene za kategoriju transakcije nije **cijena po jedinici**, nema zadane vrijednosti te ovo polje ostaje prazno. | Cijena koštanja uloge koja obavlja posao ili trošak po jedinici kategorije troška. Ovo je polje zadaje **Vrijeme koje se temelji na ulozi** i kombinaciju jedinice resursa na retku cijene uloge cjenika koštanja priloženog ugovornoj jedinici koja je na snazi za datum početka. Za troškove, ono što je zadano za ovo polje temelji se na retku cijene kategorije cjenika koštanja priloženog ugovornoj jedinici koja vrijedi za datum početka. Ako način određivanja cijene za kategoriju transakcije nije cijena po jedinici, nema zadane vrijednosti te ovo polje ostaje prazno. |
| **Procijenjeni porez** | **Brzo stvaranje** | Procijenjeni porez za ovaj posao ili trošak kao unos od strane korisnika. | Procijenjeni porez za ovaj posao ili trošak kao unos od strane korisnika. |
| **Iznos** | **Brzo stvaranje** | Ovu vrijednost korisnik može dodati u ovo polje ako su polja **Količina** i **Cijena** ostala prazna. Ako su polja **Količina** i **Cijena** popunjena, polje **Iznos** samo je za čitanje i izračunava se kao **(Količina \* Jedinična cijena) + Porez**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Ažuriranje cijene na pojedinostima retka ugovora

Ako promijenite cijene na cjeniku za projekt koji je priložen ugovoru ili cjeniku koštanja ugovorne jedinice, kako bi se odrazile promjene cijene možete osvježiti u pojedinostima pojedinog redaka ugovora. Na stranici **Ugovor** odaberite **Ponovni izračun**. Otvara se upozorenje koje vas izvješćuje da su cijene svih redaka ugovora na ovom ugovoru vrćene na zadane vrijednosti. Odaberite **Da** kako biste osvježili cijene za pojedinosti retka ugovora o prodaji i trošku.

## <a name="access-contract-line-details-for-cost"></a>Pristup pojedinostima redaka ugovora radi troška

Na kartici **Pojedinosti retka ugovora** odaberite redak u rešetki kako biste prikazali radnje na alatnoj traci podrešetke. Prva je radnja na alatnoj traci podrešetke **Otvori pojedinosti troška**. Kako biste prikazali odgovarajuću cijeni troška i iznos za ovu pojedinost retka ugovora, odaberite **Otvori pojedinosti troška**. 

> [!NOTE]
> Promjena tvrtke za resurse, jedinice resursa, količine, datuma, uloge ili vrijednosti kategorije na pojedinosti retka ugovora za **Trošak** također mijenja odgovarajuće vrijednosti na pojedinosti retka ugovora za **Prodaju**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta na pojedinostima retka ugovora za trošak i prodaju

Pojedinosti retka ugovora za **Prodaju** postavlja zadanu valutu iz cjenika za projekt koja vrijedi za datum početka pojedinosti retka ugovora.

Pojedinosti retka ugovora za **Trošak** postavlja zadanu valutu iz cjenika ugovorne jedinice postavljene u ugovoru koja vrijedi za datum početka pojedinosti retka ugovora za **Trošak**.

Izračuni isplativosti pretvaraju iznose za pojedinosti retka ugovora za **Trošak** i **Prodaju** u osnovnu valutu okruženja za izvješćivanje o ukupnim stvarnim i procijenjenim maržama u ugovoru.

> [!NOTE]
> Pogreške u zaokruživanju valuta i izmjena marži mogli bi se dogoditi zbog nedostatka tečajeva koji su na snazi na određeni datum. Upotrijebite ove izračune na ugovorima o projektu samo kao približne vrijednosti, a ne za stvarno zakonsko ili drugo izvješćivanje koje zahtijeva veću preciznost zaokruživanja i saznanje o datumu stupanja na snagu tečajeva.
