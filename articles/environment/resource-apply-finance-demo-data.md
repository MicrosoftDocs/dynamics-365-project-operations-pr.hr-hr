---
title: Primjena pokaznih podataka u okruženju aplikacije Finance hostirane u oblaku
description: U ovoj temi pojašnjava se način primjene pokaznih podataka iz aplikacije Project Operations na okruženje hostirano u oblaku aplikacije Dynamics 365 Finance.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7d8a198b3bfd71ae08bc338d17896519b5ffd6b8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000141"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Primjena pokaznih podataka u okruženju aplikacije Finance hostirane u oblaku

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

> [!IMPORTANT]
> Ova tema odnosi se samo na verziju 10.0.13 aplikacije Microsoft Dynamics 365 Finance i može se izvršavati samo u okruženju hostiranom u oblaku. Dovršite korake iz ove teme **PRIJE** primjene kvalitativnih ažuriranja na okruženje.

1. U svom LCS projektu otvorite stranicu **Pojedinosti okruženja**. Vidite da to uključuje pojedinosti potrebne za povezivanje s okruženjem s pomoću protokola udaljene radne površine (RDP, Remote Desktop Protocol).

![Pojedinosti  okruženja](./media/1EnvironmentDetails.png)

Prvi skup istaknutih vjerodajnica, vjerodajnice su lokalnog računa i sadrže hipervezu na vezu s udaljenom radnom površinom. Vjerodajnice uključuju korisničko ime i lozinku administratora okruženja. Drugi skup vjerodajnica upotrebljava se za prijavu na SQL Server u ovom okruženju.

2. Daljinski se povežite s okruženjem hipervezom u stavci **Lokalni računi**, a za provjeru autentičnosti upotrijebite **Vjerodajnice lokalnog računa**.
3. Idite na mogućnost **Internetske informacijske usluge** > **Skupine aplikacija** > **Usluga AOS** i zaustaviti uslugu. Na ovoj točki zaustavljate uslugu kako biste mogli nastaviti mijenjati SQL bazu podataka.

![Zaustavljanje AOS-a](./media/2StopAOS.png)

4. Idite na stavku **Usluge** i zaustavite sljedeće dvije stavke:

- Microsoft Dynamics 365 Unified Operations: Usluga upravljanja skupom podataka
- Microsoft Dynamics 365 Unified Operations : Okvir za izvoz/uvoz podataka

![Zaustavljanje usluge](./media/3StopServices.png)

5. Otvorite aplikaciju Microsoft SQL Server Management Studio. Prijavite se s vjerodajnicama SQL poslužitelja i upotrijebite axdbadmin korisnika i lozinku s LCS stranice **Pojedinosti okruženja**.

![SQL Server Management Studio](./media/4SSMS.png)

6. U Object Exploreru idite na postavku **Baze podataka** i pronađite **AXDB**. Bazu podataka zamijenit ćete novom bazom podataka koja se nalazi u [Centru za preuzimanje](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Kopirajte zip datoteku u VM u koji ste udaljeni i izdvojite zip sadržaj.
8. U aplikaciji SQL Server Management Studio desnom tipkom miša kliknite **AxDB**, a zatim odaberite **Zadaci** > **Vrati** > **Baza podataka**.

![Vraćanje baze podataka](./media/5RestoreDatabase.png)

9. Odaberite **Izvorni uređaj** i prijeđite na datoteku izdvojenu iz zip datoteke koju ste kopirali.

![Izvorni uređaji](./media/6SourceDevice.png)

10. Odaberite **Mogućnosti**, a zatim **Piši preko postojeće baze podataka** i **Zatvori postojeće veze s odredišnom bazom podataka**. 
11. Odaberite **U redu**.

![Vraćanje postavki](./media/7RestoreSetting.png)

Dobit ćete potvrdu kako je vraćanje AXDB-a bilo uspješno. Nakon što primite ovu potvrdu, možete zatvoriti aplikaciju SQL Services Management Studio.

12. Vratite se na mogućnost **Internetske informacijske usluge** > **Skupine aplikacija** > **Usluga AOS** i pokrenite uslugu AOS.
13. Idite na **Usluge** i pokrenite dvije usluge koje ste ranije zaustavili.

14. Pronađite alat AdminUserProvisioning na ovom VM-u. Pogledajte na putanji K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Pokrenite datoteku .ext s pomoću svoje korisničke adrese u polju **Adresa e pošte**. 
16. Odaberite **Šalji**.

![Dodjela korisnika administratora](./media/8AdminUserProvisioning.png)

To traje nekoliko minuta. Trebali biste primiti poruku s potvrdom kako je korisnik administrator uspješno ažuriran.

17. Na kraju, pokrenite Command Prompt kao Administrator i izvršite iisreset

![IIS vraćanje](./media/9IISReset.png)

18. Zatvorite sesiju udaljene radne površine i upotrijebite LCS stranicu **Pojedinosti okruženja** za prijavu u okruženje kako biste potvrdili da radi onako kako se očekivalo.

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]