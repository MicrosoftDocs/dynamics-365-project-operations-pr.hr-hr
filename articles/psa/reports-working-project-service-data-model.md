---
title: Rad s podatkovnim modelom Project Service Automation
description: Ovaj tema sadrži informacije o radu s podatkovnim modelom.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9bceb96153f0e9f5c0d40478baf691220de95f27
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642669"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Rad s podatkovnim modelom Project Service Automation

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Service Automation proširuje druge entitete aplikacija i uvodi vlastite entitete u podatkovni model Common Data Service. Ovaj tema opisuje neke entitete koje možete pronaći u uobičajenim scenarijima izvješćivanja u PSA-u.

## <a name="reporting-on-opportunities"></a>Izvješćivanje o prilikama

Project Service Automation proširuje entitet Dynamics 365 Sales **Opportunity** dodavanjem polja koja omogućuju scenarije koji se temelje na projektu. Ta su polja identificirana nazivom sheme s prefiksom **msdyn\_**. **Vrsta narudžbe** novo je polje koje je važno za izvješćivanje o prilikama u PSA-u. Vrijednost **Utemeljeno na poslu** za ovo polje pokazuje da se radi o prilici u PSA-u. Ostala polja koja su dodana entitetu uključuju polje **Ugovorena organizaciju**, koje obuhvaća tvrtku ili ustanovu koja sadrži priliku, i polje **Upravitelj računa**, koje uključuje naziv upravitelja računa koji je odgovoran za priliku.

Entitet **Redak prilike** uključuje i polja koja su povezana s aplikacijom Project Service. Polje **Način naplate** pokazuje treba li se redak prilike naplatiti na temelju vremena i materijala ili na temelju fiksne cijene, a polje **Projekt** sadrži naziv projekta povezan s prilikom. Ostala polja koja omogućuju izvješća odražavaju troškove i proračunske iznose klijenata za stavku retka.

## <a name="reporting-on-quotes"></a>Izvješćivanje o ponudama

PSA proširuje entitet Prodajna **ponuda** dodavanjem polja povezanih s projektom. **Vrsta narudžbe** razlikuje ponude u PSA-u od ponuda koji nisu u PSA-u. Vrijednost **Utemeljeno na poslu** za ovo polje pokazuje da se radi o ponudi u PSA-u. Ostala polja koja mogu biti relevantna za izvješćivanje o ponudama u PSA-u uključuju polja s iznosima, kao što **Naplativi troškovi**, **Nenaplativi troškovi**, **Bruto marža**, **Procjene** i **Proračun**. Ostala korisna polja pokazuju je li ponuda isplativa, bez obzira na to hoće li biti dovršena po rasporedu i ispunjava li očekivanja klijenata o proračunu.

PSA također proširuje entitet **Redak ponude**. Još jedno polje koje PSA dodaje je **Način naplate**, polje koje pokazuje kako će redak ponude biti naplaćen (po vremenu i materijalu ili fiksnoj cijeni). Ostala polja koja su dodana entitetu obuhvaćaju povezani projekt koji podržava redak ponude, fakturiranje, cijenu i proračun.

PSA dodaje i nove entitete povezane s ponudom u podatkovni model Dynamics 365. Evo nekoliko primjera:

- **Pojedinost retka ponude** – ovaj entitet sadrži pojedinosti o procjeni projekta za redak ponude. Ima dva zapisa za svaki redak ponude. Jedan zapis pohranjuje trošak i pojedinosti o trošku u retku ponude, a drugi zapis pohranjuje iznos prodaje i pojedinosti o prodaji u retku ponude.
- **Raspored faktura retka ponude** – ovaj entitet sadrži raspored naplate za redak ponude. Ovaj raspored izvodi se na temelju učestalosti fakturiranja koja je dodijeljena retku ponude.
- **Kontrolna točka retka ponude** – ovaj entitet sadrži kontrolne točke naplate za retke ponude s fiksnom cijenom.
- **Raščlanjivanje analitike retka ponude** – ovaj entitet sadrži financijske pojedinosti o retku ponude. Te pojedinosti mogu biti korisne za izvješćivanje o prodajama i iznosima procijenjenih troškova po različitim dimenzijama.

Ostali entiteti koje PSA dodaje u ponude su **Cjenik projekta retka ponude**, **Kategorija resursa retka ponude** i **Kategorija transakcije retka ponude**.

