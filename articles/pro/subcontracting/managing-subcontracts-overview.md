---
title: Upravljanje podugovorima u aplikaciji Project Operations
description: Ovaj članak pruža pregled procesa upravljanja kooperatom od kraja do kraja koji se obično nalazi u projektnim organizacijama.
author: rumant
ms.date: 08/02/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 783ab1b642bb8cfe2fb3b977a95c8064f33a7994
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261184"
---
# <a name="subcontract-management-in-project-operations"></a>Upravljanje podugovorima u aplikaciji Project Operations


_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ovaj članak pruža pregled procesa upravljanja kooperantima od kraja do kraja u projektnim organizacijama. Podugovaranje usluga obično slijedi tijek poslovnog procesa koji se prikazuje na dijagramu u nastavku.

![Tijek postupka podugovaranja](../media/SubcontractingProcessFlow.png)

Popis u nastavku pruža podrobni opis procesa podugovaranja.

1. Voditelj projekta sklapa podugovor s dobavljačem. Prema zadanim postavkama, cjenici koji su priloženi zapisu o dobavljaču upotrebljavaju se za podugovor. Račun dobavljača ima vrstu odnosa **Dobavljač** ili **Isporučitelj**.
2. Voditelj projekta može sve kupnje specificirati kao stavke retka na podugovoru. Redci podugovora mogu se odnositi na vrijeme, troškove ili proizvode. Klasa transakcije retka podugovora određuje čemu taj redak služi.
3. Voditelj računa dobavljača i voditelj projekta mogu ponavljati podugovor. U nabavnim cjenicima priloženim podugovoru cijene se mogu prilagoditi.
4. U ovom trenutku ili kasnije u postupku, ako je redak podugovora za vrijeme, upravitelj računa dobavljača povezuje kontakte dobavljača sa svakim retkom podugovora. Ova povezanost pruža informacije voditelju projekta koji radi na podugovoru. Kad je kontakt dobavljača povezan s retkom podugovora, sustav iz kontakta automatski stvara kontakt koji se može rezervirati, ako resurs koji se može rezervirati već ne postoji.
5. Način naplate na svakom retku podugovora može biti **Fiksna cijena** ili **Vrijeme i materijal**. Za retke podugovora s fiksnom cijenom postavljen je raspored faktura koji se temelji na kontrolnim točkama.
6.  Nakon što se sklopi podugovor i završe pregovori, on se potvrđuje. Potvrđeni podugovori ne mogu se uređivati, ali ako dođe do promjena, podugovor se može „ponovno otvoriti za uređivanja”, čime se status postavlja s **Potvrđeno** natrag na **Skica** i pregovori se mogu ponovno otvoriti. 
7.  Tijekom stvaranja generičkog člana tima na projektu, član tima može se povezati s retkom podugovora. To ukazuje na potrebu za angažman generičkog člana tima s kapacitetom podizvođača.
8.  Imenovani članovi tima mogu se stvoriti ili izravno na projektu ili tako da ih rezerviraju s pomoću iskustava u planiranju resursa. Ako je imenovani član projektnog tima radnik po ugovoru, moguće ga je povezati s retkom podugovora. Time će se dostupni kapaciteti povući na redak podugovora.
9.  Resursi podizvođača mogu evidentirati vrijeme, troškove i uporabu materijala na projektima i projektnim zadacima, a zatim to poslati na odobrenje. Slično je i sa zaposlenicima. Tijekom bilježenja vremena, radnik po ugovoru može odabrati određeni podugovor i redak podugovora.
10. Nakon odobrenja, vrijeme odobreno podugovorima bilježit će stvarne troškove projekta na temelju nabavne cijene radnika po ugovoru ili uloge koju su imali na projektu.
11. Fakture dobavljača i stavke redaka fakture dobavljača mogu se zabilježiti u sustavu za posao koji obavljaju resursi dobavljača ili proizvode koje dobavljač isporučuje. Redci faktura dobavljača moraju biti specifični za projekt i za klasu transakcije za vrijeme, trošak, proizvod/materijal, kontrolnu toču ili naknadu. Druga je mogućnost da retci faktura dobavljača upućuju na redak podugovora.
12. Sustav će automatski povezati sve stvarne troškove kojima se podudaraju redak podugovora i projekt s fakturom dobavljača. To će olakšati trosmjerno podudaranje i postupak provjere.
13. Voditelj projekta tada može pregledati automatski usklađene stvarne podatke projekta, ukloniti ili dodati druge stvarne podatke o cijenama projekta i dovršiti postupak provjere.
14. Dovršenje postupka provjere na svim redcima označit će fakturu dobavljača kao **Spremno za plaćanje**. U ovoj fazi, faktura dobavljača i njeni retci mogu se prenijeti u sustav Računovodstva ili Obveza kako bi se obradilo plaćanje dobavljaču. Prethodno zabilježeni troškovi projekta stornirat će se, a stvarni troškovi iz retka fakture dobavljača zabilježit će se na projektu.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Redci podugovora koji se temelje na količini i redci podugovora koji se temelje na radu

Redak podugovora može se temeljiti na količini ili na radu. 

Kad je redak podugovora **na temelju količine**, količina kupljena na retku podugovora za vrijeme, troškove ili materijal može se upotrijebiti na svakom projektu.

Kad je redak podugovora **na temeljenu rada**, redak podugovora mapira se na ukupnost rada koji se u planu projekta prikazuje kao čvor. Vrijednost retka podugovora zbroj je svih komponenti koje su potrebne za isporuku te ukupnosti rada. One su modelirane kao pojedinosti retka podugovora i mogu biti skup vremena, troškova ili materijala. Za redak podugovora koji se temelji na radu, redak podugovora također je namijenjen jednom projektu. Te vrste podugovaratelja nisu podržane projektnim operacijama.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

