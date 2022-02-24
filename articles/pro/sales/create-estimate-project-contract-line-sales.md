---
title: Procjena retka ugovora koji se temelji na projektu – osnovna
description: Ovaj tema pruža informacije o procjeni retka ugovora koji se temelji na projektu.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bf7941a627375604dca778ab293756bed2536049
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858068"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Procjena retka ugovora koji se temelji na projektu – osnovna

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

U aplikaciji Dynamics 365 Project Operations, redak ugovora koji se temelji na projektu sadrži pojedinosti koje pomažu pri procjeni troškova i potencijalnog prihoda od posla koji se odnosi na isporuku retka ugovora.

Kako biste procijenili redak ugovora koji se temelji na projektu, idite na karticu **Pojedinosti retka ugovora** na **Retku ugovora** koji se temelji na projektu.  Postoje dva načina za stvaranje procjene na retku ugovora koji se temelji na projektu:

   - Stvorite procjenu izravno na retku ugovora ručnim dodavanjem pojedinosti retka ugovora.
   - Stvorite projekt i projektni plan, a zatim projekt i zadatke povežite s retkom ugovora o projektu. To omogućuje postupak kojim možete uvesti procjenu plana projekta u redak ugovora koji se temelji na komponentama uključenim u redak ugovora.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Stvaranje procjene izravno na retku ugovora koji se temelji na projektu

Kako biste stvorili procjene izravno na retku ugovora koji se temelji na projektu, slijedite ove korake:

1. Idite na redak ugovora i odaberite karticu **Pojedinosti retka ugovora**. Redci koje stvarate na ovoj kartici sažeti su i prikazani kao **Ugovorena vrijednost** za ovaj **Redak ugovora**. 
2. U podrešetki **Pojedinosti retka ugovora** odaberite **Nova pojedinost retka ugovora**. Otvara se klizač za brzo stvaranje. Polja u nastavku dostupna su na stranici **Pojedinosti retka ugovora**.

| Polje | Lokacija | Opis | Utjecaj na niže razine |
| --- | --- | --- | --- |
| **Opis** | **Brzo stvaranje** | Opis specifične procjene. | Ova je vrijednost zadana za pojedinost povezanog retka ugovora za trošak koji se automatski stvorio. |
| **Razred transakcije** | **Brzo stvaranje** | Ovo je popis klasa transakcija uključenih u karticu **Općenito** retka ugovorna koji se temelji na projektu. | Ova je vrijednost zadana za pojedinost povezanog retka ugovora za trošak koji se automatski stvorio. |
| **Odabir proizvoda** | **Brzo stvaranje** | Primjenjuje se kada je klasa transakcije **Materijal**. Možete navesti kako je ovo redak procjene za **Postojeći** (kataloški) proizvod ili **Umetnut** proizvod. | Ova je vrijednost zadana za pojedinost povezanog retka ugovora za trošak koji se automatski stvorio. |
| **Proizvod** | **Brzo stvaranje** | ID proizvoda iz kataloga proizvoda. Ovo je polje omogućeno samo nakon što odaberete mogućnost **Postojeći proizvod** u polju **Odaberi proizvod**. ID se upotrebljava za dohvaćanje prodajne cijene iz cjenika za projekt u ugovoru. | Ova je vrijednost zadana za pojedinost povezanog retka ugovora za trošak koji se automatski stvorio. |
| **Umetnuti proizvod** | **Brzo stvaranje** | Tekstno polje za unos naziva proizvoda. Ovo je polje omogućeno samo nakon što odaberete mogućnost **Umetni** u polju **Odaberi proizvod**.| Ova je vrijednost zadana za pojedinost povezanog retka ugovora za trošak koji se automatski stvorio. |
| **Uloga** | **Brzo stvaranje** | Uloga osobe koja obavlja ovaj posao ili ima taj trošak. | Ova je vrijednost zadana za pojedinost povezanog retka ugovora za trošak koji se automatski stvorio.|
| **Kategorija** | **Brzo stvaranje** | Kategorija posla ili troška. |Ova je vrijednost zadana za pojedinost povezanog retka ugovora za trošak koji se automatski stvorio.|
| **Datum početka** | **Brzo stvaranje** | Datum početka posla. | Ova je vrijednost zadana za pojedinost povezanog retka ugovora za trošak koji se automatski stvorio. |
| **Datum završetka** | **Brzo stvaranje** | Datum završetka posla. | Ova je vrijednost zadana za pojedinost povezanog retka ugovora za trošak koji se automatski stvorio. |
| **Jedinica za resurse** | **Brzo stvaranje** | Jedinica za resurse koja snosi taj trošak i osigurava resurse za rad na njima. |Ova je vrijednost zadana za pojedinost povezanog retka ugovora za trošak koji se automatski stvorio i upotrijebio za dohvaćanje cijene koštanja. |
| **Raspored jedinice** | **Brzo stvaranje** | Grupa jedinica za rad, proizvod ili trošak. Jedinice koje pripadaju rasporedu jedinice ili grupi jedinica. Na primjer, *milje* i *kilometri (km)* jedinice su koje pripadaju skupini jedinica koje opisuju udaljenost. | Ova je vrijednost zadana za pojedinost povezanog retka ugovora za trošak koji se automatski stvorio. |
| **Jedinica** | **Brzo stvaranje** | Jedinica za rad, proizvod ili trošak. | Ova je vrijednost zadana za pojedinost povezanog retka ugovora za trošak koji se automatski stvorio. |
| **Količina** | **Brzo stvaranje** | Količina rada, proizvoda ili troškova. | Ova je vrijednost zadana za pojedinost povezanog retka ugovora za trošak koji se automatski stvorio. |
| **Jedinična cijena** | **Brzo stvaranje** | Cijena naplate uloge koja izvršava posao, jedinična cijena proizvoda ili prodajna cijena kategorije proizvoda ili troška. Ovo je polje zadano za **Vrijeme** koje se temelji na kombinaciji vrijednosti veličina u retku cijene uloge cjenika za projekt koja vrijedi za datum početka. Za **Troškove**, ovo se polje zadaje iz postavke cijene za kategoriju transakcije u cjeniku za projekt koja vrijedi za datum početka. Ako način određivanja cijene za kategoriju transakcije nije **cijena po jedinici**, nema zadane vrijednosti te ovo polje ostaje prazno. Za proizvode, zadana vrijednost za ovo polje temelji se na retku **Stavka cjenika** cjenika za projekta koji vrijedi za datum početka.| Cijena troška uloge koja izvršava posao ili trošak po jedinici kategorije troška ili jedinični trošak proizvoda. Ovo je polje zadano za **Vrijeme** koje se temelji na kombinaciji vrijednosti veličina u retku cijene uloge iz troškovnika priloženog ugovornoj jedinici koja vrijedi za datum početka. Za troškove, ono što je zadano za ovo polje temelji se na retku cijene kategorije cjenika koštanja priloženog ugovornoj jedinici koja vrijedi za datum početka. Ako način određivanja cijene za kategoriju transakcije nije cijena po jedinici, nema zadane vrijednosti te ovo polje ostaje prazno. Za proizvode, zadana vrijednost ovog polja temelji se na retku **Stavke cjenika** iz troškovnika priloženog ugovornoj jedinici koji vrijedi za datum početka.|
| **Procijenjeni porez** | **Brzo stvaranje** | Procijenjeni porez za ovaj rad ili trošak. | Procijenjeni porez za ovaj rad ili trošak. |
| **Iznos** | **Brzo stvaranje** | U ovo polje možete dodati vrijednost ako polja **Količina** i **Cijena** ostaju prazna. Ako su polja **Količina** i **Cijena** popunjena, polje **Iznos** samo je za čitanje i izračunava se kao **(Količina \* Jedinična cijena) + Porez**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Ažuriranje cijene na pojedinostima retka ugovora

