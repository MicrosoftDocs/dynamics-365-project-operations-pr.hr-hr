---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 38, V3
description: U ovom članku navode se značajke i popravci koji su dostupni u aplikaciji Microsoft Dynamics 365 Project Service Automation, izdanje ažuriranja 38, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915176"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovom članku navode se značajke i ispravci koji su novi ili izmijenjeni u aplikaciji Project Service Automation, izdanje ažuriranja 38, V3. Ova verzija ima broj izrade V3.10.59.117 i općenito je dostupna putem samostalnog ažuriranja u prosincu 2021.

## <a name="update-release-38"></a>Izdanje ažuriranja 38

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.

**Vrijeme i trošak**

- Iznimka se događa kada duljina dnevnika skupa odobrenja premašuje 100.000 zapisa.
- Korisnici ne mogu pristupiti rešetci **Unos vremena** s glavne stranice **Unos vremena**.
- Dijaloški okvir **Unos vremena** ne prikazuje nikakav tekst kada nijedna stavka nije prihvatljiva za uvoz.
- Korisnici mogu kreirati skupove odobrenja ako je polje **Status cilja** postavljeno na **Nepoznato**.

**Upravljanje projektom**

- Obrisi nisu ispravno prikazani u dodjelama resursa za UTC(+09:30) i UTC(+10:00) kada počne ljetno računanje vremena.
- Polje **Dodatni stupac** za strukturne analize rada skriveno je u nekim lokalitetima.
- Birač datuma za kontrolu kalendara u rešetci **Projektni zadatak** nije ispravno lokaliziran za kineski.

**Prodaje**

- Vrijednosti **Performanse ugovora** i **Stvarni trošak projekta** ne podudaraju se kada resursi koji se mogu rezervirati i koji imaju različite ugovorne jedinice i valute pošalju unose vremena.
- Prilagođeni tijek rada za automatsku potvrdu faktura ne uspijeva kada se fakture uvezu kao upravljano rješenje. Prikazuje se sljedeća poruka: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Poruka: Nevažeći status fakture."
- Kada je odabran **Korijen** kao opcija sumiranja, a projekt ima procjene iz mješavine klasa transakcija (na primjer, kombinacija procjena vremena, troškova i materijala), sustav sumira sve klase transakcija kao jedan redak naknade.
- U scenarijima u kojima se redak troškova dodaje prije povezivanja retka ugovora s projektom, točna cijena nije unesena kao zadana vrijednost u polju **Ažuriraj cijenu**.
- Negativni iznosi prodaje nisu dopušteni u entitetima **Projekt** i **Zadatak**.
