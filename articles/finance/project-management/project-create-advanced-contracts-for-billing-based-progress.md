---
title: Valmidusastmelisusel põhineva arveldamise täpsemate lepingute koostamine
description: See teema selgitab, kuidas luua projektilepinguid, et saaksite luua klientidele arveid, mis põhinevad lõpuleviidud töö protsendil.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
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
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282821"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="16f7b-103">Valmidusastmelisusel põhineva arveldamise täpsemate lepingute koostamine</span><span class="sxs-lookup"><span data-stu-id="16f7b-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="16f7b-104">See teema selgitab, kuidas luua projektilepinguid, et saaksite luua klientidele arveid, mis põhinevad lõpuleviidud töö protsendil.</span><span class="sxs-lookup"><span data-stu-id="16f7b-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="16f7b-105">Projekti jaoks seadistatavate töö eelarvekategooriate jaoks arvutatakse arvete summad automaatselt.</span><span class="sxs-lookup"><span data-stu-id="16f7b-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="16f7b-106">Arvete ajastus seadistatakse siis, kui lepite kliendiga projektilepingu tingimustes kokku.</span><span class="sxs-lookup"><span data-stu-id="16f7b-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="16f7b-107">Kasutage selles teemas toodud protsesse, et seadistada leping, seostatud projekt ja arveldusreeglid, mida kasutatakse arvesummade arvutamiseks projekti jaoks seadistatud töö eelarvekategooriate puhul.</span><span class="sxs-lookup"><span data-stu-id="16f7b-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="16f7b-108">Pärast lepingu ja projekti loomist saate seadistada projekti üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="16f7b-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="16f7b-109">Näiteks saate määratleda projekti tegevused ja määrata projekti töötajaid.</span><span class="sxs-lookup"><span data-stu-id="16f7b-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="16f7b-110">Näide</span><span class="sxs-lookup"><span data-stu-id="16f7b-110">Example</span></span>

<span data-ttu-id="16f7b-111">Teie organisatsioon on tarkvaraarenduse firma.</span><span class="sxs-lookup"><span data-stu-id="16f7b-111">Your organization is a software development firm.</span></span> <span data-ttu-id="16f7b-112">Lepite kokku, et arendate kliendile palgaarvestuse paketi kokku 20 000 USA dollari (USD) eest.</span><span class="sxs-lookup"><span data-stu-id="16f7b-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="16f7b-113">Teie organisatsioon nõustub saatma kliendile arve, kui projekti konkreetsed protsentuaalsed osad saavad valmis.</span><span class="sxs-lookup"><span data-stu-id="16f7b-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="16f7b-114">Te seadistate töö jaoks järgmised projektikategooriad, et saaksite neid kasutada arveldusprotsessis.</span><span class="sxs-lookup"><span data-stu-id="16f7b-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="16f7b-115">Nõustamine</span><span class="sxs-lookup"><span data-stu-id="16f7b-115">Consulting</span></span>
- <span data-ttu-id="16f7b-116">Kujundus</span><span class="sxs-lookup"><span data-stu-id="16f7b-116">Design</span></span>
- <span data-ttu-id="16f7b-117">Install</span><span class="sxs-lookup"><span data-stu-id="16f7b-117">Installation</span></span>

<span data-ttu-id="16f7b-118">Samuti seadistate arveldusreeglid, mis arvutavad automaatselt arvesummad igas kategoorias lõpuleviidud projekti töö protsendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="16f7b-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="16f7b-119">Eelarvejuht loob projektikategooriate eelarve.</span><span class="sxs-lookup"><span data-stu-id="16f7b-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="16f7b-120">Lõpuleviidud töö hulk arvutatakse automaatselt protsentidena, võrreldes eelarvelist hulka tegeliku tööga.</span><span class="sxs-lookup"><span data-stu-id="16f7b-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="16f7b-121">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="16f7b-121">Prerequisites</span></span>

