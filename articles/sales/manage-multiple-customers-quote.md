---
title: Upravljanje s više klijenata u ponudi projekta
description: U ovoj temi nalaze se informacije o radu s ponudama koje uključuju više klijenata koji će financirati projekt.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2b57d052d6b50ee420249cf5441077b092b4e13f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277869"
---
# <a name="manage-multiple-customers-on-a-project-quote"></a>Upravljanje s više klijenata u ponudi projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Ponude projekata podržavaju scenarij u kojem prijedlog uključuje više klijenata koji će financirati posao. Kartica **Sažetak** ponude ima polje **Potencijalni klijent** koje identificira primarnog klijenta posla. Ostali klijenti posla mogu se postaviti na karticu **Klijenti** ponude projekta.

Svi klijenti ponude na kartici **Klijenti** ponude projekta zadani su kao klijenti retka ponude na svakom **novom** retku ponude koji se temelji na projektu, a stvoren je za ponudu. Svaki postojeći redak ponude koji se temelji na projektu neće naslijediti nove zapise o klijentima stvorene nakon njih.

Klijenti ponude i klijenti retka ponude mogu se dodati, ažurirati ili izbrisati u bilo kojem trenutku prije prihvaćanja ponude. Valjani klijent na ponudi mora biti postavljen kao klijent u tvrtki vlasnici ili pravnoj osobi na stranici **Klijenti**. Pravne su osobe postavljene u modul **Upravljanje projektima i računovodstvo** aplikacije Dynamics 365 Project Operations i dostupne su kao tvrtke u modulima **Prodaja i isporuka projekata** aplikacije Project Operations.

## <a name="concept-of-a-primary-customer"></a>Koncept primarnog klijenta

Klijent naveden na kartici **Sažetak** ponude projekta kao potencijalni klijent, primarni je klijent ponude. Ako pokušate izbrisati primarnog klijenta s popisa klijenata na ponudi, prikazat će se pogreška da se primarni zapis klijenta na ponudi ne može izbrisati.

Primarni klijent ne bi se trebao ažurirati s popisa klijenata na ponudi. Međutim, možete utjecati na primarnog klijenta promjenom potencijalnog klijenta na kartici **Sažetak** ponude. Kada se ovo polje ažurira na stavci **Sažetak ponude**, novoodabrani potencijalni klijent dodaje se kao novi klijent ponude sa zastavicom postavljenom na **Primarni**. Stari potencijalni klijent i dalje će biti klijent na ponudi.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Stvaranje, ažuriranje ili brisanje zapisa o klijentu ponude

Klijent ponude može se stvoriti, ažurirati ili izbrisati iz kartice **Klijenti ponude** na stranici **Ponuda**. Polja navedena u sljedećoj tablici polja su u zapisu o klijentu ponude iz ponude projekta.

