---
title: Integracija fakture za projekt
description: U ovoj temi nalaze se informacije o integraciji dvostrukog pisanja u aplikaciji Project Operations za fakturiranje klijentu.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581229"
---
# <a name="project-invoice-integration"></a>Integracija fakture za projekt

U ovoj temi nalaze se informacije o integraciji dvostrukog pisanja u aplikaciji Project Operations za fakturiranje klijentu.

Voditelj projekta u aplikaciji Project Operations upravlja zaostalom naplatom projekta i stvara predračun za klijenta na platformi Microsoft Dataverse. Na temelju ovog predračuna, službenik za potraživanja ili računovođa projekta stvara račun za klijenta. Integracija dvostrukog pisanja osigurava da se detalji predračunske fakture sinkroniziraju s aplikacijama Financije i operacije. Nakon što se proknjiži faktura za klijenta, sustav ažurira relevantne stvarne podatke o projektu na platformi Dataverse s računovodstvenim pojedinostima. Grafički prikaz u nastavku pruža konceptualni pregled ove integracije na visokoj razini.

   ![Integracija fakture za projekt.](./media/DW5Invoicing.png)

Nakon što voditelj projekta potvrdi predračun u Dataverse sustavu, podaci zaglavlja predračunske fakture sinkroniziraju se s aplikacijama Financije i operacije pomoću karte tablice s dvostrukim pisanjem, **Prijedlog fakture za projekt V2 (fakture)**. Ovo je jednosmjerna integracija iz Dataverse aplikacija za financije i operacije. Stvaranje ili brisanje prijedloga faktura za projekt izravno u aplikacijama Financije i operacije nije podržano.

Potvrda računa na platformi Dataverse također pokreće poslovnu logiku za stvaranje zapisa povezanih s naplatom u entitetu **Stvarni podaci**. Ti se zapisi sinkroniziraju s financijama i operacijama pomoću karte tablice s dvostrukim pisanjem, **stvarne integracije projektnih operacija (msdyn\_ actuals).** Dodatne informacije potražite u članku [Procjene i stvarni podaci o projektu](resource-dual-write-estimates-actuals.md). 

Redci prijedloga fakture za projekt stvaraju se povremenim postupkom **Uvoz iz pripreme**. Ova se obrada temelji na pojedinostima stvarnih podataka naplaćene prodaje u tablici **Pripremni stvarni podaci**. Dodatne informacija potražite u članku [Upravljanje prijedlozima faktura za projekt](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
