---
title: Upravljanje s više klijenata u ugovorima o projektu – jednostavno
description: U ovoj temi nalaze se informacije o upravljanju većim brojem klijenata u ugovorima o projektu.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c9804c77cc0931352b026f15fd764f43361757f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273144"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Upravljanje s više klijenata u ugovorima o projektu – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ugovori o projektu u aplikaciji Dynamics 365 Project Operations podržavaju scenarij u kojem sporazum iz ugovora uključuje više klijenata koji financiraju posao. Kartica **Sažetak**, na stranici **Ugovor o projektu** uključuje polje **Klijent**. Ovo polje identificira primarnog klijenta posla. Ostali klijenti u poslu mogu se postaviti na karticu **Klijenti**, na stranici **Ugovor o projektu**.

Svi klijenti ugovora navedeni u ugovoru o projektu zadani su kao klijenti redaka ugovora na svakom novom retku ugovora koji se temelji na projektu koji je stvoren za ugovor o projektu. Postojeći redci ugovora koji se temelje na projektu ne nasljeđuju nove klijente ugovora jer se stvaraju novi zapisi.

Redci ugovora koji se temelje na proizvodu automatski se povezuju s primarnim klijentom.

Klijenti ugovora i retka ugovora mogu se dodati, ažurirati ili izbrisati u bilo kojem trenutku prije dobivanja ugovora.

## <a name="primary-customer"></a>Primarni klijent

Klijent naveden na kartici **Sažetak** ugovora o projektu kao mogući klijent, primarni je klijent ugovora. Kada pokušate izbrisati primarnog klijenta s popisa klijenata u ugovoru, dobit ćete poruku o pogrešci da se zapis primarnog klijenta u ugovoru ne može izbrisati.

Primarni klijent ne može se ažurirati s popisa klijenata ugovora. Umjesto toga, u ugovoru promijenite mogućeg klijenta na kartici **Sažetak**. Kada se ovo polje ažurira na stranici **Sažetak ugovora**, novi se klijent dodaje kao novi klijent ugovora s postavljenom zastavicom **Primarni**. Prethodni primarni klijent i dalje će biti klijent u ugovoru.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Stvaranje, ažuriranje ili brisanje zapisa o klijentu ugovora

Klijent ugovora može se stvoriti, ažurirati ili izbrisati na kartici **Klijenti**, na stranici **Ugovor o projektu**. Polja u sljedećoj tablici nalaze se u zapisu klijenta ugovora o projektu i treba ih imati na umu tijekom rada s ugovorom.

| Polje | Lokacija | Opis | Utjecaj na niže razine |
| --- | --- | --- | --- |
| **Poslovni subjekt** | Rešetka se može uređivati na kartici **Klijenti ugovora** te obrascima za klijenta ugovora **Glavni** i **Brzo stvaranje**. | Navodi sve aktivne račune. Ovo je polje zaključano nakon stvaranja zapisa. Kako biste ažurirali račun, izbrišite zapis i ponovo ga stvorite. Ako ste zabilježili bilo koje stvarne podatke ili ako je zapis klijenta ugovora primarni klijent, zapis ne možete izbrisati. | Klijenti ugovora kopiraju se kao klijenti retka ugovora kada se stvara redak ugovora. |
| **Postotak dijeljene naplate** | Rešetka se može uređivati na kartici **Klijenti ugovora** te obrascima za klijenta ugovora **Glavni** i **Brzo stvaranje**. | Predstavlja postotak svake nenaplaćene prodajne transakcije koja se pripisuje ovom klijentu ugovora. | Kopirano na nove ugovorne linije i na klijente retka ugovora o projektu na novim redcima ugovora o projektu. |
| **Naziv kontakta za naplatu** | Rešetka se može uređivati na kartici **Klijenti ugovora** te obrascima za klijenta ugovora **Glavni** i **Brzo stvaranje**. | Ovo tekstno polje trebalo bi se upotrebljavati za identifikaciju osobe za kontakt na fakturi za ovog klijenta. Ovo je polje zadano iz povezanog zapisa računa. | Kopirano u polje **Naplati nazivu iz ugovora** na fakturi koja se generira za ovog klijenta. |
| **Naziv za naplatu** | Rešetka se može uređivati na kartici **Klijenti ugovora** te obrascima za klijenta ugovora **Glavni** i **Brzo stvaranje** | Ovo tekstno polje trebalo bi se upotrebljavati za identifikaciju osobe za kontakt na fakturi za ovog klijenta. Ovo je polje zadano iz povezanog zapisa računa. | Kopirano u polje **Naplati nazivu iz ugovora** na fakturi koja se generira za ovog klijenta. |
| **Uvjeti plaćanja** | Rešetka se može uređivati na kartici **Klijenti ugovora** te obrascima za klijenta ugovora **Glavni** i **Brzo stvaranje**. | Vrijednosti zadaje povezani zapis računa. | Kopirano u polje **Naplati nazivu iz ugovora** na fakturi koja se generira za ovog klijenta. |
| **Na zaokruživanje** | Rešetka se može uređivati na kartici **Klijenti ugovora** te obrascima za klijenta ugovora **Glavni** i **Brzo stvaranje**. | Označava je li ovaj klijent zadani klijent zaokruživanja za ovaj posao. Na ugovoru o projektu može biti samo jedan klijent za zaokruživanje. | Kad se trošak i nenaplaćene prodaje podijele na količinu dolazi do zaokruživanja razlike, a ta se razlika primjenjuje na stvarnu vrijednost koja se mapira ovom klijentu. |
| **Ograničenje koje se ne smije prekoračiti** | Rešetka se može uređivati na kartici **Klijenti ugovora** te obrascima za klijenta ugovora **Glavni** i **Brzo stvaranje** | Označava postoji li dogovoreno ograničenje ili ograničenje ukupnog iznosa koji će se fakturirati klijentu za ovaj angažman. | Postavljanje **Ograničenja koje se ne smije prekoračiti** na razini klijenta ugovora ocjenjivat će se u stavci **Nenaplaćena stvarna prodaja** koja upućuje na ovog klijenta ugovora. |

## <a name="edit-billing-split-percentages"></a>Uređivanje postotka podjele naplate

Postoci raspodjele naplate mogu se uređivati s pomoću iskustva uređivanja rešetke unutar retka. Kada postoci raspodjele naplate ne dosegnu 100 posto, dobit ćete pogrešku. Nakon što uredite postotke dijeljene naplate, osvježite stranicu kako biste odbacili pogrešku.

Također možete odabrati mogućnost **Ravnomjerno rasporedi** na podrešetki **Klijenti ugovora** za ravnomjernu raspodjelu naplate svim klijentima ugovora. Ako postoji čimbenik zaokruživanja, on će se dodati klijentu za zaokruživanje. Jedan od klijenata ugovora uvijek je označen kao klijent za **zaokruživanje**, što znači da je na zapisu klijenta ugovora zastavica za zaokruživanje postavljena na **Da**. To je obično primarni klijent iz ugovora, ali to se također može promijeniti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]