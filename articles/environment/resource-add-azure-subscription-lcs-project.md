---
title: Dodavanje pretplate za platformu Azure LCS projektu
description: U ovoj temi nalaze se informacije o načinu povezivanja pretplate za platformu Azure s LCS projektom.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948791"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a>Dodavanje pretplate za platformu Azure LCS projektu

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Okruženja hostirana u oblaku moraju se implementirati s pomoću postojeće pretplate za platformu Azure. U ovoj temi pojašnjava se način povezivanja pretplate za platformu Azure s LCS projektom. 

## <a name="grant-admin-consent"></a>Davanje pristanka administratora

1. U vašem LCS projektu, u odjeljku **Okruženja**, odaberite **Postavke platforme Microsoft Azure**.

![Postavke značajke Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. Na stranici **Postavke projekta**, na kartici **Poveznici platforme Azure**, odaberite **Autoriziraj**. To omogućuje implementaciju okruženja na ovaj projekt.

![Poveznici platforme Azure](./media/2AzureConnectors.png)

3. Ponovno odaberite **Autoriziraj** kako biste dali pristanak administratora.

![Davanje pristanka administratora](./media/3GrantAdminConsent.png)

4. Prihvatite zahtjev za dozvolama.

![Prihvaćanje zahtjeva za dozvolom](./media/4AcceptPermissionRequest.png)

Sada je autorizacija završena. 

![Autorizacija je uspješna](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Omogućivanje pristupa uslugama sustava Dynamics za implementaciju pretplati za platformu Azure

1. Idite na odjeljak [Naplata platforme Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) i odaberite svoju pretplatu. Usluge sustava Dynamics za implementaciju moraju pristupiti ovoj pretplati kako bi se okruženja mogla implementirati.

![Pojedinosti o pretplati za platformu Azure](./media/6AzureSubscription.png)

2. Odaberite **Kontrola pristupa (IAM)** u navigacijskom oknu, a zatim odaberite **Dodaj dodjelu uloge**.
3. U klizaču s desne strane odaberite **Uloga suradnika** i na navedenom popisu pronađite i odaberite **Usluge sustava Dynamics za implementaciju**. 
4. Odaberite **Spremi**.

![Pretplatnički pristup](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Dodavanje poveznika pretplate LCS projektu

1. U vašem LCS projektu, na stranici **Postavke platforme Microsoft Azure** odaberite **Dodaj** za dodavanje novog poveznika.
2. Unesite svoj ID pretplate za platformu Azure. Svoj ID pretplate za platformu Azure možete pronaći na [portalu platforme Azure](https://ms.portal.azure.com/), pod stavkom **Postavke** u donjem lijevom dijelu zaslona.
3. U polju **Konfiguriraj uporabu usluge Resource Manager za platformu Azure** odaberite **Da**.
4. Obvezno provjerite podudara li se pretplatnička domena platforme Azure AAD domena klijenta s Azure pretplatom koja je vlasnik domene koju upotrebljavate i odaberite **Dalje**.
5. Na zaslonu **Postavke platforme Microsoft Azure** odaberite **Dalje** za potvrdu. Ako se ovom zaslonu prikaže pogreška, vratite se na odjeljak [Omogućivanje uslugama sustava Dynamics za implementaciju pristupa pretplati za platformu Azure](#provide) u ovoj temi i provjerite jeste li izvršili sve korake.
6. Preuzmite certifikat platforme Azure za upravljanje u lokalnu mapu na računalu, a zatim ga prenesite na portal platforme Azure za upravljanje tako da odete na **Postavke** > **Certifikati za upravljanje**. Ovaj certifikat omogućit će LCS-u da u vaše ime komunicira s platformom Azure. Ovaj korak možete preskočiti ako vaš korisnik ima pristup pretplati.
7. Odaberite **Dalje**.
8. Odaberite regiju platforme Azure za implementaciju i odaberite podatkovni centar koji je blizu mjesta na kojem planirate upotrebljavati ovaj sustav.
9.  Odaberite **Poveži**.

Uspješno ste povezali svoju pretplatu za platformu Azure. Sada možete implementirati okruženja aplikacije Dynamics 365 Finance u oblaku.


