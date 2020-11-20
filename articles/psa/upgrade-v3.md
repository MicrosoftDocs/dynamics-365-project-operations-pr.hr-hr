---
title: Razmatranja nadogradnje – Microsoft Dynamics 365 Project Service Automation verzija 2.x ili 1.x na verziju 3.x
description: Ova tema pruža informacije o razmatranjima koja morate napraviti kada nadograđujete s aplikacije Project Service Automation verzija 2.x ili 1.x na verziju 3.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3c51726f71cfd0d4be98982d6a02268d64a70b91
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121704"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Razmatranja nadogradnje – PSA verzija 2.x ili 1.x na verziju 3.x
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation i Field Service
Aplikacije Dynamics 365 Project Service Automation i Dynamics 365 Field Service upotrebljavaju rješenje Universal Resourcing Scheduling (URS) za planiranje resursa. Ako u svojoj instanci imate obje aplikacije, i Project Service Automation i Field Service, trebali biste planirati nadogradnju oba rješenja na najnoviju verziju (verzija 3.x za Project Service Automation, verzija 8.x za Field Service). Nadogradnja aplikacija Project Service Automation ili Field Service instalirat će najnoviju verziju rješenja URS, što znači da je moguće nedosljedno ponašanje ako se rješenja Project Service Automation i Field Service u istoj instanci ne nadograde na najnoviju verziju.

## <a name="resource-assignments"></a>Dodjele resursa
U aplikaciji Project Service Automation, verzija 2 i verzija 1, dodjele zadataka pohranjene su kao podređeni zadaci (također zadaci redaka) u **Entitet zadatka** i neizravno povezani s entitetom **Dodjela resursa**. Zadatak retka bio je vidljiv u skočnom prozoru dodjele na strukturnoj analizi rada (WBS).

![Zadaci retka na WBS-u u aplikaciji Project Service Automation, verzije 2 i 1](media/upgrade-line-task-01.png)

U verziji 3 aplikacije Project Service Automation promijenila se pozadinska shema dodjele resursa koje je moguće rezervirati za zadatke. Zadatak je retka zastario i postoji izravni odnos 1:1 između zadatka u **Entitetu zadatka** i članu tima u entitetu **Dodjela resursa**. Zadaci koji su dodijeljeni članu projektnog tima sada se pohranjuju izravno u entitet Dodjela resursa.  

Te promjene utječu na nadogradnju svih postojećih projekata koji imaju dodjele resursa za imenovane resurse koji se mogu rezervirati i generičke resurse u projektnom timu. Ova tema pruža razmatranja koja ćete morati uzeti u obzir za svoje projekte kada nadogradite na verziju 3. 

### <a name="tasks-assigned-to-named-resources"></a>Zadaci dodijeljeni imenovanim resursima
Korištenjem pozadinskog entiteta zadatka, zadaci u verziji 2 i verziji 1 omogućili su članovima tima da prikazuju ulogu različitu od njihove zadane definirane uloge. Na primjer, Jasna Filipović kojoj je prema zadanim postavkama dodijeljena uloga upravitelja programa, mogla bi biti dodijeljena zadatku s ulogom razvojnog inženjera. U verziji 3 uloga imenovanog člana tima uvijek je zadana, tako da bilo koji zadatak koji je dodijeljen Jasni Filipović koristi njezinu zadanu ulogu upravitelja programa.

Ako ste resurs dodijelili zadatku izvan njegove zadane uloge u verziji 2 i verziji 1, kada nadogradite, imenovanom će se resursu dodijeliti zadana uloga za sve dodjele zadataka, bez obzira na dodjelu uloga u verziji 2. To će rezultirati razlikama u izračunanim procjenama iz verzije 2 ili verzije 1 na verziju 3 jer se procjene izračunavaju na temelju uloge resursa, a ne dodjele zadatka retka. Na primjer, u verziji 2 dva su zadatka dodijeljena Dragici Čeh. Uloga u zadatku retka za zadatak 1 je razvojni inženjer, a za zadatak 2 upravitelj programa. Dragica Čeh ima zadanu ulogu upravitelja programa.

![Više uloga dodijeljenih jednom resursu](media/upgrade-multiple-roles-02.png)

Budući da se uloge razvojnog inženjera i upravitelja programa razlikuju, procjene troška i prodaje su sljedeće:

![Procjene troškova za uloge resursa](media/upggrade-cost-estimates-03.png)

![Procjene prodaje za uloge resursa](media/upgrade-sales-estimates-04.png)

Kada nadogradite na verziju 3, zadaci retka zamjenjuju se dodjeljivanjem resursa na zadatku člana tima resursa koji je moguće rezervirati. Dodjela će koristiti zadanu ulogu resursa koji je moguće rezervirati. Na sljedećoj je grafici Dragica Čeh koja ima ulogu upravitelja programa resurs.

![Dodjele resursa](media/resource-assignment-v2-05.png)

Budući da se procjene temelje na zadanoj ulozi za resurs, procjene prodaje i troška mogu se promijeniti. Napominjemo da u sljedećoj grafici više ne vidite ulogu **Razvojni inženjer** jer je uloga sada uzeta iz zadane uloge resursa koji je moguće rezervirati.

![Cost estimates for default roles](media/resource-assignment-cost-estimate-06.png)
![Procjene troškova za zadane uloge](media/resource-assignment-sales-estimate-07.png)

Nakon dovršetka nadogradnje možete urediti ulogu člana tima da bude drugačija od one dodijeljene prema zadanim postavkama. Međutim, ako promijenite ulogu članova tima, promijenit će se na svim dodijeljenim zadacima jer članovima tima više nije dopušteno dodijeliti više uloga u verziji 3.

