---
title: Koncepti jedinstveni za ponude koji se temelje na projektu
description: U ovom se članku nalaze informacije o ponudama za projekte u microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824318"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Koncepti jedinstveni za ponude koji se temelje na projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Prije nego što počnete koristiti ponude za projekte u Microsoftu Dynamics 365 Project Operations, trebali biste biti svjesni sljedećih ključnih koncepata.

## <a name="owning-company"></a>Tvrtka vlasnik

Vlastito poduzeće predstavlja pravnu osobu koja je vlasnik isporuke projekta. Kupac na ponudi trebao bi biti valjani kupac u toj pravnoj osobi u financijskim i operativnim aplikacijama. Valuta poduzeća u vlasništvu i valuta ugovorne jedinice odabrane na ponudi koja se temelji na projektu moraju se podudarati.

## <a name="contracting-unit"></a>Ugovorna jedinica

Ugovorna jedinica predstavlja podjelu ili praksu u čijem je vlasništvu isporuka projekta. Možete postaviti troškove resursa za svaku ugovornu jedinicu. Kada navedete troškove resursa za resurs u ugovornoj jedinici, možete postaviti različite stope troškova za resurse iz kojih jedinica ugovaranja posuđuje ili za druge odjele ili prakse u poduzeću. Ti se tečajevi nazivaju transfernim cijenama, zaduživanjem resursa ili tečajnim cijenama. Kada postavite trošak posudbe resursa iz drugih odjela, možete postaviti tečajeve u valuti odjela za posudbu.

## <a name="cost-currency"></a>Valuta troška

Valuta troška u projektnim operacijama je valuta u kojoj se iskazuju troškovi. Ova valuta izvedena je iz valute pridružene **polju Ugovorna jedinica** na ponudi, ugovoru i projektu. Troškovi za projekt mogu se zabilježiti u bilo kojoj valuti. Međutim, dolazi do konverzije valute iz valute u kojoj su troškovi zabilježeni u valuti troškova projekta.

Budući da tečajevi na Dataverse platformi ne mogu biti na snazi po datumu, ukupni iznosi troškova na zaslonu mogu se s vremenom promijeniti ako ažurirate tečajeve valuta. Međutim, troškovi koji su zabilježeni u bazi podataka ostaju nepromijenjeni, jer se iznosi pohranjuju u valuti u kojoj su nastali.

## <a name="sales-currency"></a>Valuta prodaje

Prodajna valuta u operacijama projekta valuta je u kojoj se bilježe i prikazuju procijenjeni i stvarni iznosi prodaje. To je ujedno i valuta u kojoj se kupcu fakturira za posao. Za ponudu projekta zadana prodajna valuta postavljena je iz zapisa o klijentu ili računu i može se promijeniti prilikom kreiranja ponude. Međutim, prodajna valuta ne može se promijeniti nakon spremanja ponude. Zadani cjenici proizvoda i projekata postavljaju se na temelju prodajne valute ponude.

Za razliku od troškova, prodajne vrijednosti mogu se bilježiti **samo** u prodajnoj valuti.

## <a name="billing-method"></a>Način naplate

Projekti obično imaju modele ugovaranja s fiksnom naknadom i potrošnjom. U projektnim operacijama model ugovaranja projekta predstavljen je metodom naplate. Način naplate ima dvije vrijednosti: vrijeme i materijalnu i fiksnu cijenu.

- **Vrijeme i materijal**  – model ugovaranja temeljen na potrošnji u kojem je svaki nastali trošak potkrijepljen odgovarajućim prihodom. Kako procjenjujete ili pravite više troškova, povećavaju se i odgovarajuće procijenjena i stvarna prodaja. U redcima ponude koji imaju ovaj način naplate možete odrediti ograničenja koja ne smiju premašiti. Na taj način možete ograničiti stvarni prihod. Na procijenjeni prihod ne utječu ograničenja koja se ne smiju prekoračiti.
- **Fiksna cijena**  - Model ugovaranja s fiksnom naknadom u kojem su prodajne vrijednosti neovisne o nastalim troškovima. Prodajna je vrijednost fiksna i ne mijenja se kako procijenite ili napravite više troškova.

## <a name="project-price-lists"></a>Cjenici za projekt

