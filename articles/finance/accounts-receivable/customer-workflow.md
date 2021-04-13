---
title: Kliendi töövoog
description: Selles teemas kirjeldatakse kliendi töövoogu. Saate muuta kliendi teatud välju ja saata need muudatused töövoo abil kinnitamiseks, enne kui need lisatakse kliendile.
author: mikefalkner
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: c769d225ee0f7b35719c37d9b9bc690a20060911
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817265"
---
# <a name="customer-workflow"></a><span data-ttu-id="b9ec7-104">Kliendi töövoog</span><span class="sxs-lookup"><span data-stu-id="b9ec7-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9ec7-105">Kliendi töövoog lisati versiooni 8.0.4.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="b9ec7-106">Saate muuta kliendi teatud välju ja saata need muudatused töövoo abil kinnitamiseks, enne kui need lisatakse kliendile.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="b9ec7-107">Kliendi töövoo häälestamine</span><span class="sxs-lookup"><span data-stu-id="b9ec7-107">Set up the customer workflow</span></span>

<span data-ttu-id="b9ec7-108">Enne kliendi töövoo funktsiooni kasutamist peate selle lubama.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="b9ec7-109">Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="b9ec7-110">Funktsiooni lubamiseks määrake vahekaardi **Üldine** kiirkaardil **Kliendi kinnitus** suvandi **Luba kliendi kinnitused** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="b9ec7-111">Väljal **Andmeüksuse käitumine** valige käitumine, mida andmeüksused peaksid kasutama andmete importimisel:</span><span class="sxs-lookup"><span data-stu-id="b9ec7-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="b9ec7-112">**Luba muudatused ilma kinnitamata** – üksus saab värskendada kliendikirjet ilma selle töötlemiseta läbi töövoo.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="b9ec7-113">**Hülga muudatused** – kliendikirjele ei saa muudatusi teha.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="b9ec7-114">Väljadel, mis on töövoo jaoks lubatud, importimine nurjub.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="b9ec7-115">**Loo muudatusettepanekud** – muudetakse kõiki välju peale väljade, mis on töövoo jaoks lubatud.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="b9ec7-116">Nende väljade uued väärtused lisatakse kliendile pakutud muudatustena ja töövoog käivitatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="b9ec7-117">Valige kliendiväljade loendis märkeruut **Luba** iga välja jaoks, mis tuleb enne muudatuste tegemist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="b9ec7-118">Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro töövood**.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="b9ec7-119">Valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-119">Select **New**.</span></span>
7. <span data-ttu-id="b9ec7-120">Valige **Pakutud kliendimuudatuse töövoog**.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="b9ec7-121">Häälestage töövoog nii, et see ühtiks teie heakskiidu protsessiga.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="b9ec7-122">Töövoo kinnitamise element **Töövoo kinnitus pakutud kliendimuudatuse jaoks** rakendab muudatused kliendile.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="b9ec7-123">Klienditeabe muutmine ja muudatuste esitamine töövoole</span><span class="sxs-lookup"><span data-stu-id="b9ec7-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="b9ec7-124">Kui muudate välja, mis on töövoo jaoks lubatud, kuvatakse leht **Pakutud muudatused**.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="b9ec7-125">Sellel lehel kuvatakse välja algväärtus ning uus väärtus, mille sisestasite.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="b9ec7-126">Teie muudetud välja väärtus taastatakse algväärtusele.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="b9ec7-127">Lehe olekuteade teavitab teid, et muudatusi pole edastatud.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="b9ec7-128">Iga kord, kui muudate välja, mis on töövoo jaoks lubatud, lisatakse see väli pakutud muudatuste loendisse.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="b9ec7-129">Välja pakutud väärtuse tühistamiseks kasutage loendis välja kõrval olevat nuppu **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="b9ec7-130">Kõigi muudatuste tühistamiseks kasutage lehe allosas olevat nuppu **Tühista kõik muudatused**.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="b9ec7-131">Valige lehe sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="b9ec7-132">Kui teil on vähemalt üks pakutud muudatus, kuvatakse toimingupaanil kaks uut menüüd: **Pakutud muudatused** ja **Töövoog**.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="b9ec7-133">Valige **Pakutud muudatused**, et avada leht **Pakutud muudatused** ja vaadata oma muudatused üle.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="b9ec7-134">Valige **Töövoog \> Edasta**, et edastada muudatused töövoogu.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="b9ec7-135">Lehel on olekuks nüüd **Kinnitamise ootel muudatused**.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="b9ec7-136">Töövoog järgib rakenduses standardset töövooprotsessi.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="b9ec7-137">Kinnitaja suunatakse lehele **Klient**, kus ta saab lehel **Pakutud muudatused** tehtud muudatused üle vaadata ja seejärel valida töövoo kinnitamiseks **Töövoog \> Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-137">The approver is directed to the **Customer** page where the changes can be reviewed on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="b9ec7-138">Kui kõik kinnitamised on lõpule viidud, värskendatakse väljasid teie pakutud muudatustega.</span><span class="sxs-lookup"><span data-stu-id="b9ec7-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]