---
title: Kopiranje prilika koje se temelje na projektu
description: U ovoj temi nalaze se informacije o kopiranju prilika koje se temelje na projektu u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 89f5a63581f36b30634bdd302a6d360d6b5e75bd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073327"
---
# <a name="copy-project-based-opportunities"></a>Kopiranje prilika koje se temelje na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_


Prilike za projekt mogu se lako kopirati kako bi se stvorile nove prilike za projekt. 

1. Idite na stranicu s popisom **Prilike za projekt** i s popisa odaberite priliku. Ili otvorite stranicu s pojedinostima određene prilike. 
2. S bilo koje stranice odaberite **Kopiraj**. Otvorit će se dijaloška stranica koja sadrži sljedeće podatke o polju. Ovisno vrijednostima odabranim u tom dijaloškom okviru, postupak kopiranja može se promijeniti.

    | **Polje** | **Relevantnost, svrha i smjernice** | **Utjecaj prema dolje** |
    | --- | --- | --- |
    | Tema | Unesite relevantnu temu ciljane prilike. Kada se otvori dijaloški okvir, sustav će ga postaviti na temu izvorne prilike s riječju **–kopija** dodanom uz njega. | Ovo polje ne utječe na niže razine. |
    | Poslovni subjekt | Upućuje na zapis tvrtke ili račun klijenta. Kad se otvori dijaloški okvir, sustav će ga postaviti na račun na izvornoj prilici. | Ovo polje primarni je klijent u prilici. |
    | Ugovorena jedinica | Organizacijska jedinica koja je odgovorna za isporuku projekata povezanih s ovim poslom. Kad se otvori dijaloški okvir, sustav će ga postaviti na ugovornu jedinicu izvorne prilike. | Ugovorna jedinica odjel je tvrtke koji izvršava projekte nakon zaključenja posla. Svaka ugovorna jedinica ima valutu i ta se valuta upotrebljava za izvješćivanje o procijenjenim i stvarnim troškovima nastalim tijekom izvršenja projekta. |
    | Valuta | Valuta u kojoj se transakcija posla obavlja. Kad se otvori dijaloška stranica, sustav će ga postaviti na valutu izvorne prilike. | Valuta se upotrebljava za zadavanje cjenika i izradu financijskih procjena za ponudu. Na kraju, valuta se upotrebljava za fakturiranje kupcu kada je posao dobiven. |
    | Kopiranje cijena | Vrijednost Da/Ne koja pokazuje hoće li se cijena za priliku kopirati iz izvorne prilike. | Ako je odabrano **Da** , cjenici se kopiraju iz izvora u ciljanu priliku. Ako se odabere **Ne** , cjenici se zadaju na temelju posljednje postavljenih cjenika. |

3. Odaberite **U redu**. Sustav stvara kopiju prilike za projekt na temelju odabranih parametara i otvara se nova projektna prilika.