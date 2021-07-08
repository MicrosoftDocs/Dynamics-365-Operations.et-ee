---
title: Nõudluse prognooside kohta varasemate andmete importimine
description: Täpsete nõudluse prognooside saamiseks on vaja varasemaid nõudluse andmeid kauba või kauba eraldamisvõtme kohta. Selles teemas selgitatakse, kuidas kasutada andmeüksusi varasemate nõudluse andmete importimiseks mis tahes süsteemist, et nõudluse prognoosi andmed oleksid olemas pikema perioodi kohta.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301646"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="3f1ff-104">Nõudluse prognooside kohta varasemate andmete importimine</span><span class="sxs-lookup"><span data-stu-id="3f1ff-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f1ff-105">Nõudluse prognooside täpsuse tagamiseks peab varasemaid nõudluse andmeid olema kauba või kauba eraldamisvõtme kohta võimalikult palju.</span><span class="sxs-lookup"><span data-stu-id="3f1ff-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="3f1ff-106">Kui varasemaid nõudluse andmeid pole veel imporditud, siis kasutage nende importimiseks andmeüksust **Varasem väline nõudlus** (ReqDemPlanHistoricalExternalDemandEntity) rakenduses Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3f1ff-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="3f1ff-107">Tööruumis **Andmehaldus** näete ülevaadet kõigist üksuse väljadest.</span><span class="sxs-lookup"><span data-stu-id="3f1ff-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="3f1ff-108">Avage tööruum **Andmehaldus**.</span><span class="sxs-lookup"><span data-stu-id="3f1ff-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="3f1ff-109">Valige paan **Andmeüksused**.</span><span class="sxs-lookup"><span data-stu-id="3f1ff-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="3f1ff-110">Otsige valiku **Varasem väline nõudlus** üksuste loendit.</span><span class="sxs-lookup"><span data-stu-id="3f1ff-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="3f1ff-111">Valige **Sihtväljad**.</span><span class="sxs-lookup"><span data-stu-id="3f1ff-111">Select **Target fields**.</span></span> <span data-ttu-id="3f1ff-112">Järgmised üksuste väljad on kohustuslikud: laoala (**DeliveringSiteId**), kuupäev (**DemandDate**), kogus (**DemandQuantity**) ja kas kaubakood (**ItemNumber**) või kauba eraldamisvõti (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="3f1ff-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="3f1ff-113">Andmeüksuse kasutamiseks peab teil olema Microsoft Exceli fail või komaeraldusega (CSV) fail, mis sisaldab varasema nõudluse andmeid.</span><span class="sxs-lookup"><span data-stu-id="3f1ff-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="3f1ff-114">Järgmine näide selgitab andmete importimist CSV-failist.</span><span class="sxs-lookup"><span data-stu-id="3f1ff-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="3f1ff-115">Lisateavet andmete importimise kohta, sh kuidas andmed pärast importimist korrastada, vt jaotisest [Andmete importimis- ja eksportimistööde ülevaade](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) ja sellega seotud teemadest.</span><span class="sxs-lookup"><span data-stu-id="3f1ff-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

<span data-ttu-id="3f1ff-116">Vt ka [Statistilise alusprognoosi loomine](generate-statistical-baseline-forecast.md).</span><span class="sxs-lookup"><span data-stu-id="3f1ff-116">See also [Generate a statistical baseline forecast](generate-statistical-baseline-forecast.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]