Ako promijenite cijene na cjeniku za projekt koji je priložen ugovoru ili cjeniku koštanja ugovorne jedinice, kako bi se odrazile promjene cijene možete osvježiti u pojedinostima pojedinog redaka ugovora. Na stranici **Ugovor** odaberite **Ponovni izračun**. Prikazuje se upozorenje koje vas obavještava da su cijene svih redaka tog ugovora vraćene na zadane. Odaberite **Da** kako biste osvježili cijene za pojedinosti retka ugovora o prodaji i trošku.

## <a name="access-contract-line-details-for-cost"></a>Pristup pojedinostima redaka ugovora radi troška

Na kartici **Pojedinosti retka ugovora** odaberite redak u rešetki kako biste prikazali radnje na alatnoj traci podrešetke. Prva je radnja na alatnoj traci podrešetke **Otvori pojedinosti troška**. Kako biste prikazali odgovarajuću cijeni troška i iznos za ovu pojedinost retka ugovora, odaberite **Otvori pojedinosti troška**. 

> [!NOTE]
> Promjena tvrtke za resurse, jedinice resursa, količine, datuma, uloge ili vrijednosti kategorije na pojedinosti retka ugovora za **Trošak** također mijenja odgovarajuće vrijednosti na pojedinosti retka ugovora za **Prodaju**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta na pojedinostima retka ugovora za trošak i prodaju

Pojedinosti retka ugovora za **Prodaju** postavlja zadanu valutu iz cjenika za projekt koja vrijedi za datum početka pojedinosti retka ugovora.

Pojedinosti retka ugovora za **Trošak** postavlja zadanu valutu iz cjenika ugovorne jedinice postavljene u ugovoru koja vrijedi za datum početka pojedinosti retka ugovora za **Trošak**.

Izračuni isplativosti pretvaraju iznose za pojedinosti retka ugovora za **Trošak** i **Prodaju** u osnovnu valutu okruženja za izvješćivanje o ukupnim stvarnim i procijenjenim maržama u ugovoru.

> [!NOTE]
> Pogreške u zaokruživanju valuta i izmjena marži mogli bi se dogoditi zbog nedostatka tečajeva koji su na snazi na određeni datum. Upotrebljavajte ove izračune samo na ugovorima o projektu, jer su to približni podaci i nisu stvarno propisani ili drugo izvještavanje koje zahtijeva veću preciznost zaokruživanja i svijest o učinkovitosti datuma za tečajeve.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
