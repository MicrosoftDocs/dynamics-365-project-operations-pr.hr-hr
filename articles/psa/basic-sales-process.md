---
title: Prodajni procesi
description: Ova tema pruža informacije o osnovnim prodajnim procesima.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: ad32757821a4cf966abd0b98cc4632dece613bc4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291070"
---
# <a name="sales-processes"></a>Prodajni procesi

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Prodajni procesi koji se koriste u organizaciji koja se temelji na projektu razlikuju se od prodajnih procesa koji se koriste u organizaciji koja se temelji na proizvodu. Ta se razlika pojavljuje jer su prodajni ciklusi za organizacije koje se temeljene na projektima dulji i zahtijevaju prilagođene tehnike procjene za analizu i izradu ponuda za svaki dogovor. Dynamics 365 Project Service Automation koristi neke od iste funkcionalnosti koje se koriste u prodajnom procesu za Dynamics 365 Sales. Evo nekoliko primjera:

- Entitet potencijalnog klijenta koristi se za praćenje prodajnog procesa.
- Kvalificirani potencijalni klijenti prate se kao prilike. Prodajni proces također može započeti s prilikom.
- Pristupa se svim povezanim artefaktima za priliku. Ti artefakti uključuju prodajni tim, dionike, vjerojatnost, ocjenu, faze prodaje i poslovne procese.
- Za priliku se izrađuje više ponuda.
- Ponuda se označava kao **Zatvorena kao osvojena** za izradu prodajnog naloga. U PSA, prodajni nalog prilagođen je i zove se ugovor o projektu.

Sljedeća ilustracija prikazuje tipičan prodajni proces u organizaciji koja se temelji na projektu.

