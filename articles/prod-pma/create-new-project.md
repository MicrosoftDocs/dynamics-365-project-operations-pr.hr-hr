---
title: Stvaranje novog projekta
description: U ovom se članku navode informacije o načinu izrade novog projekta.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cbe7ea7d6ee57b3494494a2758dbcb7ded735dc1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919683"
---
# <a name="create-a-new-project"></a>Stvaranje novog projekta

[!include [banner](../includes/banner.md)]

Poduzmite sljedeće korake za stvaranje novog projekta.

1. Na stranici **Upravljanje projektom** odaberite **Novi projekt** i unesite sljedeće vrijednosti:

    - **Vrsta projekta:** Vrijeme i materijal
    - **Naziv projekta:** XYZ nadogradnja 2. faze
    - **Grupa projekata:** TM\_WIP
    - **ID ugovora projekta:** 00000002

2. Odaberite **Stvori projekt**.

## <a name="assign-a-resource-to-a-project"></a>Dodjela resursa projektu

1. Na stranici **Radnici**, na popisu **Radnici**, odaberite zapis za radnika za kojeg ste prethodno postavili kompetencije i otvorite zapis za radnika.
2. U Oknu radnji na kartici **Projekt** u grupi **Postavljanje**, kliknite mogućnost **Dodjeli projekte**.
3. Na stranici **Projektni zadaci za provjeru valjanosti resursa**, na kartici **Projekti** u polju **Dodajte projekt odabranim projektima**, filtrirajte na projekt **XYZ nadogradnja 2. faze**.
4. U oknu **Preostali projekti** odaberite projekt, a zatim odaberite gumb sa strelicom kako biste ga dodali u okno **Odabrani projekti**.

Prema potrebi možete dodijeliti i kategorije za resurs. Ta je vrsta kategorije ili **Trošak** ili **Prihod**. Vrstu kategorije određuje vaša tvrtka ili ustanova. Ako za resurs nisu dodijeljene kategorije, Financije pretražuju zadanu kategoriju cijena radnih sati za trošak i prihod.

## <a name="set-up-project-resource-and-role-characteristics"></a>Postavljanje svojstava resursa i uloga za projekt

Voditelj projekta može upotrijebiti funkcionalnost projektnih resursa za stvaranje uloga potrebnih za projekt. Uloge se mogu upotrebljavati ako su potvrđeni resursi i dalje nepoznati u vrijeme rezerviranja resursa. Uloge se mogu privremeno rezervirati kao planirani resursi, tako da možete nastaviti faze planiranja projekta.

[![Primjer uloge.](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenarij:** Contoso je angažiran da dovrši projekt Vrijeme i materijal koji ima odobren ugovor o projektu. Voditelj projekta nižeg ranga još uvijek dovršava djelokrug projekta. Voditelj resursa trenutačno identificira određene resurse koji će se rezervirati za rad na novom projektu. Zbog kritične naravi projekta, sponzor projekta zatražio je ulogu voditelja projekta višeg ranga kao jednu od uloga. Voditelj resursa mora nabaviti novi resurs i definirati ulogu u sustavu u slučaju da voditelj projekta nižeg ranga tijekom planiranja projekta zatraži podatke o resursima.

U sljedećim koracima pokazan je način na koji upravitelj resursa može postaviti ulogu voditelja projekta višeg ranga i s njom povezati svojstva resursa. Kasnije se uloga može upotrijebiti za traženje dostupnih resursa koji se podudaraju s potrebnim kompetencijama resursa.

1. Na stranici **Postavljanje uloga** odaberite **Novo** i unesite sljedeće vrijednosti:

    - **ID uloge:** Voditelj projekta višeg ranga
    - **ID uloge:** Voditelj projekta višeg ranga

2. Kliknite **Stvori**.
3. Odaberite ulogu **Voditelj projekta višeg ranga**, a zatim odaberite **Konfiguriraj svojstva**.
4. U polju **Vrste svojstava** odaberite **Vještina**.
5. U polju **Dostupna svojstva** unesite vještinu koja se traži.
6. U polju **Vrsta svojstva** odaberite **Certifikat**.
7. U polju **Dostupna svojstva** unesite vrstu certifikata koja se traži.

## <a name="assign-a-project-resource-to-a-project"></a>Dodjela projektu odgovarajućih resursa

1. Na stranici **Svi projekti** odaberite projekt **XYZ nadogradnja 2. faze**.
2. Na kartici **Projektni tim i planiranje** odaberite **Dodaj**.
3. U polju **Uloga** odaberite **Član tima**.
4. Odaberite **Rezerviraj iz kalendara**.
5. Na stranici **Dostupnost resursa** odaberite **Prikaz postavki**.
6. Na stranici **Prilagodi postavke prikaza** unesite sljedeće vrijednosti:

    - **Oblik prikaza raspona datuma:** Dan
    - **Prikaži dostupne opise:** Da
    - **Prikaži preostali kapacitet:** Da

7. S popisa resursa odaberite resurs.
8. Odaberite **Fiksna rezervacija** i **Puni kapacitet**.

## <a name="assign-a-resource-to-a-default-role"></a>Dodjela resursa zadanoj ulozi

Kako bi se pomoglo upraviteljima projekata ili resursa, mogu vršiti pretraživanje kroz razine naniže na resursima koji se mogu rezervirati za projekt. Zadanu ulogu možete povezati s postojećim ili novostečenim resursom. Primjerice, kad je Daniel zaposlen, imao je iskustva i vještine da ispuni ulogu poslovnog analitičara. Voditelj resursa dodijelio je ovu ulogu Danielu kao zadanu ulogu. Stoga je voditelj resursa dodao Daniela u skup poslovnih analitičara koji su dostupni za rad na projektima.

Tijekom rezervacije resursa, voditelji projekata mogu filtrirati uloge resursa koje su dostupne za rad na projektima. Te podatke mogu upotrebljavati kao jedan kriterij kada provode višekriterijsku analizu odluka tijekom realizacije resursa. U filtar mogu dodati i druga svojstva resursa za traženje resursa koji imaju određene vještine, obrazovanje i iskustvo za dani projekt.

**Scenarij:** Odobreni je projekt započeo, a uloga voditelja projekta višeg ranga rezervirana je tijekom faze planiranja projekta kao planirani resurs. Upravitelj resursa sada je nabavio resurs za ispunjavanje uloge voditelja projekta višeg ranga.

1. Na stranici **Popis resursa** odaberite **Daniel Petek**.
2. Na stranici **Uloga za resurs** odaberite **Novo** i unesite sljedeće vrijednosti:

    - **Na snazi:** Unesite trenutačni datum.
    - **Istek:** Unesite **Nikada**.
    - **Uloga:** Unesite **Voditelj projekta višeg ranga**.

3. Odaberite **Spremi** i zatvorite stranicu.
4. Na kartici **Kompetencije** dodajte vještinu **ProjectMgmt** i certifikat **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]