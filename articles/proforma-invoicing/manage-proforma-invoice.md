---
title: Upravljanje predračunom
description: u ovoj temi nalaze se informacije o načinu upravljanja predračunima i radu s njima.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29e301062f8f3ba955a95953bc2e891f3acaf765
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287679"
---
# <a name="manage-a-proforma-invoice"></a>Upravljanje predračunom

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U aplikaciji Dynamics 365 Project Operations predračuni se izrađuju kao proširenje faktura u aplikaciji Dynamics 365 Sales. Međutim, kada je u pitanju fakturiranje, postoje mnoge razlike u postupku fakturiranja između aplikacija prodaje i Project Operations. Na primjer, nije moguće stvoriti novu fakturu sa stranice **Popis faktura** u aplikaciji Project Operations, ali je to moguće učiniti u aplikaciji Prodaja. Te razlike i proširenja postoje za podršku postupcima fakturiranja projekata koji se razlikuju od uobičajene fakture za prodajni nalog.

> [!IMPORTANT]
> Zbog tih razlika nemojte naizmjenično upotrebljavati fakture u aplikacijama Prodaja i Project Operations.

## <a name="invoice-header"></a>Zaglavlje fakture

Na zaglavlju predračuna u aplikaciji Project Operations dostupni su sljedeći podaci.

| Polje | Lokacija | Opis | Utjecaj na niže razine |
| --- | --- | --- | --- |
| **ID fakture** | Kartica **Sažetak** | ID koji se automatski generira tijekom stvaranja predračuna. Polje samo za čitanje koje je zaključano za uređivanje. | Ovo se polje koristi kao referenca za svaki predračun. |
| **Ime** | Kartica **Sažetak** | Prema zadanim postavkama postavite na naziv ugovora o projektu. Ovo polje korisnik može uređivati. | &nbsp;  |
| **Valuta** | Kartica **Sažetak** | Prema zadanim postavkama postavite na valutu ugovora o projektu. Polje samo za čitanje koje je zaključano za uređivanje. |&nbsp; |
| **Cjenik** | Kartica **Sažetak** | Prema zadanim postavkama postavite na cjenik za ugovor o projektu. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Prilika** | Kartica **Sažetak** | Referenca na povezanu priliku. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp;  |
| **Ugovor** | Kartica **Sažetak** | Referenca na povezani ugovor o projektu. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Klijent** | Kartica **Sažetak** | Referenca na povezani ugovor o projektu. Polje samo za čitanje koje je zaključano za uređivanje. |&nbsp;  |
| **Opis** | Kartica **Sažetak** | Tekstno polje u kojem se opisuje faktura. Ovo polje korisnik može uređivati. | &nbsp; |
| **Naplati od** i povezana polja | **Kartica sažetka** | Zadane vrijednosti postavlja klijent ugovora o projektu. Ovo polje korisnik može uređivati.  | &nbsp; |
| **Status** | Kartica **Sažetak** | Postavlja sljedeće mogućnosti: **Aktivno**, **Zatvoreno**, **Plaćeno** i **Otkazano**, a korisnik ih može uređivati. | Statusi koji nisu podržani za aplikaciju Project Operations uključuju **Zatvoreno** i **Otkazano**. </br> Status je postavljen na **Aktivno** kada se stvara račun. </br>Status bi trebao biti postavljen na **Plaćeno** tek nakon potvrde računa. |
| **Status fakture projekta** | Kartica **Sažetak** | Postavlja sljedeće mogućnosti: **Skica**, **Na pregledu** i **Potvrđeno**, a korisnik to može uređivati. | U oba statusa, **Skica** i **Na pregledu**, faktura se može uređivati. Faktura se ne može uređivati nakon što se potvrdi. |
| **Detaljni iznos** | Kartica **Sažetak** | Zbroj iznosa na svim redcima računa nakon predujama i odbitka. Polje samo za čitanje koje je zaključano za uređivanje. | Ovo se polje upotrebljava za izračun konačnog iznosa. |
| **Popust (%)** | Kartica **Sažetak** | Ovo polje možete urediti za unos postotak popusta. Funkcija aplikacije Project Operations ne podržava ovo polje. | Ovo polje nije podržano. |
| **Iznos popusta** | Kartica **Sažetak** | Ovo polje možete urediti za unos iznosa popusta. Funkcija aplikacije Project Operations ne podržava ovo polje. | Ovo polje nije podržano. |
| **Iznos prije vozarine** | **Kartica sažetka** | Ukupni iznos fakture nakon primjene popusta. Polje samo za čitanje koje je zaključano za uređivanje. | Ovo se polje upotrebljava za izračun konačnog iznosa. |
| **Iznos vozarine** | Kartica **Sažetak** | Ovo se polje može urediti za unos iznosa vozarine. Funkcija aplikacije Project Operations ne podržava ovo polje. | Ovo polje nije podržano. |
| **Ukupni porez** | Kartica **Sažetak** | Ukupni porez iz svih redaka fakture. Polje samo za čitanje koje je zaključano za uređivanje. | Nijedna. |
| **Ukupni iznos** | Kartica **Sažetak** | Zbroj iznosa nakon popusta i poreza. | Iznos je iznos koji klijent treba platiti. |

