---
title: Tarbimise registreerimine
description: Selles teemas tutvustatakse, kuidas varahalduses tarbimist registreerida.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderJournal, EntAssetWorkOrderAddSparePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 61aea0261a62df9c029b429f33ba7b357621988b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259982"
---
# <a name="register-consumption"></a><span data-ttu-id="f4634-103">Tarbimise registreerimine</span><span class="sxs-lookup"><span data-stu-id="f4634-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f4634-104">Kui hooldustöö on töökäsus lõpetatud, on järgmine etapp tarbimiste registreeringute tegemine ja töölehtedele sisestamine.</span><span class="sxs-lookup"><span data-stu-id="f4634-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="f4634-105">Saate registreeringuid teha järgmiste tarbimise tüüpide kohta: tunnid, kaubad ja kulud.</span><span class="sxs-lookup"><span data-stu-id="f4634-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="f4634-106">Eri tarbimise tüübid on registreeritud ja sisestatud lehele **Töökäsu töölehed**.</span><span class="sxs-lookup"><span data-stu-id="f4634-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="f4634-107">Töölehe seadistust funktsioonis **Varahaldus** kasutatakse eraldi töölehtede loomiseks ja sisestamiseks tundide, kaupade ja kulude jaoks moodulis **Projektihaldus ja raamatupidamine**.</span><span class="sxs-lookup"><span data-stu-id="f4634-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="f4634-108">Mõnel juhul saate töökäsule prognoosi ridu lisada või neid kustutada.</span><span class="sxs-lookup"><span data-stu-id="f4634-108">In some cases, you may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="f4634-109">Töökäsu töötsükli oleku seadistus, seotud projektitüüp ja seotud projektitüübi oleku reeglid määravad ära, kas saate töölehele ridu lisada või redigeerida.</span><span class="sxs-lookup"><span data-stu-id="f4634-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="f4634-110">Lisateavet töökäsu elutsükli olekute ja seotud projekti etappide kohta vt teemast [Prognoosid, töökäsud ja projektid](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="f4634-110">Read more about work order lifecycle states and related project stages in [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="f4634-111">Töökäsu töötsükli olekule on võimalik seadistada automaatne töölehtede sisestamine.</span><span class="sxs-lookup"><span data-stu-id="f4634-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="f4634-112">Lisateabe saamiseks vaadake teemat [Töökäsu töötsükli olekud](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="f4634-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="f4634-113">Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik Töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="f4634-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f4634-114">Valige töökäsk ja klõpsake valikut **Töölehed**.</span><span class="sxs-lookup"><span data-stu-id="f4634-114">Select the work order, and click **Journals**.</span></span>

3. <span data-ttu-id="f4634-115">Klõpsake **Kopeeri prognoosist**, et edastada mis tahes prognoosi read, mis võivad olla seotud töökäsuga.</span><span class="sxs-lookup"><span data-stu-id="f4634-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="f4634-116">Saate valida milliseid tarbimise ridu soovite edastada.</span><span class="sxs-lookup"><span data-stu-id="f4634-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="f4634-117">Vajaduse korral saate lisada tarbimise ridu seotud kiirkaardil, kui klõpsate **Lisa rida** ja täidate rea andmetega.</span><span class="sxs-lookup"><span data-stu-id="f4634-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="f4634-118">Töölehe ridade valideerimiseks enne sisestamist klõpsake **Valideeri töölehed**.</span><span class="sxs-lookup"><span data-stu-id="f4634-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="f4634-119">Töölehe ridade sisestamiseks klõpsake **Sisestage töölehed**.</span><span class="sxs-lookup"><span data-stu-id="f4634-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="f4634-120">Pärast tarbimise töölehtede sisestamist saate värskendada töökäsu töötsükli olekut.</span><span class="sxs-lookup"><span data-stu-id="f4634-120">After you've posted the consumption journals, you can update the work order lifecycle state.</span></span> <span data-ttu-id="f4634-121">Näiteks selleks, et näidata, et töökäsk on lõpule viidud, saate määrata töötsükli olekuks „Lõpetatud“.</span><span class="sxs-lookup"><span data-stu-id="f4634-121">For example, to indicate that the work order has been completed, you can update the lifecycle state to "Ended".</span></span>

    - <span data-ttu-id="f4634-122">Lehe **Töökäsu töölehed** ülaosa väljal **Kuva** valige milliseid töölehe ridu soovite näha: **Kõik**, **Sisestamata** või **Sisestatud**.</span><span class="sxs-lookup"><span data-stu-id="f4634-122">In the **Show** field at the top of the **Work order journals** page, select which journal lines you want to see: **All**, **Not posted**, or **Posted**.</span></span> <span data-ttu-id="f4634-123">Sisestatud töölehtedel on märgitud märkeruut **Sisestatud**.</span><span class="sxs-lookup"><span data-stu-id="f4634-123">Posted journals have a check mark in the **Posted** check box.</span></span>  
    - <span data-ttu-id="f4634-124">Kui kaubaread on loodud töökäsu töölehel, edastatakse kaubaga seotud tootedimensioonid ja jälgimisdimensioonid automaatselt töölehe reale.</span><span class="sxs-lookup"><span data-stu-id="f4634-124">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="f4634-125">Alloleval kuvatõmmisel kuvatakse näidet tunni ja kauba registreeringutest töökäsul suvandis **Töökäsu töölehed**.</span><span class="sxs-lookup"><span data-stu-id="f4634-125">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Joonis 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="f4634-127">Töökäskude tundide eraldamine mitme töökäsu tööga</span><span class="sxs-lookup"><span data-stu-id="f4634-127">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="f4634-128">Kui töökäsk sisaldab mitut töökäsu tööd, saate registreerida töötunnid, kui kasutate funktsiooni **Eralda tunnid**, mis tähendab, et ühe tunni registreerimise rea võib võrdselt jagada iga töökäsu töö jaoks.</span><span class="sxs-lookup"><span data-stu-id="f4634-128">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="f4634-129">Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik Töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="f4634-129">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f4634-130">Valige töökäsk ja klõpsake **Töölehed**.</span><span class="sxs-lookup"><span data-stu-id="f4634-130">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="f4634-131">Valige loendist tunni registreerimise rida, mida soovite eraldada ja klõpsake **Eralda tunnid**.</span><span class="sxs-lookup"><span data-stu-id="f4634-131">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="f4634-132">Dialoogis **Eralda tunnid töökäsu hooldustöödel** kuvatakse väljal **Töötaja** automaatselt selle töötaja nime, kes on sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="f4634-132">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="f4634-133">Vajaduse korral saate valida teise töötaja.</span><span class="sxs-lookup"><span data-stu-id="f4634-133">If required, you can select another worker.</span></span>

