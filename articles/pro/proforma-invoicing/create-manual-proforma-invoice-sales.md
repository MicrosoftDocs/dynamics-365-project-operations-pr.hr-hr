---
title: Stvaranje ručnog predračuna – jednostavno
description: U ovoj temi nalaze se informacije o načinu stvaranja ručnog predračuna u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176377"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Stvaranje ručnog predračuna – jednostavno

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Predračuni se u aplikaciji Dynamics 365 Project Operations, po potrebi mogu stvoriti ručno. Možete ručno stvoriti predračun sa stranice s popisom **Ugovori o projektu** ili sa stranice s pojedinostima stavke **Ugovor o projektu**.

##  <a name="project-contracts-list-page"></a>stranica s popisom ugovora o projektu

Na stranici s popisom **Ugovori o projektu** odaberite jedan ili više ugovora o projektu i stvorite račune za sve odabrane zapise.

Sustav provjerava koji od odabranih ugovora o projektu ima zaostale nefakturirane zadatke **Spremni za fakturiranje** datirane prije današnjeg datuma. Iz tih ugovora sustav stvara nacrte predračuna. Ako projektni ugovor ima više klijenata, može se stvoriti jedna faktura po klijentu i više faktura po ugovoru o projektu.

Sve stvorene fakture za projekt dostupne su na stranici **Faktura** u odjeljku **Naplata** područja **Prodaja**.

## <a name="project-contract-details-page"></a>Stranica s pojedinostima ugovora o projektu

Predračun se može stvoriti i sa stranice s pojedinostima **Ugovor o projektu** koja stvara fakturu za taj određeni ugovor o projektu. Sustav provjerava ima li ugovor o projektu zaostale nefakturirane zadatke **Spremni za fakturiranje** datirane prije današnjeg datuma. Iz tih ugovora sustav stvara nacrt predračuna na temelju broja klijenata u svakom retku ugovora.

Kada se stvori jedan predračun, otvara se stranica **Račun**. Ako postoji više računa izrađenih za taj ugovor o projektu, tada se otvara stranica s popisom **Računi** za prikaz svih stvorenih faktura.
