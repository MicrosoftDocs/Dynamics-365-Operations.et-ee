---
title: Lõpetatuna kinnitamine mitte-litsentsiplaadiga juhitavasse asukohta töökaardi vahendist
description: See teema määrab tootmisprotsessi lõpetatud toodete lõpetamise protsessi varudesse, kui numbrimärk kontrollib asukohta.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: cb809e596fd6bf3030bcee460838798435512b95
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572125"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Lõpetatuna kinnitamine mitte-litsentsiplaadiga juhitavasse asukohta töökaardi vahendist 

Protsess nimega Lõpetatuna kinnitamine viib valmistoodangu tootmistellimusel varudesse. Kui lõpetatud toode on lubatud täpsemate ladude protsesside jaoks, esitatakse toode lõpetatuks, mida nimetatakse tootmise väljundi asukohaks. Lisateavet tootmise väljundi asukoha seadistamise kohta vt [Tootmise väljundi asukoht](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Selle ülesande lõpetamiseks peate valima olemasoleva numbrimärgi numbri. Kui tootmise väljundi asukoht on seadistatud jälgima numbrimärgi järgi, tuleb tootmise väljundi asukoha lõpetatuna kinnitamisel kaasata numbrimärgi number. Välja **Numbrimärk** on kuvatud viibal **Aruande edenemine** lehel **Töökaardi seade**. See väli on nähtav ainult viibal **Aruande edenemine** tootmistellimuse viimasel operatsioonil. Välja kuvatakse ainult siis, kui tootmistellimuse kaup on laohalduse protsesside jaoks lubatud. 
