---
title: Naručivanje materijala koji nisu na zalihama za projekte s pomoću narudžbenica za projekt
description: U ovoj temi objašnjava se način naručivanja materijala koji nisu na zalihama za projekte s pomoću narudžbenica za projekt.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563013"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Naručivanje materijala koji nisu na zalihama za projekte s pomoću narudžbenica za projekt

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Odjel nabave u vašoj tvrtki ili ustanovi mogao bi upotrebljavati [narudžbenice](/dynamics365/supply-chain/procurement/purchase-order-overview) za praćenje narudžbi roba i usluga. Narudžbenice za materijale koji nisu na zalihama mogu se pripisati projektu. Pri fakturiranju ovih narudžbenica bilježe se troškovi projekta.

## <a name="prerequisites"></a>Preduvjeti
Poduzmite sljedeće korake kako biste omogućili funkcionalnost narudžbenica za projekt.

1. U aplikaciji Dynamics 365 Finance, idite na radni prostor **Upravljanje značajkama**.
2. Na popisu značajki pronađite i odaberite značajku, **Omogući narudžbenice za projekt u aplikaciji Project Operations za scenarije koji se temelje na resursima/bez zaliha**.
3. Odaberite opciju **Omogući**.
4. Konfigurirajte materijale koji nisu na zalihama i fakture dobavljača na čekanju kako je opisano u odjeljku [Konfiguriranje materijale koji nisu na zalihama i fakture dobavljača na čekanju](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Stvaranje narudžbenice za projekt s popisa narudžbenica za projekt

1. U aplikaciji Finance idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Svi projekti** i odaberite projekt.
2. U Oknu s radnjama, na kartici **Upravljanje**, u grupi **Novo**, odaberite **Zadatak stavke** > **Narudžbenica**.
3. Na stranici **Stvori narudžbenicu**, odaberite dobavljača kojem želite poslati narudžbenicu i prema potrebi unesite druge podatke, a zatim odaberite **U redu**.
4. Na stranici **Narudžbenica**, u rešetki **Redci narudžbenice**, odaberite **Dodaj redak**.
5. Unesite broj stavke, količinu, jedinicu, jediničnu cijenu i druge podatke prema potrebi.

    > [!NOTE]
    > S narudžbenicama za projekt mogu se upotrebljavati samo stavke i usluge koje nisu na zalihama. Uskladištene stavke i kategorije nabave nisu podržane.

6. Nastavite dodavati stavke prema potrebi i potvrdite narudžbenicu.

    Računi za robe i usluge mogu se evidentirati stvaranjem i knjiženjem računa za proizvod.

    > [!NOTE]
    > Računi za proizvode ne bilježe se u stvarne podatke o projektu u aplikaciji Microsoft Dataverse i ne utječu na sekundarnu knjigu projekta.

    Nakon što dobavljač pošalje račun za stavke i usluge u narudžbenici, odjel nabave može generirati fakturu za narudžbenicu tako što će otići na **Faktura** > **Generiraj** > **Faktura** u Oknu s radnjama. Dodatne informacije o fakturama dobavljača na čekanju potražite u odjeljku [Kupnja materijala koji nisu na zalihama s pomoću fakture dobavljača na čekanju](pending-vendor-invoices.md).
