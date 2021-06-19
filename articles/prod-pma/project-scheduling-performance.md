---
title: Učinkovitost planiranja projektnih resursa
description: U ovoj temi nalaze se informacije o tome kako poboljšati učinkovitost planiranja resursa za velik broj projekata.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 113023909f88cb4dd498190ef21b6955482b25dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010012"
---
# <a name="project-resource-scheduling-performance"></a>Učinkovitost planiranja projektnih resursa

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Problemi učinkovitosti koji se odnose na planiranje resursa mogu se pojaviti kada broj projekata dosegne tisuće. Kako biste poboljšali učinkovitost planiranja resursa, dostupna je značajka koja omogućuje korisnicima da smanje vrijeme potrebno za pokretanje obrasca dostupnosti resursa. Točnije, ovo uklanja postupak skupnog usklađivanja kapaciteta resursa i upotrebljava tablicu **ResProjectResource** za ubrzavanje pretraživanja resursa. Imajte na umu kako se tablica **ResRollup** više neće upotrebljavati.

> [!IMPORTANT]
> Ako postoji ovisnost ili o procesu skupne sinkronizacije kapaciteta resursa ili o tablici **ResProjectResource**, nemojte upotrebljavati ovu značajku.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Omogućivanje poboljšanje učinkovitosti planiranja resursa
Kako biste omogućili poboljšanje učinkovitosti planiranja resursa, poduzmite sljedeće korake.

1. Idite na **Upravljanje značajkama** > **Sve** i na popisu značajki pronađite **Omogući značajku poboljšanja učinkovitosti planiranja resursa projekta**.
2. Odaberite **Omogući odmah**.

> [!NOTE]
> Ako na popisu ne možete pronaći značajku, odaberite **Provjerite ima li ažuriranja** za osvježavanje popisa.

3. Osvježite svoj preglednik, a zatim idite na **Upravljanje projektima i računovodstvo** > **Povremeno** > **Resursi projekta** > **Sinkroniziraj kapacitet kalendara resursa u svim tvrtkama**.
4. Mogućnost **Ukloni postojeće zapise o kapacitetu** postavite na **Da** za uklanjanje prethodnih podataka. Ako želite generirati inkrementalne podatke, postavite mogućnost na **Ne**.
5. U polju **Kod razdoblja** odaberite razdoblje u kojem će se generirati podaci. Ako odaberete kod razdoblja, datumi početka i završetka ne moraju biti definirani.
6. Ako polje **Kod razdoblja** ostavite prazno, odaberite određene datume početka i završetka za generiranje podataka.
7. Odaberite **U redu**.

 > [!NOTE]
 > Ovim će se u tablicu **ResCalendarCapacity** opći podaci distribuirati u sve tvrtke vašeg okruženja, tako da skupni posao treba izvoditi samo u jednoj pravnoj osobi. Podaci u ovom skupnom poslu potrebni su za izračunavanje kapaciteta resursa putem povezanog kalendara.

8. Idite na **Upravljanje projektima i računovodstvo** > **Povremeno** > **Resursi projekta** > **Popuni projektne resurse u svim tvrtkama**, a zatim odaberite **U redu**. Ovo je skripta za nadogradnju podataka za opće podatke u tablicama **ResProjectResource**, **ResCalendarDateTimeRange** i **ResEffectiveDateTimeRange**. Vrijednosti polja **PSAPRojSchedRole.RootActivity** također se ažuriraju. Ako se ovo ne pokrene, primit ćete upozorenje kada pokušate izvršiti operacije planiranja resursa.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Isključivanje poboljšanja učinkovitosti planiranja resursa

1. Idite na **Upravljanje značajkama** > **Sve** i potražite mogućnost **Omogući značajku poboljšanja učinkovitosti planiranja resursa projekta**.
2. Odaberite značajku, a zatim odaberite gumb **Onemogući**.
3. Osvježite preglednik.
4. Idite na **Upravljanje projektima i računovodstvo** > **Povremeno** > **Sinkronizacija kapaciteta** > **Sinkroniziraj skupnih vrijednosti kapaciteta resursa**.
5. Na stranici **Skupna sinkronizacija kapaciteta** mogućnost **Ukloni postojeće zapise o kapacitetu** postavite na **Da** za uklanjanje prethodnih podataka. Ako želite generirati inkrementalne podatke, postavite mogućnost na **Ne**.
6. U polju **Kod razdoblja** odaberite razdoblje u kojem će se generirati podaci. Ako odaberete kod razdoblja, datumi početka i završetka ne moraju biti definirani.
7. Ako polje **Kod razdoblja** ostavite prazno, odaberite određene datume početka i završetka za generiranje podataka.
8. Odaberite **U redu**.

> [!NOTE]
> Ovim će se u tablicu **ResRollup** opći podaci distribuirati u sve tvrtke vašeg okruženja, tako da skupni posao treba izvoditi samo u jednoj pravnoj osobi. Ovaj skupni posao potreban je svim prikazima **Dostupnost resursa**. Ako se ovaj skupni posao ne pokrene, podaci **ResRollup** generirat će se u hodu, što može potrajati.


[!INCLUDE[footer-include](../includes/footer-banner.md)]