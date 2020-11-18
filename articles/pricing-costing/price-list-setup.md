---
title: Postavljanje cjenika
description: U ovoj temi nalaze se informacije o načinu postavljanja cjenika koštanja i prodaje.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 578f5641659a5d05785781afe7055fe4449cf799
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087850"
---
# <a name="set-up-price-lists"></a>Postavljanje cjenika

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Cjenici u aplikaciji Dynamics 365 Project Operations predstavljaju katalog cijena. Cijene izražavaju trošak, prodaju i cijene naplate. Ovisno o tome izražava li cjenik cijene troška ili cijene prodaje i naplate, kontekst cjenika je **Prodaja** ili **Trošak**.

Sljedeća proširenja specifična su za aplikaciju Project Operations i primjenjuju se na cjenike iz aplikacije Dynamics 365 Sales.

- **Kontekst** : Ovo polje ima podržane vrijednosti **Trošak** i **Prodaja**. Vrijednost **Kupnja** nije podržana. Kontekst postavite na **Trošak** kako biste napravili cjenik troškova ili kontekst postavite na **Prodaja** za prodajni cjenik. Cjenici troškova rješavaju cijenu za vrstu troška na zapisima procjene i stvarnih podataka. Prodajni cjenici rješavaju cijenu na zapisima procjena i stvarnih podataka nenaplaćenih i naplaćenih vrsta prodaje.
- **Jedinica vremena** : Ovo je zadana jedinica vremena za koju se cijena postavlja u odgovarajućoj tablici **Cijena uloge** za ovaj cjenik.
- **Entitet cjenika** : U aplikaciji Project Operations ovo je polje skriveno kako bi se cjenici koji su specifični za ponudu ili ugovor razlikovali od onih koji su standardni i globalno primjenjivi.

## <a name="price-list-header"></a>Zaglavlje cjenika

Sljedeća tablica uključuje polja na kartici **Općenito** cjenika koja su jedinstvena za aplikaciju Project Operations ili imaju značajne promjene u ponašanju iz cjenika prodaje.

| Polje | Lokacija | Relevantnost, svrha i smjernice | Utjecaj na niže razine |
| --- | --- | --- | --- |
| Ime | Kartica **Općenito** i obrasci **Brzo stvaranje** | Identitet cjenika. | Cjenik se s ovom vrijednošću prikazuje na svim stranicama popisa i padajućim mogućnostima.|
| Kontekst | Kartica **Općenito** i obrasci **Brzo stvaranje** | Ovo se polje može postaviti na **Trošak** ili **Prodaja**. | Cjenik postavljen na **Trošak** upotrebljava se za traženje cijene za procjene troškova i stvarne troškove. Cjenik postavljen na **Prodaja** upotrebljava se za traženje cijene za procjene prodaje i stvarnu prodaju. Samo cjenici s kontekstom postavljenim na **Prodaja** mogu se priložiti cjenicima projekta za klijente, ponude projekta ili ugovore o projektu. |
| Datum početka | Kartica **Općenito** i obrasci **Brzo stvaranje** | Datum početka razdoblja u kojem je cjenik na snazi. | Uz polje **Datum završetka** , ovo se polje upotrebljava za određivanje cjenika mjerodavnog za određeni redak procjene ili stvarnog podatka. |
| Datum završetka | Kartica **Općenito** i obrasci **Brzo stvaranje** | Datum završetka razdoblja u kojem je cjenik na snazi. | Uz polje **Datum početka** , ovo se polje upotrebljava za određivanje cjenika mjerodavnog za određeni redak procjene ili stvarnog podatka. |
| Valuta | Kartica **Općenito** i obrasci **Brzo stvaranje** | Ovo se polje upotrebljava za zadavanje valute u retku svake uloge, kategorije ili stavke cjenika povezanom s ovim cjenikom. | U cjenicima, ulogama, kategorijama ili stavki cjenika **Prodaja** redci se ne mogu stvarati ni u jednoj valuti osim ove valute. U cjenicima **Trošak** možete stvoriti redak cijene uloge u svakoj valuti. Ovdje definirana valuta upotrebljava se kao zadana. Korisničko postavljanje koje je povezano s cijenama uloga može nadjačati ovu vrijednost kako bi omogućilo postavljanje cijene troška radne snage u svakoj valuti. Cijene kategorije troškova i troškovi stavki cjenika mogu se postaviti samo u ovdje definiranoj valuti. |
| Jedinica vremena | Kartica **Općenito** i obrasci **Brzo stvaranje** | Ovo se polje upotrebljava za zadavanje vremenske jedinice u retku svake uloge povezane s ovim cjenikom. | Ova vrijednost polja upotrebljava se samo za postavljanje cijene povezane uloge. U cjenicima **Trošak** i **Prodaja** možete stvoriti redak cijene uloge u svakoj jedinici vremena. Ovdje definirana jedinica vremena upotrebljava se kao zadana. Korisničko postavljanje koje je povezano s cijenama uloga može nadjačati ovu vrijednost kako bi omogućilo postavljanje cijene troška radne snage i naplate u svakoj jedinici vremena. |
| Opis | Kartica **Općenito** i obrasci **Brzo stvaranje** | Ovo tekstno polje omogućuje vam da osigurate opis cjenika u više redaka. | Ovo se polje prikazuje u prikazu **Pridružen** na cjeniku različitih entiteta koji imaju povezane cjenike. |