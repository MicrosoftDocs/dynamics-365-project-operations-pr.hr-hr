---
title: Rezervacije u odnosu na dodjele
description: U ovoj temi nalaze se informacije o razlikama između rezervacija i dodjela resursa.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1906ebd76f5fc66215aa5963242de13206a81668cb4973cccaf5b153514672d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008441"
---
# <a name="bookings-vs-assignments"></a>Rezervacije u odnosu na dodjele

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Rezervacije mogu imati fiksno ili promjenjivo dodjeljivanje resursa projektu. Fiksne rezervacije iskorištavaju kapacitet resursa. Rezervacije predstavljaju organizacijske koncepte timova kako bi mogli razumjeti način na koji će se resursi angažirati na različitim projektima. Dynamics 365 Project Operations tretira rezervacije kao koncept na razini projekta. 

Za razliku od rezervacija, dodjele predstavljaju zaduženje resursa zadacima projekta u rasporedu projekta. Resursi mogu biti imenovani ili generički.  Kada se zahtjev za resursom izvede iz dodjele projektnog zadatka, Project Operations upotrebljava konture napora zadatka resursa za izgradnju kontura pojedinosti preduvjeta za resurs. Međutim, upućivanje na zadatke resursa ne održava se. Ažuriranja rezervacija izvedenih iz preduvjeta za resurs ne ažuriraju nikakve zadatke resursa.

Uobičajeno je zbroj rezervacija za resurs jednak zbroju dodjela resursa jednom ili većem broju zadataka. Međutim, Project Operations ne nameće takvu podudarnost. U prikazu **Usklađivanje** možete vidjeti mjesta voditelja projekta gdje se rezervacija i dodjele resursa ne podudaraju.




[!INCLUDE[footer-include](../includes/footer-banner.md)]