---
title: Korištenje dodatka Project Service za planiranje rada u programu Microsoft Project | MicrosoftDocs
description: Ova tema pruža informacije o tome kako dodati, konfigurirati i koristiti dodatak Microsoft Project za Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: ccebf1439f49092b23da5b4fc2ebb4fc484de4dd17c870eea9fe37b00fbb3689
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005292"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Pomoću dodatka Project Service Automation planirajte zadatke u programu Microsoft Project

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] olakšava planiranje projekta, uključujući procjene. Rad možete definirati tako su vrijednosti troškova, napora i prodaje jasne kod slanja konačnog prijedloga.  

 Sada možete instalirati [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] i planirati rad u poznatom okruženju programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Koristite mogućnosti planiranja i upravljanja programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], a zatim ažurirajte projektni plan s pomoću dodatka Project Service Automation.  

> [!IMPORTANT]
> - Kako biste s pomoću značajke platforme SharePoint za upravljanje dokumentima pohranili svoje datoteke [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] za projekte [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], vaš administrator sustava [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] mora uključiti značajku upravljanja dokumentima. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] kompatibilan je samo s programom [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Preuzimanje i instaliranje dodatka  
 Pripremite podatke za prijavu u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Ti su vam podaci potrebni da biste se iz programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] mogli povezati s programom [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Iz centra za preuzimanje preuzmite dodatak za svoju podržanu verziju usluge Project Service, [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) ili [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Kliknite vezu za preuzimanje.  

3.  Kada se preuzimanje završi, kliknite **Da** da biste instalirali dodatak.  

## <a name="configure-the-add-in"></a>Konfigurirajte dodatak.  

1. Otvorite [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], a zatim kliknite karticu **Project Service**.  

2. Kliknite **Poveži**.  

3. Unesite podatke za prijavu, a zatim kliknite **Prijava**.  

   Sada možete početi koristiti dodatak.  

## <a name="read-from-a-template"></a>Čitanje iz predloška  
 Čitajte iz predloška koji ste izradili u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] i kopirali u program [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] da biste započeli s planiranjem projekta. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Izradi predložak projekta (Project Service Automation)](../psa/create-project-template.md)  

1.  Na kartici **Project Service** kliknite **Čitaj** > **Predložak projekta dodatka Project Service Automation**.  

2.  S popisa odaberite predložak projekta, a zatim kliknite **Otvori**.  

    > [!NOTE]
    >  Prema zadanim postavkama, zadaci koji se kopiraju iz predloška u Projekt postavljeni su kao ručno zakazani.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Dodijeli uloge značajke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] resursima projekta  

1.  Otvorite projekt, a zatim kliknite vrpcu **Zadatak**.  

2.  Kliknite izbornik **Ganttov grafikon**, a zatim odaberite **List resursa**.  

3.  Na listu resursa kliknite padajući izbornik **Uloga resursa značajke Project Service**, a zatim odaberite ulogu dodatka Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Dodjela resursa u projekt  

1.  Na kartici Project Service, odaberite redak, a zatim kliknite **Pronađi resurse**.  

2.  Na zaslonu **Rezerviraj resurs** odaberite resurs koji želite koristiti za projekt.  

3.  Kliknite **Rezerviraj**, a zatim **U redu**.  

