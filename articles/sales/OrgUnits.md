---
title: Organizacijske jedinice
description: U ovom članku je opisan koncept organizacijskih jedinica i objašnjeno kako stvoriti i održavati organizacijske jedinice u aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921615"
---
# <a name="organizational-units-overview"></a>Pregled organizacijskih jedinica

U aplikaciji Microsoft Dynamics 365 Project Operations, *organizacijska jedinica* je zasebna grupa ili odjel u poduzeću za profesionalne usluge koja zapošljava naplative resurse koji imaju stope cijena.

Za poduzeća za profesionalne usluge koja zapošljavaju tehničke resurse u različitim područjima prakse ili poslovnim linijama, trošak popunjavanja uloge može se razlikovati ovisno o području prakse ili poslovne linije u kojoj se uloga popunjava. U ovom scenariju, koncept organizacijskih jedinica pomaže pružajući način za grupiranje skupa naplativih uloga u odjelu poduzeća koje ima različitu strukturu troškova za te uloge.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Koncept organizacijskih jedinica u aplikaciji Project Operations

U aplikaciji Project Operations, organizacijska jedinica ima određenu valutu i određeni cjenik koštanja.

Valuta organizacijske jedinice primarna je valuta koja se koristi za praćenje troškova.

Jedan ili više cjenika troškova može se priložiti svakoj organizacijskoj jedinici. Project Operations stavlja sljedeća ograničenja na cjenike koji se mogu priložiti organizacijskoj jedinici:

- Cjenici moraju biti u valuti organizacijske jedinice.
- Cjenici moraju biti cjenici koštanja.

Osim toga, entitet Resurs uključuje atribut za organizacijsku jedinicu. Svaki je resurs moguće dodijeliti jednoj organizacijskoj jedinici.

### <a name="roles-of-organizational-units"></a>Uloge organizacijskih jedinica

Organizacijska jedinica igra dvije uloge u aplikaciji Project Operations:

- **Ugovorna jedinica** – Organizacijska jedinica koja predstavlja grupu ili odjel poduzeća koja je prvenstveno odgovorna za ostvarivanje prodaje i upravljanje isporukom rada i usluga klijentu. Ugovorna jedinica identificira se poljem **Ugovorna jedinica** u odjeljku zaglavlja stranica **Prilika**, **Ponuda**, **Ugovor o projektu** i **Projekt**.
- **Jedinica resursa** – Organizacijska jedinica kojoj resurs pripada ili je dodijeljen. Ova organizacijska jedinica može osigurati svoje resurse za neke uloge na izjavama o radu (svo) i projektima koji su u vlasništvu ugovorne jedinice.