![Dijagram prikazuje odnose ponude, retka ponude i projekta](media/PS-Reporting-image2.png "Dijagram prikazuje odnose ponude, retka ponude i projekta")

## <a name="reporting-on-project-contracts"></a>Izvješćivanje o ugovorima o projektu

PSA proširuje entitet **Prodajni nalog** koji se koristi prilikom evidentiranja ugovora o projektu. Dodaje važno novo polje **Vrsta narudžbe** u kojem je ugovor definiran kao ugovor o projektu PSA-a, a ne prodajni nalog. Vrijednost **Utemeljeno na poslu** za ovo polje pokazuje da je nalog ugovor o projektu u PSA-u. Ostala nova polja koja su dodana entitetu **Entitet naloga** obuhvaćaju pojedinosti o troškovima, statusu ugovora u PSA-u i tvrtki ili ustanovi koja je vlasnik ugovora.

PSA također proširuje entitet **Redak prodajnog naloga**. Među poljima koja dodaju su polja su koja obuhvaćaju način naplate (po vremenu i materijalu ili fiksnoj cijeni), proračunske iznose klijenta i temeljni projekt.

PSA također dodaje nove entitete koji su namijenjeni ugovorima o projektu. Evo nekoliko primjera:

- **Pojedinost retka ugovora o projektu** – ovaj entitet sadrži pojedinosti na razini retka koje su uključene u iznos retka ugovora. Te pojedinosti mogu biti detaljne kao stavke retka koje su generirane iz rasporeda projekta na razini zadatka.
- **Raspored faktura retka ugovora** – ovaj entitet sadrži raspored naplate koji se generira na temelju učestalosti fakture koja je dodijeljena retku ugovora.
- **Kontrolna točka ugovora** – ovaj entitet sadrži kontrolne točke naplate za retke ugovora koji imaju rok naplate s fiksnom cijenom.

Ostali entiteti koje PSA dodaje u ugovor su **Cjenik projekta retka ugovora o projektu**, **Kategorija resursa retka ugovora o projektu** i **Kategorija transakcije retka ugovora o projektu**.

![Dijagram prikazuje odnose narudžbe, retka narudžbe i projekta](media/PS-Reporting-image3.png "Dijagram prikazuje odnose narudžbe, retka narudžbe i projekta")

## <a name="reporting-on-projects"></a>Izvješćivanje o projektima

Entitet **Projekti** i povezani entiteti svojstveni su samo PSA-u. **Projekt** je entitet najviše razine koji služi za bilježenje strane rada i troškova operacija. U nastavku potražite popis povezanih entiteta:

- **Član projektnog tima** – ovaj entitet sadrži pojedinosti o resursima koji se mogu rezervirati, a dodijeljeni su projektu. Ti resursi mogu biti generički resursi koji se mogu rezervirati ili imenovani resursi koji se mogu rezervirati koje je unio voditelj projekta ili su izvedeni iz rasporeda projekta.
- **Projektni zadatak** – ovaj entitet sadrži zadatke koji čine plan ili raspored projekta.
- **Dodjela resursa** – ovaj entitet sadrži dodjelu zadatka za resurs koji se može rezervirati.
- **Preduvjet resursa** – ovaj entitet sadrži preduvjete za članove tima generičkog resursa.
- **Procjena** i **Redak procjene** – ovi entiteti imaju odnos zaglavlje/redak i sadrže procjene troškova za projekt. Procjene zadataka pohranjene su na entitetu **Procjena resursa**.

![Dijagram prikazuje odnose preduvjeta resursa i projekta](media/PS-Reporting-image4.png "Dijagram prikazuje odnose preduvjeta resursa i projekta")

## <a name="reporting-on-resources"></a>Izvješćivanje o resursima

Resursi projekta koriste entitete **Resurs koji je moguće rezervirati** iz aplikacije Universal Resource Scheduling (URS) koji se dijele s drugim aplikacijama, kao što je Microsoft Dynamics 365 Field Service. U nastavku potražite popis entiteta kojima ćete se možda morati služiti prilikom izvješćivanja o resursima projekta:

- **Resurs koji je moguće rezervirati** – ovaj entitet predstavlja korisnika, kontakt, generički resurs, račun, grupu ili opremu koja se koristi u projektnom timu.
- **Značajke kategorije resursa koji je moguće rezervirati** – ovaj entitet uključuje vještine, certifikate ili obrazovanje resursa. Značajke mogu imati vrijednosti ocjene koje su definirane modelom ocjenjivanja.
- **Kategorija resursa koji je moguće rezervirati** – ovaj entitet predstavlja ulogu resursa koji je moguće rezervirati.
- **Rezervacije resursa koji je moguće rezervirati** – ovaj entitet predstavlja vrijeme koje je rezervirano za projekte resursa. Svaka rezervacija ima entitet zaglavlja i entitete retka, a svaki redak ima status koji predstavlja status rezervacije.

