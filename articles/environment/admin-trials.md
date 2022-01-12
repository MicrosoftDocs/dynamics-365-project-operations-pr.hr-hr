---
title: Prijava za probnu verziju aplikacije Project Operations
description: U ovoj temi nalaze se informacije o načinu implementacije probne verzije aplikacije Dynamics 365 Project Operations.
author: ruhercul
ms.date: 12/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e40b4ac23241730f5c2db89f0dc674083f9e7abe
ms.sourcegitcommit: 8f970b46d0303dafaa75fc7d00567d232e1e600b
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901608"
---
# <a name="sign-up-for-project-operations-trials"></a>Prijava za probnu verziju aplikacije Project Operations 

_**Odnosi se na:** Project Operations za scenarije koji se temelje na resursima / bez zaliha, jednostavne implementacije – od sklapanja posla do predračuna, Project Operations za scenarije koji se temelje na zalihama/proizvodnji_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

U ovoj se temi objašnjava kako se pretplatiti na pretpregled partnerske ponude i implementirati okruženje aplikacije Dynamics 365 Project Operations.

Uz novu probnu verziju aplikacije Project Operations, možete automatski implementirati bilo koji od tri podržana scenarija implementacije ispunjavanjem upitnika koji preporučuje najbolji implementacijski pristup. U ovoj temi nalaze se informacije o to me kako:

- Iskoristiti ponudu probne verzije.
- Pokrenuti dodjelu resursa.
- Konfigurirati dvostruko pisanje.
- Saznajte više o aplikaciji Project Operations. 

U sljedećoj tablici opisane su pojedinosti nove ponude probne verzije.

| **Stavka ponude**               | **Pojedinosti**                                  |
|------------------------------|----------------------------------------------|
| Vrsta ponude                   | Ova je vrsta ponude potencijalni klijent administratora pa je za iskorištavanje potreban administrator klijenta. |
| Uporaba ponude                    | Jednom po klijentu                          |
| Trajanje ponude               | 30 kalendarskih dana                             |
| Otkupnine po klijentu       | 1                                            |
| Broj korisnika              | 25                                           |
| Proširenje                    | 1 produžetak, 30 kalendarskih dana               |
| Broj okruženja probne verzije | 3                                            |


## <a name="admin-trial-details"></a>Pojedinosti probne verzije administratora
U sljedećoj tablici navedene su pojedinosti probne verzije i kako se one primjenjuju na svaku vrstu implementacije.

| **Stavka**                      | **Osnovna verzija**                                     | **Materijali koji nisu na zalihi** | **Materijali koji su na zalihi** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Dostavljeni su podaci o postavljanju           | Jest                                          | Jest                       | Da (USSI)            |
| Transakcijski podaci            | No                                           | No                        | No                    |
| Vrijeme dodjele resursa u minutima  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Preduvjeti
Kako biste implementirali probnu verziju aplikacije Dynamics 365 Project Operations, potrebni su sljedeći preduvjeti.

