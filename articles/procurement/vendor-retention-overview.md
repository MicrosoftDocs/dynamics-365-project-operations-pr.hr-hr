---
title: Pregled zadržavanja dijela plaćanja dobavljaču
description: U ovoj temi nalazi se pregled mogućnosti zadržavanja dijela plaćanja dobavljaču.
author: sigitac
ms.date: 10/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5f89904af5fb00eac46de834a438f412b371e74e
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594571"
---
# <a name="vendor-retention-overview"></a>Pregled zadržavanja dijela plaćanja dobavljaču

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Vaša će tvrtka ili ustanova možda htjeti zadržati dio plaćanja dobavljačima koji rade na njezinim projektima. Na primjer, prije nego što platite dobavljaču, možda biste htjeli biti sigurni da stavke i usluge koje obavljaju ispunjavaju vaša očekivanja.

Kada s dobavljačima pregovarate o nabavi za projekte, možete odrediti uvjete zadržavanja dijela plaćanja dobavljaču koji obuhvaćaju postotak ili iznos koji treba zadržati. Kako dobavljač isporučuje stavke i usluge, na ime zadržavanja oduzimate određeni postotak ili iznos od uplate dobavljaču. Kad se projekt dovrši ili dosegne međufazu kako je navedeno u ugovoru s dobavljačem, oslobađate zadržani iznos i vršite plaćanje dobavljaču.

## <a name="vendor-retention-example"></a>Primjer zadržavanja dijela plaćanja dobavljaču

Sljedeći primjer pokazuje kako se zadržava postotak iznosa fakture dobavljača na temelju postotka kompletnosti projekta.

Contoso Robotics USA ugovorio je s dobavljačem, tvrtkom Fabrikam, isporuku 100 sati obuke za projekt obnove opreme. Ukupna vrijednost ugovora je 30.000 USD s dogovorenom kupovnom cijenom od 300 USD po satu.

Obuka će se odvijati u tri faze prema sljedećem rasporedu:

- Faza 1: 50 sati ili 50 posto projekta
- Faza 2: 30 sati ili 80 posto od ukupnog projekta
- Faza 3: 20 sati ili 100 posto projekta

U sljedećoj tablici navedeni su rokovi zadržavanja.

| **Postotak isporučenih jedinica** | **Postotak zadržavanja** | **Postotak oslobađanja** |
| --- | --- | --- |
| 50 % | 20 % | 0 % |
| 80 % | 10 % | 10 % |
| 100 % | 0 % | 100 % |

Transakcije rezultiraju sljedećim iznosima:

- Faza 1:
  - Iznos za plaćanje je 50 x 300 ili 15.000.
  - Zadržava se 20 posto iznosa tj. 3.000, koji se oslobađa u kasnijoj fazi.
  - Iznos koji se plaća dobavljaču je 12.000.
- Faza 2:
  - Iznos za plaćanje je 30 x 300 tj. 9.000.
  - Zadržava se 10 posto iznosa tj. 900.
  - Oslobađa se 10 posto od 3.000 koliko je zadržano u prvoj fazi tj. 300.
  - Iznos koji se plaća dobavljaču je 8.400. Taj je iznos 9.000, umanjen za iznos zadržavanja od 900, uvećan za iznos od 300 koji je oslobođen od iznosa zadržanog u prvoj fazi.
- Faza 3:
  - Iznos za plaćanje je 20 x 300 tj. 6.000.
  - Nema zadržavanja iznosa.
  - Oslobođen je iznos od 3.600. Taj se iznos sastoji od 3.000 koje su zadržane u prvoj fazi, umanjen za iznos od 300 iz prve faze koji je oslobođen u drugoj fazi, uvećan za iznos od 900 koji je zadržan u drugoj fazi.
  - Iznos koji se plaća dobavljaču je 9.600. Taj se iznos sastoji od zadržanog iznosa od 3.600 uvećanog za iznos od 6.000 za završetak 3. faze.

Ukupan iznos plaćen dobavljaču nakon završetka tri faze je 30.000, što je ukupan iznos iz narudžbenice (15.000 + 9.000 + 6.000).
