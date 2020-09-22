---
title: Kako mogu prilagoditi tijek poslovnog procesa faza projekta?
description: Pregled načina na koji je moguće prilagoditi tijek poslovnog procesa faza projekta.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: 36f7df9e-117d-4f85-af4b-d842e93321bd
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d4b99f67e929ebcd1a684bcd1124756140107d17
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750080"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Kako mogu prilagoditi tijek poslovnog procesa faza projekta?
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Postoji poznato ograničenje u ranijim verzijama aplikacije Project Service da imena faza u tijeku poslovnog procesa faza projekta moraju biti potpuno jednaka očekivanim engleskim imenima (**Quote**, **Plan**, **Close**). U suprotnom poslovna logika koja se oslanja na engleska imena faza neće raditi kako se očekuje. Zato ne možete vidjeti poznate radnje poput **Zamjena procesa** ili **Uređivanje procesa** dostupne na projektnom obrascu, te se prilagođavanje tijeka poslovnog procesa ne potiče. 

Ovo ograničenje navedeno je u verziji 2.4.5.48 i novijim verzijama. U ovom članku navedena su preporučena zaobilazna rješenja za ranije verzije ako trebate prilagoditi zadani tijek poslovnog procesa.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Poslovna logika traži točno podudaranje s engleskim imenima faza

Tijek poslovnog procesa faza projekta uključuje poslovnu logiku koja pokreće sljedeća ponašanja u aplikaciji:
- Kada se ponuda pridruži projektu, šifra postavlja tijek poslovnog procesa u fazu **Quote**.
- Kada se ugovor pridruži projektu, šifra postavlja tijek poslovnog procesa u fazu **Plan**.
- Kada tijek poslovnog procesa napreduje do faze **Close**, zapis projekta se deaktivira. Kada se projekat deaktivira, obrazac projekta i strukturna analiza rada (SAR) postaju samo za čitanje, imenovane rezervacije resursa se poništavaju i bilo kakvi povezani cjenici se deaktiviraju.

Poslovna logika oslanja se na engleske nazive za faze projekta. To oslanjanje na engleske nazive faza je glavni razlog zašto se ne preporučuje prilagođavanje tijeka poslovnog procesa faza projekta, kao i zašto na entitetu projekta ne možete vidjeti uobičajene radnje tijeka poslovnog procesa, poput **Zamjena procesa** ili **Uređivanje procesa**.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Što će se dogoditi ako se nazivi faza ne podudaraju sa engleskim nazivima?

Kada se nazivi faza u tijeku poslovnog procesa u verziji 1.x aplikacije Project Service na platformi 8.2 ne podudaraju potpuno sa engleskim nazivima faza, poslovna logika koja postavlja ispravnu fazu za ponude ili ugovore ili koja zatvara projekat se preskače. Ne prikazuju se poruke o pogrešci. Stoga se čini da možete prilagoditi tijek poslovnog procesa faza projekta. Međutim, nećete moći vidjeti nikakve automatske procese rada za ponude, ugovore i zatvaranje projekta.

Desila se značajna arhitektonska izmjena tijeka poslovnog procesa u verziji 2.4.4.30 i ranijim verzijama aplikacije Project Service na platformi 9.0, zbog koje je bila potrebna izmjena poslovne logike tijeka poslovnog procesa. Zato ćete dobiti poruku o pogrešci ako nazivi faza procesa ne odgovaraju očekivanim engleskim nazivima. 

Stoga, ako želite prilagoditi tijek poslovnog procesa faza projekta za entitet projekta možete samo dodati potpuno nove faze zadanom tijeku poslovnog procesa za entitet projekta, a faze **Quote**, **Plan** i **Close** moraju ostati iste. Zahvaljujući ovom ograničenju nećete dobiti poruke o pogrešci zbog poslovne logike koja očekuje engleske nazive faza u tijeku poslovnog procesa.

U verziji 2.4.5.48 ili novijim verzijama poslovna logika opisana u ovom članku uklonjena je iz zadanog tijeka poslovnog procesa za entitet projekta. Nadogradnja na tu ili noviju verziju omogućit će vam da prilagodite ili zamijenite zadani tijek poslovnog procesa s nekim od svojih. 

## <a name="workarounds-for-earlier-versions"></a>Zaobilazna rješenja za starije verzije

Ako nemate mogućnost nadogradnje, možete prilagoditi tijek poslovnog procesa faza projekta za entitet projekta na jedan od sljedećih načina:

