---
title: Projektihinnangu eemaldamine
description: See teema annab teavet projektihinnangu eemaldamise kohta pärast selle lõpule viimist.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410210"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="84981-103">Projektihinnangu eemaldamine</span><span class="sxs-lookup"><span data-stu-id="84981-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84981-104">Projektihinnangud võimaldavad kuvada projekti jaoks hinnanguliselt vaja mineva ja plaanitud töö finantsandmeid.</span><span class="sxs-lookup"><span data-stu-id="84981-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="84981-105">Projektihinnangutega töötamiseks tuleb projekt siduda hinnanguprojektiga.</span><span class="sxs-lookup"><span data-stu-id="84981-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="84981-106">Hinnanguprojekt põhineb alati mõnel olemasoleval projektil, kuid ühele hinnanguprojektile võib viidata mitu projekti.</span><span class="sxs-lookup"><span data-stu-id="84981-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="84981-107">Hinnanguprojektidele saab lisada ainult fikseeritud hinnaga ja investeerimisprojekte ning need projektid peavad kuuluma hinnanguprojektiga samasse projektigruppi.</span><span class="sxs-lookup"><span data-stu-id="84981-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="84981-108">Hinnanguprojekti eemaldamiseks peab see olema lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="84981-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="84981-109">Järgmistes etappides on kirjeldatud, kuidas hinnangut eemaldada.</span><span class="sxs-lookup"><span data-stu-id="84981-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="84981-110">Avage **Projektihaldus ja raamatupidamine** > **Kõik projektid** ning avage projekt.</span><span class="sxs-lookup"><span data-stu-id="84981-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="84981-111">Valige vahekaardil **Haldamine** suvand **Hinnangud** ning valige lehel **Hinnangud** suvand **Eemaldamine**.</span><span class="sxs-lookup"><span data-stu-id="84981-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="84981-112">Seadke lehel **Hinnangu eemaldamine**, mis asub vahekaardil **Üldine**, järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="84981-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="84981-113">**Perioodi kood**: valige perioodi kood vajalike hinnanguprojektide valimiseks.</span><span class="sxs-lookup"><span data-stu-id="84981-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="84981-114">**Hinnangu kuupäev:** valige eemaldamiseks sobiv hinnangu kuupäev.</span><span class="sxs-lookup"><span data-stu-id="84981-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="84981-115">**Eemalda WIP-hoiatustega**: lubage see suvand teatise saamiseks, kui poolelioleva (WIP) üksusega seotud hinnang eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="84981-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="84981-116">Kui see suvand ei ole lubatud, ei saa eemaldamine mittehinnatud kannete olemasolu korral jätkuda.</span><span class="sxs-lookup"><span data-stu-id="84981-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="84981-117">See suvand on saadaval vaid siis, kui eemaldamistoimingut rakendatakse hinnanguprojekti puhul.</span><span class="sxs-lookup"><span data-stu-id="84981-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="84981-118">See ei ole saadaval, kui kasutate perioodilisi sisestusi.</span><span class="sxs-lookup"><span data-stu-id="84981-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="84981-119">See säte toimib sätetega, mis asuvad lehe **Projekti parameetrid** vahekaardil **Hinnang** väljagrupis **Luba eemaldamine mittehinnatud kannete olemasolu korral**.</span><span class="sxs-lookup"><span data-stu-id="84981-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="84981-120">**Märgi etapp lõpetatuks**: lubage see suvand, et seada hinnanguprojekti etapp pärast eemaldamise käitamist olekusse **Lõpetatud**.</span><span class="sxs-lookup"><span data-stu-id="84981-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="84981-121">**Prindi hinnanguloend**: valige hinnanguloendi printimisel kaasatav teave.</span><span class="sxs-lookup"><span data-stu-id="84981-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="84981-122">**Kuva teabelogi**: lubage see suvand teabelogi kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="84981-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="84981-123">**Sisestuskuupäev**: valige hinnangu pearaamatusse sisestamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="84981-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="84981-124">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="84981-124">Select **OK**.</span></span>
5. <span data-ttu-id="84981-125">Kui eemaldamisprotsess on lõpetatud, kuvatakse eemaldatud hinnanguprojekt negatiivse väärtusega.</span><span class="sxs-lookup"><span data-stu-id="84981-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="84981-126">Kui te ei plaaninud hinnangut eemaldada, saate valida eemaldatud hinnangu ja klõpsata suvandit **Tühista eemaldamine**.</span><span class="sxs-lookup"><span data-stu-id="84981-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
