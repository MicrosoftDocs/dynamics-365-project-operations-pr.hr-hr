---
title: Konfiguriranje upravljanja troškovima
description: U ovom se članku opisuju razmatranja i odluke koje morate donijeti tijekom postupka planiranja, prije nego što konfigurirate upravljanje troškovima u aplikaciji Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eca4362b0ff5d37b131e1d96e311aa48ac20397618314936944ba66e458dbdc2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007452"
---
# <a name="configure-expense-management"></a>Konfiguriranje upravljanja troškovima

U ovoj se temi opisuju razmatranja i odluke koje morate donijeti tijekom postupka planiranja, prije nego što konfigurirate upravljanje troškovima. U modul Upravljanje troškovima možete pohranjivati informacije o načinima plaćanja, putnim nalozima, izvješćima o troškovima, pravilima itd.

Budući da se mnoge odluke koje donosite kada planirate svoju konfiguraciju modula Upravljanje troškovima temelje na hijerarhiji i financijskoj strukturi vaše tvrtke ili ustanove, morate pogledati dokumente za planiranje tih područja.

## <a name="intercompany-expenses"></a>Međukompanijski troškovi

Kada omogućite troškove unutar tvrtke, dopuštate pravnim osobama i zaposlenicima da prave troškove u ime druge pravne osobe i prikupljaju uplate od pravne osobe koja radi unutar vaše tvrtke ili ustanove. Na primjer, zaposlenik u pravnoj osobi A dovršava projekt za pravnu osobu B, a projekt snosi povezane troškove putovanja. Ako su omogućeni troškovi unutar tvrtke, zaposlenik tada može podnijeti izvješće o troškovima koje će se knjižiti na pravnu osobu B, a trošak tada mora platiti pravna osoba A. Ako vaša tvrtka ili ustanova nema više pravnih osoba, ne morate omogućiti troškove unutar tvrtke.

**Odluka:** Želite li omogućiti troškove unutar tvrtke?

## <a name="financial-management"></a>Financijsko upravljanje

Upravljanje troškovima čvrsto je integrirano s upravljanjem financijama vaše tvrtke ili ustanove. Dosta od vaše konfiguracije za upravljanje troškovima temeljit će se na odlukama koje ste donijeli o financijama vaše tvrtke ili ustanove. Sljedeći odjeljci opisuju različita područja koja zahtijevaju planiranje i donošenje odluka, na temelju financijskih odluka vaše tvrtke ili ustanove i smjernica vašeg upravljačkog tima.

### <a name="per-diems"></a>Po danima

Morate definirati zaposlenike po dnevnicama koje osigurava vaša tvrtka ili ustanova. Budući da se dnevnice obično upotrebljavaju za pokrivanje troškova poput prehrane, smještaja i ostalih sporednih troškova, možete stvoriti pravila za dnevnice koje daje vaša tvrtka ili ustanova. Cijene dnevnica mogu se temeljiti na dobu godine, mjestu putovanja ili oboje. Kada definirate pravilo za dnevnice, možete odrediti da se od dnevnice odbija postotak ako radnik prima besplatne obroke ili usluge. Također, možete definirati razine cijena dnevnica koje se postavljaju za minimalni i maksimalni broj sati za koji se dnevnica može primijeniti kada je radnik na putu.

**Odluke:**

- Zadana pravila za dnevnice za prvi i zadnji dan:

    - Koji je minimalan broj sati koje zaposlenik može prijaviti u danu kako bi dobio dnevnicu?
    - Postoji li smanjenje iznosa koji se daje za obroke za prvi dan i zadnji dan? Ako postoji smanjenje, koliki je postotak smanjenja?
    - Postoji li smanjenje iznosa koji se daje za hotel za prvi dan i zadnji dan? Ako postoji smanjenje, koliki je postotak smanjenja?
    - Postoji li smanjenje iznosa koji se daje za ostale troškove koji nastaju prvi dan i zadnji dan? Ako postoji smanjenje, koliki je postotak smanjenja?

- Zadana pravila za dnevnicu:

    - Postoji li postotno smanjenje dnevnice za svaki obrok ako je, na primjer, obrok besplatan? Ako postoji smanjenje, koliki je postotak smanjenja za svaki obrok?
    - Izračunava li se smanjenje za obrok po danu, po putovanju ili po broju dnevnih obroka?
    - Treba li iznose dnevnica redovito popunjavati ili ih treba prikupljati?
    - Izračunavaju li se dnevnice na 24-satno razdoblje ili na kalendarski dan?

- Pravila za dnevnice koja se temelje na lokaciji:

    - Razlikuju li se dnevnice ovisno o lokaciji? Koje su lokacije uključene?
    - Ako se dnevnice razlikuju ovisno o mjestu, koliki se postotni iznos daje za sljedeće vrste troškova:

        - Obroci
        - Hoteli
        - Ostali troškovi

### <a name="expense-management-journals-and-accounts"></a>Dnevnici i računi za upravljanje troškovima

Upravljanje troškovima zahtijeva uporabu više dnevnika i računa. Morate odlučiti, na primjer, hoće li se isti račun upotrebljavati za gotovinske predujmove i povrate po kreditnim karticama.

**Odluke:**

- U koji se dnevnik glavne knjige knjiže odobrena izvješća o troškovima?
- Koji se račun upotrebljava za gotovinske predujmove?
- Treba li odmah knjižiti gotovinske predujmove?

### <a name="payment-methods"></a>Načini plaćanja