<span data-ttu-id="16f7b-122">Enne kui loote projekti, mis kasutab arveldusreegleid, peate seadistama arveldusreeglite jaoks numbriseeriad ja tasu töölehe, mida kasutatakse valmidusastmelise arvelduse sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="16f7b-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="16f7b-123">Avage **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Projektihalduse ja raamatupidamise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="16f7b-124">Seadistage lehel **Projektihalduse ja raamatupidamise parameetrid** vahekaardil **Numbriseeriad** need numbriseeriad, mida soovite arveldusreeglite loomisel kasutada.</span><span class="sxs-lookup"><span data-stu-id="16f7b-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="16f7b-125">Avage **Projektihaldus ja raamatupidamine** \> **Töölehed** \> **Tasu**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="16f7b-126">Valige lehel **Tasu tööleht** valik **Uus** ja sisestage töölehe nimi.</span><span class="sxs-lookup"><span data-stu-id="16f7b-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="16f7b-127">Valmidusastmelise arvelduse lepingu loomine</span><span class="sxs-lookup"><span data-stu-id="16f7b-127">Create a contract for progress billings</span></span>

<span data-ttu-id="16f7b-128">Selle toimingu abil saate luua projektilepingu fikseeritud hinnaga projekti jaoks.</span><span class="sxs-lookup"><span data-stu-id="16f7b-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="16f7b-129">Saate luua projekti arve, kui projektis lõpuleviidud töö hulk jõuab kindlaksmääratud protsendimäärani.</span><span class="sxs-lookup"><span data-stu-id="16f7b-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="16f7b-130">Avage **Projektihaldus ja raamatupidamine** \> **Projektid** \> **Projektilepingud**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="16f7b-131">Lehel **Projektilepingud** valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="16f7b-132">Dialoogiboksis **Uus projektileping** määrake järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="16f7b-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="16f7b-133">**Nimi**</span><span class="sxs-lookup"><span data-stu-id="16f7b-133">**Name**</span></span>
    - <span data-ttu-id="16f7b-134">**Rahastamise tüüp**</span><span class="sxs-lookup"><span data-stu-id="16f7b-134">**Funding type**</span></span>
    - <span data-ttu-id="16f7b-135">**Rahastamise allikas**</span><span class="sxs-lookup"><span data-stu-id="16f7b-135">**Funding source**</span></span>
    - <span data-ttu-id="16f7b-136">**Müügivaluuta** – vaikimisi kasutatakse seda valuutat kliendiarvete jaoks, mis on seostatud projektilepinguga.</span><span class="sxs-lookup"><span data-stu-id="16f7b-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="16f7b-137">Siiski saate muuta kindla kliendiarve müügivaluutat.</span><span class="sxs-lookup"><span data-stu-id="16f7b-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="16f7b-138">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-138">Select **OK**.</span></span> <span data-ttu-id="16f7b-139">Teave kopeeritakse lehe **Projektilepingud** päisele.</span><span class="sxs-lookup"><span data-stu-id="16f7b-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="16f7b-140">Täitke lehel **Projektilepingud** ülejäänud nõutud teave projekti jaoks.</span><span class="sxs-lookup"><span data-stu-id="16f7b-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="16f7b-141">Valmidusastmelise arvelduse projekti loomine</span><span class="sxs-lookup"><span data-stu-id="16f7b-141">Create a project for progress billings</span></span>

<span data-ttu-id="16f7b-142">Järgige neid samme, et luua projekt ja mis tahes alamprojektid, mis on projektilepinguga seostatud.</span><span class="sxs-lookup"><span data-stu-id="16f7b-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="16f7b-143">Avage **Projektihaldus ja raamatupidamine** \> **Projektid** \> **Kõik projektid**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="16f7b-144">Valige lehel **Kõik projektid** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="16f7b-145">Valige dialoogiboksis **Uus projekt** väljal **Projekti tüüp** suvand **Aeg ja materjal**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="16f7b-146">Valige projektigrupp.</span><span class="sxs-lookup"><span data-stu-id="16f7b-146">Select a project group.</span></span> <span data-ttu-id="16f7b-147">Projektigrupp määratleb sisestusteabe projektidele, mis on gruppi määratud.</span><span class="sxs-lookup"><span data-stu-id="16f7b-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="16f7b-148">Valige **Loo projekt**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-148">Select **Create project**.</span></span>
6. <span data-ttu-id="16f7b-149">Pärast projekti loomist seatakse projekti etapi olekuks **Pooleli**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="16f7b-150">Projekti eelarve loomine</span><span class="sxs-lookup"><span data-stu-id="16f7b-150">Create a budget for a project</span></span>

