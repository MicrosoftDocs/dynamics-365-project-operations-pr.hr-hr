---
title: Konfiguracija kategorija projekta
description: U ovoj temi nalaze se informacije o postavljanju kategorija projekta.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895957"
---
# <a name="configure-project-categories"></a>Konfiguracija kategorija projekta

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Project Operations pruža snažne mogućnosti za kategorizaciju prihoda i troškova na projektima. Kategorije pružaju mogućnost izvješćivanja i analize projektnih transakcija te obavljanje knjiženja u glavnu knjigu.

Dijagram u nastavku prikazuje povezanost između kategorija transakcija, dijeljenih kategorija i kategorija projekta. 

Kategorije transakcija osnovno su grupiranje za projektne transakcije. Unutar tog grupiranja postoji skup dijeljenih kategorija koje se mogu dijeliti između aplikacija i modula. Ulazeći još dublje u pojedinosti, kategorije projekta najpodrobnija su razina kategorija. Kategorije projekta specifične su za pravnu osobu, modul i aplikaciju.

![Povezanost između kategorija transakcija, dijeljenih kategorija i kategorija projekta.](media/project-categories.png)

## <a name="transaction-categories"></a>Kategorije transakcija

Kategorije transakcija predstavljaju osnovno grupiranje za projektne transakcije i nisu specifične za tvrtku ili vrstu transakcije. Na primjer, Contoso Robotics upotrebljava kategorije Dizajn, Putovanje, Instalacija i Uslužne transakcije za grupiranje projektnih transakcija.

Kategorije transakcija definirane su u modulu Project Operations. 
1. Idite na **Postavke** \> **Kategorije transakcija** kako biste otvorili postavke. 
2. Stvorite novu kategoriju transakcija bilo odabirom mogućnosti **Nova** ili **Uvoz iz programa Excel**.

## <a name="shared-categories"></a>Dijeljene kategorije

Dynamics 365 upotrebljava koncept dijeljenih kategorija za kategorizaciju troškova u različitim aplikacijama, kao što su Dynamics 365 Finance, Dynamics 365 Supply Chain i Dynamics 365 Project Operations. Za svaku stvorenu kategoriju transakcija, Project Operations automatski stvara četiri povezane dijeljene kategorije: Sati, Trošak, Naknade i Stavka. Dijeljene kategorije možete pregledati i prilagoditi odlaskom na stavku **Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Kategorije** \> **Dijeljene kategorije**.

## <a name="project-categories"></a>Kategorije projekata

Kategorije projekata predstavljaju najpodrobniju razinu konfiguracije kategorija i računovođa projekta mora ih konfigurirati odvojeno i za svaku tvrtku.

1. Idite na **Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Kategorije** \> **Kategorije projekta**.
2. Odaberite **Novo**.
3. Odaberite **ID kategorije** dijeljene kategorije koju ste stvorili u prethodnom odjeljku. Project Operations omogućuje uporabu samo onih dijeljenih kategorija koje su povezane s kategorijama transakcija.
4. Odabir grupe kategorije.

## <a name="category-groups"></a>Grupe kategorije

Grupe kategorija upotrebljavaju se za dijeljenje svojstava, prvenstveno profila knjiženja, između povezanih kategorija projekta. Za svaku vrstu transakcije mora postojati najmanje jedna grupa kategorija, a svakoj kategoriji projekta dodjeljuje se grupa.

Specifikacije knjiženja u aplikaciji Project Operations određene su pravilima profila troškova i prihoda projekta, kategorijama projekata i grupama kategorija. Grupe kategorija možete postaviti tako da odete na postavku **Upravljanje projektima i računovodstvo** \> **Postavljanje** \> **Kategorije** \> **Grupe kategorija**.
