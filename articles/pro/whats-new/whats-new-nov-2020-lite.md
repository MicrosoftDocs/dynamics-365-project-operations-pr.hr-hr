---
title: Novosti u studenom 2020 – Jednostavna implementacija aplikacije Project Operations – od sklapanja posla do predračuna
description: U ovoj temi nalaze se informacije o ažuriranjima kvalitete dostupnim u izdanju osnovne implementacije aplikacije Project Operations za studeni 2020. – od sklapanja posla do predračuna.
author: sigitac
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a65ab00c7f729b72cc32b4786055feba4aaee452ac4cf413047f81651c92290
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003267"
---
# <a name="whats-new-november-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Novosti u studenom 2020 – Jednostavna implementacija aplikacije Project Operations – od sklapanja posla do predračuna

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

U sljedećoj tablici navode se ažuriranja za aplikaciju Project Operations u verziji 4.4.0.70. okruženja platforme CDS.

| Područje značajke                 | Broj reference | Ažuriranja kvalitete                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Upravljanje prilikama       | 2036993          | Redak procjene i redci ugovora za dodjelu resursa ažuriraju se na usvojenim ponudama kada je vrsta retka ponude **Svi zadaci**.                                                 |
|   Upravljanje prilikama       | 2071514          | Nije moguće stvoriti fakturu za kontrolnu točku s fiksnom cijenom na ugovoru koji ima omogućenu naplatu na temelju zadataka.                                                                          |
| Naplata i određivanje cijene          | 2070392          | Redci ugovora o projektu na fakturi se svaki put povećavaju kada se odabere **Osvježi transakcije fakture**.                                                                       |
| Planiranje projekta             | 2043336          | Nije moguće izbrisati zapis o članu projektnog tima.                                                                                                                                    |
| Planiranje projekta             | 2046013          | Nedosljedno ponašanje za stupce procjene oznaka tijekom učitavanja u odnosu na promjenu vrste vremenske faze.                                                                                   |
| Planiranje projekta             | 2046647          | Vrijeme početka i završetka isključuje se za sat vremena kada članovi projektnog tima generiraju zahtjeve za resursima.                                                                      |
| Planiranje projekta             | 2053879          | (Prema predstojećoj implementaciji CDS-a) PublishUnassignedAssignments prekida pokušaj spremanja zadatka kada je pogreška „Vrijednost proslijeđena za ConditionOperator.In je prazna." |
| Planiranje projekta             | 2055501          | Ostavljanje stavke **Datum početka projekta** praznom uzrokuje neuspjeh u rasporedu.                                                                                                      |
| Planiranje projekta             | 2066817          | Nije moguće stvoriti generički resurs s pomoću alata za odabir ljudi na kartici **Zadaci**.                                                                                               |
| Planiranje projekta             | 2067034          | Gumb **Prikaži pojedinosti** nije dostupan na stranici **Pojedinosti o zadatku**.                                                                                                         |
| Upravljanje resursima          | 2046667          | Generički članovi tima ne brišu se ni nakon što su svi resursi ispunjeni.                                                                                                     |
| Vrijeme i brzi unos troška | 2047499          | Gumb **Novi** na stranici Unos vremena otvara stranicu **Novi potpis e-pošte**.                                                                                               |
| Vrijeme i brzi unos troška | 2059859          | Neočekivani skočni prozor otvara se tijekom stvaranja unosa troška.                                                                                                                         |
| Drugo                        | 2044181          | [Deinstalacija narudžbenice] – Pogreška, „Zapis nije dostupan” pojavljuje se kada pokušate deinstalaciju **msdyn_ProjectServiceCore_Patch** i osnovna rješenja za msdyn Project service.        |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]