---
title: Upravljanje s više klijenata u redcima ugovora koji se temelje na projektu
description: U ovoj temi nalaze se informacije o načinu rada s redcima ugovora i ugovorima koji sadrže više klijenata.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2b302368bcb476527c94d48f7693058d2044c74b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996422"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a>Upravljanje s više klijenata u redcima ugovora koji se temelje na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Redci ugovora koji se temelje na projektu mogu sadržavati popis klijenata koji su odgovorni za plaćanje. Ovaj popis klijenata na retku ugovora koji se temelji na projektu može biti jednak popisu klijenata na ugovoru, ali to nije potrebno. Kada se prihvati ponuda projekta i stvori ugovor o projektu, popis klijenata u retku ponude kopira se u odgovarajući redak ugovora. Klijenti na ponudi kopiraju se u ugovor.

Kada se fakturira ugovor o projektu, popis klijenata na retku ugovora koji se temelji na projektu ima prednost pred popisom klijenata u ugovoru. Popis klijenata na ugovoru o projektu upotrebljava se samo za zadavanje novih redaka ugovora.

Svi klijenti ugovora na kartici **Klijenti** ugovora o projektu zadani su kao klijenti retka ugovora na svakom novom retku ugovora koji je stvoren za ugovor o projektu. Svaki postojeći redak ugovora neće naslijediti nove zapise klijenta ugovora stvorene nakon njih.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Stvaranje, ažuriranje ili brisanje zapisa o retku ugovora klijenta

Možete stvoriti, ažurirati ili izbrisati klijenta iz retka ugovora iz kartice **Klijenti retka ugovora** na stranici **Retka ugovora koji se temelji na projektu**. Kada se novi kupac doda u redak ugovora koji se temelji na projektu, dodaje se i na cjelokupni ugovor kao klijent ugovora sa zadanim postotkom raspodjele naplate od nula posto. Postotak raspodjele naplate u ukupnom ugovoru kopira se u nove retke ugovora i u konačni ugovor o projektu. Međutim, tijekom fakturiranja iz ugovora upotrebljava se postotak raspodjele naplate na razini retka ugovora, a ne postotak raspodjele naplate na ukupnoj razini ugovora. 

U nastavku se nalaze polja na zapisu klijenta u retku Ugovora, retka ugovora koji se temelji na projektu kako biste ga imali na umu dok radite s njim:

| Polje | Lokacija | Opis | Utjecaj na niže razine |
| --- | --- | --- | --- |
| Poslovni subjekt | Rešetka koja se može uređivati na kartici **Klijenti retka ugovora** te obrasci Glavni i Brzo stvaranje za klijenta retka ugovora | Svi aktivni računi. Ovo je polje zaključano nakon stvaranja zapisa. Kako biste ažurirali polje, izbrišite zapis i stvorite novi zapis. Ako ste zabilježili neke stvarne podatke, zapis ne možete izbrisati. Međutim, postotak raspodjele naplate za taj račun možete označiti kao nulu. Kada je zapis označen kao nula, to utječe na sve buduće stvarne troškove i prihode koji se pripisuju ili raspodijele ovom klijentu. | Kada odaberete račun s glavnog popisa računa kako biste ga dodali i spremili, klijent retka ugovora također se dodaje kao klijent ugovora. Klijenti retka ugovora upotrebljavaju se kada se generiraju računi. |
| Postotak podjele naplate | Rešetka koja se može uređivati na kartici **Klijenti retka ugovora** te obrasci Glavni i Brzo stvaranje za klijenta retka ugovora | Polje predstavlja postotak svake nenaplaćene prodajne transakcije koja će se pripisati ovom klijentu retka ugovora. | Klijenti retka ugovora i postoci raspodjele naplate upotrebljavaju se kada se stvaraju stvarni podaci nakon odobrenja i kada se generira faktura. |
| Ograničenje koje se ne smije prekoračiti | Rešetka koja se može uređivati na kartici **Klijenti retka ugovora** te obrasci Glavni i Brzo stvaranje za klijenta retka ugovora | Označava postoji li dogovoreno ograničenje ili ograničenje ukupnog iznosa koji će se fakturirati tom klijentu za redak ugovora. | Ograničenje koje se ne smije prekoračiti za klijenta retka ugovora upotrebljava se kada se stvaraju stvarni podaci i generiraju fakture. |
| Tvrtka vlasnik | Rešetka koja se može uređivati na kartici **Klijenti retka ponude** te obrasci Glavni i Brzo stvaranje za klijenta retka ponude | Pravna osoba u kojoj je ovaj klijent postavljen. Ovo je polje samo za čitanje i postavljeno je na tvrtku vlasnicu ponude. Popis klijenata koje treba dodati u polje **Račun** već je filtrirano na popis iz ove tvrtke vlasnice. | Koncept tvrtke vlasnice izjednačava se s konceptom pravne osobe. Svi troškovi i prihodi koji proizlaze iz ovog projekta evidentirani su u Glavnoj knjizi tvrtke vlasnice. |
| Na zaokruživanje | Rešetka koja se može uređivati na kartici **Klijenti retka ugovora** te obrasci Glavni i Brzo stvaranje za klijenta retka ugovora | Ovo polje označava je li ovaj klijent zadani klijent za zaokruživanje za ovaj redak ugovora koji se temelji na projektu. | Kada generirate stvarni podatak prema postotku raspodjele naplate, mogu postojati neke razlike u zaokruživanju. U tom se slučaju razlike u zaokruživanju pripisuju ovom kupcu. |

## <a name="edit-billing-split-percentages"></a>Uređivanje postotka podjele naplate

Postoci raspodjele naplate mogu se uređivati u rešetki. Kada postoci raspodjele naplate ne dosegnu 100 posto, prikazat će se pogreška. Nakon što uredite postotke raspodjele naplate, osvježite stranicu kako biste uklonili pogrešku.

Možete pokušati i odabirom mogućnosti **Ravnomjerno raspodijeli** na podrešetki klijenta retka ugovora. Ova radnja ravnomjerno raspoređuje naplate na sve klijente retka ugovora. Ako postoji neki čimbenik zaokruživanja, on će se dodati klijentu za zaokruživanje. Jedan klijent retka ugovora uvijek se označava kao klijent za **Zaokruživanje** sa zastavicom **Zaokruživanje** postavljenom na **Da**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]