---
title: Gotovinski predujam
description: U ovoj temi nalaze se informacije o gotovinskim predujmovima.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6881fc8251a2d3c7d6af0016780a92358ce63397d09b9a0cde201126cd2912cc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988507"
---
# <a name="cash-advance"></a>Gotovinski predujam

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Gotovinski predujam omogućuje zaposlenicima posudbu novca od njihove tvrtke prije stvaranja bilo kakvih troškova. Kada se odobri i plati traženi gotovinski predujam, zaposlenik može novac upotrijebiti za poslovne troškove koji će možda nastati. 

## <a name="create-and-submit-a-cash-advance-request"></a>Stvaranje i slanje zahtjeva za gotovinski predujam
Kako biste stvorili novi gotovinski predujam i predali zahtjev za gotovinskim predujmom, učinite sljedeće: 

1. Pod stavkom **Moji troškovi** odaberite **Gotovinski predujmovi** > **Novi**. 
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

Kada izradite i predate izvješće o trošku za gotovinski predujam koji ste već dobili, troškovi će se automatski prilagoditi tom predujmu. Ako je vaš gotovinski predujam veći od utrošenog iznosa, saldo morate vratiti tvrtki s pomoću kategorije troškova **Povrat gotovine**. Ako je gotovinski predujam koji je tvrtka platila manji od iznosa koji ste potrošili, tvrtka vam mora nadoknaditi saldo. 

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Odabir gotovinskih predujmova koji se odnose na troškove
Prije nego što pošaljete izvješće o troškovima, možete odabrati gotovinski predujam koji je usklađen s transakcijama troškova u izvješću. Kako biste upotrijebili ovu funkciju, sljedeće dvije značajke moraju biti omogućene iz radnog prostora **Upravljanje značajkama**:

  - Izmijenjena izvješća o trošku
  - Mogućnost mapiranja gotovinskih predujmova u retke troškova
 
 Kad su ove značajke omogućene:
 
  - Možete dodati jedan ili više gotovinskih predujmova za svaki redak troškova.
  - Dostupni saldo gotovinskog predujma vidljiv je u stvarnom vremenu kada se spremi izvješće o troškovima. To vam omogućuje istodobno obrađivanje transakcija troškova i vraćanje gotovinskih transakcija.
  - Možete odabrati više gotovinskih predujmova za jednu transakciju troškova.
  - Podaci za usklađivanje gotovinskog predujma dostupni su s pomoću upita. 
 
Ako ne upotrebljavate ove značajke, funkcionalnost će ostati ista, s postojećim gotovinskim predujmovima koji se automatski smanjuju nakon slanja troškova.

### <a name="example"></a>Primjer 
Planirate putovati na konferenciju iz Seattla u New York. Stvarate zahtjev za gotovinskim predujmom za 3000,00 USD na temelju procijenjenih troškova ulaznice za konferenciju, letova, hotela, obroka i taksija. Isplatu nećete dobiti dok vaš voditelj ne odobri ovaj zahtjev. Nakon što vaš upravitelj odobri, traženi gotovinski predujam uplaćuje se na vaš bankovni račun u obliku 5.000,00 kn. Zatim sudjelujete na konferenciji. Nakon završetka putovanja utvrdili ste da su ukupni izdaci bili samo 3.000,00 kn. Odaberite **Gotovina** u polju **Način plaćanja** i pošaljite svoj trošak od 2790,00 USD. Iznos vašeg prijavljenog troška automatski se prilagođava gotovinskom predujmu od 5.000,00 kn koji vam je posuđen. Sada dugujete saldo od 210,00 USD (3000,00 - 2790,00), koji tvrtki možete vratiti s pomoću troškovne ktegorije **Vrati gotovinu**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
