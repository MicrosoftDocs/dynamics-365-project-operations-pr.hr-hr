---
title: Upravljanje potencijalnim klijentima
description: U ovoj temi nalaze se informacije o upravljanju potencijalnim klijentima koji se temelje na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 16f5dbb283eee12cf10ca7145ea9e17c5ef8923e
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513825"
---
# <a name="manage-leads"></a>Upravljanje potencijalnim klijentima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Potencijalnim se klijentima koji se temelje na projektu može upravljati u aplikaciji Project Operations, gdje ih se može i kvalificirati Proces upravljanja potencijalnim klijentima uključuje stvaranje potencijalnih klijenata koji se temelje na radu i njihovo kvalificiranje. 

## <a name="project-sales-leads"></a>Potencijalni klijenti prodaje projekta

U lijevom navigacijskom oknu odjeljka **Prodaja** otvorite stranicu popisa **Potencijalni klijenti** za prikaz popisa svih zapisa o potencijalnim klijentima u sustavu. Prikazani popis potencijalnih klijenata temelji se na radu i drugim vrstama potencijalnih klijenata koji se mogu stvoriti ako imate aplikaciju Dynamics 365 Sales ili Dynamics 365 Field Service.

Možete stvoriti filtrirani prikaz, kako biste vidjeli samo potencijalne klijente koji se temelje na projektu, stvaranjem filtra na vrijednosti **Vrsta**. Na primjer, možete odabrati prikazivanje samo potencijalnih klijenata koji se temelje na radu.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Stvaranje novog potencijalnog klijenta za posao koji se temelji na projektu

Kad se potencijalni klijent koji se temelji na projektu kvalificira, stvaraju se prilika i račun. Prilika koji se temelji na projektu polazna je točka za aktivnosti potrage za prodajom u fazi Prilike. Prilike koje se temelje na projektu imaju jedinstvene mogućnosti potrebne za prodaju rada na projektu. Te mogućnosti uključuju:

- Načine naplate Vrijeme i materijal te Nepromjenjiva cijena
- Više cjenika koji vrijede na datum za ljudske resurse, troškove i materijal koji su nastali na projektima

Kako bi kvalificirani potencijalni klijent automatski stvorio priliku, kada stvarate potencijalnog klijenta postavite atribut **Vrsta** na mogućnost **Na temelju rada**. Ako odaberete drugu vrstu, potencijalni klijent neće stvoriti priliku koji se temelji na projektu kad je kvalificiran. Ako se prilika koji se temelji na projektu ne stvori, mogućnosti specifične za projekt neće biti dostupne u prodajnim procesima na nižim razinama.

Sljedeća tablica uključuje bitne podatke o polju za potencijalnog klijenta i djelovanje tih polja na niže razine.
 
| **Polje** | **Mjesto** | **Opis** | **Utjecaj prema dolje** |
| --- | --- | --- | --- |
| Tema | Kartica Općenito | Ovo tekstno polje treba sadržavati kratki opis posla. | Tema potencijalnog klijenta bit će zadana kao tema Prilike, te naziv ponude i ugovor o projektu. |
| Tip | Kartica Općenito | Ovo polje skupa mogućnosti ima sljedeće mogućnosti:</br>- na temelju rada (dostupno samo kada je instalirana aplikacija Project Operations)</br>- na temelju stavke (dostupno samo kada su instalirane aplikacije Project Operations i Sales)</br>- Temeljeno na servisnom održavanju (dostupno kada se instalira aplikacija Field Service) | Kada je vrijednost ovog polja za potencijalnog klijenta postavljena na mogućnost **Na temelju rada** potencijalni klijent kvalificiran je za stvaranje prilike koji se temelji na projektu. Za ovaj posao potrebna je prilika koji se temelji na projektu koja će omogućiti sva proširenja i funkcionalnost u procesu prodaje prema nižim razinama. |
| Ime | Kartica Općenito | Ime kontakta potencijalnog klijenta | Kad se potencijalni klijent kvalificira, stvaraju se račun, kontakt i prilika. Ovdje je postavljena vrijednost za ime kontakta. |
| Prezime | Kartica Općenito | Prezime kontakta potencijalnog klijenta | Kad se potencijalni klijent kvalificira, stvaraju se račun, kontakt i prilika. Ovdje je postavljena vrijednost za prezime kontakta. |
| Tvrtka | Kartica Općenito | Naziv tvrtke potencijalnog klijenta | Kad se potencijalni klijent kvalificira, stvaraju se račun, kontakt i prilika. Naziv računa koji je stvorio ovdje postavljenu vrijednost. |
| Valuta | Kartica pojedinosti | Valuta potencijalnog klijenta | Kad se potencijalni klijent kvalificira, stvaraju se račun, kontakt i prilika. Valuta stvorenog računa vrijednost je postavljena ovdje. |

