---
title: Kopiranje prilika koje se temelje na projektu
description: U ovom se članku nalaze informacije o kopiranju prilika temeljenih na projektima u operacijama projekta.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: cc772391de97f4b2de6e9e29f97a6af4d5514319
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926123"
---
# <a name="copy-project-based-opportunities"></a>Kopiranje prilika koje se temelje na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_


Prilike za projekt mogu se lako kopirati kako bi se stvorile nove prilike za projekt. 

1. Idite na stranicu s popisom **Prilike za projekt** i s popisa odaberite priliku. Ili otvorite stranicu s pojedinostima određene prilike. 
2. S bilo koje stranice odaberite **Kopiraj**. Otvorit će se dijaloška stranica koja sadrži sljedeće podatke o polju. Ovisno vrijednostima odabranim u tom dijaloškom okviru, postupak kopiranja može se promijeniti.

    | **Polje** | **Opis** | **Utjecaj prema dolje** |
    | --- | --- | --- |
    | Tema | Unesite relevantnu temu ciljane prilike. Kada se otvori dijaloški okvir, sustav će ga postaviti na temu izvorne prilike s riječju **–kopija** dodanom uz njega. | Ovo polje ne utječe na niže razine. |
    | Poslovni subjekt | Upućuje na zapis tvrtke ili račun klijenta. Kad se otvori dijaloški okvir, sustav će ga postaviti na račun na izvornoj prilici. | Ovo polje primarni je klijent u prilici. |
    | Ugovorena jedinica | Organizacijska jedinica koja je odgovorna za isporuku projekata povezanih s ovim poslom. Kad se otvori dijaloški okvir, sustav će ga postaviti na ugovornu jedinicu izvorne prilike. | Ugovorna jedinica odjel je tvrtke koji izvršava projekte nakon zaključenja posla. Svaka ugovorna jedinica ima valutu i ta se valuta upotrebljava za izvješćivanje o procijenjenim i stvarnim troškovima nastalim tijekom izvršenja projekta. |
    | Valuta | Valuta u kojoj se transakcija posla obavlja. Kad se otvori dijaloška stranica, sustav će ga postaviti na valutu izvorne prilike. | Valuta se upotrebljava za zadavanje cjenika i izradu financijskih procjena za ponudu. Na kraju, valuta se upotrebljava za fakturiranje klijentu kada je posao dobiven. |
    | Kopiranje cijena | Vrijednost Da/Ne koja pokazuje hoće li se cijena za priliku kopirati iz izvorne prilike. | Ako je odabrano **Da**, cjenici se kopiraju iz izvora u ciljanu priliku. Ako se odabere **Ne**, cjenici se zadaju na temelju posljednje postavljenih cjenika. |

3. Odaberite **U redu**. Sustav stvara kopiju prilike za projekt na temelju odabranih parametara i otvara se nova projektna prilika.


[!INCLUDE[footer-include](../includes/footer-banner.md)]