Cjenici projekta su cjenici koji se koriste za unos zadanih cijena, a ne troškovnih stopa, za vrijeme, troškove i druge komponente povezane s projektom. Cjenika može biti više, a svaki popis može imati svoj datum stupanja na snagu za svaku ponudu projekta. Projektne operacije ne podržavaju preklapajuću efektivnost datuma za cjenike projekta.

## <a name="product-price-lists"></a>Cjenici proizvoda

Cjenici proizvoda su cenovnici koji se koriste za unos zadanih cijena, a ne troškovnih stopa za retke temeljene na proizvodu na ponudi. Postoji samo jedan cjenik proizvoda po ponudi.

## <a name="transaction-classes"></a>Klase transakcija

Project Operations podržava četiri vrste klasa transakcija:

- Vrijeme
- Izdatak
- Materijal
- Naknada

Vrijednosti troškova i prodaje mogu se procijeniti i nastati u **klasama transakcija Vrijeme**, **Trošak** i **Materijal** . **Naknada** je klasa transakcija samo prihoda.

## <a name="work-entities-and-billing-entities"></a>Entiteti rada i naplate

Projekti i zadaci su entiteti koji predstavljaju posao. Reci ponude i Reci ugovora subjekti su koji predstavljaju naplatu. Različite poslovne subjekte možete povezati s mogućnostima naplate tako da ih povežete s recima ponude ili recima ugovora.

## <a name="multi-customer-deals"></a>Poslovi s više klijenata

Ponude za više kupaca događaju se kada postoji više od jednog kupca po fakturi. Evo nekoliko tipičnih primjera:

- **Poduzeća proizvođača originalne opreme (OEM) i njihovi partneri**  - Partneri i preprodavači prodaju proizvod koji uključuje usluge s dodanom vrijednošću. Tijekom dogovora s kupcem, OEM obično nudi financiranje dijela projekta.
- **Projekti**  javnog sektora- Više odjela lokalne samouprave pristalo je financirati projekt i fakturira se prema prethodno dogovorenom razlazu. Na primjer, školski okrug i gradska uprava ili odjel lokalne uprave dogovore se financirati izgradnju bazena.

## <a name="invoice-schedules"></a>Rasporedi fakturiranja

Rasporedi faktura specifični su za svaki redak ponude i nisu obavezni. Rasporedi faktura kreiraju se na temelju određenog datuma početka i završetka te učestalosti fakture. Koriste se tijekom faze ugovora kada je konfiguriran postupak automatskog stvaranja fakture. Tijekom faze ponude rasporedi faktura nisu obavezni. Ako su kreirani tijekom faze ponude, kopiraju se u ugovor o projektu koji se stvara prilikom osvojene ponude za projekt.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Razlike u odnosu na prodajne ponude sustava Dynamics 365

Ponude za operacije projekta izrađene su na prodajnim ponudama sustava Dynamics 365. Međutim, postoje neke važne razlike u funkcionalnosti koje biste trebali znati:

- Ponude za projektne operacije imaju dvije različite vrste linija: jednu za projekte i jednu za proizvode.
- Ponude za project operations imaju vlastite elemente stranice i korisničkog sučelja ( korisničko sučelje), poslovna pravila, poslovnu logiku u dodacima i skripte na strani klijenta koje ih razlikuju od prodajnih ponuda.
- U odjeljku Prodaja jednoj prodajnoj ponudi možete priložiti više naloga. U projektnim operacijama možete priložiti samo jedan projektni ugovor ponudi.
- Kada osvojite prodajnu ponudu, povezana prilika može ostati otvorena. Nakon što se dobije projetna ponuda, povezana prilika je zatvorena.
- Prodajna ponuda ne uključuje neka polja i koncepte koje uključuje ponuda projekta. Polja uključuju **Ugovornu jedinicu**, **Upravitelja računa** i **Naziv fakture za kontakt**.
- Prodajne ponude i ponude za projekte identificiraju se poljem Vrsta **koja se temelji na** skup mogućnosti. Za prodajnu ponudu vrijednost ovog polja temelji se **na artiklu**. Za ponudu projekta vrijednost se **temelji na radu**.

Zbog tih razlika ne preporučujemo da naizmjenično koristite prodajne ponude i ponude za projektne operacije.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
