---
title: Kontrolne točke retka podugovora
description: U ovoj temi objašnjava se način stvaranja i održavanja rasporeda faktura koji se temelji na kontrolnim točkama za podugovor s dobavljačem.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3301e5a627e4842009fcd5e352f1b76fd3053ee3
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323767"
---
# <a name="subcontract-line-milestones"></a>Kontrolne točke retka podugovora

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

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

    | Polje | Opis |
    | --- | --- |
    | Naziv kontrolne točke | Naziv kontrolne točke. |
    | Opis | Opis kontrolne točke.  |
    | Datum kontrolne točke | Datum kada bi proces automatskog stvaranja fakture trebao tražiti status ove kontrolne točke kako bi se uzeo u obzir za fakturiranje. Ta je vrijednost uključena u redak fakture dobavljača pri fakturiranju za ovaj podugovor. |
    | Iznos | Iznos ili vrijednost kontrolne točke koja će se fakturirati klijentu. Ta je vrijednost uključena u redak fakture dobavljača pri fakturiranju za ovaj podugovor. |
    | Porez | Iznos poreza primijenjen na kontrolnu točku. Ta je vrijednost uključena u redak fakture dobavljača pri fakturiranju za ovaj podugovor. |
    | Iznos nakon oporezivanja | Ovo polje samo za čitanje izračunava se kao iznos + porez. Ta je vrijednost uključena u redak fakture dobavljača pri fakturiranju za ovaj podugovor. |
    | Status fakture | Nakon stvaranja kontrolne točke ovaj se status uvijek postavlja na **Nije spremno za fakturiranje**.  Kad je status **Spremno za fakturiranje**, stvaranje fakture dobavljača uključuje ovu kontrolnu točku na fakturi dobavljača. |

5. Odaberite **Spremi i zatvori**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
