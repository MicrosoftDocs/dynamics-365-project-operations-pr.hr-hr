---
title: Uvođenje prilagođenih polja za mobilnu aplikaciju Microsoft Dynamics 365 Project Timesheet na platformama iOS i Android
description: U ovom se članku nalaze uobičajeni obrasci za korištenje proširenja za implementaciju prilagođenih polja.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 03b79d58d1f91e07034b8c9efb408e6d7a9c29a8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913703"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Uvođenje prilagođenih polja za mobilnu aplikaciju Microsoft Dynamics 365 Project Timesheet na platformama iOS i Android

[!include [banner](../includes/banner.md)]

U ovom se članku nalaze uobičajeni obrasci za korištenje proširenja za implementaciju prilagođenih polja. Obuhvaćeni su sljedeći članci:

- Razne vrste podataka koje podržava prilagođeni okvir polja
- Način prikazivanja polja samo za čitanje ili uređivanje na unosima evidencije radnog vremena i spremanje vrijednosti koje su unijeli korisnici natrag u bazu podataka
- Način prikazivanja polja samo za čitanje u zaglavlju evidencije radnog vremena
- Način integriranja druge prilagođene poslovne logike za unos zadanih vrijednosti u polja i provođenje dodatne provjere valjanosti

## <a name="audience"></a>Korisnici

Ovaj članak namijenjen je programerima koji integriraju svoja prilagođena polja u mobilnu Microsoft Dynamics 365 Project Timesheet aplikaciju koja je dostupna apple iOS- u i Googleu Android. Pretpostavka je da su čitatelji upoznati s X++ razvojem i funkcionalnošću evidencije radnog vremena na projektu.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Ugovor o podacima – klasa TSTimesheetCustomField X++

Klasa **TSTimesheetCustomField** klasa je ugovora podataka X++ koja predstavlja informacije o prilagođenom polju za funkcionalnost evidencije radnog vremena. Popisi objekata prilagođenih polja prosljeđuju se na oba ugovora o podacima, i TSTimesheetDetails i TSTimesheetEntry, radi prikazivanja prilagođenih polja u mobilnoj aplikaciji.

- **TSTimesheetDetails** – Ugovor o zaglavlju evidencije radnog vremena.
- **TSTimesheetEntry** – Ugovor o transakciji evidencije radnog vremena. Grupe ovih objekata koje imaju iste podatke o projektu i vrijednost **timesheetLineRecId** čine redak.

### <a name="fieldbasetype-types"></a>fieldBaseType (vrste)

Svojstvo **FieldBaseType** na objektu **TsTimesheetCustom** određuje vrstu polja koje se prikazuje u aplikaciji. Podržane su sljedeće vrijednosti **Vrste**.

| Vrijednost vrsta | Tip              | Bilješke |
|-------------|-------------------|-------|
| 0           | Niz (i nabrajanje) | Polje se prikazuje kao tekstno polje. |
| 1           | Integer           | Vrijednost je prikazana kao broj bez decimalnih mjesta. |
| 2           | Stvaran              | Vrijednost je prikazana kao broj s decimalnim mjestima.<p>Kako biste prikazali stvarnu vrijednost kao valutu u aplikaciji, upotrijebite svojstvo **fieldExtensedType**. Možete upotrijebiti svojstvo **numberOfDecimals** za postavljanja broja decimalnih mjesta koji će se prikazati.</p> |
| 3           | Datum              | Oblici datuma određeni su korisničkom postavkom **Datum, vrijeme i oblik broja** koja je navedena pod stavkom **Preferencije jezika i zemlje/regije** u mogućnosti **Korisničke mogućnosti**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Ako svojstvo **stringOptions** nije osigurano objektu **TSTimesheetCustomField**, korisniku se omogućuje polje slobodnog teksta.

    Svojstvo **stringLength** može se upotrebljavati za postavljanje maksimalne duljine niza koju korisnici mogu unijeti.

