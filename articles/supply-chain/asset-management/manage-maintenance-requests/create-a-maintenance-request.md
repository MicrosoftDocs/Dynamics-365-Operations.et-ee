---
title: Hooldustaotluste loomine
description: Selles teemas selgitatakse, kuidas luua hooldustaotlust varahalduses.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 03e090633276cd264ad03f561ddb425a9816357e
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847501"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="09c5d-103">Hooldustaotluste loomine</span><span class="sxs-lookup"><span data-stu-id="09c5d-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="09c5d-104">Hooldustaotlusi saab kasutada juhul, kui hooldustöötajad või tootmistöötajad avastavad, et seadmed vajavad parandamist, kuid parandustööd ei saa kohe ära teha.</span><span class="sxs-lookup"><span data-stu-id="09c5d-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="09c5d-105">**Näide:** kui hooldustöötaja teeb remonti ja avastab, et samas kohas peab hooldama ka teist vara.</span><span class="sxs-lookup"><span data-stu-id="09c5d-105">**Example:** While a maintenance worker is making a repair, she discovers that another asset at the same location must be serviced.</span></span> <span data-ttu-id="09c5d-106">Hooldustöötajal ei ole aga aega ega vajalikke varuosi parandustöö jaoks.</span><span class="sxs-lookup"><span data-stu-id="09c5d-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="09c5d-107">Seetõttu loob ta vara hooldustaotluse ja sisestab probleemi lühikirjelduse.</span><span class="sxs-lookup"><span data-stu-id="09c5d-107">Therefore, she creates a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="09c5d-108">Jaotis **Aktiivsed hoolduse taotlused** paanil **Seotud teave** lehe **Kõik varad** paremal küljel või lehel **Aktiivsed varad** (**Varahaldus**\>**Üldine**\>**Varad**\>**Kõik varad** või **Aktiivsed varad**) näitab aktiivseid hooldustaotlusi, mis on seotud valitud varaga.</span><span class="sxs-lookup"><span data-stu-id="09c5d-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="09c5d-109">Valige **Varahaldus**\>**Ühised**\>**Hooldustaotlused**\>**Kõik hooldustaotlused** või **Aktiivsed hooldustaotlused**.</span><span class="sxs-lookup"><span data-stu-id="09c5d-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="09c5d-110">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="09c5d-110">Select **New**.</span></span>
3. <span data-ttu-id="09c5d-111">Dialoogiboksis **Loo taotlus** väljal **Hoolduse taotluse tüüp** valige hooldustaotluse tüüp.</span><span class="sxs-lookup"><span data-stu-id="09c5d-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="09c5d-112">Soovitatakse vaiketüüpi.</span><span class="sxs-lookup"><span data-stu-id="09c5d-112">A default type is suggested.</span></span>
4. <span data-ttu-id="09c5d-113">Väljale **Kirjeldus** sisestage nimi või pealkiri, mis kirjeldab lühidalt hooldustaotlust.</span><span class="sxs-lookup"><span data-stu-id="09c5d-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="09c5d-114">Väljadel **Funktsionaalne asukoht** ja **Vara** valige funktsionaalne asukoht või vara või funktsionaalse asukoha ja vara kombinatsioon, nii nagu soovite.</span><span class="sxs-lookup"><span data-stu-id="09c5d-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="09c5d-115">Hooldustaotlust saate luua ilma vara valimata ja vara saab hooldustaotlusele hiljem lisada.</span><span class="sxs-lookup"><span data-stu-id="09c5d-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="09c5d-116">Kui hooldustöötaja, kes on sisse logitud rakendusse Microsoft Dynamics 365 for Finance and Operations on seotud varaga seotud ressursiga, sätestatakse väli **Vara** automaatselt.</span><span class="sxs-lookup"><span data-stu-id="09c5d-116">If the maintenance worker who is signed in to Microsoft Dynamics 365 for Finance and Operations is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="09c5d-117">Kui hoolduspäring on valitud varale juba manustatud, kuvatakse dialoogiboksi **Loo taotlus** ülaosas teateriba, mis teavitab teid olemasoleva hooldustaotluse ID-st.</span><span class="sxs-lookup"><span data-stu-id="09c5d-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="09c5d-118">Sõnumiriba teavitab teid ka sellest, kas varal on garantiileping.</span><span class="sxs-lookup"><span data-stu-id="09c5d-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="09c5d-119">Valige väljal **Hooldustase** teenuse tase, mis näitab taotluse kiireloomulisust.</span><span class="sxs-lookup"><span data-stu-id="09c5d-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="09c5d-120">Kui valisite vara 5. etapis, saate kasutada välju **Vea sümptom**, **Vea ala** ja **Vea tüüp**, et luua vea registreerimine.</span><span class="sxs-lookup"><span data-stu-id="09c5d-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="09c5d-121">Kui hooldustaotlus on põhjustanud hoolduse seisakuaja, sisestage seisakuaja alguskuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="09c5d-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="09c5d-122">Väljale **Alustaja** lisatakse automaatselt teie nimi.</span><span class="sxs-lookup"><span data-stu-id="09c5d-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="09c5d-123">Väljale **Päringu kuupäev** lisatakse automaatselt praegune kuupäev.</span><span class="sxs-lookup"><span data-stu-id="09c5d-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="09c5d-124">Saate selle välja väärtust siiski muuta.</span><span class="sxs-lookup"><span data-stu-id="09c5d-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="09c5d-125">Sisestage väljale **Märkmed** kõik nõutavad täiendavad märkused.</span><span class="sxs-lookup"><span data-stu-id="09c5d-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="09c5d-126">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="09c5d-126">Select **OK**.</span></span>