## <a name="publish-your-project"></a>Objavljivanje projekta  
Kada završite s planiranjem projekta, sljedeći je korak uvoz i objavljivanje projekta u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projekt će se uvesti u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Primijenit će se postupak određivanja cijena i generiranja tima. Otvorite projekt u programu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] da biste vidjeli jesu li generirane stavke tim, procjene projekta i strukturna analiza rada. Sljedeća tablica prikazuje gdje pronaći rezultate:


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ganttov dijagram**   | Uvozi na zaslon [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Strukturna analiza rada**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **List resursa** |   Uvozi na zaslon [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Članovi projektnog tima**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Upotreba korištenja**    |    Uvozi na zaslon [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Procjene projekta**.     |

**Uvoz i objava projekta**  
1. Na kartici **Project Service** kliknite **Objavi** > **Novi projekt dodatka Project Service Automation**.  

2. U dijaloški okvir **Objavi u novi projekt u značajki Project Service** unesite **Naziv projekta**, a zatim odaberite **Klijent**.  

3. Možete i potvrditi okvir **Poveži projektni plan s dodatkom Project Service Automation** da biste datoteku projektnog plana povezali s dodatkom Project Service Automation.  

4. Kliknite **Objavi**.  

   Povezivanjem datoteke Projekt sa [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] datoteka Projekt postaje glavna datoteka i strukturu analize rada u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] prebacuje u status samo za čitanje.  Da biste mogli mijenjati projektni plan, promjene morate provesti u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i objaviti u obliku ažuriranja u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Uređivanje uvezenog projekta  
 Projektni plan koji je uvezen u dodatak [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] možete mijenjati na sljedeća dva načina:  

- Otvorite glavnu datoteku i uredite je u aplikaciji [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Poništite vezu datoteke i uredite je izravno u značajki Project Service Prema zadanim postavkama, projekt koji je učitan iz programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] zaključan je i moguće ga je uređivati samo u Projektu. Kako biste datoteku uređivali u aplikaciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], morate poništiti njezinu vezu.  

### <a name="edit-in-pn_microsoft_project"></a>Uredi u [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Na glavnom izborniku, kliknite **Project Service** > **Projekti**.  

2. Na popisu projekata, otvorite projekt koji ste izradili u [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Na vrpci kliknite **Otvori u programu MS Project**. Tako ćete povezanu glavnu datoteku otvoriti u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Poništi vezu datoteke i uredi je u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Na glavnom izborniku kliknite **Project Service** > **Projekti**.  

2. Na popisu projekata, otvorite projekt koji ste izradili u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Na vrpci kliknite **Poništi vezu s programom MS Project**.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Prijenos datoteke Projekt u sustav SharePoint ili u grupe sustava Office  
 Datoteku Projekt možete prenijeti u SharePoint i pronaći je pod Povezani dokumenti za svoj [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekt.  Administrator mora konfigurirati upravljanje dokumentima platforme SharePoint i uključiti ga za entitet Projekta. 

 Datoteku Projekt možete prenijeti i na [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] ako su postavljene grupe sustava Office.

### <a name="upload-a-file-for-sharepoint"></a>Prijenos datoteke za SharePoint  

1. Na glavnom izborniku kliknite **Project Service** > **Prenesi**.  

2. Odaberite **U dokumente dodatka Project Service Automation**.  

3. U dijaloškom okviru **Omogući značajku Otvori u aplikaciji [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** odaberite **Da** ili **Ne**.  

   - Ako kliknete **Da**, moći ćete odabrati gumb **Otvori u aplikaciji [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** u dodatku Project Service Automation, pokrenuti aplikaciju [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i prenijeti datoteku Projekt iz biblioteke dokumenata platforme SharePoint.  

   - Ako kliknete **Ne**, veza za gumb **Otvori u aplikaciji [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** neće funkcionirati.  

4. Datoteku programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] možete pronaći u odjeljku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod **Dokumenti** za određeni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekt.  

### <a name="upload-a-file-for-office-groups"></a>Prijenos datoteke za grupe sustava Office  

1. Na glavnom izborniku kliknite **Project Service** > **Prenesi**.  

2. Odaberite **U dokumente dodatka Project Service Automation**.  

3. U dijaloškom okviru **Omogući značajku Otvori u aplikaciji [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** odaberite **Da** ili **Ne**.  

   - Ako kliknete **Da**, moći ćete odabrati gumb **Otvori u aplikaciji [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** u dodatku Project Service Automation, pokrenuti aplikaciju [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i prenijeti datoteku Projekt iz biblioteke dokumenata platforme SharePoint.  

   - Ako kliknete **Ne**, veza za gumb **Otvori u aplikaciji [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** neće funkcionirati.  

4. Datoteku programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] možete pronaći u odjeljku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod **Dokumenti** za određeni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekt.  

## <a name="publish--your-project-as-a-template"></a>Objavljivanje projekta u obliku predloška  
 Možete spremiti projekt i ponovo ga upotrijebiti tako da ga spremite u obliku predloška projekta u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Predlošci projekta projektni su planovi koje je moguće ponovno upotrijebiti u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Izradi predložak projekta (Project Service Automation)](../psa/create-project-template.md)  

1. Na kartici **Project Service** kliknite **Objavi** > **Novi predložak projekta dodatka Project Service Automation**.  

2. U dijaloški okvir **Objavi u novi predložak projekta Project Service** unesite **Naziv predloška projekta**.  

3. Po želji, potvrdite okvir **Poveži projektni plan s dodatkom Project Service Automation** kako biste datoteku projektnog plana povezali s aplikacijom [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Kliknite **Objavi**.  

Povezivanjem datoteke Projekt sa [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] datoteka Projekt postaje glavna datoteka i strukturu analize rada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] predloška postavlja u status samo za čitanje.  Da biste mogli mijenjati projektni plan, promjene morate provesti u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i objaviti u obliku ažuriranja u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Čitanje rasporeda učitanih resursa

Kada projekt čitate iz aplikacije Project Service Automation, kalendar resursa nije sinkroniziran s klijentom radne površine. Ako postoje razlike u trajanju zadatka, naporu ili završetku, to je vjerojatno zato što resursi i klijent radne površine nemaju isti kalendar predložaka radnog vremena koji se primjenjuje na projekt.


## <a name="data-synchronization"></a>Sinkronizacija podataka

Sljedeća tablica opisuje kako se podaci sinkroniziraju između aplikacije Project Service Automation i programskog dodatka radne površine Microsoft Project.

| **Entitet** | **Polje** | **Microsoft Project prema aplikaciji Project Service Automation** | **Project Service Automation prema aplikaciji Microsoft Project** |
| --- | --- | --- | --- |
| Zadatak projekta | Krajnji rok | ● | - |
| Zadatak projekta | Procijenjeni rad | ● | - |
| Zadatak projekta | ID klijenta aplikacije MS Project | ● | - |
| Zadatak projekta | Nadređeni zadatak | ● | - |
| Zadatak projekta | Project | ● | - |
| Zadatak projekta | Projektni zadatak | ● | - |
| Zadatak projekta | Naziv projektnog zadatka | ● | - |
| Zadatak projekta | Jedinica za resurse (zastarjelo u verziji 3.0) | ● | - |
| Zadatak projekta | Zakazano trajanje | ● | - |
| Zadatak projekta | Datum početka | ● | - |
| Zadatak projekta | ID SAR-a | ● | - |

| **Entitet** | **Polje** | **Microsoft Project prema aplikaciji Project Service Automation** | **Project Service Automation prema aplikaciji Microsoft Project** |
| --- | --- | --- | --- |
| Član tima | ID klijenta aplikacije MS Project | ● | - |
| Član tima | Naziv položaja | ● | - |
| Član tima | projekt | ● | ● |
| Član tima | Projektni tim | ● | ● |
| Član tima | Jedinica za resurse | - | ● |
| Član tima | Uloga | - | ● |
| Član tima | Radni sati | Nije sinkronizirano | Nije sinkronizirano |

| **Entitet** | **Polje** | **Microsoft Project prema aplikaciji Project Service Automation** | **Project Service Automation prema aplikaciji Microsoft Project** |
| --- | --- | --- | --- |
| Dodjela resursa | Od datuma | ● | - |
| Dodjela resursa | h | ● | - |
| Dodjela resursa | ID klijenta aplikacije MS Project | ● | - |
| Dodjela resursa | Planirani rad | ● | - |
| Dodjela resursa | Project | ● | - |
| Dodjela resursa | Projektni tim | ● | - |
| Dodjela resursa | Dodjela resursa | ● | - |
| Dodjela resursa | Zadatak | ● | - |
| Dodjela resursa | Do danas | ● | - |

| **Entitet** | **Polje** | **Microsoft Project prema aplikaciji Project Service Automation** | **Project Service Automation prema aplikaciji Microsoft Project** |
| --- | --- | --- | --- |
| Ovisnosti projektnih zadataka | Ovisnost projektnog zadatka | ● | - |
| Ovisnosti projektnih zadataka | Vrsta veze | ● | - |
| Ovisnosti projektnih zadataka | Prethodni zadatak | ● | - |
| Ovisnosti projektnih zadataka | Project | ● | - |
| Ovisnosti projektnih zadataka | Sljedeći zadatak | ● | - |

### <a name="see-also"></a>Pogledajte također  
 [Vodič voditelja projekta](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]