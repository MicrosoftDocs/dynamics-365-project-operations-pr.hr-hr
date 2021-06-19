---
title: Planiranje rada u aplikaciji Microsoft Project s pomoću dodatka Project Service
description: U ovoj temi nalaze se informacije o načinu dodavanja, konfiguriranja i uporabe dodatka Microsoft Project za aplikaciju Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0c0ea75d34047f7145466ab427d213c5df27fbed
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014557"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Planiranje rada u aplikaciji Microsoft Project s pomoću dodatka Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] olakšava planiranje projekta, uključujući procjene. Rad možete definirati tako su vrijednosti troškova, napora i prodaje jasne kod slanja konačnog prijedloga.  

Možete instalirati [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] i planirati rad u poznatom okruženju programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Koristite mogućnosti planiranja i upravljanja programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], a zatim ažurirajte projektni plan s pomoću dodatka Project Service Automation.  

> [!IMPORTANT]
> - Kako biste s pomoću značajke platforme SharePoint za upravljanje dokumentima pohranili svoje datoteke [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] za projekte [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], vaš administrator sustava [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] mora uključiti značajku upravljanja dokumentima. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] kompatibilan je samo s programom [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Preuzimanje i instaliranje dodatka  
 Pripremite podatke za prijavu u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Ti su vam podaci potrebni da biste se iz programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] mogli povezati s programom [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Iz centra za preuzimanje preuzmite dodatak za svoju podržanu verziju usluge Project Service, [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) ili [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Odaberite vezu za preuzimanje.  

3.  Kada se preuzimanje završi, odaberite **Da** kako biste instalirali dodatak.  

## <a name="configure-the-add-in"></a>Konfigurirajte dodatak.  

1. Otvorite [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], a zatim odaberite karticu **Project Service**.  

2. Odaberite **Poveži**.  

3. Unesite podatke za prijavu, a zatim odaberite **Prijava**.  

   Sada možete početi koristiti dodatak.  

## <a name="read-from-a-template"></a>Čitanje iz predloška  
 Čitajte iz predloška koji ste izradili u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] i kopirali u program [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] da biste započeli s planiranjem projekta. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Izradi predložak projekta (Project Service Automation)](../psa/create-project-template.md)  

1.  Na kartici **Project Service** odaberite **Čitaj** > **Predložak projekta dodatka Project Service Automation**.  

2.  S popisa odaberite predložak projekta, a zatim odaberite **Otvori**.  

    > [!NOTE]
    >  Prema zadanim postavkama, zadaci koji se kopiraju iz predloška u Projekt postavljeni su kao ručno zakazani.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Dodijeli uloge značajke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] resursima projekta  

1.  Otvorite projekt, a zatim odaberite vrpcu **Zadatak**.  

2. Odaberite izbornik **Ganttov grafikon**, a zatim odaberite **List resursa**.  

3. Na listu resursa odaberite padajući izbornik **Uloga resursa značajke Project Service**, a zatim odaberite ulogu dodatka Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Dodjela resursa u projekt  

1.  Na kartici Project Service, odaberite redak, a zatim odaberite **Pronađi resurse**.  

2.  Na zaslonu **Rezerviraj resurs** odaberite resurs koji želite koristiti za projekt.  

3.  Odaberite **Rezerviraj**, a zatim odaberite **U redu**.  

