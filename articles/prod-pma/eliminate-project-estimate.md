---
title: Uklanjanje procjene projekta
description: U ovoj temi nalaze se informacije o uklanjanju procjene projekta nakon što se dovrši.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 267b5ffab7ef3a6776c31100deea81fb523752b6
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684081"
---
# <a name="eliminate-a-project-estimate"></a>Uklanjanje procjene projekta

[!include [banner](../includes/banner.md)]

Procjena projekta daje financijski prikaz za procijenjeni i raspoređeni rad za projekt. Kako biste radili s procjenama za projekt, projekt morate priložiti projektu procjene. Projekt procjene uvijek se temelji na postojećem projektu, međutim više projekata može se odnositi na jedan projekt procjene. Za projekte procjene mogu se priložiti samo projekti s fiksnom cijenom i investicijski projekti, a ti projekti moraju pripadati istoj projektnoj grupi kao i projekt procjene.

Kako bi se uklonio projekt procjene, on mora biti dovršen. Sljedeći koraci objašnjavaju način uklanjanja procjene.

1. Idite na mogućnost **Upravljanje projektima i računovodstvo** > **Svi projekti** i otvorite projekt. 
2. Na kartici **Upravljanje**, odaberite **Procjene** i na stranici **Procjena** odaberite **Ukloni**.
3. Na stranici **Ukloni procjenu**, na kartici **Općenito**, postavite sljedeće mogućnosti:

   - **Kod razdoblja**: Odaberite kod razdoblja kako biste odabrali odgovarajuće projekte procjene. 
   - **Datum procjene**: Odaberite odgovarajući datum procjene za uklanjanje.
   - **Ukloni s pomoću WIP upozorenja**: Omogućite ovu mogućnost za pružanje obavijesti kada će procjena koja je povezana s radom u tijeku (WIP) biti uklonjena. Kada ova mogućnost nije omogućena, uklanjanje se ne može nastaviti ako postoji neka transakcija koja nije procijenjena. 
   > [!NOTE]
   > Ova je mogućnost dostupna samo kada se uklanjanje primjenjuje na projekt procjene. Nije dostupno ako upotrebljavate periodična knjiženja. Ova postavka radi s postavkama na kartici **Procjena**, na stranici **Parametri projekta**, u grupi polja **Dopusti eliminaciju kada postoje transakcije koje nisu procijenjene**.
   - **Postavljanje faze na Završeno**: Omogućite ovu mogućnost kako biste postavili fazu projekta procjene na **Završeno** nakon što pokrenete uklanjanje.
   - **Ispis popisa procjena**: Odaberite podatke koji će se uključiti pri ispisu popisa procjena.
   - **Prikaži dnevnik s informacijama**: Omogućite ovu mogućnost za prikaz dnevnika s informacijama.
   - **Datum knjiženja**: Odaberite datum knjiženja procjene u glavnu knjigu.

4.  Odaberite **U redu**.
5. Nakon završetka postupka uklanjanja, uklonjeni projekt procjene prikazuje se s negativnom vrijednošću. 

Ako niste namjeravali ukloniti procjenu, možete odabrati uklonjenu procjenu i odabrati **Poništi uklanjanje**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]