---
title: Praćenje prodaje projekta
description: U ovoj temi nalaze se informacije o tome kako aplikacija Project Operations prati napredak u odnosu na prihode od rada na projektu.
author: rumant
manager: AnnBe
ms.date: 03/24/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 438c44dcfaf9677075eb07688c1e65c6e7053755
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711031"
---
# <a name="project-sales-tracking"></a>Praćenje prodaje projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations prati procjene rada i prihode od rada do najsitnijih pojedinosti plana projekta. Procjena prihoda od rada temelji se na planiranom radnom naporu i generičkim ili imenovanim resursima koji su dodijeljeni svakom zadatku lisnog čvora u planu projekta. Kada projekt započne i ljudi počnu izvješćivati o vremenu provedenom na raznim projektnim zadacima, sažima se stvarni prihod od rada čime započinje izračun projekcija.

## <a name="labor-revenue-tracking-view"></a>Prikaz praćenje prihoda od rada

Na stranici **Projekti**, na kartici **Praćenje**, možete odabrati **Praćenje** > **Trošak** kako biste otvorili prikaz **Praćenje troška**. Ili možete odabrati **Upotrijebi** > **Stopa naplate** kako biste otvorili prikaz **Praćenje prihoda**, koji pokazuje napredak prihoda od rada na svakom zadatku u planu projekta. Ovaj prikaz također uspoređuje stvarni prihod rada utrošenog na zadatak s planiranim prihodom rada na zadatku. Project Operations upotrebljava sljedeće formule za izračunavanje mjernih podataka o prihodu od rada:

- **Planirani prihod**: Procijenjene prodajne vrijednosti svih dodjela resursa na svakom zadatku lisnog čvora
- **Stvarni prihod**: Zbroj svih nenaplaćenih stvarnih prodaja za vrijeme zabilježeno na zadatku
- **Naplativi prihod %**: Stvarni prihod ÷ Procjena prihoda po završetku
- **Preostali prihod**: Procjena prihoda po završetku – Stvarni prihod
- **Procijenjeni prihod po završetku**: Preostali prihod + Stvarni prihod
- **Odstupanje prihoda**: Planirani prihod – Procijenjeni prihod po završetku


> [!NOTE]
> Project Operations prikazuje samo prihode od rada na stranici **Projekt**, na kartici **Praćenje**. Dok se potrošnja materijala i troškova može procijeniti i pratiti, ovi prihodi nisu uključeni u prihode koji se prikazuju na kartici **Praćenje**. Ova je kartica dizajnirana tako da funkcionira samo za ponovno predviđene prihode od rada ponovnim predviđanjem uloženog rada.  
> Svi prikazani iznosi prihoda pretvaraju se u valutu troška projekta. Valuta troška projekta valuta je ugovorne jedinice na projektu. Za projekte s fiksnom cijenom, iznos prihoda na prikazu **Praćenje prihoda od rada** nije relevantan jer se nefakturirana stvarna prodaja ne bilježi po odobrenju vremena.
> Procijenjene vrijednosti prodaje za vrijeme koje se prikazuje na kartici projekta **Procjena** možda se neće zbrajati s planiranom vrijednosti prihoda na kartici **Praćenje**. Izvor ove razlike proizlazi iz dva moguća razloga:
><ol>
   ><li> Kartica <b>Procjene</b> prikazuje procijenjeni prihod u valuti prodaje, dok kartica <b>Praćenje</b> prikazuje planirani prihod pretvoren u valutu troška. </li>
   ><li> Kada se procijenjena prodaje pretvori u valutu ugovora kako je prikazano na kartici <b>Procjene</b>, ta pretvorba za valutu projekta uključuje korake koji bi mogli dovesti do određene netočnosti: </li>
><ol>
><li> Procijenjeni iznos prodaje u ugovornoj valuti najprije se pretvara u osnovnu valutu (pretvorba 1).</li>
><li> Procijenjeni iznos prodaje u osnovnoj valuti pretvara se u valutu troška projekta (pretvorba 2). </li>
></ol>
></ol>
> Preciznost valute primjenjuje se u oba koraka, što rezultira odstupanjem planiranog prihoda u valuti projekta od planirane prodaje u ugovornoj valuti.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Ponovno predviđanje prihoda na zadacima lisnog čvora

