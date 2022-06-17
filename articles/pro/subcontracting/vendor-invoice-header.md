---
title: Pojedinosti zaglavlja za fakture dobavljača
description: U ovom se članku objašnjavaju funkcije koje se nalaze u zaglavlju fakture dobavljača u microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929849"
---
# <a name="header-details-for-vendor-invoices"></a>Pojedinosti zaglavlja za fakture dobavljača

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

U ovom se članku objašnjavaju funkcije koje se nalaze u zaglavlju fakture dobavljača u microsoftu Dynamics 365 Project Operations.

Budući da voditelji projekata planiraju i izvršavaju projekte, mogu zaposliti podizvođače i kupovati proizvode i usluge od dobavljača. Tijekom izvršenja projekta troškovi nastaju iz kategorija usluga, materijala i troškova koje se nabavljaju na podugovaranjima s dobavljačima. Dobavljači fakturiraju te troškove projektima kreiranjem faktura dobavljača.

U sljedećoj su tablici navedene informacije o poljima u zaglavljima fakture dobavljača u operacijama projekta.

| Polje | Opis | Funkcionalni utjecaj |
| --- | --- | --- |
| Ime/naziv | Naziv fakture dobavljača. | Na svim padajućim popisima faktura dobavljača naziv fakture dobavljača naveden je u prvom stupcu koji će vam pomoći identificirati fakturu dobavljača. Prema zadanim postavkama, kada se faktura dobavljača kreira iz kooperanta, **polje Naziv** fakture dobavljača postavljeno je na vrijednost koja se sastoji od naziva kooperanta plus trenutni datum. |
| Opis | Kratak opis usluga i proizvoda koji se fakturiraju na fakturi dobavljača. | Nijedno |
| Isporučitelj | Naziv tvrtke koja fakturira za proizvode i usluge. Ovo poduzeće trebalo bi biti zapis o poslovnom subjektu koji ima vrstu **odnosa dobavljača** ili **dobavljača**. | <p>Na temelju odabranog dobavljača zadane vrijednosti automatski se unose u sljedeća polja:</p><ul><li>Valuta</li><li>Cjenici</li><li>Uvjeti plaćanja</li><li>Adresa za plaćanje</li></ul> |
| Podugovor | Referenca na kooperant za fakturu dobavljača. | <p>Na temelju odabranog kooperanta zadane vrijednosti automatski se unose u sljedeća polja:</p><ul><li>Valuta</li><li>Cjenici</li><li>Uvjeti plaćanja</li><li>Adresa za plaćanje</li></ul><p>Kooperant odabran u zaglavlju fakture dobavljača po zadanom se unosi u retke fakture dobavljača i tamo se ne može promijeniti.</p> |
| Datum fakture | Datum za stvarne troškove koji će se kreirati prilikom potvrde fakture dobavljača. | Datum fakture koristi se i za odabir ispravnog cjenika nabave iz cjenika koji su povezani dobavljaču ili iz parametara projekta. |
| Razlog stanja | Status fakture dobavljača. | <p>Status određuje gdje se faktura dobavljača nalazi u poslovnom procesu i može li se uređivati. Evo nekih dostupnih vrijednosti:</p><ul><li>**Skica** – faktura dobavljača može se uređivati.</li><li>**Potvrđeno** – račun dobavljača je provjeren i potvrđen. Fakture dobavljača u ovom statusu ne mogu se uređivati ili brisati.</li><li>**U tijeku** – pregledava se faktura dobavljača. Fakture dobavljača u ovom statusu mogu se uređivati, ali ih nije moguće izbrisati.</li><li>**Otkazano** – faktura dobavljača je otkazana. Fakture dobavljača u ovom statusu ne mogu se uređivati ili brisati.</li></ul> |
| Valuta | Valuta u kojoj dobavljač fakturira proizvode i usluge na fakturi dobavljača. | Na fakturi dobavljača koja upućuje na podugovaranje valuta kooperanta unosi se prema zadanim postavkama kao valuta fakture dobavljača. Na fakturi dobavljača koja se ne odnosi na podugovaranje zadana vrijednost unosi se iz zapisa računa dobavljača i može se promijeniti. Nakon spremanja fakture dobavljača valuta se više ne može uređivati. |
| Ugovorna jedinica | Podjela tvrtke koja je odgovorna za primanje usluga i/ili proizvoda od dobavljača. | Nijedno |
| Uvjeti plaćanja | Uvjeti plaćanja na izdanim fakturama dobavljača. Zadana vrijednost automatski se unosi iz zapisa o računa dobavljača. | Uvjeti plaćanja iz podugovaranja kopiraju se na sve fakture dobavljača koje su povezane s podugovarateljem. Uvjeti plaćanja mogu se ažurirati ako faktura dobavljača ima status **Skica**. |
| Adresa za plaćanje | Adresa dobavljača na kojeg se moraju poslati uplate. Zadana vrijednost automatski se unosi iz zapisa o računa dobavljača. | Adresa za plaćanje iz kooperanta kopira se kao adresa za plaćanje svim fakturama dobavljača kreiranim za taj kooperant. Adresa za plaćanje može se obnoviti ako faktura dobavljača ima status **Skica**. |
| Podzbroj | Ako faktura dobavljača nema retke, unesite podzbroj fakture prije poreza. Ako faktura dobavljača ima retke, ovo je polje samo za čitanje. U tom slučaju prikazani iznos je podzbroja iz svih redaka na fakturi dobavljača. | Nijedno |
| Ukupni porez | Ako faktura dobavljača nema retke, unesite ukupne poreze na kooperant. Ako faktura dobavljača ima retke, ovo je polje samo za čitanje. U tom slučaju prikazani iznos je zbroj iznosa poreza iz svih redaka na fakturi dobavljača. | Nijedno |
| Ukupan iznos | Ova izračunato polje prikazuje ukupan iznos fakture dobavljača nakon uključivanja poreza. | Nijedno |

> [!NOTE]
> Sljedeća polja na fakturi dobavljača ne mogu se promijeniti nakon spremanja fakture dobavljača: **Dobavljač**, **Kooperant**, **Valuta**, **Ugovorna jedinica** i **Uvjeti** plaćanja. Ako su potrebna bilo kakva promjena za ta polja na fakturi dobavljača, morate izbrisati fakturu dobavljača i kreirati novu fakturu dobavljača.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
