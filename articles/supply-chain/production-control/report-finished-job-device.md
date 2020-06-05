---
title: Lõpetatuna kinnitamine mitte-litsentsiplaadiga juhitavasse asukohta töökaardi vahendist
description: See teema määrab tootmisprotsessi lõpetatud toodete lõpetamise protsessi varudesse, kui numbrimärk kontrollib asukohta.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 74e1e30f5afe51cd0ecec2530ffcb9a59eec5fee
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367241"
---
# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Lõpetatuna kinnitamine mitte-litsentsiplaadiga juhitavasse asukohta töökaardi vahendist

[!include [banner](../includes/banner.md)]

Protsess nimega Lõpetatuna kinnitamine viib valmistoodangu tootmistellimusel varudesse. Kui lõpetatud toode on lubatud täpsemate ladude protsesside jaoks, esitatakse toode lõpetatuks, mida nimetatakse tootmise väljundi asukohaks. Lisateavet tootmise väljundi asukoha seadistamise kohta vt [Tootmise väljundi asukoht](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Kui toodangu väljastuskoht on litsentsiplaadipõhine, tuleb lõpetatuna kinnitamisel esitada litsentsiplaat. Välja **Numbrimärk** on kuvatud viibal **Aruande edenemine** lehel **Töökaardi seade**. See väli on nähtav ainult viibal **Edenemistest teatamine** tootmistellimuse viimasest toimingust teatamisel ja tootmistellimuse viimane üksus lubatakse laohaldusprotsesside jaoks.

Litsentsiplaadi esitamiseks on kaks võimalust.

- Kasutaja saab valida litsentsiplaadi väljal olemasoleva litsentsiplaadi.
- Litsentsiplaat luuakse automaatselt numbriseeriast ja sisestatakse vaikimisi litsentsiplaadi väljale.

Litsentsiplaadi automaatselt loomise valik konfigureeritakse valides suvandi **Loo litsentsiplaat** lehel **Seadmete töökaardi konfigureerimine**.
