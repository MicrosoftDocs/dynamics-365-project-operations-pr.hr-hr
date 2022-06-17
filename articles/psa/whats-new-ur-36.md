---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 36, V3
description: U ovom se članku navode značajke i popravci dostupni u Microsoft Dynamics 365 Project Service Automation ažuriranju izdanja 36, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a8942713109075da2503c9d22d40b6ac95ae00be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924973"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovom se članku navode značajke i popravci koji su novi ili promijenjeni za izdanje ažuriranja automatizacije usluga project servicea 36, V3. Broj izrade ove verzije jest V3.10.57.152, a ona je uglavnom dostupna putem samostalnog ažuriranja u listopadu 2021.

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



