---
title: Põhivara soetamiste soovitamine
description: See protseduur näitab, kuidas soetada põhivara, kasutades põhivara töölehe soetussoovitust.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
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
ms.openlocfilehash: 0997af638c141661afb677e2407a90a883168aed
ms.sourcegitcommit: a8201e0b9033c2afc2b1702b0337facaf7ad4b92
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/28/2020
ms.locfileid: "3628881"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="91990-103">Põhivara soetamiste soovitamine</span><span class="sxs-lookup"><span data-stu-id="91990-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="91990-104">See protseduur näitab, kuidas soetada põhivara, kasutades põhivara töölehe soetussoovitust.</span><span class="sxs-lookup"><span data-stu-id="91990-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="91990-105">See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="91990-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="91990-106">Põhivara soetamiseks põhivara soovituse töölehe kaudu peate esmalt looma põhivarakirje ja seejärel määratlema soetusmaksumuse vararaamatus.</span><span class="sxs-lookup"><span data-stu-id="91990-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="91990-107">Avage navigeerimispaneelil **Moodulid > Põhivarad > Töölehe kanded > Põhivarade tööleht**.</span><span class="sxs-lookup"><span data-stu-id="91990-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="91990-108">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="91990-108">Select **New**.</span></span>
3. <span data-ttu-id="91990-109">Sisestage või valige väärtus väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="91990-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="91990-110">Toimingupaanil valige nupp **Alused**.</span><span class="sxs-lookup"><span data-stu-id="91990-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="91990-111">Valige **Soovitused**.</span><span class="sxs-lookup"><span data-stu-id="91990-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="91990-112">Valige **Soetussoovitus**.</span><span class="sxs-lookup"><span data-stu-id="91990-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="91990-113">Valige **Filter**.</span><span class="sxs-lookup"><span data-stu-id="91990-113">Select **Filter**.</span></span> <span data-ttu-id="91990-114">Eelmiste väärtuste eemaldamiseks klõpsake nuppu **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="91990-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="91990-115">Valige rida **Põhivara number**.</span><span class="sxs-lookup"><span data-stu-id="91990-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="91990-116">Sisestage või valige väärtus väljal **Kriteeriumid**.</span><span class="sxs-lookup"><span data-stu-id="91990-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="91990-117">Seadistage ülejäänud kriteeriumid põhivarade puhul, mida soovite selle soovitusega soetada.</span><span class="sxs-lookup"><span data-stu-id="91990-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="91990-118">Paanilt väljumiseks valige kaks korda nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="91990-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="91990-119">Kontrollige loodud kande ridu.</span><span class="sxs-lookup"><span data-stu-id="91990-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="91990-120">Soetussoovitusse kaasatakse ainult põhivarad, mille soetamiskuupäev ja soetusmaksumus on raamatus seadistatud.</span><span class="sxs-lookup"><span data-stu-id="91990-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="91990-121">Looge raamatud lehel **Raamatud**.</span><span class="sxs-lookup"><span data-stu-id="91990-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="91990-122">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="91990-122">Select **Post**.</span></span>
