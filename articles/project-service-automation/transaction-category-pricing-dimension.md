---
title: Upotreba kategorije transakcija kao dimenzije cijena
description: Ovaj tema pruža informacije o upotrebi kategorije transakcije kao dimenzije cijena.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 64b81ca7-e2db-4e4a-a202-aae0eb235ffd
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: a36e0578b8d77a0ed1ea61134453aa064771760f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750195"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Upotreba kategorije transakcija kao dimenzije cijena
U ovoj je temi objašnjena upotreba kategorije transakcije kao dimenzije cijena. Prije nego što započnete, ako još niste izradili rješenje dimenzije cijena, morat ćete stvoriti novu. Ako već imate rješenje dimenzije cijena, možete uvesti promjene u tom rješenju. Ako niste izradili novo rješenje dimenzije cijena za svoju organizaciju, provedite postupke u temi [Stvaranje prilagođenih polja i entiteta](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Dodavanje kategorije transakcije u obrasce i prikaze
Da bi kategorija transakcije bila vidljiva u korisničkom sučelju u rješenju dimenzije cijena, morat ćete proći kroz sve obrasce i prikaze ključnih entiteta i dodati ta polja obrascima i prikazima tih entiteta.
Sljedeća tablica sveobuhvatan je popis unaprijed pripremljenih obrazaca i prikaza koji su navedeni po entitetu, a moraju se ažurirati s novim poljima. Ako u prilagođavanju tih entiteta postoje dodatni prikazi ili obrasci, dodajte nova polja i njima.

|  Entitet        | Obrasci     |Prikazi        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cijena uloge|• Informacije |• Cijene kategorije aktivnog resursa<br> • Pridruženi prikaz cijene kategorije resursa|
|  Provizija cijene uloge|• Informacije|• Aktivna provizija cijene uloge<br>• Pridruženi prikaz provizije cijene uloge|
|  Pojedinost retka ponude|• Informacije o projektu<br>• Brzo stvaranje projekta|• Pojedinost retka aktivne ponude<br>• Kombinirane pojedinosti retka ponude<br>• Pridruženi prikaz pojedinosti retka ponude|
|  Pojedinost retka ugovora projekta|• Informacije o projektu<br>• Brzo stvaranje projekta|• Kombinirane pojedinosti retka ugovora<br>• Pojedinosti aktivnog retka ugovora<br>• Pridruženi prikaz pojedinosti retka ugovora|
|  Član projektnog tima|• Informacije<br>• Novi obrazac|• Aktivni članovi projektnog tima<br>• Članovi projektnog tima<br>• Pridruženi prikaz članova projektnog tima|
|  Unos vremena|• Informacije<br>• Stvaranje unosa vremena|• Moji Unos vremenai po datumu<br>• Moji Unos vremenai za ovaj tjedan<br>• Unos vremenai za odobrenje|
|  Redak u dnevniku|• Informacije<br>• Brzo stvaranje|• Reci u aktivnom dnevniku<br>• Pridruženi prikaz retka u dnevniku|
|  Pojedinost retka fakture|• Informacije<br>• Brzo stvaranje|• Pojedinosti retka aktivne fakture<br>• Naplative transakcije fakture<br>• Besplatne transakcije fakture<br>• Pridruženi prikaz pojedinosti retka fakture<br>• Nenaplative transakcije fakture|
|  Stvarni posao|• Informacije<br>• Aktivni stvarni podaci|• Pridruženi prikaz stvarnih podataka|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Postavljanje kategorije transakcija kao dimenzije cijena

1. Na web-sučelju otvorite **Project Service** > **Postavke** > **Parametri**. 
2. Na stranici **Parametri**, na kartici **Dimenzije cijena utemeljene na iznosu**, primijetite da rešetka na kartici prikazuje zapise u entitetu **Dimenzije cijena**.
3. Dodajte **Kategorija transakcije** na ovaj popis i postavite polja **Primjenjivo na trošak** i **Primjenjivo na prodaju** na **Da**.
4. U polju **Vrsta dimenzije** odaberite **Utemeljeno na iznosu**, a zatim odaberite prioritet za **kategoriju transakcije** koja je povezana s troškom i prodajom.
