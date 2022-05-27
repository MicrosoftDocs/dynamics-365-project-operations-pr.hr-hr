---
title: Razmatranja nadogradnje za moderna odobrenja
description: Tema pokriva točke koje bi administratori trebali uzeti u obzir kada omogućuju funkcionalnost modernih odobrenja.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578377"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Razmatranja nadogradnje za moderna odobrenja 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U sklopu izdanja vala 1 u travnju 2022. bit će omogućena funkcionalnost modernih odobrenja prema zadanim postavkama. Ova funkcija poboljšava pouzdanost logike odobravanja i osigurava da možete odrediti razlog ako logika odobravanja ne uspije.

Kao dio ove promjene ažuriraju se promjene statusa odobrenja projekta. Status sada ide izravno od **poslanog** na **Odobreno**. **Čekanje** više nije status za odobrenja. Da biste utvrdili je li odobrenje na čekanju, provjerite je li odobrenje dio skupa odobrenja i pregledajte stanje priloženog skupa odobrenja.

## <a name="before-you-upgrade"></a>Prije nadogradnje

Prije nadogradnje na moderna odobrenja provjerite nemate li odobrenja na čekanju. Moderna odobrenja ne koriste status Na **čekanju**. Stoga se sva odobrenja koja su i dalje označena kao **Na čekanju nakon nadogradnje** neće obraditi.

## <a name="after-you-upgrade"></a>Nakon nadogradnje

Nakon nadogradnje na moderna odobrenja administrator mora provjeriti je li omogućen tijek oblaka koji obrađuje odobrenja.

1. Prijava u [flow.microsoft.com](https://flow.microsoft.com)
2. U gornjem desnom kutu stranice prebacite okruženje na okruženje koje ste nadogradili.
3. Odaberite **Rješenja** da biste naveli rješenja instalirana u okruženju.
4. Na popisu rješenja odaberite **Projektne operacije** ili **Projektni servis**.
5. Promijenite filtar iz **Sve** u **Tokove oblaka**.
6. Provjerite je li **mogućnost Project Service – Ponavljajuće zakazivanje skupova odobrenja** projekta postavljena na **Uključeno**. Ako nije, odaberite tijek, a zatim **Uključi**.
7. Provjerite odvija li se obrada svakih pet minuta pregledom **popisa Poslovi** sustava u **području Postavke**.

## <a name="short-term-rollback"></a>Kratkoročni povratak

Ako ne možete iskoristiti promjene ili ako naiđete na ozbiljan problem s ovom značajkom, možete se privremeno vratiti na izvorni tijek odobravanja izvođenjem sljedećih koraka:
1. Prijavite se u svoje okruženje i provjerite nema li odobrenja na čekanju.
2. Otvorite **Postavke** > **parametara** projekta.
3. Odaberite **Kontrola** značajki, a zatim Moderna **odobrenja** da biste isključili značajku.

## <a name="removing-the-feature-flag"></a>Uklanjanje zastavice značajke

U ažuriranju Vala 2 iz listopada 2022. uklonit će se mogućnost isključivanja ove značajke.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
