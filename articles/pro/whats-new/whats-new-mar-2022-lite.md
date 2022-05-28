---
title: Novosti u ožujku 2022. – osnovna implementacija aplikacije Project Operations
description: Ova tema pruža informacije o ažuriranjima kvalitete koja su dostupna u izdanju implementacije lite projekta Project Operations u ožujku 2022.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583741"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Novosti u ožujku 2022. – osnovna implementacija aplikacije Project Operations

_Odnosi se na: Osnovna implementacija – od sklapanja posla do predračuna_

Ovaj tema odnosi se na sljedeće microsoftove Dynamics 365 Project Operations komponente i verzije :

- Operacije projekta u verziji okruženja Dataverse 4.30.0.99

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

- Podugovaranje: Kreiranje fakture dobavljača i podudarna iskustva

## <a name="quality-updates"></a>Ažuriranja kvalitete

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Vrijeme i trošak | 2388011 | Prikažite komentare odbijanja podnositeljima unosa vremena tijekom masovnog odobrenja. |
| Planiranje i praćenje projekta | 2495294 | Pojedinosti o projektu ne smiju se moći uređivati na stranici Detalji o **zadatku**. |
| Naplata i određivanje cijene | 2499605 | Ključne etape ugovora stvorene iz ključnih etapa ponude pogrešno su označene samo za čitanje. |
| Planiranje i praćenje projekta | 2506050 | Skup operacija ostaje na čekanju jedan sat ako nema promjene za spremanje. Skup je zatim lažno označen kao **Neuspješan**, dok bi ga trebalo odmah dovršiti. |
| Naplata i određivanje cijene | 2507401 | Zadane ugovorne jedinice pogrešno se unose u projekte zbog pogrešnog predmemoriranja. |
| Naplata i određivanje cijene | 2541660 | **Provjera valjanosti stvaranja naloga za** prodaju u dvostrukom pisanju trebala bi biti samo za narudžbe temeljene na projektima. |
| Naplata i određivanje cijene | 2552745 | Porez se ne dijeli između korisnika koji su postavili podijeljena pravila naplate. |
| Naplata i određivanje cijene | 2558859 | Poboljšane poruke o pogreškama prilikom postavljanja dimenzija određivanja cijena. |
| Naplata i određivanje cijene | 2558933 | **Uvoz iz procjena** projekta ne uspijeva kada **se msdyn\_ projekt** doda kao dimenzija određivanja cijena. |
| Naplata i određivanje cijene | 2559101 | Brisanje parametara projekta nije blokirano i uzrokuje probleme. |
|   Upravljanje prilikama | 2570390 | Dodatak s dvostrukim pisanjem prisiljava vrstu računa na ponude, narudžbe i prilike da bude **kupac**, čak i kada ta vrsta računa nije točna. |
| Naplata i određivanje cijene | 2586097 | Stvarni podijeljeni naplaćeni troškovi ne storniraju se kada se projekt ukloni iz retka ugovora o projektu. |
| Naplata i određivanje cijene | 2589619 | Porez na dopisni materijal prenosi se na neplaćene prodajne stvarne vrijednosti i račun. |
|   Upravljanje prilikama | 2594015 | Ponuda se ne može zatvoriti kao osvojena za korisnike koji imaju **Uvjete plaćanja Net60**. |
| Planiranje i praćenje projekta | 2595841 | U programu Project za web korisnici dobivaju poruku o pogrešci o stvarnom pokretanju **msdyna\_ koji nedostaje** prilikom stvaranja novog zahtjeva za resursom. |
| Vrijeme i trošak | 2602511 | Polje **Odbijeno po** za unose vremena prikazuje **Sustav** umjesto imenovanog korisnika kao odbijanje. |
| Vrijeme i trošak | 2602528 | Odobravatelj projekta može odobriti vrijeme na projektima u kojima nisu navedeni kao odobravatelj. |
| Naplata i određivanje cijene | 2608550 | Ispravak fakture može se potvrditi čak i ako nema promjena u izvorniku. |

## <a name="removed-and-deprecated-features"></a>Uklonjene i zastarjele značajke

Uklonjene [ili zastarjele značajke u projektnim operacijama](../../whats-new/removed-depreciated-features-project.md) tema opisuju značajke koje su uklonjene ili zastarjele za Dynamics 365 Project Operations.

- Značajka uklonjeno više nije dostupna u proizvodu.
- Zastarjela značajka nije u aktivnom razvoju i može se ukloniti u budućem ažuriranju.

Najava omalovažavanja pojavit će se u [značajkama Uklonjeno ili zastarjelo u projektnim operacijama](../../whats-new/removed-depreciated-features-project.md) tema 12 mjeseci prije nego što se bilo koja značajka ukloni iz proizvoda.