## <a name="qualify-a-new-project-based-lead"></a>Kvalificiranje novog potencijalnog klijenta koji se temelji na projektu

Potencijalni klijenti koji vrijednost **Vrsta** imaju postavljenu na **Na temelju rada** nazivaju se potencijalni klijenti koji se temelje na projektu. Kad se kvalificira potencijalni klijent koji se temelji na projektu, stvara se sljedeće:

- Račun koji upotrebljava polje **Tvrtka** potencijalnog klijenta.
- Zapis kontakata povezan s računom koji se temelji na vrijednostima u poljima **Ime** i **Prezime** potencijalnog klijenta.
- Prilika koji se temelji na projektu koja ima polje **Vrsta** postavljeno na **Na temelju rada**.

Podrobnije informacije o kvalificiranim potencijalnim klijentima potražite u članku [Kvalificiranje ili pretvaranje potencijalnih klijenata](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Kvalifikacija potencijalnog klijenta i podaci o pravnoj osobi 

Kada pokrenete Projektne operacije s pomoću načina implementacije, Project Operations za scenarije koji se temelje na resursima / bez zaliha, svaki klijent i prilika zahtijevat će postavljanje polja **Tvrtka vlasnica**. Tvrtka vlasnica pravna je osoba u vašoj tvrtki ili ustanovi koja je vlasnik isporuke projekta. Svaki klijent ili račun s vrstom odnosa klijenta mora u polju **Tvrtka vlasnica** imati vrijednost postavljenu za pravnu osobu koja ugovara i pregovara s ovim klijentom. Klijent može biti samo u jednoj pravnoj osobi.

Kad se potencijalni klijent kvalificira, stvoreni zapisi o klijentima i prilikama imat će polje **Tvrtka vlasnica** postavljeno na tvrtku trenutačnog korisničkog zapisa resursa koji se može rezervirati.

Ako je trenutačni korisnički zapis resursa koji se može rezervirati prazan, tada se vrijednost polja **Tvrtka vlasnica** na korisničkom zapisu upotrebljava kao zadana na zapisima klijenta i prilike.

## <a name="business-process-flow-for-project-based-deals"></a>Tijek poslovnog procesa za poslove temeljene na projektima

Sljedeći tijekovi poslovnog procesa podržani su za poslove temeljene na projektima u aplikaciji Project Operations:

- Poslovni proces od potencijalnog klijenta do prilike
- Proces prodaje prilike

Poslovni proces od potencijalnog klijenta do prilike podržava sljedeće faze:

| Naziv faze | Mapirani entitet | Funkcija |
| --- | --- | --- |
| Kvalificiraj | Potencijalni klijent | Kvalificiranje potencijalnog klijenta za stvaranje računa, kontakta i prilike. |
| Razvij | Prilika | Pripremite priliku za dodavanje više podataka o uključenom poslu, ključnim dionicima i konkurenciji. |
| Predloži | Prilika | Pripremite prijedlog i nabavite odobrenje od internog tima za pregled. |
| Zatvaranje | Prilika | Osvojite priliku kako biste okončali posao. |
