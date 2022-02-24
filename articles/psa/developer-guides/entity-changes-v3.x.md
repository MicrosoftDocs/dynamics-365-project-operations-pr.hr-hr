---
title: Promjene entiteta, kontrole i korisničkog sučelja (Project Service Automation 3.x)
description: Ova tema opisuje promjene rješenja za Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 48062eda1f524dd3ca0d5feccf11fd5577521275
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148724"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Promjene entiteta, kontrole i korisničkog sučelja (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Puštanjem aplikacije Microsoft Dynamics Project Service Automation (psa) 3.x, mnoge promjene su izvršene na entitetima, kontrolama, prikazima i korisničkom sučelju. Ova tema pruža informacije o ovim važnim promjenama:

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Nadređeno-podređeni odnosi za entitete dokumenta prodaje, retka dokumenta prodaje, pojedinosti retka dokumenta prodaje
U verzijama aplikacije Dynamics 365 Project Service Automation (PSA) izdanim prije verzije 3,0, neki od odnosa između entiteta dokumenata prodaje, redaka dokumenta prodaje i pojedinosti retka dokumenta prodaje implementirani su kroz polja nizova koja će sadržavati prikaz niza GUID-a povezanog entiteta. To je bilo zbog ograničenja platforme koja je zahtijevala značajan prilagođeni kôd rješenja poslužitelja i klijenta kako bi ti odnosi radili slično kao tipični Dynamics CRM odnosi entiteta i da bi polja nizova služila kao polja vrijednosti.

Aplikacija PSA 3,0 ažurirana je da potpomogne novim odnosima entiteta između entiteta dokumenta prodaje i entiteta retka dokumenta prodaje.

Budući da se polja vrijednosti sada mogu koristiti za povezivanje referenci s entitetima, polja koja su sadržavala vrijednost niza GUID-a povezanog entiteta u prethodnim verzijama više nisu potrebna i stoga su zastarjela. Prilagođeni kôd rješenja poslužitelja i klijenta koji obrađuje odnose koji su definirani naslijeđenim poljima nizova također je zastario.

### <a name="entity-schema-changes"></a>Promjene sheme entiteta
Sljedeća tablica sadrži popis jedan-na-jedan zastarjelih polja nizova i novih polja vrijednosti za entitete. 

 Entitet |   Zastarjelo polje (niz) | Novo polje (vrijednost)
--- | --- | ---
invoicedetail (redak fakture) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (stvarna vrijednost) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (redak ugovora projekta raspored faktura) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (redak ugovora projekta ključna točka) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (činjenica) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (pojedinost retka fakture) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (redak u dnevniku) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (redak ugovora projekta kategorija resursa) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (pojedinost retka ugovora projekta) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (redak ugovora projekta kategorija transakcije) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (redak ugovora projekta klasifikacija transakcije) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (redak ponude raspored faktura) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (redak ponude kategorija resursa) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (redak ponude ključna točka) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (pojedinost retka ponude) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (redak ponude kategorija transakcije) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (redak ponude klasifikacija transakcije) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (redak narudžbe) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Zastarjeli prilagođeni prikazi i kontrole
Sljedeći prilagođeni prikazi i kontrole te njihovi povezani artefakti su zastarjeli.

- Prikaz naplativosti.
- Prilagođene kontrole rešetke za prikaz pojedinosti retka ponude na stranici **Informacije o projektu** za redak ponude.
- Prilagođene kontrole rešetke za prikaz pojedinosti retka ugovora projekta na stranici **Informacije o projektu** za redak prodajnog naloga.

> [!NOTE]
> Cijeli popis zastarjelih resursa potražite u odjeljku [Zastarjeli web-resursi u aplikaciji Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).

## <a name="unified-client-interface-app-module"></a>Modul aplikacije Unified Client Interface
S uvođenjem modula aplikacije Unified Client Interface (UCI), unosi karte web-mjesta aplikacije PSA uklonjene su iz sustava.  
Funkcionalnost povezana s prebacivanjem obrasca za Priliku, Ponudu, Narudžbu, Fakturu zastarjela je, više nije potrebna jer modul aplikacije UCI uključuje samo PSA verzije obrazaca.  

Zastarjeli su sljedeći web-resursi:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Cijeli popis zastarjelih resursa potražite u odjeljku [Zastarjeli web-resursi u aplikaciji Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).


