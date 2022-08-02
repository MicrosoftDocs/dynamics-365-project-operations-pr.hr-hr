---
title: Integracija fakture za projekt
description: U ovom se članku nalaze informacije o integraciji dvostrukog pisanja programa Project Operations za fakturiranje korisnika.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029015"
---
# <a name="project-invoice-integration"></a>Integracija fakture za projekt

U ovom se članku nalaze informacije o integraciji dvostrukog pisanja programa Project Operations za fakturiranje korisnika.

Voditelj projekta u aplikaciji Project Operations upravlja zaostalom naplatom projekta i stvara predračun za klijenta na platformi Microsoft Dataverse. Na temelju ovog predračuna, službenik za potraživanja ili računovođa projekta stvara račun za klijenta. Integracija dvostrukog pisanja osigurava da se detalji predračuna fakture sinkroniziraju s financijskim i operativnim aplikacijama. Nakon što se proknjiži faktura za klijenta, sustav ažurira relevantne stvarne podatke o projektu na platformi Dataverse s računovodstvenim pojedinostima. Grafički prikaz u nastavku pruža konceptualni pregled ove integracije na visokoj razini.

   ![Integracija fakture za projekt.](./media/DW5Invoicing.png)

Nakon što voditelj projekta potvrdi predračun u Dataverse sustavu, podaci zaglavlja predračuna sinkroniziraju se s aplikacijama za financije i operacije pomoću karte tablice s dvostrukim pisanjem, **prijedlog fakture za projekt V2 (fakture)**. Ovo je jednosmjerna integracija s Dataverse financijskih i operativnih aplikacija. Stvaranje ili brisanje prijedloga faktura za projekt izravno u aplikacijama za financije i operacije nije podržano.

Potvrda računa na platformi Dataverse također pokreće poslovnu logiku za stvaranje zapisa povezanih s naplatom u entitetu **Stvarni podaci**. Ti se zapisi sinkroniziraju s financijama i operacijama pomoću karte tablice s dvostrukim pisanjem, **stvar integracije projektnih operacija (msdyn\_ actuals).** Dodatne informacije potražite u članku [Procjene i stvarni podaci o projektu](resource-dual-write-estimates-actuals.md). 

Redci prijedloga fakture za projekt stvaraju se povremenim postupkom **Uvoz iz pripreme**. Ova se obrada temelji na pojedinostima stvarnih podataka naplaćene prodaje u tablici **Pripremni stvarni podaci**. Dodatne informacija potražite u članku [Upravljanje prijedlozima faktura za projekt](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
