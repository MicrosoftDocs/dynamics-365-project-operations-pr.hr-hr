---
title: Upravljanje s više klijenata u ugovorima o projektu
description: U ovom se članku nalaze informacije o upravljanju većim brojem korisnika na ugovoru o projektu.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 78ee117c1068e7af4674cc3b21e1055fd05bb43a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928331"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Upravljanje s više klijenata u ugovorima o projektu

U ovom se članku nalaze informacije o upravljanju većim brojem korisnika na ugovoru o projektu. Ugovor o projektu možete upotrebljavati kada je za financiranje posla potreban ugovor s više klijenata. Na stranici **Ugovor o projektu**, kartica **Sažetak** uključuje podatke o primarnom klijentu za posao. Ostali klijenti koji sudjeluju u poslu mogu se dodati na kartici **Klijenti**.

Svi klijenti ugovora na kartici **Klijenti** ugovora o projektu zadani su kao klijenti retka ugovora u svakom novom retku ugovora koji se temelji na projektu stvorenom za ugovor o projektu. Svi postojeći redci ugovora koji se temelje na projektu ne nasljeđuju zapise novih klijenata ugovora koji su stvoreni kasnije.

Klijenti ugovora i retka ugovora mogu se dodati, ažurirati ili izbrisati u bilo kojem trenutku U bilo kojem trenutku prije dobivanja ugovora možete dodati, ažurirati ili izbrisati klijente ugovora i retka ugovora. Klijent ugovora o projektu mora biti postavljen kao klijent u tvrtki ili pravnoj osobi koja je vlasnik na stranici **Klijenti**. Pravne osobe su postavljene u modul **Upravljanje projektima i računovodstvo** aplikacije Dynamics 365 Project Operations i dostupne su kao tvrtke u modulima **Prodaja projekata** i **Isporuka** aplikacije Project Operations.

## <a name="primary-customers"></a>Primarni klijent

Mogući klijent, naveden u kartici **Sažetak** ugovora o projektu, primarni je klijent ugovora. Primarni klijent ne može se ažurirati s popisa klijenata u ugovoru. Ako pokušate izbrisati primarnog klijenta s popisa klijenata u ugovoru, prikazat će se poruka o pogrešci kako se zapis primarnog klijenta u ugovoru ne može izbrisati. Umjesto toga, promijenite klijenta u polju **Mogući klijent** kartice **Sažetak** ugovora o projektu. Kada ovo polje ažurirate, dodaje se novoodabrani klijent kao novi klijent ugovora sa zastavicom **Primarni** postavljenom na **Da**. Prethodni primarni klijent još uvijek je klijent u ugovoru, ali više nije primarni klijent.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Stvaranje, ažuriranje ili brisanje zapisa o klijentu ugovora

Klijenta ugovora možete stvoriti, ažurirati ili izbrisati na kartici **Klijenti ugovora**, na stranici **Ugovor**. Sljedeća su polja uključena u zapis ugovora o projektu o klijentu ugovora.