## <a name="project-based-invoice-lines"></a>Redci fakture koji se temelje na projektu

U aplikaciji Project Operations uvijek postoji jedan redak fakture za svaki redak ugovora o projektu. Redak fakture stvara se čak i ako nema stvarnih podataka. U retku predračuna dostupni su sljedeći podaci.

| Polje | Lokacija | Opis | Utjecaj na niže razine |
| --- | --- | --- | --- |
| **ID fakture** | Kartica **Općenito** | Referenca na ID fakture. Polje samo za čitanje koje je zaključano za uređivanje. | Veza na ID računa može se upotrijebiti za povratak na zaglavlje računa. |
| **Ime** | Kartica **Općenito** | Naziv retka fakture koji je prema zadanim postavkama postavljen iz naziva retka ugovora. Ovo polje korisnik može uređivati. | &nbsp; |
| **Project** | Kartica **Općenito** | Projekt na povezanom retku ugovora o projektu. Polje samo za čitanje koje je zaključano za uređivanje. | Veza projekta može se upotrebljavati za navigaciju do projekta. |
| **Način naplate** | Kartica **Općenito** | Način naplate na povezanom retku ugovora o projektu. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Iznos retka ugovora** | Kartica **Općenito** | Ugovoreni iznos u povezanom retku ugovora o projektu. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Fakturirano do datuma** | Kartica **Općenito** | Zbroj iznosa na svim pojedinostima retka fakture ove fakture. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Iznos** | Kartica **Općenito** | Zbroj iznosa na svim naplativim pojedinostima retka fakture ove fakture. Polje samo za čitanje koje je zaključano za uređivanje. | Ovo se polje upotrebljava za izračun konačnog iznosa na zaglavlju fakture. |
| **Porez** | Kartica **Općenito** | Zbroj iznosa poreza na svim pojedinostima retka fakture ovog retka fakture. Polje samo za čitanje koje je zaključano za uređivanje. | Ovo se polje upotrebljava za izračun konačnog iznosa poreza na zaglavlju fakture. |
| **Prošireni iznos** | Kartica **Općenito** | Zbroj ukupnog iznosa (**Porez + Iznosi**) na svim naplativim pojedinostima retka fakture ovog retka fakture. Polje samo za čitanje koje je zaključano za uređivanje. | Ovo se polje upotrebljava za izračun konačnog iznosa na zaglavlju fakture. |

## <a name="invoice-line-details"></a>Pojedinosti retka fakture

Svaki redak fakture u fakturi za projekt sadrži pojedinosti retka fakture. Te se pojedinosti retka odnose na nenaplaćene stvarne prodaje i kontrolne točke koje se odnose na redak ugovora na koji se poziva redak fakture. Sve ove transakcije označene su kao **Spremno za fakturiranje**.

Za redak **Faktura za vrijeme i materijal**, pojedinosti retka fakture grupirani su u **Naplativo**, **Nenaplativo** i **Besplatno** na stranici **Redak fakture**. Pojedinosti **Naplativog retka fakture** dodaju se u ukupnom zbroju retka fakture. **Besplatno** i **Nenaplativi stvarni podaci** ne dodaju se ukupnom zbroju retka fakture.

