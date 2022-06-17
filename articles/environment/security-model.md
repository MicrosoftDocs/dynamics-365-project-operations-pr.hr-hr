---
title: Sigurnosni model
description: U ovom se članku nalaze informacije o sigurnosnom modelu u programu Dynamics 365 Project Operations.
author: stsporen
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2f4992b1ea0c2b93a83c6c2c9a146a7610afc5fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924490"
---
# <a name="security-model"></a>Sigurnosni model

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_



Microsoft Dynamics 365 Project Operations sadrži jedinstveni sigurnosni model koji omogućuje poslovni model sigurnosti na temelju uloge u suradnji s Grupama programa Microsoft Office. 


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


Microsoft Project for the Web uključuje sljedeće uloge:

| Uloga           | Opis                                                                                                        | Opseg  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Korisnik projekta   | Suradnički korisnik Projekta koji može stvoriti vlastite projekte i pregledati sve projekte koji su s njima dijeljeni. | Korisnik   |
| Sustav projekta | Uloga koja se upotrebljava za kontekst aplikacije. Klijenti ne bi trebali upotrebljavati ovu ulogu sustava.                                    | Globalno |

## <a name="security-enforcement"></a>Provedba sigurnosti
Radnje koje se izvršavaju na razini projekta izvode se u kontekstu prijavljenog korisnika. To znači da za stvaranje, otvaranje ili brisanje projekta korisnik mora imati pristup dostupan u CDS-u. Pristup CDS-u može se odobriti putem bilo kojeg od mogućih mehanizama uključenih u platformu. Na primjer, korisnik šireg opsega može pristupiti projektu ili ako je izvršena izričita radnja dijeljenja projekta koja korisniku daje pristup.

Bitno je to uzeti u obzir tijekom stvaranja projekata u aplikaciji Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Suvremena grupna suradnja s pomoću aplikacije Project Operations
Project for the Web i Project Operations podržavaju suvremene grupe za suradnju. Korisnici dodani projektu putem grupe mogu uređivati plan projekta.

Project for the Web automatski dodaje korisnike u grupu nakon dodjele.

Grupe omogućuju suradnju na dozvolama projekta i podržavanju artefakta suradnje. Sljedeći dijagram prikazuje događaje i promjene stanja koji se događaju tijekom postupka grupnog dodjeljivanja.

Project Operations ne stvara grupu podrazumijevanom radnjom, već to čini samo izričitom radnjom pritiska na grupe.

Pretraživanje člana grupe u dijaloškom okviru **Upravljanje grupom** ograničeno je na one koji su postavljeni kao dio sigurnosne grupe okruženja. Dodatne informacije potražite u odjeljku [Upravljanje korisničkim pristupom okruženjima: sigurnosne grupe i licence](/power-platform/admin/control-user-access).

![Grupni način.](./media/groupsmode.png)

1. Projekt stvara i posjeduje Korisnik koji ga je stvorio.
2. Vlasnik projekta ažuriran je na tim.
3. Tim vlasnik preslikava se u navedenu ili stvorenu grupu sustava Office.
4. Izvorni vlasnik projekta dodan je u grupu sustava Office.

## <a name="deployment-recommendation"></a>Preporuke za implementaciju
Kako se model suradnje grupe sustava Office razvija, dodavat će se funkcionalnost koja će tijekom vremena pružati podrobniju kontrolu. Klijenti koji danas implementiraju aplikaciju Project Operations potiču se da se usredotoče na tradicionalni sigurnosni model sustava Microsoft Dynamics 365.

Dodatne informacije potražite u odjeljku [Sigurnost na platformi Common Data Service](/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Projektne operacije i Microsoft Dynamics 365 Financijska sigurnost
Project Operations uključuju sljedeće uloge:

- Upravitelj projekta
- Projektno računovodstvo

Dodatne informacije o sigurnosti u aplikaciji Finance potražite u članku [Sigurnost koja se temelji na ulozi](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).




[!INCLUDE[footer-include](../includes/footer-banner.md)]