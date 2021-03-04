---
title: Konfiguracija računovodstva za naplative projekte
description: U ovoj temi nalaze se informacije o računovodstvenim mogućnostima za naplative projekte.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 47bb5671c7b80c0e96f3f65e9c4d25f6da8184a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131964"
---
# <a name="configure-accounting-for-billable-projects"></a>Konfiguracija računovodstva za naplative projekte

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dynamics 365 Project Operations podržava razne mogućnosti računovodstva za naplative projekte koji uključuju vrijeme i materijal te transakcije s nepromjenjivom cijenom.

- **Vremenske i materijalne transakcije**: Ove transakcije fakturiraju se tijekom rada na temelju potrošnje sati, troškova, predmeta ili naknada na projektu. Ovi transakcijski troškovi mogu se uskladiti s prihodom od svake transakcije, a projekt se fakturira tijekom rada. Prihod od projekta također može biti obračunan u trenutku kada se transakcija dogodi. Tijekom fakturiranja prihod se priznaje i, ako je primjenjivo, obračunani se prihod stornira.
- **Transakcije s nepromjenjivom cijenom**: Te se transakcije fakturiraju prema rasporedu naplate koji se temelji na ugovoru o projektu. Prihod za transakcije s nepromjenjivom cijenom može se priznati na fakturiranju ili izračunati i knjižiti periodično, u skladu s načinom **Završen ugovor** ili **Postotak dovršenosti**.

Projekt se smatra naplativim kad je povezan s jednim ili više redaka ugovora. Redak ugovora o projektu sam definira dozvoljene načine naplate i vrste transakcija.

Kao primjer, Fabrikam Robotics dobio je ugovor o projektu s korporacijom Adatum za optimizaciju opreme. Adatum će platiti fiksni iznos od 10.000 USD za pokriće nastalih troškova projekta. Ovdje se radi o načinu naplate nepromjenjive cijene Vrijeme i naknade za projekt naplatit će se prema uporabi. Ovdje se radi o načinu naplate vremena i materijala. Sav posao pratit će se u okviru jednog projekta nazvanog optimizacija opreme Adatum.

Član projektnog tima prijavljuje osam sati rada na projektu optimizacije opreme Adatum. Kada voditelj projekta odobri ovo vrijeme, sustav upotrebljava način naplate vremena i materijala za stvaranje stvarnih transakcija, fakture i računa. Ova transakcija neće biti uključena u izračun procjene prihoda s nepromjenjivom cijenom.

Drugi član projektnog tima prijavljuje putni trošak od 2.000,00 USD na projektu optimizacije opreme Adatum. Kada voditelj projekta odobri ovu prijavu, sustav upotrebljava način naplate prema nepromjenjivoj cijeni za stvaranje stvarnih transakcija i računa za ovaj trošak na projektu. Klijentu se neće fakturirati na temelju ove transakcije. Umjesto toga, fakturirat će im se s pomoću zasebno konfiguriranih kontrolnih točaka u naplati. Ova transakcija troška, zajedno s procjenama troškova, uključit će se u izračun procjene prihoda s nepromjenjivom cijenom.

Računovodstvena načela za projektne transakcije definirana su u profilima troškova i prihoda projekta. Za svaku projektnu transakciju sustav određuje odgovarajući profil troškova i prihoda projekta s pomoću konfiguriranih pravila za profil troškova i prihoda projekta.

## <a name="define-project-cost-and-revenue-profiles"></a>Definiranje profila troška i prihoda projekta 

Profili troškova i prihoda projekta određuju računovodstvena pravila za projektne transakcije. Ti su profili konfigurirani u Upravljanju projektima i računovodstvu. 

Izvršite sljedeće korake za stvaranje novog profila troškova i prihoda projekta. 

