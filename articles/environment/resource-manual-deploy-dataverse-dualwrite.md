---
title: Ručna implementacija aplikacije Project Operations Dataverse s podrškom za dvostruko pisanje
description: U ovoj se temi objašnjava način na koji se vrši ručna implementacija aplikacije Project Operations Dataverse tako da podržava dvostruko pisanje.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 06325a9a9f9084d1f506f2493c32565fe7b7c52ae6fe22c81339b9c1d632e688
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986437"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Ručna implementacija aplikacije Project Operations Dataverse s podrškom za dvostruko pisanje

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

U ovoj se temi objašnjava način na koji se vrši ručna implementacija aplikacije Microsoft Dynamics 365 Project Operations na platformi Microsoft Dataverse tako da podržava dvostruko pisanje. Project Operations otkriva konfiguraciju okruženja i dodaje dodatnu podršku za dvostruko pisanje ako se ispune preduvjeti.

Ako ste, tijekom implementacije putem sustava Microsoft Dynamics Lifecycle Services (LCS), slijedili upute navedene u ovoj temi, možete preskočiti implementaciju integracije aplikacije Microsoft Power Platform (prethodno znana kao okruženje platforme Common Data Service).

Postupak implementacije aplikacije Project Operations na platformu Dataverse tako da podržava dvostruko pisanje ima četiri glavna koraka:

1. [Stvorite novo okruženje na platformi Dataverse koje podržava dvostruko pisanje](#create).
2. [Okruženju dodajte preduvjete za dvostruko pisanje](#prerequisites).
3. [Dodajte aplikaciju Project Operations Dataverse](#dataverse).
4. [Povežite svoja okruženja](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Stvaranje novog okruženja na platformi Dataverse koje podržava dvostruko pisanje

Kako biste dovršili ovaj postupak, morate se prijaviti kao administrator.

1. Otvorite [Centar za administratore aplikacije Power Platform](https://admin.powerplatform.com) i prijavite se kao administrator.
2. Stvorite novo okruženje i dajte mu naziv.
3. Odaberite vrstu okruženja. Ako ste se prijavili za ponudu probne verzije, odaberite **Probna verzija (na temelju pretplate)**.
4. Potvrdite područje implementacije.
5. Omogućite mogućnost **Stvori bazu podataka za ovo okruženje**. 
6. Potvrdite jezik, a zatim potvrdite da se valuta podudara s valutom vaših aplikacija Finance and Operations.
7. Omogućite mogućnost **Aplikacije sustava Dynamics 365** i potvrdite da je polje **Automatski postavi ove aplikacije** postavljeno na **Nijedna**.
8. Dodajte sigurnosnu grupu ako je potrebna.
9. Odaberite **Spremi** kako biste stvorili okruženje.
10. Pričekajte dok se implementacija ne dovrši i okruženje ne dosegne stanje **Spremno**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Okruženju dodajte preduvjete za dvostruko pisanje.

Podrška za dvostruko pisanje uključuje dodatna polja koja se dodaju ključnim entitetima, poput entiteta **Tvrtka**. Ako podršku za dvostruko pisanje dodajete u postojeće okruženje, možda ćete morati ažurirati podatke kako biste je omogućili. Informacije o načinu samopokretanja podataka potražite u odjeljku [Samopokretanje podataka tvrtke](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Dodatne informacije o dvostrukom pisanju potražite u odjeljku [Preduvjeti sustava za dvostruko pisanje](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Dovršite ovaj postupak kako biste svojem okruženju dodali preduvjete za dvostruko pisanje.

1. Otvorite okruženje koje ste upravo stvorili, a zatim idite na **Resurs** \> **Aplikacije sustava Dynamics 365**.
2. Odaberite stavku **Osnovno rješenje za dvostruko pisanje** na popisu aplikacija i instalirajte ga.
3. Pričekajte dok se instalacija ne dovrši. Tada na popisu aplikacija odaberite stavku **Rješenje za upravljanje aplikacijom dvostrukog pisanja** i instalirajte ga.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Dodavanje aplikacije Project Operations Dataverse

Ovaj postupak možete dovršiti samo ako ste dovršili prethodne postupke prije nego što ste instalirali aplikaciju Project Operations. Tijekom instalacije sustav analizira konfiguraciju okruženja i, ako je potrebna, dodaje podršku za dvostruko pisanje.

1. Otvorite okruženje koje ste ranije stvorili, a zatim idite na **Resurs** \> **Aplikacije sustava Dynamics 365**.
2. Odaberite stavku **Microsoft Dynamics 365 Project Operations** na popisu aplikacija i instalirajte je.

## <a name="link-your-environments"></a><a name="link"></a>Povezivanje svojih okruženja

Nakon implementacije okruženja platforme Dataverse, možete postaviti vezu u svojim aplikacijama Finance and Operations. Slijedite korake navedene u odjeljku [Uporaba čarobnjaka za dvostruko pisanje za povezivanje svojih okruženja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
