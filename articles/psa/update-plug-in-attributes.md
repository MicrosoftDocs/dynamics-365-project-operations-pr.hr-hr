---
title: Ažuriranje atributa dodatka za uključivanje novih dimenzija cijena
description: Ovaj tema pruža informacije o ažuriranju atributa dodatka za dimenzije cijena.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 603b0e9a10dc2fe23c9fa0fa7065bc3f500dc540
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147059"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Ažuriranje atributa dodatka za uključivanje novih dimenzija cijena

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Ako ne upotrebljavate značajke sastavljanja ponuda i ugovora u programu Project Service Automation (PSA), možete preskočiti ovu tema.

Ova tema podrazumijeva da ste dovršili postupke opisane u temama [Izrada prilagođenih polja i entiteta](create-custom-fields-entities.md), [Dodavanje prilagođenih polja postavljanju cijena i transakcijskim entitetima](field-references.md) i [Postavljanje prilagođenih polja kao dimenzija cijena](set-up-pricing-dimensions.md). Ako niste dovršili te postupke, vratite se i dovršite ih, a zatim se vratite na ovu temu.

Kada se pojedinost retka ponude izradi na stranici **Redak ponude** za redak ponude projekta, sustav stvara dva retka procjene u pozadini – jedan redak za stranu troška procjene i jedan za stranu prodaje. Isto vrijedi i za retke ugovora o projektu.

Kada uvedete promjenu u količinu ili polje na strani troška, ta se promjena prenosi na stranu prodaje. To je moguće zbog sljedećih dodatka koji se moraju ponovno registrirati nakon promjene dimenzija cijena.

- PreOperationContractLineDetailUpdate – Ažuriranja **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate – Ažuriranja **msdyn_quotelinetransaction**.

Koraci u nastavku objašnjavaju vam postupak registracije dodataka.

1. Otvorite **PluginRegistrationTool** i povežite se s mrežnom instancom.
2. Kliknite **Pretraži** i potražite dodatak za ažuriranje.

 ![Snimka zaslona stabla pretraživanja](media/PRT-1.png)

3. Nakon što pronađete dodatak, odaberite ga, a zatim kliknite **Odaberi u glavnom obrascu**.

4. Odaberite korak dodatka za ažuriranje, kliknite desnom tipkom miša, a zatim odaberite **Ažuriraj**.

 ![Snimka zaslona dodatka koji se ažurira](media/PRT-2.png)
 
5. U prozoru za ažuriranje kliknite tri točke (**...**) u atributima filtriranja.

 ![Snimka zaslona informacija o konfiguraciji ažuriranja postojećeg koraka](media/PRT-3.png)
 
6. Odaberite potvrdne okvire atributa cijena.

 ![Snimka zaslona s prikazom odabranog potvrdnog okvira za atribute cijena](media/PRT-4.png)

7. Kliknite **U redu** da biste zatvorili stranicu, a zatim odaberite **Ažuriraj korak**.

 ![Snimka zaslona s prikazom gumba „Ažuriraj korak”](media/PRT-5.png)
 
8. Ponovite ovaj postupak za drugi dodatak, **PreOperationQuoteLineDetail – Ažuriranje msdyn_quotelinetransaction**.

9. Zatvorite alat za registraciju dodataka.



[!INCLUDE[footer-include](../includes/footer-banner.md)]