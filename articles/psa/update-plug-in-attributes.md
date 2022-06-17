---
title: Ažuriranje atributa dodatka za uključivanje novih dimenzija cijena
description: U ovom se članku nalaze informacije o ažuriranju atributa dodatka za dimenzije određivanja cijena.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 459aefb510cc9a9ec55a86ca7e362db98ccabb70
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913197"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Ažuriranje atributa dodatka za uključivanje novih dimenzija cijena

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Ako ne koristite značajke citiranja i ugovaranja automatizacije projektnih usluga (PSA), možete preskočiti ovaj članak.

U ovom se članku pretpostavlja da ste dovršili postupke u člancima, [Kreirajte prilagođena polja i entitete](create-custom-fields-entities.md), [Dodajte prilagođena polja postavi cijena i entitetima](field-references.md) transakcija te [Postavite prilagođena polja kao dimenzije cijena](set-up-pricing-dimensions.md). Ako niste dovršili te postupke, vratite se i dovršite ih, a zatim se vratite na ovaj članak.

Kada se pojedinost retka ponude izradi na stranici **Redak ponude** za redak ponude projekta, sustav stvara dva retka procjene u pozadini – jedan redak za stranu troška procjene i jedan za stranu prodaje. Isto vrijedi i za retke ugovora o projektu.

Kada uvedete promjenu u količinu ili polje na strani troška, ta se promjena prenosi na stranu prodaje. To je moguće zbog sljedećih dodatka koji se moraju ponovno registrirati nakon promjene dimenzija cijena.

- PreOperationContractLineDetailUpdate – Ažuriranja **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate – Ažuriranja **msdyn_quotelinetransaction**.

Koraci u nastavku objašnjavaju vam postupak registracije dodataka.

1. Otvorite **PluginRegistrationTool** i povežite se s mrežnom instancom.
2. Kliknite **Pretraži** i potražite dodatak za ažuriranje.

 ![Snimka zaslona s prikazom stabla pretraživanja.](media/PRT-1.png)

3. Nakon što pronađete dodatak, odaberite ga, a zatim kliknite **Odaberi u glavnom obrascu**.

4. Odaberite korak dodatka za ažuriranje, kliknite desnom tipkom miša, a zatim odaberite **Ažuriraj**.

 ![Snimka zaslona s prikazom dodatka koji se ažurira.](media/PRT-2.png)
 
5. U prozoru za ažuriranje kliknite tri točke (**...**) u atributima filtriranja.

 ![Snimka zaslona s prikazom informacija o konfiguraciji ažuriranja postojećeg koraka.](media/PRT-3.png)
 
6. Odaberite potvrdne okvire atributa cijena.

 ![Snimka zaslona s prikazom odabranog potvrdnog okvira za atribute cijena.](media/PRT-4.png)

7. Kliknite **U redu** da biste zatvorili stranicu, a zatim odaberite **Ažuriraj korak**.

 ![Snimka zaslona s prikazom gumba „Ažuriraj korak”.](media/PRT-5.png)
 
8. Ponovite ovaj postupak za drugi dodatak, **PreOperationQuoteLineDetail – Ažuriranje msdyn_quotelinetransaction**.

9. Zatvorite alat za registraciju dodataka.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
