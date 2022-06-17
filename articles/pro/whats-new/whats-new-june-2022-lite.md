---
title: Što je novo u lipnju 2022. – implementacija osnovne aplikacije Project Operations
description: U ovom se članku nalaze informacije o kvalitetnim ažuriranjima koja su dostupna u izdanju implementacije sustava Microsoft Dynamics 365 Project Operations lite u lipnju 2022.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959603"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Što je novo u lipnju 2022. – implementacija osnovne aplikacije Project Operations

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ovaj se članak odnosi na sljedeće komponente i verzije programa Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji okruženja Dataverse 4.43.0.77

## <a name="quality-updates"></a>Ažuriranja kvalitete

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Ugovaranje o kooperaciji | 2708885 | Ispravljena je poruka o pogrešci koja se pojavljuje kada korisnik stvori zapis zaglavlja rezervacije resursa koji se može rezervirati, a u kojoj nije ispunjen resurs koji se može rezervirati. |
| Planiranje i praćenje projekta | 2629441 | Ispravio je logiku pokretanja tijeka rada kako bi se spriječila beskonačna petlja prilikom ažuriranja projektnih zadataka. |
| Vrijeme i trošak | 2641209 | Uvoz unosa vremena iz dodjela/rezervacija mora zadržati referencu resursa koja se može rezervirati. |
| Planiranje i praćenje projekta | 2651148 | Zaglavlje projektnog dokumenta mora biti čuvano.|
| Planiranje i praćenje projekta | 2653145 | Dodane su provjere valjanosti kako bi se osiguralo da se ne može stvoriti zapis projekta koji u nazivu ima znakove koji nisu valjani. |
| Vrijeme i trošak | 2654710 | Ispravljeno filtriranje na **stranici Odobrenja**. |
| Naplata i određivanje cijene | 2667805 | Dodane su provjere valjanosti kako bi se spriječilo stvaranje stvarnog iznosa naplaćene prodaje ako ne postoje neplaćene vrijednosti prodaje. |
| Naplata i određivanje cijene | 2668378 | Dodane su provjere valjanosti kako bi se spriječilo dodavanje prilagođene dimenzije određivanja cijena, osim ako se ne ispune logički naziv i naziv polja. |
| Vrijeme i trošak | 2700428 | Poboljšana je logika odobravanja kako bi se osiguralo da se drugi skupovi odobrenja za projekt mogu obraditi čak i ako je jedan od skupova odobrenja zapeo u poslovima sustava. |