- Ako je svojstvo **stringOptions** osigurano objektu **TSTimesheetCustomField**, ti su elementi popisa jedine vrijednosti koje korisnici mogu odabrati s pomoću gumba s mogućnostima (gumbi za odabir).

    U ovom slučaju polje niza može djelovati kao vrijednost nabrajanja u svrhu korisničkog unosa. Da biste spremili vrijednost u bazu podataka kao enum, ručno mapirajte vrijednost niza natrag na vrijednost enum prije spremanja u bazu podataka pomoću lanca naredbi (pogledajte odjeljak "Koristi lanac naredbi u klasi TSTimesheetEntryService za spremanje unosa vremenske tablice iz aplikacije natrag u bazu podataka" kasnije u ovom članku).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Ovo svojstvo možete upotrebljavati za oblikovanje stvarnih vrijednosti kao valute. Ovaj pristup primjenjiv je samo kada je vrijednost **fieldBaseType** **Stvarna**.

- **TSCustomFieldExtendedType: Nijedan** – Nije primijenjeno oblikovanje.
- **TSCustomFieldExtendedType::Valuta** – Formatiranje vrijednosti kao valute.

    Kada je aktivno formatiranje valute, polje **stringValue** može se upotrebljavati za dodavanje koda valute koji bi se trebao prikazati u aplikaciji. Vrijednost je vrijednost samo za čitanje.

    Polje **realValue** sadrži iznos novca koji bi se trebao spremiti u bazu podataka.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Ovo svojstvo možete upotrijebiti za određivanje mjesta u aplikaciji na kojem bi se prilagođeno polje trebalo prikazati.

- **TSCustomFieldSection::Zaglavlje** – Polje će se prikazati u odjeljku **Pogledajte više pojedinosti** u aplikaciji. Ova polja uvijek su samo za čitanje.
- **TSCustomFieldSection::Redak** – Polje će se prikazati nakon svih polja s gotovim retkom u unosima evidencije radnog vremena. Ta polja mogu se uređivati ili biti samo za čitanje.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Ovo svojstvo identificira polje kada se vrijednosti koje daje aplikacija spremaju natrag u bazu podataka.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Ovo svojstvo identificira polje kada se vrijednosti koje daje aplikacija spremaju natrag u bazu podataka.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Postavite ovo svojstvo na **Da** kako biste odredili da polje u odjeljku za unos evidencije radnog vremena trebaju uređivati korisnici. Postavite svojstvo na **Ne** kako bi polje bilo samo za čitanje.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Postavite ovo svojstvo na **Da** kako biste odredili da je polje u odjeljku za unos evidencije radnog vremena obvezno.

### <a name="label-str"></a>oznaka (niz)

Ovo svojstvo navodi oznaku koja se prikazuje pokraj polja u aplikaciji.

### <a name="stringoptions-list-of-strings"></a>stringOptions (Popis nizova)

Ovo je svojstvo primjenjivo samo kada je **fieldBaseType** postavljeno na **Niz**. Ako je stavka **stringOptions** postavljena, vrijednosti niza koje su dostupne za odabir putem gumba mogućnosti (gumb za odabir) određene su nizovima na popisu. Ako nisu navedeni nizovi, dopušten je unos slobodnog teksta u polju niza (pogledajte odjeljak "Koristi lanac naredbi u klasi TSTimesheetEntryService da biste spremili unos vremenske tablice iz aplikacije natrag u bazu podataka" kasnije u ovom članku).

### <a name="stringlength-int"></a>stringLength (int)

Ovo svojstvo određuje maksimalnu duljinu polja niza. Primjenjivo je samo kada je **fieldBaseType** postavljeno na **Niz**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Ovo svojstvo navodi broj decimalnih mjesta koja se prikazuju za stvarno polje. Primjenjivo je samo kada je **fieldBaseType** postavljeno na **Stvarno**.

### <a name="ordersequence-int"></a>orderSequence (int)

Ovo svojstvo nadzire redoslijed prikazivanja prilagođenih polja u aplikaciji kada je navedeno više od jednog prilagođenog polja. Prvo se prikazuju polja s manjim brojevima.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Za polja vrste **Boole**, ovo svojstvo prenosi Booleovu vrijednost polja između poslužitelja i aplikacije.

### <a name="guidvalue-guid"></a>guidValue (guid)

Za polja vrste **GUID**, ovo svojstvo prenosi vrijednost globalno jedinstvenog identifikatora (GUID) polja između poslužitelja i aplikacije.

### <a name="int64value-int64"></a>int64Value (int64)

