---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 14, V3
description: Ova tema pruža informacije o novostima u aplikaciji Project Service Automation, izdanje ažuriranja 14, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 00ce5c68b1141c88671f0534f7500bf0d7eebd8e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073346"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation, izdanje ažuriranja 14, V3
Zadovoljstvo nam je najaviti najnovije ažuriranje za aplikaciju Dynamics 365 Project Service Automation (PSA). Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite Centar za administratore sustava Dynamics 365 na mreži i idite na stranicu s rješenjima kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji PSA V3, izdanje ažuriranja 14. Broj izrade ove verzije jest V3.10.4.21, a ona je dostupna na sljedećem rasporedu:

- **Opća dostupnost (samostalno ažuriranje):** siječanj 2020.
- **Automatsko ažuriranje:** veljača 2020.

## <a name="update-release-14"></a>Izdanje ažuriranja 14

### <a name="enhancements"></a>Poboljšanja

- Sales

     - Prilagođene vrijednosti polja iz mogućnosti **Pojedinosti retka ponude** kopiraju se u mogućnost **Pojedinosti retka ugovora o projektu** kada se ponuda ažurirala na mogućnost **Zatvorena kao ostvarena**.
     - Potvrđeni projekti mogu biti **Zatvoreni kao izgubljeni**.

- Upravljanje resursima

     - Kada produžite rezervacije, od korisnika će se zatražiti s pomoću dijaloškog okvira za potvrdu da sažmu rezultate rezervacija i osiguraju vezu do mogućnosti Održavanje rezervacija.


### <a name="bug-fixes"></a>Ispravke pogrešaka

- Vrijeme i trošak

     - Popravljeno: Poboljšano korisničko iskustvo kada korisnik nije odabrao nijednu stavku koju treba ispraviti.

- Upravljanje resursima

     - Popravljeno: Višekratna rezervacija resursa preplavljuje ime resursa koji se može rezervirati.

- Sales

     - Popravljeno: Ukupna prodajna cijena se ne izračunava sve dok korisnik također ne unese cijenu koštanja procijenjenih troškova projekta.
     - Popravljano: Zatvaranje ponude kao **Ostvarena** ne uspijeva ako povezani ugovorni za projekt nije u stanju **Skice**.
