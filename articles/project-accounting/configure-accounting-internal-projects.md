---
title: Konfiguracija računovodstva za interne projekte
description: U ovoj temi nalaze se informacije o načinu postavljanja računovodstvene prakse za interne projekte u projektnim operacijama.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073322"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfiguracija računovodstva za interne projekte

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Interni projekti omogućuju tvrtkama praćenje troškova povezanih s aktivnostima koje se ne naplaćuju kupcu. Primjeri internih projekata uključuju:

- Razvoj proizvoda, poput mobilne aplikacije, i praćenje troškova povezanih s razvojem.
- Upravljanje vremenom i troškovima pretprodaje. Ovaj pretprodajni interni projekt može se kasnije pretvoriti u projekt koji se može naplatiti ako se prihvati ponuda.

Svaki projekt koji nije povezan s ugovorom u programu Dynamics 365 Project Operations tretira se kao interni. Profili troškova i prihoda projekta ne upotrebljavaju se za određivanje računovodstvenih pravila za projektne. Interni trošak projekta uvijek se knjiži s pomoću načela dobiti i gubitka. Računi glavne knjige za knjiženja definirani su na stranici **Postavljanje knjiženja u Glavnoj knjizi**.

- Vremenske transakcije knjiže se terećenjem računa **Trošak** i kreditiranjem računa **Raspodjela plaća**.
- Troškovne transakcije knjiže se terećenjem računa **Trošak** i kreditiranjem računa **Račun poravnanja za troškove**.

Nakon što su transakcije knjižene u projekt, ako je projekt povezan s ugovorom o projektu, sustav poništava sve nakupljene transakcije i stvara nove naplative transakcije. Transakcije koje se naplaćuju slijede računovodstvena pravila definirana u odgovarajućem profilu troškova i prihoda projekta.


