---
title: Põhivara soetamiste soovitamine
description: See protseduur näitab, kuidas soetada põhivara, kasutades põhivara töölehe soetussoovitust.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b35b13dc266fd5bccde437526400832d394b9aa
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177322"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="fc7c8-103">Põhivara soetamiste soovitamine</span><span class="sxs-lookup"><span data-stu-id="fc7c8-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc7c8-104">See protseduur näitab, kuidas soetada põhivara, kasutades põhivara töölehe soetussoovitust.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="fc7c8-105">See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="fc7c8-106">Avage navigeerimispaanil **Moodulid > Põhivarad > Töölehe kanded > Põhivarade tööleht**.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="fc7c8-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-107">Select **New**.</span></span>
3. <span data-ttu-id="fc7c8-108">Sisestage või valige väärtus väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="fc7c8-109">Toimingupaanil valige nupp **Alused**.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="fc7c8-110">Valige **Soovitused**.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="fc7c8-111">Valige **Soetussoovitus**.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="fc7c8-112">Valige **Filter**.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-112">Select **Filter**.</span></span> <span data-ttu-id="fc7c8-113">Eelmiste väärtuste eemaldamiseks klõpsake nuppu **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="fc7c8-114">Valige rida **Põhivara number**.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="fc7c8-115">Sisestage või valige väärtus väljal **Kriteeriumid**.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="fc7c8-116">Seadistage ülejäänud kriteeriumid põhivarade puhul, mida soovite selle soovitusega soetada.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="fc7c8-117">Paanilt väljumiseks valige kaks korda nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="fc7c8-118">Kontrollige loodud kande ridu.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="fc7c8-119">Soetussoovitusse kaasatakse ainult põhivarad, mille soetamiskuupäev ja soetusmaksumus on raamatus seadistatud.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="fc7c8-120">Looge raamatud lehel **Raamatud**.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="fc7c8-121">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="fc7c8-121">Select **Post**.</span></span>
