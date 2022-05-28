---
title: Što je novo studeni 2021. – implementacija lite projektnih operacija
description: Ovaj tema pruža informacije o ažuriranjima kvalitete koja su dostupna u izdanju implementacije lite projekta Project Operations u studenome 2021.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f3a19cddd1b91fc76c852153526fb7197a9f92c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587761"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Što je novo studeni 2021. – implementacija lite projektnih operacija

_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_

Ovaj tema odnosi se na sljedeće microsoftove Dynamics 365 Project Operations komponente i verzije :

- Operacije projekta u verziji okruženja Dataverse 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
  
## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

U ovo izdanje uključene su sljedeće značajke:

- Sučelja za programiranje aplikacija za planiranje projekata (API-ji) sada podržavaju mogućnost stvaranja i brisanja paketa Project

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-in-dataverse"></a>Projektne operacije u programu Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2358236 | Ispravak fakture mora dopustiti ispravke koji imaju retke nulte cijene. |
| Upravljanje resursima | 2410072 | Dopusti postavljanje resursa koji je dodijeljen zadatku kao voditelj projekta. |
| Naplata i određivanje cijene | 2430234 | Riješite problem s izračunom performansi troškova. |
| Vrijeme i trošak | 2436978 | Dopustite unos vremena u hh:mm formatu. |
| Naplata i određivanje cijene | 2448623 | Dopustite ažuriranje cjenika nakon povezivanja s organizacijskom jedinicom. |
| Vrijeme i trošak | 2460396 | Dopustite brisanje unosa vremena brisanjem ćelije. |
| Naplata i određivanje cijene | 2467386 | Dopusti brisanje projekta koji ima zadatak, čak i kada je zadatak povezan s osvojenom ponudom. |
| Vrijeme i trošak | 2461744 | Prikaz **Moje neuspjelo odobrenje** sadrži samo odobrenja projekta u **fazi Poslano**. |
| Vrijeme i trošak | 2464082 | Uklonite vezu iz odobrenja projekta na odobrenje postavljeno kada se podudara ciljni status. |
| Vrijeme i trošak | 2468108 | Zadatak Raspored ne bi trebao postaviti **status Obrade** za skup odobravanja. |
| Vrijeme i trošak | 2471503 | Izbrišite skupove odobrenja stare sedam dana. |
| Naplata i određivanje cijene | 2480687 | Referenca retka ponude ne smije se ukloniti prilikom stvaranja prekretnice retka ponude. |
