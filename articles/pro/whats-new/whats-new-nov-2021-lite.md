---
title: Što je novo u studenome 2021. – Osnovna implementacija aplikacije Project Operations
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju osnovne implementacije aplikacije Project Operations za studeni 2021.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 947e7f6183ddeef3ab9a88d140331956bbcf23bd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913795"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Što je novo u studenome 2021. – Osnovna implementacija aplikacije Project Operations

_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
  
## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

U ovo izdanje uključene su sljedeće značajke:

- Sučelja za programiranje (API-ji) aplikacije Project Scheduling sada podržavaju mogućnost stvaranja i brisanja spremnika projekta

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-in-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2358236 | Ispravak fakture mora omogućiti ispravke koji imaju retke s nultom cijenom. |
| Upravljanje resursima | 2410072 | Dopušta postavljanje resursa koji je dodijeljen zadatku kao voditelj projekata. |
| Naplata i određivanje cijene | 2430234 | Rješava problem s izračunom performansi. |
| Vrijeme i trošak | 2436978 | Dopušta da se vrijeme unese u formatu hh:mm. |
| Naplata i određivanje cijene | 2448623 | Omogućuje ažuriranje cjenika nakon povezivanja s organizacijskom jedinicom. |
| Vrijeme i trošak | 2460396 | Dopušta brisanje unosa vremena brisanjem ćelije. |
| Naplata i određivanje cijene | 2467386 | Dopušta brisanje projekta koji ima zadatak, čak i kada je zadatak povezan s osvojenom ponudom. |
| Vrijeme i trošak | 2461744 | Prikaz **Moja neuspjela odobrenja** sadrži samo odobrenja projekta u fazi **Poslano**. |
| Vrijeme i trošak | 2464082 | Uklanja vezu s odobrenja projekta na skup odobrenja kada se ciljni status podudara. |
| Vrijeme i trošak | 2468108 | Posao rasporeda ne bi trebao postaviti status **Obrada** za skup odobrenja. |
| Vrijeme i trošak | 2471503 | Briše skupove odobrenja stare sedam dana. |
| Naplata i određivanje cijene | 2480687 | Referenca retka ponude ne smije se ukloniti kada se kreira ključna točka retka ponude. |
