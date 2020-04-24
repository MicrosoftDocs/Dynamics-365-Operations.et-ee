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
ms.openlocfilehash: f5863202facc83afb91b380ba5666334783ccbcf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211165"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="12877-103">Lõpetatuna kinnitamine mitte-litsentsiplaadiga juhitavasse asukohta töökaardi vahendist</span><span class="sxs-lookup"><span data-stu-id="12877-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="12877-104">Protsess nimega Lõpetatuna kinnitamine viib valmistoodangu tootmistellimusel varudesse.</span><span class="sxs-lookup"><span data-stu-id="12877-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="12877-105">Kui lõpetatud toode on lubatud täpsemate ladude protsesside jaoks, esitatakse toode lõpetatuks, mida nimetatakse tootmise väljundi asukohaks.</span><span class="sxs-lookup"><span data-stu-id="12877-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="12877-106">Lisateavet tootmise väljundi asukoha seadistamise kohta vt [Tootmise väljundi asukoht](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="12877-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="12877-107">Kui toodangu väljastuskoht on litsentsiplaadipõhine, tuleb lõpetatuna kinnitamisel esitada litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="12877-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="12877-108">Välja **Numbrimärk** on kuvatud viibal **Aruande edenemine** lehel **Töökaardi seade**.</span><span class="sxs-lookup"><span data-stu-id="12877-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="12877-109">See väli on nähtav ainult viibal **Edenemistest teatamine** tootmistellimuse viimasest toimingust teatamisel ja tootmistellimuse viimane üksus lubatakse laohaldusprotsesside jaoks.</span><span class="sxs-lookup"><span data-stu-id="12877-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span> 

<span data-ttu-id="12877-110">Litsentsiplaadi esitamiseks on kaks võimalust</span><span class="sxs-lookup"><span data-stu-id="12877-110">There are two options for providing the license plate</span></span>
- <span data-ttu-id="12877-111">Kasutaja valib litsentsiplaadi väljal olemasoleva litsentsiplaadi.</span><span class="sxs-lookup"><span data-stu-id="12877-111">The user is selecting an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="12877-112">Litsentsiplaat luuakse automaatselt numbriseeriast ja sisestatakse vaikimisi litsentsiplaadi väljale.</span><span class="sxs-lookup"><span data-stu-id="12877-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="12877-113">Litsentsiplaadi automaatselt loomise valik konfigureeritakse valides suvandi **Loo litsentsiplaat** lehel **Seadmete töökaardi konfigureerimine**.</span><span class="sxs-lookup"><span data-stu-id="12877-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>
