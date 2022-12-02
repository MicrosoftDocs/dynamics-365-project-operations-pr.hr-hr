---
title: Ponude i reci ponude
description: U ovom se članku navode informacije o ponudama i redcima ponude.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 4c59f018adc7ee439fd77a819e2fb7620941e958
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933345"
---
# <a name="quotes-and-quote-lines"></a>Ponude i reci ponude

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

U Dynamics 365 Project Service Automation, postoje dvije vrste ponuda: projektne ponude i prodajne ponude. Dvije vrste razlikuju se na sljedeće načine:

- Na prodajnoj ponudi postoji samo jedna rešetka za stavke retka. Na projektnoj ponudi postoje dvije rešetke za stavke retka: jedna za projektne retke i jedna za linije proizvoda.
- Prodajna ponuda podržava aktivaciju i revizije. Projektna ponuda ne podržava te procese.
- Prodajnoj ponudi možete priložiti više naloga. Projektnoj ponudi možete priložiti samo jedan ugovor o projektu.
- Možete osvojiti prodajnu ponudu i zadržati povezanu priliku otvorenom. Nakon što se dobije projetna ponuda, povezana prilika je zatvorena.
- Prodajna ponuda ne uključuje neka polja i koncepte koji su uključeni u polja projektne ponude. Polja uključuju **Ugovornu jedinicu**, **Upravitelja računa** i **Naziv fakture za kontakt**.  
- Prodajne ponude i projektne ponude također se identificiraju poljem koje se temelji na skupu mogućnosti pod nazivom **Vrsta**. Za prodajnu ponudu, ovo polje ima vrijednost **Na temelju artikla**. Za projektnu ponudu, ona ima vrijednost **Na temelju rada**.

Ovaj članak usredotočit će se na pojedinosti o projektnim ponudama.

Projektna ponuda u PSA može imati stavke s više redaka ili redaka ponude. U stvari, projektna ponuda ima dvije rešetke za stavke redaka. Jedna rešetka je za retke temeljene na projektu koji omogućuju detaljne procjene. Druga rešetka je za retke temeljene na proizvodu koje koriste jednostavnu jediničnu cijenu i pristup temeljen na količini.

- **Na temelju projekta** – Iznos (navedena vrijednost) određuje se nakon procjene koliko je posla potrebno. Možete procijeniti rad na visokoj razini ili ga možete procijeniti izravno kao pojedinosti retka ispod svakog retka ponude. Naposljetku, možete procijeniti rad na temelju procjena odozdo prema gore s pomoću plana projekta i projekta. Reci ponude koji se temelje na projektu nalaze se samo u ponudama temeljenim na projektu koje su izrađene s pomoću Project Service Automation. Ova vrsta retka ponude prilagođeni je oblik redaka ponude za unos koji su dostupni u Microsoft Dynamics 365 Sales.
- **Na temelju proizvoda** – Iznos (navedena vrijednost) određuje se na temelju količine prodanih jedinica i prodajne cijene jediničnog proizvoda. Proizvod u retku koji se temelji na proizvodu može doći iz kataloga proizvoda u Prodaji ili može biti proizvod koji definirate. Ova vrsta retka ponude dostupna je i u ponudama temeljenim na projektu koje su izrađene korištenjem PSA.

Iznos na ponudi je ukupan zbroj u recima koji se temelje na proizvodu i recima koji se temelje na projektu.

> [!NOTE]
> Ponude i reci ponude nisu obavezni u PSA. Proces projekta možete pokrenuti s ugovorom o projektu (prodan projekt). Međutim, prilika je uvijek potrebna, bez obzira na to jeste li započeli s ponudom ili ugovorom o projektu.

## <a name="project-based-quote-lines"></a>Rdeci ponude na temelju projekta

Redak ponude koji se temelji na projektu u PSA ima sljedeće načine naplate:

- Vrijeme i materijal
- Fiksna cijena

### <a name="time-and-material"></a>Vrijeme i materijal

