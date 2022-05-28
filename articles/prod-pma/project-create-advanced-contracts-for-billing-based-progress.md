---
title: Stvaranje predugovora za naplatu na temelju napretka
description: U ovoj se temi objašnjava način stvaranja ugovora o projektima tako da klijentima možete generirati račune na temelju postotka dovršenog posla.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: bdafc2ed2398054d8b0bf42bdd96dfe0eccee93b
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683154"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Stvaranje predugovora za naplatu na temelju napretka
[!include [banner](../includes/banner.md)]

U ovoj se temi objašnjava način stvaranja ugovora o projektima tako da klijentima možete stvoriti račune na temelju postotka dovršenog posla. Iznosi faktura automatski se izračunavaju za proračunske kategorije posla koje ste postavili za projekt. Vrijeme računa postavlja se kada pregovarate s klijentom o ugovoru o projektu.

Upotrijebite postupke navedene u ovoj temi za postavljanje ugovora, povezanog projekta i pravila naplate koja izračunavaju iznose fakture za proračunske kategorije posla koje ste postavili za projekt.

Nakon što stvorite ugovor i projekt, možete postaviti pojedinosti projekta. Na primjer, možete definirati aktivnosti i dodijeliti radnike projektu.

## <a name="example"></a>Primjer

Vaša je tvrtka ili ustanova tvrtka za razvoj softvera. Pristajete razviti paket obračuna plaća za klijenta za ukupnu naknadu od 20.000 USD. Vaša tvrtka ili ustanova pristaje fakturirati klijentu kako dovršavate određene postotke projekta. Za posao postavljate sljedeće kategorije projekta kako biste ih mogli upotrebljavati u postupku naplate:

- Savjetovanje
- Izrađujte
- Instalacija

Postavljate i pravila naplate koja automatski izračunavaju iznose faktura za postotak dovršenosti posla na projektu za svaku kategoriju.

Upravitelj proračuna stvara proračun za kategorije projekta. Količina dovršenosti posla automatski se izračunava kao postotak stvarnog posla u odnosu na proračunske iznose.

## <a name="prerequisites"></a>Preduvjeti

Prije stvaranja projekta koji upotrebljava pravila naplate, morate postaviti brojčane nizove za pravila naplate i dnevnik naknada koji se upotrebljava za knjiženje naplate napretka.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Parametri upravljanja projektom i računovodstva**.
2. Na stranici **Parametri upravljanja projektom i računovodstva**, na kartici **Brojčani nizovi**, postavite brojčani niz koji želite upotrebljavati tijekom izrade pravila naplate.
3. Idite na **Upravljanje projektima i računovodstvo** \> **Dnevnici** \> **Naknada**.
4. Na stranici **Dnevnik naknada** odaberite **Novi** i unesite naziv dnevnika.

## <a name="create-a-contract-for-progress-billings"></a>Stvaranje ugovora za naplatu napretka

Ovaj postupak upotrebljavajte za izradu ugovora o projektu za projekt s fiksnom cijenom. Fakturu za projekt stvarate kada posao koji je dovršen na projektu dosegne određeni postotak.

1. Idite na **Upravljanje projektom i računovodstvo** \> **Projekti** \> **Ugovori o projektu**.
2. Na stranici **Ugovori o projektu** odaberite **Novi**.
3. U dijaloškom okviru **Novi ugovor o projektu** postavite sljedeća polja:

    - **Ime**
    - **Vrsta financiranja**
    - **Izvor financiranja**
    - **Valuta prodaje** – Prema zadanim postavkama, ova se valuta upotrebljava za fakture klijenta koji su povezani s ugovorom o projektu. Međutim, valutu prodaje možete promijeniti na određenoj fakturi za klijenta.

4. Odaberite **U redu**. Podaci se kopiraju u zaglavlje stranice **Ugovori o projektu**.
5. Na stranici **Ugovori o projektu** ispunite ostatak potrebnih podataka za projekt.

## <a name="create-a-project-for-progress-billings"></a>Stvaranje projekta za naplatu napretka

Slijedite ove korake za stvaranje projekta i svih potprojekata koji su povezani s ugovorom o projektu.

1. Idite na mogućnost **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti**.
2. Na stranici **Svi projekti** odaberite **Novi**.
3. U dijaloškom okviru **Novi projekt**, u polju **Vrsta projekta**, odaberite **Vrijeme i materijal**.
4. Odaberite projektnu grupu. Projektna grupa definira podatke o knjiženju za projekte koji su dodijeljeni grupi.
5. Odaberite **Stvori projekt**.
6. Nakon stvaranja projekta, postavite fazu projekta na **U postupku**.

## <a name="create-a-budget-for-a-project"></a>Stvaranje proračuna projekta

Proračunske kategorije upotrebljavaju se za automatski izračun iznosa računa za postotak dovršenosti posla za svaku kategoriju. Slijedite ove korake kako biste stvorili proračunske kategorije za procijenjene troškove.

1. Idite na mogućnost **Upravljanje projektima i računovodstvo** \> **Projekti** \> **Svi projekti**.
2. Na stranici **Svi projekti** odaberite i otvorite projekt koji želite.
3. Na stranici **Projekti**, u oknu Radnje, na kartici **Planiranje**, u grupi **Proračun**, odaberite **Proračun projekta**.
4. Na stranici **Proračun projekta** unesite procijenjeni trošak za svaku kategoriju projekta.

## <a name="create-billing-rules-for-progress-billings"></a>Stvorite pravila naplate za napredovanje naplate

1. Idite na **Upravljanje projektom i računovodstvo** \> **Projekti** \> **Ugovori o projektu**.
2. Na stranici **Ugovori o projektima** odaberite i otvorite ugovor o projektu.
3. Na stranici ugovora o projektu, na Brzoj kartici **Pravila naplate**, odaberite **Dodaj**.
4. Na stranici **Pravilo naplate**, u polju **Vrsta retka**, odaberite **Napredak**.
5. Na Brzoj kartici **Pojedinosti retka pravila naplate**, u polju **Vrijednost ugovora**, unesite ukupnu vrijednost ugovora.
6. U polju **Kategorija** odaberite kategoriju u koju ćete knjižiti transakciju naknade.
7. U polju **Projekt** odaberite projekt koji upotrebljava ovo pravilo naplate.
8. Izborno: Dodijelite pravilo naplate dodatnim projektima. Na Brzoj kartici **Projekt**, u odjeljku **Dostupni projekti**, odaberite projekt, a zatim odaberite gumb sa strelicom udesno kako biste projekt dodali odjeljku **Odabrani projekti**.
9. Neobvezno: Izračunajte postotni iznos koji kupac usteže kada plaća fakturu. Na Brzoj kartici **Uvjeti ustezanja plaćanja** odaberite izvor financiranja, a zatim u polju **Postotak ustezanja** unesite postotak ustezanja.
10. Ponovite ove korake za stvaranje dodatnih pravila naplate za ugovor o projektu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]