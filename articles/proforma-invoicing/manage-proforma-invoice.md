---
title: Upravljanje predračunom koji se temelji na projektu
description: U ovom se članku navode informacije o načinu upravljanja predračunima koji se temelje na projektu i radu s njima.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 31822947a4fbb60218ce1c3c9415a60491f6d8fa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932103"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Upravljanje predračunom koji se temelji na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U aplikaciji Dynamics 365 Project Operations predračuni se izrađuju kao proširenje faktura u aplikaciji Dynamics 365 Sales. Međutim, kada je u pitanju fakturiranje, postoje mnoge razlike u postupku fakturiranja između aplikacija prodaje i Project Operations. Na primjer, nije moguće stvoriti novu fakturu sa stranice **Popis faktura** u aplikaciji Project Operations, ali je to moguće učiniti u aplikaciji Prodaja. Te razlike i proširenja postoje za podršku postupcima fakturiranja projekata koji se razlikuju od uobičajene fakture za prodajni nalog.

> [!IMPORTANT]
> Zbog tih razlika nemojte naizmjenično upotrebljavati fakture u aplikacijama Prodaja i Project Operations.

## <a name="invoice-header"></a>Zaglavlje fakture

Na zaglavlju predračuna u aplikaciji Project Operations dostupni su sljedeći podaci.

| Polje | Lokacija | Opis |
| --- | --- | --- | 
| **ID fakture** | Kartica **Sažetak** | ID koji se automatski generira tijekom stvaranja predračuna. Polje samo za čitanje koje je zaključano za uređivanje. Ovo se polje koristi kao referenca za svaki predračun. |
| **Ime** | Kartica **Sažetak** | Prema zadanim postavkama postavite na naziv ugovora o projektu. Ovo se polje kasnije može urediti. | 
| **Valuta** | Kartica **Sažetak** | Prema zadanim postavkama postavite na valutu ugovora o projektu. Polje samo za čitanje koje je zaključano za uređivanje. |
| **Cjenik** | Kartica **Sažetak** | Prema zadanim postavkama postavite na cjenik za ugovor o projektu. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Prilika** | Kartica **Sažetak** | Referenca na povezanu priliku. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Ugovor** | Kartica **Sažetak** | Referenca na povezani ugovor o projektu. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Klijent** | Kartica **Sažetak** | Referenca na povezani ugovor o projektu. Polje samo za čitanje koje je zaključano za uređivanje. |
| **Opis** | Kartica **Sažetak** | Tekstno polje u kojem se opisuje faktura. Ovo se polje kasnije može urediti. | 
| **Naplati od** i povezana polja | **Kartica sažetka** | Zadane vrijednosti postavlja klijent ugovora o projektu. Ovo se polje kasnije može urediti.  | 
| **Stanje** | Kartica **Sažetak** | Postavlja sljedeće mogućnosti: **Aktivno**, **Zatvoreno**, **Plaćeno** i **Otkazano**, a može se uređivati. Statusi koji nisu podržani za aplikaciju Project Operations uključuju **Zatvoreno** i **Otkazano**. </br> Status je postavljen na **Aktivno** kada se stvara račun. </br>Status bi trebao biti postavljen na **Plaćeno** tek nakon potvrde računa.  | 
| **Status fakture projekta** | Kartica **Sažetak** | Postavlja sljedeće mogućnosti: **Skica**, **Na pregledu** i **Potvrđeno**, a može se uređivati. U oba statusa, **Skica** i **Na pregledu**, faktura se može uređivati. Faktura se ne može uređivati nakon što se potvrdi. | 
| **Detaljni iznos** | Kartica **Sažetak** | Zbroj iznosa na svim redcima računa nakon predujama i odbitka. Polje samo za čitanje koje je zaključano za uređivanje.  Ovo se polje upotrebljava za izračun konačnog iznosa. | 
| **Popust (%)** | Kartica **Sažetak** | Ovo polje možete urediti za unos postotak popusta. Funkcija aplikacije Project Operations ne podržava ovo polje. Ovo polje nije podržano.|  
| **Iznos popusta** | Kartica **Sažetak** | Ovo polje možete urediti za unos iznosa popusta. Funkcija aplikacije Project Operations ne podržava ovo polje. Ovo polje nije podržano. |  
| **Iznos prije vozarine** | **Kartica sažetka** | Ukupni iznos fakture nakon primjene popusta. Polje samo za čitanje koje je zaključano za uređivanje. Ovo se polje upotrebljava za izračun konačnog iznosa.  | 
| **Iznos vozarine** | Kartica **Sažetak** | Ovo se polje može urediti za unos iznosa vozarine. Funkcija aplikacije Project Operations ne podržava ovo polje. Ovo polje nije podržano. |
| **Ukupni porez** | Kartica **Sažetak** | Ukupni porez iz svih redaka fakture. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Ukupni iznos** | Kartica **Sažetak** | Zbroj iznosa nakon popusta i poreza. Iznos je iznos koji klijent treba platiti. | 

