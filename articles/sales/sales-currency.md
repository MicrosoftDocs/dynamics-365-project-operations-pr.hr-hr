---
title: Valuta
description: U ovoj se temi nalaze informacije o načinu dodavanja i uklanjanja vrsta valuta u projektnim operacijama.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1db7e76dbb220954b9f9088b2168eed1a1902abc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073420"
---
# <a name="currency"></a>Valuta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Valute određuju cijene proizvoda navedenih u katalogu proizvoda i trošak transakcija kao što su prodajne narudžbe. Ako imate klijente širom svijeta, dodajte njihove valute radi upravljanja transakcijama. Dodajte valute koje najviše odgovaraju vašim trenutačnim i budućim poslovnim potrebama.  

> [!NOTE]
> Ako je vaše okruženje okruženje usluge Common Data Service, nalazite se u centru za administratore sustava Power Platform i odaberete stranicu **Valute** ( **Okruženja** > [odaberite okruženje] > **Postavke** > **Poslovanje** > **Valute** ), stranica će biti prazna. To je zbog toga što postavljanje valute nije podržano u okruženjima Common Data Service.

## <a name="add-a-currency"></a>Dodavanje valute  
Prije nego što započnete ovaj postupak, provjerite sadrži li vaša sigurnosna uloga dozvole administratora sustava. 

1. U centru za administratore za Power Platform odaberite okruženje. 
2. Odaberite **Postavke** > **Tvrtka**.
3. Odaberite **Valute**.  
4. Odaberite **Novo**.  
5. Unesite potrebne podatke.  


   |          Polje          |                                                                                                                                                                                                                                                                                                                                                                            Opis                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Vrsta valute**    | - **Sustav** – odaberite ovu mogućnost ako želite koristiti valute dostupne u aplikacijama utemeljenima na modelu u sustavu Dynamics 365. Za pretraživanje valute odaberite mogućnost **Traženje**. Kada odaberete šifru valute, **Naziv valute** i **Simbol valute** će se automatski dodati za odabranu valutu.<br />- **Prilagođeno** – odaberite ovu mogućnost ako želite dodati valutu koja nije dostupna u aplikacijama utemeljenima na modelu u sustavu Dynamics 365. U tom slučaju potrebno je ručno unijeti vrijednosti **Šifra valute** , **Preciznost valute** , **Naziv valute** , **Simbol valute** , i **Pretvorba valute**. |
   |    **Šifra valute**    |                                                                                                                                                                                                                                                                                                                                            Kratica valute. Na primjer **USD** za United States Dollar (dolar SAD-a).                                                                                                                                                                                                                                                                                                                                            |
   | **Preciznost valute**  |                                                                                                                                                                                  Upišite broj decimalnih mjesta koje želite koristiti za valutu.  Možete dodati vrijednost između 0 i 4. **Napomena**  Ako ste postavili preciznu vrijednost u dijaloškom okviru **Postavke sustava** , ta će se vrijednost pojaviti ovdje.                                                                                                                                                                                  |
   |    **Naziv valute**    |                                                                                                                                                                                                                                         Ako ste odabrali kod valute s popisa dostupnih valuta u aplikacijama utemeljenima na modelu u sustavu Dynamics 365 , naziv valute za odabrani kod prikazuje se ovdje. Ako ste odabrali **Prilagođeno** kao vrstu valute, upišite naziv valute.                                                                                                                                                                                                                                          |
   |   **Simbol valute**   |                                                                                                                                                                                                                                                                      Ako ste odabrali šifru valute s popisa dostupnih valuta, ovdje se prikazuje simbol za odabranu valutu. Ako ste odabrali **Prilagođeno** kao vrstu valute, unesite simbol za novu valutu.                                                                                                                                                                                                                                                                       |
   | **Pretvorba valute** |                                                                                                                                                                                                                                     Upišite vrijednost odabrane valute u odnosu na jedan američki dolar. To je iznos prema kojem se odabrana valuta pretvara u osnovnu valutu. **Važno:**  pobrinite se da ažurirate valutu dovoljno često kako biste izbjegli netočne izračune u transakcijama.                                                                                                                                                                                                                                      |


6. Kada završite, na naredbenoj traci odaberite **Spremi** ili **Spremi i zatvori**.  

   > [!TIP]
   >  Da biste uredili valutu, odaberite valutu, a zatim unesite ili odaberite nove vrijednosti.  

## <a name="delete-a-currency"></a>Brisanje valute  

1. U centru za administratore za Power Platform odaberite okruženje. 
2. Odaberite **Postavke** > **Tvrtka**.
3. Odaberite **Valute**.  
4. Na prikazanom popisu valuta odaberite valutu za brisanje.  
5. Odaberite **Obriši**.  
6. Potvrdite brisanje.  

> [!IMPORTANT]
>  Valute koje koriste drugi zapisi nije moguće izbrisati, ali ih je moguće deaktivirati. Ako deaktivirate zapise valute, nećete ukloniti informacije o valuti pohranjene u postojećim zapisima, kao što su prilike ili narudžbe. Međutim, nećete moći odabrati deaktiviranu valutu za nove transakcije.  