![Ugovorne jedinice i jedinice resursa.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Najčešća pitanja o organizacijskoj jedinici

Ovdje ćete pronaći često postavljena pitanja o organizacijskim jedinicama.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Kako je entitet Organizacijska jedinica u aplikaciji Project Operations povezan s entitetom Organizacija koji već postoji u sustavu Dynamics 365?

Entitet Organizacija u sustavu Dynamics 365 predstavlja naziv globalne instance Dynamics 365. To ime obično je naziv globalnog poduzeća.

Entitet Organizacijska jedinica predstavlja grupu ili odjel u globalnom poduzeću. Ta grupa ili odjel ima skup uloga i cjenik troškova za te uloge, a te uloge i cjenik razlikuju se od uloga i cjenika drugih grupa ili odjela u poduzeću.

Kada je instalirana aplikacija Project Operations, zadana organizacijska jedinica izrađuje se na temelju organizacije. Svi postojeći resursi dodijeljeni su zadanoj organizacijskoj jedinici. Ako se neki novi korisnici ili resursi usluge Active Directory uvoze u Dynamics 365, postupak uvoza korisnika dodjeljuje ih zadanoj organizacijskoj jedinici u aplikaciji Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Kako se entitet Organizacijska jedinica razlikuje od entiteta Poslovna jedinica?

U sustavu Dynamics 365, entitet Poslovna jedinica sigurnosni je konstrukt. Povezivanje korisnika s poslovnom jedinicom određuje entitete i zapise entiteta kojima korisnik ima pristup. Također određuje dozvole (Izradi, Čitaj, Piši, Briši, Dodaj, Dodijeli ili Dijeli) koje korisnik ima za te zapise entiteta.

Entitet Organizacijska jedinica predstavlja grupu ili odjel poduzeća koji ima karakteristične stope troškova za zaposlenike koji su mu dodijeljeni. Povezivanje resursa s organizacijskom jedinicom određuje trošak resursa za angažman projekta.

Kada provodite Dynamics 365, optimizirajte odobrenje sigurnosti za hijerarhiju poslovnih jedinica i dodjeljivanje korisnika poslovnim jedinicama. Dodijelite sve korisnike koji obično moraju pristupati istom skupu zapisa istoj poslovnoj jedinici. Organizacijska jedinica nema učinka na odobrenje sigurnosti ili pristup.

**Primjer koji pokazuje jednu potencijalnu razliku u modeliranju organizacijskih jedinica i poslovnih jedinica**

Contoso, Ltd. ima uspješnu praksu s Microsoftovom tehnologijom. Ivan i Ivana oboje su C\# razvojni programeri, ali Ivana je u Sjedinjenim Američkim Državama, dok je Ivan u Indiji. Većina projektnih angažmana zahtijeva resurse i iz tvrtke Contoso, Indija i iz tvrtke Contoso, SAD, a Ivan i Ivana zahtijevaju jednaku razinu sigurnosnog pristupa projektima u ovom području prakse. Međutim, trošak razvojnih programera iz Contosa, Indija značajno se razlikuje od troška razvojnih programera iz Contosa, SAD.

Ovo je optimalan način izrade ovog scenarija s pomoću sustava Dynamics 365 i aplikacije Project Operations.

1. Izradite praksu Microsoftove tehnologije kao poslovnu jedinicu i povežite Ivana i Ivanu s njom. Na taj način pomažete osigurati da oba zaposlenika imaju jednaku razinu sigurnosnog pristupa svim projektima u tom području prakse. Oboje će moći provjeriti napredak i prijaviti ažuriranja o vremenu, troškovima, iskorištenosti materijala i zadacima.
2. Izradite dvije organizacijske jedinice da biste pomogli osigurati da se cijena projekta ispravno prikazuje.
3. Ivanu povežite s tvrtkom Contoso, SAD, a Ivana povežite s tvrtkom Contoso, Indija.
4. Dodijelite odgovarajuće cjenike troškova objema organizacijskim jedinicama. Na taj način pomažete osigurati da troškovi koji su zabilježene na projektu za Ivana i Ivanu ispravno prikazuju razliku u troškovima između tvrtke Contoso, SAD i tvrtke Contoso, Indija.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Jesu li organizacijske jedinice povezane s prodajnim teritorijima u sustavu Dynamics 365?

Nema povezivanja ili odnosa između prodajnih teritorija i organizacijskih jedinica. Prodajni teritorij obično je zemljopisno područje u kojem se odvija prodaja. Cjenik prodaje može se povezati sa svakim prodajnim teritorijem.

Organizacijska jedinica interna je grupa ili odjel u poduzeću koje prati troškove za skup uloga koje prodaje drugim odjelima ili vanjskim klijentima.

**Primjer koji pokazuje jednu potencijalnu razliku u modeliranju organizacijskih jedinica i prodajnih područja**

Contoso, Ltd. ima dva razvojna centra: Contoso, SAD i Contoso Indija. Troškovi resursa uvelike se razlikuju između tih dvaju razvojnih centara. Contoso prodaje svoje usluge informacijske tehnologije (IT) na brojnim međunarodnim tržištima, kao što su Latinska Amerika, Sjeverna Amerika, Pacifička Azija, Zapadna Europa i Bliski istok. Stope naplaćivanja za iste projektne uloge mogu se uvelike razlikovati na tim tržištima. Contoso, SAD i Contoso, Indija treba postaviti kao organizacijske jedinice, a svaka organizacijska jedinica treba imati vlastiti cjenik troškova. Azija-Pacific, Latinska Amerika, Sjeverna Amerika, Zapadna Europa i Bliski istok trebaju biti postavljeni kao prodajni teritoriji, a svaki prodajni teritorij treba imati vlastiti cjenik prodaje.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Zašto postoji ograničenje za povezivanje cjenika s organizacijskim jedinicama?

Određivanje cijena prodaje obično je jedinstveno za zemljopisna područja ili tržišta na kojima se usluge prodaju. Interni odjeli poduzeća obično nemaju vlastito određivanje cijena prodaje za istu vrstu usluga. Međutim, interni odjeli imaju različit trošak prodane robe (COGS), ovisno o vještinama osoba koje zapošljavaju i uvjetima rada regije u kojoj posluju. Budući da su organizacijske jedinice modelirane kao interni odjeli poduzeća, mogu imati samo cjenike troškova.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Zašto ne možemo cjenike prodaje povezati s organizacijskim jedinicama?

U aplikaciji Project Operations, cjenici prodaje mogu se povezati s klijentima i prodajnim područjima. Transakcijski entiteti kao što su Prilika, Ponuda, Ugovor o projektu i Projekt koriste cjenike prodaje koji su priloženi računu klijenta ili prodajnom području za određivanje stopa naplaćivanja i potencijalnih prihoda za angažman projekta.

Cjenici troškova povezani su s organizacijskim jedinicama. Transakcijski entiteti kao što su Prilika, Ponuda, Ugovor o projektu i Projekt koriste cjenike koštanja koji su priloženi ugovornoj jedinici za određivanje cijena na angažmanu projekta.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Imaju li organizacijske jedinice hijerarhijski odnos u aplikaciji Project Operations?

Ne. U trenutačnom izdanju aplikacije Project Operations, organizacijske jedinice nemaju hijerarhijski odnos. Stoga ne možete izvesti sljedeće zadatke:

- Konfigurirati uzorak za unos zadanih cijena koštanja koji se kreće hijerarhijski.
- Prijaviti prihode ili troškove koji su zbrojeni na različitim razinama hijerarhije organizacijske jedinice.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Mi smo veliko multinacionalno poduzeće koje ima kompleksnu, višerazinsku hijerarhiju cjenovnih centara, odjela i ureda za naplatu. Kako možemo najbolje koristiti koncept organizacijskih jedinica u trenutačnoj verziji aplikacije Project Operations?

Kada imate kompleksnu hijerarhiju cjenovnih centara, odjela, ureda za naplatu itd., lisne čvorove te hijerarhije postavite kao zasebne organizacijske jedinice.

Sljedeći primjer prikazuje tipičnu hijerarhiju.

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

Ako je vaša hijerarhija slična ovom primjeru, morate je postaviti kao grubi popis, kao što je prikazano ovdje:

- Contoso, Indija - SAP praksa - Tehnički savjetnici
- Contoso, Indija - SAP praksa - Funkcionalni savjetnici
- Contoso, Indija - Praksa Microsoftove tehnologije Funkcionalni savjetnici
- Contoso, Indija - Praksa Microsoftove tehnologije Funkcionalni savjetnici
- Contoso, SAD - SAP praksa - Tehnički savjetnici
- Contoso, SAD - SAP praksa - Funkcionalni savjetnici
- Contoso, SAD - Praksa Microsoftove tehnologije - Tehnički savjetnici
- Contoso, SAD - Praksa Microsoftove tehnologije - Funkcionalni savjetnici

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Mi smo malo poduzeće za profesionalne usluge koje posluje kao jedan odjel. Kako možemo najbolje koristiti koncept organizacijskih jedinica u trenutačnoj verziji aplikacije Project Operations?

Ako vaše poduzeće posluje kao jedna jedinica koja ima jedan cjenik troškova, ne morate postavljati nikakve organizacijske jedinice. Instalacijom aplikacije Project Operations izrađuje se jedna zadana organizacijska jedinica koja ima isti naziv kao i organizacija. Prema zadanim postavkama, svi su korisnici dodijeljeni toj organizacijskoj jedinici. Kad god sustav zahtijeva da se odabere organizacijska jedinica, ova organizacijska jedinica odabire se prema zadanim postavkama.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Kada se projekt izrađuje iz ponude ili retka ugovora o projektu, zadana ugovorna jedinica potječe iz ponude ili ugovora o projektu. Što je zadana ugovorna jedinica ako je projekt izrađen prije entiteta prodaje kao što je Ponuda ili Ugovor o projektu?

Kada se projekt samostalno izrađuje, zadana ugovorna jedinica projekta temelji se na korisniku koji ga izrađuje. Taj korisnik također je zadani upravitelj projekta. Ako je projekt mapiran na entitet prodaje, kao što je ponuda ili ugovor o projektu, ugovorna jedinica projekta temelji se na entitetu prodaje. U tom slučaju, procjene projekta mogu se ponovno izračunati jer se cjenik troškova koristi za izračun promjena procjene troška ako se ugovorna jedinica promijeni. Cjenik prodaje koristi se za izračun procjena prodaje koje će se promijeniti tako da su usklađene s cjenikom projekta za ponudu.

Polja **Ugovorna jedinica** i **Valuta** za projekt zaključana su za uređivanje jer moraju biti usklađena s vrijednostima entiteta prodaje (ponuda ili ugovor o projektu) na koji je projekt mapiran.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Stvaranje i održavanje organizacijskih jedinica u aplikaciji Project Operations

Slijedite ove korake za stvaranje organizacijske jedinice u aplikaciji Project Operations.

1. Idite u **Postavke \> Organizacijske jedinice**.
2. Odaberite **Novo**.
3. U području **Općenito**, u polju **Naziv**, unesite naziv organizacijske jedinice. Zatim postavite ostala polja prema potrebi.
4. Odaberite **Spremanje** za stvaranje zapisa kako biste ga mogli nastaviti uređivati.
5. U odjeljku **Cjenici koštanja** odaberite znak plus (**+**) da biste dodali cjenik. Ovdje možete dodati samo cjenike s kontekstom **Cijena**.
6. U polju **Naziv** odaberite gumb **Pretraži** i odaberite cjenik koji želite učiniti dostupnim organizacijskoj jedinici. Nastavite s dodavanjem cjenika prema potrebi.
7. Kada završite dodavanje cjenika, u donjem desnom kutu stranice odaberite **Spremi**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
