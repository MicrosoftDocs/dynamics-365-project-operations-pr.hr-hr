---
title: Konfiguracija računovodstva za interne projekte
description: U ovoj temi nalaze se informacije o načinu postavljanja računovodstvene prakse za interne projekte u projektnim operacijama.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 65d05e3a6321dc32aee55c28b3eaa4bd0bae2f86
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857969"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfiguracija računovodstva za interne projekte

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Interni projekti omogućuju tvrtkama praćenje troškova povezanih s aktivnostima koje se ne naplaćuju klijentu. Primjeri internih projekata uključuju:

- Razvoj proizvoda, poput mobilne aplikacije, i praćenje troškova povezanih s razvojem.
- Upravljanje vremenom i troškovima pretprodaje. Ovaj pretprodajni interni projekt može se kasnije pretvoriti u projekt koji se može naplatiti ako se prihvati ponuda.

Svaki projekt koji u aplikaciji Dynamics 365 Project Operations nije povezan s ugovorom, tretira se kao interni. Profili troškova i prihoda projekta ne upotrebljavaju se za određivanje računovodstvenih pravila za projektne. Interni trošak projekta uvijek se knjiži s pomoću načela dobiti i gubitka. Računi glavne knjige za knjiženja definirani su na stranici **Postavljanje knjiženja u Glavnoj knjizi**.

- Vremenske transakcije knjiže se terećenjem računa **Trošak** i kreditiranjem računa **Raspodjela plaća**.
- Troškovne transakcije knjiže se terećenjem računa **Trošak** i kreditiranjem računa **Račun poravnanja za troškove**.
- Transakcije stavki knjiže se terećenjem računa **Trošak**, a u korist računa **Trošak – Stavka**.

Nakon što su transakcije knjižene u projekt, ako je projekt povezan s ugovorom o projektu, sustav poništava sve nakupljene transakcije i stvara nove naplative transakcije. Transakcije koje se naplaćuju slijede računovodstvena pravila definirana u odgovarajućem profilu troškova i prihoda projekta.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
