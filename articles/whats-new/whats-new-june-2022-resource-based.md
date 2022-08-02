---
title: Novosti u lipnju 2022. – Project Operations za scenarije koji se temelje na resursu / bez zaliha
description: U ovom se članku nalaze informacije o ažuriranjima kvalitete koja su dostupna u microsoftovu izdanju iz Dynamics 365 Project Operations lipnja 2022. za scenarije koji se temelje na resursima/nenaseljenim resursima.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031322"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u lipnju 2022. – Project Operations za scenarije koji se temelje na resursu / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ovaj se članak odnosi na sljedeće komponente i verzije programa Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji okruženja Dataverse 4.43.0.77 ili 4.43.0.119
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

Sljedeća tablica prikazuje karte s dvostrukim pisanjem koje su izmijenjene ili dodane u izdanju Project Operations Lipanj 2022.

| Karta entiteta | Ažurirana verzija | Komentari |
| --- | --- | --- |
| Entitet izvoza fakture dobavljača projekata integracije aplikacije Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Amortizirao je naslijeđeno polje i mapirao na novo polje za praćenje stanja fakture dobavljača. |

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablica dok ažurirate rješenje za Project Operations Dataverse i verziju rješenja za financije. Neke značajke i mogućnosti možda neće ispravno raditi ako najnovija verzija karte nije aktivirana. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom pokretanja karte, slijedite upute u [odjeljku Nedostajući problemi sa stupcima tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u vodiču za otklanjanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Ugovaranje o kooperaciji | 2708885 | Ispravljena je poruka o pogrešci koja se pojavljuje kada korisnik stvori zapis zaglavlja rezervacije resursa koji se može rezervirati, a u kojoj nije ispunjen resurs koji se može rezervirati. |
| Planiranje i praćenje projekta | 2629441 | Ispravio je logiku pokretanja tijeka rada kako bi se spriječila beskonačna petlja prilikom ažuriranja projektnih zadataka. |
| Vrijeme i trošak | 2641209 | Uvoz unosa vremena iz dodjela/rezervacija mora zadržati referencu resursa koja se može rezervirati. |
| Planiranje i praćenje projekta | 2651148 | Zaglavlje projektnog dokumenta mora biti čuvano.|
| Planiranje i praćenje projekta | 2653145 | Dodane su provjere valjanosti kako bi se osiguralo da se ne može stvoriti zapis projekta koji u nazivu ima znakove koji nisu valjani. |
| Vrijeme i trošak | 2654710 | Ispravljeno filtriranje na **stranici Odobrenja**. |
| Naplata i određivanje cijene | 2667805 | Dodane su provjere valjanosti kako bi se spriječilo stvaranje stvarnog iznosa naplaćene prodaje ako ne postoje neplaćene vrijednosti prodaje. |
| Naplata i određivanje cijene | 2668378 | Dodane su provjere valjanosti kako bi se spriječilo dodavanje prilagođene dimenzije određivanja cijena, osim ako se ne ispune logički naziv i naziv polja. |
| Ugovaranje o kooperaciji | 2677485 | Ažurirao je ciljnu verziju redaka fakture dobavljača karte dvostrukog pisanja. |
| Vrijeme i trošak | 2700428 | Poboljšana je logika odobravanja kako bi se osiguralo da se drugi skupovi odobrenja za projekt mogu obraditi čak i ako je jedan od skupova odobrenja zapeo u poslovima sustava. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u financijama

Informacije o ispravcima pogrešaka obuhvaćenima ovim ažuriranjem potražite u Microsoft Dynamics članku iz baze podataka o životu (LCS) i pogledajte članak iz [baze znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
