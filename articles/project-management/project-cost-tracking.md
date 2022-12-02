---
title: Praćenje troška projekta
description: U ovom članku nalaze se informacije o tome kako aplikacija Project Operations prati napredak u odnosu na trošak rada i uloženi rad na projektu.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c069a28c6dc546e5e632c4dff29686dc7965f23e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923731"
---
# <a name="labor-cost-tracking-on-projects"></a>Praćenje troška rada na projektima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations prati procjene rada i uloženi rad do najsitnijih pojedinosti plana projekta. Financijska procjena troška od rada temelji se na planiranom radnom naporu i generičkim ili imenovanim resursima koji su dodijeljeni svakom zadatku lisnog čvora u planu projekta. Kada projekt započne i ljudi počnu izvješćivati o vremenu provedenom na raznim projektnim zadacima, sažima se stvarno uloženi rad čime započinje izračun predviđanja.

## <a name="labor-cost-tracking-view"></a>Prikaz praćenja troška rada

Na stranici **Projekti**, na kartici **Praćenje**, možete odabrati **Praćenje** > **Trošak** kako biste otvorili prikaz **Praćenje troška** i vidjeli napredak ulaganja rada na svakom zadatku u planu projekta. Ovaj prikaz uspoređuje i stvarni trošak rada uloženog na zadatku s planiranim troškom rada na zadatku. Project Operations upotrebljava sljedeće formule za izračunavanje mjernih podataka o trošku rada:

- **Planirani trošak**: Procijenjeni trošak svih dodjela resursa na svakom zadatku lisnog čvora
- **Stvarni trošak**: Zbroj svih stvarnih troškova za vrijeme zabilježeno na zadatku
- **Postotak potrošnje troškova**: Stvarni trošak ÷ Procjena troška po završetku
- **Preostali trošak**: Procjena troška po završetku – Stvarni trošak
- **Trošak po završetku**: Preostali trošak – Stvarni trošak
- **Odstupanje troška**: Planirani trošak – Procjena troška po završetku

Svaki zadatak prikazuje predviđanje odstupanja troška na zadatku. Ako je procjena troška po završetku veća od planiranog troška, predviđa se da će zadatak premašiti proračun. Ako je procjena troška po završetku manja od planiranog troška, predviđa se da će se zadatak završiti u okviru proračuna.