1. Idite na **Upravljanje projektima i računovodstvo** > **Postavljanje** > **Knjiženje** > **Profil troškova i prihoda projekta**. 
2. Odaberite **Novo** za stvaranje novog profila troškova i prihoda projekta.
3. U polje **Naziv** unesite naziv i kratki opis profila.
4. U polju **Način naplate** odaberite **Vrijeme i materijal** ili **Nepromjenjiva cijena**.
5. Proširite Brzu karticu **Glavne knjige**. Polja na ovoj kartici definiraju računovodstvena načela koja se upotrebljavaju kada se projektne transakcije unose u temeljnicu s pomoću temeljnice integracije aplikacije Project Operations, a zatim fakturiraju putem prijedloga fakture za projekt.
6. Odaberite odgovarajuće podatke u sljedećim poljima u Brzoj kartici stavke **Glavna knjiga**:

    - **Knjiženje troškova – sat**:

       - *Bez glavne knjige*: Troškovi vremenskih transakcija neće se knjižiti u glavnu knjigu kada se knjiži temeljnica integracije u aplikaciji Project Operations. Međutim, računovođa može naknadno knjižiti troškove s pomoću funkcije Knjiži troškove.
       - **Saldo**: Trošak vremenskih transakcija teretit će se vrstom računa glavne knjige, *WIP – Vrijednost troška* i pripisati *Računu za raspodjelu plaća* u postavci knjiženja glavne knjige. Računovođa će upotrijebiti funkciju knjiženja troškova kako bi taj trošak povremeno premještao s računa salda na račun dobiti i gubitka.
       - **Dobit i gubitak**: Tijekom knjiženja temeljnice integracije aplikacije Project Operations, trošak vremenske transakcije teretit će se vrstom računa glavne knjige *Trošak* i pripisati *Računu za raspodjelu plaća* definiranom na kartici **Trošak** na stranici **Postavljanje knjiženja glavne knjige** (**Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Knjiženje** \> **Postavljanje knjiženja glavne knjige**). Ovo je najčešće postavljanje vremenskih i materijalnih transakcija.
        - *Bez glavne knjige*: Troškovi vremenskih transakcija nikada neće biti knjiženi u glavnu knjigu.

    - **Knjiženje troškova – trošak**:

         - **Saldo**: Tijekom knjiženja temeljnice integracije aplikacije Project Operations, trošak transakcije izdatka tereti se vrstom računa glavne knjige *WIP – Vrijednost troška* kako je definirano na kartici **Trošak** na stranici **Postavljanje knjiženja glavne knjige** i pripisuje se računu za poravnanje u retku temeljnice. Zadani računi za naknadu troškova definirani su u postavci **Upravljanje projektima i računovodstvo** > **Postavljanje** \> **Knjiženje** \> **Zadani račun poravnanja za troškove**. Računovođa će upotrijebiti funkciju **Knjiži troškove** kako bi taj trošak povremeno premještao s računa salda na račun dobiti i gubitka.
        - **Dobit i gubitak**: Tijekom knjiženja temeljnice integracije aplikacije Project Operations, trošak transakcije izdatka tereti se vrstom računa glavne knjige *Trošak* kako je definirano na kartici **Trošak** na stranici **Postavljanje knjiženja glavne knjige** i pripisuje se računu za poravnanje u retku temeljnice. Zadani računi za naknadu troškova definirani su u postavci **Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Knjiženje** \> **Zadani račun poravnanja za troškove**.
       
    - **Fakturiranje na računu**:

        - **Saldo**: Tijekom knjiženja prijedloga fakture za projekt, djelomična transakcija (kontrolna točka za naplatu) pripisuje se vrsti računa glavne knjige *WIP fakturiran – djelomično* kako je definirano na kartici **Prihod** na stranici **Postavljanje knjiženja glavne knjige** i tereti račun salda klijenta.
         - **Dobit i gubitak**: Tijekom knjiženja prijedloga fakture za projekt, djelomična transakcija (kontrolna točka za naplatu) pripisuje se vrsti računa glavne knjige *Fakturirani prihod – djelomično* kako je definirano na kartici **Prihod** na stranici **Postavljanje knjiženja glavne knjige** i tereti račun salda klijenta. Računi salda klijenta definirani su u stavci **Potraživanja** \> **Postavljanje** \> **Profili knjiženja klijenta**.

   Kada definirate profile knjiženja za načine naplate vremena i materijala, imate mogućnost obračunati prihod po vrsti transakcije (sat, trošak i naknada). Ako je mogućnost **Obračunani prihod** postavljena na **Da**, nefakturirane prodajne transakcije u temeljnici integracije aplikacije Project Operations evidentirat će se u glavnu knjigu. Prodajna vrijednost tereti se stavkom **WIP – račun vrijednosti prodaje** i pripisuje se računu **Obračunani prihod – prodajna vrijednost** koji je postavljen na stranici **Postavljanje knjiženja glavne knjige** na kartici **Prihod**. 
  
  > [!NOTE]
  > Mogućnost **Obračunani prihod** dostupan je samo kada se odgovarajuća vrsta transakcije **Trošak** knjiži na račun dobiti i gubitka.
    
