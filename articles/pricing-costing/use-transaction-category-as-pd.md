---
title: Uporaba kategorije transakcije kao veličine za određivanje cijene
description: U ovom se članku navode informacije o korištenju polja Kategorija transakcije kao dimenzije određivanja cijena.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 648933299616a683b19bbe2f1231caac779bd1f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911685"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Uporaba kategorije transakcije kao veličine za određivanje cijene


_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_


U ovom se članku objašnjava kako koristiti **polje Kategorija** transakcije kao dimenziju određivanja cijena. 

## <a name="prerequisites"></a>Preduvjeti
Prije nego što dovršite postupke u ovom članku, morate imati novo rješenje dimenzije određivanja cijena za svoju tvrtku ili ustanovu. Ako ga već niste stvorili, pogledajte odjeljak [Stvaranje prilagođenih polja i entiteta kao veličina za određivanje cijena](create-custom-fields-entities-pricing-dimensions.md).

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]