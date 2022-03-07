---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 33, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334515"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 33, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 33. Ova verzija ima broj izdanja V3.10.54.98 i općenito je dostupna putem samostalnog ažuriranja u srpnju 2021. godine.

## <a name="update-release-33"></a>Izdanje ažuriranja 33

### <a name="bug-fixes"></a>Ispravke pogrešaka

**Vrijeme i trošak**

Popravljeni su sljedeći problemi:

- Dva zaključana polja, **msdyn_description** i **msdyn_externaldescription**, mogu se uređivati nakon slanja.
- Poruka o pogrešci prikazuje se ako se stvori trošak koji nije povezan s projektom.
- Kada se stvori vremenski unos, uloga resursa prema zadanim postavkama postaje neaktivna.
- Redci dnevnika povezani s opozvanim i izbrisanim troškom ne brišu se.
- U stavci **Brzo stvaranje obrasca za vremenski unos** ažurirajte prikaz **Popis projektnih zadataka** za promjenu zadanog prikaza datuma u datum početka zadatka.
- Kada stvarate vremenski unos iz kartice **Povezano** resursa koji se može rezervirati, vremenski se unos pogrešno stvara za prijavljenog korisnika umjesto za nadređeni resurs koji se može rezervirati.
- Nova su polja dodana u dijaloški okvir **Skupno odobrenje MDD**.

**Planiranje projekta**

Popravljeni su sljedeći problemi:
- Spora izvedba stvaranja projekta kada se primjenjuju predlošci radnog vremena projekta sa složenim kalendarima.
- Kada je datum početka veći od datuma završetka, na predlošku za kopiranje projekta prikazuje se pogreška zbog razlika u vremenskoj komponenti svakog polja.

**Upravljanje resursima**

Popravljeni su sljedeći problemi:
- Neispravan parametar upotrebljava se u upitu za uporabu resursa, a XML dovodi do netočnih rezultata filtra na rešetki **Uporaba resursa**.
- Potvrda **Produži rezervacije** prikazuje netočan datum završetka za rezervacije.

**Prodaje**

Popravljeni su sljedeći problemi:
- Prikazuje se poruka o pogrešci ako se cijena kategorije stvara s vrijednostima koje nedostaju.
- Prikazuje se poruka o pogrešci ako se kontrolna točka u retku ugovora stvara bez retka narudžbe.