Način naplate vremena i materijala temelji se na potrošnji. Kada odaberete ovaj način naplate, klijent se fakturira jer projekt snosi troškove. Fakture se izrađuju na periodičnoj frekvenciji koja se temelji na datumu. Tijekom procesa prodaje, navedena vrijednost komponente vremena i materijala daje samo procjenu krajnjeg troška klijentu. Dobavljač se ne obvezuje na dovršetak projekta za točno navedenu vrijednost. Komponente vremena i materijala povećavaju rizik klijenta. Klijenti bi mogli pregovarati o dodatnim klauzulama koje se ne mogu premašiti kako bi smanjio njihov rizik. PSA ne podržava postavljanje klauzula koje se ne smije prelaziti.

### <a name="fixed-price"></a>Fiksna cijena

U načinu naplate fiksne cijene, dobavljač se obvezuje na isporuku projekta po fiksnom trošku klijentu. Klijentu se naplaćuje navedena vrijednost retka ponude za fiksnu cijenu, bez obzira na troškove koje dobavljač snosi za isporuku tog retka ponude. Vrijednost retka ponude fiksne cijene naplaćuje se na jedan od sljedećih načina: 

- Kao paušalni iznos na početku ili kraju projekta, ili kada se dosegne ključna točka projekta. 
- Na frekvenciji koja se temelji na datumu jednakih rata fiksne vrijednosti u retku ponude. Ove rate su poznate kao periodične ključne točke.
- U ratama koje imaju monetarnu vrijednost koja je usklađena s napretkom rada ili specifičnim ključnim točkama koje se postižu na projektu. U tom slučaju, vrijednost svake rate može se razlikovati, ali sve moraju biti jednake fiksnoj vrijednosti u retku ponude.

PSA podržava sve tri vrste rasporeda faktura za retke fiksne cijene.

## <a name="transaction-classification"></a>Klasifikacija transakcije

Organizacije za profesionalne usluge obično sastavljaju ponude i izdaju fakture svojim klijentima klasifikacijom troškova. U PSA, troškovi su predstavljaju sljedećim klasifikacijama transakcija:

- **Vrijeme** – Ova klasifikacija predstavlja trošak rada ili vremena ljudskog resursa na projektu.
- **Trošak**: – Ova klasifikacija predstavlja sve druge vrste troškova na projektu. Budući da troškovi mogu biti široko klasificirani, većina organizacija izrađuje podkategorije, kao što su putovanja, iznajmljivanje automobila, hotel ili uredski materijal.
- **Naknada** – Ova klasifikacija predstavlja razne troškove, kazne i ostale stavke koji se naplaćuju klijentu. 
- **Porez** – Ova klasifikacija predstavlja iznose poreza koje korisnici dodaju dok unose troškove.
- **Materijalna transakcija** – Ova klasifikacija predstavlja stvarne podatke linija proizvoda na potvrđenoj fakturi projekta.
- **Ključna točka** – Ovom se klasifikacijom služi logika naplate fiksne cijene u PSA.

Jedna ili više tih klasifikacija transakcije može se pridružiti svakom retku ponude. Nakon što se dobije ponuda, mapiranje između klasifikacije transakcija i retka ponude prenosi se u redak ugovora.
 
> ![Snimka zaslona mapiranja vrsta transakcije u retke ponude i ugovora.](media/basic-guide-5.png)
  
Na primjer, ponuda može sadržavati sljedeće dvije retke ponude: 
- Savjetovanje koji koriste način naplate vremena i materijala u kojima se primjenjuju klasifikacije transakcija s vremenom i naknadama. Na primjer, sve transakcije s vremenom i naknadama za primjer **Implementacije AX Dynamics** sustava fakturiraju se klijentu na temelju vremena i materijala koji se koriste. 
- Povezani putni troškovi koji upotrebljavaju način naplate fiksne cijene. Na primjer, svi putni troškovi za primjer **Implementacije AX Dynamics** sustava fakturirani su po fiksnoj monetarnoj vrijednosti.

> [!NOTE]
> Kombinacija projekta i klasifikacija transakcije **Vremena**, **Troška** i **Naknade** koje su pridružene retku ponude ili retku ugovora mora biti jedinstvena. Ako je ista kombinacija razreda projekta i transakcije pridružena više od jednom retka ugovora ili retka ponude, PSA neće ispravno funkcionirati.

## <a name="billing-types"></a>Vrste naplate

Polje **Vrsta naplate** definira koncept mogućnosti naplaćivanja u PSA. To je skup mogućnosti koji ima sljedeće moguće vrijednosti:

