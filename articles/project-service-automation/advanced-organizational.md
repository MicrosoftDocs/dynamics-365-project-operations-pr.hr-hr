---
title: Organizacijske jedinice
description: Ova tema pruža informacije o organizacijskim jedinicama u sustavu Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 47855fdd-befa-4203-856d-4e917ecfc16d
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 7282b83516e9234b5717b0b5d82d6650bc70f9d2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750219"
---
# <a name="organizational-units"></a>Organizacijske jedinice 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation, organizacijska jedinica je zasebna grupa ili odjel u poduzeću za profesionalne usluge koja zapošljava naplative resurse koji imaju stope troškova.

Za poduzeća za profesionalne usluge koja zapošljavaju tehničke resurse u različitim područjima prakse ili poslovnim linijama, trošak ispune uloge u jednom području prakse ili poslovne linije može se razlikovati od troška ispune uloge u drugom području prakse ili poslovne linije. Koncept organizacijskih jedinica pomaže u ovom scenariju pružajući način za grupiranje skupa naplativih uloga u odjelu poduzeća koje ima različitu strukturu troškova za te uloge.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Ključni atributi i udruženja organizacijskih jedinica

U PSA, organizacijska jedinica u sustavu PSA ima određenu valutu i određeni cjenik troškova.

Valuta organizacijske jedinice primarna je valuta koja se koristi za praćenje troškova.

Jedan ili više cjenika troškova može se priložiti svakoj organizacijskoj jedinici. PSA stavlja sljedeća ograničenja na cjenike koji se mogu priložiti organizacijskoj jedinici:

- Cjenici moraju biti u valuti organizacijske jedinice
- Cjenici moraju biti usklađeni s cjenicima troškova

Osim toga, postoji atribut za organizacijsku jedinicu na entitetu Resurs. Svaki je resurs moguće dodijeliti jednoj organizacijskoj jedinici.

## <a name="roles-of-organizational-units"></a>Uloge organizacijskih jedinica

Organizacijska jedinica igra dvije uloge u sustavu PSA:

- **Ugovorna jedinica** – Organizacijska jedinica koja predstavlja grupu ili odjel poduzeća koja je prvenstveno odgovorna za ostvarivanje prodaje i upravljanje isporukom rada i usluga klijentu. Ugovorna jedinica identificira se poljem **Ugovorna jedinica** u odjeljku zaglavlja stranica **Prilika**, **Ponuda**, **Ugovor o projektu** i **Projekt**.
- **Jedinica resursa** – Organizacijska jedinica kojoj resurs pripada ili je dodijeljen. Ova organizacijska jedinica može osigurati svoje resurse za neke uloge na izjavama o radu (svo) i projektima koji su u vlasništvu ugovorne jedinice.

