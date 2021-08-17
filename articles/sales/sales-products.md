---
title: Proizvodi
description: U ovoj se temi nalaze informacije o katalogu proizvoda s pomoću kojeg klijentima pružate informacije o proizvodima i cijenama koje nudi vaša tvrtka ili ustanova.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 085b7e4d9274f8c8d94d7a84109cfa782acf3dbb9241bfd25ecb8c2f329e1bb8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986842"
---
# <a name="products"></a>Proizvodi

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Proizvodi su temelj vašeg poslovanja. Katalog proizvoda u aplikaciji Dynamics 365 Sales Professional zbirka je proizvoda i informacija o cijenama. Brzo stvorite katalog proizvoda i olakšajte svojim prodajnim predstavnicima povećanje prodaje.

## <a name="add-a-product"></a>Dodavanje proizvoda

1.  Provjerite imate li ulogu stručnog voditelja prodaje ili administratora sustava kako biste dodali proizvode u aplikaciju Dynamics 365 Sales Professional.
2.  U karti web-mjesta, pod stavkom **Postavljanje**, odaberite mogućnost **Proizvodi**.
3.  Odaberite **Dodaj proizvod** i popunite sljedeće podatke:

    -  **Ime**
    -  **ID proizvoda**
    -  **Nadređen**: Odaberite nadređenu skupinu proizvoda za proizvod. Ako stvarate podređeni proizvod u skupini proizvoda, ovdje se unosi naziv skupine nadređenih proizvoda. To se ne može promijeniti nakon što se zapis spremi.
    -  **Valjan od**/**Valjan do**: Definirajte razdoblje tijekom kojeg je proizvod valjan tako da odaberete datum **Valjan od** i **Valjan do**.
    -  **Grupa jedinica**: odaberite grupu jedinica. Grupa jedinica je skup različitih jedinica u kojima se prodaje proizvod i definira kako se pojedinačne stavke grupiraju u veće količine. Na primjer, ako kao proizvod dodajete sjemenke, možda ste stvorili grupu jedinica pod nazivom „Sjemenke” i definirali njenu primarnu jedinicu kao „paket”.
    -  **Zadana jedinica**: Odabir najčešće jedinice u kojoj će se proizvod prodavati. Jedinice su količine ili mjerne jedinice u kojima prodajete proizvode. Na primjer, ako ste dodali sjemenke kao proizvod, možete ih prodavati u paketima, kutijama ili paletama. Svaka od njih postaje jedinica proizvoda. Ako se sjemenke većinom prodaju u paketima, odaberite to kao jedinicu.
    -  **Zadani cjenik**: Ako je riječ o novom proizvodu, to je polje samo za čitanje. Kako biste mogli odabrati zadani cjenik, morate ispuniti sva obavezna polja, a zatim spremiti zapis. Iako zadani cjenik nije obavezan, nakon spremanja zapisa proizvoda dobro je postaviti zadani cjenik za svaki proizvod. U tom slučaju, ako zapis klijenta ne sadrži cjenik, aplikacija Sales može koristiti zadani cjenik za generiranje ponuda, narudžbi i faktura.
    -  **Podržani decimalni brojevi**: Morate unijeti cijeli broj između 0 i 5. Ako se proizvod ne može podijeliti na dijelove, unesite 0. Ako proizvodu nije pridružen cjenik, točnost polja **Količina** u zapisu ponude, narudžbe ili proizvoda na fakturi provjerava se u odnosu na vrijednost u ovom polju.
    -  **Predmet**: Taj proizvod možete povezati s predmetom. Pomoću predmeta možete kategorizirati proizvode i filtrirati izvješća.

4.  Odaberite **Spremi**.
5.  Na kartici **Dodatne pojedinosti**, u odjeljku **Stavke cjenika**, odaberite **Dodatne naredbe** i zatim odaberite mogućnost **Dodaj nove stavke cjenika**.
7.  Na kartici **Dodatne pojedinosti**, u odjeljku **Odnos proizvoda**, odaberite ikonu **Dodatne naredbe** i zatim odaberite mogućnost **Dodaj novi odnos proizvoda**.
8.  U obrascu **Novi odnos proizvoda** unesite sljedeće pojedinosti, a na naredbenoj traci odaberite mogućnost **Spremi i zatvori**:

    -   **Povezani proizvodi**: Odaberite proizvod koji želite dodati kao povezani proizvod u postojeći zapis o proizvodu na kojem radite.
    -   **Vrsta prodajnog odnosa**: Odaberite želite li dodati proizvod kao napredniji proizvod, povezani proizvod, dodatak ili zamjenski proizvod.
    -   **Smjer**: Odaberite hoće li odnos između proizvoda biti jednosmjeran ili dvosmjeran. Ako odaberete jednosmjeran, proizvod koji ste odabrali u stavci **Povezan proizvod** prikazat će se kao preporuka za postojeći proizvod, ali ne i obrnuto.

9.  Na obrascu proizvoda odaberite mogućnost **Spremi**.

## <a name="import-products"></a>Uvoz proizvoda

Možete upotrijebiti predloške za uvoz kako biste u aplikaciju Dynamics 365 Sales unijeli skupne podatke o proizvodu.

## <a name="revise-a-product"></a>Revizija proizvoda

Redovito ažurirajte zalihe proizvoda tako da, prema potrebi, brzo revidirate svojstva proizvoda i ponovno objavite informacije kako bi vaši prodajni predstavnici mogli vidjeti najnovije promjene zaliha.

1.  Provjerite imate li jednu od sljedećih sigurnosnih uloga ili ekvivalentnih dozvola: administrator sustava, osoba za prilagodbu sustava, upravitelj prodaje, potpredsjednik za prodaju, potpredsjednik za marketing, generalni ili poslovni direktor.
2.  U karti web-mjesta odaberite opciju **Proizvodi**.
3.  Otvorite aktivni proizvod koji želite promijeniti i na naredbenoj traci odaberite mogućnost **Revizija**.
4.  U dijaloškom okviru **Potvrda revizija** odaberite **Potvrdi**. To će promijeniti stanje proizvoda u **U reviziji**.
5.  Nakon što završite s izmjenama, u naredbenoj traci odaberite mogućnost **Objavljivanje**.

    > [!TIP]
    > Kako biste vratili promjene i nastavili s posljednjom aktivnom verzijom proizvoda, odaberite mogućnost **Vraćanje**. To mijenja stanje proizvoda natrag na **Aktivno**.

## <a name="clone-a-product"></a>Kloniranje proizvoda 

Kada stvarate novi proizvod, uštedite vrijeme kloniranjem postojećeg. Tako se stvara kopija izvornog zapisa sa svim detaljima osim naziva i ID-a.

1.  Provjerite imate li jednu od sljedećih sigurnosnih uloga ili ekvivalentnih dozvola: administrator sustava, osoba za prilagodbu sustava, upravitelj prodaje, potpredsjednik za prodaju, potpredsjednik za marketing, generalni ili poslovni direktor.
2.  U karti web-mjesta odaberite opciju **Proizvodi**.
3.  Odaberite zapis proizvoda koji želite klonirati i na naredbenoj traci odaberite **Kloniranje**. Prikazat će se dijaloški okvir za potvrdu.
4.  Odaberite **Potvrdi**.

Novi zapis o proizvodu otvara se s istim pojedinostima kao što su u izvorniku, osim naziva i ID-a.

## <a name="retire-a-product"></a>Opoziv proizvoda 

Ako vaša tvrtka ili ustanova više ne prodaje proizvod, opozovite ga tako da više nije dostupan vašim prodajnim predstavnicima.

1.  Provjerite imate li sigurnosnu ulogu administratora sustava ili voditelja Sales Professional ili jednakovrijedne dozvole.
2.  U karti web-mjesta odaberite opciju **Proizvodi**.
3.  Otvorite aktivni proizvod koji želite opozvati i na naredbenoj traci odaberite mogućnost **Opoziv**.
4.  U dijaloškom okviru **Potvrda opoziva** odaberite **Potvrdi**.


## <a name="delete-a-product"></a>Brisanje proizvoda

Da biste zaustavili prodaju proizvoda, izbrišite je.

> [!IMPORTANT]
> Ne možete vratiti izbrisane zapise.

1.  Provjerite imate li sigurnosnu ulogu administratora sustava ili voditelja Sales Professional ili jednakovrijedne dozvole.
2.  U karti web-mjesta odaberite opciju **Proizvodi**.
3.  Odaberite zapis proizvoda koji želite izbrisati i na naredbenoj traci odaberite mogućnost **Brisanje**.
4.  U dijaloškom okviru **Potvrdi brisanje** odaberite mogućnost **Nastavi**.
 
 ## <a name="quantity-factors-for-products"></a>Čimbenici količine za proizvode

Čimbenici količine podržavaju prodaju proizvoda temeljenih na pretplati. Za proizvode temeljene na pretplati količina u retku ponude ili ugovora o projektu izražena je kao broj korisničkih mjeseci.

Cijena softvera za pretplatu obično se pohranjuje u katalog kao mjesečna cijena po korisniku. Međutim, umjesto toga možete koristiti druge vremenske opise. Tijekom prodajnog postupka cijena u retku ponude obično je dogovorena mjesečna cijena cijena po korisniku uz popust IT prodajnog predstavnika. Svaki ugovor ima različit broj korisnika i različit broj mjeseci pretplate. Količina koja se koristi za izračun iznosa retka ponude proizvod je broja korisnika i broja mjeseci pretplate.

Čimbenici količine oslanjaju se na atribute proizvoda. Kada konfigurirate određena svojstva za proizvod, možete označiti podskup tih svojstava ili svih svojstava kao čimbenika količine.

Sustav provjerava valjanost jesu li samo numerička svojstva ili svojstva proizvoda koja imaju numeričku vrstu podataka označena kao čimbenici količine. Kada se proizvod za koji su konfigurirani čimbenici količine doda u redak ponude, polje **Količina** u retku ponude postaje polje samo za čitanje. Nakon što unesete vrijednosti za svojstva proizvoda koja su čimbenici količine, izračunava se količina retka ponude.

Na primjer, ako postoje sljedeća svojstva: 

- **Broj korisnika**: broj korisnika 
- **Broj mjeseci**: broj mjeseci pretplate
- **SKU proizvoda** 

Svojstva **Broj korisnika** i **Broj mjeseci** mogu se označiti kao čimbenici količine uređivanjem svojstava retka proizvoda. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]