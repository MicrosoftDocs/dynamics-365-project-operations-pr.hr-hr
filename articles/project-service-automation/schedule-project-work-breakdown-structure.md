---
title: Raspoređivanje projekta sa strukturnom analizom rada
description: Raspoređivanje projekta sa strukturnom analizom rada u programu Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ca9b899c-7791-4990-b02e-cdff7f652621
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 003a1c543163b7ef1df1221d0b633a078e6619cf
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750173"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Raspoređivanje projekta sa strukturnom analizom rada (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Raspored projekta objašnjava koji posao treba učiniti, koji će resursi izvesti posao i koji je vremenski okvir u kojem posao treba biti dovršen. Raspored projekta odražava sve poslove povezane s pravovremenom isporukom projekta. Jedan od prvih koraka u fazi pokretanja projekta je utvrđivanje rasporeda projekta. Da biste utvrdili raspored projekta, morate stvoriti strukturnu analizu rada.  
  
 Stvorite strukturu projekta sa strukturnom analizom rada što će vam pomoći da:  
  
- Raščlanite posao na zadatke kojima se može upravljati  
  
- Procijenite vrijeme potrebno za dovršenje zadatka  
  
- Postavite zavisnosti zadatka i trajanje zadatka  
  
- Odredite uloge koje su potrebne za dovršetak svakog zadatka  
  
  Raspored projekta u strukturnoj analizi rada ima poznati izgled sa interaktivnim Ganttovim grafikonom.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Stvaranje strukturne analize rada za projekt  
 Stvaranje strukturne analize rada za predstavljanje slijeda zadataka u projektu. Strukturna analiza rada uključuje zadatke, zahtjeve za svaki zadatak i informacije o prihodu i trošku. U strukturnu analizu rada možete dodati:  
  
-   Slijed zadataka u hijerarhiji  
  
-   Druge zadatke, ako ih ima, koje treba dovršiti prije nego što se zadatak može pokrenuti.  
  
-   Početni datum, završni datum i trajanje zadatka  
  
-   Broj sati koji je potreban za zadatak  
  
-   Potrebne vještine i obrazovanje radnika  
  
-   Radnike koji su dodijeljeni zadatku  
  
-   Očekivani prihod i troškove  
  
## <a name="task-types"></a>Vrste zadataka  
Prilikom stvaranja strukturne analize rada koristit ćete sljedeće vrsta zadataka:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Korijenski čvor projekta** | Zadatak sažetka najviše razine za projekt. Svi drugi zadaci projekta stvaraju se ispod njega. Naziv korijenskog zadatka je naziv projekta. Trud, datumi i trajanje korijenskog čvora temelje se na vrijednostima u hijerarhiji ispod njega. Ne možete uređivati svojstva korijenskog čvora ili izbrisati korijenski čvor. | 
| **Zadaci sažetka ili spremnika** | Zadatak sažetka je zadatak koji ispod sebe ima podzadatke. Zadatak sažetka ne sadrži vlastiti trud ili trošak. Njegov trud i trošak je skupna vrijednost njegovih podzadataka. Možete promijeniti naziv zadatka sažetka, ali ne možete promijeniti trud, datume ili trajanje jer se izračunavaju automatski. Brisanje zadatka sažetka briše zadatak i sve njegove podzadatke.|  
| **Zadaci lisnog čvora** | Zadatak lisnog čvora predstavlja najdetaljniji rad na projektu. Sadrži procijenjeni trud, planirani broj resursa, planirane početne i završne datume i trajanje.|

  
## <a name="task-hierarchy"></a>Hijerarhija zadataka  
 Prilikom stvaranja hijerarhije zadataka pružaju vam se sljedeće mogućnosti:  
  
- **Dodaj zadatak**.   Zadatak možete dodati na položaj koji odaberete u hijerarhiji zadataka. Ako ne odaberete položaj, vaš novi zadatak pojavit će se na kraju.  
  
- **Uvuci zadatak**.   Uvucite zadatak da biste ga učinili podređenim zadatku izravno iznad njega.  
  
- **Izvuci zadatak**.   Izvucite zadatak kako više ne bi bio podzadatak izvorno nadređenog zadatka.  
  
- **Premjesti gore i premjesti dolje**.   Premjestite zadatke gore ili dolje u hijerarhiji nadređenog zadatka. Premještanje zadataka gore ili dolje ne utječe na njegov trud, trošak, datume ili trajanje.  
  
## <a name="task-attributes"></a>Atributi zadatka  
 Naziv zadatka opisuje posao koji treba dovršiti. Koristite različite atribute zadatka da biste opisali raspored i zahtjeve za broj djelatnika za zadatak.  
  
### <a name="schedule-attributes"></a>Atributi rasporeda

 - Dodijelite vrijednosti stavkama **Sati truda**, **Broj resursa**, **Početni datum**, **Završni datum** i **Trajanje** da biste odredili raspored za zadatak. 
 - **Trud** je procjena koliko će sati biti potrebno za dovršetak zadatka.
 - **Broj resursa** je procjena voditelja projekta za zadatak koja pomaže u stvaranju najboljeg mogućeg rasporeda. 
 - **Trajanje** (u danima) označava broj radnih dana potrebnih za dovršetak zadatka.  
  
