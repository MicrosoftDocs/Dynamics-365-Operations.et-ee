---
title: Tarbimise kulum
description: Selles artiklis antakse ülevaade kulumi tarbimismeetodist.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c9d95a7a45ed99c63516749285126c786685c87
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187310"
---
# <a name="consumption-depreciation"></a><span data-ttu-id="cc85f-103">Tarbimise kulum</span><span class="sxs-lookup"><span data-stu-id="cc85f-103">Consumption depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc85f-104">Selles artiklis antakse ülevaade kulumi tarbimismeetodist.</span><span class="sxs-lookup"><span data-stu-id="cc85f-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="cc85f-105">Kui valite põhivara kulumireeglid ja teete valiku **Tarbimine** väljal **Meetod** lehel **Kulumireeglid**, määratakse põhivara kulumireeglitele kasutuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="cc85f-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="cc85f-106">Lehel **Kulumireeglid** pole vaja protsente ega intervalle seadistada.</span><span class="sxs-lookup"><span data-stu-id="cc85f-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="cc85f-107">Pärast meetodit Tarbimine kasutavate kulumireeglite loomist on meetodi seadistamiseks mitmesuguseid võimalusi.</span><span class="sxs-lookup"><span data-stu-id="cc85f-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="cc85f-108">Tarbimiskulumi seadistamine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="cc85f-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="cc85f-109">Looge lehel **Kulumireeglid** kulumireeglid.</span><span class="sxs-lookup"><span data-stu-id="cc85f-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="cc85f-110">Tarbimise arvutuste sooritamiseks peab kulumiarvestusreeglil olema ID, nimi ja valitud peab olema **Tarbimine** väljal **Meetod**.</span><span class="sxs-lookup"><span data-stu-id="cc85f-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="cc85f-111">Seadistage lehel **Tarbimistegurid** tarbimistegurid.</span><span class="sxs-lookup"><span data-stu-id="cc85f-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="cc85f-112">Igal tarbimisteguril peab olema ID, nimi ja tarbimistegur, mis on määratud koguse või protsendina.</span><span class="sxs-lookup"><span data-stu-id="cc85f-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="cc85f-113">Seadistage lehel **Tarbimisühikud** tarbimisühikud.</span><span class="sxs-lookup"><span data-stu-id="cc85f-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="cc85f-114">Igal tarbimisühikul peab olema ID ja nimi.</span><span class="sxs-lookup"><span data-stu-id="cc85f-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="cc85f-115">Kulumiühikuid kasutatakse tarbimise kulumi arvutamiseks lehel **Tarbimise kulum**.</span><span class="sxs-lookup"><span data-stu-id="cc85f-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="cc85f-116">Ühikuteks on näiteks kilomeeter (km), kilogramm (kg) ja tund.</span><span class="sxs-lookup"><span data-stu-id="cc85f-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="cc85f-117">Seadistage lehel **Põhivara** eraldi põhivarad.</span><span class="sxs-lookup"><span data-stu-id="cc85f-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="cc85f-118">Valige iga põhivara puhul väärtusmudelid ja kulumiraamatud, millel on kulumireeglid.</span><span class="sxs-lookup"><span data-stu-id="cc85f-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="cc85f-119">Peate seadistama tarbimiskulumi jaoks väärtusmudelid või kulumiraamatud, kui mõni põhivara kasutab meetodil Tarbimine põhinevaid kulumireegleid.</span><span class="sxs-lookup"><span data-stu-id="cc85f-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="cc85f-120">See seadistamine toimub kas vahekaardil **Kulum** lehel **Väärtusmudelid** või kiirkaardil **Üldine** lehel **Kulumireeglid**.</span><span class="sxs-lookup"><span data-stu-id="cc85f-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="cc85f-121">Sama väärtusmudelit saab kasutada mitme põhivara puhul.</span><span class="sxs-lookup"><span data-stu-id="cc85f-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="cc85f-122">Kulumireeglid on iga põhivara jaoks valitava väärtusmudeli või kulumiraamatu osa.</span><span class="sxs-lookup"><span data-stu-id="cc85f-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="cc85f-123">Kulumireegleid ei saa otse lehel **Põhivara** lisada ega muuta.</span><span class="sxs-lookup"><span data-stu-id="cc85f-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="cc85f-124">Kulumireegleid saab muuta ainult lehel **Kulumiraamatud**.</span><span class="sxs-lookup"><span data-stu-id="cc85f-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="cc85f-125">Sisestage lehel **Väärtusmudelid** või lehel **Kulumiraamatud** väljagrupis **Tarbimise kulum** teave järgmistele väljadele.</span><span class="sxs-lookup"><span data-stu-id="cc85f-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="cc85f-126">Tarbimistegur</span><span class="sxs-lookup"><span data-stu-id="cc85f-126">Consumption factor</span></span>
    -   <span data-ttu-id="cc85f-127">Ühik</span><span class="sxs-lookup"><span data-stu-id="cc85f-127">Unit</span></span>
    -   <span data-ttu-id="cc85f-128">Ühikukulum</span><span class="sxs-lookup"><span data-stu-id="cc85f-128">Unit depreciation</span></span>
    -   <span data-ttu-id="cc85f-129">Eeldatav tarbimine</span><span class="sxs-lookup"><span data-stu-id="cc85f-129">Estimated consumption</span></span>

    <span data-ttu-id="cc85f-130">Väljal**Sisestatud tarbimine** kuvatakse põhivara väärtusmudeli või kulumiraamatu puhul juba sisestatud tarbimiskulum määratud ühikutes.</span><span class="sxs-lookup"><span data-stu-id="cc85f-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="cc85f-131">Selle välja väärtust ei saa käsitsi värskendada.</span><span class="sxs-lookup"><span data-stu-id="cc85f-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="cc85f-132">Näited</span><span class="sxs-lookup"><span data-stu-id="cc85f-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="cc85f-133">Näide 1</span><span class="sxs-lookup"><span data-stu-id="cc85f-133">Example 1</span></span>

