---
title: Novosti u siječnju 2021. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovoj temi nalaze se informacije o ažuriranjima kvalitete dostupnim u izdanju aplikacije Project Operations za scenarije koji se temelje na resursu / bez zaliha za siječanj 2021.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9d54d5fed6e8ec1535ad798073ac8a1eec36e87d1dbba4cc4acd94d8bbdc5157
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008082"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u siječnju 2021. – Project Operations za scenarije temeljene na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_


Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

  - Project Operations u verziji 4.6.0.154 okruženja platforme Dataverse
  - Upravljanje projektima i računovodstvo u okruženju aplikacije Dynamics 365 Finance verzije 10.0.16

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| **Implementacija i konfiguracija** | 2106818 | Ispravljeno je preimenovanje web-izvora koje je uzrokovalo probleme u vezi s prilagođavanjem stranice. |
| **Naplata i određivanje cijene** | 2091908 | Ispravljena je vidljivost mogućnosti **Zaključaj cijene** i **Upotrijebi trenutačnu cijenu** na stranici **Faktura** kada je aplikacije Project Operations instalirana zajedno s rješenjem Dynamics 365 Field Service. |
| **Naplata i određivanje cijene** | 2103058 | Osvježena mogućnost **Ukupni zbrojevi projekta** za obradu nultih vrijednosti stvarnih troškova zadatka. |
| **Naplata i određivanje cijene** | 2116100 | Poboljšane poruke o pogreškama koje se upotrebljavaju s funkcijom **Točni unosi o stvarnim podacima**. |
| **Naplata i određivanje cijene** | 2116129 | Poboljšana vidljivost procjena troškova na kartici **Procjene** stranice **Projekti**. |
| **Naplata i određivanje cijene** | 2119112 | Ispravljeno je pogrešno zbrajanje stvarnih vrijednosti prodaje i troškova kada su se primjenjivali različiti tečajevi. |
| **Naplata i određivanje cijene** | 2134705 | Ispravljena je pogreška, „Nije moguće pročitati svojstvo **getResourceString** nedefiniranog” kada se otvarala stranica **Faktura** i instalirala aplikacija Field Service. |
| **Upravljanje prilikama** | 2022195 | Rešetka za naplatu temeljena na zadacima na stranici **Projekt** sadrži ikonu koja označava da postoji ugovor ili redak ponude povezan s tim zadatkom. |
| **Upravljanje prilikama** | 2029135 | Ispravljena je pogreška poslovnog procesa koja se javljala kada je korisnik pokušavao otvoriti redak fakture na potvrđenoj fakturi s fakturiranim iznosom predujma. |
| **Upravljanje prilikama** | 2040713 | Ispravljena je pogreška skripte koja se događala tijekom stvaranja fakture iz ugovora kada se instalirala aplikacija Field Service. |
| **Planiranje i praćenje projekta** | 2090202 | Poslovna pravila koja se više ne upotrebljavaju označena su kao **Zastarjelo**. |
| **Vrijeme i trošak** | 2091249 | Postrožene su kontrole tako da korisnici ne mogu promijeniti zadatak na poslanom ili odobrenom vremenskom unosu. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektom i računovodstvo u aplikaciji Dynamics 365 Finance

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| **Upravljanje projektom i računovodstvo** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Neispravan iznos ugovora na stranici **Djelomično plaćanje** za projekt s fiksnom cijenom s više izvora financiranja. |
| **Upravljanje projektom i računovodstvo** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Rezervirano mjesto **Prijedlog fakture.PSAnfRefProjId** ne prikazuje ID projekta za tijek rada **Pregled prijedloga faktura za projekt**. |
| **Upravljanje projektom i računovodstvo** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Pogrešan datum gotovinskog popusta upotrebljava se tijekom knjiženja prijedloga faktura za projekt. |
| **Upravljanje projektom i računovodstvo** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Uklanjanje i čitanje zadataka resursa u aplikaciji Project Operations udvostručuje unose predviđanja projekata u aplikaciju Financije. |
| **Upravljanje projektom i računovodstvo** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | U aplikaciji Project Operations, ne možete stvoriti procjene projekata na platformi Dataverse bez da imate redak ugovora na projektu. |
| **Upravljanje projektom i računovodstvo** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Financijska veličina transakcije troškova projekta nije sinkronizirana s povezanim vaučerom i računovodstvenom distribucijom izvješća o troškovima kada se troškovi knjiže na saldo. |
| **Upravljanje projektom i računovodstvo** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Filtar **Status fakture** za proknjižene projektne transakcije za projekte s fiksnom cijenom ne radi. |
| **Upravljanje projektom i računovodstvo** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Eliminacija stornirane procjene ne radi u odjeljku **Povremeno**. |
| **Upravljanje projektom i računovodstvo** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Redci prijedloga fakture mogu se izbrisati u aplikaciji Project Operations kada se integriraju na platformi Dataverse. |
| **Upravljanje projektom i računovodstvo** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Spriječite omogućivanja značajke višestrukih redaka ugovora bez integracije u platformu Dataverse. |
| **Upravljanje projektom i računovodstvo** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Kada je fakturiranje s djelomičnim plaćanjem jednako dobiti i gubitku, fakturirani prihod navodi se kao nula na stranici Procjene. |
| **Upravljanje projektom i računovodstvo** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Ispravke računa ne funkcioniraju u integriranim okruženjima. |
| **Upravljanje projektom i računovodstvo** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Tijekom knjiženja WIP-a – vrijednost prodaje pri fakturiranju projekata unutar tvrtke odabire pogrešan račun. |
| **Upravljanje projektom i računovodstvo** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | U aplikaciji Project Operations ovisnosti o zadacima procjene na platformi Dataverse ne mogu se ažurirati. |
| **Upravljanje projektom i računovodstvo** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Neprestano brisanje dnevnika za integraciju aplikacije Project Operations s aplikacijom Financije dovodi do gubitka podataka. |
| **Upravljanje projektom i računovodstvo** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Sljedeća se pogreška događa tijekom objavljivanja prijedloga fakture za projekt, „Transakcija nema salda na valuti izvješća kada se doda odbijeni predujam po fakturi”. |
| **Upravljanje projektom i računovodstvo** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Pogrešan ID projekta uključuje se u odbitke nakon što se zadani ugovor o projektu ažurira u aplikaciji Project Operations. |
| **Upravljanje projektom i računovodstvo** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Procjena i priznavanje prihoda ne mogu se dovršiti kada je omogućena aplikacija Project Operations. |
| **Upravljanje projektom i računovodstvo** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Uklanjanje projekta iz ugovora u aplikaciji Project Operations ne poništava zadani projekt u ugovoru. |
| **Upravljanje projektom i računovodstvo** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Na fakturi unutar tvrtke u aplikaciji Project Operations, na popisu **Dodaj redak** prikazuju se pogrešni redci troškova. |
| **Putovanje i trošak** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Redci troškova ne mogu se knjižiti jer u retku ugovora nedostaje postavka sata. |
| **Putovanje i trošak** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Kada je provjera valjanosti projekta/kategorije obvezna, kategorije troškova povezane s projektom nisu vidljive u izvješću o troškovima. |
| **Putovanje i trošak** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Saldo gotovinskog predujma ne ažurira se kada se izvješće o troškovima knjiži redom. |
| **Putovanje i trošak** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Posao **Ažuriraj podatke o plaćanju** ne uspijeva nakon storniranja poravnanja u kojima je namiren račun s dvije ili više platnih transakcija. |
| **Putovanje i trošak** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Postoji problem s izračunom smanjenja obroka za zadnji dan za kategoriju troškova za dnevnice. |
| **Putovanje i trošak** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Izvješće **Vrsta troška po zaposlenom** ne prikazuje podroban popis stavki troškova ako se korisnik prvi put povezao na jeziku es-MX. |
| **Putovanje i trošak** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Plaćanje dobavljača za fakturu iz izvješća o troškovima upotrebljava pogrešan sažeti račun za knjiženje poravnanja. |
| **Putovanje i trošak** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Kada se proknjiži izvješće o troškovima uz omogućene značajke **Omogući grupiranje transakcija na temelju računa sa zakašnjelim plaćanjem** i **Ispravljanje računovodstvenog datuma pri knjiženju** računovodstveni datumi nisu grupirani u tablici **Računovodstvena distribucija** što utječe na evidenciju poreza na promet. |
| **Putovanje i trošak** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Mapiranje potkategorije troškova uklanja se kada se potvrdni okvir Upotrijebi u trošku izbriše, a zatim ponovno odabere. |
| **Putovanje i trošak** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Izvješće o troškovima unutar tvrtke ne može se stvoriti ako se ID projekta doda na razinu zaglavlja. |
| **Putovanje i trošak** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Postoji problem s plaćanjem troškova kada je iznos troškova veći od iznosa gotovinskog predujma. |
| **Putovanje i trošak** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Polje **ID projekta** u izvješću o troškovima unutar tvrtke prazno je ako je uloga korisnika dodijeljena određenoj tvrtki ili ustanovi. |
| **Putovanje i trošak** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kategorija troškova zaključava se prilikom dodavanja novog retka troška. |
| **Putovanje i trošak** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Podroban popis redaka izvješća o troškovima koji su već podijeljeni rezultira nekompletnim knjiženjem dugovanja \ vaučera Glavne knjige. Zbog dupliciranja **TRVEXPTRANS.SOURCEDOCUMENTLINE** neispravno radi i alat Accounting Source Explorer. |
| **Putovanje i trošak** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Indeks dodan tablici **TRVREQUISITIONLINE** za koju kupac ima duplikate, rezultira pogreškom tijekom nadogradnje. |
| **Putovanje i trošak** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | U aplikaciji Project Operations, vrijeme zadataka unutar kompanije na platformi Dataverse ne može se stvoriti ili odobriti. |

## <a name="regulatory-updates"></a>Ažuriranja propisa

Za informacije o ažuriranjima propisa za aplikacije Finance and Operations, pogledajte članak [Ažuriranja propisa](/dynamics365/finance/localizations/regulatory-updates). Također se možete prijaviti na LCS i pregledati planirana regulatorna ažuriranja s pomoću alata za pretraživanje izdanja. Pretraživanje izdanja omogućuje vam pretraživanje po zemlji, vrsti značajke i izdanju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]