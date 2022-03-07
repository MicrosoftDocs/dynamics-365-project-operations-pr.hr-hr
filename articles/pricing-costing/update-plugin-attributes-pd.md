---
title: Ažuriranje atributa programskih dodataka s pomoću novih veličina za određivanje cijena
description: U ovoj temi nalaze se informacije o načinu ažuriranja atributa programskih dodatka za veličine za određivanje cijena.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d57ec617d2c7b10a01a75e7eaa9ca2d646af3f6ee1d06d4e6fb228fc0533da27
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988327"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Ažuriranje atributa programskih dodataka s pomoću novih veličina za određivanje cijena

U ovoj temi nalaze se informacije o načinu ažuriranja atributa programskih dodatka za veličine za određivanje cijena.

> [!NOTE]
> Ova se tema primjenjuje samo na ponude i značajke ugovora u aplikaciji Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Preduvjeti
Prije nego što dovršite korake navedene u ovoj temi, morate dovršiti postupke u sljedećim temama:

  - [Stvaranje prilagođenih polja i entiteta](create-custom-fields-entities-pricing-dimensions.md) 
  - [Dodavanje prilagođenih polja postavljanju cijena i transakcijskim entitetima](add-custom-fields-price-setup-transactional-entities.md)
  - [Postavljanje prilagođenih polja kao cjenovnih veličina](set-up-custom-fields-pricing-dimensions.md). 
  
Ako niste dovršili te postupke, dovršite ih, a zatim se vratite na ovu temu.

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