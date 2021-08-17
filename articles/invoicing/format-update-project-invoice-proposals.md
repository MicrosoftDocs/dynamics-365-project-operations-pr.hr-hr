---
title: Upravljanje prijedlozima faktura za projekt
description: U ovoj temi nalaze se pojedinosti o izradi faktura za klijenta s pomoću aplikacije Project Operations za scenarije temeljene na resursima / bez zaliha.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 61b43e05eb179e2b00189076290433dd72f89a6bc7ef72140fc1efd752149d43
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989902"
---
# <a name="manage-project-invoice-proposals"></a>Upravljanje prijedlozima faktura za projekt

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Prijedloge faktura za projekt može izraditi vaš odjel za naplatu kada su zadovoljena sljedeća dva uvjeta:

  - Voditelj projekta potvrđuje predračun na platformi Microsoft Dataverse.
  - Sve nenaplaćene prodajne transakcije za vrijeme i materijal koje su uključene u predračun knjiže se s pomoću dnevnika sustava Dynamics 365 **Integracija aplikacije Project Operations**.

Slijedite sljedeće korake za dovršetak prijedloga fakture za projekt u aplikaciji Dynamics 365 Finance.

1. Pregledajte podatke o naplati za transakcije vremena i materijala i proknjižite u dnevnik **Integracija aplikacije Project Operations**.
2. Pregledajte podatke o naplati za kontrolne točke koje imaju fiksnu cijenu naplate.
3. Pregledajte i oblikujte prijedlog faktura za projekt.
4. Proknjižite i ispišite fakture za projekt.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Upravljanje podacima o naplati u dnevniku integracije aplikacije Project Operations

Stvarni podaci o projektu izrađeni na platformi Dataverse pregledava i objavljuje u aplikaciji Financije računovođa projekta. Dodatne informacije o radu s dnevnikom integracije potražite u odjeljku [Dnevnik integracije u aplikaciji Project Operations](../project-accounting/project-operations-integration-journal.md).

Stvarni podaci o cijenama i nefakturiranoj prodaji dodaju se u dnevnik integracije kao zasebni redci:

  - Jedinična cijena koštanja i iznos troškova u stvarnim podacima o trošku zadani su iz transakcije stvarnih troškova na platformi Dataverse.
  - Jedinična prodajna cijena i iznos prodaje u nenaplaćenoj prodajnoj transakciji zadani su od stvarne nenaplaćene prodajne transakcije u projektu na platformi Dataverse.

### <a name="billing-sales-tax"></a>Naplata poreza na promet

Izračun poreza na promet za naplatu određuje kombinacija polja **Grupa za naplatu poreza na promet** i **Grupa za naplatu poreza na promet stavke** na zapisu o nenaplaćenoj prodaji u retku dnevnika **Integracija aplikacije Project Operations**. Sustav zadaje vrijednosti ovih polja na temelju postavki na kartici **Financije** na stranici **Upravljanje projektom i računovodstveni parametri**.

- **Metoda grupe poreza na promet** određuje zadanu logiku grupe poreza na promet za naplatu:
  
  - **Projekt**: Uvijek će zadati grupu poreza na promet za naplatu iz projekta. Možete pregledati ili promijeniti zadanu grupu poreza na promet za naplatu na projektu odabirom mogućnosti **Prikaži zadano računovodstvo** na stranici **Svi projekti**.
  - **Ugovor o projektu**: Uvijek će zadati grupu poreza na promet za naplatu iz ugovora o projektu. Možete pregledati ili promijeniti zadanu grupu poreza na promet u ugovoru o projektu odabirom mogućnosti **Prikaži zadano računovodstvo** na stranici **Ugovori o projektu**.
  - **Klijent**: Uvijek će zadati grupu poreza na promet za naplatu iz klijenta.
  - **Pretraži**: Pretražit će sve gore navedene entitete i odabrati prvu dostupnu vrijednost. Pretraživanje započinje s entitetom **Projekt**, zatim entitetom **Ugovor o projektu** i završava entitetom **Klijent**.

- **Metoda grupe poreza na promet stavke** određuje zadanu logiku grupe poreza na promet za naplatu stavke:
  
  - Za vrste transakcija s vremenom, troškovima i naknadama, grupa poreza na promet za naplatu stavke uvijek će se zadati iz entiteta **Kategorija projekta**.
  - Za vrste materijalnih transakcija, grupa poreza na promet za naplatu stavke zadana je na temelju postavke **Metoda grupe poreza na promet stavke** u stavki **Upravljanje projektom i računovodstveni parametri**. Broj stavke zadaje grupu poreza na promet stavke iz entiteta **Objavljeni proizvod**. Kategorija zadaje grupu poreza na promet stavke iz entiteta **Kategorija projekta**.

### <a name="financial-dimensions"></a>Financijske dimenzije