Za redak **Faktura s fiksnom cijenom**, pojedinosti retka fakture stvaraju se iz kontrolnih točaka koje su na povezanom retku ugovora označene kao **Spremno za fakturiranje**. Nakon što se iz kontrolne točke stvori pojedinost retka fakture, status naplate na kontrolnoj točki ažurira se na **Faktura za klijenta stvorena**.

### <a name="edit-invoice-line-details"></a>Uređivanje pojedinosti retka fakture

Sljedeća su polja dostupna na pojedinostima retka fakture iza kojih stoji nefakturirana stvarna prodaja.

| Polje | Opis | Utjecaj na niže razine |
| --- | --- | --- |
| **Redak fakture** | Referenca na **ID retka fakture**. Polje samo za čitanje zaključano je za uređivanje. | Ova veza može se upotrijebiti za povratak na zaglavlje računa. |
| **Opis** | Opis pojedinosti retka fakture. Postavljeno prema zadanim postavkama iz polja **Interni komentari** na **Unos vremena** i iz polja **Opis** na **Unos troška**. Polje korisnik može uređivati.| &nbsp; |
| **Vanjski opis** | Opis pojedinosti retka fakture. Postavljeno prema zadanim postavkama iz polja **Vanjski komentari** na **Unos vremena** i polja **Opis** na **Unos troška**. Polje korisnik može uređivati. | Ovim se opisom može odrediti što treba biti na ispisanom računu koji će se poslati klijentu. U aplikaciji Project Operations predračun nema svu potrebnu funkcionalnost za konfiguriranje postavki ispisa fakture. |
| **Datum početka** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | Ovo se polje može uređivati na novoj pojedinosti retka fakture iza kojeg ne stoji stvarni izvor. |
| **Project** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | Prema zadanim postavkama za projekt na povezanom retku ugovora. |
| **Zadatak** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | Polje se može uređivati na novoj pojedinosti retka fakture iza kojeg ne stoji stvarni izvor. Padajući popis prikazuje sve zadatke pridružene povezanom retku ugovora o projektu.  |
| **Kategorija transakcije** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | Polje se može uređivati na novoj pojedinosti retka fakture iza kojeg ne stoji stvarni izvor. |
| **Uloga** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | Polje se može uređivati na novoj pojedinosti retka fakture iza kojeg ne stoji stvarni izvor. |
| **Resurs koji je moguće rezervirati** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | Polje se može uređivati na novoj pojedinosti retka fakture iza kojeg ne stoji stvarni izvor. |
| **Tvrtka resursa** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | Polje se može uređivati na novoj pojedinosti retka fakture iza kojeg ne stoji stvarni izvor. |
| **Jedinica za resurse** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | Polje se može uređivati na novoj pojedinosti retka fakture iza kojeg ne stoji stvarni izvor. |
| **Količina** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | Polje se može uređivati na novoj pojedinosti retka fakture iza kojeg ne stoji stvarni izvor. |
| **Raspored jedinica** | Za pojedinosti retka fakture za vrijeme ovo je uvijek postavljeno na vrijeme i ne može se uređivati. Prema zadanim postavkama ovo je za troškove postavljeno iz stvarnog izvora troška. Polje samo za čitanje koje je zaključano za uređivanje. | Prema zadanim postavkama postavljeno na **Vrijeme** na novoj pojedinosti retka fakture iza koje ne stoji stvarni podatak. |
| **Jedinica** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | Polje se može uređivati na novoj pojedinosti retka fakture iza kojeg ne stoji stvarni izvor |
| **Cijena** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | Polje se može uređivati na novoj pojedinosti retka fakture iza kojeg ne stoji stvarni izvor. Ako se ne unese vrijednost, ona se prema zadanim postavkama postavlja nakon **Spremanja**. |
| **Valuta** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | Prema zadanim postavkama postavlja se iz zaglavlja fakture pri stvaranju nove pojedinosti fakture iza koje ne stoje stvarni podaci.  Polje samo za čitanje koje je zaključano za uređivanje. |
| **Iznos** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | Izračunano kao **Količina \* Cijena** tijekom izrade nove pojedinosti fakture iza koje ne stoji stvarni podatak. Izračunava se nakon **Spremanja**. Polje samo za čitanje koje je zaključano za uređivanje. |
| **Porez** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje korisnik može uređivati | Korisnik može uređivati polje tijekom izrade nove pojedinosti retka fakture iza koje ne stoji stvarni podatak. |
| **Prošireni iznos** | Izračunano polje, izračunano kao **Iznos + porez**. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Vrsta naplate** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje korisnik može uređivati. | Odabirom mogućnosti **Naplativo** dodaje se redak ukupnom zbroju redaka fakture. **Besplatno** i **Nenaplativo** isključit će ga iz ukupnog zbroja redaka fakture. |
| **Vrsta transakcije** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | Prema zadanim postavkama postavljeno na **Naplaćena prodaja** i zaključano pri stvaranju nove **Pojedinosti retka fakture** iza koje ne stoji stvarni podatak.  |
| **Razred transakcije** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | Postavlja se prema zadanim postavkama na temelju odluke korisnika hoće li stvoriti pojedinost retka fakture **Vrijeme**, **Trošak** ili **Naknada**, dok istodobno stvara i novu **Pojedinost retka fakture** iza koje ne stoji stvarni podatak. Zaključano za uređivanje. |

