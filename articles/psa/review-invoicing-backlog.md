---
title: Pregled zaostalih faktura u projektima i ugovorima o projektima
description: Ovaj članak pruža informacije o tome kako pregledati vrijeme, trošak i zaostale podatke o proizvodu te kako ih označiti kao spremne za fakturiranje.
author: rumant
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 833ace7fd6285191f4b023a029286cd36b5de8f4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928883"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Pregled zaostalih faktura u projektima i ugovorima o projektima

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Kada je transakcija spremna za izradu i obradu fakture, transakcija bi trebala imati oznaku **Spremno za fakturiranje**. Ovaj članak opisuje vrste transakcija koje se mogu izraditi.

## <a name="review-the-time-and-material-billing-backlog"></a>Pregled zaostale naplate za vrijeme i materijal

Kada je Unos vremena ili troška poslan i odobren za projekt, PSA stvara stvarni podatak projekta. Ako je kombinacija projekta i vrste transakcije preslikana u redak ugovora za projekt vremena i materijala, kad se unos odobri, nastaju dva stvarna podatka:

- Stvarni podatak o trošku 
- Stvarni podatak o nenaplaćenim prodajama

Stvarni podaci o nenaplaćenim prodajama predstavljaju zaostale naplate, a njihov status naplate mora biti postavljen na **Spremno za fakturiranje**. Kada se izradi faktura projekta, stvarni podaci o nenaplaćenim prodajama koji su označeni **Spremno za fakturiranje** kopiraju se kao pojedinosti retka fakture.

Da biste pregledali zaostale naplate za vrijeme i materijale, otvorite **Prodaja** \> **Naplata** \> **Zaostale naplate za vrijeme i materijal**. Odaberite sve nenaplaćene stvarne podatke o prodaji koji su spremni za fakturiranje, a zatim odaberite **Spremno za fakturiranje**. Status naplate tih stvarnih podataka mijenja se u **Spremno za fakturiranje**.

![Zaostale naplate za vrijeme i materijal.](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Pregled zaostalih naplata za proizvod

Kada ugovor o projektu ima retke ugovora temeljene na proizvodu, ti se reci uzimaju u obzir za fakturiranje kad god se izradi faktura za ugovor o projektu. Svaki proizvod koji ima retke ugovora koji su označeni sa **Spremno za fakturiranje** kopira se u fakturu projekta u obliku redaka fakture projekta.

Da biste pregledali zaostale naplate za proizvode, otvorite **Prodaja** \> **Naplata** \> **Zaostale naplate za proizvod**. Odaberite sve retke ugovora temeljene na proizvodu koji su spremni za fakturiranje, a zatim odaberite **Spremno za fakturiranje**. Status naplate tih redaka mijenja se u **Spremno za fakturiranje**.

![Zaostale naplate za proizvod.](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Pregled kontrolnih točaka naplate u ugovorima s fiksnom cijenom

Svaki redak ugovora o projektu koji ima način naplate s fiksnom cijenom mora imati kontrolne točke ugovora. Te Kontrolne točke ugovora mogu se fakturirati samo ako imaju oznaku **Spremno za fakturiranje**. 

Da biste pregledali kontrolne točke naplate, otvorite **Prodaja** \> **Naplata** \> **Kontrolne točke fiksne cijene**. Odaberite kontrolne točke koje su spremne za fakturiranje, a zatim odaberite **Spremno za fakturiranje**. Status naplate tih kontrolnih točaka mijenja se u **Spremno za fakturiranje**.

![Kontrolne točke fiksne cijene.](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
