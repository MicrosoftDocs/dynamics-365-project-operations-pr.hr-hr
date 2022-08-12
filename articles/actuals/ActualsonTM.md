---
title: Stvarni utjecaj u vremenu i angažmanu materijala
description: Ovaj članak pruža informacije o utjecaju na tablicu Actuals na različitim događajima tijekom životnog ciklusa vremena i angažmana materijala u Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 039700e61796bf77c7661e5269b6923101139a1e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923317"
---
# <a name="actuals-impact-in-a-time-and-materials-engagement"></a>Stvarni utjecaj u vremenu i angažmanu materijala

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

U sljedećoj su tablici navedene stvarne vrijednosti različitih vrsta transakcija koje se kreiraju na različitim događajima u vremenu i angažmanu materijala.

| Događaj | Stvarna vrijednost troškova | Stvarni podatak o nenaplaćenim prodajama | Stvarna naplaćena prodaja | Primjer |
|---|---|---|---|---|
| Vrijeme se stvara. | Nije primjenjivo | Nije primjenjivo | Nije primjenjivo | <p>Bob Kozack, iz američke organizacijske jedinice Fabrikam koja ima stopu troškova od 100 američkih dolara (100 USD) po satu, radi na projektu koji nosi naziv "Arm Installation at Adatum". Za ovaj projekt, njegova ugovorena stopa računa je USD 200 po satu. Evo oglednog vremenskog unosa Boba Kozaka:</p><p>Bob Kozack, 8 sati</p> |
| Vrijeme se šalje. | Nije primjenjivo | Nije primjenjivo | Nije primjenjivo | Za stavku vremena kreiraju se redak temeljnice troškova i neobjavljene temeljnice prodaje. Zadana cijena i stopa troška unose se u stavku temeljnice. |
| Unos vremena se opoziva prije nego što bude odobren. | Nije primjenjivo | Nije primjenjivo | Nije primjenjivo | |
| Vrijeme je odobreno: Poslani sati jednaki su naplativim satima. | Stvara se stvarni trošak. | Stvara se neograničeni iznos prodaje. | Nije primjenjivo | <p>Stvorene nove stvarne vrijednosti:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800</li><li>**Nenaplaćena prodaja stvarna:** Bob Kozack, 8 sati, USD 1,600</li></ul> |
| Vrijeme se odobrava: Naplativi sati smanjuju se ispod podnesenih sati. | Stvara se stvarni trošak. | <p>Kreiraju se dvije nenaplaćene vrijednosti prodaje:</p><ul><li>Stvarno naplaćena neplaćena prodaja za naplative sate</li><li>Nenaplaćena neplaćena vrijednost prodaje za preostalu količinu</li></ul> | Nije primjenjivo | <p>Stvorene nove stvarne vrijednosti:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800</li><li>**Nenaplaćena prodaja stvarna:** Bob Kozack, 6 sati, USD 1,200, *Chargeable*</li><li>**Neplaćena prodaja stvarna:** Bob Kozack, 2 sata, USD 400, *Nenaplativo*</li></ul> |
| Vrijeme se odobrava: Naplativi sati povećavaju se iznad podnesenih sati. | Stvara se stvarni trošak. | Stvara se neograničeni iznos prodaje. | Nije primjenjivo | <p>Stvorene nove stvarne vrijednosti:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800</li><li>**Nenaplaćena prodaja stvarna:** Bob Kozack, 10 sati, USD 2,000</li></ul> |
| Odobrenje vremena je otkazano. | <p>Status prilagodbe izvornog stvarnog troška obnavlja se u **Prilagođeno**.</p><p>Stvara se stvarni trošak storniranja koji ima status prilagodbe **nepravomoćno**.</p> | <p>Status prilagođavanja izvornog iznosa neplaćene prodaje obnavlja se u **Prilagođeno**.</p><p>Stvara se obrnuti nenaplaćeni iznos prodaje koji ima status prilagodbe neprepoznativ.**·**</p> | Nije primjenjivo | <p>Postojeće stvarne vrijednosti koje se ažuriraju:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800, *Prilagođeno*</li><li>**Neplaćena prodaja stvarna:** Bob Kozack, 8 sati, USD 1,600, *Prilagođeno*</li></ul><p>Nove stvarne vrijednosti stvorene za poništavanje prethodnog financijskog učinka:</p><ul><li>**Stvarni trošak:** Bob Kozack, (8 sati), (USD 800), *Nepravomoćno*</li><li>**Neisplativi stvarni iznos prodaje:** Bob Kozack, (8 sati), (1.600 USD), *Nepravomoćno*</li></ul> |
| Unos vremena opozvan je nakon što je odobren. | <p>Status prilagodbe izvornog stvarnog troška obnavlja se u **Prilagođeno**.</p><p>Stvara se stvarni trošak storniranja koji ima status prilagodbe **nepravomoćno**.</p> | <p>Status prilagođavanja izvornog iznosa neplaćene prodaje obnavlja se u **Prilagođeno**.</p><p>Stvara se obrnuti nenaplaćeni iznos prodaje koji ima status prilagodbe neprepoznativ.**·**</p> | Nije primjenjivo | <p>Postojeće stvarne vrijednosti koje se ažuriraju:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800, *Prilagođeno*</li><li>**Neplaćena prodaja stvarna:** Bob Kozack, 8 sati, USD 1,600, *Prilagođeno*</li></ul><p>Nove stvarne vrijednosti stvorene za poništavanje prethodnog financijskog učinka:</p><ul><li>**Stvarni trošak:** Bob Kozack, (8 sati), (USD 800), *Nepravomoćno*</li><li>**Neisplativi stvarni iznos prodaje:** Bob Kozack, (8 sati), (1.600 USD), *Nepravomoćno*</li></ul> |
| Ugovor je potvrđen. | <p>Status prilagodbe starih iznosa troškova obnavlja se u **Prilagođeno**.</p><p>Kreiraju se stvarni troškovi storniranja koji imaju status prilagodbe **nepravomoćno**.</p><p>Nove stvarne troškove stvaraju se nakon ponovne procjene ugovornih pravila.</p> | <p>Status prilagodbe starih neplaćenih iznosa prodaje obnavlja se u **Prilagođeno**.</p><p>Kreiraju se reverzne nenaplaćene prodajne stvarne vrijednosti koje imaju status prilagodbe **nepravomoćno**.</p><p>Nove nenaplaćene vrijednosti prodaje stvaraju se nakon ponovne procjene ugovornih pravila.</p> | Nije primjenjivo | <p>Postojeće stvarne vrijednosti koje se ažuriraju:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800, *Prilagođeno*</li><li>**Neplaćena prodaja stvarna:** Bob Kozack, 8 sati, USD 1,600, *Prilagođeno*</li></ul><p>Nove stvarne vrijednosti stvorene za poništavanje prethodnog financijskog učinka:</p><ul><li>**Stvarni trošak:** Bob Kozack, (8 sati), (USD 800), *Nepravomoćno*</li><li>**Neisplativi stvarni iznos prodaje:** Bob Kozack, (8 sati), (1.600 USD), *Nepravomoćno*</li></ul><p>Nove stvarne vrijednosti stvorene za ponovno procijenjeni financijski učinak:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800</li><li>**Nenaplaćena prodaja stvarna:** Bob Kozack, 8 sati, USD 1,600</li></ul> |
| Kreira se faktura. | Nije primjenjivo | Nije primjenjivo | Nije primjenjivo | |
| Račun je potvrđen. Količina u retku fakture nije promijenjena iz količine u iznosu u iznosu od neobnaplaćene prodaje. | Nije primjenjivo | <p>Ažurira se status fakture starog iznosa neplaćene prodaje.</p><p>Kreiraju se reverzne nenaplaćene prodajne stvarne vrijednosti koje imaju status prilagodbe **nepravomoćno**. | Kreira se naplaćena stvarna prodaja. | <p>Postojeća stvarna vrijednost koja ostaje nepromijenjena:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800</li></ul><p>Postojeća stvarna koja se ažurira:</p><ul><li>**Neplaćena prodaja stvarna:** Bob Kozack, 8 sati, USD 1,600, *Objavljen račun kupcu*</li></ul>Nova stvarna stvar koja se stvara kako bi se preokrenuo nedovršeni financijski rad (PUT):</p><ul><li>**Nenaplaćena stvarna prodaja:** Bob Kozack, (8 sati), (1.600 USD)</li></ul><p>Novo stvarno stvoreno za bilježenje naplaćenih vrijednosti prodaje:</p><ul><li>**Stvarna prodaja naplaćena:** Bob Kozack, 8 sati, USD 1,600</li></ul> |
| Faktura se potvrđuje nakon što se količina u retku fakture smanji od količine u iznosu na vrijednosti nenaplaćene prodaje. | Nije primjenjivo | <p>Status prilagođavanja izvornih neplaćenih iznosa prodaje obnavlja se u **Prilagođeno**.</p><p>Za izvorne nenaplaćene iznose prodaje kreiraju se reverzni nenaplaćeni iznosi prodaje. Imaju status prilagodbe **nepravomoćnog**.</p><p>Kreiraju se dva nova nenaplaćena prodajna broja:</p><ul><li>Stvarno naplaćena neplaćena prodaja za naplative sate</li><li>Nenaplaćena neplaćena vrijednost prodaje za preostalu količinu</li></ul><p>Za dvije nove nenaplaćene prodajne stvarne vrijednosti kreiraju se reverzni podaci o prodaji.</p> | <p>Kreiraju se dvije naplaćene vrijednosti prodaje:</p><ul><li>Naplaćena prodaja stvarna za naplative sate</li><li>Stvarno naplaćena prodaja koja se ne naplaćuje za preostalu količinu</li></ul> | <p>Postojeća stvarna vrijednost koja ostaje nepromijenjena:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800</li></ul><p>Postojeća stvarna koja se ažurira:</p><ul><li>**Neplaćena prodaja stvarna:** Bob Kozack, 8 sati, USD 1,600, *Prilagođeno*</li></ul><p>Nova stvarna vrijednost stvorena za storniranje prethodnog financijskog PUT-a:</p><ul><li>**Neisplativi stvarni iznos prodaje:** Bob Kozack, (8 sati), (1.600 USD), *Nepravomoćno*</li></ul><p>Nove stvarne vrijednosti stvorene za bilježenje ažuriranog prodajnog PUT-a:</p><ul><li>**Nenaplaćena prodaja stvarna:** Bob Kozack, 6 sati, USD 1,200, *Chargeable*</li><li>**Neplaćena prodaja stvarna:** Bob Kozack, 2 sata, USD 400, *Nenaplativo*</li></ul><p>Nove stvarne vrijednosti kreirane za storniranje ažuriranog PRODAJNOG PUT-a:</p><ul><li>**Nenaplaćena stvarna prodaja:** Bob Kozack, (6 sati), (USD 1,200), *Chargeable*</li><li>**Nenaplaćena stvarna prodaja:** Bob Kozack, (2 sata), (USD 400), *Nenaplativo*</li></ul><p>Nove stvarne vrijednosti kreirane za bilježenje naplaćenih prodajnih vrijednosti:</p><ul><li>**Naplaćena stvarna prodaja:** Bob Kozack, 6 sati, USD 1,200, *Naplativo*</li><li>**Stvarna naplaćena prodaja:** Bob Kozack, 2 sata, USD 400, *Nenaplativo*</li></ul> |
| Faktura se potvrđuje nakon što se količina u retku fakture poveća od količine u iznosu u nenaplaćenoj prodaji. | Nije primjenjivo | <p>Status prilagođavanja izvornih neplaćenih iznosa prodaje obnavlja se u **Prilagođeno**.</p><p>Za izvorne nenaplaćene iznose prodaje kreiraju se reverzni nenaplaćeni iznosi prodaje. Imaju status prilagodbe **nepravomoćnog**.</p><p>Za novu količinu kreiraju se novi nenaplaćeni podaci o prodaji.</p><p>Za nove nenaplaćene prodajne stvarne vrijednosti kreiraju se reverzni nenaplaćeni iznosi prodaje.</p> | Za novu količinu kreiraju se naplaćeni iznosi prodaje. | <p>Postojeća stvarna vrijednost koja ostaje nepromijenjena:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800</li></ul><p>Postojeća stvarna koja se ažurira:</p><ul><li>**Neplaćena prodaja stvarna:** Bob Kozack, 8 sati, USD 1,600, *Prilagođeno*</li></ul><p>Nova stvarna vrijednost stvorena za storniranje prethodnog financijskog PUT-a:</p><ul><li>**Neisplativi stvarni iznos prodaje:** Bob Kozack, (8 sati), (1.600 USD), *Nepravomoćno*</li></ul><p>Nova stvarna stvar stvorena za bilježenje ažuriranog prodajnog PUT-a:</p><ul><li>**Unbilled prodaja stvarni:** Bob Kozack, 10 sati, USD 2,000, *Chargeable*</li></ul><p>Nova stvarna koja je stvorena da bi se stornirao ažurirani prodajni PUT:</p><ul><li>**Neplaćena stvarna prodaja:** Bob Kozack, (10 sati), (USD 2,000), *Chargeable*, *Nepravomoćno*</li></ul><p>Novo stvarno stvoreno za bilježenje naplaćenih vrijednosti prodaje:</p><ul><li>**Stvarna naplaćena prodaja:** Bob Kozack, 10 sati, USD 2,000, *Naplativo*</li></ul> |
| Faktura se ispravlja kako bi se smanjila količina ili cijena za naplatu. | Nije primjenjivo | <p>Kreiraju se dvije nenaplaćene vrijednosti prodaje:</p><ul><li>Naplativi iznos neplaćene prodaje za kol.</li><li>Naplativi iznos neplaćene prodaje za preostalu količinu</li></ul><p>Za dvije nove nenaplaćene prodajne stvarne vrijednosti kreiraju se reverzni podaci o prodaji.</p> | <p>Kreiraju se naplaćene vrijednosti prodaje storniranja.</p><p>Za novu količinu kreiraju se nove naplaćene vrijednosti prodaje. | <p>Postojeće stvarne vrijednosti koje ostaju nepromijenjene:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800</li><li>**Neplaćena prodaja stvarna:** Bob Kozack, 8 sati, USD 1,600, *Objavljen račun kupcu*</li><li>**Nenaplaćena stvarna prodaja:** Bob Kozack, (8 sati), (1.600 USD)</li></ul><p>Postojeća stvarna koja se ažurira:</p><ul><li>**Stvarna naplaćena prodaja:** Bob Kozack, (8 sati), (USD 1,600) *Prilagođeno*</li></ul><p>Novo stvarno stvoreno za storniranje prethodnih naplaćenih prodajnih vrijednosti:</p><ul><li>**Stvarna naplaćena prodaja:** Bob Kozack, (8 sati), (USD 1,600) *Nepravomoćno*</li></ul><p>Nove stvarne vrijednosti kreirane za bilježenje ispravljenog prodajnog PUT-a:</p><ul><li>**Nenaplaćena prodaja stvarna:** Bob Kozack, 6 sati, USD 1,200, *Naplativo*, *Objavljena faktura kupca*</li><li>**Unbilled prodaja stvarni:** Bob Kozack, 2 sata, USD 400, *Chargeable*</li></ul><p>Nova stvarna koja se kreira za storniranje ispravljenog prodajnog PUT-a:</p><ul><li>**Nenaplaćena stvarna prodaja:** Bob Kozack, (6 sati), (1.200 USD), *Naplaćuje se*, *nepravomoćno*</li></ul><p>Nova stvarna koja se stvara da bi se zabilježile ispravljene naplaćene vrijednosti prodaje:</p><ul><li>**Naplaćena stvarna prodaja:** Bob Kozack, 6 sati, USD 1,200, *Naplativo*</li></ul> |
| Faktura se ispravlja kako bi se povećala količina ili cijena za naplatu. | Nije primjenjivo | <p>Za novu količinu kreiraju se novi neplaćeni podaci o prodaji.</p> <p>Za nove nenaplaćene prodajne stvarne vrijednosti kreiraju se reverzni nenaplaćeni iznosi prodaje.</p> | <p>Kreiraju se naplaćene vrijednosti prodaje storniranja.</p>Za novu količinu kreiraju se nove naplaćene vrijednosti prodaje.</p> | <p>Postojeće stvarne vrijednosti koje ostaju nepromijenjene:</p><ul><li>**Stvarni trošak:** Bob Kozack, 8 sati, USD 800</li><li>**Neplaćena prodaja stvarna:** Bob Kozack, 8 sati, USD 1,600, *Objavljen račun kupcu*</li><li>**Nenaplaćena stvarna prodaja:** Bob Kozack, (8 sati), (1.600 USD)</li></ul><p>Postojeća stvarna koja se ažurira:</p><ul><li>**Stvarna naplaćena prodaja:** Bob Kozack, (8 sati), (USD 1,600) *Prilagođeno*</li></ul><p>Novo stvarno stvoreno za storniranje prethodnih naplaćenih prodajnih vrijednosti:</p><ul><li>**Stvarna naplaćena prodaja:** Bob Kozack, (8 sati), (USD 1,600) *Nepravomoćno*</li></ul><p>Nova stvarna koja se kreira za bilježenje ispravljenog prodajnog PUT-a:</p><ul><li>**Neplaćena prodaja stvarna:** Bob Kozack, 10 sati, USD 2,000, *Naplativo*, *Objavljena faktura kupca*</li></ul><p>Nova stvarna koja se kreira za storniranje ispravljenog prodajnog PUT-a:</p><ul><li>**Nenaplaćena stvarna prodaja:** Bob Kozack, (10 sati), (USD 2,000), *Chargeable*</li></ul><p>Nova stvarna koja se stvara da bi se zabilježile ispravljene naplaćene vrijednosti prodaje:</p><ul><li>**Stvarna naplaćena prodaja:** Bob Kozack, 10 sati, USD 2,000, *Naplativo*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]