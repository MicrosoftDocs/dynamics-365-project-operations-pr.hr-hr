---
title: Novosti u aplikaciji Project Service Automation, izdanje ažuriranja 14, V3
description: Ova tema pruža informacije o novostima u aplikaciji Project Service Automation, izdanje ažuriranja 14, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750123"
---
# <a name="project-service-automation-v3-update-release-14"></a>Project Service Automation V3, izdanje ažuriranja 14
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