Za polja vrste **Int64**, ovo svojstvo prenosi Int64 vrijednost polja između poslužitelja i aplikacije.

### <a name="intvalue-int"></a>intValue (int)

Za polja vrste **Int**, ovo svojstvo prenosi int vrijednost polja između poslužitelja i aplikacije.

### <a name="realvalue-real"></a>realValue (stvarno)

Za polja vrste **Stvarno**, ovo svojstvo prenosi stvarnu vrijednost polja između poslužitelja i aplikacije.

### <a name="stringvalue-str"></a>stringValue (niz)

Za polja vrste **Niz**, ovo svojstvo prenosi vrijednost niza u polju između poslužitelja i aplikacije. Također se upotrebljava za polja vrste **Stvarno** koja su formatirana kao valuta. Za ta polja svojstvo se upotrebljava za prosljeđivanje koda valute aplikaciji.

### <a name="datevalue-date"></a>dateValue (datum)

Za polja vrste **Datum**, ovo svojstvo prenosi vrijednost datuma u polju između poslužitelja i aplikacije.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Prikaz i spremanje prilagođenog polja u odjeljku unosa evidencije radnog vremena

U nastavku se nalazi snimka zaslona mobilne aplikacije na kojoj se stvara unos evidencije radnog vremena. Prikazuje gotova i prilagođena polja u odjeljku „Unos vremena” pod nazivom „Testni niz” s već postavljenom vrijednosti nabrajanja „Druga mogućnost”.

![Testni niz prilagođenog polja u aplikaciji.](media/timesheet-entry.jpg)



U nastavku se nalazi snimka zaslona mobilne aplikacije na kojoj korisnik odabire jednu od mogućnosti nabrajanja dostupnih za prilagođeno polje „Testni niz”.  Dvije mogućnosti, „Prva mogućnost” i „Druga mogućnost”, prikazane su kao gumbi za odabir. Trenutačno je odabrana druga mogućnost.

