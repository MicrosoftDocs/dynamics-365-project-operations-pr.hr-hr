---
title: Novosti u srpnju 2022. – Project Operations za scenarije koji se temelje na resursu / bez zaliha
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju aplikacije Microsoft Dynamics 365 Project Operations iz srpnja 2022. za scenarije koji se temelje na resursu / bez zaliha.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403942"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u srpnju 2022. – Project Operations za scenarije koji se temelje na resursu / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.44.0.22
- Upravljanje projektima i računovodstvo u verziji 10.0.28 okruženja aplikacije Dynamics 365 Finance

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

U ovom izdanju nema ažuriranja za karte s dvostrukim pisanjem aplikacije Project Operations. Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](../environment/resource-dual-write-maps.md).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablice dok ažurirate svoje rješenje Project Operations Dataverse i verziju rješenja Financija. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem nedostatka stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Implementacija i konfiguracija | 2761472 | Obrađena je pogreška instalacije Project Operations. |
| Naplata i određivanje cijene | 2746940 | Naziv retka podugovora treba imati najviše 100 znakova. |
| Naplata i određivanje cijene | 2739162 | Korisnici moraju moći vidjeti gumbe na vrpci u prikazu mreže stvarnih vrijednosti. |
| Planiranje i praćenje projekta | 2730318 | Ažurirana provjera nepodržanih znakova u predmetu projekta. |
| Naplata i određivanje cijene | 2705361 | Stvarne vrijednosti ključne fakturirane prodaje moraju biti uključene u polja za praćenje projekta. |
| Naplata i određivanje cijene | 2675880 | Spriječite povezivanje projekta s retkom ugovora koji se ne temelji na poslu. |
| Naplata i određivanje cijene | 2664396 | Ako je cjenik ponude spremljen bez ponude, mora postojati greška koja navodi da ponuda ne može biti prazna. |
| Naplata i određivanje cijene | 2184019 | Kartica **Naplata na temelju zadataka** ne bi trebala biti prikazana za projekte koji nemaju prateći ugovor ili ponudu. |
| Vrijeme i trošak | 2754459 | Kada je ponavljajući tok oblaka za zakazivanje neaktivan, prikaži banner i zaobiđi asinkronu obradu. |
| Naplata i određivanje cijene | 2724391 | Pogrešna iznimka javlja se kada pravilu o podijeljenoj naplati ugovora o projektu nedostaje vrijednost korisnika. |
| Naplata i određivanje cijene | 2708638 | Zapis nije pronađen tijekom pretraživanja s pomoću pretraživanja mreže u Upotrebama materijala i Odobrenjima za upotrebu materijala.|
| Naplata i određivanje cijene | 2686977 | Spriječite provjeru valjanosti retka fakture tijekom izrade fakture. |
| Naplata i određivanje cijene | 2683032 | Kopiranje naplativih uloga i kategorija ne prelazi 5000 zapisa.|
| Naplata i određivanje cijene | 2673363 | % potrošnje troškova na projektu oštećen je kada za projekt postoje procjene i stvarne vrijednosti napora i troškova. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektom i računovodstvo u aplikaciji Finance

Za informacije o ispravcima uključenima u ovo ažuriranje prijavite se na platformu Microsoft Dynamics Lifecycle Services (LCS) i pogledajte [članak iz baze znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Značajke uključene prema zadanim postavkama u nadolazećem izdanju

Sljedeća tablica navodi značajke koje su uključene prema zadanim postavkama u verziji 10.0.29. Većina značajki koje su automatski uključene može se isključiti u [Upravljanju značajkama](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). U budućnosti bi se neke značajke koje su automatski uključene mogle ukloniti iz Upravljanja značajkama i postati obavezne. Ova promjena osigurava da korisnici koriste trenutačnu funkcionalnost, tako da se poboljšanja mogu nadograđivati na trenutačnu funkcionalnost kako se dodaju. Značajke nikada neće biti automatski omogućene za manje od godinu dana, osim ako se ne utvrdi da su bitne.

| Naziv značajke | Omogući datum | Dodana značajka | Stanje značajke | Modul |
| --- | --- | --- |--- |--- |
| Omogućite prilagodbu transakcije sata na temelju promjene u dodjeli pravila financiranja | 16. rujna 2022. | 7. listopada 2020. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Značajka storniranja fakture s pretplatom narudžbenice za projekt | 16. rujna 2022. | 6. listopada 2021. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Izbriši retke prijedloga fakture pri korištenju aplikacije Project Operations za scenarije koji se temelje na resursima / bez zaliha | 16. rujna 2022. | 6. listopada 2021. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Prilagodite računovodstvo na knjiženoj transakciji projekta | 16. rujna 2022. | 10. svibnja 2020. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Omogućite zadane postavke računovodstva za projekt | 16. rujna 2022. | 19. veljače 2020. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Omogući više redaka ugovora za projekt | 16. rujna 2022. | 29. lipnja 2020. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Učinite dnevnike Project Hour samo za čitanje ako trenutačni status odobrenja ne dopušta uređivanje | 16. rujna 2022. | 6. listopada 2021. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Omogućite sinkronizaciju redaka prodaje iz redaka nabave kad se reci nabave ažuriraju i kad je uključen parametar upravljanja promjenama narudžbenice | 16. rujna 2022. | 7. listopada 2020. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Omogućite Project Operations na Dynamics 365 Customer Engagement | 16. rujna 2022. | 29. lipnja 2020. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Značajka korekcije storniranja projektne transakcije | 16. rujna 2022. | 13. srpnja 2020. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Značajke koje postaju obavezne u nadolazećem izdanju

Sljedeća tablica navodi značajke koje su obvezne od verzije 10.0.29 nadalje.

| Naziv značajke | Omogući datum | Dodana značajka | Stanje značajke | Modul |
| --- | --- | --- | --- | --- |
| Izračunajte dodijeljenu vrijednost na izvoru financiranja bez zaokruživanja tečaja | 16. rujna 2022. | 14. lipnja 2020. | Obvezno | Upravljanje projektom i računovodstvo |
| Omogućite knjiženje prilagodbe projekta s istim računom glavne knjige kao izvorna transakcija | 16. rujna 2022. | 14. lipnja 2020. | Obvezno | Upravljanje projektom i računovodstvo |
| Pojedinosti o ugovorenom iznosu za ugovor o projektu | 16. rujna 2022. | 31. kolovoza 2019. | Obvezno | Upravljanje projektom i računovodstvo |
| Omogućite sortiranje po resursu tijekom izrade prijedloga fakture projekta | 16. rujna 2022. | 31. kolovoza 2019. | Obvezno | Upravljanje projektom i računovodstvo |
