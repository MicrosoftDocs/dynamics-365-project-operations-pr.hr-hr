---
title: Konfiguriranje fakturiranja unutar tvrtke
description: U ovoj temi nalaze se informacije i primjeri o načinu konfiguriranja fakturiranja projekata unutar tvrtke.
author: sigitac
manager: tfehr
ms.date: 11/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bdb6122d8aba84d2b449f9f17a4093388b585614
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595442"
---
# <a name="configure-intercompany-invoicing"></a>Konfiguriranje fakturiranja unutar tvrtke

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Poduzmite sljedeće korake za postavljanje fakturiranja projekata unutar tvrtke u aplikaciji Dynamics 365 Project Operations. Transakcije unutar tvrtke, transakcije su vremena i troškova iz ugovora o projektu koje pripadaju jednoj tvrtki ili organizacijskoj jedinici, dok su resursi u ugovoru o projektu dio druge tvrtke ili organizacijske jedinice.

## <a name="example-configure-intercompany-invoicing"></a>Primjer: Konfiguriranje fakturiranja unutar tvrtke

U sljedećem primjeru, Contoso Robotics USA (USPM) pravna je osoba koja se zadužuje, a Contoso Robotics UK (GBPM) pravna je osoba koja kreditira. 

1. **Konfiguriraj računovodstvo između pravnih osoba unutar tvrtke**. Svaki par pravnih osoba koje se nalaze u ulozi dužnika i kreditora mora se konfigurirati na stranici Glavne knjige [Računovodstvo između pravnih osoba unutar tvrtke](https://docs.microsoft.com/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. U aplikaciji Dynamics 365 Finance, idite na **Glavna knjiga** > **Postavljanje knjiženja** > **Računovodstvo između pravnih osoba unutar tvrtke**. Stvorite zapis koji ima sljedeće podatke:

        - **Tvrtka izvora** = **GBPM**
        - **Tvrtka odredišta** = **USPM**

2. **Konfiguriraj trgovinski odnos između pravnih osoba**. U pravnoj osobi koja kreditira mora se stvoriti zapis o klijentu koji predstavlja pravnu osobu koja se zadužuje. U pravnoj osobi koja se zadužuje mora se stvoriti zapis dobavljača koji predstavlja pravnu osobu koja kreditira.

     1. U aplikaciji Finance odaberite pravnu osobu **GBPM**.
     2. Idite na **Potraživanja** > **Klijent** > **Svi klijenti**. Stvorite novi zapis za pravnu osobu, **USPM**.
     3. Proširiti **Naziv**, filtrirajte zapise prema **Vrsti** i odaberite stavku **Pravne osobe**. 
     4. Pronađite i odaberite zapis o klijentu za **Contoso Robotics USA (USPM)**.
     5. Odaberite stavku **Upotrijebi podudaranje**. 
     6. Odaberite grupu klijenata, a zatim zapis spremite.
     7. Odaberite pravnu osobu **USPM**.
     8. Idite na **Dugovanja** > **Dobavljači** > **Svi dobavljači**. Stvorite novi zapis za pravnu osobu, **GBPM**.
     9. Proširiti **Naziv**, filtrirajte zapise prema **Vrsti** i odaberite stavku **Pravne osobe**. 
     10. Pronađite i odaberite zapis o klijentu za **Contoso Robotics UK (GBPM)**.
     11. Odaberite stavku **Upotrijebi podudaranje**, odaberite grupu dobavljača, a zatim zapis spremite.
     12. U zapisu o dobavljaču odaberite **Općenito** > **Postavljanje** > **Unutar tvrtke**.
     13. Na kartici **Trgovinski odnos** mogućnost **Aktivan** postavite na **Da**.
     14. Odaberite tvrtku dobavljača **GBPM** i u stavci **Zapis mojeg računa** odaberite zapis o klijentu koji ste stvorili ranije u postupku.

3. **Konfiguriranje postavki među tvrtkama u Upravljanju projektima i računovodstveni parametri**. 

    1. Odaberite pravnu osobu **USPM** i idite u **Upravljanje projektima i računovodstvo** > **Postavljanje** > **Upravljanje projektom i računovodstveni parametri**.
    2. Na kartici **Unutar tvrtke** na kartici odaberite kategoriju nabave kako biste uparili automatski generirane fakture dobavljača.
    3. U stavci **Zadana kategorija** odaberite **Resursi unutar tvrtke**.
    4. Odaberite pravnu osobu **GBPM** i idite u **Upravljanje projektima i računovodstvo** > **Postavljanje** > **Upravljanje projektom i računovodstveni parametri**.
    5. Na kartici **Unutar tvrtke** odaberite zadanu kategoriju projekta za svaku vrstu transakcije. Kategorije projekata upotrebljavaju se za konfiguraciju poreza kada fakturirana kategorija u transakcijama unutar tvrtke postoji samo u pravnoj osobi primatelju posudbe. Možete odabrati obračun prihoda od transakcija unutar tvrtke. Obračun se događa kada se transakcije knjiže putem dnevnika Project Operations Integration u pravnoj osobi koja kreditira. Dnevnik se poništava kada se proknjiži faktura unutar tvrtke.
    6. U grupi **Pri posudbi resursa** odaberite **...** > **Novo**. 
    7. U rešetki odaberite sljedeće podatke:

          - **Pravna osoba koja se zadužuje** = **GBPM**
          - **Obračun prihoda** = **Da**
          - **Zadana kategorija vremenske tablice** = **Zadani – sat**
          - **Zadana kategorija troška** = **Zadani – trošak**

4. **Postavljanje računa za trošak i prihod unutar tvrtke u postavkama knjiženja u Glavnu knjigu**. Odobrenje u korist račun za prihode unutar poduzeća događa se u trenutku knjiženja fakture za klijenta unutar tvrtke u pravnoj osobi koja daje kredit. Terećenje računa za trošak unutar poduzeća događa se u trenutku kada se odgovarajuća faktura dobavljača koja je na čekanju proknjiži u pravnoj osobi koja se zadužuje. Ti su računi postavljeni u odgovarajućim pravnim osobama. 
      
     1. U aplikaciji Finance odaberite pravnu osobu koja se zadužuje, **USPM**. 
     2. Idite na **Upravljanje projektima i računovodstvo** > **Postavljanje** > **Knjiženje** > **Postavljanje knjiženja Glavne knjige**. 
     3. Na kartici **Računi troškova**, u stavci **Vrsta računa Glavne knjige**, odaberite **Troškovi unutar tvrtke**. Stvorite novi zapis koji ima sljedeće podatke:
      
        - **Pravna osoba koja daje kredit** = **GBPM**
        - **Glavni račun** = Odaberite glavni račun za troškove unutar tvrtke
        
     4. Odaberite pravnu osobu koja daje kredit, **GBPM**. 
     5. Idite na **Upravljanje projektima i računovodstvo** > **Postavljanje** > **Knjiženje** > **Postavljanje knjiženja Glavne knjige**. 
     6. Na kartici **Računi za prihod**, u stavci **Vrsta računa Glavne knjige**, odaberite **Prihod unutar tvrtke**. Stvorite novi zapis koji ima sljedeće podatke:

        - **Pravna osoba koja se zadužuje** = **USPM**
        - **Glavni račun** = Odaberite glavni račun za prihod unutar tvrtke 

5. **Postavite cijene prijenosa rada**. Cijene prijenosa unutar tvrtke konfigurirane su u aplikaciji Project Operations na rješenju Dataverse. Konfigurirajte [cijene troškova rada](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) i [cijene naplate rada](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) za fakturiranje između pravnih osoba unutar tvrtke. Cijene prijenosa nisu podržane za transakcije troškova unutar tvrtke. Jedinična prodajna cijena unutar tvrtke ili ustanove uvijek će biti postavljena na istu vrijednost kao i jedinična cijena koštanja resursa.

      Trošak resursa za razvojne inženjere u tvrtki Contoso Robotics UK iznosi 88 GBP po satu. Contoso Robotics UK naplatit će tvrtki Contoso Robotics USA 120 USD za svaki sat koji je ovaj resurs radio na projektima SAD-a. Contoso Robotics USA naplatit će klijentu Adventure Works 200 USD za posao koji je izvršio resurs razvojnog inženjera tvrtke Contoso Robotics UK.

      1. U aplikaciji Project Operations u rješenju Dataverse, idite na **Prodaja** > **Cjenici**. Stvorite novi cjenik troškova pod nazivom **Cijene troškova Contoso Robotics UK.** 
      2. U cjeniku troškova stvorite zapis koji sadrži sljedeće podatke:
         - **Uloga** = **Razvojni inženjer**
         - **Trošak** = **88 GBP**
      3. Idite na **Postavke** > **Organizacijske jedinice** i priložite ovaj cjenik troškova organizacijskoj jedinici **Contoso Robotics UK**.
      4. Idite na **Prodaja** > **Cjenici**. Stvorite novi cjenik troškova pod nazivom **Cijene troškova Contoso Robotics USA**. 
      5. U cjeniku troškova stvorite zapis koji sadrži sljedeće podatke:
          - **Uloga** = **Razvojni inženjer**
          - **Tvrtka za resurse** = **Contoso Robotics UK**
          - **Trošak** = **120 USD**
      6. Idite na **Postavke** > **Organizacijske jedinice** i cjenik troškova **Cijene troškova Contoso Robotics USA** priložite organizacijskoj jedinici **Contoso Robotics USA**.
      7. Idite na **Prodaja** > **Cjenici**. Stvorite prodajni cjenik pod nazivom **Cijene naplate za Adventure Works**. 
      8. U prodajnom cjeniku stvorite zapis koji sadrži sljedeće podatke:
          - **Uloga** = **Razvojni inženjer**
          - **Tvrtka za resurse** = **Contoso Robotics UK**
          - **Cijena naplate** = **200 USD**
      9. Idite na **Prodaja** > **Ugovori o projektu** i priložite cjenik **Cijene naplate za Adventure Works** cjeniku projekta Adventure Works ugovora o projektu.
