---
title: Izvješća o trošku i više odobravatelja
description: U ovoj se temi nalaze informacije o izvješćima o troškovima koje treba odobriti više osoba.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2acae2d518a02539f01d5498450236999fe609d1e8f26b5f90e18b986b83cab1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988417"
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