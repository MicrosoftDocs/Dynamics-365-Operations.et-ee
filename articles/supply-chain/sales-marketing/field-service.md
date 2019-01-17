---
title: Integreerimine rakendusega Microsoft Dynamics 365 for Field Service
description: "Selles teemas antakse ülevaade integreerimisest rakendusega Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 08/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 95031534c43dc0578e258bc3e5376c429d72b0ab
ms.openlocfilehash: 673ab2a101cee1a3dbbb1249f582d959cecc7f7f
ms.contentlocale: et-ee
ms.lasthandoff: 12/23/2018

---

# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integreerimine rakendusega Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations võimaldab sünkroonida äriprotsesse rakenduste Finance and Operations ja Microsoft Dynamics 365 for Field Service vahel. Integreerimisstsenaariume saab konfigureerida äriprotsesside sünkroonimist lubama laiendatavates andmeintegraatori mallides ja Common Data Service’is (CDS).
Kohandatud integratsiooniprojektide loomiseks saab kasutada standardmalle, kus standardseid ja kohandatud lisavälju ja üksusi saab integratsiooni korrigeerimiseks ja konkreetsete ärivajadustega kooskõlla viimiseks vastendada. 

Välja teenuse integreerimine rajaneb olemasoleva potentsiaalse kliendi funktsioonil.

![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/field-service-integration.png)

Rakenduste Field Service ja Finance and Operations integreerimise esimeses faasis keskendutakse rakenduse Field Service töötellimuste ja lepingute arveldamise lubamisele rakenduses Finance and Operations. Toetatud voog algab rakenduses Field Service, kus töötellimuste teave sünkroonitakse müügitellimustena rakendusse Finance and Operations. Rakenduses Finance and Operations arveldatakse müügitellimused, et luua arve dokumendid. Lisaks sünkroonitakse rakenduse Field Service lepingu arvete teave rakendusse Finance and Operations. Microsoft Dynamics 365 andmeintegraator sünkroonib andmed kohandatavate projektide abil. Kohandatud integratsiooniprojektide loomiseks saab kasutada standardmalle, kus standardseid ja kohandatud lisavälju, samuti üksusi saab integratsiooni korrigeerimiseks ja konkreetsete nõuetega kooskõlla viimiseks vastendada.

Rakenduste Field Service ja Finance and Operations integratsiooni esimeses faasis võimaldatakse sünkroonida järgmisi kaupu.

- [Rakenduse Finance and Operations tooted rakenduse Field Service toote tüübi teavet sisaldavate toodetega](field-service-product.md)
- [Rakenduse Field Service töötellimused rakenduse Finance and Operations müügitellimustega](field-service-work-order.md)
- [Rakenduse Field Service arved vabas vormis arveteks rakenduses Finance and Operations](field-service-invoice.md)

