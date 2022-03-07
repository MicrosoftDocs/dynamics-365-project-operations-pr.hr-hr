---
title: Upravljanje projektima i rezervacijama u kalendaru sustava Office 365
description: Način upravljanja projektima i rezervacijama u kalendaru sustava Office 365
author: ruhercul
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
- D365PS
- ProjectOperations
ms.openlocfilehash: b38affbfc8d339ac1a2093391286ea4c095207be8de2e8eeca558e6fcc5bcc07
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985312"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Upravljanje projektima i rezervacijama u kalendaru (Project Service)

> [!Note]
> ZASTARJELO: ova je značajka zastarjela i više nije dostupna.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Pregledajte osobne obveze, rezervacije projekata i dodjele radnih naloga usluge Field service pomoću kalendara sustava [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Budući da je sve na jednom mjestu, jednostavno je rasporediti dan. Vaši sastanci, zakazane obaveze, rezervacije i zadaci dostupni su u kalendaru [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Ako upotrebljavate [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], osobne obveze možete unijeti u prikazu vremena unosa u sustavu Project Service. To omogućuje upraviteljima projekata i resursa da znaju vašu dostupnost za projekte. Time također štedite na vremenu jer ne morate dvaput unositi podatke o osobnim obvezama. Možete jednostavno uvesti osobne obveze iz kalendara u prikaz vremena unosa u sustavu Project Service.  
  
 Kalendar će sinkronizirati projekt i rezervacije radnih naloga za razdoblje koje obuhvaća četiri tjedna od današnjeg dana. Ta se postavka ne može izmijeniti.  
  
 Podržan je samo jedan način sinkronizacije – iz PSA-a u kalendar sustava [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]. Sinkronizaciju možete izvršiti obrnutim redoslijedom. 
  
 Da biste saznali kako upotrebljavati kalendar sustava [!INCLUDE[pn_office_365](../includes/pn-office-365.md)], pogledajte kalendar u programu [Outlook na webu za tvrtke](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Instalacija  
 Da biste mogli vidjeti svoje rezervacije u kalendaru sustava [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] i njima upravljati, najprije trebate postaviti nekoliko stvari.  
  
- Za to će vam trebati vjerodajnice globalnog administratora sustava [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] ili administratora sustava.  
  
- Vaš će administrator trebati konfigurirati profil poslužitelja e-pošte, a svaki korisnik trebat će konfigurirati poštanski sandučić. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Postavljanje procesiranja e-pošte putem sinkronizacije sa strane poslužitelja](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Uključivanje sinkronizacije za vašu tvrtku ili ustanovu (administratorski zadatak)  
  
1.  Na glavnom izborniku kliknite **Postavke** > **Administracija**.  
  
2.  Kliknite **Postavke sustava**.  
  
3.  Kliknite karticu **Sinkronizacija**.  
  
4.  U odjeljku **Odaberite treba li omogućiti sinkronizaciju rezervacije resursa s programom** potvrdite opciju **Sinkronizacija rezervacije resursa s programom Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Uključivanje sinkronizacije za korisnički profil (korisnički zadatak)  
  
1.  Kliknite gumb **Postavke** u gornjem desnom kutu zaslona.  
  
2.  Kliknite **Mogućnosti**.  
  
3.  Kliknite karticu **Sinkronizacija**.  
  
4.  U odjeljku **Sinkronizacija rezervacije resursa s programom Outlook** potvrdite opciju **Rezervacija resursa za sinkronizaciju s programom Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Uvoz osobnih obveza (korisnički zadatak)  
 Možete uvesti osobne obveze iz kalendara u prikaz vremena unosa sustava Project Service Automation.  
  
1. Otvorite kalendar sustava [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] i kliknite **Uvoz podataka**.  
  
2. Na zaslonu Filtri odaberite **Obveze iz sustava Exchange**, a zatim kliknite **Primijeni**.  
  
3. Sustav će povući obveze u prikaz unosa vremena kao predložene unose iz tekućeg tjedna. Da biste dodali unose za drugi tjedan, kliknite **Prethodno** ili **Sljedeće**.  
  
4. Odaberite obvezu koju želite dodati u prikaz unosa vremena sustava Project Service Automation.  
  
5. U skočnom okviru **Unos vremena** odaberite odgovarajuće opcije da biste obvezu pretvorili u prikaz unosa vremena sustava Project Service Automation.  
  
6. Kliknite **Spremi**.  
  
### <a name="see-also"></a>Pogledajte također  
 [Vodič za vrijeme, troškove i suradnju](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]