Sljedeća su polja dostupna na pojedinosti retka fakture iza koje stoji kontrolna točka:

| Polje | Opis | Utjecaj na niže razine |
| --- | --- | --- |
| **Redak fakture** | Referenca na **ID retka fakture**. Polje samo za čitanje koje je zaključano za uređivanje. | Veza se može upotrijebiti za povratak na zaglavlje računa. |
| **Opis** | Opis pojedinosti retka fakture. Prema zadanim postavkama postavljeno iz opisa kontrolne točke izvora. | &nbsp; |
|**Vanjski opis** | Opis pojedinosti retka fakture koji je zadan iz opisa kontrolne točke izvora. | Ovo polje može se upotrijebiti za određivanje onoga što treba biti na ispisanom računu koji će se poslati klijentu. Predračun u aplikaciji Project Operations nema svu potrebnu funkcionalnost za konfiguriranje postavki ispisa fakture. |
| **Datum početka** | Postavljeno prema zadanim postavkama iz datuma **Kontrolne točke** na izvoru kontrolne točke. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Project** | Prema zadanim postavkama postavljeno iz kontrolne točke. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Zadatak** | Prema zadanim postavkama postavljeno iz kontrolne točke. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Kategorija transakcije** | Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Uloga** | Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Resurs koji je moguće rezervirati** | Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Jedinica za resurse** | Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Raspored jedinica** | Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Jedinica** | Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Cijena** | Prema zadanim postavkama postavljeno iz iznosa na kontrolnoj točki izvora. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Valuta** | Prema zadanim postavkama postavljeno iz kontrolne točke. Polje samo za čitanje koje je zaključano za uređivanje. |&nbsp; |
| **Iznos** | Prema zadanim postavkama postavljeno iz iznosa na kontrolnoj točki izvora. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Porez** | Prema zadanim postavkama postavljeno iz iznosa poreza na kontrolnoj točki izvora. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Prošireni iznos** | Prema zadanim postavkama postavljeno iz dodatnog iznosa na kontrolnoj točki izvora. Polje korisnik može uređivati | &nbsp; |
| **Vrsta naplate** | Prema zadanim postavkama uvijek je postavljeno na **Naplativo**. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Vrsta transakcije** | Prema zadanim postavkama postavljeno iz kontrolne točke. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |
| **Razred transakcije** | Prema zadanim postavkama postavljeno iz kontrolne točke. Polje samo za čitanje koje je zaključano za uređivanje. | &nbsp; |

## <a name="refresh-invoice-transactions"></a>Osvježavanje transakcija fakture

Ako imate stvarne podatke koje ste dobili nakon stvaranja fakture, možete ih uključiti u fakturu.

1. U **Prikazu zaostale naplate** označe podatke kao **Spremno za fakturiranje**.   
2. Otvorite skicu predračuna i na vrpci **Radnje** kliknite **Osvježi transakcije retka fakture**.

  Ovo stvara pojedinosti retka fakture za sve stvarne podatke koji kasne, a označeni su kao **Spremno za fakturiranje**; ali nisu uključeni u fakturu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]