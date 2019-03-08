---
title: Põhivarale lisandi sisestamine
description: See protseduur kirjeldab lisandi lisamist olemasoleva põhivara hulka.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c9733f07f995dd37669f3c33fd0f082daa34dd2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "324418"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="b6642-103">Põhivarale lisandi sisestamine</span><span class="sxs-lookup"><span data-stu-id="b6642-103">Enter an addition to a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b6642-104">See protseduur kirjeldab lisandi lisamist olemasoleva põhivara hulka.</span><span class="sxs-lookup"><span data-stu-id="b6642-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="b6642-105">Põhivara lisandite eesmärk on jälgida vara kauba lisandeid, hooldust või remonti ja see on üksnes teavituslik.</span><span class="sxs-lookup"><span data-stu-id="b6642-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="b6642-106">Põhivara väärtus või kasutusea kõik muudatused tuleb teha eraldi.</span><span class="sxs-lookup"><span data-stu-id="b6642-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   



<span data-ttu-id="b6642-107">Protseduur kasutab raamatupidaja rolli ja demoandmeid USMF-i juriidilise isiku puhul.</span><span class="sxs-lookup"><span data-stu-id="b6642-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="b6642-108">Minge jaotisse Põhivarad > Põhivarad > Põhivarad.</span><span class="sxs-lookup"><span data-stu-id="b6642-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="b6642-109">Leidke ja valige loendist lisandi puhul põhivara.</span><span class="sxs-lookup"><span data-stu-id="b6642-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="b6642-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b6642-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b6642-111">Klõpsake toimingupaanil suvandit Põhivara.</span><span class="sxs-lookup"><span data-stu-id="b6642-111">On the Action Pane, click Fixed asset.</span></span>
5. <span data-ttu-id="b6642-112">Klõpsake suvandit Põhivara lisamised.</span><span class="sxs-lookup"><span data-stu-id="b6642-112">Click Fixed asset additions.</span></span>
6. <span data-ttu-id="b6642-113">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="b6642-113">Click New.</span></span>
7. <span data-ttu-id="b6642-114">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="b6642-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="b6642-115">Määrake lisamise ostu või teenuse kuupäev.</span><span class="sxs-lookup"><span data-stu-id="b6642-115">Set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="b6642-116">Sisestage vara kauba, hoolduse või muu paranduse hind.</span><span class="sxs-lookup"><span data-stu-id="b6642-116">Enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="b6642-117">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="b6642-117">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b6642-118">Kogukulu ei mõjuta põhivara väärtust ning on üksnes jälgimise ja teavitusliku otstarbega.</span><span class="sxs-lookup"><span data-stu-id="b6642-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="b6642-119">Kui kulud on kapitaliseeritud, tuleb väärtuse tõstmise korrigeerimise kanne sisestada eraldi.</span><span class="sxs-lookup"><span data-stu-id="b6642-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="b6642-120">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="b6642-120">Click the General tab.</span></span>
    * <span data-ttu-id="b6642-121">Märkige Pikendab kasutusiga, kui lisamine pikendab vara kasutusiga.</span><span class="sxs-lookup"><span data-stu-id="b6642-121">Set Increases service life if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="b6642-122">See väli on üksnes teavituslik.</span><span class="sxs-lookup"><span data-stu-id="b6642-122">This field is informational only.</span></span> <span data-ttu-id="b6642-123">Kasutusea pikendamiseks muutke kasutusiga väärtusmudelitel ja/või vara kulumiraamatutes.</span><span class="sxs-lookup"><span data-stu-id="b6642-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  

