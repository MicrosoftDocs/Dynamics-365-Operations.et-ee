---
title: Dynamics 365 Supply Chain Management-i (varahalduse) integreerimine Dynamics 365 Guides-iga
description: Selles teemas selgitatakse, kuidas integreerida Microsoft Dynamics 365 Supply Chain Management-i varahalduse moodulit Dynamics 365 Guides-iga, et saada võimalus kasutada virtuaaljuhendite võimalusi oma igapäevastes teeninduse ja hoolduse töövoogudes.
author: kamaybac
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 50cfea6656e1f13532b018784fa64b2aac10fc7f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908563"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="453a8-103">Dynamics 365 Supply Chain Management-i (varahalduse) integreerimine Dynamics 365 Guides-iga</span><span class="sxs-lookup"><span data-stu-id="453a8-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="453a8-104">Te saate integreerida Microsoft Dynamics 365 Supply Chain Management-i **varahalduse** moodulit Dynamics 365 Guides-iga, et saada võimalus kasutada virtuaaljuhendite võimalusi oma igapäevastes teeninduse ja hoolduse töövoogudes.</span><span class="sxs-lookup"><span data-stu-id="453a8-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="453a8-105">Kui juhend on seotud varahalduse töökäsuga, siis näeb mobiilirakenduses Supply Chain Management (Dynamics 365) töökäsu hoolduse kontrollnimekirja avav töötaja, et saadaval on juhend.</span><span class="sxs-lookup"><span data-stu-id="453a8-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="453a8-106">Seejärel saab töötaja juhendi tuvastada ja avada rakenduses Dynamics 365 Guides HoloLens.</span><span class="sxs-lookup"><span data-stu-id="453a8-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="453a8-107">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="453a8-107">Prerequisites</span></span>