### <a name="staffing-attributes"></a>Atributi broja djelatnika

 - **Uloga**, **Organizacijska jedinica resursa**, **Broj resursa** i **Resursi** opisuju zahtjeve za brojem djelatnika za zadatak. 
 - **Uloga** opisuje vrstu resursa potrebnih za izvođenje zadatka. 
 - **Organizacijska jedinica resursa** označava organizacijsku jedinicu iz koje treba dodijeliti djelatnike resursima za taj zadatak; to također utječe na procjenu troška i prodaje za zadatak jer se to uzima u obzir prilikom određivanja prodajne cijene jedinice za resurs. 
 - Stavka **Resursi** sadrži generički resurs ili resurs s nazivom kada je pronađen.  
  
## <a name="task-dependencies"></a>Zavisnosti zadatka  
 Možete stvoriti odnose prethodnika između jednog ili više zadataka u strukturnoj analizi rada. Možete postaviti jednu ili više vrijednosti za polje prethodnika za zadatke da biste označili zadatke o kojima će ovisiti. Kada zadatku dodijelite vrijednost prethodnika, zadatak može započeti samo nakon dovršetka svih zadataka prethodnika. Postavljanje te ovisnosti o zadatku rezultirat će ponovnim izračunavanjem planiranog početnog datuma zadatka kao najnovijeg kraja svih prethodnika. Utjecaji na raspored povezani s prethodnikom nisu ograničeni načinom zadatka definiranim za zadatak.  
  
## <a name="task-mode"></a>Način zadatka  
 Način zadatka je jedan od važnih faktora koji određuju raspoređivanje zadataka lisnog čvora. Postoje dva načina zadatka za svaki zadatak: način automatskog raspoređivanja i način ručnog raspoređivanja.  
  
-   **Automatsko zakazivanje**.   Kada način zadatka postavite na Automatsko raspoređivanje, modul raspoređivanja zadataka koristi pravila za raspoređivanje za sljedeće atribute zadatka kako bi odredio raspored za zadatak:  
  
    -   Prethodnici  
  
    -   Rad  
  
    -   Broj resursa  
  
    -   datumi početka i završetka  
  
-   **Pravila za zakazivanje**.   Početni datum zadatka lisnog čvora koji nema prethodnike vraća se na početni datum raspoređivanja projekta. Trajanje zadatka lisnog čvora uvijek se izračunava kao broj radnih dana između njegovog početnog i završnog datuma. Kada se zadatak automatski raspoređuje, modul raspoređivanja uvijek slijedi pravila u nastavku:  
  
    -   Početni i završni datumi zadatka uvijek moraju biti radni dani prema kalendaru za raspoređivanje projekta  
  
    -   Početni datum zadatka koji ima prethodnike vraća se na najnoviji završni datum prethodnika  
  
    -   Trud = broj osoba * trajanje * sati u standardnom radnom danu kalendara projekta  
  
-   **Ručno planiranje**.   U nekim slučajevima možda ćete željeti zaobići ta pravila. U takvim slučajevima možete postaviti način zadatka na ručno raspoređivanje. Time ćete zaustaviti modul raspoređivanja u izračunu vrijednosti za druge atribute raspoređivanja. Postavljanje prethodnika na zadatke uvijek utječe na početni datum ovisnog zadatka.  
  
## <a name="create-a-work-breakdown-structure"></a>Stvaranje strukturne analize rada  
  
1.  Idite na **Project Service > Projekti**.  
  
2.  Kliknite projekt na kojem radite.  
  
3.  Na traci na vrhu ekrana odaberite strelicu prema dolje pokraj naziva projekta, a zatim kliknite Strukturna analiza rada.  
  
4.  Da biste dodali zadatak, kliknite **Dodaj zadatak**. Ispunite polja za zadatak, a zatim kliknite **Spremi**.  
  
5.  Nastavite dodavati zadatke dok ne dovršite strukturnu analizu rada. Prilikom stvaranja strukturne analize rada, možete učiniti sljedeće da biste organizirali svoje zadatke:  
  
    -   Odaberite zadatak i kliknite **Uvuci** da biste ga premjestite ispod drugog zadatka ili kliknite Izvuci da biste ga izvukli za jednu razinu.  
  
    -   Odaberite zadatak i kliknite **Premjesti gore** ili **Premjesti dolje** da biste ga pomaknuli gore ili dolje na popisu.  
  
    -   Kliknite **Sakrij Ganttov grafikon** da biste sakrili dijagrama i kliknite **Prikaži Ganttov grafikon** da biste ponovno prikazali.  
  
    -   Odaberite drugo vremensko razdoblje za Ganttov grafikon pod **Vremensko mjerilo**.  
  
6.  Da biste uloge koje ste naveli u strukturnoj analizi rada dodali članovima tima projekta, kliknite **Generiraj tim za projekt**.  
  
7.  Kada ste gotovi s promjenama, kliknite **Spremi** u donjem desnom kutu zaslona.  
  
### <a name="see-also"></a>Pogledajte također  
 [Vodič za voditelje projekata](../project-service/project-manager-guide.md)
