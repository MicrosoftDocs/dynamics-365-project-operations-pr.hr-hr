---
title: Mapiranje projekata i zadataka u redak ponude koji se temelji na projektu
description: U ovoj temi nalaze se informacije o načinu mapiranja projekata i zadataka u redak zadatka koji se temelji na projektu.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d1c98d6a903393a0afc0e94d7f9859d55b9dc1f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994577"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Mapiranje projekata i zadataka u redak ponude koji se temelji na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U retke ponude koji se temelje na projektu možete mapirati određene zadatke projekta koji su već povezani s retkom ponude.

Kada mapirate zadatke u redak ponude, sljedeće će se stavke koje ste definirali u retku ponude primijeniti samo na te zadatke:

- Način naplate
- Mogućnosti naplate
- Ograničenja koja se ne smiju prekoračiti
- Klijenti

Na primjer, možda imate projekt u kojem je jedna faza nepromjenjiva cijena, a sve ostale faze su vrijeme i materijali. U tom slučaju, prvu fazu i sve njezine podređene zadatke možete povezati s retkom ponude za tu fazu uz način naplate s fiksnom cijenom. Zatim možete povezati sve ostale faze s retkom ponude koji se temelji na vremenu i materijalu.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Povezivanje zadataka s redcima ponude koji se temelje na projektu

Zadatke možete povezati s redcima ponude sa sljedećih lokacija:

- Stranica **Projekt** > kartica **Naplata zadatka** (optimalno)
- Stranica **Redak ponude** > kartica **Zadaci koji se naplaćuju** 

### <a name="from-the-project-page"></a>Sa stranice projekta

Stranica **Projekt** pruža optimalno iskustvo za povezivanje zadataka s redcima ponude. Ovu stranicu možete upotrijebiti za odabir više zadataka i povezivanje svih njih, kao i njihovih podređenih zadataka s odabranim retkom ponude.

1. Na kartici **Općenito** retka ponude koji se temelji na projektu, provjerite je li popunjeno polje **Projekt**.
2. U polju **Uključeni zadaci** odaberite mogućnost **Samo odabrani zadaci**.
3. Spremanje retka ponude utemeljenog na projektu Kada se obrazac osvježi, prikazuje se kartica **Zadaci koji se naplaćuju**.
4. Na kartici **Općenito** odaberite vezu za projekt iz polja **Projekt**.
5. Na stranici **Projekt** odaberite karticu **Naplata zadatka**.
6. U drugoj rešetki, koja se odnosi na postavke naplate određenih zadataka, odaberite jedan ili više zadataka, a zatim odaberite **Poveži retke ponude**.
7. Na dijaloškoj stranici koja se prikaže odaberite redak ponude koji na ponudi prikazuje retke ponude koji se temelje na projektu.
8. U polju **Vrsta naplate** naznačite jesu li ti zadaci naplativi ili nenaplativi.
9. Označite potvrdni okvir kako biste naznačili treba li povezanost uključivati podređene zadatke odabranih zadataka. Označavanjem okvira povezat će se podređeni zadaci odabranih zadataka s retkom ponude.
10. Odaberite **U redu** kako biste zatvorili dijaloški okvir.

### <a name="from-the-quote-line-page"></a>Sa stranice retka ponude

Projektne zadatke možete povezati s redcima ponude iz kartice **Zadaci koji se naplaćuju** na stranici **Redak ponude**.

>[!NOTE]
>Optimalno mjesto za povezivanje projektnih zadataka s redcima ponude jest na kartici **Naplata zadatka** na stranici **Projekt**. Ako povezujete zadatke iz kartice **Zadaci koji se naplaćuju** na stranici **Redak ponude**, svaki projekt morate ručno povezati.

1. Na kartici **Općenito** retka ponude koji se temelji na projektu, provjerite je li u polju **Projekt** odabran projekt.
2. U polju **Uključeni zadaci** odaberite mogućnost **Samo odabrani zadaci**.
3. Spremanje retka ponude utemeljenog na projektu Kada se obrazac osvježi, prikazuje se kartica **Zadaci koji se naplaćuju**.
4. Na kartici **Zadaci koji se naplaćuju** odaberite **Dodaj zadatak retka ponude**.
5. Na stranici **Zadatak retka ponude** u polju **Zadaci**, odaberite zadatak i u polju **Vrsta naplate** odaberite **Spremi**. 
6. Zatvorite stranicu. Odabrani zadatak sada je povezan s retkom ponude.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Prekidanje veze zadataka od redaka ponude koji se temelje na projektu

### <a name="from-the-project-page"></a>Sa stranice projekta

Ovaj način pruža najoptimalnije iskustvo za prekidanje veze zadataka od redaka ponude. Možete odabrati više zadataka, kao i njihove podređene zadatke, i prekinuti njihovu vezu s odabranim redcima ponude.

1. Na kartici **Općenito** retka ponude koji se temelji na projektu, u polju **Projekt**, odaberite vezu na projekt.
2. Na stranici **Projekt** odaberite karticu **Naplata zadatka**.
3. U drugoj rešetki, koja se odnosi na postavke naplate određenih zadataka, odaberite jedan ili više zadataka, a zatim odaberite **Prekini vezu s redcima ponude**.
4. Na dijaloškoj stranici koja se prikaže odaberite redak ponude.
5. Označite potvrdni okvir kako biste naznačili treba li se povezanost ukloniti i s podređenih zadataka odabranih zadataka. Označavanjem okvira prekinut ćete i vezu podređenih zadataka odabranih zadataka s retkom ponude.
6. Odaberite **U redu**. Poruka upozorenja izvješćuje vas da ako uklonite ovu povezanost, svi stvarni podaci koji su prethodno zabilježeni u zadatku mogu se poništiti. 
7. Odaberite **U redu** za nastavak i uklanjanje povezanosti između zadatka i retka ponude koji se temelji na projektu.

### <a name="from-the-quote-line-page"></a>Sa stranice retka ponude

Projektnim zadacima možete i prekinuti vezu s redcima ponude iz kartice **Zadaci koji se naplaćuju** na stranici **Redak ponude**.

1. Na kartici **Zadaci koji se naplaćuju** odaberite **Izbriši zadatak retka ponude**.
2. Odaberite **U redu**. Poruka upozorenja izvješćuje vas da ako uklonite ovu povezanost, svi stvarni podaci koji su prethodno zabilježeni u zadatku mogu se poništiti. 
3. Odaberite **U redu** za nastavak i uklanjanje povezanosti između zadatka i retka ponude koji se temelji na projektu.

>[!NOTE]
> Ovim postupkom zadatak se ne briše iz projekta. Time se samo uklanja povezanost zadataka iz retka ponude koji se temelji na projektu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]