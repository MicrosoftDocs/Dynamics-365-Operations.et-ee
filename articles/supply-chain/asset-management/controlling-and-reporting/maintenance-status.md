---
title: Hooldusolek
description: Selles teemas tutvustatakse, kuidas arvutada hoolduse olekut varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43389db93032ec29adb805f86ae04a686803176f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426154"
---
# <a name="maintenance-status"></a><span data-ttu-id="2def3-103">Hooldusolek</span><span class="sxs-lookup"><span data-stu-id="2def3-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2def3-104">Varahalduses saate teha ülevaatlikke arvutusi teatud perioodi kohta, et näha uusi, aktiivseid ja lõpetatud hooldusnõudeid, töökäske ja hoolduskatkestuste tegevusi.</span><span class="sxs-lookup"><span data-stu-id="2def3-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="2def3-105">Saate näha ka sama perioodi lõpetatud tingimuse hindamiste arvu.</span><span class="sxs-lookup"><span data-stu-id="2def3-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="2def3-106">Kasutage seda arvutust, et saada ülevaade sissetulevate ja lõpetatud hooldusnõuete ja töökäskude töökoormusest.</span><span class="sxs-lookup"><span data-stu-id="2def3-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="2def3-107">Hoolduse oleku arvutuse tegemine</span><span class="sxs-lookup"><span data-stu-id="2def3-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="2def3-108">Klõpsake **Varahaldus** > **Päringud** > **Hoolduse olek**.</span><span class="sxs-lookup"><span data-stu-id="2def3-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="2def3-109">Valige dialoogist **Oleku arvutamine** see ajavahemik, millele soovite väljadel **Alguskuupäev** ja **Lõppkuupäev** arvutusi teha.</span><span class="sxs-lookup"><span data-stu-id="2def3-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="2def3-110">Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohtade hoolduse ridu te soovite.</span><span class="sxs-lookup"><span data-stu-id="2def3-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="2def3-111">Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha hoolduse read ning seetõttu võivad rea olekud olla alumisel tasemel asuvate töö asukohtade summad.</span><span class="sxs-lookup"><span data-stu-id="2def3-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="2def3-112">Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki hoolduse ridu kõigi töö asukoha tasemete kohta, millega nad on seotud.</span><span class="sxs-lookup"><span data-stu-id="2def3-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="2def3-113">Arvutuse alustamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="2def3-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="2def3-114">Valige nupud **Rühmitusalus**, et vaadata arvutuse soovitud üksikasja taset.</span><span class="sxs-lookup"><span data-stu-id="2def3-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="2def3-115">Valitud nupud **Rühmitusalus** on esile tõstetud.</span><span class="sxs-lookup"><span data-stu-id="2def3-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="2def3-116">Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.</span><span class="sxs-lookup"><span data-stu-id="2def3-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="2def3-117">Pidage meeles klõpsata nuppu **Värskenda**, et värskendada arvutust iga kord, kui teete muudatusi, aktiveerides või inaktiveerides nuppe **Rühmitusalus** või tehes arvutusi uue perioodi jaoks.</span><span class="sxs-lookup"><span data-stu-id="2def3-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="2def3-118">Klõpsake valikul **Olek**, kui soovite luua uue hoolduse oleku arvutuse.</span><span class="sxs-lookup"><span data-stu-id="2def3-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="2def3-119">Jaotises **Hoolduse olek** kuvatavad tulemused sisaldavad ainult hooldusnõudeid ja töökäske, millel on tegeliku alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="2def3-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="2def3-120">Lõppkuupäev ja -kellaaeg võivad olla tühjad.</span><span class="sxs-lookup"><span data-stu-id="2def3-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="2def3-121">Näide 1</span><span class="sxs-lookup"><span data-stu-id="2def3-121">Example 1</span></span>

<span data-ttu-id="2def3-122">Alloleval kuvatõmmisel on nupud **Aasta** ja **Kuu** aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="2def3-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="2def3-123">Kui valikud **Rühmitusalus** on valitud, saate igakuiselt üldise ülevaate hooldusnõuetega ja töökäskudega seotud töökoormusest ja läbilaskevõimest.</span><span class="sxs-lookup"><span data-stu-id="2def3-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Igakuise töökoormuse näide](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="2def3-125">Näide 2</span><span class="sxs-lookup"><span data-stu-id="2def3-125">Example 2</span></span>

<span data-ttu-id="2def3-126">Alloleval kuvatõmmisel on lisatud info töö asukohtade kohta.</span><span class="sxs-lookup"><span data-stu-id="2def3-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="2def3-127">Nüüd on võimalik võrrelda töökoormust ja läbilaskevõimet töö asukohtade vahel, mis võib esindada geograafilisi asukohti, tehaseid või tööalasid.</span><span class="sxs-lookup"><span data-stu-id="2def3-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Igakuise töökoormuse näide töö asukohtadega](media/14-controlling-and-reporting.png)