Näite saamiseks, kuidas sünkroonida töökäsk Field Service’i ja Finance and Operationsi vahel, vaadake YouTube’i lühivideot [Töökäsu sünkroonimine rakenduse Microsoft Dynamics 365 integratsiooniga](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="system-requirements-for-finance-and-operations"></a>Rakenduse Finance and Operations süsteeminõuded
Rakenduse Field Service integratsioon toetab järgmisi versioone.

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations versioon 8.0 (aprill 2018) või hilisem

- Dynamics 365 for Finance and Operations versioon 8.0 (aprill 2018) väljastati aprillis 2018 ja selle rakenduse järgunumber on 8.0.30.8020 platvormivärskendusega 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Rakenduse Field Service süsteeminõuded
Rakenduse Field Service integreerimislahenduse kasutamiseks tuleb installida järgmised komponendid.

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 või hilisem

- Rakenduse Dynamics 365 for Field Service versiooni 1612 (9.0.1.733) (DB 9.0.1.733) veebiversioon või hilisem versioon.
- Lahendus Potentsiaalne klient sularahaks (P2C) rakendusele Dynamics 365, versioon 1.15.0.1 või hilisem versioon. Lahendus on allalaadimiseks saadaval [AppSource’is](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Rakenduse Field Service integreerimislahendus Dynamics 365 jaoks, versioon 1.0.0.0 või hilisem versioon. Lahendus on allalaadimiseks saadaval [AppSource’is](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegration).

# <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>Rakenduse Microsoft Dynamics 365 for Field Service integreerimine, sh lao-ja projektiinfo

Lisafunktsioon selles teises etapis on suunatud väljatehnikutele ülevaate andmiseks laoinfo kohta rakendusest Finance and Operations, võimaldades neil laovarude tasemeid uuendada ja teha materjali ülekanded. Lisaks saavad installimise või müüdud kaupade hooldamisega tegelevad firmad kasu paremast ülevaatest ja kogu müügi ja teenuse protsessi nähtavusesti koos integratsiooniprojektidega.

### <a name="functionality-includes-integration-of"></a>Funktsionaalsus sisaldab integratsiooni nende vahel:
- Laoteave
- Kaubavaru tegelik teave
- Varude ülekanded
- Varude reguleerimine
- Rakenduse Dynamics 365 for Finance and Operations projektid, mis on seotud rakenduse Dynamics 365 for Field Service töötellimustega
- Rakenduse Dynamics 365 for Field Service töötellimused, mis on seotud rakenduse Dynamics 365 for Finance and Operations projektidega, rakendage rakenduse Dynamics 365 for Finance and Operations müügitellimuse arveldamiseks selle projekti numbrit. 

![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>Rakenduste Field Service ja Finance and Operations integratsiooni teises faasis võimaldatakse sünkroonida järgmisi malle:
- Laod (rakendus Fin-Ops rakendusele Field Service) - Laod rakendusest Finance and Operations rakendusele Field Service [täpsem päring] 
- Laotoode (rakendus Fin-Ops rakendusele Field Service) - Laotaseme teave rakendusest Finance and Operations rakendusele Field Service [täpsem päring] 
- Laoseisu korrigeerimine (rakendus Field Service rakendusele Finance and Operations) - Laoseisu korrigeerimine rakendusest Field Service rakendusele Finance and Operations [täpsem päring] 
- Laoseisu ülekanded (rakendus Field Service rakendusele Finance and Operations) - Laoseisu ülekanded rakenduselt Field Service rakendusele Finance and Operations [täpsem päring] 
- Projektid (rakendus Fin-Ops rakendusele Field Service) - Projektide loend rakendusest Finance and Operations rakendusele Field Service 
- Projekti töötellimused (rakendus Field Service rakendusele Fin-Ops) – Töötellimused rakenduses Field Service müügitellimuste kohta rakenduses Finance and Operations, koos projektitoega [täpsem päring] 
- Rakenduse Field Service tooted laoühikuga (Fin-Ops müügile) – Rakenduse Finance and Operations "Müüdavad väljastatud tooted" müügile "Tooted" rakenduse Field Service jaoks, sh laoühikud 

## <a name="system-requirements-for-finance-and-operations"></a>Rakenduse Finance and Operations süsteeminõuded
Rakenduse Field Service integratsioon toetab järgmisi versioone.

- Rakenduse Dynamics 365 for Finance and Operations versioon 8.1.2 (detsember 2019) väljastati detsembris 2019 ja selle rakenduse järgunumber on 8.1.195 platvormivärskendusega 22 (7.0.5095). 

## <a name="system-requirements-for-field-service"></a>Rakenduse Field Service süsteeminõuded
Rakenduse Field Service integreerimislahenduse kasutamiseks tuleb installida järgmised komponendid.

- Rakenduse Field Service for Dynamics 365 (versioon 8.2.0.286) või uuem versioon Dynamics 365 9.1.x – väljastatud novembris 2018
- Lahendus Potentsiaalne klient sularahaks (P2C) rakendusele Dynamics 365, versioon 1.15.0.1 või hilisem versioon. Lahendus on allalaadimiseks saadaval [AppSource’is](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Rakenduse Field Service integreerimis-, projekti- ja laoseisulahendus Dynamics 365 jaoks, versioon 2.0.0.0 või hilisem versioon. Lahendus on allalaadimiseks saadaval [AppSource’is](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).