> ![Prodajni proces u organizaciji koja se temelji na projektu](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Procjena prodaje
Vrijednost prodaje može se procijeniti na temelju projekata koji su prethodno bili isporučeni i složenosti projekata. Za projekte koji uključuju proširenja na prethodne projekte ili projekte u kojima je stručno znanje dobavljača visoko i gdje se koriste dobro poznati radni predlošci, možete koristiti jednostavniji proces procjene. Složeniji projekti obično imaju dulji postupak kupnje. Stoga postoji više faza u procesu procjene prodaje. U ranoj fazi, prodajni tim koristi unos upravitelja računa i stručnjaka za predmet (MSP) da bi počeo izrađivati procjenu visoke razine za svaku različitu komponentu rada koji se navodi u ponudi. Ove komponente rada predstavljene su recima ponude. 

Možete izraditi procjenu visoke razine ponude. Na kraju, ovu procjenu visoke razine zamijenit će detaljnija procjena koja se temelji na projektnom planu koju izrađujete s pomoću standardiziranih predložaka projekta. Ti predlošci pomažu kod izrade rasporeda i određivanja monetarnih vrijednosti u ponudi i njezinim komponentama (recima ponude). 

Možete izraditi više ponuda za projekt i grupirati ih pod vrstom entiteta pojedinačne prilike. Naposljetku se jedna od tih ponuda označava kao **Zatvorena kao osvojena**, a izrađuje se ugovor projekta ili izjava o radu (SOW). Ugovor projekta sadrži ugovorenu vrijednost za svaku komponentu (redak ugovora) koju klijent prihvaća za isporuku. SOW se obično izrađuje kao Microsoft Word dokument. Sve fakture koje se šalju klijentu tijekom isporuke projekta, upućuju na ugovor projekta ili izjavu o radu.

Možete izraditi i alternativne ponude pod jednom vrstom entiteta prilike ili postaviti sustav tako da se ugovor projekta izradi kada se osvoji ponuda. U tom slučaju možete Wordov dokument koji predstavlja SOW priložiti zapisu ugovora projekta.

![Zatvaranje ponude za izradu ugovora projekta](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Konfiguriranje prodajnog procesa
Možete koristiti tijekove poslovnih procesa (BPFs) u Microsoft Dynamics 365 da biste konfigurirali svoj prodajni proces. Tijekovi poslovnih procesa daju vašem prodajnom osoblju vođeno vizualno sučelje koje mogu koristiti za vođenje dogovora kroz faze koje su uobičajene za vaše poduzeće.

Na primjer, vaše poduzeće može imati sljedećih šest faza u prodajnom procesu:

1. Kvalifikacija
2. Procjena
3. Interna revizija
4. Ugovor
5. Dostavi
6. Zatvori

Tih šest faza predstavljaju ševroni (\>) koje odaberete za proširenje u svakoj vrsti entiteta prilike koji izradite.

![Konfiguracija poslovnog procesa u sustavu Dynamics 365](media/basic-guide-3.png)
 
Vaša organizacija može koristiti različite entitete da bi predstavljala isti dogovor kako se ona razvija. Početkom prodajnog procesa ugovor predstavlja entitet Prilika. Kako vrijeme prolazi i pojavljuje se više detalja, možda ćete koristiti procjene visoke razine za izradu jedne ili više ponuda. Ako se jedna od tih ponuda revidira od strane internih dionika i klijenata dionika, entitet Ponuda predstavlja dogovor. Nakon što klijent prihvati ponudu, ugovor projekta ili SOW predstavlja dogovor. Da biste podržali to ponašanje, BPFs strukturirani su tako da je svaka faza u procesu povezana s drugom tablicom baze podataka.

Fazu **Kvalificiranje** u prodajnom procesu može poduprijeti entitet Prilika. Faze **Procjene** i **Interne revizije** može poduprijeti entitet Ponuda. Faze **Ugovor**, **Isporuka** i **Zatvori** može poduprijeti entitet Ugovor projekta.

Dok vodite dogovore kroz faze, od vas će se zatražiti da izradite odgovarajući zapis entiteta za pomoć pri vođenju kroz proces. Faze mogu biti uvjetovane. Na primjer, ako vam je potrebna interna revizija ponude samo ako ponuda koristi prilagođeni cjenik, možete konfigurirati taj uvjet u odgovarajućoj fazi poslovnog procesa. Faza **Interna revizija** zatim se prikazuje samo za ponude koje koriste prilagođeni cjenik. Za sve ostale ugovore i ponude, fazu **Procjena** slijedi faza **Ugovor**.

> [!NOTE]
> PSA ima određene stranice za entitete Prilika, Ponuda, Narudžba i Faktura. Za te entitete morate izraditi prilike, ponude, narudžbe i fakture za projektne usluge s pomoću stranica s informacijama o projektu. Ako koristite drugu stranicu za izradu zapisa, nećete moći otvoriti zapis sa stranice **Informacije o projektu**. Ako želite otvoriti zapis sa stranice **Informacije o projektu**, morate izbrisati zapis i ponovno ga izraditi s pomoću stranice **Informacije o projektu**. Na stranici **Informacije o projektu**, poslovna logika za svaku od tih vrsta entiteta osigurava ispravno postavljanje polja **Vrste** zapisa i pravilnu inicijalizaciju svih obaveznih pojmova.

> ![Informacije o projektu za novu narudžbu](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Razlike između Project Service Automation i Prodaje
Iako prodajni proces u sustavu PSA koristi osnovne mogućnosti prodajnog procesa u Prodaji, on ima neke ključne razlike zbog varijacija u poslovnim praksama organizacija koje se temelje na projektu. Evo nekoliko primjera:

- **Ponude projekta** – u sustavu Project Service Automation, ponuda se zatvara nakon izrade ugovora projekta iz ponude. U Prodaji možete držati ponudu otvorenom nakon što je osvojite. Razlog za tu razliku je da je podudaranje između ponude i ugovora projekta bolje za organizacije koje se temelje na projektu. 
- **Aktivacija i revizije** – u sustavu PSA, aktivacija i revizije nisu podržane za ponude projekta. U Prodaji, ponuda se može zaključati da bi se spriječila dodatna uređivanja.
- **Zatvaranje ponude kao izgubljene ili osvojene** – u sustavu PSA, kada je ponuda projekta zatvorena kao osvojena ili izgubljena, prilika ostaje otvorena. Sve ostale ponude na prilici zatvorene su kao izgubljene. U Prodaji, kada je ponuda zatvorena kao osvojena ili izgubljena, od korisnika se traži da poduzme radnju u prilici. Ovisno o unosu korisnika, moguće je priliku zatvoriti ili ostaviti otvorenu.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Praćenje revizija ponuda i projektnih planova u prodajnom ciklusu
U sustavu PSA, ne možete pratiti revizije koje se provode na ponudi. Umjesto toga morate označiti postojeću ponudu **Zatvorena kao izgubljena**, a zatim izraditi novu ponudu. Možete kopirati ponudu ili klonirati ponudu koja se temelji na projektu s pomoću PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Praćenje komentara i odobrenja ponuda i ugovora projekta
Možete upravljati pregledom i odobrenjem ponuda i ugovora projekta s pomoću zida zapisa i objava. Vaša organizacija može izraditi prilagođene tijekove rada i dodatke za dodjelu, preusmjeravanje, eskalaciju i upravljanje obavijestima o radnim stavkama pregleda i odobravanja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]