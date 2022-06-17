---
title: Novosti u veljači 2022. – osnovna implementacija aplikacije Project Operations
description: U ovom se članku nalaze informacije o ažuriranjima kvalitete koja su dostupna u izdanju implementacije lite programa Project Operations u veljači 2022.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922811"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Novosti u veljači 2022. – osnovna implementacija aplikacije Project Operations

_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_

Ovaj se članak odnosi na sljedeće komponente i verzije programa Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji okruženja Dataverse 4.28.0.120

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

Od ovog izdanja možete dodati do 300 članova tima u jedan projekt. Ranije je ograničenje broja članova tima bilo 150. Dodatne informacije potražite u članku [Ograničenja projekta](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Ažuriranja kvalitete

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2497369 | Korekcija materijala mora slijediti vrijednost datuma u parametrima **Ispravak**. |
| Naplata i određivanje cijene | 2498697 | Poboljšana je konfiguracija sigurnosti za **opoziv** unosa vremena. |
| Naplata i određivanje cijene | 2517455 | Ne **smije se dopustiti da se akcija transakcija osvježenog retka fakture** pokreće više puta istovremeno za istu fakturu. |
| Naplata i određivanje cijene | 2517465 | Akcija Deaktiviraj detalje retka **fakture** blokirana je jer nije podržana. |
| Naplata i određivanje cijene | 2556660 | Fiksne su provjere efektivnosti datuma izvršene na cjeniku koji je priložen zapisu parametara projekta. |
|   Upravljanje prilikama | 2369202 | Ispravljena je poslovna logika kojom se provjerava mogu li se cjenici koji imaju preklapajuće datume efektivnosti priložiti istom ugovoru o projektu. |
|   Upravljanje prilikama | 2385965 | Ispravljeno je ponašanje na kartici Kupci **na** stranici Ugovor **o** projektu kada odaberete **Spremi i zatvori**. |
