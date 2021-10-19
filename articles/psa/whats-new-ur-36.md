---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 36, V3
description: U ovoj se temi navode značajke i popravci koji su dostupni u ažuriranom izdanju 36, V3, sustava Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606734"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj se temi navode značajke i ispravke koje su nove ili promijenjene u 36. izdanju ažuriranja aplikacije Project Service Automation, V3. Broj izrade ove verzije jest V3.10.57.152, a ona je uglavnom dostupna putem samostalnog ažuriranja u listopadu 2021.

## <a name="update-release-36"></a>Izdanje ažuriranja 36

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.

**Općenito**
- Naziv polja **Zadani predložak radnog vremena** na stranici **Parametri projekta** pogrešno je preveden.
- Asinkroni dodaci ne upravljaju ispravno iznimkama povezanima sa stavkom **SharedVariableService**.

**Vrijeme i trošak**
- Kad redci dnevnika nedostaju ili korisnik nema ispravne ovlasti za čitanje redaka dnevnika, dolazi do netočne pogreške pri otkazivanju odobrenja projekta.
- Korisnici ne mogu otkazati odobrenje ako unos troška ili vremena ima više od jednog povezanog odobrenja za projekt.
- **Odsutnost** i **Odmor** pogrešno su prevedeni na kineski jezik u pretraživanju, na stranici **Vremenski unos**.

**Upravljanje resursima**
- Korisnik ne može tražiti resurse u stavci **Pomoćnik za planiranje** kada je način prikaza postavljen na **Dan**, **Tjedan** ili **Mjesec**.
- Generičkim je resursima pogrešno omogućeno da imaju prazne nazive pozicija. 
- Zatvaranje ugovora kao izgubljenog ne otkazuje buduće rezervacije.

**Prodaje**
- Kada okruženje ima veliku količinu proizvoda, smanjuju se performanse u rešetki **Procjena materijala**.
- Tijekom stvaranja projekta iz predloška, valuta projekta nije zadana za ugovornu jedinicu odgovarajućeg voditelja projekta.
- Stvarni iznosi ne poklapaju se uvijek s onim što se odražava na dospjeli projekt tj. iznosi postaju negativni u posebnim scenarijima opoziva.
- Do greške dolazi kada projekt koji je stvoren iz predloška projekta povežete s retkom ugovora.
- Korisnici mogu izbrisati redak ugovora s kontrolnim točkama, **Spremno za fakturiranje** i **Stvorena faktura**. To se ne smije dozvoliti.
- Kada se procjene uvoze iz projekta, naplativost pojedinosti retka ponude nije ispravno postavljena kada je za redak ponude omogućena naplata koja se temelji na zadatku.
- Kada dodate kontrolnu točku za naplatu s fiksnom cijenom, ta se kontrolna točka ne odražava u podrešetki kontrolne točke sve dok se stranica ne osvježi.
- Izuzetak nulte reference generira se kada stvarate ugovor o projektu s nazivom ponude koji je nula.
- Zadaci ručnog načina rada u kojima se valuta projekta razlikuje od valute resursa rezultiraju netočnim procjenama cijene.
- Korisnici ne mogu pozivati transakciju koja je uspješno ispravljena korektivnom fakturom.
- Deaktivirane kategorije transakcija pojavljuju se u rešetki **Procjene troškova**.