<span data-ttu-id="453a8-108">Enne kui saate lisada juhendid varahalduse töökäskudele, peate täitma järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="453a8-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="453a8-109">[Seadistage Dynamics 365 Supply Chain Management-i](../../fin-ops-core/fin-ops/index.md) versioon 10.0.9 või uuem versioon.</span><span class="sxs-lookup"><span data-stu-id="453a8-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="453a8-110">[Lülitage Supply Chain Managementi rakendustes sisse topeltkirjutamine](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="453a8-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="453a8-111">[Lülitage sisse eelväljaande funktsioon](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) **MRGuidesFeature** jaoks.</span><span class="sxs-lookup"><span data-stu-id="453a8-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="453a8-112">(Tootmiskeskkondade puhul peate esmalt esitama tugipileti, et teie rentnik lisataks eelväljaande gruppi.)</span><span class="sxs-lookup"><span data-stu-id="453a8-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="453a8-113">[Lülitage sisse järgmised konfiguratsioonivõtmed](/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) lehel **Litsentsi konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="453a8-113">[Turn on the following configuration keys](/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="453a8-114">Varahaldus \> Virtuaalne varahaldus</span><span class="sxs-lookup"><span data-stu-id="453a8-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="453a8-115">Virtuaalne \> Virtuaalne juhend</span><span class="sxs-lookup"><span data-stu-id="453a8-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="453a8-116">[Seadistage Dynamics 365 Guides-i](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versioon 200.0.0.96 või uuem versioon.</span><span class="sxs-lookup"><span data-stu-id="453a8-116">[Set up Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="453a8-117">Dynamics 365 Guides-i kasutamine varahaldusel</span><span class="sxs-lookup"><span data-stu-id="453a8-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="453a8-118">Juhendi seostamiseks kasutate varahalduse real hoolduse kontrollnimekirja.</span><span class="sxs-lookup"><span data-stu-id="453a8-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="453a8-119">Te saate seose luua hoolduse kontrollnimekirja malli, hooldustöö tüübi või töökäsu kaudu, kuna kõik kolm sisaldavad hoolduse kontrollnimekirja ridu.</span><span class="sxs-lookup"><span data-stu-id="453a8-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="453a8-120">Malli kasutamine aitab aega säästa, kuna malli saab seostada kõigi hooldustöö tüüpidega, mis seda kasutavad.</span><span class="sxs-lookup"><span data-stu-id="453a8-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="453a8-121">Näiteks seostatakse hooldustöö tüübiga seostatud juhend automaatselt ka kõigi seda töötüüpi täpsustavate töökäskudega.</span><span class="sxs-lookup"><span data-stu-id="453a8-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="453a8-122">Seevastu otse töökäsuga seostatud juhend on saadaval vaid selle konkreetse töökäsu jaoks.</span><span class="sxs-lookup"><span data-stu-id="453a8-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="453a8-123">Juhendi seostamine hoolduse kontrollnimekirja malliga</span><span class="sxs-lookup"><span data-stu-id="453a8-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="453a8-124">Juhendi seostamiseks hoolduse kontrollnimekirja malliga toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="453a8-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="453a8-125">Looge rakenduste Dynamics 365 Guides PC ja HoloLens abil juhend.</span><span class="sxs-lookup"><span data-stu-id="453a8-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="453a8-126">Juhendi loomise kohta lisateabe saamiseks vaadake järgmisi teemasid.</span><span class="sxs-lookup"><span data-stu-id="453a8-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="453a8-127">Kasutage juhendi loomiseks arvutirakendust</span><span class="sxs-lookup"><span data-stu-id="453a8-127">Use the PC app to create a guide</span></span>](/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="453a8-128">Kasutage hologrammide paigutamiseks HoloLens-i rakendust</span><span class="sxs-lookup"><span data-stu-id="453a8-128">Use the HoloLens app to place your holograms</span></span>](/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="453a8-129">Looge rakenduses Supply Chain Management [hoolduse kontrollnimekirja mall](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span><span class="sxs-lookup"><span data-stu-id="453a8-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="453a8-130">Loodud juhendi seostamine uue hoolduse kontrollnimekirja malli hoolduse kontrollnimekirja reaga.</span><span class="sxs-lookup"><span data-stu-id="453a8-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="453a8-131">Valige kiirkaardil **Hoolduse kontrollnimekirja read** rida, mida soovite juhendiga seostada.</span><span class="sxs-lookup"><span data-stu-id="453a8-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="453a8-132">Valige kiirkaardil **Seotud juhendid** suvand **Lisa juhend**.</span><span class="sxs-lookup"><span data-stu-id="453a8-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="453a8-133">![Seostage juhend hoolduse kontrollnimekirja reaga](media/am-guides-integration-add-guide.png "Seostage juhend hoolduse kontrollnimekirja reaga")</span><span class="sxs-lookup"><span data-stu-id="453a8-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="453a8-134">Valige juhend väljal **Nimi** ja seejärel valige suvand **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="453a8-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="453a8-135">![Valige nimeväljal juhend](media/am-guides-integration-select-guide.png "Valige nimeväljal juhend")</span><span class="sxs-lookup"><span data-stu-id="453a8-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="453a8-136">Hoolduse kontrollnimekirja seostamine töötüübiga.</span><span class="sxs-lookup"><span data-stu-id="453a8-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="453a8-137">[Looge hooldustöö tüüp](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) või valige olemasolev hooldustöö tüüp.</span><span class="sxs-lookup"><span data-stu-id="453a8-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="453a8-138">Valige tegevuspaanil suvand **Hooldustöö tüübi vaikesuvandid**.</span><span class="sxs-lookup"><span data-stu-id="453a8-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="453a8-139">![Hooldustöö tüübi vaikesuvandite nupp](media/am-guides-integration-job-defaults.png "Hooldustöö tüübi vaikesuvandite nupp")</span><span class="sxs-lookup"><span data-stu-id="453a8-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="453a8-140">Looge rida ja seejärel valige suvand **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="453a8-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="453a8-141">![Looge rida](media/am-guides-integration-add-line.png "Looge rida")</span><span class="sxs-lookup"><span data-stu-id="453a8-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="453a8-142">Valige toimingupaanil suvand **Hoolduse kontrollnimekiri**.</span><span class="sxs-lookup"><span data-stu-id="453a8-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="453a8-143">![Hoolduse kontrollnimekirja nupp](media/am-guides-integration-maintenance-checklist.png "Hoolduse kontrollnimekirja nupp")</span><span class="sxs-lookup"><span data-stu-id="453a8-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="453a8-144">Lisage rida kiirkaardil **Hoolduse kontrollnimekirja read** ja seejärel muutke välja **Tüüp** väärtuseks **Mall**.</span><span class="sxs-lookup"><span data-stu-id="453a8-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="453a8-145">![Muutke tüübi väärtus](media/am-guides-integration-checklist-lines.png "Muutke tüübi väärtus")</span><span class="sxs-lookup"><span data-stu-id="453a8-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="453a8-146">Valige kiirkaardil **Rea üksikasjad** väljal **Mall** see mall, mille seostasite juhendiga ja seejärel klõpsake **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="453a8-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="453a8-147">![Valige mall](media/am-guides-integration-checklist-line-details.png "Valige mall")</span><span class="sxs-lookup"><span data-stu-id="453a8-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="453a8-148">[Looge töökäsk](work-orders/manually-created-workorders.md#create-work-order) ja seejärel valige hooldustöö tüüp, mis kasutab hoolduse kontrollnimekirja malli, mille seostasite juhendiga.</span><span class="sxs-lookup"><span data-stu-id="453a8-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="453a8-149">See juhend on automaatselt töökäsuga seotud.</span><span class="sxs-lookup"><span data-stu-id="453a8-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="453a8-150">![Valige hooldustöö tüüp](media/am-guides-integration-create-work-order.png "Valige hooldustöö tüüp")</span><span class="sxs-lookup"><span data-stu-id="453a8-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="453a8-151">Töökäsu ja töötajatega seotud juhendi kuvamine.</span><span class="sxs-lookup"><span data-stu-id="453a8-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="453a8-152">Avage töökäsule ligi pääsemiseks [varahalduse mobiilne tööruum](asset-management-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="453a8-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="453a8-153">[Avage töökäsu hoolduse kontrollnimekiri](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job).</span><span class="sxs-lookup"><span data-stu-id="453a8-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="453a8-154">Valige kontrollnimekirja rida, et näha sellega seotud juhendit.</span><span class="sxs-lookup"><span data-stu-id="453a8-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="453a8-155">![Kontrollnimekirja reaga seotud juhend](media/am-guides-integration-show-guide.png "Kontrollnimekirja reaga seotud juhend")</span><span class="sxs-lookup"><span data-stu-id="453a8-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="453a8-156">Avage juhend rakenduses HoloLens.</span><span class="sxs-lookup"><span data-stu-id="453a8-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="453a8-157">![Avage juhend rakenduses HoloLens](media/am-guides-integration-hololens-select.png "Avage juhend rakenduses HoloLens")</span><span class="sxs-lookup"><span data-stu-id="453a8-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="453a8-158">Juhendi võite seostada ka otse töökäsu või töötüübi hoolduse kontrollnimekirjaga.</span><span class="sxs-lookup"><span data-stu-id="453a8-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="453a8-159">On levinud probleem, et kui seostate hoolduse kontrollnimekirja hooldustöö tüübi vaikesättega, siis ei kajastu malliga seotud juhend lehe **Hooldustöö tüübi vaikesuvandid** kiirkaardil **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="453a8-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="453a8-160">Küll aga ilmub juhend nähtavale pärast seda, kui kiirkaardil **Seotud juhendid** on töökäsu suhtes rakendatud seda töötüüpi.</span><span class="sxs-lookup"><span data-stu-id="453a8-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="453a8-161">Vt ka</span><span class="sxs-lookup"><span data-stu-id="453a8-161">See also</span></span>

- [<span data-ttu-id="453a8-162">Topeltkirjutusega ülevaade</span><span class="sxs-lookup"><span data-stu-id="453a8-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="453a8-163">Varahalduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="453a8-163">Asset management overview</span></span>](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]