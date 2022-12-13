---
title: Mapiranje projekata i zadataka u redak ugovora o projektu
description: U ovom se članku navode informacije o dodavanju projekata i zadataka u redak ugovora i uklanjanju istih iz retka ugovora.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 45118bb5a36203a3121a5f7ada0992d2c2491a4a
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825049"
---
# <a name="map-projects-and-tasks-to-a-project-contract-line"></a>Mapiranje projekata i zadataka u redak ugovora o projektu 

_**Primjenjuje se na:** Osnovna implementacija – od dogovora do predračuna, Project Operations za scenarije koji se temelje na resursima / bez zaliha_

U recima ugovora o projektu možete mapirati određene zadatke u projektu u redak ugovora.

Kada mapirate određene zadatke na redak ugovora, način naplate, mogućnosti naplate, ograničenja koja se ne smiju prekoračiti i klijente definirane na retku ugovora bit će primjenjivi samo na te određene zadatke.

Ako imate scenarij u kojem je jedna faza projekta, na primjer faza prototipa, fiksna cijena, a sve ostale faze su vrijeme i materijal, fazu prototipa i sve povezane podređene zadatke moći ćete povezati s retkom ugovora za tu fazu s načinom naplate s fiksnom cijenom.

Sve ostale faze u strukturnoj analizi rada (WBS) vašeg projekta mogu se povezati s retkom ugovora koji se temelji na vremenu i materijalu.

## <a name="associate-tasks-to-project-contract-lines"></a>Pridruživanje zadataka recima ugovora o projektu

Zadaci se mogu povezati s redcima ugovora iz kartice **Naplativi zadaci** na stranici **Redak ugovora** ili iz kartice **Naplata zadatka** na stranici **Projekt**.

### <a name="from-the-contract-line-page"></a>Sa stranice retka ugovora

Poduzmite sljedeće korake za povezivanje projektnih zadataka s retkom ugovora iz kartice **Naplativi zadaci** na stranici **Redak ugovora**.

1. Na kartici **Općenito** retka ugovora koji se temelji na projektu, provjerite je li polje **Projekt** popunjeno.
2. U polju **Uključeni zadaci** odaberite **Samo odabrani zadaci**.
3. Spremite promjene. Obrazac će se osvježiti i vidjet će se kartica **Naplativi zadaci**.
4. Odaberite karticu **Naplativi zadaci** i u podrešetki odaberite **Dodaj zadatak retka ugovora**.
5. Na stranici **Zadaci retka ugovora** u padajućem izborniku **Zadaci** odaberite zadatak. 
6. Unesite podatke u polje **Vrsta naplate**, a zatim odaberite **Spremi i zatvori**. Odabrani zadatak povezan je s retkom ugovora.

> [!NOTE]
> Ovo nije najoptimalnije iskustvo za povezivanje projektnih zadataka s redcima ugovora. U ovom iskustvu svaki će se projekt morati ručno povezati. Preferirani način je iz kartice **Naplata zadatka** na stranici **Projekt**.

### <a name="from-the-project-page"></a>Sa stranice projekta

Ovo je optimalni način za povezivanje zadataka s redcima ugovora. Možete odabrati više zadataka te sve njih i njihove podređene zadatke povezati s odabranim retkom ugovora. Dovršite sljedeće korake za povezivanje zadataka s retkom ugovora sa stranice **Projekt**.

1. Na kartici **Općenito** retka ugovora koji se temelji na projektu, provjerite je li polje **Projekt** popunjeno.
2. U polju **Uključeni zadaci** odaberite **Samo odabrani zadaci**.
3. Spremite redak ugovora koji se temelji na projektu. Obrazac će se osvježiti i vidjet će se kartica **Naplativi zadaci**. Ovo je samo u svrhu provjere valjanosti.
4. Na kartici **Općenito** retka ugovora koji se temelji na projektu, u polju **Projekt**, odaberite vezu na projekt.
5. Na stranici **Projekt** odaberite karticu **Postavke naplate zadatka**.
6. Postoje dvije rešetke. Jedna je rešetka za retke ugovora koji se odnose na cijeli projekt. Druga rešetka odnosi se na postavke naplate specifične za zadatak. U drugoj rešetki odaberite jedan ili više zadataka, a zatim odaberite **Poveži retke ugovora**.
7. Na dijaloškoj stranici koja se otvori odaberite redak ugovora s padajućeg izbornika.
8. Upotrijebite padajući izbornik **Vrsta naplate** za označavanje zadataka kao naplativih ili nenaplativih.
9. Označite potvrdni okvir kako biste naznačili treba li povezanost obuhvatiti i podređene zadatke odabranih zadataka. Označavanjem okvira podređeni će se zadaci odabranih zadataka također povezati s retkom ugovora.
10. Odaberite **U redu** kako biste zatvorili dijaloški okvir.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Prekidanje veze zadataka iz redaka ugovora koji se temelje na projektu

### <a name="from-the-contract-line-page"></a>Sa stranice retka ugovora

Poduzmite sljedeće korake za prekidanje veze projektnih zadataka iz retka ugovora na kartici **Naplativi zadaci** stranice **Redak ugovora**.

1. Na kartici **Naplativi zadaci** odaberite **Brisanje zadatka iz retka ugovorne**.
2. Poruka upozorenja ukazuje kako bi uklanjanje ove povezanosti moglo dovesti do poništavanja svih stvarnih podataka koji su prethodno zabilježeni u zadatku. Odaberite **U redu** u dijaloškom okviru kako biste uklonili povezanost između zadatka i retka ugovora koji se temelji na projektu. 

> [!NOTE]
> Ovim ne brišete zadatak iz projekta. Umjesto toga, uklanja povezivanje zadatka s retkom ugovora koji se temelji na projektu.

### <a name="from-the-project-page"></a>Sa stranice projekta

Ovo je najoptimalnije iskustvo za prekidanje povezivanja projektnih zadataka iz redaka ugovora. Možete odabrati više zadataka te za sve njih i njihove podređene zadatke prekinuti povezanost iz odabranog retka ugovora. Dovršite sljedeće korake za prekidanje povezivanja zadataka iz retka ugovora.

1. S kartice **Općenito** retka ugovora koji se temelji na projektu, u polju **Projekt**, kliknite na vezu za projekt.
2. Na stranici **Projekt** odaberite karticu **Postavke naplate zadatka**.
3. Na stranici se nalaze dvije rešetke. Jedna je rešetka za retke ugovora koja se odnosi na cijeli projekt, a druga se odnosi na postavke naplate specifične za zadatak. U drugoj rešetki odaberite jedan ili više zadataka, a zatim odaberite **Prekini povezanost redaka ugovora**.
4. Na dijaloškoj stranici koja se otvori odaberite redak ugovora s padajućeg izbornika.
5. Označite potvrdni okvir kako biste naznačili treba li povezanost ukloniti i iz svih podređenih zadataka odabranih zadataka. Označavanjem okvira podređenim će se zadacima odabranih zadataka također prekinuti povezanost iz retka ugovora.
6. Odaberite **U redu**. Poruka upozorenja ukazuje kako bi uklanjanje ove povezanosti moglo dovesti do poništavanja svih stvarnih podataka koji su prethodno zabilježeni u zadatku. Odaberite **U redu** u dijaloškom okviru upozorenja kako biste uklonili povezanost između zadatka i retka ugovora koji se temelji na projektu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
