---
title: Ponude – Osnovni koncepti
description: U ovoj se temi nalaze informacije o ponudama projekta i ponudama prodaje koje su dostupne u aplikaciji Project Operations.
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b252f6e02d0809c352d3665731ec5e02e4e9a73f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898433"
---
# <a name="quotes---key-concepts"></a>Ponude – Osnovni koncepti

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

U aplikaciji Dynamics 365 Project Operations, postoje dvije vrste ponuda: za projekt i prodaju. Te dvije vrste ponuda razlikuju se na sljedeće načine:

- **Rešetke za stavke retka**: Na ponudi prodaje postoji samo jedna rešetka za stavke retka. Ponuda projekta ima dvije rešetke za stavke redaka. Jedna je rešetka za retke projekta, a druga za retke proizvoda.
- **Aktivacija i revizije**: Ponude prodaje podržavaju aktivaciju i revizije. Ovi procesi nisu podržani u ponudi projekta.
- **Priložene narudžbe**: Ponudi prodaje možete priložiti više narudžbi. Ponudi projekta možete priložiti samo jedan ugovor o projektu.
- **Usvajanje ponude** : Kada osvojite ponudu prodaje, povezana prilika može ostati otvorena. Nakon što se dobije projetna ponuda, povezana prilika je zatvorena.
- **Polja i koncepti**: Ponuda prodaje ne uključuje neka polja i koncepte koji su uključeni u ponudu projekta. Polja uključuju **Ugovornu jedinicu**, **Upravitelja računa** i **Naziv fakture za kontakt**.  
- **Vrsta**: Ponude prodaje i projekta također se identificiraju poljem koje se temelji na skupu mogućnosti,**Vrsta**. Za prodajnu ponudu, ovo polje ima vrijednost **Na temelju artikla**. Za projektnu ponudu, ona ima vrijednost **Na temelju rada**.

U ovoj temi usredotočit ćemo se na pojedinosti o ponudama projekta.

Ponuda projekta u aplikaciji Project Operations može imati stavke s više redaka ili retke ponuda. U stvari, projektna ponuda ima dvije rešetke za stavke redaka. Jedna rešetka je za retke temeljene na projektu koji omogućuju detaljne procjene. Druga rešetka je za retke temeljene na proizvodu koje koriste jednostavnu jediničnu cijenu i pristup temeljen na količini.

- **Na temelju projekta**: Vrijednost ponude određuje se nakon procjene koliko je posla potrebno. Možete procijeniti rad na visokoj razini, izravno kao pojedinosti retka ispod svakog retka ponude ili na temelju procjena najsitnijih pojedinosti, uporabom projekta i plana projekta. Redci ponude koji se temelje na projektu nalaze se samo u ponudama temeljenim na projektu koje su izrađene s pomoću aplikacije Project Operations. Ova vrsta retka ponude prilagođeni je oblik redaka ponude za unos koji su dostupni u Microsoft Dynamics 365 Sales.

- **Na temelju proizvoda**: Vrijednost ponude određuje se na temelju količine prodanih jedinica i prodajne cijene jediničnog proizvoda. Proizvod u retku koji se temelji na proizvodu može doći iz kataloga proizvoda u Prodaji ili može biti proizvod koji definirate. Ova vrsta retka ponude dostupna je i u ponudama temeljenim na projektu koje su izrađene uporabom aplikacije Project Operations.

Iznos na ponudi je ukupan zbroj u recima koji se temelje na proizvodu i recima koji se temelje na projektu.

> [!NOTE]
> Ponude i redci ponude nisu obavezni u aplikaciji Project Operations. Proces projekta možete pokrenuti s ugovorom o projektu (prodan projekt). Međutim, prilika je uvijek potrebna, bez obzira na to jeste li započeli s ponudom ili ugovorom o projektu.

## <a name="project-based-quote-lines"></a>Redci ponude utemeljeni na projektu

Redak ponude koji se temelji na projektu u aplikaciji Project Operations ima sljedeće načine naplate:

- Vrijeme i materijal
- Fiksna cijena

### <a name="time-and-material"></a>Vrijeme i materijal