![Gumbi mogućnosti (gumbi za odabir) za prilagođeno polje Testni niz.](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Proširivanje tablice TSTimesheetLine tako da ima prilagođeno polje

U uobičajenim scenarijima vjerojatno će se podaci za prilagođeno polje u odjeljku unosa evidencije radnog vremena spremiti u tablicu TSTimesheetLine. Međutim, druge se tablice mogu upotrebljavati ako se podaci mogu dohvatiti na temelju dostavljenog zapisa TSTimesheetTrans ili ako nema određenog konteksta zapisa (na primjer, ako je u parametrima projekta polje postavljeno kao samo za čitanje).

Imajte na umu da prilagođena polja ne moraju imati nikakve sigurnosne zapise baze podataka. Mogu se dinamički generirati na temelju X++ logike. Ovaj pristup može biti koristan u scenarijima samo za čitanje (primjer dinamički generiranih vrijednosti prilagođenih polja potražite u odjeljku „Uporaba lanca naredbi na klasi TSTimesheetDetails, načina buildCustomFieldListForHeader za popunjavanje pojedinosti evidencije radnog vremena”.)

U nastavku se nalazi snimka zaslona aplikacije Visual Studio na kojem se nalazi stablo objekata aplikacije. Ona prikazuje proširenje tablice TSTimesheetLine poljem TestLineString koje je dodano kao prilagođeno polje.

![Niz retka.](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Uporaba lanca naredbi u načinu buildCustomFieldList klase TSTimesheetSettings za prikaz polja u odjeljku unosa evidencije radnog vremena

Ovaj kôd regulira postavke zaslona za polje u aplikaciji. Na primjer, regulira vrstu polja, oznaku, je li polje obavezno i u kojem se odjeljku polje prikazuje.

Sljedeći primjer prikazuje polje niza za unose vremena. Ovo polje ima dvije mogućnosti, **Prva mogućnost** i **Druga mogućnost**, koje su dostupne putem gumba mogućnosti (gumbi za odabir). Polje u aplikaciji povezano je s poljem **TestLineString** koje se dodaje tablici TSTimesheetLine.

Obratite pažnju na uporabu načina **TSTimesheetCustomField::newFromMetatdata()** za pojednostavljivanje inicijalizacije svojstava prilagođenog polja: **fieldBaseType**, **tableName**, **fieldname**, **oznaka**, **isEditable**, **isMandatory**, **stringLength** i **numberOfDecimals**. Te parametre možete postaviti i ručno, ako želite.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Uporaba lanca naredbi u načinu buildCustomFieldListForEntry klase TSTimesheetEntry za unos vrijednosti u unos evidencije radnog vremena

Način **buildCustomFieldListForEntry** upotrebljava se za unos vrijednosti u spremljene retke evidencije radnog vremena u mobilnoj aplikaciji. Kao parametar uzima se zapis TSTimesheetTrans. Polja iz tog zapisa mogu se upotrebljavati za popunjavanje vrijednosti prilagođenog polja u aplikaciji.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Uporaba lanca naredbi u klasi TSTimesheetEntryService za spremanje unosa evidencije radnog vremena iz aplikacije natrag u bazu podataka

Kako biste spremili prilagođeno polje natrag u bazu podataka uobičajenom uporabom, morate proširiti više načina:

- Način **timesheetLineNeedsUdddating** upotrebljava se za utvrđivanje je li korisnik promijenio zapis retka u aplikaciji i mora li se spremiti u bazu podataka. Ako izvedba nije zabrinjavajuća, ovaj način možete pojednostaviti tako da on uvijek vrati vrijednost **točno**.
- Načini **populateTimesheetLineFromEntryDuringCreate** i **populateTimesheetLineFromEntryDuringUpdate** mogu se proširiti tako da unose vrijednosti u zapis baze podataka TSTimesheetLine iz danog zapisa ugovornih podataka TSTimesheetEntry. U primjeru koji slijedi vidjet ćete kako se ručno vrši mapiranje između polja baze podataka i polja unosa putem X++ koda.
- Način **populateTimesheetWeekFromEntry** također se može proširiti ako se prilagođeno polje mapira na objekt **TSTimesheetEntry** mora upisati natrag u tablicu baze podataka TSTimesheetLineweek.

> [!NOTE]
> U sljedećem primjeru, vrijednost **firstOption** ili **secondOption** koju korisnik odabire sprema se u bazu podataka kao sirova vrijednost niza. Ako je polje baze podataka polje vrste **Nabrajanje**, te se vrijednosti mogu ručno preslikati na vrijednost nabrajanja, a zatim spremiti u polje nabrajanja u tablici baze podataka.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Prikaz prilagođenog polja u odjeljku zaglavlja evidencije radnog vremena

U nastavku se nalazi snimka zaslona mobilne aplikacije na kojoj korisnik pregledava evidenciju radnog vremena. U gornjem desnom kutu odabran je gumb „Više informacija” za prikazivanje mogućnosti „Prikaži više pojedinosti”.  

![Naredba prikaz više pojedinosti.](media/show-more.png)

U nastavku se nalazi snimka zaslona mobilne aplikacije na kojoj se prikazuje odjeljak „Više” evidencije radnog vremena. Prilagođeno polje pod nazivom „Stopa iskorištavanja ove evidencije radnog vremena (izračunano prilagođeno polje)” dodano je u odjeljak zaglavlja evidencije radnog vremena. U prilagođenom polju postavljena je vrijednost samo za čitanje „0.667”.

![Više odjeljaka.](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Proširivanje tablice TSTimesheetTable tako da ima prilagođeno polje

U uobičajenim scenarijima vjerojatno će se podaci za prilagođeno polje u odjeljku zaglavlja povući iz tablice TSTimesheetHeader. Međutim, druge se tablice mogu upotrebljavati ako se podaci mogu dohvatiti na temelju dostavljenog zapisa TSTimesheetTable ili ako nema određenog konteksta zapisa (na primjer, ako je u parametrima projekta polje postavljeno kao samo za čitanje).

Imajte na umu da prilagođena polja ne moraju imati nikakve sigurnosne zapise baze podataka. Mogu se dinamički generirati na temelju X++ logike. Primjer koji slijedi pokazuje ovaj pristup.

Polja u odjeljku zaglavlja u aplikaciji su uvijek samo za čitanje.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Uporaba lanca naredbi u načinu buildCustomFieldList klase TSTimesheetSettings za prikaz polja u odjeljku zaglavlja

Ovaj kôd regulira postavke zaslona za polje u aplikaciji. Na primjer, regulira vrstu polja, oznaku, je li polje obavezno i u kojem se odjeljku polje prikazuje.

Sljedeći primjer prikazuje izračunanu vrijednost u odjeljku zaglavlja u aplikaciji.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Uporaba lanca naredbi u načinu buildCustomFieldListForHeader klase TSTimesheetDetails za popunjavanje pojedinosti evidencije radnog vremena

Način **buildCustomFieldListForHeader** upotrebljava se za popunjavanje pojedinosti zaglavlja evidencije radnog vremena u mobilnoj aplikaciji. Kao parametar uzima se zapis TSTimesheetTable. Polja iz tog zapisa mogu se upotrebljavati za popunjavanje vrijednosti prilagođenog polja u aplikaciji. Sljedeći primjer ne čita nikakve vrijednosti iz baze podataka. Umjesto toga, upotrebljava logiku X++ za generiranje izračunane vrijednosti koja se zatim prikazuje u aplikaciji.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Ostale mogućnosti konfiguracije/proširivosti

### <a name="adding-additional-validation-for-the-app"></a>Dodavanje dodatne provjere valjanosti za aplikaciju

Postojeća logika funkcionalnosti evidencije radnog vremena na razini baze podataka i dalje će raditi kako se očekivalo. Kako biste prekinuli dovršavanje operacija spremanja ili slanja i prikazali određenu poruku o pogrešci, možete kôdu dodati **odbaci pogrešku („poruka korisniku”)** putem proširenja lanca naredbe. Evo tri primjera korisnih proširivih načina:

- Ako **validateWrite** u tablici TSTimesheetLine vraća vrijednost **netočno** tijekom operacije spremanja retka evidencije radnog vremena, u mobilnoj se aplikaciji prikazuje poruka o pogrešci.
- Ako **validateSubmit** u tablici TSTimesheetTable vraća vrijednost **netočno** tijekom operacije slanja retka evidencije radnog vremena u aplikaciju, korisniku se prikazuje poruka o pogrešci.
- Logika koja popunjava polja (na primjer, **Svojstvo retka**) tijekom načina **umetni** na tablici TSTimesheetLine i dalje će se izvršavati.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Sakrivanje i označavanje gotovih polja kao polja samo za čitanje putem konfiguracije

Iz parametara projekta možete napraviti gotova polja samo za čitanje ili skrivena u mobilnoj aplikaciji. Postavite mogućnosti u odjeljak **Mobilne evidencije radnog vremena** na kartici **Evidencija radnog vremena** na stranici **Parametri upravljanja projektom i računovodstveni parametri**.

![Parametri projekta.](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Promjena aktivnosti dostupnih za odabir putem proširenja

Aktivnosti dostupne za odabir za projekt popunjavaju se putem načina **getActivitiesForProject()** i **getActivityQuery()** u klasi **TsTimesheetProjectService**. Možete koristiti lanac naredbi kako biste promijenili ovo ponašanje tako da pristaje vašem poslovnom scenariju za aktivnosti koje su dostupne za odabir za određeni projekt.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Unos zadane kategorije projekta u unose evidencije radnog vremena

Unos zadane kategorije projekta u unose evidencije radnog vremena događa se na tri razine. Možete upotrebljavati lanac naredbi kako biste proširili ponašanje na bilo kojoj ili svim ovim razinama radi postizanja željenog ponašanja. Upotrebljava se sljedeća hijerarhija:

1. Aplikacija pokušava staviti zadanu kategoriju iz resursa projekta. Ova zadana kategorija postavljena je u načine **getCurrentUserResource** i **getDelegatedResourcesForCurrentUser** u klasu **TSTimesheetSettingsService**.
2. Ako zadana kategorija nije navedena na razini resursa projekta, aplikacija je pokušava povući iz aktivnosti projekta. Ova zadana kategorija postavljena je u način **getActivitiesForProject** u klasu **TSTimesheetProjectService**.
3. Ako zadana kategorija nije navedena na razini aktivnosti projekta, aplikacija je pokušava uzeti iz parametara projekta. Ova zadana kategorija postavljena je u način **getProjectDetailsbyRule** u klasu **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]