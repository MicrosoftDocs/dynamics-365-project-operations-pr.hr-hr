---
title: Ažuriranje atributa programskih dodataka s pomoću novih veličina za određivanje cijena
description: U ovom se članku nalaze informacije o ažuriranju atributa dodatka za dimenzije određivanja cijena.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ae502fea533d9f199ef5ee1cc85b623f08cbd84
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920005"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Ažuriranje atributa programskih dodataka s pomoću novih veličina za određivanje cijena

U ovom se članku nalaze informacije o ažuriranju atributa dodatka za dimenzije određivanja cijena.

> [!NOTE]
> Ovaj se članak primjenjuje samo na ponudu i značajke ugovora u sustavu Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Preduvjeti
Prije nego što dovršite korake u ovom članku, morate dovršiti postupke u sljedećim člancima:

  - [Stvaranje prilagođenih polja i entiteta](create-custom-fields-entities-pricing-dimensions.md) 
  - [Dodavanje prilagođenih polja postavljanju cijena i transakcijskim entitetima](add-custom-fields-price-setup-transactional-entities.md)
  - [Postavljanje prilagođenih polja kao cjenovnih veličina](set-up-custom-fields-pricing-dimensions.md). 
  
Ako niste dovršili te postupke, dovršite ih, a zatim se vratite na ovaj članak.

## <a name="register-a-plug-in"></a>Registrirajte programski dodatak
Kada se stvara pojedinost ponude na stranici **Redak ponude** za redak ponude projekta, sustav stvara dva retka procjene. Jedan redak odnosi se na troškovnu stranu procjene, a drugi na prodajnu stranu. Isto vrijedi i za retke ugovora o projektu.

Kada uvedete promjenu u količinu ili polje na strani troška, ta se promjena unosi i na stranu prodaje. To je moguće jer programski dodaci PreOperation na entitetima Pojedinosti retka ponude i Pojedinosti retka ugovora povezuju određene atribute na troškovnoj i prodajnoj strani transakcije. Ako trebate unijeti promjene u vrijednosti veličina za određivanje cijena na prodajnoj strani kako bi se izvršile i na troškovnoj strani, sljedeći se programski dodaci moraju ponovno registrirati nakon unošenja promjena u veličinu za određivanje cijene.

Ovo su programski dodaci za ažuriranje i ponovnu registraciju:

- PreOperationContractLineDetailUpdate – **Ažuriraj msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate – **Ažurira msdyn_quotelinetransaction**

Za ažuriranje i ponovnu registraciju programskih dodataka poduzmite sljedeće korake.

1. Otvorite **PluginRegistrationTool** i povežite se s okruženjem aplikacije Project Operations platforme Dataverse.
2. Odaberite **Traži** i upišite prvih nekoliko slova programskog dodatka koji će se ažurirati.
3. Nakon što pronađete dodatak, odaberite ga, a zatim odaberite **Odaberi u glavnom obrascu**.
4. Odaberite korak **Ažuriraj msdyn_orderlinetransaction**, kliknite desnu tipku miša i zatim odaberite **Ažuriraj**.
5. Na dijaloškoj stranici **Ažuriranje** odaberite tri točke (**...**) u atributima za filtriranje.
6. Otvara se prozor za filtriranje atributa na kojem se navodi popis svih atributa u entitetu i veličina za određivanje cijena. Označite potvrdne okvire za atribute veličina za određivanje cijena.
7. Odaberite **U redu** kako biste zatvorili stranicu, a zatim odaberite **Ažuriraj korak**.
8. Ponovite korake od 2 do 7 za drugi programski dodatak, **PreOperationQuoteLineDetail**. Za ovaj programski dodatak, morate ažurirati korak **Ažuriranje msdyn_quotelinetransaction**.
9. Zatvorite **Alat za registraciju programskih dodataka**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]