---
title: Pregled priznavanja prihoda
description: U ovom članku nalaze se informacije o priznavanju prihoda u aplikaciji Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 22486693226256f765589b272e6df36aceaf9c1c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926261"
---
# <a name="revenue-recognition-overview"></a>Pregled priznavanja prihoda

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Načela priznavanja prihoda u aplikaciji Dynamics 365 Project Operations razlikuju se ovisno o odabranom načinu naplate za projekt ili dio projekta. U ovom članku nalaze se informacije o priznavanju prihoda u aplikaciji Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Obračun transakcija za koje se upotrebljava način naplate vremena i materijala

- Priznavanje troškova i prihoda povezano je. Troškovi transakcije i nenaplaćene prodaje knjiže se s pomoću [Dnevnika integracije aplikacije Project Operations](../project-accounting/project-operations-integration-journal.md).
- Profil troškova i prihoda projekta određuje jesu li nenaplaćene prodajne transakcije knjižene u glavnu knjigu. Ako je odabran **Akumulirani prihod**, sustav tijekom knjiženja upotrebljava račune **WIP prodajna vrijednost** i **Prodajna vrijednost akumuliranog prihoda**. Slijedi primjer ovog načina.  

  | Vrsta transakcije | Terećenje/kredit | Iznos |
  | --- | --- | --- |
  | WIP prodajna vrijednost | Terećenje | 100 |
  | Prodajna vrijednost akumuliranog prihoda | Kredit | 100 |

- Prihod se priznaje tijekom fakturiranja. Tijekom knjiženja sustav upotrebljava račun **Fakturirani prihod**. Slijedi primjer ovog načina.  

  | Vrsta transakcije | Terećenje/kredit | Iznos |
  | --- | --- | --- |
  | Saldo klijenta | Terećenje | 120 |
  | Plaća se porez na promet | Kredit | 20 |
  | Fakturirani prihod | Kredit | 100 |

- Ako je prihod nastao pri knjiženju nenaplaćene prodaje, sustav će pri fakturiranju stornirati prihod.

  | Vrsta transakcije | Terećenje/kredit | Iznos |
  | --- | --- | --- |
  | WIP prodajna vrijednost | Kredit | 100 |
  | Prodajna vrijednost akumuliranog prihoda | Terećenje | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Obračun transakcija za koje se upotrebljava način naplate fiksnom cijenom

- Priznavanje troškova i prihoda odvojeno je. Troškovi transakcije knjiže se s pomoću [Dnevnika integracije aplikacije Project Operations](../project-accounting/project-operations-integration-journal.md). Nenaplaćene se prodajne transakcije ne stvaraju.
- Prihod se može priznati tijekom fakturiranja ako profil troškova i prihoda projekta ima **Načelo upotrijebljeno za izračun završetka projekta** postavljeno na **Bez WIP-a**. Ovaj način upotrebljavajte samo za kratkoročne, jednostavne projekte.
- Prihod se može priznati s pomoću procjene prihoda od fiksne cijene, bilo načinom **Ugovor dovršen** ili **Priznavanje prihoda od postotka dovršenosti**.

## <a name="additional-resources"></a>Dodatni resursi
[Konfiguriranje računovodstva za naplative proizvode iz projekata](../project-accounting/configure-accounting-billable-projects.md)

[Projekti s procjenom prihoda od fiksne cijene](rev-rec-percentage-completion-method.md)

[Upravljanje procjenama prihoda](rev-rec-completed-contract-method.md)

[Načini troškova do završetka](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]