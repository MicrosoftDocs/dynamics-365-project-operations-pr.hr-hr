---
title: Određivanje cijene i prihoda za projekt
description: Određivanje procjene troška i prihoda projekta u programu Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 66fa8f4374caa08b07663cc9d261bfff8ce30c87
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132999"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Određivanje cijene i prihoda za projekt 

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Procjena projekta daje financijski prikaz za procijenjeni i raspoređeni rad u strukturnoj analizi rada projekta. Prikaz procjene vas obavještava o trošku i prihodu od planiranog rada. Prikaz procjene pruža alat za prikaz podataka na nekoliko unaprijed definiranih dimenzija kako biste bili što bolje informirani o financijskom učinku projekta.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Trošak i prodajna vrijednost projekta  
[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] cjenici definiraju stope troškova i naplate za uloge projekta. Na temelju uloga povezanih sa zadacima u strukturnoj analizi rada projekta, možete odrediti trošak i prihod od rada.  
  
## <a name="cost-price-defaulting"></a>Vraćanje cijene koštanja na zadanu vrijednost  
Svaki projekt pripada organizaciji (navedenoj u stavci **Vlasnička jedinica** u projektu). Cjenik povezan s vlasničkom organizacijskom jedinicom određuje cijenu koštanja jedinice. Mogućnosti [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] određuju cijene koštanja za uloge traženjem kombinacije uloge, jedinice i organizacijske jedinice u cjeniku koštanja kako bi se dobila ispravna cijena koštanja za važeći datum redaka procjene.  
  
Ako kombinacija uloge, jedinice i organizacijske jedinice ne rezultira cijenom koštanja iz cjenika vlasničke jedinice, jedinica se zanemaruje u korist kombinacije uloge i organizacijske jedinice. Ako postoji cijena koštanja, ta cijena se pretvara u jedinicu koju ste odabrali u retku procjene.  
  
Ako kombinacija uloge i organizacijske jedinice ne rezultira cijenom koštanja, organizacijska jedinica se zanemaruje u korist kombinacije uloge i jedinice, a cijena se po potrebi nakon primjene pretvaranja vraća na zadanu vrijednost.  
  
 Ako nema cijena za ulogu, cijena koštanja vraća se na zadanu vrijednost 0,00 u retku procjene.  
  
 Svi iznosi troška u recima procjene troška projekta su u valuti vlasničke organizacijske jedinice.  
  
## <a name="sales-price-defaulting"></a>Vraćanje prodajne cijene na zadanu vrijednost  
Prodajni cjenik temelji se na prodajnom entitetu kojem je projekt pridružen. Prodajni cjenik povezan s ponudom ili ugovorom određuje prodajnu cijenu jedinice. Ako ponuda ili ugovor ima prilagođeni cjenik, to će biti zadani prodajni cjenik za procjenu projekta. Ako nema povezivanja s prodajnim entitetima, zadani prodajni cjenik konfiguriran u postavkama parametara biti će zadani prodajni cjenik za projekt. Svakom retku procjene pridružena je organizacijska jedinica resursa iz koje će se rezervirati resursi za dovršavanje zadatka. Prodajna cijena za povezane uloge određuju se traženjem kombinacije uloge, jedinice i organizacijske jedinice resursa u prodajnom cjeniku kako bi se dobila ispravna prodajna cijena za važeći datum u recima procjene.  
  
Ako kombinacija uloge, jedinice i organizacijske jedinice resursa ne rezultira prodajnom cijenom iz prodajnog cjenika, sustav će zanemariti jedinicu i tražiti kombinaciju uloge i organizacijske jedinice resursa. Ako se pronađe prodajna cijena, ta cijena se pretvara u jedinicu koju ste odabrali u retku procjene prodaje.  
  
Ako sustav ne pronađe cijenu za ulogu, prodajna cijena koštanja mora se vratiti na zadanu vrijednost 0,00 u retku procjene.  
  
Prikaz procjene je prikaz rešetke koji prikazuje plošnu rešetku redaka procjene s troškom jedinice, ukupnim troškom i prodajnom cijenom.  
  
