---
title: Izvedba prijedloga fakture za projekt
description: U ovom članku nalaze se informacije o poboljšanjima izvedbe prijedloga faktura za projekt.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 70069778b7d4326cb23d6bb36e2c78a33da12573
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927181"
---
# <a name="project-invoice-proposal-performance"></a>Izvedba prijedloga fakture za projekt

[!include [banner](../includes/banner.md)]

Kada izrađujete novi prijedlog fakture, mogli biste naići na probleme s izvedbom kako se povećava broj projekata i potprojekata. Kako bi se poboljšala izvedba, dostupna je značajka koja smanjuje vrijeme potrebno za stvaranje novog prijedloga fakture za knjižene projektnih transakcija.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Omogućivanje poboljšanja izvedbe prijedloga fakture za projekt
Kako biste omogućili značajku poboljšanja izvedbe prijedloga fakture za projekt, poduzmite korake u nastavku.

1.  Idite na **Upravljanje značajkama** > **Sve**. Na popisu značajki pronađite **Poboljšanje izvedbe prijedloga fakture za projekt**.
2.  Odaberite **Omogući odmah**.
3.  Osvježite svoj preglednik, a zatim stvorite novi prijedlog fakture.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Isključivanje poboljšanja izvedbe prijedloga fakture za projekt
Kako biste isključili značajku poboljšanja izvedbe prijedloga fakture za projekt, poduzmite korake u nastavku.

1.  Idite na **Upravljanje značajkama** > **Sve**. Na popisu značajki pronađite **Poboljšanje izvedbe prijedloga fakture za projekt**.
2.  Odaberite **Onemogući**.
3.  Osvježite preglednik.

> [!NOTE]
> Izvedba prijedloga fakture ne može se primijeniti kada su omogućena pravila naplate.
> 
> Tijekom skupnog postupka izrade prijedloga faktura, broj podzadataka podijelit će zadatke na maksimalni broj na temelju broja ugovora s transakcijama koje je moguće fakturirati, bez obzira na to što ste unijeli. Na primjer, ako unesete **3** za broj podzadataka za stvaranje prijedloga fakture u skupu, a postoje samo dva ugovora s transakcijama koje je moguće fakturirati, stvaraju se samo dva podzadatka.
