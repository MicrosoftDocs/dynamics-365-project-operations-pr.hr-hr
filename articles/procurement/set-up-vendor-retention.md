---
title: Postavljanje zadržavanja dijela uplate dobavljaču
description: U ovoj se temi objašnjava način postavljanja zadržavanja dijela uplate dobavljaču.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9511da6212aafbf5b173efc6eb1ceaacbc8264a2
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594572"
---
# <a name="set-up-vendor-retention"></a>Postavljanje zadržavanja dijela uplate dobavljaču

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovoj temi nalaze se informacije o načinu postavljanja zadržavanja dijela uplate dobavljaču.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Postavljanje računa za zadržavanje dijela uplate dobavljaču u Glavnoj knjizi

1. U aplikaciji Dynamics 365 Finance, idite na **Glavna knjiga** > **Postavljanje knjiženja** > **Računi za automatske transakcije**.
2. Dodajte novi redak.
3. U polju **Vrsta knjiženja** odaberite **Zadržavanje dijela uplate dobavljaču**.
4. Odaberite glavni račun za knjiženje zadržavanja dijela uplate dobavljaču.

## <a name="create-vendor-retention-terms"></a>Stvaranje rokova za zadržavanje dijela plaćanja dobavljaču

Upotrijebite stranicu **Rokovi za zadržavanje dijela plaćanja dobavljaču** za postavljanje i održavanje rokova za zadržavanje plaćanja dobavljaču. Unesite postotak zadržavanja plaćanja dobavljaču i postotak prethodno zadržanih iznosa koji se trebaju osloboditi. Iznosi se automatski zadržavaju od faktura dobavljača sve dok ugovor ne dosegne određeno stanje završenosti. Nakon što se za dobavljača postave rokovi za zadržavanje, možete ih primijeniti na bilo koji projekt na kojem dobavljač radi.

1. U aplikaciji Finance idite na **Upravljanje projektima i računovodstvo** > **Postavljanje** > **Zadržavanje** > **Rokovi za zadržavanje plaćanja dobavljaču**.
2. Odaberite **Novo** kako biste dodali novi uvjet za zadržavanje plaćanja dobavljaču. Vrijednost u polju **ID pravila** za novi uvjet unosi se automatski. 
3. U polje **Opis** unesite opisni naziv novog uvjeta.
4. Na kartici **Uvjeti** odaberite **Dodaj redak** za unos roka za zadržavanje dijela plaćanja dobavljaču.
5. U polje **Postotak isporučenih jedinica** unesite postotak dovršenosti pravila. Iznosi se automatski zadržavaju na fakturama dobavljača sve dok se faza završetka projekta ne izjednači s postotkom koji unesete. Na primjer, ako unesete 50,00, iznosi se zadržavaju sve dok projekt ne bude završen 50 posto.
6. U polje **Postotak za zadržavanje** unesite postotak iznosa fakture dobavljača koji treba zadržati. Na primjer, ako unesete 10,00 u ovo polje, 10 posto iznosa na fakturama dobavljača zadržava se sve dok projekt ne dosegne postotak završetka koji odaberete u polju **Postotak isporučenih jedinica**.
7. U polje **Postotak za oslobađanje** unesite postotak prethodno zadržanih iznosa koji se oslobađaju na odabranoj razini završetka projekta.

> [!NOTE]
> Ako imate više od jedne kontrolne točke za različite razine završetka projekta, unesite zaseban redak za rok zadržavanja dijela plaćanja dobavljaču za svako pravilo zadržavanja. Za svaki redak može se odrediti drugačiji postotak za zadržavanje i postotak za oslobađanje za svaku naznačenu razinu završetka projekta.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Postavljanje ugovora s dobavljačem za projekt

Postavite rokove za zadržavanje dijela plaćanja dobavljaču koji se primjenjuju na projekt. Uvjeti zadržavanja plaćanja dobavljaču prikazuju se i na narudžbenicama koje stvarate za dobavljača.

1. U aplikaciji Finance idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Svi projekti**. 
2. Odaberite projekt, a zatim na Oknu s radnjama odaberite **Projektna grupa** > **Ugovori s dobavljačima**.
3. Na stranici **Ugovori s dobavljačima** dodajte novi redak.
4. U polju **Kod računa** odaberite jednu od sljedećih mogućnosti:
   - **Tablica**: Uvjeti zadržavanja plaćanja dobavljaču primjenjuju se na pojedinog dobavljača.
   - **Grupa**: Uvjeti zadržavanja plaćanja dobavljaču primjenjuju se na sve dobavljače u grupi dobavljača.
   - **Svi**: Uvjeti zadržavanja plaćanja dobavljaču primjenjuju se na sve dobavljače.
5. U polju **Dobavljač / grupa dobavljača** odaberite dobavljača ili grupu dobavljača na koje se primjenjuju rokovi za zadržavanje plaćanja. Ako ste u prethodnom koraku odabrali **Svi**, ovo polje nije dostupno.
6. U polju **Rokovi za zadržavanje dijela plaćanja dobavljaču** odaberite ID pravila za rokove zadržavanja koji će se primijeniti na ovog dobavljača.

