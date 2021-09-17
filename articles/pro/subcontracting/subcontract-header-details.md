---
title: Pojedinosti zaglavlja za podugovaratelje
description: U ovoj temi objašnjava se funkcija navedena u zaglavlju podugovora u aplikaciji Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323632"
---
# <a name="header-details-for-subcontracts"></a>Pojedinosti zaglavlja za podugovaratelje

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

U ovoj temi objašnjava se funkcija navedena u zaglavlju podugovora u aplikaciji Dynamics 365 Project Operations.

Budući da voditelji projekata planiraju i izvršavaju projekte, oni mogu zapošljavati podizvođače i kupovati proizvode i usluge od dobavljača. Kada voditelj projekta treba kupiti proizvode ili usluge, može stvoriti podugovor u aplikaciji Project Operations.

Kako biste stvorili podugovor, poduzmite sljedeće korake.

1. U navigacijskom oknu odaberite **Podugovaratelji**, a na stranici **Podugovor** odaberite **Novo**.
2. Unesite potrebne informacije, a zatim odaberite **Spremi**.

    U tablici u nastavku nalaze se podaci o poljima na stranici Zaglavlje podugovora.

    | **Polje** | **Opis** |
    | --- | --- | 
    | Ime/naziv | Naziv podugovora. |
    | Opis | Kratak opis usluga i proizvoda koje se kupuju podugovorom. |
    | Isporučitelj | Naziv tvrtke od koje se kupuju proizvodi i usluge. Taj zapis računa ima vrstu odnosa **Dobavljač** ili **Isporučitelj**. |
    | Datum podugovora | Datum stvaranja podugovora. |
    | Razlog statusa | Status podugovora. |
    | Valuta | Valuta kupnje proizvoda i usluga. Vrijednost u ovom polju zadaje se iz računa dobavljača, ali se može promijeniti. Cjenici projekta koji se upotrebljavaju za određivanje cijena proizvoda i usluga u podugovoru trebaju biti u toj valuti. Cjenici u nekoj drugoj valuti ne mogu se povezati s podugovorom. Troškovi proizvoda i usluga nastali po ovom podugovoru zabilježit će se na projektu u ovoj valuti. |
    | Ugovorena jedinica | Sektor tvrtke koji sklapa kupoprodajni ugovor ili podugovor s dobavljačem. |
    | Uvjeti plaćanja | Uvjeti plaćanja na fakturama dobavljača koje su izdane po ovom podugovoru. Vrijednost u ovom polju zadaje se iz zapisa računa dobavljača. |
    | Adresa za plaćanje | Adresa na koju se šalje plaćanje po fakturama dobavljača. Vrijednost u ovom polju zadaje se iz zapisa računa dobavljača. |
    | Naziv za naplatu | Ime osobe ili sektora u tvrtki dobavljača koja će poslati fakturu. Vrijednost u ovom polju zadana je iz zapisa računa dobavljača i upotrebljavat će se kao naziv primarnog kontakta na fakturama dobavljača stvorenima za ovaj podugovor. |
    | Adresa naplate | Adresa koja se upotrebljava na fakturama ovog dobavljača. Vrijednost u ovom polju zadaje se iz zapisa računa dobavljača. Ova se adresa također upotrebljava kao adrese pošiljatelja fakturame na fakturama dobavljača stvorenim za ovaj podugovor. |
    | Podzbroj | Ako podugovor nema redaka, unesite vrijednost u ovo polje koja označava međuzbroj narudžbe prije oporezivanja. Ako podugovor ima retke, ovo polje je samo za čitanje. Prikazani je iznos međuzbroj iznosa svih redaka podugovora. |
    | Ukupni porez | Ako podugovor nema redaka, u ovo polje unesite vrijednost koja označava poreze na ovom podugovoru. Ako podugovor ima retke, ovo polje je samo za čitanje. Prikazani je iznos zbroj iznosa poreza iz svih redaka podugovora. |
    | Ukupni iznos |  Ovo izračunano polje prikazuje ukupni iznos retka podugovora nakon uključivanja poreza.  |
    | Potvrđeni datum | Datum potvrde podugovora.  |
    | Zatražio | Vrijednost u ovom polju zadana je imenom korisnika koji stvara podugovor. Ovu vrijednost može promijeniti autor podugovora kako bi naznačio tu osobu u čije ime stvara podugovor.  |
    | Voditelj računa isporučitelja | Naziv primarnog kontakta računa dobavljača. Vrijednost u ovom polju zadaje se iz zapisa računa dobavljača. Ovu vrijednost polja može promijeniti korisnik tako da odabere drugi kontakt kao upravitelja računa dobavljača podugovora. Ovaj kontakt može konfigurirati i poslati upozorenja e-poštom i pregovore o cijenama. |


