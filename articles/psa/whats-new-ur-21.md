---
title: Novosti ili izmjene u aplikaciji Project Service Automation, izdanje ažuriranja 21, V3
description: U ovoj se temi navode značajke i ispravke dostupne u rješenju Project Service Automation, izdanje ažuriranja 21, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: e7bf9d5c85d2fab0d17c435bdd96057c0c80be8f41b16f94afe6b1f554e7a9fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6984728"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation, izdanje ažuriranja 21, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je najaviti najnovije ažuriranje aplikacije Project Service Automation za sustav Dynamics 365. Ovo izdanje uključuje neka bitna poboljšanja kvalitete, značajki i upotrebljivosti. Ovo je izdanje kompatibilno sa sustavom Dynamics 365 9.x. Kako biste ažurirali ovo izdanje, posjetite stranicu Centra za administratore za sustav Dynamics 365 s rješenjima na mreži, kako biste instalirali ažuriranje. Dodatne informacije potražite u članku [Instaliranje, ažuriranje ili uklanjanje željenog rješenja](/power-platform/admin/install-remove-preferred-solution).

Ova tema navodi značajke i ispravke koje su nove ili promijenjene u aplikaciji Project Service Automation V3, izdanje ažuriranja 21. Ova verzija ima broj međuverzije V 3.10.32.50 i uglavnom je dostupna putem samostalnog ažuriranja u lipnju 2020. godine.

## <a name="update-release-21"></a>Izdanje ažuriranja 21

### <a name="bug-fixes"></a>Ispravke pogrešaka

**Vrijeme i trošak**

Popravljeni su sljedeći problemi:

- Tijekom hostiranja **Kontrole rešetke unosa vremena** na nadzornim pločama, rešetka ne upotrebljava cijelu širinu spremnika rešetke nadzorne ploče.
- Za određene vremenske zone kontrola rešetke **Vremenski unos** ne prikazuje zapise.
- Vremenski unosi koji slijede nakon 21:00 prikazuju se pogrešnog dana.
- Korisnici ne mogu poslati troškove ako kategorija troškova **Potrebna je potvrda o troškovima** nema vrijednost.

**Upravljanje resursima**

Popravljeni su sljedeći problemi:

- Neaktivne rezervacije prikazuju su u prozoru **Usklađivanje**.
- Za ispunjenje generičkih resursa nedostajala je provjera valjanosti kako bi se osiguralo postojanje valjanog statusa rezervacije.

**Upravljanje projektom**

Popravljeni su sljedeći problemi:

- Rešetke obrasca **Projekta** (**Dodjela resursa**, **Zadatak**, prikaz **Usklađivanja**, **Procjene troškova**) mogu se i dalje uređivati i kad projekt nije aktivan.
- Duplicirani klijenti ne mogu se spojiti s klijentima koji su povezani s potvrđenim projektnim ugovorima.
- Kada se doda resurs koji nema valjani kalendar, sustav ne vraća poruku o pogrešci prilagođenu korisniku.
- Gumb **Dodaj zadatak** na rešetki zadataka omogućen je kad je projekt povezan s **Dodatkom aplikacije Microsoft Project**.
- Napor nekontrolirano raste kada je zadatak s kategorijom dodijeljen resursu s ulogom za koju je definirana cijena koštanja.

**Sales**

Napravljena su sljedeća poboljšanja:

- **Učestalost fakture** i **Početak naplate** preseljeni su u karticu **Raspored faktura**.

Popravljeni su sljedeći problemi:

- **Ukupna prodajna cijena** je nula (0) za **Kategoriju** čak i ako **Uloga** ima ukupnu prodajnu cijenu koja nije nula.
- Klijenti ne mogu mijenjati vrijednost polja **Status fakture** u **Spremno za fakturiranje** kada neki drugi prilagođeni postupak ažurira dodatno polje.
- Gumb **Osvježi retke fakture** može stvoriti više dupliciranih redaka ako se uzastopno odabire.
- Gumb **Ažuriraj cijene** ne radi u podrešetki **Cijene uloga** u obrascu **Brzi pogled**.
- Logika **Razlučivosti cjenika prodaje** nepravilno upravlja vremenskim zonama, što dovodi do pogrešnog odabira cjenika.
- **Ukupni stvarni trošak** projekta može se isključiti djelomičnim iznosom nakon što se odobri pojedinačni unos.
- Logika **Razlučivosti cijene** ne daje poruku o pogrešci prilagođenu korisniku ako **Dohvaćena CijenaUloge** nema vrijednosti u poljima **„Primarna jedinica”** i **„Cijena u primarnoj jedinici”**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]