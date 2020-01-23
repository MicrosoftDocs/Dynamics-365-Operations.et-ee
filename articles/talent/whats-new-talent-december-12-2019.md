---
title: Mis on Dynamics 365 Talent-is uut või mida on muudetud (10. detsember 2019)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b4bb599be27e7d97fed1c060f97627c7c6a868e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915506"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>Mis on Dynamics 365 Talent-is uut või mida on muudetud (10. detsember 2019)

Selles teemas kirjeldatakse Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Muutused Onboardis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2660. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Funktsioonihalduse tööruum

Tööruumis **Funktsioonihaldus** on toodud loend igas väljaandes saadetud funktsioonidest. Vaikimisi on uued funktsioonid välja lülitatud. Saate kasutada tööruumi funktsioonide sisselülitamiseks ja nende dokumentatsiooni vaatamiseks. Lisateavet funktsioonihalduse kohta vt [Funktsioonihalduse ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Kõik uued funktsioonid jäävad vähemalt 30 päevaks eelvaatesse ja tavaliselt 30–60 päevaks. Peamised funktsioonid on tavaliselt saadaval eelvaate perioodile järgneva iga aasta oktoobris ja aprillis. Kohe kui näete tööruumis **Funktsioonihaldus** uusi võimalusi, saate need sisse lülitada. Mõned funktsioonid võivad olla vaikimisi sisse lülitatud.
 
Mõnikord on lahutamatu funktsioon vaikimisi sisse lülitatud ja seda ei saa välja lülitada (nt tööruum **Funktsioonihaldus**).
 
Kui funktsioon on üldsusele saadaval, võib selle tootmiskeskkonnas sisse või välja lülitada. Tööruum **Funktsioonihaldus** näitab, millal muutub eelvaate funktsioon kohustuslikuks. See kuupäev on tavaliselt 1. oktoobril või 1. aprillil, et ühitada poolaasta väljalaskeplaanidega. Kohustuslikke funktsioone välja lülitada ei saa. Kuni see muutub kohustuslikuks, saate funktsiooni kõikides keskkondades sisse ja välja lülitada.

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>Sujuvam töötaja vorm on liikunud funktsioonihalduse tööruumi (390583)

Selle muudatusega saab sujuvama töötaja vormi nüüd tööruumis **Funktsioonihaldus** lubada. See funktsioon on teisaldatud vormist **Süsteemi parameetrid** suvandis **Süsteemihaldus**.

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>Kirjete HcmWorkerPayrollInfo ilma töötaja väärtuseta kirjutamise takistamine (394526)

Selles väljaandes ei looda enam kirjeid **HcmWorkerPayrollInfo** allpool ilma töötaja viiteta selles stsenaariumis. 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>Tegevusega seostatud sõnumilogi ei asustada, kui tegevuse lõpetamine ebaõnnestub (374007)

See väljaanne hõlmab muudatust asustada tegevuse sõnumilogi, kui tegevus teatud stsenaariumites ebaõnnestub. 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>Teenuse Common Data Service integreerimise pakett-töö loomine (388030)

Selle muudatusega luuakse teenuse Common Data Service integreerimiseks pakett-tööd, kui teenus on lubatud.

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Täiendavaid komplekteerimislehe väärtuseid kohandatud väljade jaoks ei kajastata teenuses Common Data Service pärast rakendusnupu vajutamist kohandatud väljade vormil (379599)

Selle muudatusega sünkroonitakse nüüd muudatuste rakendamisel teenusega Common Data Service uued Talenti sisestatud komplekteerimislehtede väärtused.

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>Värskendage teenuseni Common Data Service, et puhkuse pangakande olem muutuks Talenti poolel sisendiks (352938)

See muudatus parandab probleemi, kus puhkuse pangakande olemi uuendamine lõi uue kirje Talentis.

## <a name="in-preview"></a>Eelvaates

Eelvaatefunktsioonid on saadaval ainult keskkondades **Liivakast**.

### <a name="print-performance-reviews"></a>Jõudluse ülevaadete printimine

Vt [Jõudluse ülevaadete printimine](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews), rakenduse Dynamics 365 2019. aasta väljalaskevoo plaanis 2.

