---
title: Projekti s procjenom prihoda od fiksne cijene
description: U ovom članku nalaze se informacije o prihodu od projekta s fiksnom cijenom.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928377"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Projekti s procjenom prihoda od fiksne cijene 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Kada stvarate redak ugovora o projektu sa sljedećim atributima u aplikaciji Dynamics 365 Project Operations rješenja Microsoft Dataverse, sustav automatski stvara projekt s procjenom prihoda od fiksne cijene. Podaci u ovom projektu temelje se na sljedećem:

  - Načinu naplate s fiksnom cijenom.
  - Povezanom projektu.
  - Najmanje jednoj kontrolnoj točki definiranoj na kartici **Raspored faktura**, na stranici **Redak ugovora o projektu**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Pregled projekata s procjenom prihoda od fiksne cijene
Kako biste pregledali projekte s procjenom prihoda od fiksne cijene, poduzmite sljedeće korake:

1. U okruženju aplikacije Dynamics 365 Finance idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Projekti s procjenom prihoda od fiksne cijene**.
2. Odaberite projekt koji želite pogledati i dvaput kliknite na stavku **ID procjene projekta** kako biste otvorili zapisnik i pregledati pojedinosti projekta.
3. Proširite karticu **Projekt**. Vidjet ćete jedan projekt u rešetki **Odabrani projekti**. Sustav to upotrebljava kao zadani projekt jer je to projekt povezan s retkom ugovora o projektu. 
4. Kako biste promijenili povezanost, odaberite dodatne projekte i dodajte ih rešetki **Odabrani projekti**. Ako je u ovoj rešetki odabrano više projekata, postotak dovršenosti projekta i procjene prihoda izračunavaju se zajedno za sve odabrane projekte.

  Troškovi projekta, profil prihoda, predložak troškova i kôd razdoblja mogu se postaviti ručno. Ako se ne postave ručno, vrijednosti će se zadati tijekom prvog izračuna procjene za projekt s pomoću pravila konfiguriranih za profile troškova i prihoda projekta.



[!INCLUDE[footer-include](../includes/footer-banner.md)]