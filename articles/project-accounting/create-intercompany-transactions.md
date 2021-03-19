---
title: Stvaranje transakcija unutar tvrtke
description: U ovoj temi nalaze se informacije o načinu stvaranja transakcija unutar tvrtke.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6d23e45d99be61e93d98a8377ff5fa05b3febb6b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287409"
---
# <a name="create-intercompany-transactions"></a>Stvaranje transakcija unutar tvrtke

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Transakcije unutar tvrtke, transakcije su vremena i troškova iz ugovora o projektu koje pripadaju jednoj tvrtki ili organizacijskoj jedinici, dok su resursi u ugovoru o projektu dio druge tvrtke ili organizacijske jedinice.

Kada se odobri transakcija unutar tvrtke, stvaraju se sljedeće stvarne transakcije

| **Vrsta transakcije** | **Primijenjeni cjenik** | **Valuta transakcije** |
| --- | --- | --- |
| Cijena | Cjenik koštanja ugovorne jedinice | Valuta u retku cijene |
| Nenaplaćena prodaja. Stvoreni su samo za stvarne podatke koji su povezani s retkom ugovora koji sadrži vrstu naplate, vrijeme i materijal. | Prodajni cjenik ugovora o projektu | Valuta ugovora |
| Jedinična cijena resursa | Cjenik koštanja jedinice resursa | Valuta u retku cijene |
| Prodaja između organizacijskih jedinica | Cjenik koštanja ugovorne jedinice | Valuta u retku cijene |

Trošak, jedinična cijena resursa te jedinična cijena i valuta međuorganizacijske prodajne transakcije ovise o **organizacijskoj jedinici**. To je važno imati na umu pri odlučivanju o strukturiranju tvrtki i organizacijskih jedinica u vašoj implementaciji.

Kada stvarate priliku, ponudu, ugovor o projektu i zapise o projektu, sustav provjerava podudara li se valuta ugovorne jedinice s knjigovodstvenom valutom ugovorne tvrtke. Kad nisu iste, te zapise nije moguće stvoriti. Valuta organizacijske jedinice definira se u aplikaciji Dynamics 365 Project Operations odlaskom na **Dataverse** > **Postavke** > **Organizacijske jedinice**. Računovodstvena valuta tvrtke definira se u aplikaciji Dynamics 365 Finance odlaskom na **Glavna knjiga** > **Postavljanje knjige** > **Knjiga**. Valuta je sinkronizirana s vašim okruženjem Dataverse s pomoću karte knjiga dvostrukog upisa.

Sustav stvara cijenu jedinice resursa i stvarne podatke o prodaji između organizacijskih jedinica u sljedećim situacijama:

  - Kada se jedinica resursa razlikuje od ugovorne jedinice
  - Kada se tvrtka za resurse razlikuje od ugovorne tvrtke

Međutim, samo će se transakcije koje imaju drugu tvrtku za resurse, koja se razlikuje od ugovorne tvrtke, prenijeti u okruženje Dynamics 365 Finance za dodatno računovodstvo.

Računovodstvo stvarnih podataka o projektu zabilježeno je u dnevniku integracije aplikacije Project Operations u aplikaciji Finance. Sustav stvara sljedeće retke dnevnika.

| **Vrsta transakcije** | **Poslovna osoba** | **Stvara projektnu transakciju u knjiženju** | **Financijske veličine zadane iz** | **Zadana grupa za naplatu poreza na promet i grupa za naplatu poreza na promet stavke** |
| --- | --- | --- | --- | --- |
| Cijena | Ne dodaje se u dnevnik o integraciji | Nije dostupno | Nije dostupno | Nije dostupno |
| Nenaplaćene prodaje | Dnevnik integracije pravne osobe koja se zadužuje | Jest | Project | **Grupa poreza na promet za naplatu** : Utemeljeno na **ugovorni klijent** <br/> **Grupa poreza na promet za stavku naplate**: Iz trenutačne kategorije projekta pravnog entiteta na redak dnevnika |
| Jedinična cijena resursa | Dnevnik integracije pravne osobe koja kreditira | No | Klijent unutar tvrtke | **Grupa poreza na promet za naplatu**: Utemeljeno na **klijentu unutar tvrtke** <br/> **Grupa poreza na promet za stavku naplate**: Iz trenutačne kategorije projekta pravnog entiteta na redak dnevnika |
| Međuorganizacijska prodaja | Dnevnik integracije pravne osobe koja kreditira | No | Klijent unutar tvrtke | **Grupa poreza na promet za naplatu**: Utemeljeno na **klijentu unutar tvrtke** <br/> **Grupa poreza na promet za stavku naplate**: Iz trenutačne kategorije projekta pravnog entiteta na redak dnevnika |

### <a name="example-intercompany-transactions"></a>Primjer: Transakcija unutar tvrtke