Način naplate vremena i materijala temelji se na potrošnji. Kada odaberete ovaj način naplate, kupac se fakturira jer projekt snosi troškove. Fakture se izrađuju na periodičnoj frekvenciji koja se temelji na datumu. Tijekom procesa prodaje, navedena vrijednost komponente vremena i materijala daje samo procjenu krajnjeg troška klijentu. Dobavljač se ne obvezuje na dovršetak projekta za točno navedenu vrijednost. Komponente vremena i materijala povećavaju rizik klijenta. Klijenti bi mogli pregovarati o dodatnim klauzulama koje se ne mogu premašiti kako bi smanjio njihov rizik. Project Operations ne podržava postavljanje klauzula koje se ne smije prelaziti.

### <a name="fixed-price"></a>Fiksna cijena

U načinu naplate fiksne cijene, dobavljač se obvezuje na isporuku projekta po fiksnom trošku klijentu. Klijentu se naplaćuje navedena vrijednost retka ponude za fiksnu cijenu, bez obzira na troškove koje dobavljač snosi za isporuku tog retka ponude. Vrijednost retka ponude fiksne cijene naplaćuje se na jedan od sljedećih načina: 

- Kao paušalni iznos na početku ili kraju projekta, ili kada se dosegne ključna točka projekta. 
- Na frekvenciji koja se temelji na datumu jednakih rata fiksne vrijednosti u retku ponude. Ove rate su poznate kao periodične ključne točke.
- U ratama koje imaju monetarnu vrijednost koja je usklađena s napretkom rada ili specifičnim ključnim točkama koje se postižu na projektu. U tom slučaju, vrijednost svake rate može se razlikovati, ali sve moraju biti jednake fiksnoj vrijednosti u retku ponude.

Project Operations podržava sve tri vrste rasporeda faktura za retke ponude s fiksnom cijenom.

## <a name="transaction-classification"></a>Klasifikacija transakcije

Organizacije za profesionalne usluge obično sastavljaju ponude i izdaju fakture svojim klijentima klasifikacijom troškova. Troškovi su predstavljeni sljedećim klasifikacijama transakcija:

- **Vrijeme**: Ova klasifikacija predstavlja trošak rada ili vremena ljudskog resursa na projektu.
- **Trošak**: Ova klasifikacija predstavlja sve druge vrste troškova na projektu. Budući da troškovi mogu biti široko klasificirani, većina organizacija izrađuje podkategorije, kao što su putovanja, iznajmljivanje automobila, hotel ili uredski materijal.
- **Naknada**: Ova klasifikacija predstavlja razne opće troškove, kazne i ostale stavke koji se naplaćuju klijentu. 
- **Porez**: Ova klasifikacija predstavlja iznose poreza koje korisnici dodaju tijekom unosa troškova.
- **Materijalna transakcija**: Ova klasifikacija predstavlja stvarne podatke iz redaka s proizvodima na potvrđenoj fakturi za projekt.
- **Ključna točka**: Ovom se klasifikacijom služi logika naplate fiksne cijene.

Jedna ili više tih klasifikacija transakcije može se pridružiti svakom retku ponude. Nakon što se dobije ponuda, mapiranje između klasifikacije transakcija i retka ponude prenosi se u redak ugovora.
  
Na primjer, ponuda može sadržavati sljedeće dvije retke ponude: 

- Savjetovanje koji koriste način naplate vremena i materijala u kojima se primjenjuju klasifikacije transakcija s vremenom i naknadama. Na primjer, sve transakcije s vremenom i naknadama za primjer **Implementacije AX Dynamics** sustava fakturiraju se klijentu na temelju vremena i materijala koji se koriste. 
- Povezani putni troškovi koji upotrebljavaju način naplate fiksne cijene. Na primjer, svi putni troškovi za primjer **Implementacije AX Dynamics** sustava fakturirani su po fiksnoj monetarnoj vrijednosti.

> [!NOTE]
> Kombinacija projekta i klasifikacija transakcije **Vremena**, **Troška** i **Naknade** koje su pridružene retku ponude ili retku ugovora mora biti jedinstvena. Ako je ista kombinacija razreda projekta i transakcije pridružena više od jednom retku ugovora ili retku ponude, Project Operations neće ispravno funkcionirati.

## <a name="billing-types"></a>Vrste naplate

Polje **Vrsta naplate** definira koncept mogućnosti naplate. To je skup mogućnosti koji ima sljedeće moguće vrijednosti:

- **Naplativo**: Trošak koji se obračunava ovom ulogom/kategorijom izravan je trošak koji pokreće izvršenje projekta, a klijent će platiti za ovaj rad. Plaćanje se može provoditi kao aranžman na temelju vremena i materijala ili kao aranžman fiksne cijene. Međutim, zaposlenik koji provede ovo vrijeme primit će odgovarajuću plaću za svoje naplativo korištenje.
- **Nenaplativo**: Trošak koji se obračunava ovom ulogom/kategorijom smatra se izravnim troškom koji pokreće izvršenje projekta, iako klijent ne uvažava tu činjenicu i neće platiti za taj rad. Zaposlenik koji provodi ovo vrijeme neće biti plaćen za naplativim korištenjem za njega.
- **Besplatno**: Trošak koji se obračunava ovom ulogom/kategorijom smatra se izravnim troškom koji pokreće izvršenje projekta, a klijent uvažava tu činjenicu. Zaposlenik koji provodi ovo vrijeme biti će plaćen za naplativo korištenje za njega. Međutim, taj se trošak ne naplaćuje klijentu.
- **Nije dostupno**: S pomoću ove mogućnosti prate se troškovi nastali na internim projektima koji ne zahtijevaju praćenje prihoda.

## <a name="invoice-schedule"></a>Raspored faktura

Raspored faktura je niz datuma kada se pojavljuje fakturiranje za projekt. Po želji možete stvoriti raspored faktura u retku ponude. Svaki redak ponude može imati vlastiti raspored faktura. Da biste izradili raspored faktura, morate navesti sljedeće vrijednosti atributa:

- Datum početka naplate 
- Datum isporuke koji predstavlja datum završetka naplate na projektu
- Učestalost faktura

Te tri vrijednosti atributa upotrebljavaju se za generiranje privremenog skupa datuma za uspostavljanje fakturiranja.

## <a name="invoice-frequency"></a>Učestalost faktura

Učestalost fakture je entitet koji pohranjuje vrijednosti atributa koje pomažu izraziti učestalost izrade fakture. Sljedeći atributi izražavaju ili definiraju entitet Učestalost fakture:

- **Razdoblje**: Podržavaju se mjesečna, dvotjedna i tjedna razdoblja. 
- **Izvršavanje po razdoblju**: Za tjedna i dvotjedna razdoblja, možete definirati samo jedno izvršavanje po razdoblju. Za mjesečna razdoblja, možete definirati između jednog i četiri izvođenja po razdoblju. 
- **Dani izvršavanja**: Dani kada bi trebalo izvršiti fakturiranje. Ovaj atribut možete konfigurirati na dva načina:
  - **Radni dani** – Na primjer, možete odrediti da se fakturiranje izvršava svakog ponedjeljka ili svakog drugog ponedjeljka. Klijenti koji moraju postaviti fakturiranje za izvođenje na radni dan možda preferiraju ovu vrstu konfiguracije. 
  - **Kalendarski dani**: Na primjer, možete odrediti da se fakturiranje izvršava sedmog i dvadesetprvog dana svakog mjeseca. Neke tvrtke možda preferiraju ovu vrstu konfiguracije jer pomaže jamčiti da se fakturiranje izvodi prema fiksnom rasporedu svaki mjesec.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Raspored faktura za redak ponude fiksne cijene

Za redak ponude fiksne cijene možete koristiti rešetku **Raspored faktura** da biste izradili ključne točke za naplatu koje su jednake vrijednosti retka ponude.

- Da biste izradili ključne točke za naplatu koje su podjednako podijeljene, odaberite učestalost fakture, unesite početni datum naplate u redak ponude i odaberite **Traženi datum dovršetka** za ponudu u odjeljku **Sažetak** u zaglavlju ponude. Zatim odaberite **Generiraj periodične ključne točke** za izradu podjednako podijeljenih ključnih točaka na temelju odabrane frekvencije fakture. 
- Da biste izradili ključnu točku naplate u paušalnom iznosu, izradite ključnu točku, a zatim unesite vrijednost retka ponude kao iznos ključne točke.
- Da biste izradili ključne točke za naplatu koje se temelje na određenim zadacima u planu projekta, izradite ključnu točku i mapirajte ju u element rasporeda projekta u korisničkom sučelju ključne točke za naplatu.
