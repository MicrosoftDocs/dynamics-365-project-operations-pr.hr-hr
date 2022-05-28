---
title: Dnevnik integracije u aplikaciji Project Operations
description: U ovoj temi nalaze se informacije o radu s dnevnikom integracije u aplikaciji Project Operations.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5e1a455d055fe562a1946cc3b90c8274ef1a4b12
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582425"
---
# <a name="integration-journal-in-project-operations"></a>Dnevnik integracije u aplikaciji Project Operations

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Unosi vremena i troškova stvaraju **Stvarne** transakcije koje predstavljaju operativni prikaz dovršenog posla na projektu. Dynamics 365 Project Operations pruža računovođama alat za prikaz transakcija i, prema potrebi, prilagodbu računovodstvenih atributa. Nakon završetka pregleda i prilagodbi, transakcije se knjiže u sporednu knjigu i glavnu knjigu projekta. Računovođa može obavljati te aktivnosti pomoću temeljnice Integracija operacija **projekta (** Dynamics 365 Finance **Project management i accounting** > **Journals** > **Project Operations Integration** > **.**

![Tijek dnevnika integracije.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Stvaranje zapisa u dnevniku integracije aplikacije Project Operations

Zapisi u dnevniku integracije aplikacije Project Operations stvaraju se povremenim postupkom, **Uvoz iz pripremne tablice**. Taj postupak možete pokrenuti tako da **otvorite Dynamics 365 Finance** > **Project upravljanje i računovodstvo** > **Periodična** > **integracija integracije** > **projektnih operacija Uvoz iz pripremne tablice**. Postupak možete pokrenuti interaktivno ili ga prema potrebi konfigurirati tako da se pokreće u pozadini.

Kada se povremeni postupak pokrene, pronalaze se svi stvarni podaci koji još nisu dodani u dnevnik integracije aplikacije Project Operations. Stvara se redak dnevnika za svaku stvarnu transakciju.
Sustav grupira retke temeljnice u zasebne temeljnice na temelju vrijednosti odabrane u polju Razdoblje u **polju Temeljnica** integracije operacija projekta (**upravljanje financijskim** > **projektima i računovodstveni** > **parametri postave i računovodstveni** > **parametri**, **Operacije projekta na kartici Dynamics 365 Customer Engagement**). Moguće vrijednosti za ovo polje uključuju:

  - **Dani**: Stvarni su podaci grupirani po datumu transakcije. Za svaki dan izrađuje se zaseban dnevnik.
  - **Mjeseci**: Stvarni su podaci grupirani prema kalendarskom mjesecu. Za svaki mjesec izrađuje se zaseban dnevnik.
  - **Godine**: Stvarni su podaci grupirani prema kalendarskoj godini. Za svaku godinu izrađuje se zaseban dnevnik.
  - **Sve**: Sve stvarne transakcije uključene su u isti dnevnik integracije. Ako dnevnik nije dostupan kada se povremeni postupak izvodi, na primjer ako je dnevnik u postupku knjiženja transakcija, stvara se novi dnevnik.

Redci dnevnika stvaraju se na temelju stvarnih podataka o projektu. Sljedeći popis uključuje neka značajnijih zadanih i transformacijskih pravila:

  - Svaka stvarna transakcija projekta ima redak u dnevniku integracije aplikacije Project Operations. Transakcije troškova i nenaplaćene prodaje za vrstu naplate vremena i materijala prikazani su u odvojenim redcima.
  - Polje **Datum** predstavlja datum transakcije. Polje **Datum knjiženja** predstavlja datum evidentiranja transakcije u glavnu knjigu. Ako se datum knjiženja odvija u [zatvorenom financijskom razdoblju](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), i parametar **Automatski postavi datum knjiženja na razdoblje otvorene glavne knjige** je postavljen na kartici **Financijski** na stranici **Upravljanje projektom i računovodstveni parametri**, sustav će prilagoditi datum knjiženja transakcije prvom datumu u sljedećem razdoblju otvorene glavne knjige.
  - Polje **Vaučer** prikazuje broj vaučera za svaku stvarnu transakciju. Redoslijed brojeva vaučera definiran je na kartici **Brojčani nizovi** na stranici **Upravljanje projektom i računovodstveni parametri**. Svakom retku dodjeljuje se novi broj. Nakon što je vaučer proknjižen, odabirom mogućnosti **Povezani vaučeri** na stranici **Transakcija vaučera** možete vidjeti kako su povezane transakcije troškova i nenaplaćene prodajne.
  - Polje **Kategorija** predstavlja projektnu transakciju i zadane vrijednosti na temelju kategorije transakcije za povezani stvarni podatak o projektu.
    - Ako je **Kategorija transakcije** postavljena u stvarnom podatku o projektu, a povezana **Kategorija projekta** postoji u određenoj pravnoj osobi, za ovu kategoriju projekta kategorija je zadana.
    - Ako **kategorija** Transakcija nije postavljena u stvarnom programu Project, sustav koristi vrijednost u **polju Zadane vrijednosti kategorije** Projekta na **kartici Operacije projekta na Dynamics 365 Customer Engagement** na **stranici Parametri upravljanja projektom i računovodstva**.
  - Polje **Resurs** predstavlja resurs projekta koji se odnosi na ovu transakciju. Resurs se upotrebljava kao referenca u prijedlozima faktura za projekt za klijente.
  - Polje tečaja **zadano** je od **tečaja** valute postavljenog u Dynamics 365 Finance. Ako postavka tečaja nedostaje, povremeni postupak **Uvoz iz pripreme** neće dodati zapis u dnevnik i u zapisnik o izvršenju posla dodat će se poruka o pogrešci.
  - Polje **Svojstvo retka** predstavlja vrstu naplate u stvarnim podacima o projektu. Mapiranje svojstva retka i vrste naplate definirano je **na kartici Operacije projekta na Dynamics 365 Customer Engagement** na **stranici Parametri upravljanja projektom i računovodstva**.

Samo se sljedeći računovodstveni atributi mogu ažurirati u redcima dnevnika integracije aplikacije Project Operations:

- **Grupa za naplatu poreza na promet** i **Grupa za naplatu poreza na promet stavke**
- **Financijske veličine** (uporaba radnje **Raspodijeli iznose**)

Redci dnevnika integracije mogu se izbrisati, no svi redci koji nisu proknjiženi bit će ponovno umetnuti u dnevnik nakon što ponovno pokrenete povremeni postupak **Uvoza iz pripreme**.

Kada proknjižite dnevnik integracije, stvaraju se transakcije sporedne knjige i glavne knjige. Koriste se za fakturiranje klijentu, priznavanju prihoda i financijsko izvješćivanje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