7. Proširite Brzu karticu **Procijeni**. Polja na ovoj kartici definiraju postavke izračuna za procjene prihoda s nepromjenjivom cijenom. Polja na ovoj kartici odnose se samo na profile troškova i prihoda projekta s načinom naplate **Nepromjenjiva cijena**.
8. Odaberite odgovarajuće podatke u sljedećim poljima u Brzoj kartici mogućnosti **Procijeni**:

    - **Načelo upotrijebljeno za izračun završetka projekta**:

        - **Završen ugovor**: Usklađivanje troškova i priznavanje prihoda ne događa se do kraja projekta. Troškovi se do završetka projekta u saldu odražavaju kao WIP.
        - **Postotak dovršenosti**: Obračunani prihod izračunava se i knjiži u glavnu knjigu svakog razdoblja na temelju postotka dovršenosti projekta. Dostupno je više načina za izračunavanje postotka dovršenosti. Ti načini mogu biti automatski na osnovi konfiguracije ili ručni.
        - **Bez WIP-a**: Ova postavka upotrebljava se za projekte s nepromjenjivom cijenom i kratkim vremenskim rasponom te tamo gdje se faktura i troškovi javljaju u istom razdoblju. U tom slučaju vrijednost polja **Djelomično fakturiranje** na Brzoj kartici **Glavna knjiga** automatski se postavlja na **Dobit i gubitak** kako bi se osiguralo da se prihod prizna pri fakturiranju. Postupak procjene prihoda neće se upotrebljavati za profil troška i prihoda tog projekta.

    - **Načela podudaranja**: Ovo polje određuje kako će se izračunana prodajna vrijednost  (obračunani prihod) knjižiti u glavnu knjigu.

        - Uporabom načela **Prodajna vrijednost** sustav će izračunati prodajnu vrijednost podudaranjem troškova i prihoda, a zatim će ih knjižiti kao jedan iznos.
        - Uporabom načela **Proizvodnja i dobit** sustav će prodajnu vrijednost podijeliti na ostvarene troškove i izračunanu dobit. Oni se knjiže zasebno.

    - **Predlošci troškova**: Dozvolite grupiranje projektnih transakcija na temelju vrste transakcije i kategorije projekta te za ove grupe definirajte pravila izračuna postotka dovršenosti.
    - **Šifre razdoblja**: Definirajte učestalost izračunavanja procjene prihoda za određeni profil troška i prihoda projekta.
    - **Kategorije za procjenu**: Upotrebljava se za knjiženje vrijednosti prodaje (obračunani prihod) u projektne transakcije. Prvo konfigurirajte namjensku kategoriju projekta za vrstu transakcije **Naknada**, a zatim postavite zastavicu, **Procjeni** za ovu kategoriju projekata. Nadalje, ovisno o odabranom načelu podudaranja, odaberite ovu kategoriju projekta u vrijednosti **Prodaja** ili polju **Dobit** u profilu troškova i prihoda projekta.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Uzorci konfiguracija za profile troškova i prihoda projekta

Vrijeme i materijali – bez WIP-a

![Profil troškova i prihoda: Vrijeme i materijali – bez WIP-a](media/time-material-no-wip.png)

