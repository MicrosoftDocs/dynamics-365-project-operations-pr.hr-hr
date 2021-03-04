---
title: Stvaranje rasporeda faktura na retku ugovora koji se temelji na projektu – jednostavno
description: U ovoj temi nalaze se informacije o stvaranju rasporeda faktura i kontrolnih točaka.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 728a35b2b69fb63a2b20f218c250365c5068370f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180318"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Stvaranje rasporeda faktura na retku ugovora koji se temelji na projektu – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Možete priložiti raspored faktura retku ugovora koji se temelji na projektu. Fakturiranje je dopušteno samo nakon što se dobije ugovor za stvaranje ugovora o projektu. Rasporedi faktura omogućuju automatsko stvaranje nacrta faktura za redak ugovora koji se temelji na projektu. Ako planirate uvijek stvarati račune ručno, možete preskočiti stvaranje rasporeda računa na retku ugovora koji se temelji na projektu ili na retku ugovora.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Stvaranje rasporeda faktura za vrijeme i materijal za redak ugovora koji se temelji na projektu

Kada je način naplate retka ugovora koji se temelji na projektu vrijeme i materijal, možete stvoriti raspored računa na temelju datuma. Kako biste automatski generirali raspored računa na temelju datuma, poduzmite sljedeće korake.

1. Idite na **Postavke** > **Učestalosti faktura** kako biste postavili učestalost faktura.
2. Otvorite ugovor o projektu i na kartici **Sažetak** postavite traženi datum isporuke.
3. Otvorite redak ugovora o vremenu i materijalu za koji želite stvoriti datumski raspored faktura. 
4. Na kartici **Raspored faktura** odaberite datum početka naplate i učestalost faktura. 
5. Na podrešetki odaberite **Generiraj raspored faktura**.

    Sustav generira raspored faktura sa sljedećim podacima o polju:

    - **Datum pokretanja fakture** postavljen je na datum na temelju učestalosti faktura.
    - **Datum završetka transakcije** postavljen je na dan prije **Datuma pokretanja fakture**.
    - **Status pokretanja** automatski se postavlja na **Ne pokreći**. Kada se posao automatskog stvaranja fakture odvija za određeni **Datum pokretanja fakture**, to će se polje ažurirati na **Uspješno pokretanje** ili **Neuspješno pokretanje**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Stvaranje rasporeda faktura s fiksnom cijenom za redak ugovora koji se temelji na projektu

Kada redak ugovora koji se temelji na projektu ima način naplate s fiksnom cijenom, možete stvoriti raspored faktura zasnovan na kontrolnoj točki. Dovršite sljedeće korake za automatsko generiranje rasporeda faktura koje se temelje na kontrolnoj točki za fiksni skup kontrolnih točaka koje se podjednako raspoređuju za kalendarsko razdoblje.

1. Idite na **Postavke** > **Učestalosti faktura** kako biste postavili učestalost faktura.
2. Otvorite ugovor o projektu i na kartici **Sažetak** postavite traženi datum isporuke.
3. Otvorite redak ugovora s fiksnom cijenom na kojem trebate stvoriti raspored kontrolnih točaka. 
4. Na kartici **Raspored faktura (kontrolne točke naplate)** odaberite datum početka naplate i učestalost faktura. 
5. Na podrešetki odaberite **Generiraj povremene kontrolne točke**.

    Sustav generira raspored faktura sa sljedećim podacima o kontrolnoj točki.

    - **Naziv kontrolne točke** postavljen je na datum koji se određuje na temelju učestalosti faktura.
    - **Datum kontrolne točke** postavljen je na datum koji se određuje na temelju učestalosti faktura.
    - **Iznos kontrolne točke** izračunava se dijeljenjem iznosa ugovora na retku ugovora koji se temelji na projektu s brojem kontrolnih točaka kako ih određuje učestalost, početak naplate i traženi datumi isporuke.
    - Ako redak ugovora ima vrijednost u polju **Procijenjeni iznos poreza**, to se polje pri generiranju periodičnih kontrolnih točaka također raspoređuje na svaku kontrolnu točku podjednako.

Kontrolne točke za naplatu trebale bi biti jednake ugovorenoj vrijednosti retka ugovora koji se temelji na projektu. Ako nisu jednaki, dolazi do pogreške. Tu pogrešku možete popraviti tako da provjerite čini li ukupni iznos naplate kontrolnih točaka ugovorenu vrijednost retka bilo stvaranjem, uređivanjem ili brisanjem kontrolnih točaka. Nakon izvršenih promjena osvježite stranicu.

### <a name="manually-create-milestones"></a>Ručno stvaranje kontrolnih točaka

Kontrolne točke s fiksnom cijenom mogu se generirati ručno kada se povremeno ne dijele. Kako biste ručno stvorili kontrolnu točku, poduzmite sljedeće korake.

1. Otvorite redak ugovora s fiksnom cijenom na kojem želite stvoriti kontrolnu točku. 
2. Na kartici **Raspored faktura** na podrešetki, odaberite **+ Stvori novu kontrolnu točku retka ugovora**.
3. Na obrascu **Stvaranje kontrolne točke** unesite tražene podatke na temelju sljedeće tablice. 

| Polje | Lokacija | Opis | Utjecaj na niže razine |
| --- | --- | --- | --- |
| Naziv kontrolne točke | Brzo stvaranje | Tekstno polje za naziv kontrolne točke. | Ovo je polje uključeno u kontrolnu točku retka ugovora o projektu i fakture. |
| Zadatak projekta | Brzo stvaranje | Ako je kontrolna točka vezana uz projektni zadatak, upotrijebite ovu referencu za dodavanje prilagođene logike i postavljanje statusa kontrolne točke na temelju statusa zadatka. | Ne postoji nizvodni utjecaj ove reference na zadatak. |
| Datum kontrolne točke | Brzo stvaranje | Datum kada bi postupak automatskog stvaranja fakture trebao tražiti status ove kontrolne točke kako bi je uzeo u obzir za fakturiranje. | Ovo je uključeno u kontrolnu točku retka ugovora o projektu i fakture. |
| Status fakture | Brzo stvaranje | Kada se stvori kontrolna točka, taj se status uvijek postavi na **Nije spremno za fakturiranje** ili **Nije započeto**. | Ovo je uključeno u kontrolnu točku retka ugovora o projektu i fakture. |
| Iznos retka | Brzo stvaranje | Iznos ili vrijednost kontrolne točke koja će se fakturirati klijentu. | Ovo je polje uključeno u kontrolnu točku retka ugovora o projektu i fakture, |
| Porez | Brzo stvaranje | Iznos poreza primijenjen na kontrolnu točku. | Ovo je uključeno u kontrolnu točku retka ugovora o projektu i fakture. |

4. Odaberite **Spremi i zatvori**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]