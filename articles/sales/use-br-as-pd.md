---
title: Uporaba resursa koji se može rezervirati kao veličine za određivanje cijene
description: U ovom se članku navode informacije o korištenju resursa koji se može rezervirati kao dimenzije određivanja cijena.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c467c45885bbd8931eccc75862f537c0f46433ef
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914807"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Uporaba resursa koji se može rezervirati kao veličine za određivanje cijene

 _**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_ 

U ovom se članku navode informacije o korištenju resursa koji se može rezervirati kao dimenzije određivanja cijena. Ako je vaša strategija određivanja cijena postavljena tako da svaki resurs koji možete rezervirati mora imati određenu cijenu ili cijenu koštanja, upotrijebite resurs koji se može rezervirati kao veličina za određivanje cijene.

## <a name="prerequisites"></a>Preduvjeti
Prije nego što dovršite postupke u ovom članku, morate imati novo rješenje dimenzije određivanja cijena za svoju tvrtku ili ustanovu. Ako ga već niste stvorili, pogledajte odjeljak [Stvaranje prilagođenih polja i entiteta](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Dodavanje polja resursa koji se može rezervirati u obrasce i prikaze
Kako bi polje **Resursi koji se mogu rezervirati** bilo vidljivo u rješenju veličine za određivanje cijena, morate dodati polje svim obrascima i prikazima kao entitet.

U sljedećoj se tablici navode svi gotovi obrasci i prikazi po entitetu. Novo ćete polje morati dodati i u sve dodatne obrasce ili prikaze u svojim prilagođenim entitetima.

|   Entity        | Obrasci   |Prikazi        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cijena uloge| Podaci | - Cijene kategorije aktivnog resursa<br> - Povezane cijene kategorije resursa |
|  Provizija cijene uloge| Podaci| - Provizija na cijenu aktivne uloge<br>- Povezana provizije na cijenu uloge |
|  Pojedinost retka ponude| - Informacije o projektu<br>- Brzo stvaranje projekta| - Pojedinost retka aktivne ponude<br>- Pojedinosti retka složene ponude<br>- Povezana pojedinost retka ponude |
|  Pojedinost retka ugovora projekta| - Informacije o projektu<br>- Brzo stvaranje projekta| - Kombinirane pojedinosti retka ugovora<br>- Pojedinosti aktivnog retka ugovora<br>- Povezana pojedinost retka ugovora |
|  Zadatak projekta| - Podaci<br>- Novi obrazac| &nbsp; |
|  Članov projektnog tima| - Podaci<br>- Novi obrazac| - Aktivni članovi projektnog tima<br>- Članovi projektnog tima<br>- Povezani članovi projektnog tima |
|  Unos vremena| - Podaci<br>- Stvaranje Unosa vremena| - Moji Unosi vremena po datumu<br>- Moji Unosi vremena za ovaj tjedan<br>- Unos vremenai za odobrenje|
|  Redak u dnevniku| - Podaci<br>- Brzo stvaranje| - Redci aktivnog dnevnika<br>- Povezani redak dnevnika |
|  Pojedinost retka fakture| - Podaci<br>- Brzo stvaranje| - Pojedinosti retka aktivne fakture<br>- Naplative transakcije fakture<br>- Besplatne transakcije fakture<br>- Povezane pojedinosti retka fakture <br>- Nenaplative transakcije fakture|
|  Stvarno| - Podaci<br>- Aktivne stvarne vrijednosti| Povezane stvarne vrijednosti |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Postavljanje resursa koji je moguće rezervirati kao veličine za određivanje cijena
Kako biste resurs koji je moguće rezervirati postavili kao veličinu za određivanje cijena, slijedite ove korake:

1. Idite na **Postavke** > **Parametri**. 
2. Na stranici **Parametri**, na kartici **Veličine za određivanje cijena koje se temelje na iznosu**, potvrdite da rešetka prikazuje zapise u entitetu **Veličine za određivanje cijena**. 
2. Dodajte **Resurs koji je moguće rezervirati** na ovaj popis dimenzija određivanja cijena kao **kao msdyn_bookableresource**. 
3. U postavkama **Odnosi se na troškove** i **Odnosi se na prodaju**, odaberite vrijednost.
4. U stavci **Vrsta veličine** odaberite **Koja se temelji na iznosu**. 
5. Odaberite prioritet troškova i prodaje za resurs koji je moguće rezervirati. Uobičajeno je da resurs koji se može rezervirati ima najveći prioritet kada je uključen kao veličina za određivanje cijene. Postavite prioritet na **1** (ili **0** ovisno o tome kako računate prioritet) kako biste osigurali ovo ponašanje.

## <a name="set-up-pricing-dimension-field-names"></a>Postavi nazive polja dimenzije određivanja cijena

Kada se naziv polja veličine za određivanje cijena u tablici **Cijena uloge** razlikuje od naziva polja u nekom drugom entitetu gdje se upotrebljava zadana cijena, zapis veličine za određivanje cijena mora dobiti informaciju o različitim nazivima.  

Za resurs koji je moguće rezervirati, entitet **Članovi projektnog tima** ima malo drugačiji naziv polja od naziva na entitetu **Cijena uloge**: 

 - Entitet **Članovi projektnog tima** = **msdyn_bookableresourceid**
 - Entitet **Cijena uloge** = **msdyn_bookableresource**

Zapis veličine za određivanje cijena za **msydn_bookableresource** mora imati informaciju o toj razlici.

1. Dvaput kliknite redak u rešetki **Veličine za određivanje cijena** kako biste otvorili stranicu veličine **msdyn_bookableresource**.
2. Na stranici dimenzije, na kartici **Povezano** odaberite **Nazivi polja veličine za određivanje cijena**.

  ![Kartica Nazivi polja veličina za određivanje cijena.](media/PD-fieldname.png)

3. Na povezanom prikazu koji se otvori, odaberite **Dodaj novi naziv polja veličine za određivanje cijena**.

  ![Dodajte nove nazive polja veličina za određivanja cijena.](media/Add-NewPD-fieldname.png)

  To otvara stranicu **Novi naziv polja dimenzije određivanja cijena** za **msdyn_bookableresource**. 

4. Na stranici **Novi naziv polja veličine za određivanje cijena** dodajte **msdyn_projectteam** u **Logični naziv entiteta**.
5. Dodajte **msdyn_bookableresourceid** u **Naziv polja**.

 ![Obrazac novog naziva polja veličine za određivanje cijena.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]