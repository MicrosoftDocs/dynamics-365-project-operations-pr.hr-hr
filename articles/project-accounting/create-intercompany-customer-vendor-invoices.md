---
title: Stvaranje faktura za klijenta i dobavljača unutar tvrtke
description: U ovoj temi nalaze se informacije o načinu stvaranja faktura za klijenta i dobavljače unutar tvrtke.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f1560469d2bdbb8e81dc26c16b272c44446ab20a
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595440"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Stvaranje faktura za klijenta i dobavljača unutar tvrtke

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Računovođa projekta u pravnoj osobi koja kreditira stvara fakturu za klijenta unutar tvrtke za troškove projekta koji se prenose na entitet koji se zadužuje. Nakon odobrenja i knjiženja računa za klijenta unutar tvrtke, pravna osoba koja kreditira šalje fakturu unutar tvrtke pravnoj osobi koja se zadužuje.

Računovođa projekta pravne osobe koja kreditira može postaviti skupni postupak za generiranje ponavljajućih faktura unutar tvrtke. Računovođa projekta određuje kriterije, kao što su određeni projekti, za stvaranje skupnih faktura unutar tvrtke.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Ručno stvaranje fakture za klijenta unutar tvrtke za projektne transakcije 

Ovaj postupak upotrijebite za ručno stvaranje fakture za klijenta unutar tvrtke za projektne transakcije. Potražite radno vrijeme koje su radnici prijavili za rad na projektima u pravnim osobama koje se zadužuju i za troškove koje je vaša pravna osoba napravila u ime pravnih osoba koje se zadužuju. Možete pretraživati prema nazivu pravne osobe, broju ugovora o projektu, broju projekta, rasponu datuma ili bilo kojoj kombinaciji ovih mogućnosti. U rezultatima pretraživanja odaberite transakcije koje ćete dodati fakturi unutar tvrtke.

1. U aplikaciji Dynamics 365 Finance, idite na **Upravljanje projektima i računovodstvo** > **Fakture za projekt** > **Fakture za klijenta unutar tvrtke**. Na stranici s popisom **Fakture za klijenta unutar tvrtke**, u Oknu radnji, odaberite **Nova.**
2. Na stranici **Stvori fakturu unutar tvrtke**, u polju **Pravna osoba**, odaberite pravnu osobu koja se zadužuje.
3. Neobvezno: Unesite određeni ugovor o projektu i broj projekta.
4. Suzite pretraživanje odabirom raspona datuma. Unesite određene datume u polja **Datum početka** i **Datum završetka**. U rezultatima pretraživanja prikazuju se samo transakcije unutar tvrtke koje su proknjižene unutar ovog raspona datuma.
5. Postavite **Napredni parametar retka dnevnika projekta** na **Da** i odaberite **Traži**.
6. U rezultatima pretraživanja odaberite transakcije koje ćete uključiti u prijedlog fakture unutar tvrtke, a zatim odaberite **U redu**.
7. Na stranici **Faktura za klijenta unutar tvrtke** prikazuju se transakcije projekta unutar tvrtke koje ste odabrali iz rezultata pretraživanja. Kako biste izmijenili transakcije prije nego što fakturu pošaljete pravnoj osobi koja se zadužuje, učinite sljedeće:
  
    1. Otvorite stranicu **Stvaranje prijedloga fakture**. Odaberite dodatne transakcije unutar tvrtke za trenutačnu fakturu, a zatim **Dodaj redak**.
    2. Kako biste uklonili redak, kliknite ga i odaberite **Ukloni**.
    3. Pogledajte komentare, razloge, financijske veličine i ostale podatke o odabranom retku na BrzojKartici **Redci fakture**.
    
8. Za knjiženje fakture za klijenta unutar tvrtke, u Oknu radnje odaberite **Knjiži**.

> [!NOTE]
> Ako vaša tvrtka ili ustanova zahtijeva pregled fakture unutar tvrtke prije knjiženja, administrator sustava može postaviti tijek rada za fakture unutar tvrtke. Ako za fakture unutar tvrtke tijek rada nije postavljen, možete knjižiti fakturu unutar tvrtke.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Stvaranje skupnog posla za fakture unutar tvrtke

Možete istodobno stvoriti više faktura unutar tvrtke za sve pravne osobe koje se zadužuju. S pomoću funkcionalnosti pretraživanja možete, na primjer, pretraživati sve transakcije koje su prijavili posuđeni radnici, a povezane su s projektima kojima upravljaju druge pravne osobe. Zatim, za svaku pravnu osobu koja se zadužuje, možete stvoriti fakturu unutar tvrtke za transakcije navedene u rezultatima pretraživanja.

1. Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Računi za projekt** > **Stvaranje faktura za klijenta unutar tvrtke**.
2. Na stranici **Stvaranje faktura za klijenta unutar tvrtke**, u polju **Tvrtka**, odaberite pravnu osobu kojoj se fakturira. Ako ne odaberete tvrtku, prikazuju se sve transakcije koje zadovoljavaju kriterije pretraživanja za sve pravne osobe koje se zadužuju.
3. U stavci **Stvori fakturu po** odaberite želite li stvoriti fakturu za transakcije unutar tvrtke koje se temelje na projektu ili pravnoj osobi koja se zadužuje.
4. Neobvezno: Kako biste odabrali određeni projekt i ugovor o projektu za koji će se stvoriti fakture unutar tvrtke, kliknite **Odaberi**. Na stranici **Upit**, u polju **Kriteriji**, odaberite ugovor o projektu, broj projekta ili oboje, a zatim odaberite **U redu**.
5. Na kartici **Skupina** postavite skupni postupak za stvaranje ponavljajućih faktura unutar tvrtke. Dodatne informacije potražite u članku [Slanje posla skupne obrade iz obrasca](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Za knjiženje fakture unutar tvrtke, u Oknu radnje odaberite **Knjiži**.

> [!NOTE]
> Ako vaša tvrtka ili ustanova zahtijeva pregled fakture unutar tvrtke prije knjiženja, administrator sustava može postaviti tijek rada za fakture unutar tvrtke. Ako za fakture unutar tvrtke tijek rada nije postavljen, možete knjižiti fakture unutar tvrtke.

## <a name="post-the-intercompany-vendor-invoice"></a>Knjiženje računa dobavljača unutar tvrtke

Računovođa projekta u pravnoj osobi koja se zadužuje može pregledati fakture dobavljača na čekanju unutar tvrtke kada se knjiži odgovarajuća faktura klijenta unutar tvrtke. U aplikaciji Finance, u pravnoj osobi koja se zadužuje, idite na **Dugovanja** > **Fakture** > **Faktura dobavljača na čekanju**. Broj fakture na čekanju podudarat će se s brojem fakture za klijenta unutar tvrtke. Provjerite je li faktura točna, a zatim je proknjižite. Knjiženjem fakture dobavljača unutar tvrtke stvara se sporedna knjiga projekta i transakcija glavne knjige koja odražava troškove transakcije u pravnoj osobi koja se zadužuje.