## <a name="publish-your-project"></a>Objavljivanje projekta  
Kada završite s planiranjem projekta, sljedeći je korak uvoz i objavljivanje projekta u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projekt će se uvesti u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Primijenit će se postupak određivanja cijena i generiranja tima. Otvorite projekt u programu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] da biste vidjeli jesu li generirane stavke tim, procjene projekta i strukturna analiza rada. Sljedeća tablica prikazuje gdje pronaći rezultate.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ganttov dijagram**   | Uvozi na zaslon [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Strukturna analiza rada**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **List resursa** |   Uvozi na zaslon [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Članovi projektnog tima**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Upotreba korištenja**    |    Uvozi na zaslon [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Procjene projekta**.     |

**Uvoz i objava projekta**  
1. Na kartici **Project Service** idite na **Objavi** > **Novi projekt dodatka Project Service Automation**.  

2. U dijaloški okvir **Objavi u novi projekt u značajki Project Service** unesite **Naziv projekta**, a zatim odaberite **Klijent**.  

3. Možete i odabrati stavku **Poveži projektni plan s dodatkom Project Service Automation** kako biste datoteku projektnog plana povezali s dodatkom Project Service Automation.  

4. Odaberite **Objavi**.  

   Povezivanjem datoteke Projekt sa [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] datoteka Projekt postaje glavna datoteka i strukturu analize rada u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] prebacuje u status samo za čitanje.  Da biste mogli mijenjati projektni plan, promjene morate provesti u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i objaviti u obliku ažuriranja u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Uređivanje uvezenog projekta  
 Projektni plan koji je uvezen u dodatak [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] možete mijenjati na sljedeća dva načina:  

- Otvorite glavnu datoteku i uredite je u aplikaciji [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Poništite vezu datoteke i uredite je izravno u značajki Project Service Prema zadanim postavkama, projekt koji je učitan iz programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] zaključan je i moguće ga je uređivati samo u Projektu. Kako biste datoteku uređivali u aplikaciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], morate poništiti njezinu vezu.  

### <a name="edit-in-pn_microsoft_project"></a>Uređujte u [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Na glavnom izborniku idite na **Project Service** > **Projekti**.  

2. Na popisu projekata, otvorite projekt koji ste stvorili u modulu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Na vrpci odaberite **Otvori u programu MS Project**. Tako ćete povezanu glavnu datoteku otvoriti u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Poništi vezu datoteke i uredi je u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Na glavnom izborniku idite na **Project Service** > **Projekti**.  

2. Na popisu projekata, otvorite projekt koji ste stvorili u modulu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Na vrpci odaberite **Poništi vezu s programom MS Project**.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Prijenos datoteke Projekt u sustav SharePoint ili u grupe sustava Office  
 Datoteku Projekt možete prenijeti u SharePoint i pronaći je pod Povezani dokumenti za svoj [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekt.  Administrator mora konfigurirati upravljanje dokumentima platforme SharePoint i uključiti ga za entitet Projekta. 

 Datoteku Projekt možete prenijeti i na [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] ako su postavljene grupe sustava Office.

### <a name="upload-a-file-for-sharepoint"></a>Prijenos datoteke za SharePoint  

1. Na glavnom izborniku idite na **Project Service** > **Prenesi**.  

2. Odaberite **U dokumente dodatka Project Service Automation**.  

3. U dijaloškom okviru **Omogući Otvori u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** odaberite **Da** ili **Ne**.  

   - Ako odaberete **Da**, moći ćete odabrati gumb **Otvori u [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** u dodatku Project Service Automation te pokrenuti [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i prenijeti datoteku Projekt iz biblioteke dokumenata SharePoint.  

   - Ako odaberete **Ne**, veza za **Otvori u modulu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** neće raditi.  

4. Datoteku programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] možete pronaći u odjeljku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod **Dokumenti** za određeni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekt.  

### <a name="upload-a-file-for-office-groups"></a>Prijenos datoteke za grupe sustava Office  

1. Na glavnom izborniku idite na **Project Service** > **Prenesi**.  

2. Odaberite **U dokumente dodatka Project Service Automation**.  

3. U dijaloškom okviru **Omogući Otvori u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** odaberite **Da** ili **Ne**.  

   - Ako odaberete **Da**, moći ćete odabrati gumb **Otvori u [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** u dodatku Project Service Automation te pokrenuti [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i prenijeti datoteku Projekt iz biblioteke dokumenata SharePoint.  

   - Ako odaberete **Ne**, veza za **Otvori u modulu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** neće raditi.  

4. Datoteku programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] možete pronaći u odjeljku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod **Dokumenti** za određeni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekt.  

## <a name="publish--your-project-as-a-template"></a>Objavljivanje projekta u obliku predloška  
 Možete spremiti projekt i ponovo ga upotrijebiti tako da ga spremite u obliku predloška projekta u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Predlošci projekta projektni su planovi koje je moguće ponovno upotrijebiti u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Dodatne informacije potražite u odjeljku [Stvaranje predloška projekta (Project Service Automation)](../psa/create-project-template.md). 

1. Na kartici **Project Service** idite na **Objavi** > **Novi predložak projekta aplikacije Project Service Automation**.  

2. U dijaloški okvir **Objavi u novi predložak projekta aplikacije Project Service** unesite **Naziv predloška projekta**.  

3. Možete i odabrati okvir **Poveži projektni plan s aplikacijom Project Service Automation** kako biste datoteku projekta povezali s modulom [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Odaberite **Objavi**.  

Povezivanjem datoteke Projekt sa [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] datoteka Projekt postaje glavna datoteka i strukturu analize rada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] predloška postavlja u status samo za čitanje.  Da biste mogli mijenjati projektni plan, promjene morate provesti u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i objaviti u obliku ažuriranja u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Čitanje rasporeda učitanih resursa

Kada projekt čitate iz aplikacije Project Service Automation, kalendar resursa nije sinkroniziran s klijentom radne površine. Ako postoje razlike u trajanju zadatka, naporu ili završetku, to je vjerojatno zato što resursi i klijent radne površine nemaju isti kalendar predložaka radnog vremena koji se primjenjuje na projekt.


## <a name="data-synchronization"></a>Sinkronizacija podataka
Tablice u ovom odjeljku pružaju informacije o sinkronizaciji podataka entiteta između aplikacije Project Service Automation i dodatka radne površine Microsoft Project.

### <a name="project-task-entity-table"></a>Tablica entiteta Projektni Zadatak
U sljedećoj tablici opisuje se način sinkronizacije podataka entiteta Projektni zadatak između aplikacije Project Service Automation i dodatka radne površine Microsoft Project.

| **Entitet** | **Polje** | **Microsoft Project prema aplikaciji Project Service Automation** | **Project Service Automation prema aplikaciji Microsoft Project** |
| --- | --- | --- | --- |
| Zadatak projekta | Krajnji rok | Synchronized | Nije sinkronizirano |
| Zadatak projekta | Procijenjeni rad | Synchronized | Nije sinkronizirano |
| Zadatak projekta | ID klijenta aplikacije MS Project | Synchronized | Nije sinkronizirano |
| Zadatak projekta | Nadređeni zadatak | Synchronized | Nije sinkronizirano |
| Zadatak projekta | Project | Synchronized | Nije sinkronizirano |
| Zadatak projekta | Projektni zadatak | Synchronized | Nije sinkronizirano |
| Zadatak projekta | Naziv projektnog zadatka | Synchronized | Nije sinkronizirano |
| Zadatak projekta | Jedinica za resurse (zastarjelo u verziji 3.0) | Synchronized | Nije sinkronizirano |
| Zadatak projekta | Zakazano trajanje | Synchronized | Nije sinkronizirano |
| Zadatak projekta | Datum početka | Synchronized | Nije sinkronizirano |
| Zadatak projekta | ID SAR-a | Synchronized | Nije sinkronizirano |

### <a name="team-member-entity-table"></a>Tablica entiteta člana tima
Sljedeća tablica opisuje način sinkronizacije podataka entiteta Član tima između aplikacije Project Service Automation i dodatka radne površine Microsoft Project

| **Entitet** | **Polje** | **Microsoft Project prema aplikaciji Project Service Automation** | **Project Service Automation prema aplikaciji Microsoft Project** |
| --- | --- | --- | --- |
| Član tima | ID klijenta aplikacije MS Project | Synchronized | Nije sinkronizirano |
| Član tima | Naziv položaja | Synchronized | Nije sinkronizirano |
| Član tima | projekt | Synchronized | Synchronized |
| Član tima | Projektni tim | Synchronized | Synchronized |
| Član tima | Jedinica za resurse | Nije sinkronizirano | Synchronized |
| Član tima | Uloga | Nije sinkronizirano | Synchronized |
| Član tima | Radni sati | Nije sinkronizirano | Nije sinkronizirano |

### <a name="resource-assignment-entity-table"></a>Tablica entiteta Dodjela resursa
Sljedeća tablica opisuje način sinkronizacije podataka entiteta Dodjela resursa između aplikacije Project Service Automation i dodatka radne površine Microsoft Project

| **Entitet** | **Polje** | **Microsoft Project prema aplikaciji Project Service Automation** | **Project Service Automation prema aplikaciji Microsoft Project** |
| --- | --- | --- | --- |
| Dodjela resursa | Od datuma | Synchronized | Nije sinkronizirano |
| Dodjela resursa | h | Synchronized | Nije sinkronizirano |
| Dodjela resursa | ID klijenta aplikacije MS Project | Synchronized | Nije sinkronizirano |
| Dodjela resursa | Planirani rad | Synchronized | Nije sinkronizirano |
| Dodjela resursa | Project | Synchronized | Nije sinkronizirano |
| Dodjela resursa | Projektni tim | Synchronized | Nije sinkronizirano |
| Dodjela resursa | Dodjela resursa | Synchronized | Nije sinkronizirano |
| Dodjela resursa | Zadatak | Synchronized | Nije sinkronizirano |
| Dodjela resursa | Do danas | Synchronized | Nije sinkronizirano |

### <a name="project-task-dependencies-entity-table"></a>Tablica entiteta Ovisnosti projektnog zadatka
Sljedeća tablica opisuje način sinkronizacije podataka entiteta Ovisnosti projektnog zadatka između aplikacije Project Service Automation i dodatka radne površine Microsoft Project

| **Entitet** | **Polje** | **Microsoft Project prema aplikaciji Project Service Automation** | **Project Service Automation prema aplikaciji Microsoft Project** |
| --- | --- | --- | --- |
| Ovisnosti projektnih zadataka | Ovisnost projektnog zadatka | Synchronized | Nije sinkronizirano |
| Ovisnosti projektnih zadataka | Vrsta veze | Synchronized | Nije sinkronizirano |
| Ovisnosti projektnih zadataka | Prethodni zadatak | Synchronized | Nije sinkronizirano |
| Ovisnosti projektnih zadataka | Project | Synchronized | Nije sinkronizirano |
| Ovisnosti projektnih zadataka | Sljedeći zadatak | Synchronized | Nije sinkronizirano |

### <a name="additional-resources"></a>Dodatni resursi
 [Vodič voditelja projekta](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]