---
title: Integracija fakture za projekt
description: U ovom se članku nalaze informacije o integraciji dvostrukog pisanja programa Project Operations za fakturiranje korisnika.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912093"
---
# <a name="project-invoice-integration"></a>Integracija fakture za projekt

U ovom se članku nalaze informacije o integraciji dvostrukog pisanja programa Project Operations za fakturiranje korisnika.

Voditelj projekta u aplikaciji Project Operations upravlja zaostalom naplatom projekta i stvara predračun za klijenta na platformi Microsoft Dataverse. Na temelju ovog predračuna, službenik za potraživanja ili računovođa projekta stvara račun za klijenta. Integracija dvostrukog pisanja osigurava da se detalji predračunske fakture sinkroniziraju s aplikacijama Financije i operacije. Nakon što se proknjiži faktura za klijenta, sustav ažurira relevantne stvarne podatke o projektu na platformi Dataverse s računovodstvenim pojedinostima. Grafički prikaz u nastavku pruža konceptualni pregled ove integracije na visokoj razini.

   ![Integracija fakture za projekt.](./media/DW5Invoicing.png)

Nakon što voditelj projekta potvrdi predračun u Dataverse sustavu, podaci zaglavlja predračunske fakture sinkroniziraju se s aplikacijama Financije i operacije pomoću karte tablice s dvostrukim pisanjem, **Prijedlog fakture za projekt V2 (fakture)**. Ovo je jednosmjerna integracija iz Dataverse aplikacija za financije i operacije. Stvaranje ili brisanje prijedloga faktura za projekt izravno u aplikacijama Financije i operacije nije podržano.

Potvrda računa na platformi Dataverse također pokreće poslovnu logiku za stvaranje zapisa povezanih s naplatom u entitetu **Stvarni podaci**. Ti se zapisi sinkroniziraju s financijama i operacijama pomoću karte tablice s dvostrukim pisanjem, **stvarne integracije projektnih operacija (msdyn\_ actuals).** Dodatne informacije potražite u članku [Procjene i stvarni podaci o projektu](resource-dual-write-estimates-actuals.md). 

Redci prijedloga fakture za projekt stvaraju se povremenim postupkom **Uvoz iz pripreme**. Ova se obrada temelji na pojedinostima stvarnih podataka naplaćene prodaje u tablici **Pripremni stvarni podaci**. Dodatne informacija potražite u članku [Upravljanje prijedlozima faktura za projekt](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
