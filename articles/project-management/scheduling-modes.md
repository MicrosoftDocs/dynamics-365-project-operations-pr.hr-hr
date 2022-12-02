---
title: Načini planiranja
description: U ovom se članku nalaze informacije o načinima planiranja.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3cbe14f8d458c5d9631e0595912afa8cbb87b9de
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923639"
---
# <a name="scheduling-modes"></a>Načini planiranja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_


Dynamics 365 Project Operations pruža tvrtkama i ustanovama mogućnost definiranja načina upravljanja promjenama ključnih varijabli u zadacima unutar strukture analize rada. Na temelju specifičnih potreba tvrtke ili ustanove, voditelji projekata mogu nakon stvaranja projekta napraviti promjene načina planiranja.

U aplikaciji Project Operations dostupna su tri načina planiranja:

  - Nepromjenjivo trajanje (ovo je zadani način)
  - Fiksni napor (*Rad*)
  - Fiksne jedinice

Vrijednosti na koje utječe definicija određenog načina planiranja određuju se prema sljedećoj formuli:

  Napor = Trajanje x Jedinice

Kada definirate način planiranja projekta, postavljate jednu od ovih vrijednosti koje se potom ne mogu mijenjati. Držanje ove vrijednosti kao konstante stavlja prioritet na tu vrijednost, što izvješćuje sustav da je ne mijenja kada se promijene druge dvije vrijednosti. Sljedeća tablica pruža informacije o utjecajima odabira određenog načina.

| **U ovom zadatku**             | **Ako promijenite jedinice**   | **Ako promijenite trajanje** | **Ako promijenite napor**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Nepromjenjive jedinice zadatka     | Trajanje se preračunava. | Napor se preračunava.    | Trajanje se preračunava. |
| Zadatak nepromjenjivog napora    | Trajanje se preračunava. | Jedinice se preračunavaju.    | Trajanje se preračunava. |
| Zadatak nepromjenjivog trajanja  | Napor se preračunava.   | Napor se preračunava.    | Jedinice se preračunavaju.   |

Dodatne informacije o implikacijama određenog načina potražite u članku [Promjena vrste zadatka za preciznije planiranje](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). U članku se pojam **Rad** upotrebljava umjesto pojma **Napor**.

## <a name="change-the-organizations-scheduling-mode"></a>Promjena načina planiranja u tvrtki ili ustanovi

Poduzmite sljedeće korake kako biste definirali način planiranja u tvrtki ili ustanovi.

1. Idite na **Postavke** \> **Općenito** \> **Parametri**, a zatim odaberite parametar projekta. 
2. Na stranici **Parametri projekta** odaberite zadani način planiranja za tvrtku ili ustanovu, a zatim definirajte mogućnost da upravitelj projekta nadjača postavku tijekom stvaranja novog projekta.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Promjena postavke načina planiranja u projektu

Ako tvrtka ili ustanova dozvoljava voditelju projekta da nadjača zadani način planiranja, voditelj projekta može izvršiti tu promjenu tijekom stvaranja novog projekta. Međutim, nakon što se projekt spremi, način planiranja ne može se promijeniti.

## <a name="copied-projects"></a>Kopirani projekti

Budući da se projekt stvara kad se poduzme radnja kopiranja, voditelj projekta ne može postaviti način planiranja. Odredišni projekt uvijek će biti zadan za način definiran na razini tvrtke ili ustanove.

## <a name="copied-tasks"></a>Kopirani zadaci

Kada se zadatak kopira iz jednog projekta u drugi, zadatak nasljeđuje način planiranja odredišnog projekta.
