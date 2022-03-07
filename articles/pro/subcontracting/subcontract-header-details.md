---
title: Pojedinosti zaglavlja za podugovaratelje
description: U ovoj temi objašnjava se funkcija navedena u zaglavlju podugovora u aplikaciji Project Operations.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee863d31b45e7de962488fe804202ddfe580eb04
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501317"
---
# <a name="header-details-for-subcontracts"></a>Pojedinosti zaglavlja za podugovaratelje

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

U ovoj temi objašnjava se funkcija navedena u zaglavlju podugovora u aplikaciji Dynamics 365 Project Operations.

Budući da voditelji projekata planiraju i izvršavaju projekte, oni mogu zapošljavati podizvođače i kupovati proizvode i usluge od dobavljača. Kada voditelj projekta treba kupiti proizvode ili usluge, može stvoriti podugovor u aplikaciji Project Operations.

Kako biste stvorili podugovor, poduzmite sljedeće korake.

1. U navigacijskom oknu odaberite **Podugovaratelji**, a na stranici **Podugovor** odaberite **Novo**.
2. Unesite potrebne informacije, a zatim odaberite **Spremi**.

    U tablici u nastavku nalaze se podaci o poljima na stranici **Zaglavlje podugovora**.

    | Polje | Opis |Funkcionalni utjecaj |
    |---|------|---| 
    | Ime/naziv | Naziv podugovora. | Na svim padajućim popisima podugovora, naziv podugovora naveden je u prvom stupcu kako biste lakše identificirali podugovor. | 
    | Opis | Kratak opis usluga i proizvoda koje se kupuju podugovorom. | Nijedno |
    | Isporučitelj | Naziv tvrtke od koje se kupuju proizvodi i usluge. Taj zapis računa ima vrstu odnosa **Dobavljač** ili **Isporučitelj**. | Na temelju odabranog dobavljača, zadane se vrijednosti automatski unose za sljedeća polja:<br/> **• Valuta** </br> **• Cjenici** </br> **• Uvjeti plaćanja**</br> **• Adresa za plaćanje**</br> **• Adresa za naplatu**</br> **• Naziv za naplatu** </br>**• Voditelj računa dobavljača**|
    | Datum podugovora | Datum sklapanja podugovor. | Datum podugovora upotrebljava se za odabir ispravnog nabavnog cjenika bilo iz cjenika koji su priloženi povezanom dobavljaču ili iz parametara projekta. |
    | Razlog statusa | Status podugovora. | Stanje određuje gdje se u poslovnom procesu podugovor nalazi i može li se urediti. <br/>Vrijednosti uključuju:<br>• **Skica**: Podugovor se može uređivati. Možete uređivati samo podugovore koji su u stanju **Nacrt**.<br/>• **Potvrđeno**: Pregovori s dobavljačem završeni su i podugovor je odobren za isporuku. <br/>• **Zatvoreno**: Isporuka po podugovoru je potpuna.<br/>• **Otkazano**: Podugovor je otkazan i isporuka nije planirana.  | 
    | Valuta | Valuta u kojoj se nabavljaju proizvodi i usluge. Zadana vrijednost automatski se unosi iz računa dobavljača, ali se može promijeniti. | Valuta podugovora upotrebljava se za odabir nabavnog cjenika bilo iz cjenika koji su priloženi povezanom dobavljaču ili iz parametara projekta. Cjenici u drugoj valuti ne mogu se povezati s podugovorom. Cijena vremena, troškova i materijala koje isporučuju resursi dobavljača iz ovog podugovora evidentiraju se na projektu u toj valuti. Nakon spremanja zapisa o podugovoru, valuta na podugovoru ne može se promijeniti.|
    | Ugovorena jedinica | Sektor tvrtke koji sklapa kupoprodajni ugovor ili podugovor s dobavljačem. | Nijedno |
    | Uvjeti plaćanja | Uvjeti plaćanja na fakturama dobavljača koji su izdani po ovom podugovoru. Zadana vrijednost automatski se unosi iz zapisa o računa dobavljača. | Uvjeti plaćanja iz podugovora kopiraju se na sve fakture dobavljača koje su povezane s ovim podugovorom. Uvjeti plaćanja mogu se ažurirati ako je podugovor u stanju **Skica**. | 
    | Adresa za plaćanje | Adresa dobavljača na kojeg se moraju poslati uplate. Zadana vrijednost automatski se unosi iz zapisa o računa dobavljača. | Adresa za plaćanje iz podugovora kopira se kao adresa za plaćanje svih faktura dobavljača koje su stvorene za ovaj podugovor. Adresa plaćanja može se ažurirati ako je podugovor u stanju **Skica**.|
    | Naziv za naplatu | Ime osobe ili sektora u tvrtki dobavljača koja će poslati fakturu. Zadana vrijednost automatski se unosi iz zapisa o računa dobavljača. | Vrijednost **Naziv za naplatu** iz podugovora kopira se na sve fakture dobavljača koje su povezane s ovim podugovorom. Ovo se polje može ažurirati ako je podugovor u stanju **Skica**.|
    | Adresa naplate | Adresa koja se upotrebljava na fakturama dobavljača. Zadana vrijednost automatski se unosi iz zapisa o računa dobavljača. | Ova adresa, adresa je „izdavatelja fakture” na fakturama dobavljača koje su stvorene za ovaj podugovor. |
    | Podzbroj | Ako podugovor nema retke, unesite međuzbroj narudžbe prije oporezivanja. Ako podugovor ima retke, ovo polje je samo za čitanje. Prikazani je iznos međuzbroj svih redaka podugovora. | Nijedno |
    | Ukupni porez | Ako podugovor nema retke, unesite ukupan iznos poreza na tom podugovoru. Ako podugovor ima retke, ovo polje je samo za čitanje. Prikazani je iznos zbroj iznosa poreza svih redaka podugovora. | Nijedno |
    | Ukupni iznos | Ovo izračunano polje prikazuje ukupni iznos retka podugovora nakon uključivanja poreza. | Nijedno |
    | Potvrđeni datum | Datum potvrde podugovora. | Nijedno |
    | Zatražio | Prema zadanim postavkama ovo je polje postavljeno na ime korisnika koji stvara podugovor. Međutim, tvorac podugovora može promijeniti vrijednost kako bi naznačio osobu u čije ime stvara podugovor. | Nijedno |
    | Voditelj računa isporučitelja | Naziv primarnog kontakta računa dobavljača. Zadana vrijednost automatski se unosi iz zapisa o računa dobavljača. Možete odabrati drugi kontakt kao upravitelja računa dobavljača za podugovor. | Možete postaviti upozorenja e-poštom kako biste obavijestili kontakt kada se izvrše izmjene podugovora kao rezultat pregovora o cijeni. |
