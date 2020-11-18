---
title: Upravljanje projektnim prilikama
description: U ovoj temi nalaze se informacije o načinu rada s prilikama koje su povezane s projektima.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 39ce52d5da4c7027ee2f2fa44579c0d4bf74925e
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087848"
---
# <a name="manage-project-based-opportunities"></a>Upravljanje projektnim prilikama

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Projektne tvrtke obično imaju svoje načine funkcioniranja pri isporuci u više zemalja i zemljopisnih područja. Troškovi izvršenja i isporuke projekta mogu se razlikovati ovisno o tome koje zemljopisno područje ili sektor upravlja isporukom. Zauzvrat, to može utjecati na marže posla. Dostava projektnih usluga obično uključuje velike količine vremena koje troše ljudski resursi, značajne troškove putovanja, materijalne troškove i druge troškove.

Projektne prilike u aplikaciji Dynamics 365 Project Operations oblikovane su s pomoću proširenja za aplikaciju Dynamics 365 Sales. Ova tema donosi pojedinosti o različitim poljima i poslovnoj logici koja je uključena u dodatnu funkcionalnost koja je potrebna projektnim tvrtkama za upravljanje projektnim mogućnostima.

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

Možete urediti tijek poslovnog procesa proizvoda ili stvoriti vlastite tijekove poslovnog procesa kako biste, po potrebi, pratili svoj prodajni postupak. Dodatne informacije o tijekovima poslovnog procesa potražite u članku [Pregled tijekova poslovnog procesa](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).