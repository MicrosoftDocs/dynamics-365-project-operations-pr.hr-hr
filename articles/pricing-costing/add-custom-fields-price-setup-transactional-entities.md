---
title: Dodavanje potrebnih prilagođenih polja postavljanju cijena i transakcijskim entitetima
description: U ovoj se temi nalaze informacije o načinu dodavanja potrebne reference prilagođenih polja na entitete te na obrasce i prikaze.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a27bfe881fdb6431941fa860d279e3e7b526f623
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898297"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Dodavanje potrebnih prilagođenih polja postavljanju cijena i transakcijskim entitetima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

U ovoj se temi pretpostavlja kako ste dovršili u temi opisane postupke, [Stvaranje prilagođenih polja i entitete koji će se upotrebljavati kao dimenzije za određivanje cijena](create-custom-fields-entities-pricing-dimensions.md). Ako niste dovršili te postupke, vratite se i dovršite ih, a zatim se vratite na ovu temu. 

U ovoj temi, postupci će vam pokazati kako dodati potrebne reference prilagođenih polja entitetima i elementima korisničkog sučelja (UI) kao što su obrasci i prikazi.

## <a name="add-custom-pricing-dimension-fields"></a>Dodaj polja dimenzije prilagođenog određivanja cijena 
Nakon izrade prilagođenih polja i entiteta, sljedeći je korak da entiteti postavljanja cijena i transakcijski entiteti prepoznaju bilo koje prilagođene entitete ili skupove mogućnosti s pomoću izrade referentnih polja. Ovisno o tome uključuje li popis dimenzija određivanja cijena dimenzije skupa mogućnosti ili dimenzije entiteta ili oboje, slijedite samo korake u **Dimenzije prilagođenog određivanja cijena koje se temelje na skupu mogućnosti** ili **Dimenzije prilagođenog određivanja cijena koje se temelje na entitetu** ili oboje.

### <a name="option-set-based-custom-pricing-dimensions"></a>Dimenzije prilagođenog određivanja cijena koje se temelje na skupu mogućnosti
Kada se dimenzija prilagođenog određivanja cijena mogućnost koja se temelji na skupu, dodajte je ključnim entitetima kao polje. U sljedećem postupku, **Mjeso rada resursa** i **Radno vrijeme resursa** koriste se kao dimenzije određivanja cijena na temelju skupa mogućnosti. Oni prvo moraju biti dodani kao polja u entitete određivanja cijena, **Cijena uloge** i **Marža cijene uloge**.

1. U aplikaciji Project operations odaberite **Postavke** > **Rješenja** i dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**. 
2. U istraživaču rješenja, u lijevom navigacijskom oknu odaberite **Entiteti > Cijena uloge**.
3. Proširite entitet **Cijena uloge** i odaberite **Polja**.
4. Odaberite **Novo** kako biste stvorili novo polje pod nazivom **Mjesto rada resursa** i kao vrstu polja odaberite **Skup mogućnosti**. 
5. Odaberite **Upotrijebi postojeći skup mogućnosti**, odaberite skup mogućnosti **Mjesto rada resursa**, a zatim odaberite **Spremi**.
6. Ponovite korake 1 - 5 da biste dodali ovo polje entitetu **Marža cijene uloge**. 
7. Ponovite korake 1 - 5 za skup mogućnosti **Radno vrijeme resursa**.

> [!IMPORTANT]
> Kada dodate polje u više entiteta, koristite isti naziv polja na svim entitetima. 

U fazama prodaje i procjene projekta, procjene radnih napora potrebnih za dovršetak **Terenskog** i **Uredskog** rada, u **Redoviti sati** i **Prekovremeni sati**  koriste se za procjenu vrijednosti ponude/projekta. Polja **Mjesto rada resursa** i **Radno vrijeme resursa** dodat će se entitetima procjene, **Pojedinost retka ponude**, **Pojedinost retka ugovora**, **Član tima projekta** i **Redak procjene**.

1. U aplikaciji Project operations odaberite **Postavke** > **Rješenja** i zatim dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**. 
2. U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Entiteti > Pojedinost retka ponude**.
3. Proširite entitet **Pojedinost retka ponude** i odaberite **Polja**.
4. Odaberite **Novo** kako biste stvorili novo polje pod nazivom **Mjesto rada resursa** i odaberite vrstu polja, **Skup mogućnosti**. 
5. Odaberite **Upotrijebi postojeći skup mogućnosti** i **Mjesto rada resursa**, a zatim odaberite **Spremi**.
6. Ponovite korake 1 - 5 da biste dodali ovo polje u entitete **Pojedinost retka ugovora projekta**, **Član tima projekta** i **Redak procjene**.
7. Ponovite korake 1 - 6 za skup mogućnosti **Radno vrijeme resursa**. 

