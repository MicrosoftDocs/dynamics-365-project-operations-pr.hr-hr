---
title: Rezervacije u odnosu na dodjele
description: U ovom se članku navode informacije o razlikama između rezervacija resursa i dodjela resursa.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3410a45ce8401905dc162db66b0975e4aa3350dc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918579"
---
# <a name="bookings-vs-assignments"></a>Rezervacije u odnosu na dodjele

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Rezervacije mogu imati fiksno ili promjenjivo dodjeljivanje resursa projektu. Fiksne rezervacije iskorištavaju kapacitet resursa. Rezervacije predstavljaju organizacijske koncepte timova kako bi mogli razumjeti način na koji će se resursi angažirati na različitim projektima. Dynamics 365 Project Operations tretira rezervacije kao koncept na razini projekta. 

Za razliku od rezervacija, dodjele predstavljaju zaduženje resursa zadacima projekta u rasporedu projekta. Resursi mogu biti imenovani ili generički.  Kada se zahtjev za resursom izvede iz dodjele projektnog zadatka, Project Operations upotrebljava konture napora zadatka resursa za izgradnju kontura pojedinosti preduvjeta za resurs. Međutim, upućivanje na zadatke resursa ne održava se. Ažuriranja rezervacija izvedenih iz preduvjeta za resurs ne ažuriraju nikakve zadatke resursa.

Uobičajeno je zbroj rezervacija za resurs jednak zbroju dodjela resursa jednom ili većem broju zadataka. Međutim, Project Operations ne nameće takvu podudarnost. U prikazu **Usklađivanje** možete vidjeti mjesta voditelja projekta gdje se rezervacija i dodjele resursa ne podudaraju.




[!INCLUDE[footer-include](../includes/footer-banner.md)]