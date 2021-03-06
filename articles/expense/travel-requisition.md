---
title: Putni nalozi
description: U ovoj temi nalaze se informacije o putnim nalozima.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906104"
---
# <a name="travel-requisitions"></a>Putni nalozi

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U putnom nalogu navode se troškovi koji će nastati na namjeravanom putovanju. Putni nalog šalje se na pregled i može se upotrebljavati za autorizaciju troškova.

Možda ćete putni nalog morati poslati prije nego što nastane bilo kakav trošak koji se zaračunava tvrtki ili ustanovi. Ovaj se zahtjev primjenjuje, neovisno o tome plaćate li troškove kreditnom karticom poduzeća, trošite li gotovinski predujam koji ste dobili ili imate neposredne troškove koje nadoknađuje tvrtka ili ustanova.

Putni nalog i pravilnici mogu se upotrebljavati za upravljanje troškovima tvrtke ili ustanove. Na primjer, ako vaša tvrtka ili ustanova radi na projektu s fiksnom cijenom koji zahtijeva putovanje, putni troškovi članova projektnog tima moraju se uklapati u proračun projekta. Zahtijevajući da se putni troškovi odobre prije nego što nastanu, tvrtka ili ustanova može pomoći da projekt ostane u okviru proračuna.

## <a name="configuration"></a>Konfiguracija 

Putni nalozi mogu se konfigurirati kao „obvezni” omogućivanjem parametra „Predautorizacija putovanja je obavezna” u parametrima upravljanja troškovima. 

## <a name="create-and-submit-a-travel-requisition"></a>Stvaranje i slanje putnog naloga

1. Idite na stavku **Moji troškovi: Putni nalog** i odaberite **Novi putni nalog**.
2. Unesite svrhu i odredište naloga.
3. U polje **Opis putovanja** unesite sve dodatne podatke. 
4. Za svaki od očekivanih troškova, poput leta, obroka ili najma automobila, stvorite stavku retka troška. Uključite procijenjeni datum, iznos i valutu za svaki trošak. 
5. Kada završite s dodavanjem očekivanih troškova, odaberite **Spremi**.
6. Kada budete spremni poslati putni nalog, odaberite **Tijek rada** > **Pošalji**.

Odobrene putne naloge možete pogledati pod stavkom **Moji troškovi: Putni nalog**. 

## <a name="view-available-travel-requisitions"></a>Prikaz dostupnih putnih naloga

Sve putne naloge možete pogledati pod stavkom **Moji troškovi: Putni nalozi**.

## <a name="approve-travel-requisitions"></a>Odobravanje putnih naloga

Odaberite putni nalog koji želite odobriti, a zatim odaberite **Tijek rada** > **Odobri**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Pošaljite izvješće o troškovima s pomoću odobrenog putnog naloga

1. Stvorite novo izvješće o troškovima i u zaglavlju izvješća o troškovima, a zatim s popisa odobrenih putnih naloga, odaberite **Mapiraj u putni nalog**.
2. Polje **Iznos putnog naloga** automatski se ažurira u zaglavlju izvješća o troškovima.
3. Dodavanje svih troškova nastalih tijekom putovanja. Ako je omogućeno polje **Predautorizirano**, ažurirat će se usklađeni iznos i odobreni iznos za određenu kategoriju troška.

> [!NOTE]
> Kada mapirate izvješće o troškovima u odobreni putni nalog, iznos transakcije ne može biti veći od autoriziranog iznosa. 
