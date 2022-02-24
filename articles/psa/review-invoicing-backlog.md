---
title: Pregled zaostalih faktura u projektima i ugovorima o projektima
description: Ovaj tema pruža informacije o tome kako pregledati vrijeme, trošak i zaostale podatke o proizvodu te kako ih označiti kao spremne za fakturiranje.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 092455a131f556e4f943f6bb89d7e38358f0a697
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150479"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Pregled zaostalih faktura u projektima i ugovorima o projektima

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Kada je transakcija spremna za izradu i obradu fakture, transakcija bi trebala imati oznaku **Spremno za fakturiranje**. Ovaj tema opisuje vrste transakcija koje se mogu izraditi.

## <a name="review-the-time-and-material-billing-backlog"></a>Pregled zaostale naplate za vrijeme i materijal

Kada je Unos vremena ili troška poslan i odobren za projekt, PSA stvara stvarni podatak projekta. Ako je kombinacija projekta i vrste transakcije preslikana u redak ugovora za projekt vremena i materijala, kad se unos odobri, nastaju dva stvarna podatka:

- Stvarni podatak o trošku 
- Stvarni podatak o nenaplaćenim prodajama

Stvarni podaci o nenaplaćenim prodajama predstavljaju zaostale naplate, a njihov status naplate mora biti postavljen na **Spremno za fakturiranje**. Kada se izradi faktura projekta, stvarni podaci o nenaplaćenim prodajama koji su označeni **Spremno za fakturiranje** kopiraju se kao pojedinosti retka fakture.

Da biste pregledali zaostale naplate za vrijeme i materijale, otvorite **Prodaja** \> **Naplata** \> **Zaostale naplate za vrijeme i materijal**. Odaberite sve nenaplaćene stvarne podatke o prodaji koji su spremni za fakturiranje, a zatim odaberite **Spremno za fakturiranje**. Status naplate tih stvarnih podataka mijenja se u **Spremno za fakturiranje**.

![Zaostale naplate za vrijeme i materijal](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Pregled zaostalih naplata za proizvod

Kada ugovor o projektu ima retke ugovora temeljene na proizvodu, ti se reci uzimaju u obzir za fakturiranje kad god se izradi faktura za ugovor o projektu. Svaki proizvod koji ima retke ugovora koji su označeni sa **Spremno za fakturiranje** kopira se u fakturu projekta u obliku redaka fakture projekta.

Da biste pregledali zaostale naplate za proizvode, otvorite **Prodaja** \> **Naplata** \> **Zaostale naplate za proizvod**. Odaberite sve retke ugovora temeljene na proizvodu koji su spremni za fakturiranje, a zatim odaberite **Spremno za fakturiranje**. Status naplate tih redaka mijenja se u **Spremno za fakturiranje**.

![Zaostale naplate za proizvod](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Pregled kontrolnih točaka naplate u ugovorima s fiksnom cijenom

Svaki redak ugovora o projektu koji ima način naplate s fiksnom cijenom mora imati kontrolne točke ugovora. Te Kontrolne točke ugovora mogu se fakturirati samo ako imaju oznaku **Spremno za fakturiranje**. 

Da biste pregledali kontrolne točke naplate, otvorite **Prodaja** \> **Naplata** \> **Kontrolne točke fiksne cijene**. Odaberite kontrolne točke koje su spremne za fakturiranje, a zatim odaberite **Spremno za fakturiranje**. Status naplate tih kontrolnih točaka mijenja se u **Spremno za fakturiranje**.

![Kontrolne točke fiksne cijene](media/FPBacklog.png)