![Ažuriranje uloge resursa](media/resource-role-assignment-08.png)

To vrijedi i za zadatke retka koji su dodijeljeni imenovanim resursima kada promijenite jedinicu tvrtke ili ustanove resursa iz zadane u drugu jedinicu tvrtke ili ustanove. Nakon dovršetka nadogradnje verzije 3, dodjela će koristiti zadanu jedinicu tvrtke ili ustanove resursa umjesto one postavljene u zadatku retka.

### <a name="tasks-assigned-to-generic-resources"></a>Zadaci dodijeljeni generičkim resursima
U verziji 2 i verziji 1 možete postaviti ulogu i jedinicu tvrtke ili ustanove na zadatku, a zatim koristiti značajku **Generiraj tim** za generiranje generičkih resursa na temelju atributa postavljenih na zadatku. U verziji 3 stvorite generičke članove tima s ulogom i jedinicom tvrtke ili ustanove, a zatim dodijelite članove tima zadacima.

U verziji 2 i verziji 1 projekti s generičkim resursima mogu biti u dva stanja ili mješavina obaju na razini zadatka. Na primjer, možete imati sljedeće scenarije:

- Zadaci s ulogama i jedinicama tvrtke ili ustanove su postavljeni, ali nije generirano nijedno pridruženo dodjeljivanje resursa.
- Zadaci s generičkim dodjeljivanjem resursa članovima tima koji su dodijeljeni stvaranjem generičkog resursa pomoću značajke **Generiraj tim**.

Prije nego što započnete nadogradnju, preporučujemo da ponovno generirate tim za svaki projekt koji ima zadatke dodijeljene generičkim resursima ili još nije imao pokrenut postupak generiranja tima.

Za zadatke koji su dodijeljeni generičkim članovima tima koji su generirani pomoću značajke **Generiraj tim**, nadogradnja će ostaviti generički resurs u timu i ostaviti dodjelu tom generičkom članu tima. Preporučujemo da generirate uvjet resursa za generičkog člana tima nakon nadogradnje, ali prije nego što rezervirate ili pošaljete zahtjev za resursima. Time će se očuvati sve dodjele jedinica tvrtke ili ustanove za generičke članove tima koje su različite od projektne ugovorene jedinice tvrtke ili ustanove.

Na primjer, u projektu Projekt Z ugovorena je jedinica tvrtke ili ustanove Contoso US. U planu projekta zadaci testiranja u fazi implementacije dodijeljeni su ulozi tehničkog savjetnika, a dodijeljena je jedinica tvrtke ili ustanove Contoso India.

![Dodjela faze organizacije tvrtke ili ustanove](media/org-unit-assignment-09.png)

Nakon faze implementacije zadatak testiranja integracije dodijeljen je ulozi tehničkog savjetnika, ali tvrtka ili ustanova je postavljena na Contoso US.  

![Dodjela zadatka testiranja integracije tvrtke ili ustanove](media/org-unit-generate-team-10.png)

Kada generirate tim za projekt, dva generička člana tima stvaraju se zbog različitih jedinica tvrtke ili ustanove na zadacima. Tehničkom savjetniku 1 dodijelit će se zadaci Contoso India, a tehnički će savjetnik 2 imati zadatke Contoso USA.  

![Generirani generički članovi tima](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> U verziji 2 i verziji 1 aplikacije Project Service Automation član tima ne drži jedinicu tvrtke ili ustanove koja se održava na zadatku retka.

![Verzije 2 i 1 zadataka retka u aplikaciji Project Service Automation](media/line-tasks-12.png)

Jedinicu tvrtke ili ustanove možete vidjeti u prikazu procjena. 

![Procjene jedinice tvrtke ili ustanove](media/org-unit-estimates-view-13.png)
 
Kada se nadogradnja dovrši, jedinica tvrtke ili ustanove u zadatku retka koja odgovara generičkom članu tima dodaje se generičkom članu tima, a zadatak retka se uklanja. Stoga preporučujemo da prije nadogradnje generirate ili ponovno generirate tim na svakom projektu koji sadrži generičke resurse.

Za zadatke koji su dodijeljeni ulozi s jedinicom tvrtke ili ustanove koja se razlikuje od jedinice tvrtke ili ustanove ugovorenog projekta, a tim nije generiran, nadogradnja će stvoriti generičkog člana tima za ulogu, ali će koristiti ugovorenu jedinicu projekta za članove tima jedinice tvrtke ili ustanove. Pozivajući se na primjer s projektom Z, to znači da je ugovorena jedinica tvrtke ili ustanove Contoso SAD i zadaci testiranja plana projekta u fazi implementacije dodijelila ulogu tehničkog savjetnika s jedinicom tvrtke ili ustanove dodijeljene Contoso India. Zadatak testiranja integracije koji je dovršen nakon faze implementacije dodijeljen je ulozi tehničkog savjetnika. Jedinica tvrtke ili ustanove je Contoso US i tim nije generiran. Nadogradnja će stvoriti jednog generičkog člana tima, tehničkog savjetnika koji ima dodijeljene sate svih triju zadataka i jedinicu tvrtke ili ustanove Contoso US, projektu ugovorenu jedinicu tvrtke ili ustanove.   
 
Promjena zadanih postavki različitih resursa u jedinicama tvrtke ili ustanove članova tima koji se nije generirao razlog je što preporučujemo da generirate ili ponovno generirate tim na svakom projektu koji sadrži generičke resurse prije nadogradnje tako da se dodjele jedinica tvrtke ili ustanove ne izgube.

