---
title: Lähetage töökäsk
description: Selles teemas tutvustatakse, kuidas lähetada töökäsku varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d46beb04923d06aa8ccec05355731aa1b3f27c5b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889285"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="7a056-103">Lähetage töökäsk</span><span class="sxs-lookup"><span data-stu-id="7a056-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="7a056-104">Saate ajastada ühe töökäsu või selle töid ühele töötajale funktsiooni **Lähetus** kaudu.</span><span class="sxs-lookup"><span data-stu-id="7a056-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="7a056-105">Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik Töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="7a056-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="7a056-106">Valige loendist töökäsk.</span><span class="sxs-lookup"><span data-stu-id="7a056-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="7a056-107">Klõpsake vahekaardil **Üldine** suvandit **Lähetus**.</span><span class="sxs-lookup"><span data-stu-id="7a056-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="7a056-108">Valige dialoogi **Plaani töökäsk** väljal **Töötaja** töötaja.</span><span class="sxs-lookup"><span data-stu-id="7a056-108">In the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="7a056-109">Välja **Ajasta töötunde** saate sisestada eeldatavad töötunnid, kui need erinevad eelarve tundidest.</span><span class="sxs-lookup"><span data-stu-id="7a056-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="7a056-110">Vajaduse korral saate väljal **Kavandatud algus** muuta alguskuupäeva ja kellaaega.</span><span class="sxs-lookup"><span data-stu-id="7a056-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="7a056-111">Kui kavandamisprotsess peaks jälgima teistele töödele juba kavandatud ressursside võimsuse piiranguid, veenduge et tumblernuppude **Vara**, **Tööriist** ja **Töötaja** väärtus on **Jah**.</span><span class="sxs-lookup"><span data-stu-id="7a056-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to **Yes**.</span></span> <span data-ttu-id="7a056-112">Kui soovite näha üksikasjalikumat teavet kavandamisprotsessi kohta, valige tumblernupu **Sõnaohter** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="7a056-112">If you want to see detailed information about the scheduling process, select **Yes** on the **Verbose** toggle button.</span></span> <span data-ttu-id="7a056-113">See tähendab, et töökäsu arvutatud skooride üksikasjalikku teavet näidatakse Infologis.</span><span class="sxs-lookup"><span data-stu-id="7a056-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="7a056-114">Kalendris suletud päevade eiramiseks valige tumblernupu **Eira kava** väärtuseks **Jah** (kehtib vara, töötaja ja tööriistade osas).</span><span class="sxs-lookup"><span data-stu-id="7a056-114">Select **Yes** on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="7a056-115">Valige tumblernupu **Eira käivitamisajakava** väärtuseks **Jah**, et eirata piiranguid, mis võivad olla valitud kavandamise töökäsus.</span><span class="sxs-lookup"><span data-stu-id="7a056-115">Select **Yes** on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> 

    <span data-ttu-id="7a056-116">Käitamisajakava seadistamise teabe leiate jaotisest [Käitamisajakava](../setup-for-work-orders/scheduled-execution.md).</span><span class="sxs-lookup"><span data-stu-id="7a056-116">For information on the setup of scheduled execution, see the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section.</span></span>

9. <span data-ttu-id="7a056-117">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a056-117">Click **OK**.</span></span> <span data-ttu-id="7a056-118">Töökäsu töötsükli olekut värskendatakse ise vastavalt **Kavandatud** töötsükli olekule, mis on määratud kohas **Varahaldus** > **Seadistus** > **Töökäsud** > **Töötsükli mudelid**.</span><span class="sxs-lookup"><span data-stu-id="7a056-118">The work order lifecycle state is automatically updated to the **Scheduled** lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="7a056-119">Alloleval joonisel kuvatakse näidet lähetuse valikutest dialoogis **Töökäsu kavandamine**.</span><span class="sxs-lookup"><span data-stu-id="7a056-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![Joonis 1](media/04-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="7a056-121">Töökäsu ajakava kustutamiseks valige töökäsk kohas **Kõik töökäsud** ja seejärel klõpsake vahekaardil **Üldine** valikut **Kustuta ajakava**. Ärge unustage ajakava kustutamisel värskendada käsitsi töökäsu töötsükli olekut.</span><span class="sxs-lookup"><span data-stu-id="7a056-121">If you want to delete the schedule on a work order, select the work order in **All work orders**, and then click **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>