> ![Ugovorne jedinice i jedinice resursa](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Često postavljena pitanja o Organizacijskim jedinicama

Ovdje ćete pronaći često postavljena pitanja o organizacijskim jedinicama.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Kako je entitet Organizacijska jedinica u sustavu PSA povezan s entitetom Organizacija koji već postoji u sustavu Dynamics 365?

Entitet Organizacija u sustavu Microsoft Dynamics 365 predstavlja naziv globalne instance Dynamics 365. To ime obično je naziv globalnog poduzeća.

Entitet Organizacijska jedinica predstavlja grupu ili odjel u globalnom poduzeću. Ta grupa ili odjel ima skup uloga i cjenik troškova za te uloge, a te uloge i cjenik razlikuju se od uloga i cjenika drugih grupa ili odjela u poduzeću.

Kada je instalirana aplikacija PSA, zadana organizacijska jedinica izrađuje se na temelju organizacije. Svi postojeći resursi dodijeljeni su zadanoj organizacijskoj jedinici. Ako se neki novi korisnici ili resursi usluge Active Directory uvoze u Dynamics 365, postupak uvoza korisnika dodjeljuje ih zadanoj organizacijskoj jedinici u sustavu PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Kako se entitet organizacijske jedinice razlikuje od entiteta poslovne jedinice?

U sustavu Dynamics 365, entitet Poslovna jedinica sigurnosni je konstrukt. Povezivanje korisnika s poslovnom jedinicom određuje entitete i zapise entiteta kojima korisnik ima pristup. Također određuje dozvole (Izradi, Čitaj, Piši, Briši, Dodaj, Dodijeli ili Dijeli) koje korisnik ima za te zapise entiteta.

Entitet Organizacijska jedinica predstavlja grupu ili odjel poduzeća koji ima karakteristične stope troškova za zaposlenike koji su mu dodijeljeni. Povezivanje resursa s organizacijskom jedinicom određuje trošak resursa za angažman projekta.

Kada provodite Dynamics 365, optimizirajte odobrenje sigurnosti za hijerarhiju poslovnih jedinica i dodjeljivanje korisnika poslovnim jedinicama. Dodijelite sve korisnike koji obično moraju pristupati istom skupu zapisa istoj poslovnoj jedinici. Organizacijska jedinica nema učinka na odobrenje sigurnosti ili pristup.

#### <a name="example-of-organizational-units-and-business-units"></a>Primjer organizacijskih jedinica i poslovnih jedinica

Contoso, Ltd. ima uspješnu praksu s Microsoftovom tehnologijom. Ivan i Ivana oboje su C\# razvojni programeri, ali Ivana je u Sjedinjenim Američkim Državama, dok je Ivan u Indiji. Većina projektnih angažmana zahtijeva resurse iz Contosa, Indija i Contosa, SAD, a Ivan i Ivana zahtijevaju jednaku razinu sigurnosnog pristupa projektima u ovom području prakse. Međutim, trošak razvojnih programera iz Contosa, Indija značajno se razlikuje od troška razvojnih programera iz Contosa, SAD.

Ovo je optimalan način izrade ovog scenarija s pomoću sustava Dynamics 365 i PSA.

1. Izradite praksu Microsoftove tehnologije kao poslovnu jedinicu i povežite Ivana i Ivanu s njom. Na taj način osiguravate da oba zaposlenika imaju jednaku razinu sigurnosnog pristupa svim projektima u tom području prakse. Oboje će moći provjeriti napredak i prijaviti ažuriranja o vremenu, troškovima i zadacima. 
2. Izradite dvije organizacijske jedinice da biste osigurali da se trošak projekta ispravno prikazuje. 
3. Ivanu povežite s Contosom, SAD, a Ivana povežite s Contosom, Indija.
4. Dodijelite odgovarajuće cjenike troškova objema organizacijskim jedinicama. Na taj način osiguravate da troškovi koji su zapisani na projektu za Ivana i Ivanu ispravno prikazuju razliku u troškovima između Contosa, SAD i Contosa, Indija.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Jesu li organizacijske jedinice povezane s prodajnim teritorijima u sustavu Dynamics 365?

Nema povezivanja ili odnosa između prodajnih teritorija i organizacijskih jedinica. Prodajni teritorij obično je zemljopisno područje u kojem se odvija prodaja. Cjenik prodaje može se povezati sa svakim prodajnim teritorijem.

Organizacijska jedinica interna je grupa ili odjel u poduzeću koje prati troškove za skup uloga koje prodaje drugim odjelima ili vanjskim klijentima.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Primjer organizacijskih jedinica i prodajnih teritorija

Contoso, Ltd. ima dva razvojna centra: Contoso, SAD i Contoso Indija. Troškovi resursa uvelike se razlikuju između tih dvaju razvojnih centara.

Contoso prodaje svoje IT usluge na brojnim međunarodnim tržištima, kao što su Latinska Amerika, Sjeverna Amerika, Azija-Pacific, Zapadna Europa i Bliski istok. Stope naplaćivanja za iste projektne uloge mogu se uvelike razlikovati na tim tržištima.

Contoso, SAD i Contoso, Indija treba postaviti kao organizacijske jedinice, a svaka organizacijska jedinica treba imati vlastiti cjenik troškova. Azija-Pacific, Latinska Amerika, Sjeverna Amerika, Zapadna Europa i Bliski istok trebaju biti postavljeni kao prodajni teritoriji, a svaki prodajni teritorij treba imati vlastiti cjenik prodaje.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Zašto postoji ograničenje za povezivanje cjenika s organizacijskim jedinicama? 

Određivanje cijena prodaje obično je jedinstveno za zemljopisna područja ili tržišta na kojima se usluge prodaju. Interni odjeli poduzeća obično nemaju vlastito određivanje cijena prodaje za istu vrstu usluga. Međutim, interni odjeli imaju različit trošak prodane robe (COGS), ovisno o vještinama osoba koje zapošljavaju i uvjetima rada regije u kojoj posluju. Budući da su organizacijske jedinice modelirane kao interni odjeli poduzeća, mogu imati samo cjenike troškova.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Zašto ne možemo cjenike prodaje povezati s organizacijskim jedinicama?

U sustavu PSA, cjenici prodaje mogu se povezati s klijentima i prodajnim teritorijima. Transakcijski entiteti kao što su Prilika, Ponuda, Ugovor o projektu i Projekt koriste cjenike prodaje koji su priloženi računu klijenta ili prodajnom teritoriju za određivanje stopa naplaćivanja i potencijalnih prihoda na angažmanu projekta.

Cjenici troškova povezani su s organizacijskim jedinicama. Transakcijski entiteti kao što su Prilika, Ponuda, Ugovor o projektu i Projekt koriste cjenike troškova koji su priloženi ugovornoj jedinici za određivanje troškova na angažmanu projekta.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Imaju li organizacijske jedinice hijerarhijski odnos u sustavu PSA?

Ne. U trenutačnom izdanju sustava PSA, organizacijske jedinice nemaju hijerarhijski odnos. To znači da ne možete:

- Konfigurirati uzorak za zadane cijene troškova koji se kreće hijerarhijski. 
- Prijaviti prihode ili troškove koji su zbrojeni na različitim razinama hijerarhije organizacijske jedinice.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Mi smo veliko multinacionalno poduzeće s kompleksnom, višerazinskom hijerarhijom troškovnih centara, odjela i ureda za naplatu. Kako možemo najbolje iskoristiti koncept organizacijske jedinice u ovoj verziji aplikacije Project Service?

Kada imate kompleksnu hijerarhiju troškovnih centara, odjela, ureda za naplatu itd., završne čvorove te hijerarhije postavite kao zasebne organizacijske jedinice.
Sljedeći primjer prikazuje tipičnu hijerarhiju:

**Contoso, Indija**

  - SAP praksa 

    - Tehnički savjetnici 
    - Funkcionalni savjetnici 
    
  - Praksa Microsoftove tehnologije 

    - Tehnički savjetnici
    - Funkcionalni savjetnici 
    
**Contoso, SAD**

 - SAP praksa 

    - Tehnički savjetnici 
    - Funkcionalni savjetnici 
    
 - Praksa Microsoftove tehnologije 

    - Tehnički savjetnici 
    - Funkcionalni savjetnici 
 
Ako je vaša hijerarhija slična, morate je postaviti kao grubi popis, kao što je prikazano ovdje:
- Contoso, Indija - SAP praksa - Tehnički savjetnici 
- Contoso, Indija - SAP praksa - Funkcionalni savjetnici       
- Contoso, Indija - Praksa Microsoftove tehnologije Funkcionalni savjetnici 
- Contoso, Indija - Praksa Microsoftove tehnologije Funkcionalni savjetnici 
- Contoso, SAD - SAP praksa - Tehnički savjetnici  
- Contoso, SAD - SAP praksa - Funkcionalni savjetnici  
- Contoso, SAD - Praksa Microsoftove tehnologije - Tehnički savjetnici 
- Contoso, SAD - Praksa Microsoftove tehnologije - Funkcionalni savjetnici

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Mi smo malo poduzeće za profesionalne usluge koje posluje kao jedan odjel. Kako možemo najbolje koristiti koncept organizacijske jedinice u trenutačnoj verziji sustava PSA?

Ako vaše poduzeće posluje kao jedna jedinica koja ima jedan cjenik troškova, ne morate postavljati nikakve organizacijske jedinice. Tijekom instalacije sustava PSA, Dynamics 365 izrađuje jednu zadanu organizacijsku jedinicu koja ima isti naziv kao i organizacija. Prema zadanim postavkama, svi su korisnici dodijeljeni toj organizacijskoj jedinici. Kad god sustav zahtijeva da se odabere organizacijska jedinica, ova organizacijska jedinica odabire se prema zadanim postavkama.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Kada se projekt izrađuje iz ponude ili retka ugovora o projektu, zadana ugovorna jedinica potječe iz ponude ili ugovora o projektu. Ako je projekt izrađen prije entiteta prodaje poput ponude ili ugovora o projektu, koja je zadana ugovorna jedinica?

Kada se projekt samostalno izrađuje, zadana ugovorna jedinica projekta temelji se na korisniku koji ga izrađuje. Taj korisnik također je zadani upravitelj projekta. Ako je projekt mapiran na entitet prodaje, kao što je ponuda ili ugovor o projektu, ugovorna jedinica na projektu temelji se na entitetu prodaje. U tom slučaju, procjene projekta mogu se ponovno izračunati jer se cjenik troškova koristi za izračun promjena procjene troška ako se ugovorna jedinica promijeni. Cjenik prodaje koristi se za izračun procjena prodaje koje će se promijeniti tako da su usklađene s cjenikom projekta na ponudi.

Polja **Ugovorna jedinica** i **Valuta** na projektu zaključana su za uređivanje jer moraju biti usklađena s vrijednostima na entitetu prodaje (ponuda ili ugovor o projektu) na koji je projekt mapiran.
