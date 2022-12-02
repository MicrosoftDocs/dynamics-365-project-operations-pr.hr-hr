---
title: Razmatranja o nadogradnji za Suvremena odobrenja
description: Ovaj članak pokriva točke koje bi administratori trebali uzeti u obzir kada omogućuju funkcionalnost Suvremena odobrenja.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931735"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Razmatranja o nadogradnji za Suvremena odobrenja 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Kao dio izdanja 1. vala iz travnja 2022., funkcija Suvremena odobrenja bit će omogućena prema zadanim postavkama. Ova funkcionalnost poboljšava pouzdanost logike odobrenja i osigurava utvrđivanje razloga zakazivanja logike odobrenja.

Kao dio ove promjene ažuriraju se statusne promjene za odobrenja projekta. Status se sada izravno mijenja iz **Poslano** u **Odobreno**. **Na čekanju** više nije status za odobrenja. Da biste utvrdili je li odobrenje na čekanju, provjerite je li odobrenje dio skupa odobrenja i pregledajte stanje priloženog skupa odobrenja.

## <a name="before-you-upgrade"></a>Prije nadogradnje

Prije nadogradnje na Suvremena odobrenja provjerite imate li odobrenja na čekanju. Funkcionalnost Suvremena odobrenja ne upotrebljava status **Na čekanju**. Stoga sva odobrenja koja su još uvijek označena kao **Na čekanju** nakon nadogradnje neće biti obrađena.

## <a name="after-you-upgrade"></a>Nakon nadogradnje

Nakon što nadogradite na Suvremena odobrenja, administrator mora potvrditi da je tok oblaka koji obrađuje odobrenja omogućen.

1. Prijavite se na [flow.microsoft.com](https://flow.microsoft.com)
2. U gornjem desnom kutu stranice promijenite svoje okruženje u okruženje koje ste nadogradili.
3. Odaberite **Rješenja** za popis rješenja koja su instalirana u okruženju.
4. Na popisu rješenja odaberite **Project Operations** ili **Project Service**.
5. Promijenite filtar iz **Svi** u **Tok oblaka**.
6. Provjerite je li mogućnost **Project Service – Zakažite skupove odobrenja projekta u ponavljanju** postavljen na **Uključeno**. Ako nije, odaberite tok, a zatim odaberite **Uključi**.
7. Provjerite odvija li se obrada svakih pet minuta pregledom popisa **Poslovi sustava** u području **Postavke**.

## <a name="short-term-rollback"></a>Kratkoročno vraćanje u prethodno stanje

Ako ne možete prihvatiti promjene ili ako naiđete na ozbiljan problem s ovom značajkom, možete se privremeno vratiti na izvorni tok odobrenja izvođenjem sljedećih koraka:
1. Prijavite se u svoje okruženje i provjerite ima li odobrenja na čekanju.
2. Otvorite **Project Service** > **Project parametri**.
3. Odaberite **Kontrola značajki** i zatim odaberite **Suvremena odobrenja** za isključivanje značajke.

## <a name="removing-the-feature-flag"></a>Uklanjanje oznake značajke

U ažuriranju 2. vala iz listopada 2022. mogućnost isključivanja ove značajke bit će uklonjena.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