5. <span data-ttu-id="f4634-134">Valige tunni registreerimise jaoks kategooria väljal **Kategooria**.</span><span class="sxs-lookup"><span data-stu-id="f4634-134">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="f4634-135">Sisestage väljale **Tunnid** eraldatavad töötunnid.</span><span class="sxs-lookup"><span data-stu-id="f4634-135">Insert number of work hours to be split in the **Hours** field.</span></span>

    ![Joonis 2](media/02-consumption.png)

7. <span data-ttu-id="f4634-137">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4634-137">Click **OK**.</span></span>

<span data-ttu-id="f4634-138">*Näide*: alloleval kuvatõmmisel kuvatakse töökäsu töölehe read, mis sisaldavad kolme töökäsu tööd.</span><span class="sxs-lookup"><span data-stu-id="f4634-138">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="f4634-139">Esimene rida, mis sisaldab kolme töötundi, on eraldatud ja üks töötund on registreeritud iga töökäsu töö kohta.</span><span class="sxs-lookup"><span data-stu-id="f4634-139">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="f4634-140">Pärast kolme tunni registreerimise rea loomist saate valida, mida teha algse tunni registreerimise reaga (näite esimene rida).</span><span class="sxs-lookup"><span data-stu-id="f4634-140">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="f4634-141">Saate selle jätta selliseks nagu ta on või selle kustutada.</span><span class="sxs-lookup"><span data-stu-id="f4634-141">You can keep it as is or delete it.</span></span> 

![Joonis 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="f4634-143">Tarbimise registreerimiste finantsdimensioonid</span><span class="sxs-lookup"><span data-stu-id="f4634-143">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="f4634-144">Kui teete tarbimise registreeringuid, lisatakse eri registreerimise tüüpidega seotud finantsdimensioonid registreeringutele kindlas järjekorras.</span><span class="sxs-lookup"><span data-stu-id="f4634-144">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

- <span data-ttu-id="f4634-145">*Töö ja kulu registreeringud*: esimesena lisatakse finantsdimensioonid töölehe päisest, kui neid on.</span><span class="sxs-lookup"><span data-stu-id="f4634-145">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="f4634-146">Järgmisena lisatakse seotud töökäsu projekti finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="f4634-146">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="f4634-147">Viimasena lisatakse ressursi (töötaja) finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="f4634-147">Finally, financial dimensions from the resource (worker) are added.</span></span>

- <span data-ttu-id="f4634-148">*Kauba registreeringud*: esimesena lisatakse finantsdimensioonid töölehe päisest, kui neid on.</span><span class="sxs-lookup"><span data-stu-id="f4634-148">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="f4634-149">Seejärel lisatakse seotud töökäsu projekti finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="f4634-149">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="f4634-150">Järgmisena lisatakse koha finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="f4634-150">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="f4634-151">Viimasena lisatakse kauba finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="f4634-151">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="f4634-152">Kõigi kolme registreerimise tüübi puhul on finantsdimensioonide kombinatsioon valideeritud ja kehtetud kombinatsioonid jäetakse tühjaks.</span><span class="sxs-lookup"><span data-stu-id="f4634-152">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="f4634-153">See on standardne seadistus koos teiste lahenduse Finance and Operations rakendustega.</span><span class="sxs-lookup"><span data-stu-id="f4634-153">This is standard setup with other Finance and Operations apps.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]