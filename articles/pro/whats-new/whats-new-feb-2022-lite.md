---
title: Novosti u veljači 2022. – osnovna implementacija aplikacije Project Operations
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju osnovne implementacije aplikacije Project Operations za veljaču 2022.
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

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.28.0.120

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

Od ovog izdanja možete dodati do 300 članova tima u jedan projekt. Ranije je ograničenje broja članova tima bilo 150. Dodatne informacije potražite u članku [Ograničenja projekta](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Ažuriranja kvalitete

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2497369 | Ispravak materijala mora slijediti vrijednost datuma u parametrima **Ispravak**. |
| Naplata i određivanje cijene | 2498697 | Poboljšana sigurnosna konfiguracija za **Podsjećanje na unos vremena**. |
| Naplata i određivanje cijene | 2517455 | Radnja **Osvježene transakcije retka fakture** ne smije se pokretati više puta istovremeno za istu fakturu. |
| Naplata i određivanje cijene | 2517465 | Radnja **Deaktiviraj pojedinosti retka fakture** bokirana je jer nije podržana. |
| Naplata i određivanje cijene | 2556660 | Ispravljene su provjere datumske učinkovitosti koje se provode na cjeniku koji je priložen uz zapis parametara projekta. |
|   Upravljanje prilikama | 2369202 | Ispravljena je poslovna logika koja potvrđuje da se cjenici koji imaju preklapajuće datume stupanja na snagu mogu priložiti istom projektnom ugovoru. |
|   Upravljanje prilikama | 2385965 | Ispravljeno ponašanje u kartici **Kupci** na stranici **Ugovor o projektu** kada odaberete **Spremi i zatvori**. |
