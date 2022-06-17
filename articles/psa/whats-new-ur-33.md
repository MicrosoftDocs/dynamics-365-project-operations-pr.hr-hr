---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 33, V3
description: U ovom se članku navode značajke i popravci dostupni u ažuriranju ažuriranja automatizacije usluge project servicea 33, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: d9c282e8b95b111ce71fb441e4dbb2d04f904e0f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915407"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 33, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je objaviti najnovije ažuriranje aplikacije Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Kompatibilno je sa sustavom Dynamics 365 9.x. Kako biste ažurirali na ovo izdanje, posjetite stranicu Centar za administratore za rješenja sustava Dynamics 365 na mreži i instalirajte ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

U ovom se članku navode značajke i popravci koji su novi ili promijenjeni za automatizaciju usluga projekta V3, Ažuriraj izdanje 33. Ova verzija ima broj izdanja V3.10.54.98 i općenito je dostupna putem samostalnog ažuriranja u srpnju 2021. godine.

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
