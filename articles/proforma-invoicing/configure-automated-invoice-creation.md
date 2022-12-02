---
title: Konfiguriranje automatskog stvaranja fakture
description: U ovom se članku navode informacije o načinu konfiguriranja sustava za automatsko generiranje faktura.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 273e00e7841c8a34e249e54a7d868034bc34a1f7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920603"
---
# <a name="configure-automatic-invoice-creation"></a>Konfiguriranje automatskog stvaranja fakture

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_


Dovršite sljedeće korake kako biste konfigurirali automatiziranu fakturu koja se izvršava u aplikaciji Dynamics 365 Project Operations.

1. Idite na **Postavke** > **Skupni poslovi**.
2. Stvorite skupni posao i dodijelite mu naziv **Fakture stvorene u aplikacije Project Operations**. Naziv skupnog posla mora sadržavati riječi „stvaranje faktura”.
3. U polju **Vrsta posla** odaberite **Ništa**. Prema zadanim postavkama mogućnosti **Dnevna učestalost** i **Aktivno** postavljene su na **Da**.
4. Odaberite **Pokreni tijek rada**. U dijaloškom okviru **Pretraživanje zapisa** vidjet ćete tri tijeka rada:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Odaberite **ProcessRunCaller**, a zatim **Dodaj**.
6. U sljedećem dijaloškom okviru odaberite **U redu**. Nakon tijeka rada **Sleep** slijedi tijek rada **Process**.

  > [!NOTE]
  > U petom koraku možete odabrati i **ProcessRunner**. Zatim, kada odaberete **U redu**, nakon tijeka rada **Process** slijedi tijek rada **Sleep**.

Tijekovi rada **ProcessRunCaller** i **ProcessRunner** stvaraju fakture. **ProcessRunCaller** poziva **ProcessRunner**. **ProcessRunner** jest tijek rada koji stvara fakture. Prolazi kroz sve retke ugovora za koje je potrebno stvoriti fakture i stvara fakture za te retke. Da bi se odredili reci ugovora za koje je potrebno stvoriti fakture, posao traži datume stvaranja faktura za retke ugovora. Ako reci ugovora koji pripadaju jednom ugovoru imaju isti datum stvaranja fakture, transakcije se kombiniraju u jednu fakturu koja ima dva retka fakture. Ako nema transakcija za stvaranje faktura, posao preskače stvaranje faktura.

Nakon pokretanja funkcije **ProcessRunner** poziva se **ProcessRunCaller**, navodi se vrijeme završetka i funkcija se zatvara. **ProcessRunCaller** zatim pokreće mjerač vremena koji se izvodi 24 sata od navedenog vremena završetka. Po završetku izvođenja mjerača vremena funkcija **ProcessRunCaller** zatvara se.

Skupni postupak stvaranja faktura ponavljajući je posao. Ako se taj skupni postupak izvodi više puta, stvaraju se višestruke instance posla koje uzrokuju pogreške. Stoga biste trebali pokrenuti skupni postupak samo jednom i ponovno ga pokrenuti samo ako se prestane izvoditi.

> [!NOTE]
> Skupno fakturiranje izvršava se samo za retke ugovora o projektu koji su konfigurirani prema rasporedu faktura. Ugovorni redci s načinom naplate fiksne cijene moraju imati konfigurirane prekretnice. Redak projektnog ugovora s vremenskim i materijalnim načinom naplate treba imati postavku rasporeda računa na temelju datuma. Isto se odnosi i na redak ugovora koji se temelji na projektu.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]