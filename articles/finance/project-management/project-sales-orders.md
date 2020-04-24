---
title: Aja- ja materjalikulu projektide müügitellimused
description: Selles teemas kirjeldatakse, kuidas aja- ja materjalikulu projektides projektipõhiseid müügitellimusi luua.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: d19ee9de70cd14c78a997b7a87c10b53ab3917b0
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249089"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="800b0-103">Aja- ja materjalikulu projektide müügitellimused</span><span class="sxs-lookup"><span data-stu-id="800b0-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="800b0-104">See teema kirjeldab, kuidas luua projekti müügitellimust.</span><span class="sxs-lookup"><span data-stu-id="800b0-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="800b0-105">Müügitellimusi saab luua ainult projektide puhul, mille tüüp on **aja- ja materjalikulu**.</span><span class="sxs-lookup"><span data-stu-id="800b0-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="800b0-106">Kui aja- ja materjalikulu projekti lepingus on mitu rahastamisallikat, peate lehel **Projektihalduse ja -arvestuse parameetrid** lubama parameetri **Luba müügitellimused mitme rahastamisallikaga projektide puhul**.</span><span class="sxs-lookup"><span data-stu-id="800b0-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="800b0-107">Mitme rahastamisallikaga projektide müügitellimuste tugi on saadaval rakenduse väljalaskes 10.0.2 ja uuemates väljalasetes.</span><span class="sxs-lookup"><span data-stu-id="800b0-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="800b0-108">Parameeter, millega lubada mitme rahastamisallikaga projektide müügitellimuste tugi, eemaldatakse 2020. aasta aprilli väljalaskevooga, pärast mida on funktsioon alati lubatud.</span><span class="sxs-lookup"><span data-stu-id="800b0-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="800b0-109">Projektipõhiseid müügitellimusi saate luua kahel viisil.</span><span class="sxs-lookup"><span data-stu-id="800b0-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="800b0-110">Otse projektis.</span><span class="sxs-lookup"><span data-stu-id="800b0-110">Go to the project itself.</span></span> <span data-ttu-id="800b0-111">Valige Tegumiribal **Halda > Kaubatoimingud > Müügitellimus**.</span><span class="sxs-lookup"><span data-stu-id="800b0-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="800b0-112">Projektiteave kasutab vaikimisi projekti müügitellimust.</span><span class="sxs-lookup"><span data-stu-id="800b0-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="800b0-113">Kui projektilepingus on rohkem kui üks rahastamisallikas, peate müügitellimuse kliendi määramiseks valima rahastamisallika.</span><span class="sxs-lookup"><span data-stu-id="800b0-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="800b0-114">Kui projektil on ainult üks rahastamisallikas, siis määratakse klient automaatselt.</span><span class="sxs-lookup"><span data-stu-id="800b0-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="800b0-115">Liikuge loendilehele **Kõik müügitellimused** ja looge uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="800b0-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="800b0-116">Peate valima müügitellimuse projekti.</span><span class="sxs-lookup"><span data-stu-id="800b0-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="800b0-117">Kui projekt on valitud, määratakse klient rahastamisallikast või kui projektil on mitu rahastamisallikat, peate valima rahastamisallika.</span><span class="sxs-lookup"><span data-stu-id="800b0-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

