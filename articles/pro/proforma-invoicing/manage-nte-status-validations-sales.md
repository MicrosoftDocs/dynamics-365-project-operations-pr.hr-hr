---
title: Upravljanje statusom koji se ne smije premašiti i provjerama valjanosti
description: U ovoj temi nalaze se informacije o provjeri ograničenja koja se ne smiju prekoračiti u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5c491d4014ffc2568d7df72b542761ec9b1a90b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274002"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Upravljanje statusom koji se ne smije premašiti i provjerama valjanosti 

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

## <a name="not-to-exceed-on-approvals"></a>Odobrenja koje se ne smiju prekoračiti

Kada se šalje unos vremena ili troškova, stvara se zapis o odobrenju. Ako je odobrenje naplativo i mapira se na redak ugovora za vrijeme i materijal, sustav izvršava provjeru valjanosti koja ne smije prekoračiti na sljedećim razinama:

  - Provjera prema ograničenju postavljenom za klijenta na retku ugovora o projektu
  - Provjera prema ograničenju postavljenom na retku ugovora
  - Provjera prema ograničenju postavljenom za klijenta
  - Provjera prema ograničenju postavljenom na ugovoru

Provjere na svakoj razini uključuju osiguravanje da iznos prodajne vrijednosti na tom odobrenju neće prekršiti ograničenje koje se ne smije prekoračiti na toj razini nakon obračunavanja već evidentiranog iznosa zaostalih naplata i do danas fakturiranog iznosa na toj razini.

Ako provjera uspije, odobrenje dobiva status potvrde **Uspjelo**.

Ako provjera ne uspije, odobrenje dobiva status potvrde **Nije uspjelo**. Pojedinost valjanosti koji se ne smije prekoračiti izvijestit će korisnika na kojoj razini provjera valjanosti nije uspjela.

Kada se prijavljeni unos vremena ili troškova smatra nenaplativim, status provjere koji ne smije prekoračiti postavlja se na **Nije primjenjivo** s pojedinosti provjere izjednačenim sa **Nije primjenjivo**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Stvarna nenaplaćena prodaja koja se ne smije prekoračiti

Kada se odobri unos vremena ili troška, stvaraju se stvarni zapisi o troškovima i nenaplaćenim prodajama. Ako je stvorena stvarno nenaplaćena prodaja naplativa i mapira se na redak ugovora za vrijeme i materijal, aplikacija izvršava provjeru valjanosti koja ne smije prekoračiti na sljedećim razinama:

  - Provjera prema ograničenju postavljenom za klijenta retka ugovora o projektu
  - Provjera prema ograničenju postavljenom na retku ugovora
  - Provjera prema ograničenju postavljenom za klijenta
  - Provjera prema ograničenju postavljenom na ugovoru

Provjere na svakoj razini osiguravaju da iznos prodajne vrijednosti na stvarnom podatku neće prekršiti ograničenje koje se ne smije prekoračiti na toj razini nakon obračunavanja već evidentiranog iznosa zaostalih naplata i do danas fakturiranog iznosa na toj razini.

Ako provjera uspije, stvarno nenaplaćena prodaja dobiva status koji se ne smije prekoračiti **Angažirano**.

Ako provjera ne uspije, stvarno nenaplaćena prodaja dobiva status koji se ne smije prekoračiti **Neuspjelo**. Pojedinost valjanosti izvješćuje korisnika na kojoj razini provjera valjanosti nije uspjela.

Kada se stvarna prodaja bez fakture smatra nenaplativom ili besplatnom, ako ni na jednoj od četiri razine nije postavljeno ograničenje koje se ne smije prekoračiti ili ako je stvoreni stvarni podatak trošak, akontacija, jedinica za resurse ili međuorganizacijska prodaja, polja **Status koji se ne smije prekoračiti** i **Pojedinost provjere valjanosti koja se ne smije prekoračiti** polja moraju biti postavljena na **Nije primjenjivo**.

## <a name="reset-the-not-to-exceed-status"></a>Vraćanje statusa koji se ne smije prekoračiti

Možete izvršiti skupno vraćanje statusa koji se ne smije prekoračiti. To projektnim menadžerima omogućuje prilagodbu provjere koja se ne smije prekoračiti kako bi dali prednost fakturiranju jednom određenom dijelu posla, vremena ili troškova pred drugima koji su već angažirani iz dostupnog iznosa koji se ne smije prekoračiti.

Nakon vraćanja statusa koji se ne smije prekoračiti na stvarne nenaplaćene prodaje, angažirani se iznos smanjuje. Voditelj projekta može odabrati neki drugi dio posla, vremena ili troškova za koje prethodno nije uspjela provjera valjanosti koja se ne smije prekoračiti i ponovno im provjeriti valjanost. Uz smanjenje angažiranog iznosa, provjera ovih stvarnih podataka sada će biti uspješna. To pomaže voditelju projekta da izvrši veći utjecaj i kontrolu nad fakturiranim transakcijama za to razdoblje.

Kako biste vratili status koji se ne smije prekoračiti, odaberite jedan ili više stvarnih podataka iz prikaza **Zaostala naplata vremena i materijala** ili **Stvarni podaci**, a zatim odaberite **Vrati status koji se ne smije prekoračiti**.

Status koji se ne smije prekoračiti vraćen je na **Nije procijenjeno** na svim relevantnim odabranim stvarnim podacima. Stvarni podaci čiji se status ne smije prekoračiti su stvarne nenaplaćene prodaje koje još nisu fakturirane, nisu na skici fakture i označene su kao naplative. Svi drugi odabrani stvarni podaci ignoriraju se.

## <a name="reevaluate-not-to-exceed-status"></a>Ponovna procjena vrijednosti statusa koja se ne smije prekoračiti

Možete izvršiti skupnu ponovnu procjenu vrijednosti statusa koji se ne smije prekoračiti. Ponovna procjena vrijednosti statusa koji se ne smije prekoračiti korisna je u sljedećim situacijama:

  - Kada se s klijentom ponovnih pregovara o ograničenjima koja se ne smiju prekoračiti i potrebno je ponovno procijeniti stvarne podatke.
  - Kada voditelj projekta želi precizno prilagoditi fakturiranje zaostalih neplaćenih prodaja davanjem prednosti jednom dijelu posla u odnosu na drugi.

Kako biste ponovno procijenili vrijednost statusa koji se ne smije prekoračiti, odaberite jedan ili više stvarnih podataka iz prikaza **Zaostala naplata vremena i materijala** ili **Stvarni podaci** i odaberite **Ponovno procijeni vrijednost statusa koji se ne smije prekoračiti**.

Svim će se relevantnim odabranim stvarnim podacima s ograničenjem koje se ne smije prekoračiti ponovno procijeniti vrijednost u odnosu na postavke ograničenja koje se ne smiju prekoračiti. Stvarni podaci koji su relevantni za ponovnu procjenu vrijednosti statusa koji se ne smije prekoračiti su stvarne nenaplaćene prodaje koje još nisu fakturirane, nisu na skici fakture i označene su kao naplative. Odabiru se svi drugi odabrani stvarni podaci.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]