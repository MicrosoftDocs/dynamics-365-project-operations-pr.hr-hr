---
title: Zatvaranje ponude – jednostavno
description: U ovoj temi nalaze se informacije o zatvaranju ponude u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6214e1b5bec5c9173a6b6e69578de14654da633e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272260"
---
# <a name="close-a-quote---lite"></a>Zatvaranje ponude – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ponuda projekta mogu se zatvoriti kao ostvarene ili neostvarene. Nacrt ponude može se zatvoriti jer operacije Aktiviranje i Revizija ponude nisu podržane u aplikaciji Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Zatvaranje ponude kao ostvarene

Kada ponudu za projekt zatvorite kao Dobivena, stanje se postavlja na Zatvorena, a razlog stanja je Dobiveno. Zatvaranje ponude čini ponudu projekta ponudom samo za čitanje i stvara nacrt ugovora o projektu koji sadrži podatke o ponudi. Budući da se zatvorena ponuda ne može ponovo otvoriti, dijaloški okvir za potvrdu potvrdit će vaše promjene.

Ako je ponuda priložena uz priliku, svaka druga ponuda projekta za priliku automatski se zatvaraju kao Izgubljena.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Financijski utjecaj zatvaranja ponude kao ostvarene

Ako postoje stvarni podaci o vremenu utrošenom na projektu dok je još uvijek priložen nacrtu ponude, bilježe se samo troškovi vremena ili izdataka. Nakon što se ponuda zatvori kao ostvarena, aplikacija će refaktorirati troškove poništavanjem starijih stvarnih podataka o trošku i ponovnim stvaranjem novih stvarnih podataka o trošku. Aplikacija će obraditi ove stvarne podatke o trošku na temelju metode naplate retka ugovora povezanog projekta. Ako se stvarni podaci o troškovima odnose na redak ugovora o vremenu i materijalu, odgovarajući se nenaplaćeni stvarni podaci o prodaji stvaraju nakon zatvaranja ponude i stvaranja ugovora o projektu. Ako se stvarni trošak odnosi na redak ugovora s fiksnom cijenom, aplikacija će zaustaviti ponovnu obradu stvarnog troška koji se temelji na pravilima podijeljene naplate za klijente ugovora o projektu.

## <a name="closing-a-quote-as-lost"></a>Zatvaranje ponude kao neostvarene:

Kada ponudu za projekt zatvorite kao Izgubljenu, stanje se postavlja na Zatvorena, a razlog stanja je Izgubljena. Zatvaranje ponude čini ponudu projekta ponudom samo za čitanje. Budući da se zatvorena ponuda ne može ponovno otvoriti, prije nego što zatvorite ponudu, dijaloški okvir potvrdit će vaše promjene.

Ako se ponuda projekta koja je zatvorena kao Izgubljena odnosi na neki od redaka projekta, taj se projekt također označuje kao Zatvoren. Sve se rezervacije resursa od tog dana nadalje otkazuju.

> [!NOTE]
> U aplikaciji Project Operations zatvaranje ponude kao Ostvarene ili Neostvarene neće utjecati na status Prilike, koji će ostati otvoren sve dok se ručno ne zatvori.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]