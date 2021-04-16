---
title: Põhivara soetamiste soovitamine
description: See protseduur näitab, kuidas soetada põhivara, kasutades põhivara töölehe soetussoovitust.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817158"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="cc8d5-103">Põhivara soetamiste soovitamine</span><span class="sxs-lookup"><span data-stu-id="cc8d5-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cc8d5-104">See protseduur näitab, kuidas soetada põhivara, kasutades põhivara töölehe soetussoovitust.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="cc8d5-105">See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="cc8d5-106">Põhivara soetamiseks põhivara soovituse töölehe kaudu peate esmalt looma põhivarakirje ja seejärel määratlema soetusmaksumuse vararaamatus.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="cc8d5-107">Vara soetussoovituse loomine</span><span class="sxs-lookup"><span data-stu-id="cc8d5-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="cc8d5-108">Viige vara soetussoovituse loomiseks lõpule järgmised sammud.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="cc8d5-109">Avage navigeerimispaneelil **Moodulid > Põhivarad > Töölehe kanded > Põhivarade tööleht**.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="cc8d5-110">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-110">Select **New**.</span></span>
3. <span data-ttu-id="cc8d5-111">Sisestage või valige väärtus väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="cc8d5-112">Toimingupaanil valige nupp **Alused**.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="cc8d5-113">Valige **Soovitused**.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="cc8d5-114">Valige **Soetussoovitus**.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="cc8d5-115">Valige **Filter**.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-115">Select **Filter**.</span></span> <span data-ttu-id="cc8d5-116">Eelmiste väärtuste eemaldamiseks klõpsake nuppu **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="cc8d5-117">Valige rida **Põhivara number**.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="cc8d5-118">Sisestage või valige väärtus väljal **Kriteeriumid**.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="cc8d5-119">Seadistage ülejäänud kriteeriumid põhivarade puhul, mida soovite selle soovitusega soetada.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="cc8d5-120">Paanilt väljumiseks valige kaks korda nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="cc8d5-121">Kontrollige, kas kanderead loodi.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="cc8d5-122">Soetussoovitusse kaasatakse ainult põhivarad, mille soetamiskuupäev ja soetusmaksumus on raamatus seadistatud.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="cc8d5-123">Looge raamatud lehel **Raamatud**.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="cc8d5-124">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="cc8d5-125">Lisage soetussoovitusse vaike-finantsdimensioonid</span><span class="sxs-lookup"><span data-stu-id="cc8d5-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="cc8d5-126">Soetuskande saab luua Exceli lisandmoodulite abil, minnes **Põhivarad > Töölehe kirjed > Põhivara tööleht**.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="cc8d5-127">Looge uus tööleht ja liikuge lehekülje jaotisesse **Read** ja valige Exceli ikoon ning seejärel valige põhivara töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="cc8d5-128">Süsteem loob ja avab tööleheridu tähistava Exceli malli.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="cc8d5-129">Saate mallis lisada andmeid lisatavatele tööleheridadele ja seejärel selle teabe süsteemis avaldada.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="cc8d5-130">Kui valitud vararaamatu ja vastavate põhivarade jaoks on seadistatud vaikedimensioonid, mis sisestati Exceli malli, võetakse vaike-finantsdimensioonid põhivararaamatu koondandmetest, kui tööleht avaldatakse Excelist süsteemi.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="cc8d5-131">Finantsdimensioonide lisamiseks põhivararaamatusse automaatselt põhivara töölehe avaldamisel Exceli lisandmoodulist, peavad vaikedimensioonid olema eelnevalt seadistatud.</span><span class="sxs-lookup"><span data-stu-id="cc8d5-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
