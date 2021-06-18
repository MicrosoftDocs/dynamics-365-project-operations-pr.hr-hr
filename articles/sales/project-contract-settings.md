---
title: Postavke ugovora o projektu
description: U ovoj temi nalaze se informacije o poljima koja utječu na retke ugovora i informacije o ugovoru koje su sažete u svim stavkama retka.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e6971553bb436ee5bcad2c335d32c929ddc4800
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996152"
---
# <a name="header-details-for-project-based-contracts"></a>Pojedinosti zaglavlja za ugovore koje se temelje na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovoj temi nalaze se informacije o poljima koja se primjenjuju na cjelokupni ugovor o projektu, uključujući postavke koje utječu na sve retke ugovora. Uključene su i informacije o ugovoru koje su sažete u svim stavkama retka za pokretanje KPI-jeva ugovora o projektu.

Tablica u nastavku prikazuje polja u ugovoru o projektu koja su jedinstvena za aplikaciju Dynamics 365 Project Operations ili imaju neke značajne promjene u ponašanju iz prodajnih naloga u aplikaciji Dynamics 365 Sales.

| Polje | Lokacija | Opis | Utjecaj na niže razine |
| --- | --- | --- | --- |
| Tip | Kartica **Sažetak**(skrivena) | Ovo je polje skupa mogućnosti i ima sljedeće mogućnosti:</br>- **Na temelju rada** (dostupno samo kada je instalirana aplikacija Project Operations)</br>- **Na temelju stavke** (dostupno samo kada su instalirane aplikacije Project Operations i Prodaja)</br>- **Na temelju usluge održavanja** (dostupno kada je instalirana aplikacija Dynamics 365 Field Service) | U aplikaciji Project Operations vrijednost ovog polja zadana je za mogućnost **Na temelju rada** i klasificira ugovor kao ugovor koji se temelji na projektu. Ugovor bi se trebao temeljiti na projektu kako bi se omogućila sva proširenja i funkcionalnosti specifične za projekt. |
| Tvrtka vlasnik | Kartica **Sažetak** | Pravna osoba koja obračunava troškove i prihod koji proizlaze iz ovog projekta ili projekata povezanih s ovim ugovorom o projektu. Kada je iz prilike stvori ugovor, ovo se polje kopira iz odgovarajućeg polja u zapisu ponude. | Tvrtka vlasnica izjednačava se s konceptom pravne osobe u modulu **Upravljanje projektima i računovodstvo** aplikacije Project Operations. Svi troškovi i prihod koji su proizašli iz ovog projekta evidentiraju se u glavnoj knjizi tvrtke vlasnice. |
| Klijent | Kartica **Sažetak** | Upućivanje na zapis tvrtke ili računa klijenta. Kada je iz prilike stvori ugovor, ovo se polje kopira iz odgovarajućeg polja u zapisu ponude. | Valuta na ugovoru o projektu zadana je na temelju valute klijenta. Valuta se može promijeniti prije nego što se ugovor spremi. |
| Voditelj računa | Kartica **Sažetak** | Naziv upravitelja računa za ovaj posao. Kada je iz prilike stvori ugovor, ovo se polje kopira iz odgovarajućeg polja u zapisu ponude. | Upravitelj računa odgovoran je za upravljanje odnosom s klijentom kroz dovršetak ovog projekta. Na temelju zapisa resursa koji se može rezervirati vezanog za upravitelja računa, ugovorna jedinica zadana je u ugovoru o projektu. |
| Ugovorena jedinica | Kartica **Sažetak** | Organizacijska jedinica koja je odgovorna za isporuku projekata povezanih s ovim ugovorom. Kada je iz prilike stvori ugovor, ovo se polje kopira iz odgovarajućeg polja u zapisu ponude. | Ugovorna jedinica sektor je tvrtke koji izvršava projekte. Svaka ugovorna jedinica ima valutu i ta se valuta upotrebljava za izvješćivanje o procijenjenim i stvarnim troškovima nastalim tijekom izvršenja projekta. |
| Cjenik proizvoda | Kartica **Sažetak** | Ovaj se cjenik upotrebljava za zadavanje cijena na redcima ugovora koji se temelje na proizvodu. Popis padajućih mogućnosti za ovo polje prikazuje popis cjenika na kojima se valuta cjenika podudara s valutom ugovora. Kada je iz prilike stvori ugovor, ovo se polje kopira iz odgovarajućeg polja u zapisu ponude. Ovo polje na ugovoru o projektu zadano je iz zapisa računa, ali se može promijeniti. | Za to polje. nema nizvodne relevantnosti. |
| Valuta | Kartica **Sažetak** | Valuta koja se upotrebljava za izvješćivanje o vrijednosti ovog posla i valuta u kojoj će se klijentu fakturirati. Kada je iz prilike stvori ugovor, ovo se polje kopira iz odgovarajućeg polja u zapisu ponude. Ovo polje na ugovoru o projektu zadaje se iz zapisa računa, ali se može promijeniti. | Nakon spremanja ugovora, ovo se polje više ne može uređivati. To se polje upotrebljava za zadavanje cjenika proizvoda i projekta u ugovoru. Valuta na ugovoru upotrebljava se za podudaranje s valutom na cjeniku. |
| Ograničenje koje se ne smije prekoračiti | Kartica **Sažetak** | To polje ukazuje na ugovorenu gornju granicu konačne vrijednosti na koje je klijent pristao za ovaj posao. | Gornja se granica procjenjuje tijekom izvršenja i primjenjivo je na sve stavke i projekte povezane s ovom poslom. |
| Zatraženi datum dostave | Kartica **Sažetak** | Kada je iz ponude projekta stvori ugovor, ovo se polje kopira iz odgovarajućeg polja u ponudi projekta. | Taj datum upotrebljava se kao datum završetka za generiranje rasporeda računa. |