Prihodi od rada na zadatku lisnog čvora ne mogu se izravno ponovno predvidjeti na kartici **Praćenje** stranice **Projekt**. Međutim, možete upotrijebiti prikaz **Praćenje rada** za ponovno predviđanje preostalog rada na zadatku. To uzrokuje ponovni izračun preostalog prihoda na zadatku. Slijedi opis načina na koji to funkcionira.

1. Voditelj projekta može ponoviti predviđanje rada na zadacima ažuriranjem zadane vrijednosti u polju **Preostali rad** s novom procjenom preostalog rada na zadatku. Ponovno predviđanje uzrokuje ponovno izračunavanje procjene rada po završetku zadatka (EAC, estimate at complete), postotka napretka i predviđena odstupanja rada na zadatku. EAC, procjena za dovršetak (ETC) i postotak napretka na zadacima sažetka također se ponovno izračunavaju i stvara se novo predviđanje odstupanja rada.
2. Na temelju nove vrijednosti za preostali rad na zadatku, sustav izračunava preostali prihod na prikazu **Praćenje prihoda**. Kako bi izračunao preostali prihod na temelju preostalog rada, sustav najprije izračunava prosječni prihod od jednog sata rada na zadatku kao planirani prihod ili planirani rad. Planirani prihod zbroj je prihoda svih dodjela resursa na zadatku. Prosječni prihod po satu upotrebljava se za izračunavanje preostalog prihoda za novo predviđeni preostali rad na zadatku.
3. Ponovno se izračunavaju procijenjeni prihod po završetku i postotak potrošnje prihoda na zadatku lisnog čvora.
4. Ponovno se izračunava vrijednost prihoda po završetku za zadatke sažetka sve do korijenskog čvora.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Ponovno predviđanje prihoda na zadacima sažetka

Možete ponovno predvidjeti prihode od rada na zadacima sažetka ili na zadacima spremnika. Međutim, prihode od rada ne možete izravno ponovno predvidjeti na sažetom projektnom zadatku na kartici **Praćenje** stranice **Projekt**. Slično zadacima lisnog čvora, zadaci sažetka i spremišta ponovnog predviđanja može se izvršiti s pomoću prikaza **Praćenje rada**. U ovom prikazu možete ponovno predvidjeti preostali rad na zadatku sažetka i time uzrokovati ponovni izračun preostalog prihoda na zadatku sažetka. Slijedi opis načina na koji to funkcionira.

1. Voditelj projekta može ponoviti predviđanje rada na zadacima ažuriranjem zadane vrijednosti u polju **Preostali rad** s novom procjenom **Preostalog rada** na zadatku. Ponovno predviđanje uzrokuje ponovno izračunavanje procjene po završetku zadatka (EAC, estimate at complete), postotka napretka i predviđena odstupanja rada na zadatku. EAC, ETC i postotak napretka na zadacima sažetka također se ponovno izračunavaju i stvara se novo predviđanje odstupanja rada.
2. Na temelju nove vrijednosti u polju **Preostali rad** na zadatku, sustav izračunava preostali prihod na prikazu **Praćenje prihoda**. Kako bi izračunao preostali prihod na temelju preostalog rada, sustav najprije izračunava prosječni prihod od jednog sata rada na zadatku kao planirani prihod ili planirani rad. Planirani prihod zbroj je prihoda svih dodjela resursa na zadatku. Ovaj se prosječni prihod po satu zatim upotrebljava se za izračunavanje prihoda za novo predviđeni preostali rad na zadatku.
3. Ponovno se izračunavaju procijenjeni prihod po završetku i postotaka potrošnje prihoda na zadatku sažetka.
4. Nova se vrijednost procijenjenog prihoda po završetku raspoređuje na podređene zadatke u istom omjeru kao izvorno planirani prihod na zadatak.
5. Izračunava se novi predviđeni prihod po završetku za svaki od pojedinačnih zadataka sve do lisnog čvora. Na temelju ove vrijednosti, ponovno će se, na temelju vrijednosti prihoda po završetku, izračunati postotak potrošenog i preostalog prihoda zahvaćenih podređenih zadataka sve do lisnog čvora. To dovodi do novog predviđanja odstupanja prihoda od zadatka. 
6. Ponovno se izračunava vrijednost prihoda po završetku za zadatke sažetka sve do korijenskog čvora.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

