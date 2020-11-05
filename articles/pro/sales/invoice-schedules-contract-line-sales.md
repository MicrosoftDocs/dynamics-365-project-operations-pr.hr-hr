---
title: Stvaranje rasporeda faktura na retku ugovora koji se temelji na projektu
description: U ovoj temi nalaze se informacije o stvaranju rasporeda faktura i kontrolnih točaka u redcima ugovora.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2183b915dd2f67e03964246cb0689003e48363f7
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4073622"
---
# <a name="creating-invoice-schedules-on-a-project-based-contract-line"></a>Stvaranje rasporeda faktura na retku ugovora koji se temelji na projektu

_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_


Možete stvoriti raspored faktura za redak ugovora koji se temelji na projektu. Fakturiranje je dozvoljeno tek nakon što sklopite ugovor i stvorite ugovor o projektu. Raspored računa omogućuje automatsko stvaranje nacrta računa za redak ugovora koji se temelji na projektu. Ako, međutim, samo ručno stvarate račune, možete preskočiti stvaranje rasporeda računa na redcima ugovora.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Stvaranje rasporeda faktura za vrijeme i materijal za redak ugovora

Kada je način naplate retka ugovora koji se temelji na projektu vrijeme i materijal, možete stvoriti raspored računa na temelju datuma. Kako biste automatski generirali raspored računa na temelju datuma, poduzmite sljedeće korake.

1. Idite na **Postavke** > **Učestalost faktura** i postavite učestalost faktura.
2. Idite na zapis ugovora o projektu i na kartici **Sažetak** u polju **Traženi datum isporuke** odaberite datum.
3. Otvorite redak ugovora **Vrijeme i materijal** za koji trebate napraviti raspored faktura koji se temelji na datumu. 
4. Na kartici **Raspored faktura** odaberite datum početka naplate i učestalost faktura.
5. Na podrešetki odaberite **Generiraj raspored faktura**. Raspored faktura generira se s poljima **Datum pokretanja fakture** , **Datum presjeka transakcije** i **Status pokretanja** postavljenima na sljedeći način:

    - **Datum pokretanja fakture** : Taj datum određuje učestalost faktura.
    - **Datum presjeka transakcije** : Dan prije datuma pokretanja fakture.
    - **Status pokretanja** : Automatski se postavlja na **Ne pokreći**. Kada se posao automatskog stvaranja fakture odvija za određeni datum pokretanja fakture, to će se polje ažurirati na **Uspješno pokretanje** ili **Neuspješno pokretanje**.


## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Stvaranje rasporeda faktura nepromjenjive cijene za redak ugovora

Kada redak ugovora ima nepromjenjiv način naplate, možete stvoriti raspored faktura na temelju kontrolne točke. Poduzmite sljedeće korake za generiranje rasporeda faktura koje se temelje na kontrolnoj točki za nepromjenjivi skup kontrolnih točaka koje su podjednako raspoređene za kalendarsko razdoblje.

1. Idite na **Postavke** > **Učestalost faktura** i postavite učestalost faktura.
2. Idite na zapis ugovora o projektu i na kartici **Sažetak** u polju **Traženi datum isporuke** odaberite datum.
3. Otvorite redak ugovora **Nepromjenjiva cijena** za koji trebate stvoriti raspored kontrolnih točaka. Na kartici **Kontrolne točke za naplatu** odaberite datum početka naplate i učestalost faktura. 
4. Na podrešetki odaberite **Generiraj povremene kontrolne točke**. Raspored faktura generira se s poljima **Naziv kontrolne točke** , **Datum kontrolne točke** i **Iznos kontrolne točke** koja su postavljena na sljedeći način:

    - **Naziv kontrolne točke** : Taj datum određuje učestalost faktura.
    - **Datum kontrolne točke** : Taj datum određuje učestalost faktura.
    - **Iznos kontrolne točke** : Ovaj se iznos izračunava dijeljenjem ugovornog iznosa na retku ugovora koji se temelji na projektu s brojem kontrolnih točaka kako je određeno učestalošću te početkom naplate i zatraženim datumima isporuke.

    Ako redak ugovora ima vrijednost u polju **Procijenjeni iznos poreza** , tada se to polje također raspodjeljuje na svaku kontrolnu točku podjednako kada se generiraju periodične kontrolne točke.

Kontrolne točke naplate trebale bi biti jednake ugovorenoj vrijednosti retka ugovora. Ako to ne učine, dobit ćete pogrešku na stranici **Redak ugovora**. Pogrešku možete popraviti provjerom stvaraju li kontrolne točke za naplatu ugovorenu vrijednost retka stvaranjem, uređivanjem ili brisanjem kontrolnih točaka. Nakon izvršenih promjena osvježite stranicu kako biste uklonili pogrešku.

### <a name="manually-create-milestones"></a>Ručno stvaranje kontrolnih točaka

Kontrolne točke s nepromjenjivom cijenom možete generirati ručno kada se povremeno ne dijele. Poduzmite sljedeće korake za ručno stvaranje kontrolne točke.

1. Otvorite redak ugovora s fiksnom cijenom za koji stvarate kontrolnu točku i na kartici **Raspored računa** , na podrešetki, odaberite **+ Stvori novu kontrolnu točku za redak ugovora**. 
2. Na stranici **Stvaranje kontrolne točke** unesite tražene podatke na temelju sljedeće tablice.

| Polje | Lokacija | Relevantnost, svrha i smjernice | Utjecaj na niže razine |
| --- | --- | --- | --- |
| Naziv kontrolne točke | Brzo stvaranje | Tekstno polje za naziv kontrolne točke. | To se prenosi na kontrolnu točku retka ugovora o projektu i na fakturu. |
| Projektni zadatak | Brzo stvaranje | Ako je kontrolna točka vezana uz projektni zadatak, s pomoću ove reference dodajte prilagođenu logiku koja je postavila status kontrolne točke na temelju statusa zadatka. | Ta referenca aplikacije nema nikakav utjecaj na niže razine u zadatku. |
| Datum kontrolne točke | Brzo stvaranje | Postavite datum na koji bi postupak automatskog stvaranja fakture trebao tražiti status ove kontrolne točke kako bi se uzela u obzir za fakturiranje. | To se prenosi na kontrolnu točku retka ugovora o projektu i na fakturu. |
| Status fakture | Brzo stvaranje | Kad se stvori kontrolna točka, taj se status uvijek postavi na **Nije spremno za fakturiranje** ili **Nije započelo**. | To se prenosi na kontrolnu točku retka ugovora o projektu i na fakturu. |
| Iznos retka | Brzo stvaranje | Iznos ili vrijednost kontrolne točke koja će se fakturirati klijentu. | To se prenosi na kontrolnu točku retka ugovora o projektu i na fakturu. |
| Porez | Brzo stvaranje | Iznos poreza primijenjen na kontrolnu točku. | To se prenosi na kontrolnu točku retka ugovora o projektu i na fakturu. |

3. Odaberite **Spremi i zatvori**.
| Iznos retka | Brzo stvaranje | Iznos ili vrijednost kontrolne točke koja će se fakturirati klijentu | To se proširuje na kontrolnu točku retka ugovora o projektu i na fakturu | | Porez | Brzo stvaranje | Iznos poreza koji će se primijeniti na kontrolnu točku | To se proširuje na kontrolnu točku retka ugovora o projektu i na fakturu |