- **Naplativo** – Trošak koji se obračunava ovom ulogom/kategorijom izravan je trošak koji pokreće izvršenje projekta, a klijent će platiti za ovaj rad. Plaćanje se može provoditi kao aranžman na temelju vremena i materijala ili kao aranžman fiksne cijene. Međutim, zaposlenik koji provede ovo vrijeme primit će odgovarajuću plaću za svoje naplativo korištenje.
- **Nneaplativo** – Trošak koji se obračunava ovom ulogom/kategorijom smatra se izravnim troškom koji pokreće izvršenje projekta, iako klijent ne uvažava tu činjenicu i neće platiti za taj rad. Zaposlenik koji provodi ovo vrijeme neće biti plaćen za naplativim korištenjem za njega.
- **Besplatno** – Trošak koji se obračunava ovom ulogom/kategorijom smatra se izravnim troškom koji pokreće izvršenje projekta, a klijent uvažava tu činjenicu. Zaposlenik koji provodi ovo vrijeme biti će plaćen za naplativo korištenje za njega. Međutim, taj se trošak ne naplaćuje klijentu.
- **Nije dostupno** – Troškovi nastali na unutarnjim projektima koji ne zahtijevaju praćenje prihoda prate se s pomoću ove mogućnosti.

## <a name="invoice-schedule"></a>Raspored faktura

Raspored faktura je niz datuma kada se pojavljuje fakturiranje za projekt. Po želji možete izraditi raspored faktura u retku ponude u PSA. Svaki redak ponude može imati vlastiti raspored faktura. Da biste izradili raspored faktura, morate navesti sljedeće vrijednosti atributa:

- Datum početka naplate 
- Datum isporuke koji predstavlja datum završetka naplate na projektu
- Učestalost faktura

PSA koristi te tri vrijednosti atributa da bi generirao određeni skup datuma za uspostavljanje fakturiranja.

## <a name="invoice-frequency"></a>Učestalost faktura

Učestalost fakture je entitet koji pohranjuje vrijednosti atributa koje pomažu izraziti učestalost izrade fakture. Sljedeći atributi izražavaju ili definiraju entitet Učestalost fakture:

- **Razdoblje** - podržavaju se mjesečna, dvotjedna i tjedna razdoblja. 
- **Izvođenja po razdoblju** -za tjedna i dvotjedna razdoblja, možete definirati samo jedno izvođenje po razdoblju. Za mjesečna razdoblja, možete definirati između jednog i četiri izvođenja po razdoblju. 
- **Dani izvođenja** – Dani kada je potrebno izvesti fakturiranje. Ovaj atribut možete konfigurirati na dva načina:
  - **Radnim danom** - Na primjer, možete odrediti da se fakturiranje izvodi svakog ponedjeljka ili svakog drugog ponedjeljka. Klijenti koji moraju postaviti fakturiranje za izvođenje na radni dan možda preferiraju ovu vrstu konfiguracije. 
  - **Kalendarski dani** -Na primjer, možete odrediti da se fakturiranje izvodi sedmog i dvadesetprvog dana svakog mjeseca. Neke tvrtke možda preferiraju ovu vrstu konfiguracije jer pomaže jamčiti da se fakturiranje izvodi prema fiksnom rasporedu svaki mjesec.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Raspored faktura za redak ponude fiksne cijene

Za redak ponude fiksne cijene možete koristiti rešetku **Raspored faktura** da biste izradili ključne točke za naplatu koje su jednake vrijednosti retka ponude.

- Da biste izradili ključne točke za naplatu koje su podjednako podijeljene, odaberite učestalost fakture, unesite početni datum naplate u redak ponude i odaberite **Traženi datum dovršetka** za ponudu u odjeljku **Sažetak** u zaglavlju ponude. Zatim odaberite **Generiraj periodične ključne točke** za izradu podjednako podijeljenih ključnih točaka na temelju odabrane frekvencije fakture. 
- Da biste izradili ključnu točku naplate u paušalnom iznosu, izradite ključnu točku, a zatim unesite vrijednost retka ponude kao iznos ključne točke.
- Da biste izradili ključne točke za naplatu koje se temelje na određenim zadacima u planu projekta, izradite ključnu točku i mapirajte ju u element rasporeda projekta u korisničkom sučelju ključne točke za naplatu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
