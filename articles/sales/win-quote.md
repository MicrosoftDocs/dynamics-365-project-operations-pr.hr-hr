---
title: Zatvaranje ponude
description: U ovom se članku nalaze informacije o zatvaranju ponuda u projektnim operacijama.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 45bdfe5fb9eddb8f96ed1bc017596c8fe436245e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931873"
---
# <a name="close-a-quote"></a>Zatvaranje ponude

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ponuda projekta mogu se zatvoriti kao ostvarene ili neostvarene. Budući da funkcije Aktivacija i Revizija nisu podržane u ponudi u aplikaciji Microsoft Dynamics 365 Project Operations, skicu ponude možete zatvoriti.

## <a name="close-a-quote-as-won"></a>Zatvaranje ponude kao ostvarene

Zatvaranje ponude za projekt kao Ostvarene postavit će status ponude na **Zatvorena** i razlog statusa na **Ostvaren**. Zatvaranje ponuda čini ponudu projekta ponudom samo za čitanje i stvara nacrt ugovora o projektu koji sadrži sve podatke o ponudi. Budući da se zatvorena ponuda ne može ponovno otvoriti, prije nego što zatvorite ponudu, dijaloški okvir potvrdit će vaše promjene.

Ugovor o projektu stvoren iz ponude projekta također je dostupan u modulu Upravljanje projektima i računovodstvo aplikacije Project Operations. Ako ugovor o projektu nije mapiran ni na jednom od redaka projekta, ovaj ugovor o projektu postaje dostupan kao neaktivni ugovor o projektu i postaje aktivan čim se projekt mapira na barem jedan od njegovih redaka ugovora.

Ako je ponuda priložena uz priliku, svaka druga ponuda projekta za priliku automatski se zatvaraju kao Izgubljena.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Financijski utjecaj zatvaranja ponude kao ostvarene

Ako postoje stvarni podaci o vremenu zabilježenom na projektu, dok je on još uvijek priložen nacrtu ponude, bilježe se samo troškovi vremena ili izdataka. Nakon što se ponuda zatvori kao ostvarena, aplikacija će refaktorirati troškove poništavanjem starijih stvarnih podataka o trošku i ponovnim stvaranjem novih stvarnih podataka o trošku. Aplikacija će obraditi ove stvarne podatke o trošku na temelju metode naplate retka ugovora povezanog projekta. Ako se stvarni podaci o trošku odnose na redak ugovora o vremenu i materijalu, sustav će automatski stvoriti odgovarajuće nenaplaćene stvarne prodajne podatke za vrijeme zatvaranja ponude i izrade ugovora o projektu. Ako se stvarni podaci o trošku odnose na redak ugovora s fiksnom cijenom, aplikacija će zaustaviti ponovnu obradu stvarnih podataka o trošku na temelju pravila podijeljene naplate za klijente ugovora o projektu.

Svi ponovno obrađeni stvarni podaci dostupni su u modulu Upravljanje projektom i računovodstvo kako bi ih knjigovođa mogao pregledati, ažurirati i proknjižiti u glavnoj knjizi. 

## <a name="close-a-quote-as-lost"></a>Zatvaranje ponude kao neostvarene

Zatvaranjem ponude projekta kao Neostvarene postavit će status na **Zatvorena**, a razlog statusa na **Neostvarena**. Zatvaranje ponude čini je ponudom samo za čitanje. Budući da se zatvorena ponuda ne može ponovno otvoriti, prije nego što zatvorite ponudu, dijaloški okvir potvrdit će vaše promjene.

Ako ponuda projekta koja je zatvorena kao Izgubljena ima projekt naveden na nekom od svojih redaka, taj projekt se također označava kao Zatvoren i sve rezervacije resursa od toga dana nadalje otkazuju se.

> [!NOTE]
> U aplikaciji Project Operations zatvaranje ponude kao Ostvarene ili Neostvarene neće utjecati na status Prilike, koji će ostati otvoren sve dok se ručno ne zatvori.


[!INCLUDE[footer-include](../includes/footer-banner.md)]