Molly Clark, razvojna inženjerka zaposlena u GBPM, bilježi 10 sati rada na projektu USPM Adventure Works, što voditelj projekta odobrava. Trošak razvojnog inženjera u GBPM iznosi 88 GBP po satu. GBPM će naplaćivati od USPM 120 USD po satu razvojnog inženjera. USPM će klijentu naplatiti Adventure Works, 200 USD, za rad koji je obavio resurs GBPM. Dodatne informacije potražite u odjeljku [Konfiguriranje određivanja cijena unutar tvrtke](configure-intercompany-invoicing.md).

1. U aplikaciji Project Operations idite na **Resursi** i s popisa odaberite **Molly Clark**. Na kartici **Planiranje**, u polju **Tvrtka**, odaberite mogućnost **GBPM**.
2. Idite na **Prodaja** > **Klijenti** i odaberite **Novi** za stvaranje novog zapis o klijentu za rješenje Adventure Works.
    1. Postavite tvrtku na **USPM**.
    2. Postavite stavku **Vrsta veze** na **Klijent**.
    3. Odaberite **Grupa klijenata 10 – Domaći**.
    4. Postavite valutu na **USD**.
    5. Spremite zapis.
3. Idite na **Prodaja** > **Ugovori o projektu** i stvorite novi ugovor o projektu za aplikaciju Adventure Works.
    1. Postavite tvrtku vlasnicu na **USPM**, a ugovornu jedinicu na **Contoso Robotics US**.
    2. Kao klijenta odaberite Adventure Works.
    3. Odaberite cjenik proizvoda i spremite zapis.
    4. Na kartici **Redci ugovora** stvorite novi redak ugovora. Postavite neki naziv i kao način naplate odaberite **Vrijeme i materijali**.
    5. Stvorite novi projekt i povežite ga s ovim retkom ugovora.
4. Prijavite se kao resurs **Molly Clark**. Idite na **Projekti** > **Unosi vremena** i stvorite unos vremena za projekt Adventure Works.
5. Prijavite se kao voditelj projekta. Idite na **Projekti** > **Odobrenja** i odobrite transakciju vremenskog unosa koju je zabilježila Molly Clark.
6. Idite na projekt Adventure Works i odaberite **Povezano** > **Stvarne vrijednosti**. Stvorene su sljedeće stvarne transakcije.

| **Vrsta transakcije** | **Cijena** | **Valuta transakcije** | **Iznos** |
| --- | --- | --- | --- |
| Cijena | 120 | USD | 1200 |
| Nenaplaćene prodaje | 200 | USD | 2000 |
| Jedinična cijena resursa | 88 | GBP | 880 |
| Prodaja između organizacijskih jedinica | 120 | USD | 1200 |

7. Prijavite se kao računovođa USPM-a. Otvorite instancu aplikacije Finance u aplikaciji Project Operations i odaberite tvrtku **USPM**. 
8. Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Project Operations na Customer Engagement** > **Uvoz iz faza** i odaberite pokretanje periodičnog postupka. Ovaj periodični postupak popunjavat će dnevnik integracije aplikacije Project Operations.
9. Idite na **Upravljanje projektima i računovodstvo** > **Dnevnici** > **Dnevnik integracije aplikacije Project Operations** i pregledajte retke dnevnika. Sustav stvara sljedeći redak.

    | **Vrsta transakcije** | **Cijena** | **Valuta transakcije** | **Iznos** |
    | --- | --- | --- | --- |
    | Nenaplaćene prodaje | 200 | USD | 2000 |

    Ako je sustav postavljen za obračun prihoda za ovaj projekt, knjiži se sljedeće:

    - Dugovanje: Projekt – WIP prodajna vrijednost od 200 USD
    - Kredit: Projekt – Obračunani prihod 200 USD

    Ova nefakturirana prodaja sada je spremna za fakturiranje. Faktura za klijenta Adventure Works može se financijski knjižiti po potrebi.

10. Prijavite se kao računovođa tvrtke **GBPM**. Otvorite instancu aplikacije Finance u aplikaciji Project Operations i otvorite tvrtku **GBPM**. 
11. Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Project Operations na Customer Engagement** > **Uvoz iz faza** i odaberite pokretanje periodičnog postupka za popunjavanje dnevnika integracije aplikacije Project Operations.
12. Idite na **Upravljanje projektima i računovodstvo** > **Dnevnici** > **Dnevnik integracije aplikacije Project Operations** i pregledajte retke. Sustav stvara sljedeće retke.

    | **Vrsta transakcije** | **Cijena** | **Valuta transakcije** | **Iznos** |
    | --- | --- | --- | --- |
    | Jedinična cijena resursa | 88 | GBP | 880 |
    | Prodaja između organizacijskih jedinica | 120 | USD | 1200 |

    Knjiženje ovih zapisa rezultira sljedećim transakcijama vaučera:

    - Dugovanje: Trošak projekta 88 GBP
    - Kredit: Raspodjela plaćanja 88GBP

    Ako je sustav postavljen za obračun prihoda unutar tvrtke, knjiži se sljedeće:

    - Dugovanje: Projekt – WIP prodajna vrijednost od 120 USD
    - Kredit: Projekt – Obračunani prihod 120 USD

    Sustav je sada spreman za stvaranje fakture za klijenta unutar tvrtke.


[!INCLUDE[footer-include](../includes/footer-banner.md)]