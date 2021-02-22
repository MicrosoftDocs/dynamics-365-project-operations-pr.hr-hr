---
title: Pregled priznavanja prihoda
description: U ovoj temi nalaze se informacije o priznavanju prihoda u aplikaciji Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531380"
---
# <a name="revenue-recognition-overview"></a>Pregled priznavanja prihoda

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Načela priznavanja prihoda u aplikaciji Dynamics 365 Project Operations razlikuju se ovisno o odabranom načinu naplate za projekt ili dio projekta. U ovoj temi nalaze se informacije o priznavanju prihoda u aplikaciji Project Operations.

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