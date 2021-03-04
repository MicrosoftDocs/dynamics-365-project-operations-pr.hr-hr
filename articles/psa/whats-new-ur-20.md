---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 20, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 20, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147104"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation, izdanje ažuriranja 20, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 20. Ova verzija ima broj međuverzije V 3.10.31.37 i uglavnom je dostupna putem samostalnog ažuriranja u lipnju 2020. godine.

## <a name="update-release-20"></a>Izdanje ažuriranja 20

### <a name="bug-fixes"></a>Ispravke pogrešaka

**Upravljanje projektom**

Popravljeni su sljedeći problemi:

- Uvoz članova projektnog tima metodom raspodjele koja zahtijeva sate rezultira nejasnom porukom o pogrešci kada je navedeno nula sati.
- Korisnici primaju neispravnu pogrešku kada je u polje **Opis** unesen maksimalni broj znakova za projektni zadatak.
- Stranica **Preuzimanje dodataka Microsoft Dynamics 365 Project Service Automation** preusmjerava se na stranicu za preuzimanje na engleskom jeziku kada su postavke jezika korisnika postavljene na japanski jezik.
- Kada se dogodi pogreška na poslužitelju, oznaka za sinkronizaciju na kartici **Raspored** obrasca **Projekti** ponekad nedostaje.
- Suvišna ažuriranja zadatka šalju se poslužitelju kada je zadatak izmijenjen.

**Sales**

Popravljeni su sljedeći problemi:

- Ako na obrascu **Ugovor** dvaput kliknite mogućnost **Stvori fakturu**, stvaraju se dvije fakture za jedan zapis o stvarnim podacima.
- U programu Internet Explorer 11 korisnici ne mogu stvoriti unose troškova.
- Poništavanje troška i nenaplaćenih stvarnih podataka o prodaji nisu povezani.
- Gumb **Osvježi stvarne podatke** na obrascu **Projekt** ne osvježava **Stvarne sate zadatka**.
- Dodatak **PreValidateProjectTeamMemberCreate** može stvoriti duplicirane generičke resurse koji se mogu rezervirati kad je atribut **msdyn_isgenericresourceprojectscoped** postavljen na **netočno**.
- **Ponovni izračun** briše zaračunate troškove pojedinosti retka ponude koji se temelje na proizvodima i retka ugovora.
- U specifičnim scenarijima, dodatak **PostEstimateLineUpdate** prikazuje pogrešku iznimke prazne reference.
- Trajanje vremenske faze na **Grafikonu analize profitabilnosti** ne odgovara trajanju troškova u pojedinostima retka ponude s fiksnom cijenom.
- Vrijednosti jedinica i grupe jedinica ne postavljaju se ispravno za kategorije troškova na obrascima **Pojedinosti retka ugovora** i **Pojedinosti retka ponude**.
- Popisi **Cijena koštanja OrgUnit** dopuštaju preklapanje u efektivnosti datuma.
- Korisnicima nije dopušteno mijenjati **OrgUnit** kada vrsta narudžbe nije zasnovana na radu jer će dovesti do pogreške iznimke prazne reference.
- Pri pokušaju navigacije s obrasca **Pojedinosti retka ponude** natrag na karticu **Ponuda**, obrazac se osvježava i prikazuje karticu **Sažetak**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]