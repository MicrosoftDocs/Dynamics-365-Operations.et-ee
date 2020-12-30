---
title: Kataloogihoolduse nõude üksikasjad
description: Selles teemas selgitatakse, kuidas luua hooldustaotlust Asset Management.
author: josaw1
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5abb62e7f92f62d4635309625d765e1c081052eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426316"
---
# <a name="maintenance-request-reports"></a><span data-ttu-id="d1252-103">Kataloogihoolduse nõude üksikasjad</span><span class="sxs-lookup"><span data-stu-id="d1252-103">Maintenance request reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d1252-104">Varahalduses saate luua kaks aruannet, mis on seotud hooldustaotlustega.</span><span class="sxs-lookup"><span data-stu-id="d1252-104">In Asset Management, you can generate two reports that are related to maintenance requests.</span></span> <span data-ttu-id="d1252-105">Ühes aruandes kuvatakse üksikasjad ja teine aruanne sisaldab loendit, mida saab kasutada planeerimise ja järelkontrolli jaoks.</span><span class="sxs-lookup"><span data-stu-id="d1252-105">One report shows details, and the other report provides a list that can be used for planning and follow-up.</span></span>

## <a name="create-a-maintenance-request-details-report"></a><span data-ttu-id="d1252-106">Hooldustaotluse üksikasjade aruande loomine</span><span class="sxs-lookup"><span data-stu-id="d1252-106">Create a Maintenance request details report</span></span>

<span data-ttu-id="d1252-107">Aruandes **Hooldustaotluse üksikasjad** kuvatakse mitmesugused hooldustaotlustega seotud andmed.</span><span class="sxs-lookup"><span data-stu-id="d1252-107">The **Maintenance request details** report shows various information that is related to maintenance requests.</span></span>

1. <span data-ttu-id="d1252-108">Valige **Varahaldus**\>**Aruanded**\>**Hooldustaotlused**\>**Hooldustaotluse üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="d1252-108">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request details**.</span></span>
2. <span data-ttu-id="d1252-109">Kiirkaardil **Kaasatavad kirjed** saate aruandesse kaasamiseks valida konkreetsed hooldustaotlused.</span><span class="sxs-lookup"><span data-stu-id="d1252-109">On the **Records to include** FastTab, you can select specific maintenance requests to include on the report.</span></span>
3. <span data-ttu-id="d1252-110">Kiirkaardil **Käivita taustal** saate seadistada aruande koostamise pakett-tööna, nagu seda vajate.</span><span class="sxs-lookup"><span data-stu-id="d1252-110">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="d1252-111">Aruande loomiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1252-111">Select **OK** to generate the report.</span></span>

<span data-ttu-id="d1252-112">Järgnev illustratsioon näitab aruande **Hooldustaotluse üksikasjade** näidet.</span><span class="sxs-lookup"><span data-stu-id="d1252-112">The following illustration shows an example of the **Maintenance request details** report.</span></span>

![Hooldusnõuete üksikasjade aruanne](media/09-manage-maintenance-requests.png)

## <a name="create-a-maintenance-request-list-report"></a><span data-ttu-id="d1252-114">Looge hooldusnõuete loendi aruanne</span><span class="sxs-lookup"><span data-stu-id="d1252-114">Create a Maintenance request list report</span></span>

<span data-ttu-id="d1252-115">Aruanne **Hooldustaotluse loend** kuvatakse kõigi sama taotlusetüübi hooldustaotluste loend.</span><span class="sxs-lookup"><span data-stu-id="d1252-115">The **Maintenance request list** report shows a list of all maintenance requests of the same request type.</span></span>

1. <span data-ttu-id="d1252-116">Valige **Varahaldus**\>**Aruanded**\>**Hooldustaotlused**\>**Hooldustaotluse loend**.</span><span class="sxs-lookup"><span data-stu-id="d1252-116">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request list**.</span></span>
2. <span data-ttu-id="d1252-117">Kiirkaardil **Kaasatavad kirjed** saate teha valikuid, et määratleda, millised hooldustaotlused aruandesse kaasatakse.</span><span class="sxs-lookup"><span data-stu-id="d1252-117">On the **Records to include** FastTab, you can make selections to define which maintenance requests are included on the report.</span></span>
3. <span data-ttu-id="d1252-118">Kiirkaardil **Käivita taustal** saate seadistada aruande koostamise pakett-tööna, nagu seda vajate.</span><span class="sxs-lookup"><span data-stu-id="d1252-118">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="d1252-119">Aruande loomiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1252-119">Select **OK** to generate the report.</span></span>

<span data-ttu-id="d1252-120">Järgnev illustratsioon näitab kõigi hooldustaotluste aruande **Hooldustaotluse loend** näidet.</span><span class="sxs-lookup"><span data-stu-id="d1252-120">The following illustration shows an example of the **Maintenance request list** report for all active maintenance requests.</span></span>

![Hooldusnõuete loendi aruanne](media/10-manage-maintenance-requests.png)
