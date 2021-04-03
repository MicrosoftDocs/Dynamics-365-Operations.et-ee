---
title: Ostulepingu loomine
description: Selles teemas jagatakse juhiseid, kuidas luua ostulepingut.
author: RichardLuan
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fb3d397b277429954ef91e13445189fe21560b6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237199"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="6b088-103">Ostulepingu loomine</span><span class="sxs-lookup"><span data-stu-id="6b088-103">Create a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6b088-104">Selles teemas jagatakse juhiseid, kuidas luua ostulepingut.</span><span class="sxs-lookup"><span data-stu-id="6b088-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="6b088-105">Seda teeb tavaliselt ostujuht.</span><span class="sxs-lookup"><span data-stu-id="6b088-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="6b088-106">Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="6b088-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="6b088-107">Enne alustamist peate seadistama ostulepingu klassifikatsioonid.</span><span class="sxs-lookup"><span data-stu-id="6b088-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="6b088-108">Kui olete lepingu loonud, saate seda kasutada ostutellimuse loomisel ning sellega kopeeritakse ostulepingu tingimused lepinguga seotud tellimuse päisesse ja kõigile ridadele.</span><span class="sxs-lookup"><span data-stu-id="6b088-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="6b088-109">Uue ostulepingu loomine</span><span class="sxs-lookup"><span data-stu-id="6b088-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="6b088-110">Avage **Navigeerimispaan > Moodulid > Hanked > Ostulepingud > Ostulepingud**.</span><span class="sxs-lookup"><span data-stu-id="6b088-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="6b088-111">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6b088-111">Click **New**.</span></span>
3. <span data-ttu-id="6b088-112">Väljal **Hankija konto** valige rippmenüü ja valige soovitud kirje rida.</span><span class="sxs-lookup"><span data-stu-id="6b088-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="6b088-113">Väljal **Ostulepingu klassifikatsioon** valige rippmenüü ja valige soovitud kirje rida.</span><span class="sxs-lookup"><span data-stu-id="6b088-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="6b088-114">Suurendage vahekaarti **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="6b088-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="6b088-115">Väljale **Aegumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="6b088-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="6b088-116">Aegumiskuupäev kehtib vaikimisi kõigile kohustuseridadele ja määratleb, kui kaua konkreetne kohustus kehtib.</span><span class="sxs-lookup"><span data-stu-id="6b088-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="6b088-117">Väljale **Dokumendi pealkiri** sisestage oma ostulepingu nimi.</span><span class="sxs-lookup"><span data-stu-id="6b088-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="6b088-118">Jätke välja **Vaikekohustus** seadistuseks **Toote koguse kohustus** (või muutke see, kui see pole nii seadistatud).</span><span class="sxs-lookup"><span data-stu-id="6b088-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it's not set to this).</span></span>  
    - <span data-ttu-id="6b088-119">Vaikekohustuse väärtus määratleb teie suvandid lepingu ridadel.</span><span class="sxs-lookup"><span data-stu-id="6b088-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="6b088-120">Kui vajate lepingu ridade loomisel uut kohustuse tüüpi, peate muutma päises vaikekohustust.</span><span class="sxs-lookup"><span data-stu-id="6b088-120">If you need a new commitment type when you're creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="6b088-121">Kohustusi on 4 tüüpi: **Toote koguse kohustus** - konkreetse tootekoguse jaoks; **Toote väärtuse kohustus** - konkreetse toote valuuta summa jaoks; **Toote kategooria väärtuse kohustus** - konkreetse toote valuuta summa jaoks hankekategoorias, kus summa võib olla kataloogikauba või kataloogivälise kauba jaoks; **Väärtuse kohustus** - konkreetse valuuta summa jaoks, mille võib täita mis tahes toode või hankekategooria.</span><span class="sxs-lookup"><span data-stu-id="6b088-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="6b088-122">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b088-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="6b088-123">Kommentaari lisamine</span><span class="sxs-lookup"><span data-stu-id="6b088-123">Add a commitment</span></span>
1. <span data-ttu-id="6b088-124">Valige **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="6b088-124">Select **Add line**.</span></span>
2. <span data-ttu-id="6b088-125">Väljal **Kaubakood** valige rippmenüüst soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6b088-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="6b088-126">Sisestage arv väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="6b088-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="6b088-127">See on lõplik kogus, mille ostmises oma hankijalt olete kokku leppinud.</span><span class="sxs-lookup"><span data-stu-id="6b088-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="6b088-128">Sisestage arv väljale **Ühiku hind**.</span><span class="sxs-lookup"><span data-stu-id="6b088-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="6b088-129">Laiendage jaotist **Rea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="6b088-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="6b088-130">Määrake suvandi **Maksimaalne on jõustatud** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="6b088-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="6b088-131">Suvand **Maksimaalne on jõustatud** piirab kohustuse kasutust.</span><span class="sxs-lookup"><span data-stu-id="6b088-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="6b088-132">Saate osta ainult kuni rea väljal **Kogus** määratud koguseni.</span><span class="sxs-lookup"><span data-stu-id="6b088-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="6b088-133">Päise tingimuste lisamine</span><span class="sxs-lookup"><span data-stu-id="6b088-133">Add header conditions</span></span>
1. <span data-ttu-id="6b088-134">Toimingupaanil valige **Suvandid**.</span><span class="sxs-lookup"><span data-stu-id="6b088-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="6b088-135">Valige **Muuda vaadet**.</span><span class="sxs-lookup"><span data-stu-id="6b088-135">Select **Change view**.</span></span>
3. <span data-ttu-id="6b088-136">Valige **Päise vaade**.</span><span class="sxs-lookup"><span data-stu-id="6b088-136">Select **Header view**.</span></span>
4. <span data-ttu-id="6b088-137">Laiendage jaotist **Tingimused**.</span><span class="sxs-lookup"><span data-stu-id="6b088-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="6b088-138">Väljal **Makseviis** valige rippmenüüst soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6b088-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="6b088-139">Maksetingimused hankija kontolt kuvatakse siin vaikimisi.</span><span class="sxs-lookup"><span data-stu-id="6b088-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="6b088-140">Väljal **Tarneviis** valige rippmenüüst soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6b088-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="6b088-141">Väljal **Tarnetingimused** valige rippmenüü nupp, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="6b088-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="6b088-142">Leppe kinnitamine ja aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="6b088-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="6b088-143">Toimingupaanil valige **Ostuleping**.</span><span class="sxs-lookup"><span data-stu-id="6b088-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="6b088-144">Valige **Kinnitus**.</span><span class="sxs-lookup"><span data-stu-id="6b088-144">Select **Confirmation**.</span></span> <span data-ttu-id="6b088-145">Määrake suvandi **Märgi leping kehtivaks** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="6b088-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="6b088-146">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b088-146">Select **OK**.</span></span>
4. <span data-ttu-id="6b088-147">Toimingupaanil valige **Ostuleping**.</span><span class="sxs-lookup"><span data-stu-id="6b088-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="6b088-148">Valige **Ostulepingu kinnitused**.</span><span class="sxs-lookup"><span data-stu-id="6b088-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="6b088-149">Suvand **Eelvaade/prindi** lubab teil luua ostulepingu jaoks dokumendi, mille saate seejärel printida või hankijale saata.</span><span class="sxs-lookup"><span data-stu-id="6b088-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="6b088-150">Lepingu hiljem muutmisel ja uuesti kinnitamisel kuvatakse siin mõlemad versioonid.</span><span class="sxs-lookup"><span data-stu-id="6b088-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="6b088-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6b088-151">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]