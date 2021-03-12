---
title: Hankija töövoog
description: Muutke hankija teavet ja kasutage töövoogu selle kinnitamiseks.
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 1fad41fa4fb3562ab94adde522d3899271c85467
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979160"
---
# <a name="vendor-workflow"></a><span data-ttu-id="e14fc-103">Hankija töövoog</span><span class="sxs-lookup"><span data-stu-id="e14fc-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e14fc-104">Hankija töövoogu kasutades saadetakse konkreetsetes väljades tehtud muudatused enne hankijale lisamist kinnitamiseks töövoogu.</span><span class="sxs-lookup"><span data-stu-id="e14fc-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="e14fc-105">Hankija töövoo seadistamine</span><span class="sxs-lookup"><span data-stu-id="e14fc-105">Set up the vendor workflow</span></span>

<span data-ttu-id="e14fc-106">Enne kui saate töövoo funktsiooni kasutada, peate selle lubama.</span><span class="sxs-lookup"><span data-stu-id="e14fc-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="e14fc-107">Avage **Ostureskontro \> Seadistus \> Ostureskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e14fc-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="e14fc-108">Määrake vahekaardil **Üldine** kiirkaardil **Hankija kinnitus** suvandi **Hankija kinnituste lubamine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e14fc-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="e14fc-109">Valige väljast **Andmeüksuse käitumine** käitumine, mida tuleks andmete importimisel kasutada.</span><span class="sxs-lookup"><span data-stu-id="e14fc-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="e14fc-110">**Luba muudatused ilma kinnitamata** – andmeüksus saab hankijakirjet uuendada ilma seda läbi töövoo töötlemata.</span><span class="sxs-lookup"><span data-stu-id="e14fc-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="e14fc-111">**Hülga muudatused** – hankijakirjet ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="e14fc-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="e14fc-112">Import nurjub väljade puhul, mis on töövoos lubatud.</span><span class="sxs-lookup"><span data-stu-id="e14fc-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="e14fc-113">**Loo muudatusettepanekud** – muudetakse kõiki välju peale töövoos lubatud väljade.</span><span class="sxs-lookup"><span data-stu-id="e14fc-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="e14fc-114">Nende väljade uued väärtused lisatakse hankijale pakutud muudatustena ja töövoog käivitatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="e14fc-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="e14fc-115">Valige hankija väljade loendist märkeruut **Luba** iga välja kohta, mis tuleb enne muudatuste tegemist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="e14fc-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="e14fc-116">Avage **Ostureskontro \> Seadistus \> Ostureskontro töövood**.</span><span class="sxs-lookup"><span data-stu-id="e14fc-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="e14fc-117">Valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e14fc-117">Select **New**.</span></span>
7. <span data-ttu-id="e14fc-118">Valige **Pakutud hankijamuudatuste töövoog**.</span><span class="sxs-lookup"><span data-stu-id="e14fc-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="e14fc-119">Seadistage töövoog nii, et see ühtiks teie kinnitusprotsessiga.</span><span class="sxs-lookup"><span data-stu-id="e14fc-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="e14fc-120">Töövoo kinnitamise element **Töövoo kinnitus pakutud hankijamuudatuse jaoks** rakendab muudatused hankijale.</span><span class="sxs-lookup"><span data-stu-id="e14fc-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="e14fc-121">Hankijateabe muutmine ja muudatuste kinnitamine töövoogu</span><span class="sxs-lookup"><span data-stu-id="e14fc-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="e14fc-122">Kui muudate välja, mis on töövoo jaoks lubatud, ilmub leht **Pakutud muudatused**.</span><span class="sxs-lookup"><span data-stu-id="e14fc-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="e14fc-123">Sellel lehel kuvatakse välja algväärtus ning uus väärtus, mille sisestasite.</span><span class="sxs-lookup"><span data-stu-id="e14fc-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="e14fc-124">Muudetud väljal taastatakse algne väärtus.</span><span class="sxs-lookup"><span data-stu-id="e14fc-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="e14fc-125">Olekuteade teavitab teid, et teie muudatusi ei kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="e14fc-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="e14fc-126">Iga kord kui muudate välja, mis on töövoos lubatud, lisatakse see väli loendisse lehel **Pakutud muudatused**.</span><span class="sxs-lookup"><span data-stu-id="e14fc-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="e14fc-127">Välja pakutud muudatuse tühistamiseks kasutage nuppu **Hülga** välja kõrval loendis.</span><span class="sxs-lookup"><span data-stu-id="e14fc-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="e14fc-128">Kõikide muudatuste hülgamiseks kasutage nuppu **Hülga kõik muudatused** lehe allosas.</span><span class="sxs-lookup"><span data-stu-id="e14fc-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="e14fc-129">Lehe sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="e14fc-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="e14fc-130">Kui teil on vähemalt üks pakutud muudatus, ilmuvad tegumiribale kaks täiendavat vahekaarti: **Pakutud muudatused** ja **Töövoog**.</span><span class="sxs-lookup"><span data-stu-id="e14fc-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="e14fc-131">Valige vahekaart **Pakutud muudatused**, et avada leht **Pakutud muudatused** ja muudatused üle vaadata.</span><span class="sxs-lookup"><span data-stu-id="e14fc-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="e14fc-132">Valige suvandid **Töövoog \> Edasta, et edastada muudatused töövoogu**.</span><span class="sxs-lookup"><span data-stu-id="e14fc-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="e14fc-133">Lehel on olekuks nüüd **Kinnitamise ootel muudatused**.</span><span class="sxs-lookup"><span data-stu-id="e14fc-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="e14fc-134">Töövoog järgib standardset töövooprotsessi.</span><span class="sxs-lookup"><span data-stu-id="e14fc-134">The workflow follows the standard workflow process.</span></span> <span data-ttu-id="e14fc-135">Kinnitaja suunatakse lehele **Hankija**, kus ta saab üle vaadata muudatused lehel **Pakutud muudatused** ja seejärel valida töövoo kinnitamiseks suvandid **Töövoog \> Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="e14fc-135">The approver is directed to the **Vendor** page where the changes can be reviewed on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="e14fc-136">Kui kõik kinnitamised on lõpule viidud, värskendatakse väljasid teie pakutud muudatustega.</span><span class="sxs-lookup"><span data-stu-id="e14fc-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
