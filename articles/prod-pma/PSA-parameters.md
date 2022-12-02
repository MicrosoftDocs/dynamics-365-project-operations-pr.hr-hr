---
title: Parametri integracije usluge Project Service Automation
description: U ovom se članku objašnjava način konfiguracije unosa zadanih podataka tijekom integracije usluge Microsoft Dynamics 365 for Project Service Automation s aplikacijom Microsoft Dynamics 365 Finance.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a4abeb2960981196ed1d7c453e7daa0558e326ef
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932287"
---
# <a name="project-service-automation-integration-parameters"></a>Parametri integracije usluge Project Service Automation

[!include[banner](../includes/banner.md)]

Na stranici **Parametri integracije usluge Project Service Automation** možete konfigurirati način unosa zadanih podataka tijekom integracije usluge Dynamics 365 Project Service Automation s aplikacijom Dynamics 365 Finance. Kako bi se projekti uspješno sinkronizirali iz usluge Project Service Automation u Financije, morate postaviti sljedeća polja.

Kako biste otvorili stranicu **Parametri integracije usluge Project Service Automation**, idite na **Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Parametri integracije usluge Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - Integracija projektnog zadatka, kategorije transakcija izdataka, procjene sati, procjene izdataka i zaključavanje funkcionalnosti dostupni su u verziji 8.0.
> - Integracija stvarnih podataka dostupna je u verziji 8.0.1. i kasnijim.


| Kartica                    | Polje                | Opis |
|------------------------|----------------------|-------------|
| Općenito                | Zadana vrsta projekta | Odaberite zadanu vrstu projekta. Kada se projekti sinkroniziraju iz usluge Project Service Automation, ova se vrijednost upotrebljava ako u integracijski predložak niste unijeli zadanu vrijednost. Tijekom sinkronizacije, polje **Vrsta projekta** novih projekata postavljeno je na tu vrijednost. Međutim, vrijednost se može ažurirati kada se redci ugovora o projektu sinkroniziraju iz usluge Project Service Automation. |
|                        | Vremenska kategorija        | Odaberite zadane vremenske kategorije. Ova se vrijednost upotrebljava kada se procjene sati sinkroniziraju iz usluge Project Service Automation. Polje **Kategorija** novih predviđanja sati za projekt u Financijama postavljeno je na tu vrijednost kada se procijenjeni i stvarni sati sinkroniziraju iz usluge Project Service Automation. |
|                        | Kategorija naknade         | Odaberite zadanu kategoriju naknade. Ova se vrijednost upotrebljava kada se stvarne naknade sinkroniziraju iz usluge Project Service Automation. Polje **Kategorija** novih transakcija naknade u Financijama postavljeno je na tu vrijednost kada se stvarne naknade sinkroniziraju iz usluge Project Service Automation. |
| Zadane vrijednosti grupe projekata | Vrsta projekta         | Kliknite **Novo** za dodavanje retka u kojem možete odabrati vrstu projekta za koju ćete postaviti zadanu grupu projekata. Određena se vrsta projekta u konfiguraciji može odabrati samo jednom. |
|                        | Grupa projekata        | Odaberite zadanu grupu projekata za odabranu vrstu projekta. Kada se novi projekti sinkroniziraju iz usluge Project Service Automation, polje **Grupa projekata** postavljeno je na zadanu vrijednost za vrstu projekta ako u predložak integracije niste unijeli zadanu vrijednost. |
| Zadane postavke vrste naplate  | Vrsta naplate         | Kliknite **Novo** za dodavanje retka u kojem možete odabrati vrstu naplate za koju ćete postaviti zadano svojstvo retka. Određena se vrsta naplate u konfiguraciji može odabrati samo jednom. |
|                        | Svojstvo retka        | Odaberite zadano svojstvo retka za odabranu vrstu naplate. Kada se nove procjene sati i izdataka ili novi stvarni podaci sinkroniziraju iz usluge Project Service Automation, polje **Svojstvo retka** postavlja se na zadanu vrijednost za vrstu naplate. |
| Zaključavanje funkcija  | Nije primjenjivo       | Odaberite funkciju koju ćete onemogućiti u Financijama za projekte i ugovore koji potječu iz usluge Project Service Automation. Na primjer, možete isključiti mogućnost uređivanja ugovora i projekata, stvoriti strukturnu analizu rada i u Financije unijeti evidenciju radnog vremena. Polja koja se odnose na računovodstvo i dalje će biti omogućena, čak i ako zbog postavke parametra postanu nedostupna. Prema zadanim postavkama omogućene su sve funkcije. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]