Kad zaposlenicima dopuštate da prave troškove u ime vaše tvrtke, morate definirati načine plaćanja koje zaposlenici smiju upotrebljavati. Na primjer, zaposlenicima možete dopustiti uporabu gotovine ili korporativne kreditne kartice. Također zaposlenicima možete dopustiti da se koriste osobnom kreditnom karticom, nakon čega im nadoknađujete novac. Morate donijeti sljedeće odluke za svaki način plaćanja koji dopustite.

**Odluke:**

- Koji su načini plaćanja dopušteni?
- Tko podmiruje troškove načina plaćanja?
- Postoji li vrsta računa za prijeboj? Ako postoji vrsta računa za prijeboj, što je to?
- Ako postoji vrsta računa za prijeboj, što je račun?
- Ako je način plaćanja kreditna kartica, treba li se način plaćanja upotrebljavati samo s uvoznim transakcijama?

### <a name="expense-categories-and-shared-categories"></a>Kategorije troškova i dijeljene kategorije

Kad zaposlenici stvaraju izvješće o troškovima, svaki trošak koji evidentiraju mora biti povezan s kategorijom troška. Kategorije troškova izvedene su iz dijeljenih kategorija koje se mogu dijeliti između pravnih osoba u vašoj tvrtki ili ustanovi. Te se kategorije također mogu dijeliti u Upravljanju projektima i računovodstvu, ovisno o načinu na koji je definirana vaša tvrtka ili ustanova. Na temelju definicije vaše tvrtke ili ustanove i smjernica implementacijskog tima, morate odrediti hoće li se kategorije koje se upotrebljavaju u Upravljanju troškovima upotrebljavati samo u Upravljanju troškovima ili bi ih se trebalo dijeliti između Upravljanja projektom i računovodstvom i Upravljanja troškovima. Imajte na umu kako se te kategorije mogu dijeliti između Projekta i Troška ili Projekta i Proizvodnje, ali ne i između Troška i Proizvodnje. Morate donijeti sljedeće odluke za svaku kategoriju troškova.

**Odluke:**

- Što je kategorija troškova? Primjeri uključuju kategorije za letove, hotele ili kilometražu.
- Može li se kategorija troškova upotrebljavati i za Upravljanje projektima i računovodstvo?
- Što je vrsta troškova?
- Koji je zadani način plaćanja za kategoriju troškova?
- Moraju li se specificirati troškovi iz kategorije troškova?
- Koji je glavni zadani račun za kategoriju troškova?
- Koja je zadana stavka grupe poreza na promet za kategoriju troškova?
- Jesu li dodatni načini plaćanja dozvoljeni za kategoriju troškova? Ako su dopušteni dodatni načini plaćanja, koji su to načini?
- Postoje li potkategorije u ovoj kategoriji troškova? Ako postoje potkategorije, morate također donijeti sljedeće odluke:

    - Je li neka od potkategorija izuzeta iz povrata poreza?
    - Koja je stavka grupe poreza na promet potkategorija?

Ako se kategorija troškova upotrebljava i u Upravljanju projektom i računovodstvu, odgovorite na preostala pitanja. U suprotnom, prijeđite na sljedeći odjeljak.

- Koji će se računi za troškove upotrebljavati za sljedeće troškove?

    - Cijena
    - Raspodjela plaća
    - Vrijednost troškova WIP-a
    - Troškovna stavka
    - Vrijednosna stavka troškova WIP-a
    - Obračunani gubitak
    - Obračunani gubitak WIP-a

- Koji će se računi za prihod upotrebljavati za sljedeće?

    - Fakturirani prihod
    - Obračunani prihod – vrijednost prodaje
    - Prodajna vrijednost WIP-a
    - Obračunani prihod proizvodnje
    - Proizvodnja WIP-a
    - Obračunani prihod – dobit
    - Dobit WIP-a
    - Obračunani prihod – pretplata
    - Pretplata WIP-a

### <a name="taxes"></a>Porezi

Za poreze povezane s troškovima morate odrediti što je uključeno ili omogućeno u izvješćima o troškovima.

**Odluke:**

- Je li porez na promet uključen u iznose troškova?
- Treba li omogućiti povrat poreza na troškove?

    > [!NOTE]
    > Kada ste planirali glavnu knjigu, ako ste odlučili primijeniti porez na promet SAD-a i upotrebljavati odgovarajuće porezne propise, ne možete omogućiti povrat poreza na troškove. (Kako biste primijenili porez na promet SAD-a i upotrebljavali odgovarajuće porezne propise, mogućnost **Primijeni pravila oporezivanja poreza na promet** postavite na **Da**.)

## <a name="policies"></a>Pravilnici

Stvaranjem pravila za izvješćivanje o troškovima možete pomoći svojoj tvrtki ili ustanovi da uštedi vrijeme i novac kada zaposlenici naprave troškove u njezino ime. Pravila jamče da zaposlenici ostanu unutar proračuna, pruže sve potrebne podatke i troše novac samo onako kako im je potrebno. Morate donijeti sljedeće odluke za svaki pravilnik za izvješća o troškovima i za odobravanje izvješća o troškovima koje stvarate.

**Odluke:**

- Koji je naziv pravilnika?
- Čemu služi pravilnik o trošku?
- Ako ste prethodno odlučili omogućiti troškove među tvrtkama, na koje će se tvrtke u vašoj tvrtki ili ustanovi primjenjivati ovaj pravilnik?
- Kada pravilnik stupa na snagu?
- Kada pravilnik prestaje vrijediti?
- Što je pravilo iz pravilnika?
- Koji je ishod pravila iz pravilnika?


[!INCLUDE[footer-include](../includes/footer-banner.md)]