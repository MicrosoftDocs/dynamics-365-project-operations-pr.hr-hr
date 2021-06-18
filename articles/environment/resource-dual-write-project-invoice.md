---
title: Integracija fakture za projekt
description: U ovoj temi nalaze se informacije o integraciji dvostrukog pisanja u aplikaciji Project Operations za fakturiranje klijentu.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996557"
---
# <a name="project-invoice-integration"></a>Integracija fakture za projekt

U ovoj temi nalaze se informacije o integraciji dvostrukog pisanja u aplikaciji Project Operations za fakturiranje klijentu.

Voditelj projekta u aplikaciji Project Operations upravlja zaostalom naplatom projekta i stvara predračun za klijenta na platformi Microsoft Dataverse. Na temelju ovog predračuna, službenik za potraživanja ili računovođa projekta stvara račun za klijenta. Integracija dvostrukog pisanja osigurava sinkronizaciju pojedinosti predračuna s aplikacijama Finance and Operations. Nakon što se proknjiži faktura za klijenta, sustav ažurira relevantne stvarne podatke o projektu na platformi Dataverse s računovodstvenim pojedinostima. Grafički prikaz u nastavku pruža konceptualni pregled ove integracije na visokoj razini.

   ![Integracija fakture za projekt](./media/DW5Invoicing.png)

Nakon što voditelj projekta potvrdi predračun na platformi Dataverse, podaci zaglavlja predračuna sinkroniziraju se s aplikacijama Finance and Operations s pomoću karte tablice s dvostrukim pisanjem **Prijedlog fakture za projekt V2 (fakture)**. Ovo je jednosmjerna integracija s platforme Dataverse u aplikacije Finance and Operations. Stvaranje ili brisanje prijedloga faktura za projekt izravno u aplikacijama Finance and Operations nije podržano.

Potvrda računa na platformi Dataverse također pokreće poslovnu logiku za stvaranje zapisa povezanih s naplatom u entitetu **Stvarni podaci**. Ti zapisi sinkronizirani su s aplikacijama Finance and Operations s pomoću karte tablice s dvostrukim ispisom **Stvarni podaci o integraciji aplikacije Project Operations (msdyn\_actuals).** Dodatne informacije potražite u članku [Procjene i stvarni podaci o projektu](resource-dual-write-estimates-actuals.md). 

Redci prijedloga fakture za projekt stvaraju se povremenim postupkom **Uvoz iz pripreme**. Ova se obrada temelji na pojedinostima stvarnih podataka naplaćene prodaje u tablici **Pripremni stvarni podaci**. Dodatne informacija potražite u članku [Upravljanje prijedlozima faktura za projekt](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
