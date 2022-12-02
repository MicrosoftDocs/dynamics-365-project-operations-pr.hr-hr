---
title: Pojedinosti zaglavlja za fakture dobavljača
description: U ovom se članku objašnjava funkcija koja je dostupna u zaglavlju fakture dobavljača u aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d575ebe44e45411e1009c64e9b575777b741322f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261644"
---
# <a name="header-details-for-vendor-invoices"></a>Pojedinosti zaglavlja za fakture dobavljača

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

U ovom se članku objašnjava funkcija koja je dostupna u zaglavlju fakture dobavljača u aplikaciji Microsoft Dynamics 365 Project Operations.

Budući da voditelji projekata planiraju i izvršavaju projekte, oni mogu zapošljavati podizvođače i kupovati proizvode i usluge od dobavljača. Tijekom izvođenja projekta nastaju troškovi usluga, materijala i kategorija troškova koji se nabavljaju na temelju podugovora s dobavljačima. Dobavljači te troškove projekata fakturiraju izradom faktura dobavljača.

Tablica u nastavku pruža informacije o poljima u zaglavljima fakture dobavljača u aplikaciji Project Operations.

| Polje | Opis | Funkcionalni utjecaj |
| --- | --- | --- |
| Ime/naziv | Naziv fakture dobavljača. | Na svim padajućim popisima fakture dobavljača naziv fakture dobavljača naveden je u prvom stupcu da biste ju lakše prepoznali. Prema zadanim postavkama, kada se faktura dobavljača izrađuje iz podugovora, polje **Naziv** fakture dobavljača postavljeno je na vrijednost koja se sastoji od naziva podugovora i trenutačnog datuma. |
| Opis | Kratak opis usluga i proizvoda koje dobavljač fakturira u fakturi dobavljača. | Nijedno |
| Isporučitelj | Naziv tvrtke koja izdaje fakturu za proizvode i usluge. Ta bi tvrtka trebala biti zapis računa koji ima vrstu odnosa **Dobavljač** ili **Isporučitelj**. | <p>Na temelju odabranog dobavljača, zadane se vrijednosti automatski unose u sljedeća polja:</p><ul><li>Valuta</li><li>Cjenici</li><li>Uvjeti plaćanja</li><li>Adresa za plaćanje</li></ul> |
| Podugovor | Upućivanje na podugovor za fakturu dobavljača. | <p>Na temelju odabranog podugovora, zadane se vrijednosti automatski unose u sljedeća polja:</p><ul><li>Valuta</li><li>Cjenici</li><li>Uvjeti plaćanja</li><li>Adresa za plaćanje</li></ul><p>Podugovor koji je odabran u zaglavlju fakture dobavljača unosi se prema zadanim postavkama u retke fakture dobavljača i ne može se promijeniti.</p> |
| Datum fakture | Datum stvarnih troškova će se kreirati kada se potvrdi faktura dobavljača. | Datum fakture upotrebljava se i za odabir ispravnog nabavnog cjenika, bilo iz cjenika koji su priloženi povezanom dobavljaču ili iz projektnih parametara. |
| Razlog stanja | Status fakture dobavljača. | <p>Stanje određuje gdje se u poslovnom procesu nalazi faktura dobavljača i može li se urediti. Ovo su neke od dostupnih vrijednosti:</p><ul><li>**Skica** – Faktura dobavljača može se uređivati.</li><li>**Potvrđeno** – Faktura dobavljača je provjerena i potvrđena. Faktura dobavljača s ovim statusom ne može se uređivati niti brisati.</li><li>**U tijeku** – U tijeku je pregled fakture dobavljača. Fakture dobavljača s ovim statusom mogu se uređivati, ali se ne mogu brisati.</li><li>**Otkazano** – Faktura dobavljača je otkazana. Faktura dobavljača s ovim statusom ne može se uređivati niti brisati.</li></ul> |
| Valuta | Valuta u kojoj dobavljač fakturira proizvode i usluge na fakturi dobavljača. | Na fakturi dobavljača koja upućuje na podugovor valuta podugovora unosi se prema zadanim postavkama kao valuta fakture dobavljača. Na fakturi dobavljača koja ne upućuje na podugovor, zadana vrijednost unosi se iz zapisa računa dobavljača i može se promijeniti. Nakon što se faktura dobavljača spremi, valuta se više ne može uređivati. |
| Ugovorna jedinica | Odjel tvrtke koji je odgovoran za primanje usluga i/ili proizvoda od dobavljača. | Nijedno |
| Uvjeti plaćanja | Uvjeti plaćanja na fakturama dobavljača koje su izdane. Zadana vrijednost automatski se unosi iz zapisa o računa dobavljača. | Uvjeti plaćanja iz podugovora kopiraju se na sve fakture dobavljača koje su povezane s podugovorom. Uvjeti plaćanja mogu se ažurirati ako faktura dobavljača ima status **Skica**. |
| Adresa za plaćanje | Adresa dobavljača na kojeg se moraju poslati uplate. Zadana vrijednost automatski se unosi iz zapisa o računa dobavljača. | Adresa za plaćanje iz podugovora kopira se kao adresa za plaćanje na sve fakture dobavljača koje su kreirane za taj podugovor. Adresa za plaćanje može se ažurirati ako faktura dobavljača ima status **Skica**. |
| Podzbroj | Ako faktura dobavljača nema retke, unesite međuzbroj fakture prije poreza. Ako faktura dobavljača ima retke, ovo polje je samo za čitanje. U ovom slučaju prikazani je iznos međuzbroj svih redaka fakture dobavljača. | Nijedno |
| Ukupni porez | Ako faktura dobavljača nema retke, unesite ukupni porez na podugovor. Ako faktura dobavljača ima retke, ovo polje je samo za čitanje. U tom slučaju prikazani je iznos zbroj iznosa poreza iz svih redaka fakture dobavljača. | Nijedno |
| Ukupni iznos | Ovo izračunato polje prikazuje ukupni iznos fakture dobavljača nakon uključivanja poreza. | Nijedno |

> [!NOTE]
> Sljedeća polja na fakturi dobavljača ne mogu se mijenjati nakon spremanja fakture dobavljača: **Dobavljač**, **Podugovor**, **Valuta**, **Ugovorna jedinica** i **Uvjeti plaćanja**. Ako su potrebne izmjene u ovim poljima na fakturi dobavljača, morate izbrisati fakturu dobavljača i stvoriti novu fakturu dobavljača.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
