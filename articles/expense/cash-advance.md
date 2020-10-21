---
title: Gotovinski predujam
description: U ovoj temi nalaze se informacije o gotovinskim predujmovima.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907960"
---
# <a name="cash-advance"></a>Gotovinski predujam

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Gotovinski predujam omogućuje zaposlenicima posudbu novca od njihove tvrtke prije stvaranja bilo kakvih troškova. Kada se odobri i plati traženi gotovinski predujam, zaposlenik može novac upotrijebiti za poslovne troškove koji će možda nastati. 

## <a name="create-and-submit-a-cash-advance-request"></a>Stvaranje i slanje zahtjeva za gotovinski predujam

1. Kako biste stvorili novi gotovinski predujam, pod stavkom **Moji troškovi** odaberite **Gotovinski predujmovi** > **Novi**. 
2. Na stranici **Novi zahtjev za gotovinski predujam** unesite svrhu troška i odaberite mjesto na kojem će trošak nastati.
3. Unesite traženi iznos i valutu, a zatim odaberite mogućnost **Spremi**. 
4. Kada zahtjev za gotovinski predujam bude spreman za slanje, na stranici **Zahtjev za gotovinski predujam** odaberite **Tijek rada** > **Pošalji**.

## <a name="modify-a-cash-advance-request"></a>Izmjena zahtjeva za gotovinskim predujmom

Zahtjev za gotovinski predujam možete izmijeniti ako nije poslan na odobrenje.

1. Pod stavkom **Moji troškovi: Gotovinski predujmovi** pronađite i odaberite gotovinski predujam koji želite urediti.
2. Odaberite mogućnost **Uredi** i unesite potrebne izmjene u zahtjev za gotovinski predujam. 
3. Odaberite **Spremi i zatvori**.


## <a name="view-cash-advance-requests"></a>Prikaz zahtjeva za gotovinski predujam
Pod stavkom **Moji troškovi: Gotovinski predujmovi** možete pregledati popis svih gotovinskih predujmova koji su u nacrtu, predani, u pregledu ili plaćeni. 

## <a name="approve-cash-advance-requests"></a>Odobrenje zahtjeva za gotovinski predujam

Voditelji ili korisnici konfigurirani kao odobravatelji u tijeku rada moći će odobriti gotovinske predujmove koji su im dostavljeni na pregled. 

1. Kako biste odobrili gotovinski predujam, pod stavkom **Obradi gotovinske predujmove**, odaberite **Gotovinski predujmovi za moj pregled**.
2. Odaberite gotovinski predujam koji trebate pregledati i odaberite **Odobri**.  

## <a name="pay-cash-advances"></a>Plaćanje gotovinskih predujmova 
Sljedeći postupak obično dovršava računovođa ili korisnik s računovodstvenim dozvolama.

1. Za knjiženje odobrenih gotovinskih predujmova, odaberite **Odobreni gotovinski predujmovi**, a zatim odaberite **Plati i prenesi**.  
2. Navedite pojedinosti temeljnice za gotovinske predujmove, a zatim odaberite **U redu**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Pošaljite izvješće o troškovima u odnosu na plaćeni gotovinski predujam 

Kada izradite i predate izvješće o trošku za gotovinski predujam koji ste već primili, troškovi će se automatski prilagoditi tom predujmu. Ako je vaš gotovinski predujam veći od utrošenog iznosa, saldo morate vratiti tvrtki s pomoću kategorije troškova **Povrat gotovine**. Ako je gotovinski predujam koji je platila tvrtka manji od iznosa koji ste potrošili, tvrtka vam mora nadoknaditi saldo. 

### <a name="example"></a>Primjer
Planirate putovati na konferenciju iz Splita u Zagreb. Stvorite zahtjev za gotovinski predujam za 5,000,00 kn jer ste procijenili da su troškovi konferencijske karte, letova, hotela, obroka i taksija približno taj iznos. Nećete biti plaćeni sve dok vaš upravitelj ne odobri ovaj zahtjev. Nakon što vaš upravitelj odobri, traženi gotovinski predujam uplaćuje se na vaš bankovni račun u obliku 5.000,00 kn. Zatim sudjelujete na konferenciji. Nakon završetka putovanja utvrdili ste da su ukupni izdaci bili samo 3.000,00 kn. Odaberite mogućnost **Gotovina** u polju **Način plaćanja** i pošaljite svoj trošak na 3.000,00 kn. Iznos vašeg prijavljenog troška automatski se prilagođava gotovinskom predujmu od 5.000,00 kn koji vam je posuđen. Sada tvrtki dugujete preostali iznos od 2.000,00 kn (5.000,00 – 3.000,00) koji tvrtki možete vratiti s pomoću kategorija troškova **Povrat gotovine**. 
