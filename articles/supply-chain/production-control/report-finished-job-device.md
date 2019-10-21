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
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995138"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Lõpetatuna kinnitamine mitte-litsentsiplaadiga juhitavasse asukohta töökaardi vahendist 

Protsess nimega Lõpetatuna kinnitamine viib valmistoodangu tootmistellimusel varudesse. Kui lõpetatud toode on lubatud täpsemate ladude protsesside jaoks, esitatakse toode lõpetatuks, mida nimetatakse tootmise väljundi asukohaks. Lisateavet tootmise väljundi asukoha seadistamise kohta vt [Tootmise väljundi asukoht](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Selle ülesande lõpetamiseks peate valima olemasoleva numbrimärgi numbri. Kui tootmise väljundi asukoht on seadistatud jälgima numbrimärgi järgi, tuleb tootmise väljundi asukoha lõpetatuna kinnitamisel kaasata numbrimärgi number. Välja **Numbrimärk** on kuvatud viibal **Aruande edenemine** lehel **Töökaardi seade**. See väli on nähtav ainult viibal **Aruande edenemine** tootmistellimuse viimasel operatsioonil. Välja kuvatakse ainult siis, kui tootmistellimuse kaup on laohalduse protsesside jaoks lubatud. 