| **Polje** | **Mjesto** | **Opis** | **Utjecaj prema dolje** |
| --- | --- | --- | --- |
| Poslovni subjekt | Rešetka koja se može uređivati na kartici **Klijenti ponude** te obrasci **Glavni** i **Brzo stvaranje** za klijenta ponude. | Navodi sve aktivne račune. Ovo je polje zaključano nakon stvaranja zapisa. Ako ga želite ažurirati, izbrišite zapis i ponovo ga stvorite. Ako ste zabilježili bilo koje stvarne podatke ili ako je zapis klijenta ponude primarni klijent, moći ćete ga izbrisati. | Kada se stvori redak ponude, klijenti ponude kopiraju se kao klijenti retka ugovora. Kada se prihvati ponuda, klijenti ponude kopiraju se također u klijente ugovora. o projektu |
| Postotak podjele naplate | Rešetka koja se može uređivati na kartici **Klijenti ponude** te obrasci **Glavni** i **Brzo stvaranje** za klijenta ponude. | Predstavlja postotak svake nenaplaćene prodajne transakcije koja će se pripisati ovom klijentu ponude. | Kopira se u novostvorene retke ponude i klijente ugovora o projektu. |
| Naziv kontakta za naplatu | Rešetka koja se može uređivati na kartici **Klijenti ponude** te obrasci **Glavni** i **Brzo stvaranje** za klijenta ponude. | Ovo je tekstno polje i trebalo bi se upotrebljavati za identifikaciju osobe za kontakt na fakturi za ovog klijenta. One su zadane iz povezanog zapisa računa | Kopira se u klijente ugovora o projektu kada se ponuda prihvati i povratno u polje Naziv ugovora za naplatu na fakturi koja se generira za tog klijenta. |
| Naziv za naplatu | Rešetka koja se može uređivati na kartici **Klijenti ponude** te obrasci **Glavni** i **Brzo stvaranje** za klijenta ponude. | Ovo tekstno polje trebalo bi se upotrebljavati za identifikaciju osobe za kontakt na fakturi za ovog klijenta. | Kopira se u klijente ugovora o projektu kada se ponuda prihvati i povratno u polje **Naziv ugovora za naplatu** na fakturi koje se generira za tog klijenta. |
| Uvjeti plaćanja | Rešetka koja se može uređivati na kartici **Klijenti ponude** te obrasci **Glavni** i **Brzo stvaranje** za klijenta ponude. | Ovo je skup mogućnosti s vrijednostima koje se zadaju iz povezanog zapisa računa. | Kopira se u klijente ugovora o projektu kada se ponuda prihvati i povratno u polje **Naziv ugovora za naplatu** na fakturi koje se generira za tog klijenta. |
| Na zaokruživanje | Rešetka koja se može uređivati na kartici **Klijenti ponude** te obrasci **Glavni** i **Brzo stvaranje** za klijenta ponude. | Označava je li ovaj klijent zadani klijent zaokruživanja za ovaj posao. | Kopira se klijentima ugovora o projektu kada se prihvati ponuda. |
| Tvrtka vlasnik | Rešetka koja se može uređivati na kartici **Klijenti ponude** te obrasci **Glavni** i **Brzo stvaranje** za klijenta ponude. | Pravna osoba u kojoj je ovaj klijent postavljen u modul **Upravljanje projektima i računovodstvo**. Ovo je polje samo za čitanje i postavljeno je za tvrtku vlasnicu same ponude. Popis klijenata koje treba dodati u polje **Račun** već je filtrirano na popis iz te tvrtke vlasnice u modul **Upravljanje projektima i računovodstvo** aplikacije Project Operations. | Tvrtka vlasnica izjednačava se s konceptom pravne osobe u modulu **Upravljanje projektima i računovodstvo** aplikacije Project Operations. Svi troškovi i prihod koji proizlaze iz ovog projekta evidentiraju se u glavnoj knjizi tvrtke vlasnice. |
| Ograničenje koje se ne smije prekoračiti | Rešetka koja se može uređivati na kartici **Klijenti ponude** te obrasci **Glavni** i **Brzo stvaranje** za klijenta ponude. | Označava postoji li dogovoreno ograničenje ili gornja granica ukupnog iznosa koji će se fakturirati ovom klijentu za ovaj angažman. | Kopira se klijentima ugovora o projektu kada se prihvati ponuda. |

## <a name="editing-billing-split-percentages"></a>Uređivanje postotka podjele naplate

Postotke podjele naplate možete urediti s pomoću iskustva uređivanja rešetke u retku. Kada postoci podjele naplate ne iznose 100 %, doći će do pogreške. Nakon što ažurirate postotke podjele naplate, osvježite stranicu kako biste uklonili pogrešku.

Također možete pokušati odabrati mogućnost **Ravnomjerno rasporedi** na podrešetki ponude za klijenta. Ova radnja raspoređuje podjelu naplate na sve klijente iz ponude. Ako postoji faktor zaokruživanja, to će se dodati klijentu zaokruživanja. Jedan od klijenata iz ponude uvijek je označen kao klijent zaokruživanja. to znači da zapis klijenta iz ponude ima zastavicu **Zaokruživanje** postavljenu na **Da**. To je obično primarni klijent iz ponude, ali to se može promijeniti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]