Vrijeme i materijali – WIP (prihod)

![Profil troškova i prihoda: Vrijeme i materijali – WIP](media/time-material-with-wip.png)

Nepromjenjiva cijena – bez WIP-a

![Profil troška i prihoda: Nepromjenjiva cijena – bez WIP-a](media/fixed-price-no-wip.png)

Nepromjenjiva cijena – završeni ugovor

![Profil troška i prihoda: Nepromjenjiva cijena – završeni ugovor](media/fixed-price-completed-contract.png)

Nepromjenjiva cijena – postotak dovršenosti

![Profil troška i prihoda: Nepromjenjiva cijena – postotak dovršenosti](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Primjeri računovodstvenih događaja za uzorak profila troška i prihoda projekta.

| Računovodstveni događaj                  | Vrijeme i materijal – bez WIP-a                       | Vrijeme i materijal – WIP                                                                                           | Nepromjenjiva cijena – bez WIP-a                                            | Nepromjenjiva cijena – Završeni ugovor                                                                            | Nepromjenjiva cijena – postotak dovršenosti                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Vremenske transakcije temeljnice    | Terećenje – trošak <br>Kredit – raspodjela plaća          | Terećenje – trošak <br>Kredit – raspodjela plaća <br>Terećenje – WIP prodajna vrijednost <br>Kredit - prodajna vrijednost  obračunanih prihoda                | Terećenje – trošak <br>Kredit – raspodjela plaća                         | Terećenje – trošak <br>Kredit – raspodjela plaća                                                                    | Terećenje – trošak <br>Kredit – raspodjela plaća                       |
| Transakcije troškova temeljnice | Terećenje – trošak <br>Kredit – račun poravnanja za troškove | Terećenje – trošak <br>Kredit – račun poravnanja za troškove <br>Terećenje – WIP prodajna vrijednost <br>Kredit - prodajna vrijednost  obračunanih prihoda      | Terećenje – trošak <br>Kredit – račun poravnanja za troškove                 | Terećenje – trošak<br> Kredit – račun poravnanja za troškove                                                            | Terećenje – trošak <br>Kredit – račun poravnanja za troškove               |
| Fakturiranje klijentu                | Terećenje – Saldo klijenta <br>Kredit – fakturirani prihod | Terećenje – Saldo klijenta <br>Kredit – fakturirani prihod <br>Kredit – prodajna vrijednost WIP-a Terećenje – prodajna vrijednost obračunane dobiti | Terećenje – Saldo klijenta <br>Kredit – fakturirani prihod – djelomično | Terećenje – Saldo klijenta <br>Kredit – WIP – djelomično fakturirano                                                  | Terećenje – Saldo klijenta <br>Kredit – WIP – djelomično fakturirano    |
| Procjena proknjiženog prihoda             | Nije primjenjivo                                   | Nije primjenjivo                                                                                                    | Nije primjenjivo                                                  | Terećenje – vrijednost troškova WIP-a <br>Kredit – trošak                                                                         | Terećenje – WIP – prodajna vrijednost <br>Kredit – prodajna vrijednost  obračunanog prihoda |
| Ukloni                         | Nije primjenjivo                                   | Nije primjenjivo                                                                                                    | Nije primjenjivo                                                  | Terećenje – vrijednost troškova WIP-a <br>Terećenje – trošak <br>Kredit – obračunani prihod – prodajna vrijednost  <br>Kredit – WIP djelomično fakturirano | Kredit – WIP – djelomično fakturirano <br>Kredit – WIP prodajna vrijednost     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Konfiguracija pravila profila troška i prihoda projekta

Pravila profila troškova i prihoda projekta određuju profil troškova i prihoda projekta koji se moraju upotrebljavati tijekom obrade svih naplativih projektnih transakcija. Definirajte pravila odlaskom na postavku **Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Knjiženje** \> **Pravila profila troškova i prihoda projekta**.

Pravila se mogu definirati ugovorom o projektu, projektnom grupom ili putem određenog projekta. Sustav će uvijek prvo odabrati najpodrobnije pravilo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]