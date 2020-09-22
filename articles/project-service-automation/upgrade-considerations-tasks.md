---
title: Razmatranja nadogradnje za strukturnu analizu rada
description: Ova tema pruža informacije o nadogradnji strukturne analize rada s Project Service Automation 2.x na 3.x.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750161"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Razmatranja nadogradnje za strukturnu analizu rada
Ova tema pruža informacije o nadogradnji strukturne analize rada s Project Service Automation 2.x na 3.x. Ova tema definira zdravo stanje projekta u Project Service Automation (PSA) koje je potrebno za uspješnu nadogradnju. Postoje i informacije o uobičajenim uvjetima blokiranja koji će uzrokovati neuspjeh nadogradnje. Dodatne informacije o određivanju projektnih zadataka i njihovih funkcija unutar rasporeda projekta potražite u članku [Rasporedi projekata](project-creating.md).

## <a name="key-entities"></a>Ključni entiteti
Za točnu strukturnu analizu rada koja je već napunjena resursima, potrebni su sljedeći entiteti:

- [Projekt](../developer/entities/msdyn_project.md)
- [Projektni tim](../developer/entities/msdyn_projectteam.md)
- [Projektni zadatak](../developer/entities/msdyn_projecttask.md)
- [Dodjele resursa](../developer/entities/msdyn_resourceassignment.md)
- [Ovisnost projektnog zadatka](../developer/entities/msdyn_projecttaskdependency.md)
- [Resursi koje je moguće rezervirati](../developer/entities/bookableresource.md)

Da biste definirali strukturnu analizu rada napunjenu resursima, morate dovršiti sljedeće korake:

1. Stvorite novi projekt. Dodatne informacije o tome kako stvoriti novi projekt potražite u članku [msdyn_project](../developer/entities/msdyn_project.md).
2. Stvorite jedan ili više zadataka. Dodatne informacije o tome kako stvoriti novi zadatak potražite u članku [msdyn_projecttast](../developer/entities/msdyn_projecttask.md).
3. Definirajte ovisnosti zadataka. Dodatne informacije potražite u članku [Ovisnost projektnog zadatka](../developer/entities/msdyn_projecttaskdependency.md).
4. Dodijelite članove projektnih timova projektu. Dodatne informacije potražite u članku [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).
5. Dodijelite članove projektnih timova zadatku. Dodatne informacije potražite u članku [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).

## <a name="project-team-relationships"></a>Odnosi projektnog tima

Da bi se osigurala uspješna nadogradnja, sljedeći se odnosi moraju pravilno održavati:
- Svi članovi tima projektnih timova moraju biti pridruženi resursu koji se može rezervirati.
- Svi članovi tima projektnih timova moraju biti pridruženi istom projektu. 

## <a name="project-task-relationships"></a>Odnosi projektnih zadataka
Da bi se osigurala uspješna nadogradnja, sljedeći se odnosi moraju pravilno održavati:

- Svi povezani zadaci moraju biti pridruženi istom projektu.
- Svaki zadatak retka mora imati nadređeni zadatak.
- Svaki zadatak mora imati nadređeni projekt.

### <a name="valid-conditions"></a>Valjani uvjeti

- Sva trajanja zadatka moraju biti veća ili jednaka (> =) od jednog sata i manja od 1.800,000 minuta (1.250 dana). *
- Svi zadaci moraju imati datum početka ne ranije od 1. 1. 2000. *
- Svi zadaci moraju imati datum početka najkasnije 17 godina od ovog dana. *
- Svi zadaci moraju imati datum početka ranije ili jednak datumu završetka.
- Sve vrste transakcija za klasifikacije (rashodi, materijal, porez i vrijeme) moraju imati vrijednosti za **Zadanu jedinicu** i **Grupu jedinica**.
- Oblike datuma sa slovima treba izbjegavati.

### <a name="potential-mitigation-steps"></a>Mogući koraci ublažavanja
- Upotrijebite mogućnost Napredno pretraživanje kako biste odredili Projektne zadatke koji ne sadrže ID projekta.
- Upotrijebite mogućnost Napredno pretraživanje kako biste odredili Projektne zadatke planiranog trajanja duljeg od > 1.800.000.
- Prije nego što izvršite bilo kakve promjene podataka, trebali biste istražiti sve prilagodbe povezane s entitetom koje su mogle dovesti do lošeg stanja podataka. Ovim bi se prilagodbama trebalo pozabaviti prije nego što nastavite s ažuriranjem koje se odnosi na podatke.
- Za određene zadatke koji su bili izolirani, razmotrite brisanje tih zadataka ako nisu potrebni ili ako bi trebali biti povezani s ispravnim nadređenim projektom.
- Za sve zadatke u kojima je trajanje dulje od 1.250 dana, razmislite o dodavanju više zadataka kako biste prikazali ukupno trajanje, ako je izvedivo.

> [!NOTE]
> Stavke označene zvjezdicom (\*) imaju ograničenja koja postoje zbog činjenice da upravljanje odnosima s klijentima (CRM) podržava samo 7.320 poslova proširenja. Morate ostati ispod ove granice.

## <a name="resource-assignment-relationships"></a>Odnosi dodjele resursa
Da bi se osigurala uspješna nadogradnja, sljedeći se odnosi moraju pravilno održavati:

- Sve Dodjele resursa u strukturnoj analizi rada moraju biti povezane s istim projektom.
- Sve Dodjele resursa u strukturnoj analizi rada moraju biti povezane s članovima projektnog tima u istom projektu.

### <a name="potential-mitigation-steps"></a>Mogući koraci ublažavanja
- Odredite sve zadatke koji izlaze izvan gore opisanih uvjeta.  
- Sve Dodjele resursa koje više nisu valjane treba izbrisati.

## <a name="project-task-dependency-relationships"></a>Ovisni odnosi projektnih zadataka
Da bi se osigurala uspješna nadogradnja, sljedeći se odnosi moraju pravilno održavati:

- Sve ovisnosti projektnih zadataka moraju biti povezane s istim projektom.
- Zadatak ne može imati istu ovisnost koja se spominje više puta.
