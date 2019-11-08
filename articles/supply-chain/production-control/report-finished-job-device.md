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

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="9cd74-103">Lõpetatuna kinnitamine mitte-litsentsiplaadiga juhitavasse asukohta töökaardi vahendist</span><span class="sxs-lookup"><span data-stu-id="9cd74-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="9cd74-104">Protsess nimega Lõpetatuna kinnitamine viib valmistoodangu tootmistellimusel varudesse.</span><span class="sxs-lookup"><span data-stu-id="9cd74-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="9cd74-105">Kui lõpetatud toode on lubatud täpsemate ladude protsesside jaoks, esitatakse toode lõpetatuks, mida nimetatakse tootmise väljundi asukohaks.</span><span class="sxs-lookup"><span data-stu-id="9cd74-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="9cd74-106">Lisateavet tootmise väljundi asukoha seadistamise kohta vt [Tootmise väljundi asukoht](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="9cd74-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="9cd74-107">Selle ülesande lõpetamiseks peate valima olemasoleva numbrimärgi numbri.</span><span class="sxs-lookup"><span data-stu-id="9cd74-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="9cd74-108">Kui tootmise väljundi asukoht on seadistatud jälgima numbrimärgi järgi, tuleb tootmise väljundi asukoha lõpetatuna kinnitamisel kaasata numbrimärgi number.</span><span class="sxs-lookup"><span data-stu-id="9cd74-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="9cd74-109">Välja **Numbrimärk** on kuvatud viibal **Aruande edenemine** lehel **Töökaardi seade**.</span><span class="sxs-lookup"><span data-stu-id="9cd74-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="9cd74-110">See väli on nähtav ainult viibal **Aruande edenemine** tootmistellimuse viimasel operatsioonil.</span><span class="sxs-lookup"><span data-stu-id="9cd74-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="9cd74-111">Välja kuvatakse ainult siis, kui tootmistellimuse kaup on laohalduse protsesside jaoks lubatud.</span><span class="sxs-lookup"><span data-stu-id="9cd74-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 
