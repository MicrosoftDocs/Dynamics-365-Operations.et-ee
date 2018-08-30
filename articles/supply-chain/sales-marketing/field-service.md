---
title: Integreerimine rakendusega Microsoft Dynamics 365 for Field Service
description: "Selles teemas antakse ülevaade integreerimisest rakendusega Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
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
ms.sourcegitcommit: a57e23691a6b4d48c6b8dd6d1f61fc9730365b39
ms.openlocfilehash: 0c1268d2fddcf7b28ecfc3197f21e9d30a5a5855
ms.contentlocale: et-ee
ms.lasthandoff: 05/31/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integreerimine rakendusega Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations võimaldab sünkroonida äriprotsesse rakenduste Finance and Operations ja Microsoft Dynamics 365 for Field Service vahel. Integreerimisstsenaariume saab konfigureerida äriprotsesside sünkroonimist lubama laiendatavates andmeintegraatori mallides ja Common Data Service’is (CDS).

[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/field-service-integration.png)](./media/field-service-integration.png)

Rakenduste Field Service ja Finance and Operations integreerimise esimeses faasis keskendutakse rakenduse Field Service töötellimuste ja lepingute arveldamise lubamisele rakenduses Finance and Operations. Toetatud voog algab rakenduses Field Service, kus töötellimuste teave sünkroonitakse müügitellimustena rakendusse Finance and Operations. Rakenduses Finance and Operations arveldatakse müügitellimused, et luua arve dokumendid. Lisaks sünkroonitakse rakenduse Field Service lepingu arvete teave rakendusse Finance and Operations. Microsoft Dynamics 365 andmeintegraator sünkroonib andmed kohandatavate projektide abil. Kohandatud integratsiooniprojektide loomiseks saab kasutada standardmalle, kus standardseid ja kohandatud lisavälju, samuti üksusi saab integratsiooni korrigeerimiseks ja konkreetsete nõuetega kooskõlla viimiseks vastendada.

Rakenduste Field Service ja Finance and Operations integratsiooni esimeses faasis võimaldatakse sünkroonida järgmisi kaupu.

- [Rakenduse Finance and Operations tooted rakenduse Field Service toote tüübi teavet sisaldavate toodetega](field-service-product.md)
- [Rakenduse Field Service töötellimused rakenduse Finance and Operations müügitellimustega](field-service-work-order.md)
- [Rakenduse Field Service arved vabas vormis arveteks rakenduses Finance and Operations](field-service-invoice.md)

Näite saamiseks, kuidas sünkroonida töökäsk Field Service’i ja Finance and Operationsi vahel, vaadake YouTube’i lühivideot [Töökäsu sünkroonimine rakenduste Dynamics 365 for Field Service ja Finance and Operations vahel](https://www.youtube.com/watch?v=hAB4TDVMjxU).

## <a name="system-requirements-for-finance-and-operations"></a>Rakenduse Finance and Operations süsteeminõuded
Rakenduse Field Service integratsioon toetab järgmisi versioone.

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations versioon 8.0 (aprill 2018) või hilisem

- Dynamics 365 for Finance and Operations versioon 8.0 (aprill 2018) väljastati aprillis 2018 ja selle rakenduse järgunumber on 8.0.30.8020 platvormivärskendusega 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Rakenduse Field Service süsteeminõuded
Rakenduse Field Service integreerimislahenduse kasutamiseks tuleb installida järgmised komponendid.

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 või hilisem

- Rakenduse Dynamics 365 for Field Service versiooni 1612 (9.0.1.733) (DB 9.0.1.733) veebiversioon või hilisem versioon.
- Lahendus Potentsiaalne klient sularahaks (P2C) rakendusele Dynamics 365, versioon 1.15.0.1 või hilisem versioon. Lahendus on allalaadimiseks saadaval [AppSource’is](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Rakenduse Field Service integreerimislahendus Dynamics 365 jaoks, versioon 1.0.0.0 või hilisem versioon. Lahendus on allalaadimiseks saadaval [AppSource’is](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).