Da bi se izvršili isporuka i fakturiranje, za završeni rad mora biti precizno određena cijena da bi se moglo odabrati je li izvršen **Na terenu** ili **U uredu** te je li dovršen tijekom **Redovitih sati** ili **Prekovremenih sati** u Stvarnim vrijednostima projekta. Polja **Radno mjesto resursa** i **Radno vrijeme resursa** treba dodati u entitete **Unos vremena**, **Stvarna vrijednost**, **Pojedinost retka fakture** i **Redak u dnevniku**.

1. Odaberite **Postavke** > **Rješenja** i zatim dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**.
2. U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite  **Entiteti > Unos vremena**.
3. Proširite entitet **Pojedinost retka ponude** i zatim odaberite **Polja**.
4. Odaberite **Novo** kako biste stvorili novo polje pod nazivom **Mjesto rada resursa** i kao vrstu polja odaberite **Skup mogućnosti**. 
5. Odaberite **Upotrijebi postojeći skup mogućnosti**, odaberite skup mogućnosti **Mjesto rada resursa**, a zatim odaberite **Spremi**.
6. Ponovite korake 1 - 5 da biste dodali ovo polje u entitete **Stvarna vrijednost**, **Pojedinost retka fakture** i **Redak u dnevniku**.
7. Ponovite korake 1 - 6 za skup mogućnosti **Radno vrijeme resursa**. 

Time se dovršavaju promjene sheme potrebne za prilagođene dimenzije koje se temelje na skupu mogućnosti.

## <a name="entity-based-custom-pricing-dimensions"></a>Dimenzije prilagođenog određivanja cijena koje se temelje na entitetu

Kada je dimenzija prilagođenog određivanja cijena entitet, dodat ćete odnose 1:N između entiteta dimenzije i ključnih entiteta. Korištenjem primjera Standardna titula koji je naveden gore, razumno je očekivati da je svakom zaposleniku dodijeljena standardna titula. Kao rezultat toga, trebat ćete odnos 1:N Standardne titule prema Resursu koji se može rezervirati ili odnos N:1 ako se stvara u slučaju Resursa koji se može rezervirati prema Standardnoj tituli.

1. U aplikaciji Project operations odaberite **Postavke** > **Rješenja** i zatim dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**. 
2. U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Entiteti > Standardna titula**.
3. Proširite entitet **Standardna titula** i odaberite **Odnosi 1:N**.
4. Odaberite **Novo** kako biste stvorili novi odnos 1:N pod nazivom **Standardni naslov resursa koji se može rezervirati**. Unesite potrebne informacije, a zatim odaberite **Spremi**.

Standardni će se naslov također morati dodati entitetima za određivanje cijena, **Cijena uloge** i **Provizija cijene uloge**. To se također izvodi koristeći odnose 1:N između entiteta **Standardna titula** i **Cijena uloge** i entiteta **Standardna titula** i **Marža cijene uloge**.

1. U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Entiteti > Standardna titula**.
2. Proširite entitet **Standardna titula** i odaberite **Odnosi 1:N**.
3. Odaberite **Novo** kako biste stvorili novi odnos 1:N pod nazivom **Standardni naslov cijene uloge**. Unesite potrebne informacije, a zatim odaberite **Spremi**.
4. Ponovite korake 1 - 4 da biste stvorili odnose 1:N između entiteta **Standardna titula** i **Marža cijene uloge**,

U fazama prodaje i procjene za projekt, kod određivanja cijena ponude/projekta potrebne su procjene radnog napora za svaku standardnu titulu. To znači da su potrebni odnosi 1:N Standardnog naslova prema svakom od tih entiteta procjene: 

- **Pojedinost retka ponude**
- **Pojedinost retka ugovora projekta**
- **Član tima projekta**
- **Redak procjene**

5. Ponovite korake 1 - 5 za stvaranje odnosa 1: N **Standardne titule** prema **Pojedinosti retka ponude**, **Pojedinosti retka ugovora projekta**, **Članu tima projekta**, i **Retku procjene**.

  U fazama isporuke i fakturiranja, za rad dovršen od strane svake standardne titule mora biti točno određena cijena na stvarnim vrijednostima projekta. To znači da moraju postojati odnosi 1:N **Standardne titule** prema **Unosu vremena**, **Stvarnoj vrijednosti**, **Pojedinosti retka fakture** i **Entitetima retka u dnevniku**.

