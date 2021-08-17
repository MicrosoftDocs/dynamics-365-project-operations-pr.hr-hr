---
title: Upravljanje s više klijenata u redcima ponude koji se temelje na projektu – jednostavno
description: U ovoj temi opisuje se način upravljanja višestrukim klijentima u redcima ponude koji se temelje na projektu.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d015e9107741fd496f7d3639731f33fcdcc9b9bdd5f501c9ad2617e37a707f35
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001692"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines---lite"></a>Upravljanje s više klijenata u redcima ponude koji se temelje na projektu – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Redci ponude koji se temelje na projektu podržavaju scenarije u kojima svaki redak ponude ima popis klijenata koji to plaćaju. Ovaj popis klijenata u retku ponude koji se temelji na projektu može biti jednak popisu klijenata na ponudi. Također možete promijeniti popis klijenata kako bi bio drugačiji. Kada se prihvati ponuda projekta, popis klijenata na retku ponude koji se temelji na projektu kopira se u odgovarajući redak ugovora koji se temelji na projektu kako bi se stvorio konačni ugovor o projektu. Klijenti u ponudi koji se temelji na projektu kopiraju se u ugovor o projektu.

Kada fakturirate konačni ugovor o projektu, popis klijenata u retku ugovora koji se temelji na projektu ima prednost pred popisom u ugovoru o projektu. Popis klijenata na ugovoru o projektu upotrebljava se samo za zadane postavke u novim redcima ugovora o projektu.

Svi klijenti ponude na kartici **Klijenti** ponude projekta zadani su kao klijenti retka ponude na svakom novom retku ponude koji se temelji na projektu, a stvoren je za ponudu projekta. Svaki postojeći redak ponude koji se temelji na projektu ne nasljeđuje nove zapise o klijentima stvorene nakon njih.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Stvaranje, ažuriranje ili brisanje zapisa o klijentu retka ponude

Možete stvoriti, ažurirati ili izbrisati klijenta retka ponude na kartici **Klijenti retka ponude** na stranici **Redak ponude koji se temelji na projektu**. Kada dodate novog klijenta u redak ponude koji se temelji na projektu, klijent se dodaje i ukupnoj ponudi kao klijent ponude, sa zadanim postotkom podjele naplate u ukupnoj ponudi od 0%. Postotak podjele naplate u ukupnoj ponudi kopira se u nove retke ponude i na konačni ugovor o projektu. Međutim, tijekom fakturiranja iz ugovora upotrebljava se postotak podjele naplate na razini retka ponude, a ne postotak podjele naplate na ukupnoj razini ugovora. 

Sljedeća tablica prikazuje polja u zapisu o klijentu retka ponude koji se temelji na projektu.

| Polje | Lokacija | Opis i smjernice | Utjecaj na niže razine |
| --- | --- | --- | --- |
| **Poslovni subjekt** | Rešetka koja se može uređivati na kartici **Klijenti retka ponude**, glavni obrazac i obrasci za brzo stvaranje za klijenta retka ponude. | Navodi sve aktivne račune. Ovo je polje zaključano nakon stvaranja zapisa. Ako trebate ažurirati polje, izbrišite i ponovno stvorite zapis. Ako ste zabilježili neke stvarne podatke, zapis ne možete izbrisati. | Kada odaberete račun s glavnog popisa računa koji želite dodati, klijent retka ponude također se dodaje kao klijent ponude kada ga spremite. Kada se prihvati ponuda, klijenti retka ponude kopiraju se u klijente retka ugovora. |
| **Postotak dijeljene naplate** | Rešetka koja se može uređivati na kartici **Klijenti retka ponude**, glavni obrazac i obrasci za brzo stvaranje za klijenta retka ponude. | Predstavlja postotak svake nefakturirane prodajne transakcije koja će se pripisati ovom klijentu retka ponude. | Kopirano na klijente retka ugovora o projektu. |
| **Ograničenje koje se ne smije prekoračiti** | Rešetka koja se može uređivati na kartici **Klijenti retka ponude**, glavni obrazac i obrasci za brzo stvaranje za klijenta retka ponude. | Označava postoji li dogovoreno ograničenje ili gornja granica ukupnog iznosa koji će se fakturirati ovom klijentu za ovaj redak ponude. | Kopira se preko klijenata iz redaka ugovora o projektu kada se prihvati ponuda. |
| **Zaokruženo je** | Rešetka koja se može uređivati na kartici **Klijenti retka ponude**, glavni obrazac i obrasci za brzo stvaranje za klijenta retka ponude. | Označava je li ovaj klijent zadani klijent za zaokruživanje za ovaj redak ponude zasnovan na projektu. | Kopira se preko klijenata ugovora o projektu kada se prihvati ponuda. |

## <a name="edit-billing-split-percentages"></a>Uređivanje postotka podjele naplate

Postotke podjele naplate možete urediti u retku. Kada postoci podjele naplate ne iznose 100 %, dogodi se pogreška. Nakon što uredite postotke podjele naplate, osvježite stranicu retka ponude kako biste uklonili pogrešku.

Upotrijebite radnju ravnomjerne raspodjele na podrešetki klijenata iz retka ponude kako biste podjele naplate dodijelili svim klijentima iz retka ponude. Ako postoji faktor zaokruživanja, to će se dodati klijentu zaokruživanja. Jedan od klijenata retka ponude uvijek je označen kao klijent zaokruživanja, što znači da zapis klijenta retka ponude ima zastavicu zaokruživanja postavljenu na **Da**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]