---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 43, V3
description: U ovom se članku navode značajke i popravci dostupni u Microsoft Dynamics 365 Project Service Automation ažuriranju izdanja 43, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: b12cfda08f1ea1fc441782003130be445a437f7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915299"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 43, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilan je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovom se članku navode značajke i popravci koji su novi ili promijenjeni za izdanje ažuriranja automatizacije usluga project servicea 43, V3. Ova verzija ima broj međuverzije V3.10.74.200 i uglavnom je dostupna putem samostalnog ažuriranja u svibnju 2022. godine.

## <a name="update-release-43"></a>Izdanje ažuriranja 43

### <a name="bug-fixes"></a>Ispravke pogrešaka

Popravljeni su sljedeći problemi.


**Vrijeme i trošak**

- Prilikom uvoza vremenskih unosa iz rezervacija ili dodjela resursa ne zadržava se upućivanje na povezani resurs koji se može rezervirati.
- Kada se rešetka za unos vremena proširi na cijeli zaslon, navigacija rešetkom pomoću tipke tabulatora ne funkcionira.
- Prilikom slanja vremenske stavke koju je stvorio drugi korisnik, **polje Poslano po** neispravno se popunjava korisnikom koji je stvorio vremenski list.
