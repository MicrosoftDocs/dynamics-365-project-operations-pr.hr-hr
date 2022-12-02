---
title: Novosti u ožujku 2022. – osnovna implementacija aplikacije Project Operations
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju osnovne implementacije aplikacije Project Operations za ožujak 2022.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934219"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Novosti u ožujku 2022. – osnovna implementacija aplikacije Project Operations

_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.30.0.99

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

- Podugovaranje: izrada faktura dobavljača i usklađivanje iskustava

## <a name="quality-updates"></a>Ažuriranja kvalitete

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Vrijeme i trošak | 2388011 | Prikaži komentare odbijanja podnositeljima unosa vremena tijekom skupnog odobrenja. |
| Planiranje i praćenje projekta | 2495294 | Detalji projekta ne smiju se moći uređivati na stranici **Detalji zadatka**. |
| Naplata i određivanje cijene | 2499605 | Ključne točke ugovora koje su stvorene iz ključnih točaka ponude neispravno su označene kao samo za čitanje. |
| Planiranje i praćenje projekta | 2506050 | Skup operacija ostaje na čekanju jedan sat ako nema promjena za spremanje. Skup je tada lažno označen kao **Neuspjeh** iako bi trebao biti dovršen odmah. |
| Naplata i određivanje cijene | 2507401 | Zadane ugovorne jedinice netočno su unesene u projekte zbog netočnog predmemoriranja. |
| Naplata i određivanje cijene | 2541660 | **Provjera valjanosti izrade prodajnog naloga** u dvostrukom pisanju treba biti samo za narudžbe temeljene na projektu. |
| Naplata i određivanje cijene | 2552745 | Porez se ne dijeli među kupcima koji su postavili pravila podijeljene naplate. |
| Naplata i određivanje cijene | 2558859 | Poboljšane poruke o pogrešci kada se postavljaju dimenzije cijena. |
| Naplata i određivanje cijene | 2558933 | **Uvoz iz procjena projekta** ne uspije kada se **msdyn\_project** dodaje kao dimenzija cijene. |
| Naplata i određivanje cijene | 2559101 | Brisanje parametara projekta nije blokirano i uzrokuje probleme. |
|   Upravljanje prilikama | 2570390 | Dodatak za dvostruko pisanje prisiljava vrstu računa za ponude, narudžbe i prilike da bude **Kupac**, čak i kada ta vrsta računa nije ispravna. |
| Naplata i određivanje cijene | 2586097 | Stvarne vrijednosti podijeljenog naplaćenog troška ne poništavaju se kada se projekt ukloni iz retka ugovora o projektu. |
| Naplata i određivanje cijene | 2589619 | Porez na upisani materijal prenosi se na stvarne vrijednosti nenaplaćene prodaje i fakturu. |
|   Upravljanje prilikama | 2594015 | Ponuda se ne može zatvoriti kao dobivena za kupce koji imaju uvjete plaćanja **Net60**. |
| Planiranje i praćenje projekta | 2595841 | U aplikaciji Project for the Web korisnici dobivaju poruku o pogrešci o nedostatku **msdyn\_actualstart** kada kreiraju novi zahtjev za resurs. |
| Vrijeme i trošak | 2602511 | Polje **Odbijen od strane** za unose vremena prikazuje **Sustav** umjesto imenovanog korisnika kao onog koji je odbio. |
| Vrijeme i trošak | 2602528 | Osoba koja odobrava projekte može odobriti vrijeme za projekte za koje nije navedena kao osoba koja odobrava. |
| Naplata i određivanje cijene | 2608550 | Ispravak računa može se potvrditi čak i ako nema promjena na izvorniku. |

## <a name="removed-and-deprecated-features"></a>Uklonjene i zastarjele značajke

Članak [Uklonjene ili zastarjele značajke u aplikaciji Project Operations](../../whats-new/removed-depreciated-features-project.md) opisuje značajke koje su uklonjene ili zastarjele za aplikaciju Dynamics 365 Project Operations.

- Značajka uklonjeno više nije dostupna u proizvodu.
- Značajka zastarjelo ne nalazi se u aktivnom razvoju i u nekom budućem ažuriranju može biti uklonjena.

Obavijest o zastarjelosti pojavit će se u članku [Uklonjene ili zastarjele značajke u aplikaciji Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 mjeseci prije uklanjanja bilo koje značajke iz proizvoda.
