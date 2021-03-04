---
title: Stvaranje ručnog predračuna – jednostavno
description: U ovoj temi nalaze se informacije o načinu stvaranja ručnog predračuna u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764494"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Stvaranje ručnog predračuna – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

U aplikaciji Dynamics 365 Project Operations, predračuni se po potrebi mogu stvarati ručno. Možete ručno stvoriti predračun sa stranice s popisom **Ugovori o projektu** ili sa stranice s pojedinostima stavke **Ugovor o projektu**.

##  <a name="project-contracts-list-page"></a>stranica s popisom ugovora o projektu

Na stranici s popisom **Ugovori o projektu** odaberite jedan ili više ugovora o projektu i stvorite račune za sve odabrane zapise.

Sustav provjerava koji od odabranih ugovora o projektu ima zaostale nefakturirane zadatke sa statusom **Spremni za fakturiranje** datirane prije današnjeg datuma. Iz tih ugovora sustav stvara nacrte predračuna. Ako projektni ugovor ima više klijenata, može se stvoriti jedna faktura po klijentu i više faktura po ugovoru o projektu.

Sve stvorene fakture za projekt dostupne su na stranici **Faktura** u odjeljku **Naplata** područja **Prodaja**.

## <a name="project-contract-details-page"></a>Stranica s pojedinostima ugovora o projektu

Predračun se također može stvoriti sa stranice s pojedinostima **Ugovor o projektu**. Sustav provjerava ima li ugovor o projektu zaostalih nefakturiranih zadataka sa statusom **Spremni za fakturiranje** datiranih prije današnjeg datuma. Iz tih ugovora sustav stvara nacrt predračuna na temelju broja klijenata u svakom retku ugovora.

Kada se stvori jedan predračun, otvara se stranica **Račun**. Ako se stvori više računa za taj ugovor o projektu, otvara se stranica s popisom **Fakture** kako bi se prikazale sve stvorene fakture.
