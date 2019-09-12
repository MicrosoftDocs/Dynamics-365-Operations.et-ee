---
title: Lähetage töökäsk
description: Selles teemas tutvustatakse, kuidas lähetada töökäsku varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3b1621cf0f1e47d7bd5fe2fa0b41fbcd61f14def
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887201"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="b05a0-103">Lähetage töökäsk</span><span class="sxs-lookup"><span data-stu-id="b05a0-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="b05a0-104">Saate ajastada ühe töökäsu või selle töid ühele töötajale funktsiooni **Lähetus** kaudu.</span><span class="sxs-lookup"><span data-stu-id="b05a0-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="b05a0-105">Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik Töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="b05a0-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="b05a0-106">Valige loendist töökäsk.</span><span class="sxs-lookup"><span data-stu-id="b05a0-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="b05a0-107">Klõpsake vahekaardil **Üldine** suvandit **Lähetus**.</span><span class="sxs-lookup"><span data-stu-id="b05a0-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="b05a0-108">Dialoogi **Plaani töökäsk** väljas **Töötaja** valige töötaja.</span><span class="sxs-lookup"><span data-stu-id="b05a0-108">n the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="b05a0-109">Välja **Ajasta töötunde** saate sisestada eeldatavad töötunnid, kui need erinevad eelarve tundidest.</span><span class="sxs-lookup"><span data-stu-id="b05a0-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="b05a0-110">Vajaduse korral saate väljal **Kavandatud algus** muuta alguskuupäeva ja kellaaega.</span><span class="sxs-lookup"><span data-stu-id="b05a0-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="b05a0-111">Kui kavandamisprotsess peaks jälgima teistele töödele juba kavandatud ressursside võimsuse piiranguid, veenduge et tumblernuppude **Vara**, **Tööriist** ja **Töötaja** väärtus on „Jah“.</span><span class="sxs-lookup"><span data-stu-id="b05a0-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to "Yes".</span></span> <span data-ttu-id="b05a0-112">Kui soovite näha üksikasjalikumat teavet kavandamisprotsessi kohta, valige tumblernupu **Sõnaohter** väärtuseks „Jah“.</span><span class="sxs-lookup"><span data-stu-id="b05a0-112">If you want to see detailed information about the scheduling process, select "Yes" on the **Verbose** toggle button.</span></span> <span data-ttu-id="b05a0-113">See tähendab, et töökäsu arvutatud skooride üksikasjalikku teavet näidatakse Infologis.</span><span class="sxs-lookup"><span data-stu-id="b05a0-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="b05a0-114">Kalendris suletud päevade eiramiseks valige tumblernupu **Eira kava** väärtuseks „Jah“ (kehtib varad, töötaja ja tööriistade osas).</span><span class="sxs-lookup"><span data-stu-id="b05a0-114">Select "Yes" on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="b05a0-115">Valige tumblernupu **Eira käivitamisajakava** väärtuseks „Jah“, et eirata piiranguid, mis võivad olla valitud kavandamise töökäsus.</span><span class="sxs-lookup"><span data-stu-id="b05a0-115">Select "Yes" on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> <span data-ttu-id="b05a0-116">Käitamisajakava seadistamise teabe leiate jaotisest [Käitamisajakava](../setup-for-work-orders/scheduled-execution.md).</span><span class="sxs-lookup"><span data-stu-id="b05a0-116">Refer to the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section for information on the setup of scheduled execution.</span></span>

9. <span data-ttu-id="b05a0-117">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="b05a0-117">Click **OK**.</span></span> <span data-ttu-id="b05a0-118">Töökäsu töötsükli olekut värskendatakse ise vastavalt „Kavandatud“ töötsükli olekule, mis on määratud kohas **Varade haldus** > **Häälestus** > **Töökäsud** > **Töötsükli mudelid**.</span><span class="sxs-lookup"><span data-stu-id="b05a0-118">The work order lifecycle state is automatically updated to the "Scheduled" lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="b05a0-119">Alloleval joonisel kuvatakse näidet lähetuse valikutest dialoogis **Töökäsu kavandamine**.</span><span class="sxs-lookup"><span data-stu-id="b05a0-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![Joonis 1](media/04-work-order-scheduling.png)

>[!NOTE]
><span data-ttu-id="b05a0-121">Töökäsu ajakava kustutamiseks valige töökäsk kohas **Kõik töökäsud** ja klõpsake vahekaardil **Üldine** valikut **Kustuta ajakava**. Ärge unustage ajakava kustutamisel värskendada käsitsi töökäsu töötsükli olekut.</span><span class="sxs-lookup"><span data-stu-id="b05a0-121">If you want to delete the schedule on a work order, this is done by selecting the work order in **All work orders** and clicking **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>

