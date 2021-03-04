---
title: Pregled prodajnog postupka
description: Ova tema pruža informacije o osnovnim prodajnim procesima.
author: rumant
manager: Annbe
ms.date: 10/29/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5da29d2959a6e49defa185630f45d280dba283c4
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177592"
---
# <a name="sales-process-overview"></a>Pregled prodajnog postupka

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Prodajni procesi koji se koriste u organizaciji koja se temelji na projektu razlikuju se od prodajnih procesa koji se koriste u organizaciji koja se temelji na proizvodu. To je zbog toga što su prodajni ciklusi za tvrtke ili ustanove koje se temeljene na projektima dulji i zahtijevaju prilagođene tehnike procjene za analizu i izradu ponuda za svaki dogovor. Dynamics 365 Project Operations upotrebljava neke od sljedećih funkcionalnosti koje se upotrebljavaju u prodajnom postupku:

- Zapis potencijalnog klijenta upotrebljava se za praćenje prodajnog postupka.
- Kvalificirani potencijalni klijenti prate se kao prilike.
- Dostupni su svi povezani artefakti za priliku. Ti artefakti uključuju prodajni tim, dionike, vjerojatnost, ocjenu, faze prodaje i poslovne procese.
- Za priliku se izrađuje više ponuda.
- Ponudi se daje status **Zatvorena kao osvojena** za stvaranje prodajnog naloga. U aplikaciji Project Operations prodajni je nalog prilagođen i naziva se ugovor o projektu.

## <a name="estimate-a-sale"></a>Procjena prodaje
Vrijednost prodaje može se procijeniti na temelju projekata koji su prethodno bili isporučeni i složenosti projekata. Za projekte koji uključuju proširenja na prethodne projekte ili projekte u kojima je stručno znanje dobavljača visoko i gdje se koriste dobro poznati radni predlošci, možete koristiti jednostavniji proces procjene. Složeniji projekti obično imaju dulji postupak kupnje. Stoga postoji više faza u procesu procjene prodaje. U ranoj fazi postupka, prodajni tim upotrebljava unos upravitelja računa i stručnjaka za predmet (SME, subject matter expert) kako bi stvarao procjenu visoke razine za svaku različitu komponentu rada koja se navodi u ponudi. Ove komponente rada predstavljene su recima ponude. 

Možete izraditi procjenu visoke razine ponude. Na kraju, ovu procjenu visoke razine zamijenit će detaljnija procjena koja se temelji na projektnom planu koju izrađujete s pomoću standardiziranih predložaka projekta. Ti predlošci pomažu kod izrade rasporeda i određivanja monetarnih vrijednosti u ponudi i njezinim komponentama (recima ponude). 

Možete stvoriti više ponuda za projekt i grupirati ih pod zapisom pojedinačne prilike. Naposljetku se jedna od ponuda označava kao **Zatvorena kao osvojena**, a izrađuje se ugovor projekta ili izjava o radu (SOW, statement of work). Ugovor projekta sadrži ugovorenu vrijednost za svaku komponentu (redak ugovora) koju klijent prihvaća za isporuku. SOW se obično izrađuje kao Microsoft Word dokument. Sve fakture koje se šalju klijentu tijekom isporuke projekta, upućuju na ugovor projekta ili izjavu o radu.

Možete stvoriti i alternativne ponude pod jednim zapisom prilike ili postaviti sustav tako da se ugovor projekta stvori kada se osvoji ponuda. U tom slučaju možete Wordov dokument koji predstavlja SOW priložiti zapisu ugovora projekta.

## <a name="configure-the-sales-process"></a>Konfiguriranje prodajnog postupka
Možete upotrijebiti tijekove poslovnih procesa kako biste konfigurirali svoj prodajni postupak. Ti tijekovi pružaju vođeno vizualno sučelje za pomicanje poslova naprijed kroz faze prodajnog postupka.

Na primjer, vaše poduzeće može imati sljedećih šest faza u prodajnom procesu:

1. Kvalificiraj
2. Procjena
3. Interna revizija
4. Ugovor
5. Dostavi
6. Zatvaranje
 
Vaša organizacija može koristiti različite entitete da bi predstavljala isti dogovor kako se ona razvija. Početkom prodajnog procesa ugovor predstavlja entitet Prilika. Kako vrijeme prolazi i pojavljuje se više detalja, možda ćete koristiti procjene visoke razine za izradu jedne ili više ponuda. Ako se jedna od tih ponuda revidira od strane internih dionika i klijenata dionika, entitet Ponuda predstavlja dogovor. Nakon što klijent prihvati ponudu, ugovor projekta ili SOW predstavlja dogovor. Da biste podržali to ponašanje, BPFs strukturirani su tako da je svaka faza u procesu povezana s drugom tablicom baze podataka.

Fazu **Kvalificiranje** u prodajnom procesu može poduprijeti entitet Prilika. Faze **Procjene** i **Interne revizije** može poduprijeti entitet Ponuda. Faze **Ugovor**, **Isporuka** i **Zatvori** može poduprijeti entitet Ugovor projekta.

Dok vodite dogovore kroz faze, od vas će se zatražiti da izradite odgovarajući zapis entiteta za pomoć pri vođenju kroz proces. Faze mogu biti uvjetovane. Na primjer, ako vam je potrebna interna revizija ponude samo ako ponuda koristi prilagođeni cjenik, možete konfigurirati taj uvjet u odgovarajućoj fazi poslovnog procesa. Faza **Interna revizija** zatim se prikazuje samo za ponude koje koriste prilagođeni cjenik. Za sve ostale ugovore i ponude, fazu **Procjena** slijedi faza **Ugovor**.

> [!NOTE]
> Project Operations ima određene stranice za zapise entiteta Prilika, Ponuda, Narudžba i Faktura. Za te entitete te zapise morate stvoriti s pomoću stranica s informacijama o projektu. U suprotnom, nećete moći otvoriti zapise sa stranice **Informacije o projektu**. Ako želite otvoriti zapis sa stranice **Informacije o projektu**, morate izbrisati zapis i ponovo ga stvoriti s pomoću stranice **Informacije o projektu** na kojoj poslovna logika za svaku od ovih vrsta entiteta osigurava da je polje zapisa **Vrsta** postavljeno ispravno i da su svi obvezni koncepti pravilno pokrenuti.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Praćenje revizija ponuda i projektnih planova u prodajnom ciklusu
U aplikaciji Project Operations ne možete pratiti revizije koje se provode na ponudi. Umjesto toga morate označiti postojeću ponudu **Zatvorena kao izgubljena**, a zatim izraditi novu ponudu. Možete kopirati ponudu ili klonirati ponudu koja se temelji na projektu.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Praćenje komentara i odobrenja ponuda i ugovora o projektu
Možete upravljati pregledom i odobrenjem ponuda i ugovora projekta s pomoću zida zapisa i objava. Vaša tvrtka ili ustanova može izraditi prilagođene tijekove rada i dodatke za dodjelu, preusmjeravanje, eskalaciju i upravljanje obavijestima o radnim stavkama pregleda i odobravanja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]