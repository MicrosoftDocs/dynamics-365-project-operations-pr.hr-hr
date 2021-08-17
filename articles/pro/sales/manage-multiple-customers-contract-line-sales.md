---
title: Upravljanje s više klijenata u redcima ugovora koji se temelje na projektu – jednostavno
description: U ovoj temi nalaze se informacije o upravljanju većim brojem klijenata u redcima ugovora koji se temelje na projektu.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a7e29b1a92a5fefcf4812931383d03e5f81a27001f0e6525bb4eeb8dc93b18b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001782"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Upravljanje s više klijenata u redcima ugovora koji se temelje na projektu – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Redci ugovora koji se temelje na projektu mogu sadržavati popis klijenata koji su odgovorni za plaćanje. Ovaj popis klijenata na retku ugovora koji se temelji na projektu može biti jednak popisu klijenata na ugovoru, ali to nije potrebno. Kada se prihvati ponuda projekta i stvori ugovor o projektu, popis klijenata u retku ponude kopira se u odgovarajući redak ugovora. Klijenti na ponudi kopiraju se u ugovor.

Kada se fakturira ugovor o projektu, popis klijenata na retku ugovora koji se temelji na projektu ima prednost pred popisom klijenata u ugovoru. Popis klijenata na ugovoru o projektu upotrebljava se samo za zadavanje novih redaka ugovora.

Svi klijenti ugovora na kartici **Klijenti** ugovora o projektu zadani su kao klijenti retka ugovora na svakom novom retku ugovora koji je stvoren za ugovor o projektu. Svaki postojeći redak ugovora neće naslijediti nove zapise klijenta ugovora stvorene nakon njih.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Stvaranje, ažuriranje ili brisanje zapisa o retku ugovora klijenta

Možete stvoriti, ažurirati ili izbrisati klijenta iz retka ugovora iz kartice Klijenti iz retka ugovora na stranici retka ugovora koji se temelji na projektu. Kada se novi kupac doda u redak ugovora koji se temelji na projektu, dodaje se i na cjelokupni ugovor kao klijent ugovora sa zadanim postotkom raspodjele naplate od nula posto. Postotak raspodjele naplate u ukupnom ugovoru kopira se u nove retke ugovora i u konačni ugovor o projektu. Međutim, tijekom fakturiranja iz ugovora upotrebljava se postotak raspodjele naplate na razini retka ugovora, a ne postotak raspodjele naplate na ukupnoj razini ugovora.

U nastavku se nalaze polja na zapisu klijenta u retku **Ugovora** retka ugovora koji se temelji na projektu kako biste ga imali na umu dok radite s njim:

| Polje | Lokacija | Opis | Utjecaj na niže razine |
| --- | --- | --- | --- |
| **Poslovni subjekt** | Mreža koja se može uređivati na kartici **Ugovorni klijenti** te obrasci **Glavni** i **Brzo stvaranje** za ugovornog klijenta. | Svi aktivni računi. Ovo je polje zaključano nakon stvaranja zapisa. Kako biste ažurirali polje, izbrišite zapis i stvorite novi zapis. Ako ste zabilježili neke stvarne podatke, zapis ne možete izbrisati. Međutim, postotak raspodjele naplate za taj račun možete označiti kao nulu. Kada je zapis označen kao nula, to utječe na sve buduće stvarne troškove i prihode koji se pripisuju ili raspodijele ovom klijentu. | Kada odaberete račun s glavnog popisa računa kako biste ga dodali i spremili, klijent retka ugovora također se dodaje kao klijent ugovora. Klijenti retka ugovora upotrebljavaju se kada se generiraju računi. |
| **Postotak dijeljene naplate** | Mreža koja se može uređivati na kartici **Ugovorni klijenti** te obrasci **Glavni** i **Brzo stvaranje** za ugovornog klijenta. | Polje predstavlja postotak svake nenaplaćene prodajne transakcije koja će se pripisati ovom klijentu retka ugovora. | Klijenti retka ugovora i postoci raspodjele naplate upotrebljavaju se kada se stvaraju stvarni podaci nakon odobrenja i kada se generira faktura. |
| **Ograničenje koje se ne smije prekoračiti** | Mreža koja se može uređivati na kartici **Ugovorni klijenti** te obrasci **Glavni** i **Brzo stvaranje** za ugovornog klijenta. | Označava postoji li dogovoreno ograničenje ili ograničenje ukupnog iznosa koji će se fakturirati tom klijentu za redak ugovora. | Ograničenje koje se ne smije prekoračiti za klijenta retka ugovora upotrebljava se kada se stvaraju stvarni podaci i generiraju fakture. |
| **Na zaokruživanje** | Mreža koja se može uređivati na kartici **Ugovorni klijenti** te obrasci **Glavni** i **Brzo stvaranje** za klijenta retka ugovora. | Ovo polje označava je li ovaj klijent zadani klijent za zaokruživanje za ovaj redak ugovora koji se temelji na projektu. | Kada generirate stvarni podatak prema postotku raspodjele naplate, mogu postojati neke razlike u zaokruživanju. U tom se slučaju razlike u zaokruživanju pripisuju ovom kupcu. |

## <a name="edit-billing-split-percentages"></a>Uređivanje postotka podjele naplate

Postoci raspodjele naplate mogu se uređivati u rešetki. Kada postoci raspodjele naplate ne dosegnu 100 posto, prikazat će se pogreška. Nakon što uredite postotke raspodjele naplate, osvježite stranicu kako biste uklonili pogrešku.

Možete odabrati i mogućnost **Ravnomjerno raspodijeli** na podrešetki klijenta retka ugovora. Ova radnja ravnomjerno raspoređuje naplate na sve klijente retka ugovora. Ako postoji neki čimbenik zaokruživanja, on će se dodati klijentu za zaokruživanje. Jedan klijent retka ugovora uvijek se označava kao klijent za **Zaokruživanje** sa zastavicom **Zaokruživanje** postavljenom na **Da**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]