Financijske veličine za zapise o nenaplaćenoj prodaji u dnevniku **Integracija aplikacije Project Operations** zadane su iz entiteta **Projekt**. Financijske veličine mogu se pregledati i prilagoditi odabirom mogućnosti **Raspodijeli iznose**. Ako trebate promijeniti financijske veličine zapisa nefakturirane prodaje nakon knjiženja dnevnika integracije, ali prije potvrde predračuna, idite na **Svi projekti** > **Upravljaj** > **Proknjižene transakcije**, odaberite transakciju, a zatim odaberite **Postupak** > **Prilagodi računovodstvo**.

### <a name="exchange-rates"></a>Tečajevi

Valuta nenaplaćene transakcije na platformi Dataverse upotrebljava se kao valuta transakcije u aplikaciji Financije i pretvara u računovodstvenu valutu tvrtke s pomoću tečajeva određenih u aplikaciji Financije.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Upravljanje financijskim atributima kontrolnih točaka naplate 

Fakturiraju se redci ugovora o projektu koji upotrebljavaju metodu naplate s fiksnom cijenom [Kontrolne točke s fiksnom cijenom](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Računovođa projekta može pregledati kontrolne točke za naplatu u aplikaciji Financije tako što će otići na **Upravljanje projektima i računovodstvo** > **Svi projekti** > **Upravljaj** > **Transakcije djelomičnog plaćanja**.

### <a name="billing-sales-tax"></a>Naplata poreza na promet

Vrijednosti **Grupa poreza na promet** i **Grupa poreza na promet stavke** zadane su iz postavki kada se stvori nova kontrolna točka naplate na platformi Dataverse. Sustav zadaje vrijednosti ovih polja na temelju postavki na kartici **Financije** na stranici **Upravljanje projektom i računovodstveni parametri**.

- **Metoda grupe poreza na promet** određuje zadanu logiku **Grupe poreza na promet za naplatu**:

    - **Projekt**: Uvijek će zadati grupu poreza na promet za naplatu iz projekta. Možete pregledati ili promijeniti zadanu grupu poreza na promet na projektu odabirom mogućnosti **Prikaži zadano računovodstvo** na stranici **Svi projekti**.
    - **Ugovor o projektu**: Uvijek će zadati grupu poreza na promet za naplatu iz ugovora o projektu. Možete pregledati ili promijeniti zadanu grupu poreza na promet u ugovoru o projektu odabirom mogućnosti **Prikaži zadano računovodstvo** na stranici **Ugovori o projektu**.
    - **Klijent**: Uvijek će zadati grupu poreza na promet za naplatu iz klijenta.
    - **Pretraži**: Pretražit će sve entitete navedene u tom popisu i odabrati prvu dostupnu vrijednost. Pretraživanje započinje s entitetom **Projekt**, zatim entitetom **Ugovor o projektu** i zatim entitetom **Klijent**.

- **Grupa poreza na promet stavki s nepromjenjivim cijenama na kontrolnim točkama** upotrebljava se kao zadana vrijednost u polju **Grupa poreza na promet stavke** za kontrolnu točku za naplatu. Računovođa može pregledati i izmijeniti ovu vrijednost na stranici **Transakcije po obračunu**. Pri stvaranju retka prijedloga fakture za projekt sustav upotrebljava vrijednost iz transakcije po obračunu.
 

### <a name="financial-dimensions"></a>Financijske dimenzije

Zadane financijske veličine za kontrolnu točku naplate s fiksnom cijenom postavljene su u redcima ugovora o projektu. Idite na **Ugovori o projektu** > **Prikaži zadano računovodstvo** i na kartici **Redci ugovora** odaberite **redak ugovora s cijenom**, a zatim postavite vrijednosti financijske veličine koje želite upotrebljavati kao zadane.

Računovođa projekta može uređivati podatke o porezu na promet i podatke o financijskim veličinama na kontrolnim točkama fakture sve dok se ne stvori prijedlog fakture za projekt.


## <a name="create-project-invoice-proposals"></a>Stvaranje prijedloga fakture za projekt

Prijedlozi faktura za projekt mogu se pregledati u modulu **Upravljanje projektima i računovodstvo** odlaskom na **Fakture za projekt** > **Prijedlozi faktura za projekt**.

Zaglavlje prijedloga fakture za projekt stvara se u aplikaciji Financije kada je Predračun potvrđen na platformi Dataverse. Radi lakšeg usklađivanja, sustav postavlja broj prijedloga fakture za projekt u aplikaciji Financije na isti broj ID-a predračuna na platformi Dataverse. Budući nije nužno da se predračuni potvrđuju istim redoslijedom kojim su stvoreni, redoslijed brojeva prijedloga faktura za projekt u aplikaciji Financije mora omogućiti promjene na niže i više brojeve. Konfigurirajte brojčane nizove s pomoću sljedećih koraka:

1. U aplikaciji Financije idite na **Administracija tvrtke ili ustanove** > **Broj nizova** > **Broj nizova**.
2. U filtru **Područje** odaberite **Projekti**.
3. U filtru **Referenca** odaberite **Prijedlog fakture**.
4. Upotrijebite polje **Društvo** za filtriranje svake pravne osobe s integracijom aplikacije Project Operations na platformi Dataverse.
5. Otvorite **Pojedinosti broje niza** i na kartici **Općenito** postavite:

    - **Dopusti korisničke promjene: na niži broj** = **Da**
    - **Dopusti korisničke promjene: na viši broj** = **Da**

Retke prijedloga fakture za projekt sustav dodaje s pomoću povremenog postupka **Uvoz iz pripremne tablice** (**Upravljanje projektima i računovodstvo** > **Povremeno** > **Integracija aplikacije Project Operations** > **Uvoz iz pripremne tablice**). Ovaj se postupak može pokrenuti ručno ili s pomoću povremenog rasporeda. Sustav neće dodavati retke u dokument prijedloga fakture dok svi redci ne budu spremni za fakturiranje. Transakcije vremena i materijala spremne su za fakturiranje samo kada su knjižene s pomoću dnevnika **Integracija aplikacije Project Operations**.

## <a name="format-and-print-invoice-proposals"></a>Oblikovanje i ispis prijedloga faktura

Računovođa projekta može prilagoditi ispis fakture za projekt s pomoću stranice **Oblikovanje prijedloga fakture** i mogućnosti upravljanja ispisom.

### <a name="format-invoice-proposals"></a>Oblikovanje prijedloga faktura

Stranica **Oblikovanje prijedloge faktura** omogućuje prilagođeno grupiranje transakcija radi prikaza na fakturi za projekt klijenta.

1. Na stranici **Prijedlog fakture za projekt** odaberite **Ispis** > **Oblikuj prijedlog fakture**.
2. Odaberite **Novi** za stvaranje novog grupiranja za ispis fakture za projekt.
3. U polju **Pojedinosti/sažetak** odaberite mogućnosti za ovo grupiranje:

    - Odaberite **Pojedinosti** za ispis pojedinosti o transakciji s fakture klijenta.
    - Odaberite **Sažetak** za ispis sažetka transakcije s fakture klijenta.

> [!NOTE]
> Odabir u polju **Pojedinosti/sažetak** na stranici **Oblikovanje prijedloga fakture** poništava mogućnost odabranu u polju **Oblik fakture** na stranici **Prijedlozi faktura** za ispis fakture s pojedinostima ili sažete fakture.

- Odaberite retke transakcija koje ćete uključiti u ovaj odjeljak na kartici **Dostupne transakcije** i odaberite **Uključi transakcije** kako biste ih premjestili na karticu **Odabrane transakcije**.
- Odaberite **Pomakni se gore** i **Pomakni se dolje** kako biste promijenili redoslijed odjeljaka.
- Odaberite **Pretpregled prije ispisa** kako biste pretpregledali formatirane fakture.

### <a name="print-management"></a>Upravljanje ispisom

Upravljanje ispisom upotrebljava različite datoteke izvješća za ispis, određivanje odredišta i prilagodbu teksta podnožja za fakturu. Upravljanje ispisom može se postaviti na razini modula, no te se postavke mogu nadjačati za određenog kupca, ugovor ili prijedlog fakture. Kako biste pristupili ovoj funkciji na stranici **Prijedlog fakture za projekt**, odaberite **Ispis** > **Upravljanje ispisom**.

Postavljanje upravljanja ispisom prikazuje se u obliku stabla, gdje svaka razina čvora prikazuje dostupne dokumente za prilagodbu. Možete dodijeliti prilagođene ispise na razini modula, klijenta, ugovora ili dokumenta s prijedlogom fakture. Kako biste izmijenili ispis izvornog dokumenta, proširite željeni čvor i odaberite **Izvorna stavka**. U polju **Oblik izvješća** odaberite oblik izvješća koji će se upotrebljavati za ispis. Možete upotrebljavati prilagođene oblike izvješća s pomoću [okvira za Upravljanje poslovnim dokumentima](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Knjiženje prijedloga faktura

Nakon što je faktura pregledana i uređena, a redci prijedloga fakture zadovoljavaju, provjerite ukupne iznose fakture i porez na promet. U grupi **Pojedinosti** odaberite **Ukupno**, a zatim odaberite **Knjiži** za knjiženje fakture.

Kako biste pregledali fakturu prije knjiženja, očistite potvrdni okvir **Knjiženje**. **Pro forma** je tekst koji će se ispisati na fakturi kako bi se označilo da je to uzorak fakture. Kako biste ispisali fakturu, odaberite potvrdni okvir **Ispis fakture**.

Osim na stranici **Prijedlog fakture**, prijedlozi faktura mogu se knjižiti i pokretanjem povremenog posla **Knjiženje prijedloga faktura**. Kako biste pronašli ovaj posao, idite na **Upravljanje projektima i računovodstvo** > **Povremeno** > **Fakture za projekt** > **Knjiženje prijedloga faktura**.

Ova stranica prikazuje sve prijedloge faktura koji su spremni za knjiženje. Možete planirati knjiženje prijedloga faktura odabirom **Serija**. Postavite **Parametar serijske obrade** na **Da** i postavite ponavljanje serijske obrade odabirom **Ponavljanje**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