![Dijagram prikazuje odnose svojstava resursa koje se može rezervirati](media/PS-Reporting-image5.png "Dijagram prikazuje odnose svojstava resursa koje se može rezervirati")

## <a name="reporting-on-actual-transactions"></a>Izvješćivanje o stvarnim transakcijama

Kada odobrite vremensku tablicu ili trošak ili fakturirate ugovor u PSA-u, poslovna transakcija bilježi se na entitetu **Stvarno**. Taj entitet može poslužiti kao osnova za gotovo sva financijska izvješća u PSA-u. Entitet **Stvarno** bilježi transakcije troška i prodaje za poslovni događaj. Bilježi i brojne relevantne atribute.

Kada radite s entitetom **Stvarno**, važno je da imate uvid u to koja se transakcija ili transakcije bilježe u entitetu i kada se transakcije bilježe. Slijedi uobičajeni tijek kada radite s vremenskim unosima (tijek za unose troška je sličan):

1. Kada se Unos vremena spremi, u entitetu **Stvarno** nema izrađenih zapisa.
2. Kada se Unos vremena pošalje, u entitetu **Stvarno** nema izrađenih zapisa.
3. Kada se Unos vremena odobri, jedan je zapis izrađen u entitetu **Stvarno**, a može biti izrađen i drugi zapis. U prvom se zapisu pohranjuje trošak unosa vremena. U drugom zapisu pohranjuje se iznos nenaplaćene prodaje unosa vremena. Drugi zapis ovisi o tome je li projektu dodijeljen klijent, ponuda ili redak ugovora.

    | Datum dokumenta | Vrsta transakcije | Razred transakcije | Klijent         | Ugovor   | Resurs     | Uloga resursa | Vrsta naplate | Količina | Jedinična cijena | Iznos |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 02.03.2018.        | Trošak             | Time              | Alpska skijaška koliba | Alpski CRM | Dragica Čeh | Voditelj projekta   | Naplativo   | 8.0      | 50,00      | 400,00 |
    | 02.03.2018.        | Nenaplaćene prodaje   | Time              | Alpska skijaška koliba | Alpski CRM | Dragica Čeh | Voditelj projekta   | Naplativo   | 8.0      | 100,00     | 800,00 |

    Ova su dva zapisa zasebni, ali povezani zapisi. Oni nisu dugovanja ni potraživanja.

4. Ako je ugovor pridružen projektu, kada se fakturira Unos vremena, u entitetu **Stvarno** stvaraju se još dva zapisa. Prvo se stvara negativan iznos za zapis nenaplaćene prodaje. Ovaj zapis zapravo poništava nenaplaćenu prodaju. Zatim se stvara transakcija za naplaćenu prodaju. Ovi su zapisi zasebni, ali povezani zapisi, a ne dugovanja i potraživanja.

    | Datum dokumenta | Vrsta transakcije | Razred transakcije | Klijent         | Ugovor   | Resurs     | Uloga resursa | Vrsta naplate | Količina | Jedinična cijena | Iznos   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 02.04.2018.        | Nenaplaćene prodaje   | Time              | Alpska skijaška koliba | Alpski CRM | Dragica Čeh | Voditelj projekta   | Naplativo   | - 8,0    | 100,00     | - 800,00 |
    | 02.04.2018.        | Naplaćene prodaje     | Time              | Alpska skijaška koliba | Alpski CRM | Dragica Čeh | Voditelj projekta   | Naplativo   | 8.0      | 100,00     | 800,00   |

Entitet **Izvor transakcije** bilježi izvor zapisa **Stvarno**, a entitet **Veza transakcije** bilježi povezane zapise za zapis **Stvarno**. Osim toga, zapis **Stvarno** sadrži reference za projekt, ugovor o projektu (nalog), resurs koji se može rezervirati i klijenta.

![Dijagram prikazuje odnose transakcijske veze, podrijetla i ostvarenja](media/PS-Reporting-image6.png "Dijagram prikazuje odnose transakcijske veze, podrijetla i ostvarenja")