## <a name="project-based-invoice-lines"></a>Redci fakture koji se temelje na projektu

U aplikaciji Project Operations uvijek postoji jedan redak fakture za svaki redak ugovora o projektu. Redak fakture stvara se čak i ako nema stvarnih podataka. U retku predračuna dostupni su sljedeći podaci.

| Polje | Lokacija | Opis | 
| --- | --- | --- |
| **ID fakture** | Kartica **Općenito** | Referenca na ID fakture. Polje samo za čitanje koje je zaključano za uređivanje. Veza na ID računa može se upotrijebiti za povratak na zaglavlje računa. | 
| **Ime** | Kartica **Općenito** | Naziv retka fakture koji je prema zadanim postavkama postavljen iz naziva retka ugovora. Ovo se polje kasnije može urediti. |
| **Project** | Kartica **Općenito** | Projekt na povezanom retku ugovora o projektu. Polje samo za čitanje koje je zaključano za uređivanje. Veza projekta može se upotrebljavati za navigaciju do projekta. | 
| **Način naplate** | Kartica **Općenito** | Način naplate na povezanom retku ugovora o projektu. Polje samo za čitanje koje je zaključano za uređivanje. |
| **Iznos retka ugovora** | Kartica **Općenito** | Ugovoreni iznos u povezanom retku ugovora o projektu. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Fakturirano do datuma** | Kartica **Općenito** | Zbroj iznosa na svim pojedinostima retka fakture ove fakture. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Iznos** | Kartica **Općenito** | Zbroj iznosa na svim naplativim pojedinostima retka fakture ove fakture. Polje samo za čitanje koje je zaključano za uređivanje. Ovo se polje upotrebljava za izračun konačnog iznosa na zaglavlju fakture. | 
| **Porez** | Kartica **Općenito** | Zbroj iznosa poreza na svim pojedinostima retka fakture ovog retka fakture. Polje samo za čitanje koje je zaključano za uređivanje. Ovo se polje upotrebljava za izračun konačnog iznosa poreza na zaglavlju fakture. | 
| **Prošireni iznos** | Kartica **Općenito** | Zbroj ukupnog iznosa (**Porez + Iznosi**) na svim naplativim pojedinostima retka fakture ovog retka fakture. Polje samo za čitanje koje je zaključano za uređivanje. Ovo se polje upotrebljava za izračun konačnog iznosa na zaglavlju fakture. |

## <a name="invoice-line-details"></a>Pojedinosti retka fakture

Svaki redak fakture u fakturi za projekt sadrži pojedinosti retka fakture. Te se pojedinosti retka odnose na nenaplaćene stvarne prodaje i kontrolne točke koje se odnose na redak ugovora na koji se poziva redak fakture. Sve ove transakcije označene su kao **Spremno za fakturiranje**.

Za redak **Faktura za vrijeme i materijal**, pojedinosti retka fakture grupirani su u stavke **Naplativo**, **Nenaplativo** i **Besplatno** na stranici **Redak fakture**. Pojedinosti **Naplativog retka fakture** dodaju se u ukupnom zbroju retka fakture. **Besplatno** i **Nenaplativi stvarni podaci** ne dodaju se ukupnom zbroju retka fakture.

Za redak **Faktura s fiksnom cijenom**, pojedinosti retka fakture stvaraju se iz kontrolnih točki koje su označene kao **Spremno za fakturiranje** na povezanom retku ugovora. Nakon što se iz kontrolne točke stvori pojedinost retka fakture, status naplate na kontrolnoj točki ažurira se na **Faktura za klijenta stvorena**.

### <a name="edit-invoice-line-details"></a>Uređivanje pojedinosti retka fakture

Sljedeća su polja dostupna na pojedinostima retka fakture iza kojih stoji nefakturirana stvarna prodaja.

