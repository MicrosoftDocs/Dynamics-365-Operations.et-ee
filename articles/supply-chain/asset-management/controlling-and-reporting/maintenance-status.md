---
title: Hooldusolek
description: Selles teemas tutvustatakse, kuidas arvutada hoolduse olekut varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918345"
---
# <a name="maintenance-status"></a><span data-ttu-id="e6c89-103">Hooldusolek</span><span class="sxs-lookup"><span data-stu-id="e6c89-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="e6c89-104">Varahalduses saate teha arvutusi, et näha uute, aktiivsete ja lõpetatud hooldusnõuete, töökäskude ja hoolduskatkestuste tegevuste ülevaadet teatud ajaperioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="e6c89-104">In Asset Management, you can make a calculation to see an overview of new, active, and completed maintenance requests, work orders, and maintenance downtime activities for a specific period.</span></span> <span data-ttu-id="e6c89-105">Saate näha ka sama perioodi lõpetatud tingimuse hindamiste arvu.</span><span class="sxs-lookup"><span data-stu-id="e6c89-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="e6c89-106">Kasutage seda arvutust, et saada ülevaade sissetulevate ja lõpetatud hooldusnõuete ja töökäskude töökoormusest.</span><span class="sxs-lookup"><span data-stu-id="e6c89-106">Use this calculation to get an overview of workload regarding incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="e6c89-107">Hoolduse oleku arvutuse tegemine</span><span class="sxs-lookup"><span data-stu-id="e6c89-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="e6c89-108">Klõpsake **Varahaldus** > **Päringud** > **Hoolduse olek**.</span><span class="sxs-lookup"><span data-stu-id="e6c89-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="e6c89-109">Valige dialoogist **Oleku arvutamine** see periood, millele soovite väljadel **Alguskuupäev** ja **Lõppkuupäev** arvutusi teha.</span><span class="sxs-lookup"><span data-stu-id="e6c89-109">In the **Calculate status** dialog, select the period for which you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="e6c89-110">Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohtade hoolduse ridu te soovite.</span><span class="sxs-lookup"><span data-stu-id="e6c89-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> <span data-ttu-id="e6c89-111">Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha hoolduse read ning seetõttu võivad rea olekud olla alumisel tasemel asuvate töö asukohtade summad.</span><span class="sxs-lookup"><span data-stu-id="e6c89-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="e6c89-112">Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki hoolduse ridu kõigi töö asukoha tasemete kohta, millega nad on seotud.</span><span class="sxs-lookup"><span data-stu-id="e6c89-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="e6c89-113">Arvutuse alustamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6c89-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="e6c89-114">Toimingupaani rühmades **Rühmitusalus** klõpsake asjakohastele nuppudele, et näidata arvutuse soovitud üksikasja taset.</span><span class="sxs-lookup"><span data-stu-id="e6c89-114">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="e6c89-115">Valitud toimingupaani nupud on esile tõstetud.</span><span class="sxs-lookup"><span data-stu-id="e6c89-115">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="e6c89-116">Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.</span><span class="sxs-lookup"><span data-stu-id="e6c89-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="e6c89-117">Pidage meeles klõpsata nupul **Värskenda**, et värskendada arvutust iga kord, kui teete muudatusi, aktiveerides või inaktiveerides nuppe **Rühmitusalus...** või tehes arvutusi uue perioodi jaoks.</span><span class="sxs-lookup"><span data-stu-id="e6c89-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by...** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="e6c89-118">Klõpsake valikul **Olek**, kui soovite luua uue hoolduse oleku arvutuse.</span><span class="sxs-lookup"><span data-stu-id="e6c89-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="e6c89-119">Jaotises **Hoolduse olek** kuvatavad tulemused sisaldavad ainult hooldusnõudeid ja töökäske, millel on tegeliku alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="e6c89-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="e6c89-120">Lõppkuupäev ja -kellaaeg võivad olla tühjad.</span><span class="sxs-lookup"><span data-stu-id="e6c89-120">End date and time may be blank.</span></span>

<span data-ttu-id="e6c89-121">*Näide 1.*</span><span class="sxs-lookup"><span data-stu-id="e6c89-121">*Example 1:*</span></span>

<span data-ttu-id="e6c89-122">Alloleval joonisel on nupud **Aasta** ja **Kuu** aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="e6c89-122">In the figure below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="e6c89-123">Siin saate igakuiselt üldise ülevaate hooldusnõuetega ja töökäskudega seotud töökoormusest ja läbilaskevõimest.</span><span class="sxs-lookup"><span data-stu-id="e6c89-123">Here, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Joonis 1](media/13-controlling-and-reporting.png)

<span data-ttu-id="e6c89-125">*Näide 2.*</span><span class="sxs-lookup"><span data-stu-id="e6c89-125">*Example 2:*</span></span>

<span data-ttu-id="e6c89-126">Alloleval joonisel on lisatud info töö asukohtade kohta.</span><span class="sxs-lookup"><span data-stu-id="e6c89-126">In the figure below, information about functional locations has been added.</span></span> <span data-ttu-id="e6c89-127">Nüüd on võimalik võrrelda töökoormust ja läbilaskevõimet töö asukohtade vahel, mis võib esindada geograafilisi asukohti, tehaseid või tööalasid.</span><span class="sxs-lookup"><span data-stu-id="e6c89-127">Now, it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Joonis 2](media/14-controlling-and-reporting.png)

