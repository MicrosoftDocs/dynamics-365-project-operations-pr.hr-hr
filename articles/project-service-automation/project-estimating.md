---
title: Troškovi i prihod projekta
description: Ova tema pruža informacije o procjeni troškova i prihoda projekta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: e9d82a6c-0164-4177-838b-c34571be041c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3eb52d97fbd5df0364bc9a1a1ef11a0a0f7ee127
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750211"
---
# <a name="project-costs-and-revenue"></a>Troškovi i prihod projekta

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Procjena projekta daje financijski prikaz za procijenjeni i raspoređeni rad u rasporedu projekta. Kartica **Procjene** na stranici **Projekti** prikazuje učinak troška i prihoda rada koji planirate. Također pruža informacije o brojnim unaprijed definiranim dimenzijama. 

> ![Kartica Procjene](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Trošak i prodajne vrijednosti projekta

Cjenici definiraju stope troškova i naplate za uloge u projektu. Možete odrediti učinak troška i prihoda rada, na temelju uloga koje su pridružene nazivu položaja i imenovanom resursu koji je dodijeljen zadatku. Ako postoje zadaci koji nemaju dodjele (generičke ili imenovane), ne možete dobiti procjene troška ili prodaje. Trošak i prodajne vrijednosti u obzir uzimaju datum definiran na cjenicima.

### <a name="default-cost-price"></a>Zadana cijena troškova  

Svaki projekt pripada tvrtki ili ustanovi. Ta tvrtka ili ustanova prikazuje se u polju **Ugovorna jedinica** u projektu. Cjenik koji je povezan s ugovornom jedinicom koristi se za određivanje cijene troškova jedinice. Da biste odredili ispravne cijene troškova za uloge za datum koji je definiran u recima procjene, pretražite kombinaciju uloge, jedinice i organizacijske jedinice u cjeniku troškova. 

Da bi se njihove cijene troškova mogle izračunati, svi zadaci moraju biti dodijeljeni resursu. Svaki nedodijeljeni zadatak imat će cijenu troškova od 0,00.

Ako kombinacija uloge, jedinice i organizacijske jedinice ne vraća cijenu troškova s cjenika ugovorne jedinice, sustav zanemaruje jedinicu. Umjesto toga, pretražuje samo kombinaciju uloge i organizacijske jedinice. Ako je cijena troškova pronađena, čimbenici konverzije koriste se za njezino pretvaranje u jedinicu koju ste odabrali u retku procjene.

Ako kombinacija uloge, jedinice i organizacijske jedinice ne vraća cijenu troškova, sustav zanemaruje organizacijsku jedinicu. Umjesto toga, pretražuje kombinaciju uloge i jedinice za postavljanje zadane cijene (nakon primjene bilo koje konverzije).

Ako sustav ne pronađe cijenu za ulogu, cijena troškova u retku procjene postavlja se na zadanu vrijednost **0,00**. Svi iznosi troška u recima procjene troškova projekta biilježe se u valuti ugovorne jedinice.

> [!NOTE]
> Prema zadanim postavkama Microsoft Dynamics 365 pohranjuje iznose troškova u osnovnoj valuti. Međutim, iznosi troškova prikazani na kartici **Procjene** navedeni su u valuti ugovorne jedinice.  

### <a name="default-sales-price"></a>Zadana prodajna cijena 

Cjenik prodaje određuje prodajni entitet kojem je projekt pridružen ili klijent projekta. Kada je prodajni entitet (npr. prilika, ponuda ili ugovor) povezan s projektom, prodajna cijena prodajnog entiteta određuje se prema cjeniku koji je povezan s ponudom ili ugovorom. Ako ponuda ili ugovor ima prilagođeni cjenik, taj cjenik upotrebljava se kao zadani prodajni cjenik za procjenu projekta. Ako nema povezivanja s prodajnim entitetima, zadani prodajni cjenik iz parametara koristi se kao zadani prodajni cjenik projekta koji odgovara valuti klijenta koja je definirana u projektu.

Svaki redak procjene ima povezanu jedinicu za resurse. Jedinica za resurse označava organizacijsku jedinicu iz koje se resursi rezerviraju radi dovršetka zadatka. Da biste odredili prodajnu cijenu za povezane uloge, pretražite kombinaciju uloge, jedinice i jedinice za resurse u prodajnom cjeniku. Ako u zadatku nema dodjela, prodajna cijena za zadatak iznosi 0,00.

Ako kombinacija uloge, jedinice i jedinice za resurse ne vraća prodajnu cijenu s prodajnog cjenika, sustav zanemaruje jedinicu. Umjesto toga, pretražuje samo kombinaciju uloge i jedinice za resurse. Ako je prodajna cijena pronađena, čimbenici konverzije koriste se za njezino pretvaranje u jedinicu koju ste odabrali u retku procjene prodaje. 

Ako kombinacija uloge, jedinice i jedinice za resurse ne vraća prodajnu cijenu s prodajnog cjenika, sustav zanemaruje jedinicu za resurse. Umjesto toga, pretražuje kombinaciju uloge i jedinice za postavljanje zadane cijene (nakon primjene bilo koje konverzije).

Ako sustav ne pronađe cijenu za ulogu, prodajna cijena u retku procjene postavlja se na zadanu vrijednost **0,00**.

Kartica **Procjene** ima prikaz rešetke koji prikazuje retke procjene. Rešetka uključuje stupce za jedinicu, ukupnu cijenu troškova i ukupnu prodajnu cijenu, kao što je prikazano na sljedećoj ilustraciji. 

> ![Prikaz rešetke na kartici Procjene](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Prikaz procjene projekta s vremenskim fazama

Prikaz s vremenskim fazama procjene projekta prikazuje podatke procjene iz prikaza rešetke na vremenskoj crti u vremenskom mjerilu koje odaberete. Prema zadanim postavkama podaci procjene zaokreću se po dimenziji **Uloga**.

> ![Prikaz procjena projekta s vremenskim fazama](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Dodjela procijenjenog rada na temelju načina zadatka

U prikazu s vremenskim fazama ukupni procijenjeni rad za zadatak raspoređuje se dodjelom određenog broja sati rada po vremenskom razdoblju odabranog vremenskog mjerila. Način zadatka određuje kako se rad dodjeljuje za vrijeme trajanja zadatka. Dvije su vrste dodjele **Ravnomjerno** i **Na temelju radnog vremena**.

### <a name="work-hours-based-allocation"></a>Dodjela na temelju radnog vremena
 
U načinu automatskog raspoređivanja zadataka dnevni zadani sati za resurse zadatka postavljeni su na puno radno vrijeme. To se ponašanje primjenjuje i kada se rad dodjeljuje dijeljenjem na trajanje zadatka u prikazu s vremenskim fazama. Na primjer, ako procijenite da će se zadatak dovršiti s jednim resursom jednom u vremenskom mjerilu **Dan**, dodijeljeni rad po danu neće premašivati radno vrijeme po danu definirano u kalendaru projekta. Zbog toga dodjela rada uvijek osigurava da se procjenjuje korištenje resursa cijeli dan.

### <a name="even-allocation"></a>Ravnomjerna dodjela

U ručno zakazanom načinu zadatka ne koristi se radno vrijeme iz kalendara projekta. Umjesto toga, raspored zadatka temelji se na korisničkom unosu. Za takve zadatke dodjela rada po vremenskom razdoblju odabranog vremenskog mjerila nema ograničavajuće čimbenike. Ukupni rad na zadatku ravnomjerno se dijeli i dodjeljuje za svako vremensko razdoblje jedinice u odabranom vremenskom mjerilu. Stoga definirani način zadatka određuje distribuciju rada ili dodjelu rada po vremenskom razdoblju jedinice u procjenama s vremenskim fazama.

## <a name="grouping-and-time-phasing-options"></a>Mogućnosti grupiranja i vremenskih faza

Ovaj prikaz s vremenskim fazama prikazuje distribuciju procjene rada, troška i prodaje na dnevnoj, tjednoj, mjesečnoj i godišnjoj osnovi. Prema zadanim postavkama podaci procjene zaokreću se po dimenziji **Uloga**. Međutim, možete koristiti mogućnost **Grupiraj po** da biste zaokrenuli druge dvije dimenzije: **Kategorija** i **Resurs**.

U prikazu rešetke i prikazu s vremenskim fazama možete odabrati koja će se polja prikazivati. Ukupne vrijednosti za svaki vremenski blok prikazuju se na dnu projekta. One prikazuju ukupni procijenjeni rad, trošak i prodaju za dan, tjedan, mjesec ili godinu. Zadana cijena troška i prodajna cijena temelje se na datumu. Drugim riječima, mijenjaju se za svaki resurs na temelju prikaza s vremenskim fazama koji ste odabrali.

## <a name="expense-estimates"></a>Procjena troška

Gumb **Dodaj novu procjenu troška** u prikazu rešetke omogućuje vam bilježenje svih troškova nastalih u projektu, no onih koji nisu izravno povezani s radom. Procjene troškova možete bilježiti za određeni zadatak ili za cijeli projekt. Odaberite kategorije troškova i uvjetni datum kada se trošak očekuje. Ako povezani cjenik troškova i prodajni cjenik imaju zadane cijene (ili definiranu profitnu maržu za kategorije troškova), one se automatski unose u retku procjene kod povezivanja.
