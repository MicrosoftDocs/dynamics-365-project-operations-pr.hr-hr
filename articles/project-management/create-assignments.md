---
title: Stvaranje dodjela resursa
description: U ovom se članku navode informacije o izradi generičkih i imenovanih dodjela resursa.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811984"
---
# <a name="create-resource-assignments"></a>Stvaranje dodjela resursa

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_


Dodjela resursa izravna je povezanost člana projektnog tima sa zadatkom lisnog čvora. U ovom se članku navode informacije o različitim načinima za dodjelu resursa.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Izrada generičkog člana tima putem dodjele zadatka


Kada stvarate generičkog člana tima putem dodjele zadatka, stvarate rezervirano mjesto ili generički resurs. Ovaj generički resurs opisuje karakteristike imenovanog resursa na kojem u konačnici želite raditi na zadacima. Zatim generirate zahtjev ili pošaljete zahtjev pomoću zahtjeva koji se koristi za traženje i rezerviranje imenovanog resursa.

1. Na rešetki Raspored za zadatak, odaberite ikonu Resurs u ćeliji **Resurs**.
2. Upišite naziv koji će služiti kao naziv resursa rezerviranog mjesta. Na primjer, upravitelj programa.
3. Odaberite **Izradi** i u polju **Brza izrada projektnog člana tima** postavite ulogu za generički resurs.
4. Prema potrebi, dodijelite zadatke tom resursu rezerviranog mjesta odabirom resursa na **Biraču resursa** za taj zadatak. Resursi navedeni pod stavkom **Članovi tima**.
5. Kada završite s dodjelom generičkog resursa, na **kartici Tim** odaberite generički resurs, a zatim odaberite **Generiraj zahtjev da biste stvorili zahtjev resursa** za generički resurs.
6. Odaberite **Rezerviraj** za generički resurs, a zatim možete upotrijebiti ploču s rasporedom za pronalaženje i rezerviranje stvarnog resursa. Možete poslati i zahtjev za ispunjenje od strane upravitelja resursa.
7. Kada je generički resurs u potpunosti ispunjen imenovanim resursom, generički resurs se uklanja iz tima. (Djelomično ispunjavanje zahtjeva za resursima neće rezultirati dodjelom resursa.) Dodjele zadataka za generički resurs dodijeljene su imenovanom resursu koji je ispunio zahtjev resursa generičkog resursa.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Dodijeli imenovani resurs s popisa svih resursa koje je moguće rezervirati

Možete upotrijebiti okvir za pretraživanje u **Biraču resursa** za pretraživanje svih aktivnih resursa koje je moguće rezervirati i dodijeliti ih svakom zadatku lisnog čvora. Resursi dodijeljeni na taj način dodaju se timu bez rezervacija. To je slično dodavanju člana tima i odabiru mogućnosti **Nijedan** kao načina dodjele. Resurs se prikazuje na karticama **Tim**, **Dodjela resursa** i **Usklađivanje** kao resursi koji imaju samo zadatke i manjak rezervacija. Rezervirajte ih ako želite da iskoristite njihovu dostupnost.

1. Iz rešetke zadatka, ploče ili vremenske trake pomaknite se na stranicu **Dodijeljeno za**.
2. U okvir za pretraživanje počnite upisivati naziv. Rezultati pretraživanja za naziv prikazuju se u **Biraču resursa** pod stavkom **Ostali resursi**.
3. Odaberite resurs koji želite dodijeliti zadatku ili odaberite naziv resursa pod stavkom **Ostali resursi tima**.

## <a name="editing-resource-assignment-contours"></a>Uređivanje kontura za dodjelu resursa

Prema zadanim postavkama, kada su resursi dodijeljeni zadatku u rasporedu, njihov se napor linearno distribuira svakom resursu, na temelju radnog vremena tog resursa i načina rasporeda projekta. Voditelj projekta može koristiti mrežu dodjele resursa za sužavanje procjena napora svakog resursa koji je dodijeljen jednom ili više zadataka u različitim vremenskim skalama. Ova značajka pomaže voditeljima projekata da proizvedu točnije procjene troškova i prodaje, koje su potaknute konturama dodjele resursa koje se generiraju kada je resurs dodijeljen zadatku. Osim toga, voditelji projekata mogu lakše odražavati potražnju resursa koja je potrebna za izgradnju potražnje u zahtjevu za resursima.

### <a name="navigation"></a>Kretanje

Da bi pristupio rešetki za uređivanje kontura, voditelj projekta najprije odabire karticu **Zadaci** na glavnoj stranici projekta, a zatim karticu **Dodjele** .

![Kartica Dodjele na kartici Zadaci glavne stranice projekta.](media/AssignmentGrid.png)

Rešetka podržava dvije metode grupiranja: **grupiranje po resursu** i **grupiranje po zadatku**. Za razliku od prikaza rešetke, stupci se ne mogu konfigurirati. Dodijeljeni su jedini vidljivi stupci,Naziv zadatka,Početak **·** **dodjele,** Završetak **dodjele i** Napor dodjele. **·** **·**

Kada je rešetka u početku prikazana, počinje od najranije konture zadatka. Ako vaš raspored ne sadrži zadatke koji se trude, mreža će biti prazna i neće ništa prikazati.

![Prazna rešetka dodjele.](media/emptyassignmentgrid.png)

Ako želite pregledati konture i različite vremenske skale, dostupna je i rešetka dodjele resursa samo za čitanje i mreža usklađivanja resursa.

### <a name="resource-calendars"></a>Kalendari resursa

Mogućnost uređivanja konture za određeni dan regulirana je radnim danima resursa, što se odražava u njihovom kalendaru. Ako je ćelija onemogućena za određeni resurs, taj resurs nema radne dane tijekom tog razdoblja.

Konture resursa mogu se proširiti izvan trenutnog datuma početka i završetka dodijeljenog zadatka. Ako se kontura ažurira tako da je nakon posljednjeg datuma završetka zadatka ili najranijeg datuma početka zadatka, datum završetka zadatka ili datum početka zadatka promijenit će se prema potrebi. Međutim, ako se kontura ažurira tako da je ranija od datuma početka zadatka koji je povezan s prethodnikom, ažuriranje neće uspjeti jer će dodjela pokrenuti zadatak prije dovršetka prethodnika, a to ponašanje trenutno nije podržano.

### <a name="co-authoring"></a>Koautorstvo

Promjene u rešetki dodjele resursa automatski se odražavaju u svim pridruženim prikazima, uključujući prikaze grafikona, vremenske trake, ploče i rešetke. Ako više korisnika istovremeno pregledava projekt, sve promjene koje jedan korisnik napravi odrazit će se na mrežu. S druge strane, sve promjene napravljene u rešetki dodjele resursa prikazat će se svim ostalim korisnicima koji gledaju projekt u istoj sesiji.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