| **Polje** | **Mjesto** | **Opis** | 
| --- | --- | --- | 
| Poslovni subjekt | Rešetka koja se može uređivati na kartici **Klijenti ugovora** te glavna stranica i stranica za brzo stvaranje za klijenta ugovora. | Navodi sve aktivne račune. Ovo je polje zaključano nakon stvaranja zapisa. Kako biste ažurirali zapis, trebate ga izbrisati i zatim ponovo stvoriti. Ako ste zabilježili bilo koje stvarne podatke ili ako je zapis klijenta ugovora primarni klijent, zapis ne možete izbrisati. Klijenti ugovora kopiraju se kao klijenti retka ugovora kada se stvara redak ugovora. |
| Postotak dijeljene naplate | Rešetka koja se može uređivati na kartici **Klijenti ugovora** te glavna stranica i stranica za brzo stvaranje za klijenta ugovora. | Predstavlja postotak svake nenaplaćene prodajne transakcije pripisane klijentu ugovora. Kada se stvaraju novi redci ugovora o projektu, postotak podjele naplate kopira se u sve novostvorene retke ugovora i za klijente redaka ugovora o projektu. |
| Naziv kontakta za naplatu | Rešetka koja se može uređivati na kartici **Klijenti ugovora** te glavna stranica i stranica za brzo stvaranje za klijenta ugovora. | Ovo tekstno polje treba upotrebljavati za identifikaciju osobe za kontakt na računu za klijenta. Zadana vrijednost dolazi iz povezanog zapisa računa. Naziv kontakta kopira se u stavku **Naplati nazivu iz ugovora** na fakturi koja se generira za klijenta. |
| Naziv za naplatu | Rešetka koja se može uređivati na kartici **Klijenti ugovora** te glavna stranica i stranica za brzo stvaranje za klijenta ugovora. | Ovo polje upotrebljavajte za identifikaciju osobe za kontakt na računu za klijenta. Zadana vrijednost dolazi iz povezanog zapisa računa. Naziv se kopira u polje **Naplati nazivu iz ugovora** na fakturi generiranoj za klijenta. |
| Uvjeti plaćanja | Rešetka koja se može uređivati na kartici **Klijenti ugovora** te glavni stranica i stranica za brzo stvaranje za klijenta ugovora. | Zadana vrijednost dolazi iz povezanog zapisa računa. Naziv kontakta kopira se u stavku **Naplati nazivu iz ugovora** na fakturi generiranoj za klijenta. |
| Tvrtka vlasnik | Rešetka koja se može uređivati na kartici **Klijenti ugovora o projektu** te glavna stranica i stranica za brzo stvaranje za klijenta ugovora o projektu. | Pravna osoba u kojoj je klijent postavljen u modul **Upravljanje projektom i računovodstvo**. Ovo je polje samo za čitanje i postavljeno je na tvrtku vlasnicu ugovora o projektu.</br>Popis klijenata koje treba dodati u polje **Račun** već je filtrirano na popis iz tvrtke vlasnice u modul **Upravljanje projektima i računovodstvo** aplikacije Project Operations. Tvrtka vlasnica jednaka je pravnoj osobi u modulu **Upravljanje projektima i računovodstvo** aplikacije Project Operations. Svi troškovi i prihodi koji proizlaze iz projekta evidentirani su u Glavnoj knjizi tvrtke vlasnice. |
| Na zaokruživanje | Rešetka koja se može uređivati na kartici **Klijenti ugovora** te glavna stranica i stranica za brzo stvaranje za klijenta ugovora. | Označava je li klijent zadani klijent za zaokruživanje za posao. Na ugovoru o projektu može biti samo jedan klijent za zaokruživanje. Kad se trošak i nenaplaćene prodaje podijele na količinu i dovedu do zaokruživanja razlike, ta se razlika primjenjuje na stvarnu vrijednost koja se mapira klijentu. |
| Ograničenje koje se ne smije prekoračiti | Rešetka koja se može uređivati na kartici **Klijenti ugovora** te glavna stranica i stranica za brzo stvaranje za klijenta ugovora. | Označava postoji li dogovoreno ograničenje ili ograničenje ukupnog iznosa koji će se fakturirati klijentu za angažman. Postavljanje ograničenja koje se ne smije prekoračiti na razini klijenta ugovora ocjenjuje se na temelju stvarnih vrijednosti nenaplaćene prodaje koje se odnose na ovog klijenta ugovora. |

## <a name="edit-billing-split-percentages"></a>Uređivanje postotka podjele naplate

Postotke raspodjele naplate možete uređivati u rešetki. Kada postoci raspodjele naplate ne dosegnu 100 posto, prikazuje se pogreška. Nakon što uredite postotak raspodjele naplate, osvježite stranicu **Ugovor o projektu** kako biste uklonili pogrešku.

Možete odabrati i mogućnost **Ravnomjerno raspodijeli** na podrešetki klijenata ugovora o projektu. Raspodjele naplate ravnomjerno su raspoređene na sve klijente ugovora o projektu. Ako postoji neki čimbenik zaokruživanja, on će se dodati klijentu za zaokruživanje. Jedan od klijenata ugovora uvijek ima zastavicu **Zaokruživanje** postavljenu na **Da**. Taj je klijent, klijent za zaokruživanje. Obično je klijent za zaokruživanje ujedno i primarni klijent ugovora, ali to nije uvjet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]