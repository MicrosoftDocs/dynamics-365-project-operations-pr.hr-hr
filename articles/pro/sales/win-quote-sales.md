---
title: Zatvaranje ponude – jednostavno
description: U ovoj temi nalaze se informacije o zatvaranju ponude u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175702"
---
# <a name="close-a-quote---lite"></a>Zatvaranje ponude – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ponuda projekta mogu se zatvoriti kao ostvarene ili neostvarene. Operacije aktiviranja i revizije ponuda nisu podržane u aplikaciji Microsoft Dynamics 365 Project Operations, tako da se nacrt ponude može zatvoriti.

## <a name="close-a-quote-as-won"></a>Zatvaranje ponude kao ostvarene

Zatvaranje ponude za projekt kao Ostvarene zatvorit će ponudu sa statusom postavljenim na Zatvorena i razlogom statusa postavljenim na Ostvaren. Zatvaranje ponude čini ponudu projekta ponudom samo za čitanje i stvara nacrt ugovora o projektu koji sadrži podatke o ponudi. Postoji dijaloški okvir za potvrdu prije nego što se promjene izvrše, jer se zatvorena ponuda ne može ponovo otvoriti i promjene su nepovratne.

Ako je ponuda priložena uz priliku, svaka druga ponuda projekta za priliku automatski se zatvaraju kao Izgubljena.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Financijski utjecaj zatvaranja ponude kao ostvarene

Ako postoje stvarni podaci o vremenu zabilježenom na projektu, dok je on još uvijek priložen nacrtu ponude, bilježe se samo troškovi vremena ili izdataka. Nakon što se ponuda zatvori kao ostvarena, aplikacija će refaktorirati troškove poništavanjem starijih stvarnih podataka o trošku i ponovnim stvaranjem novih stvarnih podataka o trošku. Aplikacija će obraditi ove stvarne podatke o trošku na temelju metode naplate retka ugovora povezanog projekta. Ako se stvarni podaci o trošku odnose na redak ugovora o vremenu i materijalu, sustav će automatski stvoriti odgovarajuće nenaplaćene stvarne prodajne podatke za vrijeme zatvaranja ponude i izrade ugovora o projektu. Ako se stvarni podaci o trošku odnose na redak ugovora s fiksnom cijenom, aplikacija će zaustaviti ponovnu obradu stvarnih podataka o trošku na temelju pravila podijeljene naplate za klijente ugovora o projektu.

## <a name="closing-a-quote-as-lost"></a>Zatvaranje ponude kao neostvarene:

Zatvaranjem ponude projekta kao neostvarene postavit će status na Zatvoreno, a razlog statusa na Izgubljena. Zatvaranje ponude čini ponudu projekta ponudom samo za čitanje. Budući da se zatvorena ponuda ne može ponovno otvoriti, prije nego što zatvorite ponudu, dijaloški okvir potvrdit će vaše promjene.

Ako ponuda projekta koja je zatvorena kao Izgubljena ima projekt naveden na nekom od svojih redaka, taj projekt se također označava kao Zatvoren i sve rezervacije resursa od toga dana nadalje otkazuju se.

> [!NOTE]
> U aplikaciji Project Operations zatvaranje ponude kao Ostvarene ili Neostvarene neće utjecati na status Prilike, koji će ostati otvoren sve dok se ručno ne zatvori.
