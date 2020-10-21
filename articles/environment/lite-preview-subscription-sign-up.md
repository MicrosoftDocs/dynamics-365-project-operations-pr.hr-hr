---
title: Prijava za pretplatu na pretpregled
description: U ovoj temi nalaze se informacije o načinu pretplate i uvođenja jednostavne aplikacije Project Operations – od sklapanja posla do predračuna.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948789"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Prijava za pretplatu na pretpregled za jednostavno uvođenje – posao s predračunom

U ovoj temi pojašnjava se način pretplate na pretpregled ponude partnera i uvođenja jednostavne aplikacije Dynamics 365 Project Operations – od sklapanja posla do predračuna.

> [!NOTE]
> Ovaj će se postupak promijeniti u predstojećim izdanjima aplikacije Project Operations.

## <a name="prerequisites"></a>Preduvjeti

- Dobit ćete e-poštu s pozivom da sudjelujete u pretpregledu. Možete zatražiti pretpregled na [Web-mjestu aplikacije Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Korisnik koji uvodi pretpregled mora imati globalna prava administratora za klijent platforme Azure.
- Korisniku koji uvodi pretpregled potreban je telefonski broj i valjana kreditna kartica. Tijekom prijave kartica se neće naplaćivati narednih šest mjeseci. Nakon šest mjeseci morate otkazati pretplatu. 
- Pregledajte sve uvjete i odredbe.

## <a name="subscribe"></a>Pretplata

Kada primite odobrenje [zahtjeva za pretpregled](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), e-poštom ćete primiti dvije ponude od tvrtke Microsoft. Te ponude omogućuju vam postavljanje pretpregleda aplikacije Project Operations:

- Probni pretpregled aplikacije Dynamics 365 Customer Service – šifra za jednokratnu uporabu
- Dynamics 365 Project Operations – probni pretpregled

### <a name="dynamics-365-customer-service-paid-offer"></a>Ponuda za plaćanje aplikacije Dynamics 365 Customer Service

1. S pomoću prozora preglednika U privatnosti / Anonimno možete iskoristiti prvi kôd ponude za aplikaciju Dynamics 365 Customer Service. Kako biste se prijavili za aplikaciju Customer Service, trebat će vam sljedeće:

- Broj telefona
- Kreditna kartica. Kada se prijavite, kartica se neće naplaćivati narednih šest mjeseci. Nakon šest mjeseci morate otkazati pretplatu.
- Pregledajte sve uvjete i odredbe.

2. Navedite svoje podatke za kontakt.

![Podaci za kontakt](./media/1ContactInformation.png)

3. Navedite pojedinosti o novom klijentu.

![Stvorite ID korisnika](./media/2CreateUserID.png)

4. Potvrdite svoj identitet, spremite novi korisnički ID, a zatim odaberite **Postavi**.

![Spremite podatke](./media/3SaveInfo.png)

5. Dovršite registraciju kreditne kartice i pregledajte sve uvjete i odredbe. 

![Dovrši kreditnu karticu](./media/4CompleteCreditCard.png)

![Plati kreditnom karticom](./media/5CreditCardCheckout.png)

![Spremi narudžbu](./media/6SaveOrder.png)

![Potvrda kreditne kartice](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>Otkazivanje ponude aplikacije Dynamics 365 Customer Service za poduzeće

Ponuda aplikacije Dynamics 365 Customer Service za poduzeće omogućuje besplatnu uporabu šest mjeseci. Ponuda će se obnoviti po punoj cijeni na kraju šestomjesečnog razdoblja. Kako biste otkazali prije datuma obnove, slijedite sljedeće upute. 

> [!NOTE]
> Nakon što dovršite ove korake, više nećete moći upotrebljavati okruženje javnog pretpregleda aplikacije Project Operations.

1. Idite na [Portal za administratore](https://admin.microsoft.com/) i pod stavkom **Naplata**, odaberite **Vaši proizvodi**.

![Portal za administratore, stranica Vaši proizvodi](./media/8AdminPortal.png)

2. Odaberite **Ponudu za poduzeće aplikacije Dynamics 365 Customer Service**.

![Otkazivanje pretplate](./media/9CancelSubscription.png)

3. Odaberite **Postavke** > **Radnje** > **Otkaži pretplatu**.
4. U obrazac **Otkazivanje pretplate** unesite podatke u obvezna polja.
5. Odaberite **Otkaži** > **Pretplata**.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – probni pretpregled

1. Iskoristite drugu ponudu probne aplikacije Dynamics 365 Project Operations s pomoću URL-adrese navedene u poruci dobrodošlice koju ste dobili e-poštom.

![Korištenje ponude 2](./media/10RedeemOffer2.png)

2. Provjerite jeste li prijavljeni kao korisnik koji pripada istoj tvrtki ili ustanovi koja je pretplaćena s pomoću prvog koda ponude, a zatim nastavite s iskorištavanjem ponude. 
3. Odaberite **Da, dodaj na moj račun**.

![Dodavanje na račun](./media/11AddToAccount.png)

![Zaslon Pokušaj sada](./media/12TryNow.png)

![Detalji narudžbe](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Dodjela licenci

> [!IMPORTANT]
> Trebat će vam administrativni pristup portalu sustava Office 365 vaše tvrtke ili ustanove za dovršetak sljedećih koraka.

1. Idite do [Centra za administratore sustava Microsoft 365](https://portal.office.com/) kako biste dodijelili licence svojim korisnicima.

![Početna stranica Centra za administratore](./media/14AdminPortal.png)

2. Na stranici **Aktivni korisnici** odaberite korisnike kojima želite dodijeliti licencu.

![Dodjela licenci](./media/15AssignLicenses.png)

3. Provjerite jesu li odabrane licence za **Customer Service Enterprise** i **Project Operations** i odaberite **Spremi promjene**.

## <a name="create-a-new-cds-environment"></a>Stvaranje novog CDS okruženja

Pripremite novo okruženje za uvođenje CDS-a aplikacije Project Operations slijedeći upute u temi [Model uvođenja CDS-a](lite-deployment.md).

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instaliranje CDS konfiguracije i postavljanje pokaznih podataka

Instalirajte CDS konfiguraciju i postavite pokazne podatke slijedeći upute u temi [Primjena pokaznih postavki i konfiguracijskih podataka](lite-apply-demo-setup-config-data.md).