>[!NOTE]
> Project Operations prikazuje samo troškove od rada na stranici **Projekt**, na kartici **Praćenje**. Dok se potrošnja materijala i troškova može procijeniti i pratiti, ovi troškovi nisu uključeni u troškove koji se prikazuju na kartici **Praćenje**. Ova je kartica dizajnirana tako da funkcionira samo za ponovno predviđene troškove od rada ponovnim predviđanjem uloženog rada.
Svi prikazani iznosi troška pretvaraju se u valutu troška projekta iz valute cijene koštanja projekta koja se upotrebljava za određivanje cijene troška. Valuta troška projekta valuta je ugovorne jedinice na projektu. Procijenjene vrijednosti troška za vrijeme koje se prikazuje na kartici **Procjene**, na stranici **Projekt** možda se neće dodati planiranom trošku na kartici **Praćenje**. Razlog za ovo odstupanje jest razlika u načinu sažimanja procijenjenog troška na rešetki **Procjene** i izračunavanja planiranog troška na rešetki **Praćenje**. 
>
> - Na kartici **Procjene** procijenjeni se trošak izračunava s pomoću iste valute cijene troška koja se nalazi u cjeniku. Zatim se procijenjeni trošak u valuti cjenika pretvara u procijenjeni trošak u valuti troškova projekta. Procijenjeni trošak u valuti projekta prikazuje se zaokružen na 2 decimale. Tijekom ove pretvorbe preciznost valute ne primjenjuje se ni u jednom trenutku. 
> - Izračun planiranog troška na kartici **Praćenje** slijedi malo drugačiji redoslijed izračuna koji uključuje preciznost valuta koja se primjenjuje u dvije faze: 
   ><ol>
   ><li>Procijenjeni iznos troška u valuti cjenika pretvara se u osnovnu valutu (pretvorba 1).</li>
   ><li>Procijenjeni iznos troška u osnovnoj valuti pretvara se u valutu troška projekta (pretvorba 2). </li>
   ></ol>
   >Preciznost valute primjenjuje se u oba koraka kako bi se dobio planirani trošak (na kartici **Praćenje**) koji malo odstupa od procijenjenog troška (na prikazu **Vrijeme – fazno** na kartici **Procjene**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Ponovna procjena troškova na zadacima lisnih čvorova

Troškovi rada na zadatku lisnog čvora ne mogu se izravno ponovno predvidjeti na kartici **Praćenje** stranice **Projekt**. Međutim, možete upotrijebiti prikaz **Praćenje rada** za ponovno predviđanje preostalog rada na zadatku. To uzrokuje ponovni izračun preostalog troška na zadatku. Slijedi opis načina na koji to funkcionira.

1. Voditelj projekta može ponoviti predviđanje rada na zadacima ažuriranjem zadane vrijednosti u polju **Preostali rad** s novom procjenom preostalog rada na zadatku. Ponovno predviđanje uzrokuje ponovno izračunavanje procjene rada po završetku zadatka (EAC, estimate at complete), postotka napretka i predviđena odstupanja rada na zadatku. EAC, procjena za dovršetak (ETC) i postotak napretka na zadacima sažetka također se ponovno izračunavaju i stvara se novo predviđanje odstupanja rada.
2. Na temelju nove vrijednosti za preostali rad na zadatku, sustav izračunava preostali trošak na prikazu **Praćenje troška**. Kako bi izračunao preostali trošak na temelju preostalog rada, sustav najprije izračunava prosječni trošak jednog sata rada na zadatku kao planirani trošak ili planirani rad. Planirani trošak zbroj je troškova svih dodjela resursa na zadatku. Prosječni trošak po satu upotrebljava se za izračunavanje preostalog troška za novo predviđeni preostali rad na zadatku.
3. Ponovno se izračunavaju postotci troška po završetku i upotrijebljenog troška na zadatku lisnog čvora.
4. Ponovno se izračunava vrijednost troška po završetku za zadatke sažetka sve do korijenskog čvora.

## <a name="reprojecting-costs-on-summary-tasks"></a>Ponovno predviđanje troška na zadacima sažetka

Možete ponovno predvidjeti troškove rada na zadacima sažetka ili na zadacima spremnika. Međutim, trošak rada ne možete izravno ponovno predvidjeti na sažetom projektnom zadatku na kartici **Praćenje** stranice **Projekt**. Slično zadacima lisnog čvora, zadaci sažetka i spremišta ponovnog predviđanja može se izvršiti s pomoću prikaza **Praćenje rada**. U ovom prikazu možete ponovno predvidjeti preostali rad na zadatku sažetka i time uzrokovati ponovni izračun preostalog troška na zadatku sažetka. Slijedi opis načina na koji to funkcionira.

1. Voditelj projekta može ponoviti predviđanje rada na zadacima sažetka ažuriranjem zadane vrijednosti preostalog rada s novom procjenom zadatka. Ovo ažuriranje uzrokuje ponovno izračunavanje procjene po završetku (EAC, estimate at complete) zadatka sažetka, postotka napretka i odstupanje projektnog rada na zadatku. EAC, ETC i postotak napretka na zadacima sažetka također se ponovno izračunavaju i stvara se novo predviđanje odstupanja rada.
2. Na temelju nove vrijednosti za preostali rad na zadatku sažetka, sustav izračunava preostali trošak na prikazu **Praćenje troška**. Kako bi izračunao preostali trošak na temelju preostalog rada, sustav najprije izračunava prosječni trošak jednog sata rada na zadatku sažetka kao planirani trošak ili planirani rad. Prosječni trošak po satu upotrebljava se za izračunavanje troška novo predviđenog preostalog rada na zadatku sažetka.
3. Ponovno se izračunavaju postotci troška po završetku i upotrijebljenog troška na zadatku sažetka lisnog čvora.
4. Nova se vrijednost procijenjenog troška po završetku raspoređuje na podređene zadatke u istom omjeru kao izvorno planirani trošak na zadatak.
5. Izračunava se nova vrijednost troška po završetku za svaki od pojedinačnih zadataka sve do lisnog čvora. Na temelju ove vrijednosti, ponovno će se, na temelju vrijednosti troška po završetku, izračunati postotak potrošenog i preostalog troška zahvaćenih podređenih zadataka sve do lisnog čvora. Ta vrijednost dovodi do novog predviđanja za odstupanje troška zadatka. 


Polje **Izvršenje troška** može se postaviti iz podataka koji se prate. Kada je odstupanje troška za korijenski čvor u prikazu **Praćenje troška** negativno, ovo polje možete postaviti na **U okviru proračuna**. Kada je odstupanje troška za korijenski čvor pozitivno, vrijednost možete postaviti na **Premašuje proračun**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
