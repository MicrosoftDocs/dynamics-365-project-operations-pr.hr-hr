---
title: Izvješća o trošku i više odobravatelja
description: U ovoj se temi nalaze informacije o izvješćima o troškovima koje treba odobriti više osoba.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfa8677f38e9468aa3236f587d2e9bd5af839054
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120984"
---
# <a name="expense-reports-and-multiple-approvers"></a>Izvješća o trošku i više odobravatelja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Ovisno o pravilima vaše tvrtke ili ustanove za odobravanje troškova, možda će podneseno izvješće o troškovima morati odobriti više osoba. Kada postavljate postupak tijeka rada za odobrenje izvješća o troškovima, možete dodati elemente tijeka rada koji obuhvaćaju zadatke ili korake za jednog ili više odobravatelja izvješća o troškovima. Na primjer, možda ćete tražiti da sva izvješća o troškovima odobre dvije odvojene osobe, rukovoditelj zaposlenika koji je podnio izvješće i koordinator dugovanja.

Ako odlučite tražiti više odobravatelja izvješća o troškovima, elemente tijeka rada možete dodati na jedan od sljedećih načina:

- Dodajte jedan element odobrenja koji ima jedan korak. Na primjer, korak može zahtijevati da se izvješće o troškovima dodijeli grupi korisnika i da ga odobri 50 posto članova grupe korisnika.
- Dodajte jedan element odobrenja koji ima više koraka. Na primjer, element odobrenja može imati sljedeće korake:

    1. Izvješće o troškovima odobrava rukovoditelj zaposlenika koji je podnio izvješće.
    2. Službenik za dugovanja provjerava račune i stavke izvješća o troškovima.
    3. Izvješće o troškovima odobrava vlasnik proračuna.

- Dodajte više elemenata odobrenja, od kojih svaki ima jedan korak. Na primjer, možete dodati zasebni element odobrenja za svaki od sljedećih koraka:

    1. Izvješće o troškovima odobrava rukovoditelj zaposlenika.
    2. Izvješće o troškovima odobrava vlasnik proračuna.


[!INCLUDE[footer-include](../includes/footer-banner.md)]