---
title: Teenusetellimuste etapid
description: Hooldustellimuse etappide määratlemine ja töötajatele määramine võimaldab teil juhtida hooldustellimuse voogu ülesannetes, mida täidab teenuseorganisatsioonis mitu inimest.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6ab601891faac34db6bc5397b387c126fa1289f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215052"
---
# <a name="service-order-stages"></a><span data-ttu-id="2a19d-103">Teenusetellimuste etapid</span><span class="sxs-lookup"><span data-stu-id="2a19d-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2a19d-104">Saate häälestada teenusetellimuse etapid, et määratleda ülesanded, mis tuleb täita, ülesannete täitmise järjekord ja töötajad, kes vastutavad ülesannete täitmise eest.</span><span class="sxs-lookup"><span data-stu-id="2a19d-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="2a19d-105">Teenusetellimuse etappide määratlemine ja töötajatele määramine võimaldab teil juhtida teenusetellimuse voogu ülesannetes, mida täidab teenuseorganisatsioonis mitu inimest.</span><span class="sxs-lookup"><span data-stu-id="2a19d-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="2a19d-106">Etapiseeria peab hõlmama esmast etappi.</span><span class="sxs-lookup"><span data-stu-id="2a19d-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="2a19d-107">Saate määratleda ka igas etapis lubatud toimingud.</span><span class="sxs-lookup"><span data-stu-id="2a19d-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="2a19d-108">Näiteks kui tühjendate ruudu **Sisesta** kõikide etappide jaoks peale viimase, takistate hooldustellimuste sisestamist enne kõikide etappide läbimist.</span><span class="sxs-lookup"><span data-stu-id="2a19d-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="2a19d-109">Teenusetellimuse etappide harud</span><span class="sxs-lookup"><span data-stu-id="2a19d-109">Branching in service order stages</span></span>

<span data-ttu-id="2a19d-110">Hoolduse etapi häälestamisel saate luua mitu valikut ehk haru, mille vahel hoolduse järgmises etapis valida.</span><span class="sxs-lookup"><span data-stu-id="2a19d-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="2a19d-111">Kõik loodavad harud on pärast esmase etapi lõpuleviimist valimiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="2a19d-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="2a19d-112">Näiteks saate esimesena häälestada etapi **Plaanimine**.</span><span class="sxs-lookup"><span data-stu-id="2a19d-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="2a19d-113">Loote kaks etappi nimega **Pooleli** ja **Tühista** ning seejärel valite etapi **Plaanimine** nende emaüksuseks.</span><span class="sxs-lookup"><span data-stu-id="2a19d-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="2a19d-114">Määrate etapi **Plaanimine** müügitellimusse.</span><span class="sxs-lookup"><span data-stu-id="2a19d-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="2a19d-115">Kui müügitellimuse plaanimisetapp jõuab lõpule, saate valida etapi **Pooleli**, kui müügitellimus on töötlemiseks valmis, või etapi **Tühista**, kui müügitellimus tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="2a19d-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a19d-116">Vt ka</span><span class="sxs-lookup"><span data-stu-id="2a19d-116">See also</span></span>

[<span data-ttu-id="2a19d-117">Saate häälestada hooldustellimuse etappe.</span><span class="sxs-lookup"><span data-stu-id="2a19d-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="2a19d-118">teenustellimuse etapi muutmine</span><span class="sxs-lookup"><span data-stu-id="2a19d-118">Change the service order stage</span></span>](change-service-order-stage.md)

  