<span data-ttu-id="16f7b-151">Eelarvekategooriaid kasutatakse automaatselt kliendile arvesummade arvutamiseks igas kategoorias lõpetatud töö protsendi kohta.</span><span class="sxs-lookup"><span data-stu-id="16f7b-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="16f7b-152">Järgige neid samme hinnanguliste maksumuste eelarvekategooriate loomiseks.</span><span class="sxs-lookup"><span data-stu-id="16f7b-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="16f7b-153">Avage **Projektihaldus ja raamatupidamine** \> **Projektid** \> **Kõik projektid**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="16f7b-154">Valige lehel **Kõik projektid** soovitud projekt ja avage see.</span><span class="sxs-lookup"><span data-stu-id="16f7b-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="16f7b-155">Valige lehe **Projektid** toimingupaanil vahekaardi **Plaan** grupis **Eelarve** valik **Projekti eelarve**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="16f7b-156">Sisestage lehel **Projekti eelarve** projekti iga kategooria hinnanguline maksumus.</span><span class="sxs-lookup"><span data-stu-id="16f7b-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="16f7b-157">Valmidusastmelise arvelduse arveldusreeglite loomine</span><span class="sxs-lookup"><span data-stu-id="16f7b-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="16f7b-158">Avage **Projektihaldus ja raamatupidamine** \> **Projektid** \> **Projektilepingud**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="16f7b-159">Valige lehel **Projektilepingud** projektileping ja avage see.</span><span class="sxs-lookup"><span data-stu-id="16f7b-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="16f7b-160">Valige projektilepingu lehel kiirkaardil **Arveldusreeglid** valik **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="16f7b-161">Valige lehel **Arveldusreeglid** väljal **Rea tüüp** valik **Edenemine**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="16f7b-162">Sisestage kiirkaardil **Arveldusreegli rea üksikasjad** väljale **Lepingu väärtus** lepingu koguväärtus.</span><span class="sxs-lookup"><span data-stu-id="16f7b-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="16f7b-163">Väljal **Kategooria** valige soovitud kategooria tasu kande sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="16f7b-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="16f7b-164">Väljal **Projekt** valige projekt või ülesanne, mis kasutab seda arveldusreeglit.</span><span class="sxs-lookup"><span data-stu-id="16f7b-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="16f7b-165">Valikuline: määrake arvereegel teistele projektidele.</span><span class="sxs-lookup"><span data-stu-id="16f7b-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="16f7b-166">Valige projekt kiirkaardi **Projekt** jaotises **Saadaolevad projektid** ja seejärel valige parem noolenupp, et lisada projekt jaotisse **Valitud projektid**.</span><span class="sxs-lookup"><span data-stu-id="16f7b-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="16f7b-167">Valikuline: arvutage protsendimäär, mida klient arve maksetest kinni peab.</span><span class="sxs-lookup"><span data-stu-id="16f7b-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="16f7b-168">Kiirkaardil **Makse kinnipidamise tingimused** valige rahastamisallikas ja sisestage seejärel väljale **Kinnipidamise protsent** kinnipidamise protsent.</span><span class="sxs-lookup"><span data-stu-id="16f7b-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="16f7b-169">Korrake neid samme, et luua projektilepingu jaoks täiendavad arveldusreeglid.</span><span class="sxs-lookup"><span data-stu-id="16f7b-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