Sljedeći su KPI-jevi dostupni na kartici **Izvršenje ugovora** ugovora o projektu.

| Polje | Lokacija | Opis |
| --- | --- | --- |
| Vrijednost ugovora | Ukupni ugovor | Ukupna vrijednost ugovora o projektu. |
| Naplaćeni iznos | Ukupni ugovor | Zbroj iznosa na svim računima prema ovom ugovoru. |
| Nastao trošak | Ukupni ugovor | Zbroj svih stvarnih troškova evidentiranih na svim projektima koji su mapirani u ugovor. |
| Bruto marža | Ukupni ugovor | Naplaćeni iznos – Trošak nastao do datuma / Naplaćeni iznos |
| Očekivana marža | Ukupni ugovor | (Vrijednost ugovora – Procijenjeni troškovi) / Vrijednosno procijenjeni troškovi ugovora = Zbroj svih procijenjenih troškova na svim projektima mapiranim u ugovor.|
| Vrijednost ugovora | Redci utemeljeni na projektu | Vrijednost retka ugovora. |
| Naplaćeni iznos | Redci utemeljeni na projektu | Za redak ugovora s fiksnom cijenom: Zbroj iznosa na svim naplaćenim stvarnim podacima kontrolnih točaka prodaje u odnosu na ovaj redak ugovora na raznim računima stvorenim za ovaj ugovor. Za redak ugovora za vrijeme i materijal: Zbroj iznosa na svim naplativim obračunanim stvarnim podacima prodaje u odnosu na ovaj redak ugovora na raznim računima stvorenim za ovaj ugovor. |
| Nastao trošak | Redci utemeljeni na projektu | Zbroj svih stvarnih troškova evidentiranih na svim projektima mapiranim u redak ugovora. |
| Bruto marža | Redci utemeljeni na projektu | (Naplaćeni iznos – Trošak nastao do datuma) / Naplaćeni iznos |
| Očekivana marža | Redci utemeljeni na projektu | (Iznos retka ugovora u osnovnoj valuti – Procijenjeni troškovi za redak ugovora u osnovnoj valuti) / Iznos retka ugovora u osnovnoj valuti |
| Nastao trošak | Pojedinosti retka koji se temelji na projektu | Vrijeme: Zbroj iznosa stvarnih troškovima vremena evidentiranih za ovu ulogu na projektu mapiranom u redak ugovora. Troškovi: Zbroj iznosa svih stvarnih troškova vremena evidentiranih za ovu kategoriju na projektu mapiranom u redak ugovora. |
| Prijavljena količina | Pojedinosti retka koji se temelji na projektu | Vrijeme: Ukupna količina vremena na stvarnim troškovima vremena evidentiranim za ulogu na projektu koja je mapirana u taj redak ugovora. Troškovi: Sve količine stvarnih troškova za tu kategoriju troškova na projektu koje su mapirane u taj redak ugovora. |
| Naplaćeni iznos | Pojedinosti retka koji se temelji na projektu | Za redak ugovora s fiksnom cijenom ovo polje ostaje prazno na razini pojedinosti i prikazuje se samo na razini retka ugovora. Za redak ugovora s vremenom i materijalom izračuni se dovršavaju na razini pojedinosti. Pojedinosti prikazuju zbroj iznosa na svim naplaćenim redcima prihoda u odnosu na ovaj redak ugovora koji je naplativ. |
| Naplaćena količina | Pojedinosti retka koji se temelji na projektu | Za redak ugovora s fiksnom cijenom ovo polje ostaje prazno na razini pojedinosti i prikazuje se samo na razini retka ugovora. Za redak ugovora s vremenom i materijalom izračuni se dovršavaju na razini pojedinosti za vrijeme i troškove. Vrijeme: Zbroj sati na svim naplaćenim redcima prihoda za tu ulogu u odnosu na ovaj redak ugovora koji je naplativ. Troškovi: Sve količine stvarnih troškova za tu kategoriju troškova na projektu koje su mapirane u taj redak ugovora. |
| Vrijednost ugovora | Redci utemeljeni na proizvodu | Vrijednost retka ugovora ovog retka ugovora koji se temelji na proizvodu. |
| Naplaćeni iznos | Redci utemeljeni na proizvodu | Zbroj iznosa na svim redcima fakture u odnosu na ovaj redak ugovora koji se temelji na proizvodu na različitim fakturama koje su stvorene za ovaj ugovor. |
| Nastao trošak | Redci utemeljeni na proizvodu | Zbroj svih stvarnih troškova evidentiranih za redak ugovora koji se temelji na proizvodu. |
| Bruto marža | Redci utemeljeni na projektu | Naplaćeni iznos – Trošak nastao do datuma / Naplaćeni iznos |
| Očekivana marža | Redci utemeljeni na proizvodu | (Vrijednost retka ugovora – Procijenjeni troškovi za redak ugovora) / Vrijednost retka ugovora |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