![Joonis 1](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="09c5d-128">Hoolduse taotluste hilisem töötlemine</span><span class="sxs-lookup"><span data-stu-id="09c5d-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="09c5d-129">Kui hooldustaotlus on loodud, kuid see on enne teisendatud töötellimuseks, tuleks sellel värskendada mitmesuguseid andmeid.</span><span class="sxs-lookup"><span data-stu-id="09c5d-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="09c5d-130">Tavaliselt täidab selle ülesande plaanija või mõni muu administratiivtöötaja.</span><span class="sxs-lookup"><span data-stu-id="09c5d-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="09c5d-131">Lehel **Kõik hooldustaotlused** või **Aktiivsed hooldustaotlused** valige taotlus töötamiseks ja seejärel valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="09c5d-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="09c5d-132">Üksikasjade vaates saate värskendada mitmesugust teavet.</span><span class="sxs-lookup"><span data-stu-id="09c5d-132">In the details view, you can update various information.</span></span> <span data-ttu-id="09c5d-133">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="09c5d-133">Here are some examples:</span></span>

- <span data-ttu-id="09c5d-134">Vara valimine ja kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="09c5d-134">Select and verify the asset.</span></span> <span data-ttu-id="09c5d-135">Kui peate hiljem valima mõne muu vara, valige suvandi **Vara kinnitatud** väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="09c5d-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="09c5d-136">Valige vastutustundlik hooldustöötajate rühm ja/või vastutustundlik hooldustöötaja.</span><span class="sxs-lookup"><span data-stu-id="09c5d-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="09c5d-137">Nõutava seadistuse kohta lisateabe saamiseks vaadake teemat [Vastutustundlikud hooldustöötajaid](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="09c5d-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="09c5d-138">Valige hooldustöö tüüp ja kui see teave on asjakohane, seotud hooldustöö variant ja töökaubandus.</span><span class="sxs-lookup"><span data-stu-id="09c5d-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="09c5d-139">Väljadele **Laius** ja **Pikkus** sisestage geograafilised koordinaadid.</span><span class="sxs-lookup"><span data-stu-id="09c5d-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="09c5d-140">Kõik hooldustaotlusele lisatud koordinaadid kantakse automaatselt üle seotud töötellimusele.</span><span class="sxs-lookup"><span data-stu-id="09c5d-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![Joonis 2](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="09c5d-142">Kui valite hooldustaotluse loomisel vara, saate sellele varale lisada ühe vea.</span><span class="sxs-lookup"><span data-stu-id="09c5d-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="09c5d-143">Pärast hooldustaotluse loomist saate lisada rohkem vigu, kui vajate.</span><span class="sxs-lookup"><span data-stu-id="09c5d-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="09c5d-144">Vigade lisamiseks valige **Vara viga** lehel **Kõik hoolduspäringud**.</span><span class="sxs-lookup"><span data-stu-id="09c5d-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>
