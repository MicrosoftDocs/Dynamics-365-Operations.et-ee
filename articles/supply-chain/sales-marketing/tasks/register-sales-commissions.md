---
title: Müügi komisjonitasude registreerimine
description: Selles teemas selgitatakse, kuidas arvutatakse ja registreeritakse müügi komisjonitasusid.
author: omulvad
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee75f3a0c9dea7a7c4a4f927651aaab1d6bdb5c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836370"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="95d30-103">Müügi komisjonitasude registreerimine</span><span class="sxs-lookup"><span data-stu-id="95d30-103">Register sales commissions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="95d30-104">Selles teemas selgitatakse, kuidas arvutatakse ja registreeritakse müügi komisjonitasusid.</span><span class="sxs-lookup"><span data-stu-id="95d30-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="95d30-105">Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.</span><span class="sxs-lookup"><span data-stu-id="95d30-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="95d30-106">Enne selle juhendi avamist käivitage juhend „Müügi komisjonitasu reeglite seadistamine” veendumaks, et teil on kõik vajalikud komisjonitasu arvutused seadistatud.</span><span class="sxs-lookup"><span data-stu-id="95d30-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="95d30-107">Märkige üles komisjonitasu töötlemiseks valitud kliendi ja kauba koodid ning kasutage neid, kui teil palutakse selles juhendis luua müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="95d30-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="95d30-108">Müügiisikule komisjonitasu kvalifitseeriva müügitellimuse arveldamine</span><span class="sxs-lookup"><span data-stu-id="95d30-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="95d30-109">Avage navigeerimispaanil **Moodulid > Müük ja turundus > Müügitellimused > Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="95d30-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="95d30-110">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="95d30-110">Select **New**.</span></span>
3. <span data-ttu-id="95d30-111">Väljal **Kliendi konto** valige rippmenüüst soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="95d30-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="95d30-112">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="95d30-112">Select **OK**.</span></span>
5. <span data-ttu-id="95d30-113">Toimingupaanil valige **Suvandid**.</span><span class="sxs-lookup"><span data-stu-id="95d30-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="95d30-114">Valige **Muuda vaadet**.</span><span class="sxs-lookup"><span data-stu-id="95d30-114">Select **Change view**.</span></span>
7. <span data-ttu-id="95d30-115">Valige **Päise vaade**.</span><span class="sxs-lookup"><span data-stu-id="95d30-115">Select **Header view**.</span></span>
8. <span data-ttu-id="95d30-116">Laiendage jaotist **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="95d30-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="95d30-117">Väärtus väljal **Müügigrupp** esindab rühma, millele on määratud üks või enam müügiesindajat.</span><span class="sxs-lookup"><span data-stu-id="95d30-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="95d30-118">Grupis olevad inimesed on need, kes saavad tellimuse arveldamisel komisjonitasu eelmääratletud määrade ja jaotuse järgi.</span><span class="sxs-lookup"><span data-stu-id="95d30-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="95d30-119">Väärtus kopeeritakse kliendikaardilt, kuid seda saab soovi korral muuta.</span><span class="sxs-lookup"><span data-stu-id="95d30-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="95d30-120">Müügigrupp kopeeritakse ka müügitellimuse reale.</span><span class="sxs-lookup"><span data-stu-id="95d30-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="95d30-121">Saate seda muuta, nii et see võib päise ja/või ridade vahel erineda.</span><span class="sxs-lookup"><span data-stu-id="95d30-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="95d30-122">Väärtus väljal **Komisjonitasu grupp** esindab rühma, mille olete loonud ühe või enama kliendiga, eesmärgiga jälgida komisjonitasusid.</span><span class="sxs-lookup"><span data-stu-id="95d30-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="95d30-123">Väärtus kopeeritakse kliendikaardilt, kuid seda saab soovi korral muuta.</span><span class="sxs-lookup"><span data-stu-id="95d30-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="95d30-124">Toimingupaanil valige **Suvandid**.</span><span class="sxs-lookup"><span data-stu-id="95d30-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="95d30-125">Valige **Muuda vaadet**.</span><span class="sxs-lookup"><span data-stu-id="95d30-125">Select **Change view**.</span></span>
11. <span data-ttu-id="95d30-126">Valige **Reavaade**.</span><span class="sxs-lookup"><span data-stu-id="95d30-126">Select **Line view**.</span></span>
12. <span data-ttu-id="95d30-127">Välja **Kaubakood** rippmenüüst valige kaup, millele olete seadistanud komisjonitasud.</span><span class="sxs-lookup"><span data-stu-id="95d30-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="95d30-128">Sisestage arv väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="95d30-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="95d30-129">Märkige üles rea netosumma.</span><span class="sxs-lookup"><span data-stu-id="95d30-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="95d30-130">See tähistab müügitulu, mis siintoodud näites on komisjonitasu arvutamise aluseks.</span><span class="sxs-lookup"><span data-stu-id="95d30-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="95d30-131">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="95d30-131">Select **Save**.</span></span>
15. <span data-ttu-id="95d30-132">Toimingupaanil valige **Arve**.</span><span class="sxs-lookup"><span data-stu-id="95d30-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="95d30-133">Valige **Arve**.</span><span class="sxs-lookup"><span data-stu-id="95d30-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="95d30-134">Laiendage jaotist **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="95d30-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="95d30-135">Valige väljal **Kogus** suvand **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="95d30-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="95d30-136">Valige väärtus **Jah** väljal **Sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="95d30-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="95d30-137">Valige **OK** seejärel valige järgmisel paanil **OK**.</span><span class="sxs-lookup"><span data-stu-id="95d30-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="95d30-138">Kande sisestamiseks võib kuluda ligikaudu minut.</span><span class="sxs-lookup"><span data-stu-id="95d30-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="95d30-139">Oodake, kuni töötlemine on lõpule viidud, ja ärge lehte sulgege.</span><span class="sxs-lookup"><span data-stu-id="95d30-139">Allow the processing to complete and don't close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="95d30-140">Registreeritud müügi komisjonitasude ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="95d30-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="95d30-141">Toimingupaanil valige **Arve** seejärel valige uuesti **Arve**.</span><span class="sxs-lookup"><span data-stu-id="95d30-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="95d30-142">Toimingupaanil valige **Arve** seejärel valige **Komisjonitasude kanded**.</span><span class="sxs-lookup"><span data-stu-id="95d30-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="95d30-143">Vahekaardil **Ülevaade** kuvatakse read, mis esindavad müügiesindajatele makstavate komisjonitasude summasid, kes on seotud müügitellimusega, mille kohta on arve esitatud.</span><span class="sxs-lookup"><span data-stu-id="95d30-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="95d30-144">Vaadakem üksikasjad üle.</span><span class="sxs-lookup"><span data-stu-id="95d30-144">Let's review the details.</span></span>  
    - <span data-ttu-id="95d30-145">Kui kasutasite juhendit "Müügi komisjonitasude reeglite seadistamine", et seadistada rühm **Komisjonitasude müük**, on kaks müügiisikut, kes saavad müügi komisjonitasu ja komisjonitasu jagatakse nende vahel võrdselt.</span><span class="sxs-lookup"><span data-stu-id="95d30-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="95d30-146">Selle näite puhul arvutatakse komisjonitasu kogusumma protsendina müügitulust (tellimuserea netosummast).</span><span class="sxs-lookup"><span data-stu-id="95d30-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="95d30-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="95d30-147">Close the page.</span></span>
4. <span data-ttu-id="95d30-148">Valige **Kanne**.</span><span class="sxs-lookup"><span data-stu-id="95d30-148">Select **Voucher**.</span></span> <span data-ttu-id="95d30-149">Saate üle vaadata komisjonitasu summade kandeid, mis on sisestatud eelmääratletud komisjonitasu kulukontodele ja komisjonitasu ostureskontrotele.</span><span class="sxs-lookup"><span data-stu-id="95d30-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]