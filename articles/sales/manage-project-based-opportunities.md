---
title: Upravljanje projektnim prilikama
description: U ovoj temi nalaze se informacije o načinu rada s prilikama koje su povezane s projektima.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f39940ac063a8c202f33797ed649518907563e31
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600411"
---
# <a name="manage-project-based-opportunities"></a>Upravljanje projektnim prilikama

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Projektne tvrtke obično imaju svoje načine funkcioniranja pri isporuci u više zemalja i zemljopisnih područja. Troškovi izvršenja i isporuke projekta mogu se razlikovati ovisno o tome koje zemljopisno područje ili sektor upravlja isporukom. Zauzvrat, to može utjecati na marže posla. Dostava projektnih usluga obično uključuje velike količine vremena koje troše ljudski resursi, značajne troškove putovanja, materijalne troškove i druge troškove.

Prilike koje se temelje na projektu u aplikaciji Dynamics 365 Project Operations dizajnirane su s proširenjima za aplikaciju Dynamics 365 Sales. Ova tema donosi pojedinosti o različitim poljima i poslovnoj logici koja je uključena u dodatnu funkcionalnost koja je potrebna projektnim tvrtkama za upravljanje projektnim mogućnostima.

## <a name="view-all-project-based-opportunities"></a>Prikaz svih projektnih prilika

Popis svih projektnih prilika može se vidjeti na stranici s popisom **Prilika**. 

1. Idite na **Prodaja** > **Prilike**.
2. Upotrijebite **Preklopni gumb za prikaz** za odabir drugih filtriranih prikaza prilika. Možete stvoriti vlastite prikaze s prilagođenim kriterijima filtra kako biste konfigurirali te prikaze i mogućnosti navigacije.

Prilike za projekt mogu se stvoriti ili izbrisati s ove stranice s popisom ili stranice s pojedinostima.

## <a name="business-process-flow-for-project-based-deals"></a>Tijek poslovnog procesa za poslove temeljene na projektima

Sljedeći tijekovi poslovnog procesa podržani su za poslove temeljene na projektima u aplikaciji Project Operations:

- Poslovni proces od potencijalnog klijenta do prilike
- Proces prodaje prilike

### <a name="lead-to-opportunity-business-process"></a>Poslovni proces od potencijalnog klijenta do prilike 
Poslovni proces od potencijalnog klijenta do prilike podržava sljedeće faze:

| Faza | Mapirani entitet | Funkcija |
| --- | --- | --- |
| Kvalificiraj | Potencijalni klijent | Kvalificiranje potencijalnog klijenta za stvaranje računa, kontakta i prilike. |
| Razvij | Prilika | Pripremite priliku za dodavanje više podataka o uključenom poslu, ključnim dionicima i konkurenciji. |
| Predloži | Prilika | Pripremite prijedlog i nabavite odobrenje od internog tima za pregled. |
| Zatvaranje | Prilika | Osvojite priliku kako biste okončali posao. |

### <a name="opportunity-sales-process"></a>Proces prodaje prilike
Postupak Prodajne prilike u aplikaciji Project Operations proširenje je poslovnog tijeka postupka Prodajne prilike u aplikaciji Prodaja. Ovaj poslovni proces dizajniran je kao gotov za podršku sljedećim fazama u projektnim prilikama.

| Faza | Mapirani entitet | Funkcija |
| --- | --- | --- |
| Kvalificiraj | Prilika | Kvalificiranje potencijalnog klijenta za stvaranje računa, kontakta i prilike. |
| Predloži | Ponuda | Razradite prijedlog s pomoću ponuda projekta i nabavite odobrenje internog tima za pregled. |
| Ugovor | Ugovor o projektu | Ako se prihvati vaša ponuda, stvorite ugovor i počnite s izvršenjem i isporukom projekta. |
| Zatvaranje | Ugovor o projektu | Uspješno završite posao i zatvorite ugovor o projektu. |

> [!NOTE]
> Ako je vaš projektni posao započeo s potencijalnim klijentom, poslovni proces „Od potencijalnog klijenta do prilike“ ima prednost.
>
> Ako je vaš projektni posao započeo s Prilikom, prednost ima postupak Prodaje prilike.

Možete urediti tijek poslovnog procesa proizvoda ili stvoriti vlastite tijekove poslovnog procesa kako biste, po potrebi, pratili svoj prodajni postupak. Dodatne informacije o tijekovima poslovnog procesa potražite u članku [Pregled tijekova poslovnog procesa](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]