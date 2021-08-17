---
title: Postavke projekta
description: Ova tema pruža informacije o upravljanju postavkama projekta.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 5f6fec091c50f35589e333fce4b3a296dd736d10dd2f56b6c11209a55b493836
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996922"
---
# <a name="project-settings"></a>Postavke projekta

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Koristite sljedeće postavke da biste pristupili značajkama planiranja projekta.

## <a name="work-template"></a>Poslovni predložak

Da biste stvorili raspored projekta, stvorite predložak kalendara projekta koji definira radno vrijeme po danu i neradno vrijeme. Da biste stvorili predložak kalendara projekta, povežite radni predložak s poljem **Predložak kalendara** za projekt. Poduzmite ove korake da biste stvorili radni predložak.

1. U PSA-u u navigacijskom oknu slijeva kliknite **Resursi**. 
2. Na stranici popisa **Resursi** otvorite zapis korisnika, a zatim odaberite **Prikaži radno vrijeme**.

  > [!NOTE]
  > Provjerite jeste li omogućili skočne prozore na stranici preglednika. To vam omogućuje da vidite radno vrijeme postavljeno za resurs.
  
3. Na kartici **Mjesečni prikaz** kliknite **Postavi**. Prikazat će se popis s tri mogućnosti: 

  - Novi tjedni raspored
  - Radni raspored za jedan dan
  - Slobodno vrijeme

> ![Postavite mogućnosti.](media/project-13.png)

4. Odaberite **Novi tjedni raspored**, a zatim postavite mogućnosti za ovaj raspored resursa. Možete postaviti tjedni raspored s ponavljanjem, parametre dnevnih sati, neradno vrijeme itd.
5. Postavite datumski raspon, odaberite **Spremi**, a zatim kliknite **Zatvori**. 
6. Vratite se na stranicu popisa **Resursi** i odaberite resurs za koji ste postavili radno vrijeme. 
7. Odaberite **Postavi kalendar kao** da biste postavili predložak rada. 
8. U dijaloškom okviru **Radni predložak** unesite naziv radnog predloška, a zatim odaberite **Primijeni**. 

Sada možete povezati predložak rada s predloškom kalendara projekta.

## <a name="resource-roles"></a>Uloge resursa

Izraz *uloga resursa* odnosi se na skup vještina, kompetencija i certifikacija koje osoba mora imati za obavljanje određenog skupa zadataka u projektu. PSA omogućuje određivanje troška i naplate vremena resursa na temelju uloge s kojim je resurs povezan. Svaka tvrtka ili ustanova mora postaviti te uloge pomoću lijeve navigacijske trake na izborniku **Project Service**.

Svaka tvrtka ili ustanova mora postaviti te uloge na stranici **Kategorije aktivnih resursa**. Da biste otvorili tu stranicu, u lijevom navigacijskom oknu odaberite **Uloge resursa**.

## <a name="price-lists"></a>Cjenici

Cjenici vam omogućuju da odredite trošak i prodajne cijene za uloge resursa u organizaciji, kategorije troškova, proizvode i druge elemente u tvrtki ili ustanovi. Prije nego što postavite financijske procjene za isporučeni rad u projektu, trebate stvoriti sigurnosni trošak i prodajni cjenik. U odjeljku parametara također trebate postaviti zadani trošak i prodajni cjenik koji se primjenjuje na sve projekte koji su stvoreni u tvrtki ili ustanovi. Na stranici **Parametri aktivnog projekta** provjerite jeste li postavili zadani trošak i prodajni cjenik.


[!INCLUDE[footer-include](../includes/footer-banner.md)]