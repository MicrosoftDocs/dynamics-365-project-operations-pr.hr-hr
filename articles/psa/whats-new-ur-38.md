---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 38, V3
description: U ovoj se temi navode značajke i popravci koji su dostupni u ažuriranom izdanju 38, V3, sustava Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: 1e5175b12c9e06962888bf09c8e07119b9505dda
ms.sourcegitcommit: 2aba2082d50b20b596ee86735045644cd647c2b0
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/08/2021
ms.locfileid: "7901506"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj se temi navode značajke i ispravke koje su nove ili promijenjene u 38. izdanju ažuriranja aplikacije Project Service Automation, V3. Ova verzija ima broj izrade V3.10.59.117 i općenito je dostupna putem samostalnog ažuriranja u prosincu 2021.

## <a name="update-release-38"></a>Izdanje ažuriranja 38

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.

**Vrijeme i trošak**

- Iznimka se događa kada duljina zapisnika skupa odobravanja prelazi 100.000 zapisa.
- Korisnici ne mogu pristupiti **rešetki Unos vremena** s **glavne stranice Unos** vremena.
- Dijaloški **okvir Uvoz unosa vremena** ne prikazuje tekst kada nijedna stavka ne ispunjava uvjete za uvoz.
- Korisnici mogu kreirati skupove odobravanja u kojima **je polje Ciljni status** postavljeno na **Nepoznato**.

**Upravljanje projektom**

- Konture se ne prikazuju ispravno u dodjelama resursa za UTC(+09:30) i UTC(+10:00) kada započne ljetno računanje vremena.
- **Polje Dodatni stupac za** strukture raščlambe rada skriveno je u nekim regionalnim shemama.
- Birač datuma za kontrolu kalendara u **rešetki projektnog** zadatka nije ispravno lokaliziran za kineski.

**Prodaje**

- **Vrijednosti izvedbe ugovora** i **stvarnog troška projekta** ne podudaraju se kada resursi koji se mogu rezervirati i koji imaju različite ugovorne jedinice i valute pošalju stavke vremena.
- Prilagođeni tijek rada za automatsku potvrdu faktura ne uspijeva kada se fakture uvoze kao upravljano rješenje. Prikazana je sljedeća poruka: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Status fakture nije valjan."
- Kada **je Root odabran kao opcija** sažimanja, a projekt ima procjene iz mješavine kategorija transakcija (na primjer, kombinacija vremena, troškova i materijalnih procjena), sustav sažima različite kategorije transakcija kao jednu liniju naknada.
- U scenarijima u kojima se redak troška dodaje prije povezivanja retka ugovora s projektom, ispravne cijene ne unose se kao zadana vrijednost u **polje Cijena** ažuriranja.
- Negativni iznosi prodaje nisu dopušteni u **entitetima Projekta** i **Zadatka**.
