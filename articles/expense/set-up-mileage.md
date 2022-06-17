---
title: Postavljanje kilometraže s pomoću tarifnih razreda kilometraže
description: Ovaj članak pruža informacije o stopama kilometraže i razinama stope kilometraže.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 03ca18c8fef6228f2ba553ebe50447beda5a857c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930125"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Postavljanje kilometraže s pomoću tarifnih razreda kilometraže

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Kada se prijavi trošak, a odabrana kategorija troškova je **Kilometraža**, iznos za tu vrstu troškova izračunava se prema iznosu *cijena po kilometru*. Taj se iznos određuje uporabom definiranih razina kilometraže ili, ako nisu postavljene cjenovne razine kilometraže, slijedeći standardnu cijenu kilometraže. 

Cjenovne razine kilometraže mogu se postaviti tako da odete na **Upravljanje troškovima** > **Postavi** > **Općenito** > **Kategorije troškova** > **Kilometraža** > **Postavljanje kategorije**.

Ako vaša tvrtka ili ustanova upotrebljava kategoriju troškova kilometraže, nakon nadogradnje na verziju 10.0.18 razmislite o omogućivanju značajke kilometraže nakon pregleda promjena dizajna u nastavku. 

Novi dizajn cjenovne razine kilometraže utječe na način obrade vrijednosti u polju **Količina**. Prije izdanja 10.0.18, vrijednost u polju **Količina** smatrala se donjom granicom. Kad je akumulacija prešla tu vrijednost, upotrebljavala se odgovarajuća cijena.  Od verzije 10.0.18., vrijednost u polju **Količina** smatra se gornjom granicom. Odgovarajuća se cijena upotrebljava kada je akumulirana kilometraža manja od vrijednosti u polju **Količina**.  Novi model za razine kilometraže uspostavlja dosljednost na razinama kilometraže i bolju upotrebljivost.   

Sva odobrena izvješća o troškovima ponovno će se izračunati tijekom knjiženja prema novom dizajnu.

## <a name="example"></a>Primjer
 
### <a name="before-version-10018"></a>Prije verzije 10.0.18
Uz dvije sjenovne razine kilometraže, polje **Količina** na svakoj razini predstavlja donju granicu kilometraže. Trenutačno, prva razina ima vrijednost nula (0) i cijenu od 0,45, a druga razina ima vrijednost 1000 i cijenu od 0,25. Ako akumulirane milje ili kilometri prijeđu vrijednost u polju, upotrebljava se povezana cijena. Ako ne postoji vrsta s nultom količinom, sustav upotrebljava cijenu kilometraže koja je definirana u upravljanju troškovima. 
 
Ako zaposlenik pošalje izvješće o trošku sa 1.500 milja, dvije vrste kilometraže u izvješću o proknjiženom troškovima bile bi: 1000 (cijena 0,45) + 500 (cijena 0,25) = 575,00.

### <a name="after-version-10018"></a>Nakon verzije 10.0.18
U verziji 10.0.18, polje **Količina** na svakoj razini predstavlja gornju granicu razine. Trenutačno, prva razina ima vrijednost 999 i cijenu od 0,45, a druga razina ima vrijednost 999.999.999,00 i cijenu od 0,25. Ako akumulirane milje ili kilometri prijeđu vrijednost u polju **Količina**, upotrebljava se povezana cijena. Ako se prekorače sve gornje granice, sustav upotrebljava cijenu kilometraže koja je definirana u upravljanju troškovima. 
 
Kako bi se ispravno izračunao isti scenarij, postavljena razina mora se promijeniti. Polje **Količina** ima vrijednost 999,00 na prvoj razini, a vrijednost 999.999.999,00 na drugoj. Ako zaposlenik premaši ukupnu količinu milja ili kilometara na prvoj razini, sustav upotrebljava cijenu kilometraže koja je definirana u upravljanju troškovima. 
  
Ako zaposlenik pošalje izvješće o trošku sa 1.500 milja, dvije vrste kilometraže u izvješću o proknjiženom troškovima bile bi: 1000 (cijena 0,45) + 500 (cijena 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Omogućivanje značajke izračuna iznosa kilometraže za više razina kilometraže s istom cijenom

Značajka **Izračuna iznosa kilometraže za više razina kilometraže s istom cijenom** poboljšava izračun cijene kilometraže. Poduzmite sljedeće korake kako biste omogućili ovu značajku.

1. Idite na **Radni prostori** > **Upravljanje značajkama**. 
2. Na popisu pronađite i odaberite **Izračun količine kilometraže za više razina kilometraže s istom cijenom**, a zatim odaberite **Omogući odmah**.

Nakon što omogućite značajku, vratite razine kilometraže na zadane kako bi ispravno odražavale vrijednost polja **Količina**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
