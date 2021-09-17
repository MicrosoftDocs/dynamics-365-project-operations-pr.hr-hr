---
title: Redci podugovora za kategorije troška
description: U ovoj temi objašnjava se način bilježenja redaka podugovora za trošak i uporabe polja za bilježenje kupnje vremena od dobavljača.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323812"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Redci podugovora za kategorije troška

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Podugovor u aplikaciji Dynamics 365 Project Operations može imati redak za kategorije troška. Redci podugovora za kategorije troška omogućuju voditelju projekta da od dobavljača kupi kategorije usluga ili proizvoda koje mogu naplatiti projektu.

Kako biste stvorili redak podugovora za kategorije troška u aplikaciji Project Operations, poduzmite sljedeće korake.

1. U navigacijskom oknu odaberite **Podugovori** i otvorite podugovor na kojem želite raditi.
2. Na kartici **Retci podugovora** odaberite **Novi** kako biste stvorili novi redak.
3. Na stranici **Brzo stvaranje**, u polju **Klasa transakcije**, odaberite **Trošak** i unesite ili odaberite odaberite neki drugi obvezni podatak o polju.

U tablici u nastavku nalaze se podaci o poljima na stranici s pojedinostima **Redak podugovora** i stranici **Brzo stvaranje**.

| **Polje** |  **Opis** |
| ----------| ---------------- |
| Ime/naziv | Naziv retka podugovora. |
| Opis | Kratak opis usluga ili kategorija proizvoda koje se kupuju u retku podugovora. |
| Vrsta retka | Ovo polje ima zadanu vrijednost stavke **Na temelju količine**.  |
| Način naplate | Način naplate retka podugovora. Na temelju načina naplate retka, raspored faktura koji se temelji na kontrolnim točkama dostupan je za način naplate s fiksnom cijenom.  |
| Razred transakcije | Ovo polje ima zadanu vrijednost stavke **Vrijeme**. Za stvaranje redaka podugovora za kupnju proizvoda, polje **Klasa transakcije** postavite na **Trošak**. Ova vrijednost polja označava da se redak podugovora upotrebljava za bilježenje kupnje kategorija proizvoda ili usluga koje će se upotrebljavati na projektima. |
| Kategorija transakcije | Odaberite kategoriju transakcije. |
| Zatraženi početak | Datum kada kategorije kupnje moraju biti dostupne od dobavljača. Traženi početak upotrebljava se za odabir cjenika projekta iz cjenika projekta priloženih podugovoru. Cijena kategorije na retku podugovora zadaje se iz tog cjenika. |
| Zatraženi završetak | Datum kada kategorije kupnje više nisu potrebne. Ovaj datum poziva upozorenje kada voditelj projekta poveže ovaj redak podugovora s posebnim procjenama troškova za projekte koji su datirani nakon tog datuma. |
| Naručena količina | Količina kategorije koja se kupuje od dobavljača. Kada voditelj projekta prekorači kupljenu količinu, prikazat će se upozorenje.  |
| Grupa jedinica | Zadana vrijednost ovog polja temelji se na zadanoj grupi jedinica koja je postavljena za odabranu kategoriju. |
| Jedinica | Zadana vrijednost ovog polja temelji se na zadanoj jedinici postavljenoj za odabranu kategoriju. Kombinacija kategorije i jedinice upotrebljava se za zadavanje jedinične cijene u retku podugovora. |
| Jedinična cijena | Jedinična cijena vrijednosti polja zadana je iz kombinacije kategorije i jedinice iz cijena kategorije povezanih s cjenikom za projekt koji se primjenjuje za traženi početak retka podugovora.  |
| Podzbroj | Ovo je polje samo za čitanje koje se automatski izračunava kao količinska jedinična cijena, ako su unesene vrijednosti i količine i jedinične cijene. Ako je jedno ili su oba polja prazna, u to polje možete ručno unijeti vrijednost.  |
| Porez na promet | Unesite iznos poreza na prodaju.  |
| Ukupni iznos | Ukupni iznos retka podugovora, uključujući porez. Ovo polje izračunava se kao međuzbroj + porez na promet.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
