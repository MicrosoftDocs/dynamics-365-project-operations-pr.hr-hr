---
title: Uporaba kategorije transakcije kao veličine za određivanje cijene
description: U ovoj temi nalaze se informacije o načinu uporabe polja kategorije transakcije kao veličine za određivanje cijena.
author: rumant
manager: tfehr
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bace11455d34fdda95e08be1a7cc37850a0cf589
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513968"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Uporaba kategorije transakcije kao veličine za određivanje cijene


_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_


U ovoj se temi objašnjava način uporabe polja **Kategorija transakcije** kao veličine za određivanje cijena. 

## <a name="prerequisites"></a>Preduvjeti
Prije nego što dovršite postupke iz ove teme, morate imati novo rješenje veličine za određivanje cijena za svoju tvrtku ili ustanovu. Ako ga već niste stvorili, pogledajte odjeljak [Stvaranje prilagođenih polja i entiteta kao veličina za određivanje cijena](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Dodavanje polja Kategorija transakcije u obrasce i prikaze
Kako bi polje **Kategorija transakcije** bilo vidljivo u rješenju veličine za određivanje cijena, morate dodati polje svim obrascima i prikazima kao entitet.

U sljedećoj se tablici navode svi gotovi obrasci i prikazi po entitetu. Novo ćete polje morati dodati i u sve dodatne obrasce ili prikaze u svojim prilagođenim entitetima.

|  Entity        | Obrasci     |Prikazi        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cijena uloge| Podaci |- Cijene kategorije aktivnog resursa<br> - Povezane cijene kategorije resursa |
|  Provizija cijene uloge| Podaci|- Provizija na cijenu aktivne uloge<br>- Povezana provizije na cijenu uloge |
|  Pojedinost retka ponude|- Informacije o projektu<br>- Brzo stvaranje projekta| - Pojedinost retka aktivne ponude<br>- Pojedinosti retka složene ponude<br>- Povezana pojedinost retka ponude |
|  Pojedinost retka ugovora projekta|- Informacije o projektu<br>- Brzo stvaranje projekta|- Kombinirane pojedinosti retka ugovora<br>- Pojedinosti aktivnog retka ugovora<br>- Povezana pojedinost retka ugovora |
|  Zadatak projekta|- Podaci<br>- Novi obrazac| &nbsp; |
|  Članov projektnog tima|- Podaci<br>- Novi obrazac|- Aktivni članovi projektnog tima<br>- Članovi projektnog tima<br>- Povezani članovi projektnog tima |
|  Unos vremena|- Podaci<br>- Stvaranje Unosa vremena|- Moji Unosi vremena po datumu<br>- Moji Unosi vremena za ovaj tjedan<br>- Unosi vremena za odobrenje|
|  Redak u dnevniku|- Podaci<br>- Brzo stvaranje|- Redci aktivnog dnevnika<br>- Povezani redak dnevnika|
|  Pojedinost retka fakture|- Podaci<br>- Brzo stvaranje|- Pojedinosti retka aktivne fakture<br>- Naplative transakcije fakture<br>- Besplatne transakcije fakture<br>- Povezane pojedinosti retka fakture <br>- Nenaplative transakcije fakture|
|  Stvarno|- Podaci<br>- Aktivne stvarne vrijednosti| Povezane stvarne vrijednosti |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Postavljanje polja Kategorije transakcija kao veličine za određivanje cijena

1. Idite na **Postavke** > **Parametri**. 
2. Na stranici **Parametri**, na kartici **Veličine za određivanje cijena koje se temelje na iznosu**, potvrdite da rešetka prikazuje zapise u entitetu **Veličine za određivanje cijena**.
3. Dodajte **Kategorija transakcije** na ovaj popis i postavite polja **Primjenjivo na trošak** i **Primjenjivo na prodaju** na **Da**.
4. U polju **Vrsta veličine** odaberite **Utemeljeno na iznosu**, a zatim odaberite prioritet za **Kategoriju transakcije** jer je povezana s troškom i prodajom.