## <a name="time-phased-view-of-project-estimates"></a>Prikaz procjene projekta s vremenskim fazama  
U prikazu za procjenu projekta s vremenskim fazama podaci procjene iz prikaza rešetke se prema zadanim postavkama zaokreću po ulozi i prikazuju proširenje podataka procjene na vremenskoj crti u odabranom vremenskom mjerilu.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Dodjela procjene truda na temelju načina zadatka  
U prikazu s vremenskim fazama, ukupni procijenjeni trud za zadatak raspoređuje se dodjelom određenog broja sati truda po vremenskom razdoblju jedinice odabranog vremenskog mjerila. U usluzi Project Service način zadatka određuje kako se trud dodjeljuje za vrijeme trajanja zadatka. Dvije vrste dodjele su ravnomjerna dodjela i dodjela na temelju radnog vremena  
  
## <a name="work-hours-based-allocation"></a>Dodjela na temelju radnog vremena  
Način zadatka automatskog raspoređivanja zahtijeva da se procijenjeni broj resursa za zadatak koristi puno radno vrijeme po danu. To se primjenjuje i kada se trud dodjeljuje dijeljenjem na trajanje zadataka u prikazu s vremenskim fazama. Na primjer, jednom na "Dan" vremensko mjerilo, za zadatak za koji se procjenjuje da će se dovršiti s jednim resursom, dodijeljeni trud po danu neće premašivati radno vrijeme po danu definirano u kalendaru projekta. Zbog toga dodjela truda uvijek osigurava da se procjenjuje korištenje resursa cijeli dan.  
  
## <a name="even-distribution"></a>Ravnomjerna distribucija  
Ručno raspoređeni način zadatka ne uzima obzir radno vrijeme, kalendar projekta ili broj resursa definiran za zadatak. Raspored zadatka temelji se na korisničkom unosu. Za takve zadatke dodjela truda po vremenskom razdoblju jedinice odabranog vremenskog mjerila nema ograničavajuće faktore. Ukupni trud za zadatak ravnomjerno se dijeli i dodjeljuje za svako vremensko razdoblje jedinice na odabranom vremenskom mjerilu.  
  
Na taj način definirani način zadatka određuje distribuciju truda ili dodjelu truda po vremenskom razdoblju jedinice u procjenama s vremenskim fazama.  
  
## <a name="grouping-and-time-phasing-options"></a>Mogućnosti grupiranja i vremenskih faza  
Ovaj prikaz vam pomaže u razumijevanju distribucije procjene truda, troška i prodaje na dnevnoj, tjednoj, mjesečnoj i godišnjoj bazi. Mogućnost Grupiraj po omogućuje zaokretanje podataka procjene po dvije druge dimenzije: kategorije i resurs. I za prikaz rešetke i prikaz s vremenskim fazama možete odabrati polja koja želite prikazati. Na dnu svakog od vremenskih blokova prikazuju se ukupni iznosi truda, troška i prodaje za dan, tjedan, mjesec ili godinu.  
  
Vraćanje cijene koštanja i prodajne cijene na zadanu vrijednost je za važeći datum – kada se stope za ulogu promijene, prikaz s vremenskim fazama bit će pregledniji kad se podaci procjene zaokrenu po stavci "Resurs" i prikaz s vremenskim fazama po tjednu.  
  
## <a name="expense-estimates"></a>Procjena troška  
Svaki trošak koji će nastati u projektu koji nije izravno povezan s radnom snagom može se zabilježiti u procjenu projekta u prikazu rešetke. To možete ostvariti korištenjem mogućnosti **Dodaj procjenu troška** u prikazu rešetke. Procjena troška može se zabilježiti za određeni zadatak ili za cijeli projekt; možete odabrati kategorije troška za te retke i odabrati uvjetni datum kada se trošak očekuje. Ako povezani cjenik troška i prodajni cjenik imaju zadane cijene ili definiranu profitnu maržu za kategorije troška, vratit će se na zadanu vrijednost u retku procjene kod povezivanja.  
  
### <a name="see-also"></a>Pogledajte također  
 [Vodič voditelja projekta](../psa/project-manager-guide.md)