1. Dodajte dodatne faze zadanoj konfiguraciji bez mijenjanja engleskih naziva faza za **Quote**, **Plan** i **Close**.

   > [!div class="mx-imgBorder"] 
   > ![Slnimka zaslona dodavanja faza zadanoj konfiguraciji](media/FAQ-Customize-BPF-1.png)
 
2. Stvorite vlastiti tijek poslovnog procesa i učinite ga primarnim tijekom poslovnog procesa za entitet projekta, nakon čega ćete moći imati kakve god želite nazive faza. Međutim, ako želite koristiti iste standardne faze projekta **Quote**, **Plan** i **Close**, morate odraditi odrađena prilagođavanja radi prilagođenih naziva faza. Složenija logika je u zatvaranju projekta, a možete ju pokrenuti i samim deaktiviranjem zapisa projekta.

   > [!div class="mx-imgBorder"] 
   > ![Snimka zaslona prilagođavanja BPF-a](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Dodatne napomene za verziju 2.4.4.30 ili starije verzije aplikacije Project Service na platformi 9.0

U verziji 2.4.4.30 ili ranijim verzijama aplikacije Project Service na platformi 9.0, s prilagođenim tijekom poslovnog procesa, polje **Naziv faze** u entitetu projekta, korišteno na grafikonu **Projekat po fazi**, i prikazi popisa projekta neće biti ažurirani jer su usklađeni s zadanim tijekom poslovnog procesa faza projekta. Taj problem možete riješiti na sljedeći način:

- Dodajte prilagođeno polje da biste zabilježili trenutnu fazu tijeka poslovnog procesa koja se ažurira dok korisnik napreduje u prilagođeom tijeku poslovnog procesa.

- Izmijenite grafikon **Projekat po fazi** da biste radili s prilagođenim poljem umjesto s zadanom konfiguracijom.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Koraci za stvaranje vlastitog tijeka poslovnog procesa za entitet projekta

Slijedite sljedeće korake da biste stvorili vlastiti tijek poslovnog procesa za entitet projekta:

1. Idite na **Postavke** > **Procesni centar**. Nemojte kopirati tijek poslovnog procesa faza projekta jer time ćete kopirati i poslovnu logiku aplikacije Project Service.

   > [!div class="mx-imgBorder"] 
   > ![Snimka zaslona prilagođavanja BPF-a](media/FAQ-Customize-BPF-3.png)

2. Koristite dizajnera procesa za stvaranje naziva faza koje želite. Ako želite iste funkcije koje imaju zadane faze za **Quote**, **Plan** i **Close**, morat ćete to stvoriti na temelju prilagođenih naziva faza tijeka poslovnog procesa.

   > [!div class="mx-imgBorder"] 
   > ![Snimka zaslona dizajnera procesa koji se koristi za prilagođavanje BPF-a](media/FAQ-Customize-BPF-4.png) 

3. U dizajneru procesa kliknite **Narudžba tijeka procesa** da biste prilagođeni tijek poslovnog procesa učinili primarnim tijekom poslovnog procesa za entitet projekta time što ćete ga premjestiti na vrh popisa iznad tijeka poslovnog procesa faza projekta.

   > [!div class="mx-imgBorder"] 
   > ![Snimka zaslona korištenja narudžbe tijeka procesa](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Sljedeći koraci se odnose na verziju 2.4.4.30 ili starije verzije aplikacije Project Service na platformi 9.0

4. Dodajte novo prilagođeno polje entitetu projekta da biste zabilježili prilagođene faze u prilagođenom poslovnom procesu. Morat ćete dodati poslovnu logiku (dodatak/tijek rada) da biste ažurirali ovo polje kada ažurirate fazu u prilagođenom tijeku poslovnog procesa.

   > [!div class="mx-imgBorder"] 
   > ![Snimka zaslona prilagođavanja entiteta projekta](media/FAQ-Customize-BPF-6-720.png)

5. Izmijenite grafikon **Projekat po fazi** da biste koristili novo prilagođeno polje za faze.

   > [!div class="mx-imgBorder"] 
   > ![Snimka zaslona korištenja grafikona projekta po fazi](media/FAQ-Customize-BPF-7-720.png)

6. Izmijenite bilo koje prikaze za entitet projekta da biste uključili novo prilagođeno polje za faze.

   > [!div class="mx-imgBorder"] 
   > ![Snimka zaslona mijenjanja prikaza na entitetu projekta](media/FAQ-Customize-BPF-8-720.png)

