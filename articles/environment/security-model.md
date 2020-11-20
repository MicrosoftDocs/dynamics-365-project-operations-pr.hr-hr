---
title: Sigurnosni model
description: U ovoj temi nalaze se informacije o sigurnosnom modelu u aplikaciji Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 3fc4101d0ea4b8e2a4ba8f1d43540d57239cf402
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124359"
---
# <a name="security-model"></a>Sigurnosni model

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Microsoft Dynamics 365 Project Operations sadrži jedinstveni sigurnosni model koji omogućuje poslovni model sigurnosti koji se temelji na ulozi koja surađuje s Grupama sustava Microsoft Office. 


## <a name="security-roles"></a>Sigurnosne uloge
Pristupne mogućnosti aplikacije Project Operations uključuju sljedeće uloge:

| Uloga                          | Opis                                                                                                                                                                 | Opseg |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Upravitelj prakse              | Podržava izvješćivanje između projekata.                                                                                                            | Poslovna jedinica              |
| Odobravatelj projekta              | Odobrava vrijeme i troškove projekta                                                                                                                              | Poslovna jedinica |
| Administrator naplate projekta | Izrađuje prijedlog fakture.                                                                                                                                                 | Poslovna jedinica |
| Upravitelj projekta               | Izrađuje plan projekta i zahtjeve za resursima.                                                                                                                              | Poslovna jedinica |
| Resurs projekta              | Članovi tima koji se mogu rezervirati i prijaviti vrijeme.                                                                                                          | Poslovna jedinica|
| Upravitelj resursa              | Sve funkcije upravljanja resursima, poput ispunjavanja zahtjeva za resursima i rezervacija, odvojene su za podršku hibridnoj konfiguraciji Upravitelja projekata i Upravitelja resursa te jedinstvenu i centraliziranu ulogu upravitelja resursa. | Poslovna jedinica |


Microsoft Project za web uključuje sljedeće uloge:

| Uloga           | Opis                                                                                                        | Opseg  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Korisnik projekta   | Suradnički korisnik Projekta koji može stvoriti vlastite projekte i pregledati sve projekte koji su s njima dijeljeni. | Korisnik   |
| Sustav projekta | Uloga koja se upotrebljava za kontekst aplikacije. Klijenti ne bi trebali upotrebljavati ovu ulogu sustava.                                    | Globalno |

## <a name="security-enforcement"></a>Provedba sigurnosti
Radnje koje se izvršavaju na razini projekta izvode se u kontekstu prijavljenog korisnika. To znači da za stvaranje, otvaranje ili brisanje projekta korisnik mora imati pristup dostupan u CDS-u. Pristup CDS-u može se odobriti putem bilo kojeg od mogućih mehanizama uključenih u platformu. Na primjer, korisnik šireg opsega može pristupiti projektu ili ako je izvršena izričita radnja dijeljenja projekta koja korisniku daje pristup.

Bitno je to uzeti u obzir tijekom stvaranja projekata u aplikaciji Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Suvremena grupna suradnja s pomoću aplikacije Project Operations
Projekt za web i projektne operacije podržava suvremene grupe za suradnju. Korisnici dodani projektu putem grupe mogu uređivati plan projekta.

Projekt za web automatski dodaje korisnike u grupu nakon dodjele.

Grupe omogućuju suradnju na dozvolama projekta i podržavanju artefakta suradnje. Sljedeći dijagram prikazuje događaje i promjene stanja koji se događaju tijekom postupka grupnog dodjeljivanja.

Project Operations ne stvara grupu podrazumijevanom radnjom, već to čini samo izričitom radnjom pritiska na grupe.

Pretraživanje člana grupe u dijaloškom okviru **Upravljanje grupom** ograničeno je na one koji su postavljeni kao dio sigurnosne grupe okruženja. Dodatne informacije potražite u odjeljku [Upravljanje korisničkim pristupom okruženjima: sigurnosne grupe i licence](https://docs.microsoft.com/power-platform/admin/control-user-access).

![Grupni način](./media/groupsmode.png)

1. Projekt stvara i posjeduje Korisnik koji ga je stvorio.
2. Vlasnik projekta ažuriran je na tim.
3. Tim vlasnik preslikava se u navedenu ili stvorenu grupu sustava Office.
4. Izvorni vlasnik projekta dodan je u grupu sustava Office.

## <a name="deployment-recommendation"></a>Preporuke za implementaciju
Kako se model suradnje grupe sustava Office razvija, dodavat će se funkcionalnost koja će tijekom vremena pružati podrobniju kontrolu. Klijenti koji danas implementiraju aplikaciju Project Operations potiču se da se usredotoče na tradicionalni sigurnosni model sustava Microsoft Dynamics 365.

Dodatne informacije potražite u odjeljku [Sigurnost na platformi Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Projektne operacije i sigurnost aplikacije Microsoft Dynamics 365 Finance
Project Operations uključuju sljedeće uloge:

- Upravitelj projekta
- Projektno računovodstvo

Dodatne informacije o sigurnosti u aplikaciji Finance potražite u članku [Sigurnost koja se temelji na ulozi](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