- Prijavite se za aplikaciju [Dynamics 365 Project Operations – probna verzija pretpregleda](https://www.aka.ms/try-po).
- Korisnik koji uvodi pretpregled mora imati globalna prava administratora za klijent platforme Azure.

> [!IMPORTANT]
> Samo jedna osoba u tvrtki ili ustanovi, administrator klijenta, treba izvršiti ovaj zadatak. Ako niste pretplatnik na ovo izdanje, pričekajte dok se vaša tvrtka ili ustanova ne prijavi i ne dobijete svoje vjerodajnice.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations – probna verzija pretpregleda 

Prije nego što započnete, prijavite se u preglednik s korisničkim radnim računom na klijentu na kojem želite pretpregled aplikacije Project Operations.

1. Iskoristite kod prve ponude, **Dynamics 365 Project Operations – probna verzija pretpregleda** tako da ga zalijepite na URL-adresu preglednika.

    ![Korištenje ponude](./media/16RedeemFirstOfferNew.png)

2. Potvrdite svoj nalog.

    ![Potvrda naloga](./media/17ConfirmOrderNew.png)

  Vidjet ćete kako je potvrdna ponuda uspješno iskorištena.

   ![Potvrda](./media/18OrderConfirmationNew.png)

  Bit ćete preusmjereni na [centar za administratore aplikacije Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Upitnik i dodjela resursa

1.  Idite u [centar za administratore aplikacije Power Platform](https://admin.powerplatform.com/projectoperationstrial) i dovršite upitnik.  
2.  Pregledajte preporučenu vrstu implementacije i odaberite mogućnost **Započni postavljanje** za pokretanje dodjele resursa.
3.  Pregledajte uvjete i odredbe, a zatim odaberite **Početak**.

   Nakon pokretanja dodjele resursa bit ćete preusmjereni na popis okruženja u centru za administratore aplikacije Power Platform. Dok je dodjela resursa u tijeku, vaše je okruženje u stanju **PreparingInstance**.
 
  Kad je dodjela resursa dovršena, stanje vašeg okruženja je **Spremno**. Dodjela resursa okruženja uključuje uvođenje pokaznih podataka.
 
4.  Odaberite odgovarajuće URL-adrese aplikacija Microsoft Dataverse i Finance and Operations za provjeru uvođenja.

## <a name="configuring-dual-write"></a>Konfiguriranje dvostrukog pisanja
- Da biste konfigurirali bezbednosne uloge za dva pisanja, [pročitajte članak Ažuriranje sigurnosnih postavki u programu Project Operations u programu Dataverse](resource-provision-new-environment.md).
- Da biste konfigurirali karte s dvostrukim pisanjem, pročitajte [članak Pokretanje mapa s dvostrukim pisanjem operacija projekta](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Dodjela licenci

Trebat će vam administrativni pristup portalu sustava Microsoft 365 vaše tvrtke ili ustanove za dovršetak sljedećih koraka.

1. Idite u [centar za administratore sustava Microsoft 365](https://portal.office.com/) kako biste dodijelili licence svojim korisnicima.

   ![Početna stranica Centra za administratore](./media/14AdminPortal.png)

2. Na stranici **Aktivni korisnici** odaberite korisnike kojima želite dodijeliti licencu.

   ![Dodjela licenci](./media/15AssignLicenses.png)

3. Provjerite je li odabrana licenca **Pretpregled sustava Dynamics 365 Project Operations**, a zatim odaberite **Spremi promjene**.

## <a name="additional-resources"></a>Dodatni resursi

Sljedeći izvori pružaju korisne smjernice dok započinjete svoj put s aplikacijom Project Operations:

- [Videoserija – Pretpregled aplikacije Project Operations sadrži sitne pojedinosti i kartu puta](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Odredite vrstu implementacije](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Najčešća pitanja

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Što ako za svoje okruženje aplikacija sustava Finance and Operations trebam ALM ili ELM?

- Za partnere koji trebaju potpune mogućnosti upravljanja životnim ciklusom okruženja, pogledajte [Zahtjev za licencu za sigurnosnu ogradu partnera](https://experience.dynamics.com/requestlicense) kako biste pregledali novu ponudu partnera. 
- Za partnere koji traže dodatne informacije o pravima interne uporabe, pogledajte članak [Prednosti prava interne uporabe u oblaku i softveru (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Mogu li produžiti probno razdoblje nakon 30 dana?
Kako biste produžili probno razdoblje, poduzmite sljedeće korake.

1. U **Centru za administratore sustava Microsoft 365** idite na **Naplata** > **Vaši proizvodi**.
2. Odaberite **Dynamics 365 Project Operations (CE) – probna verzija pretpregleda**.
3. Pod stavkom **Datum isteka** odaberite **Produži datum**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Mogu li nadograditi iz implementacije osnovne verzije na implementaciju scenarija zasnovanog na resursima / bez zaliha?
Trenutačno ne postoji podrška za nadogradnju okruženja iz implementacije osnovne verzije u implementaciju zasnovanu bez zaliha.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Mogu li pristupiti rješenju Lifecycle Services (LCS) za svoja okruženja aplikacije Finance?  
Ne. Za ove probne verzije implementacijom se upravlja putem centra za administratore aplikacije Power Platform. Pristup okruženju aplikacije Finance ograničen je.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Mogu li instalirati probnu verziju na postojeće okruženje?
Ako imate postojeće okruženje, bit će vam dopušteno instalirati implementaciju osnovne verzije na postojeće okruženje prodaje platforme Dataverse iz centra za administratore aplikacije Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
