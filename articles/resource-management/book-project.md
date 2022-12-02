---
title: Rezerviranje za projekt
description: U ovom se članku navode informacije o načinu rezervacije resursa za projekt.
author: ruhercul
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dca9d722eae595af7a81c2b4684729d7658ed012
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928515"
---
# <a name="book-to-a-project"></a>Rezerviranje za projekt

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Postoje slučajevi u kojima će voditelj projekta ili voditelj resursa trebati dodijeliti resurs projektu bez da generički član tima definira određeni zahtjev. To se može postići na jedan od tri načina.

- Rezervacija iz rešetke člana tima.
- Rezerviranje s ploče s rasporedom
- Rezervacija iz obrasca **Projekt**

## <a name="book-from-the-team-member-grid"></a>Rezervacija iz rešetke člana tima.

Ako vaša tvrtka ili ustanova radi u hibridnom načinu raspodjele resursa, voditelj projekta može rezervirati resurs izravno projektu izvršavajući sljedeće korake.

1. Iz projekta idite na rešetku člana tima i odaberite mogućnost **Novi**.
2. Definirajte naziv položaja i ulogu resursa.
3. Odaberite resurs koji možete rezervirati iz dostupnog pretraživanja.
4. Nakon što odaberete resurs, definirajte sljedeće podatke o polju kako biste rezervirali resurs:

    - Datum početka
    - Datum završetka
    - Način dodjele
    - Sati, ako je primjenjivo
    - Odobravatelj projekta

6. Odaberite **Spremi i zatvori**

## <a name="book-from-the-schedule-board"></a>Rezerviranje s ploče s rasporedom

Kada upravitelj resursa treba rezervirati resurs izravno projektu, može upotrijebiti ploču s rasporedom i zahtjev projekta. Preduvjet projekta preduvjet je resursa koji je uvijek dostupan za rezerviranje. Kako biste rezervirali izravno obrascu projekta ploče s rasporedom, izvršite sljedeće korake.

1. Pomaknite se do ploče s rasporedom i na lijevoj stranici filtrirajte resurse koje razmatrate za zahtjev.
2. U donjem oknu odaberite karticu **Projekt** za prikaz popisa projektnih zahtjeva.
3. Povucite zahtjev na resurs i definirajte sljedeće podatke:

    - Datum početka
    - Datum završetka
    - Status rezervacije
    - Način rezervacije
    - Trajanje
   
   > [!NOTE]
   > Dynamics 365 Project Operations trenutačno ne podržava ploču rasporeda.   

## <a name="book-from-the-project-form"></a>Rezervacija iz obrasca Projekt

Kao voditelj projekta, možda ćete trebati rezervirati resurs za projekt, ali znate samo kriterije, a ne i naziv resursa. Izvršite sljedeće korake kako biste s pomoću pomoćnika za raspored pronašli resurs utemeljen na nekom dostupnom atributu resursa. 

1. Pomaknite se do projekta i odaberite mogućnost **Rezerviraj** kako biste otvorili pomoćnika za raspored.
2. S pomoću filtara s lijeve strane pomoćnika za raspored suzite kriterije i odaberite mogućnost **Traži**.
3. Na temelju resursa vraćenih u rezultatima, možete rezervirati resurs.

> [!NOTE]
> Ova metoda ne stvara nikakve rezervacije za resurs. Umjesto toga, ona resurs dodaje timu. Nakon što je član tima dodan u projekt, voditelj projekta može upotrijebiti održavanje rezervacija ili produžiti rezervacije kako bi potrebne resurse dodao resursu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
