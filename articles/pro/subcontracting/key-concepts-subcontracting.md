---
title: Ključni koncepti podugovaranja
description: U ovom se članku objašnjavaju neki ključni koncepti koji se primjenjuju na podugovaranje u Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0ac84d132a2d62528d97ed3776a78062a589a380
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927687"
---
# <a name="key-concepts-in-subcontracting"></a>Ključni koncepti podugovaranja

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

U članku se objašnjavaju neki ključni koncepti kojih biste trebali biti svjesni prije nego što počnete koristiti funkciju podugovaranja u Microsoftu Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Ugovorna jedinica za podugovor

Ugovorna jedinica predstavlja sektor ili praksu koja je vlasnik isporuke mogućeg projekta. Ugovorna jedinica također je sektor koji stupa u ugovorni odnos s prodavateljem.

## <a name="purchase-currency"></a>Valuta kupnje

U aplikaciji Project Operations valuta kupnje je valuta u kojoj je sklopljen podugovor. To je također valuta u kojoj se bilježe troškovi podizvođača na projektu. Valuta kupnje može se razlikovati od valute projekta, a valuta projekta može se razlikovati od valute prodaje.

## <a name="billing-methods-on-subcontract-lines"></a>Načini naplate na redcima podugovora

Za projekte obično postoje modeli ugovaranja na temelju potrošnje s fiksnim naknadama. Project Operations podržava ove načine naplate u kontekstu prodaje i kupnje. Kada se radi o kupnji, metode naplate funkcioniraju na sljedeći način:

- **Vrijeme i materijal** – Kada redak podugovora upotrebljava način naplate **Vrijeme i materijal**, trošak vremena bilježi se na projektu kao rad podizvođača na tom projektu i bilježi vrijeme. Ove se transakcije troškova od podizvođača zatim usklađuju sa stavkama retka na fakturama dobavljača. U ovom načinu, voditelji projekata koji upotrebljavaju rješenje Project Operations mogu usporediti i provjeriti retke fakture dobavljača s vremenom podizvođača koje je zabilježeno i odobreno. Nakon dovršetka provjere, prethodni se stvarni troškovi koji su zabilježeni nakon odobrenja poništavaju, a na projektu se stvaraju novi stvarni troškovi koji se temelje na fakturi dobavljača.
- **Fiksna cijena** – U ovom modelu ugovaranja s fiksnom naknadom, fakture dobavljača temelje se na fiksnim kontrolnim točkama. Međutim, resursi podizvođača također mogu prijaviti vrijeme. Vrijeme zatim pregledava i odobrava voditelj projekta. Kad se odobri, Project Operations stvaraju privremene stvarne troškove na projektu. Nakon što dobavljač pošalje fakturu za kontrolnu točku, voditelj projekta može usporediti prethodno zabilježene stvarne troškove s onima na kontrolnoj točki. Kada se provjera dovrši, stvarni se troškovi poništavaju, a bilježi se trošak koji se temelji na kontrolnoj točki.

## <a name="project-price-lists-on-subcontracts"></a>Cjenici projekta u podugovorima

Cjenici projekta su cjenici koji se upotrebljavaju za postavljanje nabavnih cijena za vrijeme, troškove i ostale komponente povezane s projektom. Može postojati više cjenika, od kojih svaki može imati vlastiti podugovor s datumom stupanja na snagu u rješenju Project Operations. Project Operations ne podržava preklapanje datuma stupanja na snagu na cjenicima projekta za podugovor.

## <a name="transaction-classes-on-subcontracts"></a>Klase transakcija na podugovorima

Project Operations podržava četiri vrste klasa transakcija:

- Vrijeme
- Izdatak
- Materijal
- Naknada

Troškovi kupnje mogu se procijeniti i nastati samo na klasama transakcija **Vrijeme**, **Trošak** i **Materijal**. **Naknada** je klasa transakcije samo za prihod i nije dostupna u sadržaju kupnje.

## <a name="purchase-pricing-dimensions"></a>Veličine za određivane cijena kupnje

Veličine cijena omogućuju vam da odlučite koji se atributi upotrebljavaju za postavljanje nabavne cijene i zadane vrijednosti na vremenskim transakcijama. U odnosu na kupnju, Project Operations podržavaju samo skupove fiksnih veličina za postavljanje nabavne cijene i zadane vrijednosti. Atributi za postavljanje nabavne cijene i zadane vrijednosti na redcima podugovora i vremenskim transakcijama podugovora su **Uloga** i **Resurs koji se može rezervirati**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
