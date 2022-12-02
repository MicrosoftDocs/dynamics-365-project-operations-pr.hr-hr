---
title: Kontrolne točke retka podugovora
description: U ovom članku objašnjava se način stvaranja i održavanja rasporeda faktura koji se temelji na kontrolnim točkama za podugovor s dobavljačem.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 431a57adf82c79f72d44886636183d48e0931f53
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522410"
---
# <a name="subcontract-line-milestones"></a>Kontrolne točke retka podugovora

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U aplikaciji Dynamics 365 Project Operations, redak podugovora s načinom naplate po fiksnoj cijeni može odrediti raspored faktura koji se temelji na kontrolnim točkama s pomoću dobavljača.

Kontrolne točke za fakturiranje dobavljača mogu se generirati automatski s pomoću zadane učestalosti ili ih možete stvoriti ručno.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Automatsko stvaranje rasporeda faktura za redak podugovora na temelju kontrolnih točaka

Kako biste automatski generirali raspored faktura koji se temelji na kontrolnim točkama za fiksni skup jednako raspoređenih kontrolnih točaka, poduzmite sljedeće korake.

1. Idite na **Postavke** > **Učestalosti faktura** i postaviti učestalost faktura za retke podugovora.
2. Otvorite stranicu **Podugovori**, otvorite podugovor na kojem želite raditi, a zatim otvorite redak podugovora s fiksnom cijenom za koji ćete stvoriti raspored kontrolnih točaka.
3. Na kartici **Kontrolne točke retka podugovora** odaberite **Generiraj povremene kontrolne točke**.
4. U dijaloški okvir unesite ili odaberite datumski raspon, broj kontrolnih točaka i učestalost faktura. Možete odabrati datum početka, ili broj kontrolnih točaka i učestalost faktura ili datum početka, ili možete odabrati datum završetka i učestalost faktura. Ne možete odabrati datum završetka i broj kontrolnih točaka.
S pomoću ovih podataka, sustav generira kontrolne točke i zapise koji se prikazuju u rešetki **Kontrolne točke**.

   - **Naziv kontrolne točke** – Naziv kontrolne točke postavljen je na datum kontrolne točke koji se temelji na učestalosti faktura.
   - **Datum kontrolne točke** – Datum koji se temelji na učestalosti faktura.
   - **Iznos kontrolne točke** – Izračunano dijeljenjem iznosa međuzbroja na retku podugovora s brojem kontrolnih točaka.

Ako redak podugovora ima vrijednost u polju **Procijenjeni iznos poreza**, ta se vrijednost jednako dodaje svakoj kontrolnoj točki pri generiranju povremenih kontrolnih točaka.

Zbroj iznosa kontrolnih točki retka podugovora mora biti jednak vrijednosti u retku podugovora. Ako nisu jednaki, dolazi do pogreške. Možete ispraviti pogrešku i provjeriti je li ukupna vrijednost kontrolne točke jednaka vrijednosti retka podugovora stvaranjem, uređivanjem ili brisanjem kontrolne točke i iznosa poreza. Nakon izvršenih promjena spremite i osvježite stranicu kako biste bili sigurni da nema više pogrešaka.

## <a name="manually-create-subcontract-line-milestones"></a>Ručno stvaranje kontrolnih točaka retka podugovora

Kontrolne točke s fiksnom cijenom na retku podugovora mogu se generirati ručno ako se povremeno ne dijele. Kako biste ručno stvorili kontrolnu točku retka podugovora, poduzmite sljedeće korake.

1. U navigacijskom oknu odaberite **Podugovori** i otvorite podugovor na kojem želite raditi.
2. Otvorite redak podugovora s fiksnom cijenom za koji želite stvoriti kontrolnu točku.
3. Na kartici **Kontrolne točke retka podugovora**, u podrešetki, odaberite **+ Nova kontrolna točka retka podugovora**.
4. Na stranici **Kontrolna točka novog retka podugovora** unesite obvezne podatke na temelju sljedeće tablice.

    | Polje | Opis |Funkcionalni utjecaj|
    | --- | --- |----------------------|
    | Naziv kontrolne točke | Naziv kontrolne točke. |To će se prikazati kao prvi stupac u svim pretraživanjima koja se temelje na kontrolnim točkama retka podugovara. Redak fakture dobavljača koji je stvoren na temelju ove kontrolne točke također će upotrebljavati naziv kontrolne točke retka podugovora kao zadani naziv retka fakture dobavljača.|
    | Opis | Opis kontrolne točke. |Redak fakture dobavljača koji je stvoren na temelju ove kontrolne točke također će upotrebljavati opis kontrolne točke retka podugovora kao zadani opis retka fakture dobavljača.|
    | Datum kontrolne točke | Datum kada bi proces automatskog stvaranja fakture trebao tražiti status ove kontrolne točke kako bi se uzeo u obzir za fakturiranje.| Ova će se vrijednost upotrebljavati kao zadani datum retka fakture dobavljača pri fakturiranju ovog retka podugovora. |
    | Iznos | Iznos ili vrijednost kontrolne točke koja će se fakturirati klijentu. |Ova se vrijednost upotrebljava kao zadana količina u retku fakture dobavljača pri fakturiranju ovog retka podugovora. |
    | Porez | Iznos poreza primijenjen na kontrolnu točku.| Ova se vrijednost upotrebljava kao zadana količina poreza u retku fakture dobavljača pri fakturiranju ovog retka podugovora. |
    | Iznos nakon oporezivanja | Ovo polje samo za čitanje izračunava se kao iznos + porez.|Ova se vrijednost upotrebljava kao zadana u retku fakture dobavljača pri fakturiranju ovog retka podugovora. |
    | Status fakture | Nakon stvaranja kontrolne točke ovaj se status uvijek postavlja na **Nije spremno za fakturiranje**.|  Kad je status **Spremno za fakturiranje**, stvaranje fakture dobavljača uključuje ovu kontrolnu točku na fakturi dobavljača. |

5. Odaberite **Spremi i zatvori**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
