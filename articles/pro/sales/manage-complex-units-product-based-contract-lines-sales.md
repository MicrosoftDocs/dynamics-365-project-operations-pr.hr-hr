---
title: Upravljanje složenim jedinicama za retke ugovora utemeljene na proizvodu – jednostavno
description: U ovoj temi nalaze se informacije o podršci prodaji proizvoda koji se temelje na pretplati.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177367"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Upravljanje složenim jedinicama za retke ugovora utemeljene na proizvodu – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Dynamics 365 Project Operations upotrebljava čimbenike količine za podršku pri prodaji proizvoda temeljenih na pretplati. Za proizvode temeljene na pretplati količina u retku ugovora ili ugovora o projektu izražena je kao broj korisničkih mjeseci.

Cijena softvera za pretplatu pohranjuje se u katalog kao mjesečna cijena po korisniku. Tijekom prodajnog postupka cijena u retku ugovora obično je dogovorena mjesečna cijena po korisniku uz popust prodajnog predstavnika. Svaki ugovor ima različit broj korisnika i različit broj mjeseci pretplate. Količina koja se upotrebljava za izračun iznosa retka ugovora proizvod je broja korisnika i broja mjeseci pretplate.

Kako bi se podržala ova vrsta prodaje, Project Operations podržava koncept *čimbenika količine*. Čimbenici količine oslanjaju se na atribute proizvoda. Kada konfigurirate određena svojstva za proizvod, možete označiti podskup tih svojstava ili svih svojstava kao čimbenika količine.

Project Operations provjerava valjanost jesu li samo numerička svojstva ili svojstva proizvoda koja imaju numeričku vrstu podataka označena kao čimbenici količine. Kad se proizvod s konfiguriranim čimbenicima količine doda u redak ugovora, polje **Količina** postaje samo za čitanje. Nakon što unesete vrijednosti za svojstva proizvoda koja su čimbenici količine, Project Operations izračunava količinu retka ugovora.

Na primjer, Dynamics 365 Sales može imati sljedeća svojstva:

- **Broj korisnika**: Broj korisnika.
- **Broj mjeseci**: Broj mjeseci pretplate.
- **SKU proizvoda**: Skladišni broj (SKU) proizvoda.

Svojstva **Broj korisnika** i **Broj mjeseci** mogu se označiti kao čimbenici količine uređivanjem svojstava retka proizvoda.

Kako biste stvorili čimbenike količine iz svojstava proizvoda, poduzmite sljedeće korake.

1. U aplikaciji **Project Operations** odaberite **Prodaja-Proizvodi**.
2. Otvorite proizvod za koji trebate postaviti faktore količine. Uvjerite se da proizvod ima svojstva koja su već postavljena.
3. Na stranici **Informacije o projektu** odaberite karticu **Čimbenici količine**.
4. U podrešetki odaberite **+ Izračun novog polja**.
5. Unesite naziv **Čimbenika količine** i odaberite vrijednost svojstva koja se mapira u izračun polja.
6. Spremanje i zatvaranje obrasca.
7. Ponovite korake 2 – 6 za sva svojstva koja će zajedno činiti količinu za redak ugovora koji se temelji na proizvodu.

S postavljenim čimbenicima količine, kada korisnik stvara redak ugovora za ovaj proizvod, količina retka ugovora zaključava se. Količina se zatim izračunava kao umnožak vrijednosti svojstva za taj redak ugovora.