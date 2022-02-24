---
title: Dnevnik integracije u aplikaciji Project Operations
description: U ovoj temi nalaze se informacije o radu s dnevnikom integracije u aplikaciji Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a5f4d524530594bd3118f9b320acf4033c5d503
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948321"
---
# <a name="integration-journal-in-project-operations"></a>Dnevnik integracije u aplikaciji Project Operations

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Unosi vremena i troškova stvaraju **Stvarne** transakcije koje predstavljaju operativni prikaz dovršenog posla na projektu. Dynamics 365 Project Operations pruža računovođama alat za prikaz transakcija i, prema potrebi, prilagodbu računovodstvenih atributa. Nakon završetka pregleda i prilagodbi, transakcije se knjiže u sporednu knjigu i glavnu knjigu projekta. Računovođa može obavljati ove aktivnosti s pomoću dnevnika **Integracija aplikacije Project Operations** (dnevnik **Dynamics 365 Finance** > **Upravljanje projektom i računovodstvo** > **Dnevnici** > **Integracija aplikacije Project Operations**.

![Tijek dnevnika integracije](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Stvaranje zapisa u dnevniku integracije aplikacije Project Operations

Zapisi u dnevniku integracije aplikacije Project Operations stvaraju se povremenim postupkom, **Uvoz iz pripremne tablice**. Ovaj postupak možete pokrenuti odlaskom na **Dynamics 365 Finance** > **Upravljanje projektom i računovodstvo** > **Povremeno** > **Integracija aplikacije Project Operations** > **Uvoz iz pripremne tablice**. Postupak možete pokrenuti interaktivno ili ga prema potrebi konfigurirati tako da se pokreće u pozadini.

Kada se povremeni postupak pokrene, pronalaze se svi stvarni podaci koji još nisu dodani u dnevnik integracije aplikacije Project Operations. Stvara se redak dnevnika za svaku stvarnu transakciju.
Sustav grupira retke dnevnika u zasebne dnevnike na temelju vrijednosti odabrane u polju **Jedinica razdoblja u dnevniku integracije aplikacije Project Operations** (**Financije** > **Upravljanje projektom i računovodstvo** > **Postavljanje** > **Upravljanje projektom i računovodstveni parametri**, kartica **Project Operations u sustavu Dynamics 365 Customer Engagement**). Moguće vrijednosti za ovo polje uključuju:

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
    - Ako **Kategorija transakcije** nije postavljen u stvarnom podatku o projektu, sustav upotrebljava vrijednost u polju **Zadane postavke kategorije projekta** na kartici **Project Operations u sustavu Dynamics 365 Customer Engagement** na stranici **Upravljanje projektom i računovodstveni parametri**.
  - Polje **Resurs** predstavlja resurs projekta koji se odnosi na ovu transakciju. Resurs se upotrebljava kao referenca u prijedlozima faktura za projekt za klijente.
  - Polje **Tečaj** zadano je iz **Tečaja valute** postavljenog u aplikaciji Dynamics 365 Finance. Ako postavka tečaja nedostaje, povremeni postupak **Uvoz iz pripreme** neće dodati zapis u dnevnik i u zapisnik o izvršenju posla dodat će se poruka o pogrešci.
  - Polje **Svojstvo retka** predstavlja vrstu naplate u stvarnim podacima o projektu. Svojstvo retka i mapiranje vrste naplate definirani su na kartici **Project Operations u sustavu Dynamics 365 Customer Engagement** na stranici **Upravljanje projektom i računovodstveni parametri**.

Samo se sljedeći računovodstveni atributi mogu ažurirati u redcima dnevnika integracije aplikacije Project Operations:

- **Grupa za naplatu poreza na promet** i **Grupa za naplatu poreza na promet stavke**
- **Financijske veličine** (uporaba radnje **Raspodijeli iznose**)

Redci dnevnika integracije mogu se izbrisati, no svi redci koji nisu proknjiženi bit će ponovno umetnuti u dnevnik nakon što ponovno pokrenete povremeni postupak **Uvoza iz pripreme**.

Kada proknjižite dnevnik integracije, stvaraju se transakcije sporedne knjige i glavne knjige. Koriste se za fakturiranje klijentu, priznavanju prihoda i financijsko izvješćivanje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]