<span data-ttu-id="cc85f-134">31. jaanuari jaoks on seadistatud järgmine tarbimistegur:</span><span class="sxs-lookup"><span data-stu-id="cc85f-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="cc85f-135">Kogus on 1000.</span><span class="sxs-lookup"><span data-stu-id="cc85f-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="cc85f-136">Põhivarale määratud ühikukulumi väärtus on 1,5.</span><span class="sxs-lookup"><span data-stu-id="cc85f-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="cc85f-137">Kulumisoovitus on 31. jaanuaril järgmine: kogus × ühikukulum 1000 × 1,5 = 1500 Kui põhivarale määratud tegur on protsenditegur, korrutatakse kogust, mis on prognoositud põhivara väärtusmudelile väljal **Eeldatav tarbimine**, valitud lõppkuupäeva jaoks seadistatud protsendiga.</span><span class="sxs-lookup"><span data-stu-id="cc85f-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="cc85f-138">Saadud kogus pakutakse seejärel välja perioodi kulumikogusena.</span><span class="sxs-lookup"><span data-stu-id="cc85f-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="cc85f-139">Näide 2</span><span class="sxs-lookup"><span data-stu-id="cc85f-139">Example 2</span></span>

<span data-ttu-id="cc85f-140">Järgmine tarbimiskulumi tegur on seadistatud 31. jaanuari jaoks:</span><span class="sxs-lookup"><span data-stu-id="cc85f-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="cc85f-141">protsendimäär on 10.</span><span class="sxs-lookup"><span data-stu-id="cc85f-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="cc85f-142">Põhivarale määratud ühikukulumi väärtus on 1,5.</span><span class="sxs-lookup"><span data-stu-id="cc85f-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="cc85f-143">Eeldatav põhivara kogus on 2000.</span><span class="sxs-lookup"><span data-stu-id="cc85f-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="cc85f-144">Kulumisoovitus on 31. jaanuaril järgmine: hinnanguline kogus × protsent × ühikukulum 2000 × 0,10 × 1,5 = 300</span><span class="sxs-lookup"><span data-stu-id="cc85f-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>



