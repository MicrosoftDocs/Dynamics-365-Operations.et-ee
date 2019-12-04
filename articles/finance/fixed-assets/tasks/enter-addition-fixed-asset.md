---
title: Põhivarale lisandi sisestamine
description: See protseduur kirjeldab lisandi lisamist olemasoleva põhivara hulka.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe1a1d4db696ac013afee05b697b301383232134
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186942"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="64daf-103">Põhivarale lisandi sisestamine</span><span class="sxs-lookup"><span data-stu-id="64daf-103">Enter an addition to a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="64daf-104">See protseduur kirjeldab lisandi lisamist olemasoleva põhivara hulka.</span><span class="sxs-lookup"><span data-stu-id="64daf-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="64daf-105">Põhivara lisandite eesmärk on jälgida vara kauba lisandeid, hooldust või remonti ja see on üksnes teavituslik.</span><span class="sxs-lookup"><span data-stu-id="64daf-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="64daf-106">Põhivara väärtus või kasutusea kõik muudatused tuleb teha eraldi.</span><span class="sxs-lookup"><span data-stu-id="64daf-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   

<span data-ttu-id="64daf-107">Protseduur kasutab raamatupidaja rolli ja demoandmeid USMF-i juriidilise isiku puhul.</span><span class="sxs-lookup"><span data-stu-id="64daf-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="64daf-108">Avage navigeerimispaanil **Moodulid > Põhivara > Põhivara > Põhivara**.</span><span class="sxs-lookup"><span data-stu-id="64daf-108">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="64daf-109">Leidke ja valige loendist lisandi puhul põhivara.</span><span class="sxs-lookup"><span data-stu-id="64daf-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="64daf-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="64daf-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="64daf-111">Klõpsake toimingupaanil **Põhivara**.</span><span class="sxs-lookup"><span data-stu-id="64daf-111">On the Action Pane, click **Fixed asset**.</span></span>
5. <span data-ttu-id="64daf-112">**Klõpsake suvandit Põhivara lisamised.**</span><span class="sxs-lookup"><span data-stu-id="64daf-112">Click **Fixed asset additions**.</span></span>
6. <span data-ttu-id="64daf-113">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="64daf-113">Click **New**.</span></span>
7. <span data-ttu-id="64daf-114">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="64daf-114">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="64daf-115">Väljal **Soetamiskuupäev** määrake lisandostu või teenuse kuupäev.</span><span class="sxs-lookup"><span data-stu-id="64daf-115">In the **Acquisition date** field, set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="64daf-116">**Sisestage vara kauba, hoolduse või muu paranduse hind.**</span><span class="sxs-lookup"><span data-stu-id="64daf-116">In the **Unit cost** field, enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="64daf-117">Sisestage arv väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="64daf-117">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="64daf-118">Kogukulu ei mõjuta põhivara väärtust ning on üksnes jälgimise ja teavitusliku otstarbega.</span><span class="sxs-lookup"><span data-stu-id="64daf-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="64daf-119">Kui kulud on kapitaliseeritud, tuleb väärtuse tõstmise korrigeerimise kanne sisestada eraldi.</span><span class="sxs-lookup"><span data-stu-id="64daf-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="64daf-120">Klõpsake vahekaarti **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="64daf-120">Click the **General** tab.</span></span>

    * <span data-ttu-id="64daf-121">Märkige **Pikendab kasutusiga**, **Jah** kui lisamine pikendab vara kasutusiga.</span><span class="sxs-lookup"><span data-stu-id="64daf-121">Set **Increases service life** to **Yes** if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="64daf-122">See väli on üksnes teavituslik.</span><span class="sxs-lookup"><span data-stu-id="64daf-122">This field is informational only.</span></span> <span data-ttu-id="64daf-123">Kasutusea pikendamiseks muutke kasutusiga väärtusmudelitel ja/või vara kulumiraamatutes.</span><span class="sxs-lookup"><span data-stu-id="64daf-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  