6. Ponovite korake 1 - 6 da biste stvorili odnose 1:N **Standardne titule** prema **Unosu vremena**, **Stvarnoj vrijednosti**, **Pojedinosti retka fakture** i **Entitetima retka u dnevniku**.

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Postavljanje zadane vrijednosti dimenzije s pomoću značajki mapiranja platforme
Za Unos vremena, bilo bi korisno da sustav standardnu titulu na Unosu vremena postavi kao zadanu od Resursa koji se može rezervirati koji zapisuje Unos vremena. Koristite sljedeće korake za dodavanje mapiranja polja u odnos 1:N **Resursa koji se može rezervirati** prema **Unosu vremena**.

1. U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Entiteti > Standardna titula**.
2. Proširite entitet **Standardna titula** i odaberite **Odnosi 1:N**.
3. Kliknite dvaput **Resurs koji se može rezervirati prema unosu vremena**. Na stranici **Odnos**, odaberite **Upotrijebi mapiranja polja**. 
4. Odaberite **Novo** kako biste stvorili novo mapiranje polja između polja **Standardni naslov** u entitetu **Resurs koji se može rezervirati** prema polju refernce **Standardni naslov** u entitetu **Vremenski unos**. 

Time se dovršavaju promjene sheme potrebne za prilagođene dimenzije koje se temelje na entitetu.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Dodaj prilagođena polja obrascima, prikazima i poslovnim pravilima

Nakon što ste izvršili sve potrebne promjene sheme, sljedeći je korak omogućavanje vidljivosti polja u korisničkom sučelju dodavanjem polja obrascima i prikazima.

1. Otvorite obrazac ili prikaz. U desnom navigacijskom oknu, odaberite polje i povucite ga u radno područje obrasca. 
2. Ako uređujete prikaz, upotrijebite desno navigacijsko okno, odaberite **Dodaj polja**, a zatim u dijaloškom okviru **Popis polja** odaberite polja koja vam trebaju i odaberite **U redu**.

Sljedeća tablica prikazuje sveobuhvatan popis gotovih obrazaca i prikaza koji su navedeni po entitetu, a koji se trebaju ažurirati s novim poljima. Ako u prilagodbama tih entiteta postoje dodatni prikazi ili obrasci, njima također dodajte nova polja.

| Entity        | Obrasci kojima je potrebno novo polje   |Prikazi kojima je potrebno novo polje      |
| ------------------------------|---------------------------------|----------------------------------|
|  Cijena uloge|• Informacije |• Cijene kategorije aktivnog resursa<br> • Pridruženi prikaz cijene kategorije resursa|
|  Provizija cijene uloge|• Informacije|• Aktivna provizija cijene uloge<br>• Pridruženi prikaz provizije cijene uloge|
|  Pojedinost retka ponude|• Informacije o projektu<br>• Brzo stvaranje projekta|• Pojedinost retka aktivne ponude<br>• Kombinirane pojedinosti retka ponude<br>• Pridruženi prikaz pojedinosti retka ponude|
|  Pojedinost retka ugovora projekta|• Informacije o projektu<br>• Brzo stvaranje projekta|• Pojedinosti retka kombiniranog ugovora<br>• Pojedinosti aktivnog retka ugovora<br>• Povezani pogled pojedinosti retka ugovora|
|  Član projektnog tima|• Informacije<br>• Novi obrazac|• Aktivni članovi projektnog tima<br>• Članovi projektnog tima<br>• Pridruženi prikaz članova projektnog tima|
|  Unos vremena|• Informacije<br>• Stvaranje unosa vremena|• Moji Unosi vremena po datumu<br>• Moji Unosi vremena za ovaj tjedan<br>• Unos vremena za odobrenje|
|  Redak u dnevniku|• Informacije<br>• Brzo stvaranje|• Reci u aktivnom dnevniku<br>• Pridruženi prikaz retka u dnevniku|
|  Pojedinost retka fakture|• Informacije<br>• Brzo stvaranje|• Pojedinosti retka aktivne fakture<br>• Naplative transakcije fakture<br>• Besplatne transakcije fakture<br>• Pridruženi prikaz pojedinosti retka fakture<br>• Nenaplative transakcije fakture|
|  Stvarna vrijednost|• Informacije<br>• Aktivni stvarni podaci|• Pridruženi prikaz stvarnih podataka|

Prilagođena polja potencijalno se također moraju dodati na poslovna pravila, ovisno o tome što ste definirali. Jedan gotovi primjer je za poslovno pravilo **Uređivanje unosa vremena na temelju statusa**. Ovo pravilo definira koja je polja potrebno zaključati kada se Unos vremena nalazi u statusu nemogućnosti uređivanja, kao što je **Odobreno**. Dodajte polja ovom poslovnom pravilu tako da su polja zaključana za uređivanje kada je Unos vremena u statusu koji nije **Skica** ili **Vraćeno**.
