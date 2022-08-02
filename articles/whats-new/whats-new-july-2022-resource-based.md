---
title: Novosti u srpnju 2022. – Project Operations za scenarije koji se temelje na resursu / bez zaliha
description: U ovom se članku nalaze informacije o ažuriranjima kvalitete koja su dostupna u izdanju microsofta Dynamics 365 Project Operations za scenarije temeljene na resursima/neuskladcima u srpnju 2022.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183880"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u srpnju 2022. – Project Operations za scenarije koji se temelje na resursu / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ovaj se članak odnosi na sljedeće komponente i verzije programa Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji okruženja Dataverse 4.44.0.22
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

U ovom izdanju nema ažuriranja za karte s dvostrukim pisanjem aplikacije Project Operations. Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](../environment/resource-dual-write-maps.md).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablica dok ažurirate rješenje za Project Operations Dataverse i verziju rješenja za financije. Neke značajke i mogućnosti možda neće ispravno raditi ako najnovija verzija karte nije aktivirana. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom pokretanja karte, slijedite upute u [odjeljku Nedostajući problemi sa stupcima tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u vodiču za otklanjanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Implementacija i konfiguracija | 2761472 | Obrađena je pogreška instalacije operacija projekta. |
| Naplata i određivanje cijene | 2746940 | Naziv retka podugovaranja trebao bi imati maksimalnu duljinu od 100 znakova. |
| Naplata i određivanje cijene | 2739162 | Korisnici moraju moći vidjeti gumbe vrpce u stvarnom prikazu rešetke. |
| Planiranje i praćenje projekta | 2730318 | Ažurirana provjera valjanosti za nepodržane znakove u predmetu projekta. |
| Naplata i određivanje cijene | 2705361 | Stvarni iznosi prodaje naplaćeni ključnom etakom moraju biti uključeni u polja za praćenje projekata. |
| Naplata i određivanje cijene | 2675880 | Spriječite povezivanje projekta s retkom ugovora koji se ne temelji na radu. |
| Naplata i određivanje cijene | 2664396 | Ako je cjenik ponude spremljen bez ponude, mora postojati pogreška koja kaže da ponuda ne može biti prazna. |
| Naplata i određivanje cijene | 2184019 | Kartica Naplata **temeljena na zadacima ne bi trebala biti prikazana** za projekte koji nemaju ugovor o potpori ili ponudu. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u financijama

Informacije o ispravcima pogrešaka obuhvaćenima ovim ažuriranjem potražite u Microsoft Dynamics članku iz baze podataka o životu (LCS) i pogledajte članak iz [baze znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Značajke uključene prema zadanim postavkama u nadolazećem izdanju

U sljedećoj su tablici navedene značajke koje su prema zadanim postavkama uključene u verziji 10.0.29. Većina značajki koje su automatski uključene mogu se isključiti u [upravljanju značajkama](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Ubuduće bi se neke značajke koje su automatski uključene mogle ukloniti iz upravljanja značajkama i postati obvezne. Ova promjena osigurava da korisnici koriste trenutnu funkcionalnost kako bi se poboljšanja mogla nadovezati na trenutnu funkcionalnost kako se dodaju. Značajke se nikada neće automatski omogućiti za manje od godinu dana, osim ako se utvrdi da su bitne.

| Naziv značajke | Omogući datum | Dodana značajka | Stanje značajke | Modul |
| --- | --- | --- |--- |--- |
| Omogući prilagodbu transakcije sata na temelju promjene u dodjeli pravila financiranja | 16. rujna 2022. | 7. listopada 2020. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Značajka storniranja fakture za akontaciju/pretplatu na narudžbenicu za projekt | 16. rujna 2022. | 6. listopada 2021. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Brisanje redaka prijedloga fakture prilikom korištenja operacija projekta za scenarije temeljene na resursima/neutemeljenim scenarijima | 16. rujna 2022. | 6. listopada 2021. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Prilagodba računovodstva za proknjiženu projektnu transakciju | 16. rujna 2022. | 10. svibnja 2020. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Omogući zadanu postavu računovodstva za projekt | 16. rujna 2022. | 19. veljače 2020. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Omogući više redaka ugovora za projekt | 16. rujna 2022. | 29. lipnja 2020. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Neka temeljnice paketa Project Hour budu samo za čitanje ako trenutni status odobrenja ne dopušta uređivanje | 16. rujna 2022. | 6. listopada 2021. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Omogućivanje sinkroniziranja redaka prodaje iz redaka nabave prilikom ažuriranja redaka nabave i uključivanja parametra upravljanja promjenom narudžbenice | 16. rujna 2022. | 7. listopada 2020. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Omogući projektne operacije na Dynamics 365 Customer Engagement | 16. rujna 2022. | 29. lipnja 2020. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |
| Značajka poništenja ispravka transakcije projekta | 16. rujna 2022. | 13. srpnja 2020. | Uključeno prema zadanim postavkama | Upravljanje projektom i računovodstvo |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Značajke koje postaju obvezne u nadolazećem izdanju

U sljedećoj su tablici navedene značajke koje su obavezne od verzije 10.0.29 nadalje.

| Naziv značajke | Omogući datum | Dodana značajka | Stanje značajke | Modul |
| --- | --- | --- | --- | --- |
| Izračunajte predanu vrijednost na izvor financiranja bez zaokruživanja tečaja | 16. rujna 2022. | 14. lipnja 2020. | Obvezno | Upravljanje projektom i računovodstvo |
| Omogući knjiženje prilagođavanja projekta s istim računom analitike kao i izvorna transakcija | 16. rujna 2022. | 14. lipnja 2020. | Obvezno | Upravljanje projektom i računovodstvo |
| Pojedinosti o iznosu dodijeljenog ugovora o projektu | 16. rujna 2022. | 31. kolovoza 2019. | Obvezno | Upravljanje projektom i računovodstvo |
| Omogući sortiranje po resursu tijekom izrade prijedloga fakture za projekt | 16. rujna 2022. | 31. kolovoza 2019. | Obvezno | Upravljanje projektom i računovodstvo |
