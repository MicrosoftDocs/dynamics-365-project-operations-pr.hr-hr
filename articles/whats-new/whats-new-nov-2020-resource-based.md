---
title: Novosti u studenom 2020. – Project Operations za scenarije koji se temelje na resursu / bez zaliha
description: U ovoj temi nalaze se informacije o ažuriranjima kvalitete dostupnim u izdanju aplikacije Project Operations za scenarije koji se temelje na resursu / bez zaliha za studeni 2020.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9eda9d75f5a4d71e6e4b8bd22dce973270639db3f927ac6a76be5b3c4303fc31
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007947"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u studenom 2020. – Project Operations za scenarije koji se temelje na resursu / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

- Project Operations u verziji 4.4.0.70 okruženja platforme CDS
- Upravljanje projektima i računovodstvo u okruženju aplikacije Dynamics 365 Finance verzije 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Ažuriranja aplikacije Project Operations za scenarije koji se temelje na resursu / bez zaliha

### <a name="project-operations-on-cds"></a>Project Operations na platformi CDS

| Područje značajke                 | Broj reference | Ažuriranja kvalitete                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Upravljanje prilikama       | 2036993          | Redak procjene i redci ugovora za dodjelu resursa ažuriraju se na usvojenim ponudama kada je vrsta retka ponude **Svi zadaci**.                                                 |
| Naplata i određivanje cijene          | 2070392          | Redci ugovora o projektu na fakturi svaki put se povećavaju kada se odabere **Osvježi transakcije fakture**.                                                                         |
| Planiranje projekta             | 2043336          | Nije moguće izbrisati zapis o članu projektnog tima.                                                                                                                                  |
| Planiranje projekta             | 2046013          | Nedosljedno ponašanje za stupce procjene oznaka tijekom učitavanja u odnosu na promjenu vrste vremenske faze.                                                                                   |
| Planiranje projekta             | 2046647          | Vrijeme početka i završetka isključuje se za sat vremena kada članovi projektnog tima generiraju zahtjeve za resursima.                                                                      |
| Planiranje projekta             | 2053879          | (Prema predstojećoj implementaciji CDS-a) PublishUnassignedAssignments prekida pokušaj spremanja zadatka kada je pogreška „Vrijednost proslijeđena za ConditionOperator.In je prazna."                       |
| Planiranje projekta             | 2055501          | Ostavljanje stavke **Datum početka projekta** praznom uzrokuje neuspjeh u rasporedu.                                                                                                      |
| Planiranje projekta             | 2066817          | Nije moguće stvoriti generički resurs s pomoću alata za odabir ljudi na kartici **Zadaci**.                                                                                                   |
| Planiranje projekta             | 2067034          | Gumb **Prikaži pojedinosti** nije dostupan na stranici **Pojedinosti o zadatku**.                                                                                                       |
| Upravljanje resursima          | 2046667          | Generički članovi tima ne brišu se ni nakon što su svi resursi ispunjeni.                                                                                                    |
| Vrijeme i brzi unos troška | 2047499          | Gumb **Novi** na stranici Unos vremena otvara stranicu **Novi potpis e-pošte**.                                                                                               |
| Vrijeme i brzi unos troška | 2059859          | Neočekivani skočni prozor otvara se tijekom stvaranja unosa troška.                                                                                                                         |
| Drugo                        | 2044181          | (Deinstalacija narudžbenice) Kada pokušate deinstalaciju msdyn_ProjectServiceCore_Patch i osnovna rješenja za msdyn Project service, dolazi do pogreške „Zapis nije dostupan”.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektom i računovodstvo u aplikaciji Dynamics 365 Finance

| Područje značajke        | Broj reference | Ažuriranja kvalitete                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Priznavanje prihoda | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Procjena postotka završetka projekta pogrešna je kada se u ugovoru upotrebljava strana valuta i postotak napretka posla za cjelokupnu metodu.                     |
| Priznavanje prihoda | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Nije moguće knjižiti procjene s pomoću metoda dovršenja **Stvarni trošak**.                                                                                                    |
| Priznavanje prihoda | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Eliminacija ne uspijeva zbog pogreške u neravnoteži vaučera kada se valuta tvrtke i valuta transakcije razlikuju.                                              |
| Upravljanje troškovima  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Za korisnike koji nisu administratori, vrijednosti pretraživanja za stupce retka troškova poput **ID projekta** i **Kategorija troška** ne prikazuju se ispravno u okviru poveznika podataka. |
| Upravljanje troškovima  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Zadana vrijednost svojstva retka ne prikazuje se za kategorije troškova.                                                                                                         |
| Upravljanje troškovima  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Integracija troškova mora sadržavati svojstvo retka iz izvješća o troškovima.                                                                                             |
| Fakturiranje           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Nije moguće knjižiti prijedloge faktura za projekt zbog poruke pogreške koja navodi da nije provjerena valjanost kombinacija FD-a.                                                    |
| Fakturiranje           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Nije moguće prikazati transakcije iz stranice s pojedinostima **faktura**.                                                                                                              |
| Fakturiranje           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Redci prijedloga fakture mogu se izbrisati.                                                                                                                                  |
| Projektno računovodstvo  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Stavke izbornika **Predviđanje** nisu vidljive na stranici s popisom **Projekti**.                                                                                                   |
| Projektno računovodstvo  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Nije moguće otvoriti **Izjava o projektu**   > **Transakcije i predviđanja**.                                                                                                       |
| Projektno računovodstvo  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Prilagodi računovodstvo** nije omogućeno za fakturirane projektne transakcije.                                                                                                  |
| Projektno računovodstvo  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Pojedinosti o računovodstvu nisu uključene u tablicu **ProjCDSActualsImport** kada je dnevnik **Integracija** proknjižen.                                                  |
| Projektno računovodstvo  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Unos predviđanja projekta udvostručuje se kada uklonite, a zatim ponovno dodate dodjelu resursa.                                                                            |
| Projektno računovodstvo  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Odabirom veze ID projekta ne otvara se URL-adresa dubinske veze platforme CDS.                                                                                                         |
| Projektno računovodstvo  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Nije moguće ažurirati datum početka zadatka na platformi CDS.                                                                                                                           |
| Projektno računovodstvo  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Omogućivanjem značajke nisu mogući višestruki redci ugovora nije moguće bez integracije platforme CDS.                                                                                   |

### <a name="regulatory-updates"></a>Ažuriranja propisa
Za informacije o ažuriranjima propisa za aplikacije Finance and Operations, pogledajte članak [Ažuriranja propisa](/dynamics365/finance/localizations/regulatory-updates). Također se možete prijaviti na LCS i pregledati planirana regulatorna ažuriranja s pomoću alata za pretraživanje izdanja. Pretraživanje izdanja omogućuje vam pretraživanje po zemlji, vrsti značajke i izdanju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]