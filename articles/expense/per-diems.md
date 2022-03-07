---
title: Po danima
description: U ovoj temi nalaze se informacije o pravilima za dnevnice koja se upotrebljavaju za upravljanje troškovima.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073262"
---
# <a name="per-diems"></a>Po danima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_


Dnevnica je naknada koja se isplaćuje radniku koji putuje zbog posla. U upravljanju troškovima možete stvoriti pravila za dnevnice za različite situacije putovanja. Cijene dnevnica mogu se temeljiti na dobu godine, mjestu putovanja ili oboje. Kada stvarate pravilo za dnevnice, možete odrediti da se od dnevnice odbija postotak ako radnik prima besplatne obroke ili usluge. Također možete postaviti minimalni i maksimalni broj sati za koji se dnevnica može primijeniti kada je radnik na putu.

## <a name="configuration"></a>Konfiguracija 

1. Kako biste dodali mjesta za dnevnice, idite na **Postavljanje** > **Izračuni i kodovi** > **Dnevnice**.
2. Za svaku od gore dodanih lokacija odaberite cijenu dnevnice i valutu koja vrijedi između određenog datuma početka i završetka za hotel, obroke i ostale troškove. Stope dnevnica i valute konfigurirane su pod stavkom **Postavljanje** > **Izračuni i kodovi** > **Dnevnice**.
3. Na stranici **Dnevnice**, konfigurirajte razine dnevnica. Razine dnevnica omogućuju vam definiranje postotka podjele dnevnice za hotelske, prehrambene i druge troškove. 
4. Kako biste odredili postotak smanjenja za doručak, ručak ili večeru, ažurirajte polja na stranici **Parametri upravljanja troškovima**, na kartici **Dnevnice**. 
    
## <a name="submit-expenses-using-per-diem"></a>Slanje troškova s pomoću dnevnice
Kako biste poslali troškove korištenja dnevnica, kada stvarate izvješće o troškovima upotrijebite kategoriju troška **Dnevnice**. Unesite podatke **Dnevnica od datuma**, **Dnevnica do datuma** i **Dnevnica za mjesto**. Iznos će se izračunati na temelju iznosa dnevnice za odabranu lokaciju, a smanjenje obroka na temelju razina dnevnica.
