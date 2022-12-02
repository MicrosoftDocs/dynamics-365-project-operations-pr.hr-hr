---
title: Stvaranje ad hoc predujma za ugovor
description: U ovom se članku navode informacije o stvaranju predujma za ugovor, ako je potrebno.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3e450a17990c6fc783ddffdb05e1ab5b9429a3c1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922167"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Stvaranje ad hoc predujma za ugovor

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Microsoft Dynamics 365 Project Operations podržava scenarije fakturiranja koji uključuju plaćanja unaprijed i predujmove. Postupak uporabe mogućnosti **Predujmovi** u aplikaciji **Project Operations** sličan je ugovorima o **Akontaciji**. 

Izvršite sljedeće korake kako biste klijentu fakturirali predujam.

1. Idite na stranicu **Ugovor o projektu**, a zatim odaberite karticu **Predujmovi i akontacije**.
2. U podrešetki koja sadrži popis svih prethodno zabilježenih predujmova i plaćanja unaprijed odaberite **+ Nova akontacija ugovora o projektu**. 

    Otvara se obrazac **Brzo stvaranje** za bilježenje plaćanja unaprijed ili predujma.
    
3. U donjoj tablici navedena su polja za bilježenje predujma i razmatranja koja treba imati na umu tijekom stvaranja novih:

    | Polje | Opis | Utjecaj na niže razine |
    | --- | --- | --- |
    | **Klijent ugovora projekta** | Ta polja označavaju klijenta na ugovoru kojem će se fakturirati za ovaj predujam. | Ako imate više klijenata na ugovoru i ako svakom od njih trebate fakturirati određeni iznos akontacije ili predujma, za svakog pojedinog klijenta stvorite predujam. |
    | **Opis** | Opis svrhe ili vremena predujma koji će vam pomoći identificirati taj predujam. | Ovaj se opis prikazuje u retku fakture za taj predujam. |
    | **Iznos** | Iznos plaćanja unaprijed ili predujma. | Ovaj se iznos prikazuje u retku fakture za taj predujam. |
    | **Datum fakture** | Datum na koji se klijentu fakturira ovaj predujam. | Ovo je datum za automatizirani postupak stvaranja fakture za stvaranje retka fakture za ovaj predujam. |
    | **Status fakture** | Ovo je postavka mogućnosti koja označava dodaje li se taj predujam u nacrt fakture za ovog klijenta. Moguće su sljedeće vrijednosti:</br>- **Nije spremno za fakturiranje**</br>- **Spremno za fakturiranje** | Kada je avans ili plaćanje unaprijed označeno kao **Spremno za fakturiranje**, dodaje se kao vremenski redak na nacrtu fakture. Samo se potpuno fakturirani predujam može upotrijebiti za usklađivanje s troškovima projekta za sljedeće razdoblje fakture. |

4. Odaberite mogućnost **Spremi i zatvori** u dijaloškom okviru za brzo stvaranje kako biste zabilježili predujam ili plaćanje unaprijed.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]