| Polje | Opis |
| --- | --- | 
| **Redak fakture** | Referenca na **ID retka fakture**. Ovo je polje samo za čitanje i zaključano je za uređivanje. Ova veza može se upotrijebiti za povratak na zaglavlje računa. | 
| **Opis** | Opis pojedinosti retka fakture. Postavljeno prema zadanim postavkama iz polja **Interni komentari** na **Unos vremena** i iz polja **Opis** na **Unos troška**. Polje kasnije može urediti.| 
| **Vanjski opis** | Opis pojedinosti retka fakture. Postavljeno prema zadanim postavkama iz polja **Vanjski komentari** na **Unos vremena** i polja **Opis** na **Unos troška**. Polje kasnije može urediti. Ovim se opisom može odrediti što treba biti na ispisanom računu koji će se poslati klijentu. U aplikaciji Project Operations predračun nema svu potrebnu funkcionalnost za konfiguriranje postavki ispisa fakture. | 
| **Datum početka** | Ovo je polje samo za čitanje koje je postavljeno prema zadanim postavkama iz stvarnog izvora. |
| **Project** | Ovo je polje samo za čitanje koje je prema zadanim postavkama postavljeno iz stvarnog izvora u projekt na povezani redak ugovora. |  
| **Zadatak** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. |
| **Kategorija transakcije** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Uloga** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. |  
| **Resurs koji je moguće rezervirati** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Tvrtka resursa** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Jedinica za resurse** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Količina** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. |  
| **Raspored jedinica** | Za pojedinosti retka fakture za vrijeme ovo je uvijek postavljeno na vrijeme i ne može se uređivati. Prema zadanim postavkama ovo je za troškove postavljeno iz stvarnog izvora troška. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Jedinica** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. |  
| **Cijena** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. |
| **Valuta** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Iznos** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Porez** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje kasnije može urediti.| 
| **Prošireni iznos** | Izračunano polje, izračunano kao **Iznos + porez**. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Vrsta naplate** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje kasnije može urediti. Odabirom mogućnosti **Naplativo** dodaje se redak ukupnom zbroju redaka fakture. **Besplatno** i **Nenaplativo** isključit će ga iz ukupnog zbroja redaka fakture.| 
| **Odabir proizvoda** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. |
| **Proizvod** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Naziv proizvoda** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. |  
| **Opis umetnute stavke** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. |
| **Vrsta transakcije** | Ovo je polje samo za čitanje koje je postavljeno prema zadanim postavkama iz stvarnog izvora u **Naplaćena prodaja**. |  
| **Razred transakcije** | Postavljeno prema zadanim postavkama iz stvarnog izvora. Polje samo za čitanje koje je zaključano za uređivanje. | 

Sljedeća su polja dostupna na pojedinosti retka fakture iza koje stoji kontrolna točka.

| Polje | Opis |
| --- | --- | 
| **Redak fakture** | Referenca na **ID retka fakture**. Polje samo za čitanje koje je zaključano za uređivanje. Veza se može upotrijebiti za povratak na zaglavlje računa.  | 
| **Opis** | Opis pojedinosti retka fakture. Prema zadanim postavkama postavljeno iz opisa kontrolne točke izvora. | 
|**Vanjski opis** | Opis pojedinosti retka fakture koji je zadan iz opisa kontrolne točke izvora. Ovo polje može se upotrijebiti za određivanje onoga što treba biti na ispisanom računu koji će se poslati klijentu. Predračun u aplikaciji Project Operations nema svu potrebnu funkcionalnost za konfiguriranje postavki ispisa fakture. | 
| **Datum početka** | Postavljeno prema zadanim postavkama iz datuma **Kontrolne točke** na izvoru kontrolne točke. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Project** | Prema zadanim postavkama postavljeno iz kontrolne točke. Polje samo za čitanje koje je zaključano za uređivanje. |
| **Zadatak** | Prema zadanim postavkama postavljeno iz kontrolne točke. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Kategorija transakcije** | Polje samo za čitanje koje je zaključano za uređivanje. |
| **Uloga** | Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Resurs koji je moguće rezervirati** | Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Jedinica za resurse** | Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Raspored jedinica** | Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Jedinica** | Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Cijena** | Prema zadanim postavkama postavljeno iz iznosa na kontrolnoj točki izvora. Polje samo za čitanje koje je zaključano za uređivanje. |
| **Valuta** | Prema zadanim postavkama postavljeno iz kontrolne točke. Polje samo za čitanje koje je zaključano za uređivanje. |
| **Iznos** | Prema zadanim postavkama postavljeno iz iznosa na kontrolnoj točki izvora. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Porez** | Prema zadanim postavkama postavljeno iz iznosa poreza na kontrolnoj točki izvora. Polje samo za čitanje koje je zaključano za uređivanje. |
| **Prošireni iznos** | Prema zadanim postavkama postavljeno iz dodatnog iznosa na kontrolnoj točki izvora. Polje kasnije može urediti. | 
| **Vrsta naplate** | Prema zadanim postavkama uvijek je postavljeno na **Naplativo**. Polje samo za čitanje koje je zaključano za uređivanje. |
| **Vrsta transakcije** | Prema zadanim postavkama postavljeno iz kontrolne točke. Polje samo za čitanje koje je zaključano za uređivanje. | 
| **Razred transakcije** | Prema zadanim postavkama postavljeno iz kontrolne točke. Polje samo za čitanje koje je zaključano za uređivanje. | 

## <a name="refresh-invoice-transactions"></a>Osvježavanje transakcija fakture

Ako imate stvarne podatke koje ste dobili nakon stvaranja fakture, možete ih uključiti u fakturu.

1. U **Prikazu zaostale naplate** označe podatke kao **Spremno za fakturiranje**.   
2. Otvorite skicu predračuna i na vrpci **Radnje** odaberite **Osvježi transakcije u retku fakture**.

  Pojedinosti retka fakture stvaraju se za sve stvarne podatke s prošlim datumima koji su označeni kao **Spremno za fakturiranje**, ali nisu obuhvaćeni fakturom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
