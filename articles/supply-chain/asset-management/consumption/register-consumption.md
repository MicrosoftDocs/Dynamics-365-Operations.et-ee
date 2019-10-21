---
title: Tarbimise registreerimine
description: Selles teemas tutvustatakse, kuidas varahalduses tarbimist registreerida.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 174c816c7a6442b07e4722c03045293b94c59153
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024656"
---
# <a name="register-consumption"></a><span data-ttu-id="77e98-103">Tarbimise registreerimine</span><span class="sxs-lookup"><span data-stu-id="77e98-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="77e98-104">Kui hooldustöö on töökäsus lõpetatud, on järgmine etapp tarbimiste registreeringute tegemine ja töölehtedele sisestamine.</span><span class="sxs-lookup"><span data-stu-id="77e98-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="77e98-105">Saate registreeringuid teha järgmiste tarbimise tüüpide kohta: tunnid, kaubad ja kulud.</span><span class="sxs-lookup"><span data-stu-id="77e98-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="77e98-106">Eri tarbimise tüübid on registreeritud ja sisestatud lehele **Töökäsu töölehed**.</span><span class="sxs-lookup"><span data-stu-id="77e98-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="77e98-107">Töölehe seadistust funktsioonis **Varahaldus** kasutatakse eraldi töölehtede loomiseks ja sisestamiseks tundide, kaupade ja kulude jaoks moodulis **Projektihaldus ja raamatupidamine**.</span><span class="sxs-lookup"><span data-stu-id="77e98-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="77e98-108">Saate töökäsule prognoosi ridu lisada või neid kustutada.</span><span class="sxs-lookup"><span data-stu-id="77e98-108">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="77e98-109">Töökäsu töötsükli oleku seadistus, seotud projektitüüp ja seotud projektitüübi oleku reeglid määravad ära, kas saate töölehele ridu lisada või redigeerida.</span><span class="sxs-lookup"><span data-stu-id="77e98-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="77e98-110">Lisateavet töökäsu töötsükli olekute ja seotud projekti etappide kohta lugege teemast [Projektihalduse ja raamatupidamisega integreerimine](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="77e98-110">Read more about work order lifecycle states and related project stages in [Integration to project management and accounting](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="77e98-111">Töökäsu töötsükli olekule on võimalik seadistada automaatne töölehtede sisestamine.</span><span class="sxs-lookup"><span data-stu-id="77e98-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="77e98-112">Lisateabe saamiseks vaadake teemat [Töökäsu töötsükli olekud](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="77e98-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="77e98-113">Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik Töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="77e98-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="77e98-114">Valige töökäsk ja klõpsake **Töölehed**.</span><span class="sxs-lookup"><span data-stu-id="77e98-114">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="77e98-115">Klõpsake **Kopeeri prognoosist**, et edastada mis tahes prognoosi read, mis võivad olla seotud töökäsuga.</span><span class="sxs-lookup"><span data-stu-id="77e98-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="77e98-116">Saate valida milliseid tarbimise ridu soovite edastada.</span><span class="sxs-lookup"><span data-stu-id="77e98-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="77e98-117">Vajaduse korral saate lisada tarbimise ridu seotud kiirkaardil, kui klõpsate **Lisa rida** ja täidate rea andmetega.</span><span class="sxs-lookup"><span data-stu-id="77e98-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="77e98-118">Töölehe ridade valideerimiseks enne sisestamist klõpsake **Valideeri töölehed**.</span><span class="sxs-lookup"><span data-stu-id="77e98-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="77e98-119">Töölehe ridade sisestamiseks klõpsake **Sisestage töölehed**.</span><span class="sxs-lookup"><span data-stu-id="77e98-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="77e98-120">Pärast tarbimise töölehtede sisestamist, saate värskendada töökäsu töötsükli olekut, näiteks olekule "Lõpetatud", mis näitab, et töökäsk on lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="77e98-120">After you've posted the consumption journals, you can update the work order lifecycle state, for example to "Ended", to indicate that the work order has been completed.</span></span>

- <span data-ttu-id="77e98-121">Lehe **Töökäsu töölehed** ülaosas asuval väljal **Kuva** valige milliseid töölehe ridu soovite näha: kõik, sisestamata või sisestatud.</span><span class="sxs-lookup"><span data-stu-id="77e98-121">In the **Show** field placed at the top of the **Work order journals** page, select which journal lines you want to see: All, Not posted, or Posted.</span></span> <span data-ttu-id="77e98-122">Sisestatud töölehtedel on märgitud märkeruut **Sisestatud**.</span><span class="sxs-lookup"><span data-stu-id="77e98-122">Posted journals have a check mark in the **Posted** check box.</span></span>  
- <span data-ttu-id="77e98-123">Kui kaubaread on loodud töökäsu töölehel, edastatakse kaubaga seotud tootedimensioonid ja jälgimisdimensioonid automaatselt töölehe reale.</span><span class="sxs-lookup"><span data-stu-id="77e98-123">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="77e98-124">Alloleval kuvatõmmisel kuvatakse näidet tunni ja kauba registreeringutest töökäsul suvandis **Töökäsu töölehed**.</span><span class="sxs-lookup"><span data-stu-id="77e98-124">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Joonis 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="77e98-126">Töökäskude tundide eraldamine mitme töökäsu tööga</span><span class="sxs-lookup"><span data-stu-id="77e98-126">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="77e98-127">Kui töökäsk sisaldab mitut töökäsu tööd, saate registreerida töötunnid, kui kasutate funktsiooni **Eralda tunnid**, mis tähendab, et ühe tunni registreerimise rea võib võrdselt jagada iga töökäsu töö jaoks.</span><span class="sxs-lookup"><span data-stu-id="77e98-127">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="77e98-128">Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik Töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="77e98-128">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="77e98-129">Valige töökäsk ja klõpsake **Töölehed**.</span><span class="sxs-lookup"><span data-stu-id="77e98-129">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="77e98-130">Valige loendist tunni registreerimise rida, mida soovite eraldada ja klõpsake **Eralda tunnid**.</span><span class="sxs-lookup"><span data-stu-id="77e98-130">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="77e98-131">Dialoogis **Eralda tunnid töökäsu hooldustöödel** kuvatakse väljal **Töötaja** automaatselt selle töötaja nime, kes on sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="77e98-131">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="77e98-132">Vajaduse korral saate valida teise töötaja.</span><span class="sxs-lookup"><span data-stu-id="77e98-132">If required, you can select another worker.</span></span>

5. <span data-ttu-id="77e98-133">Valige tunni registreerimise jaoks kategooria väljal **Kategooria**.</span><span class="sxs-lookup"><span data-stu-id="77e98-133">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="77e98-134">Sisestage väljale **Tunnid** eraldatavad töötunnid.</span><span class="sxs-lookup"><span data-stu-id="77e98-134">Insert number of work hours to be split in the **Hours** field.</span></span>

![Joonis 2](media/02-consumption.png)

7. <span data-ttu-id="77e98-136">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="77e98-136">Click **OK**.</span></span>

<span data-ttu-id="77e98-137">*Näide*: alloleval kuvatõmmisel kuvatakse töökäsu töölehe read, mis sisaldavad kolme töökäsu tööd.</span><span class="sxs-lookup"><span data-stu-id="77e98-137">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="77e98-138">Esimene rida, mis sisaldab kolme töötundi, on eraldatud ja üks töötund on registreeritud iga töökäsu töö kohta.</span><span class="sxs-lookup"><span data-stu-id="77e98-138">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="77e98-139">Pärast kolme tunni registreerimise rea loomist saate valida, mida teha algse tunni registreerimise reaga (näite esimene rida).</span><span class="sxs-lookup"><span data-stu-id="77e98-139">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="77e98-140">Saate selle jätta selliseks nagu ta on või selle kustutada.</span><span class="sxs-lookup"><span data-stu-id="77e98-140">You can keep it as is or delete it.</span></span> 

![Joonis 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="77e98-142">Tarbimise registreerimiste finantsdimensioonid</span><span class="sxs-lookup"><span data-stu-id="77e98-142">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="77e98-143">Kui teete tarbimise registreeringuid, lisatakse eri registreerimise tüüpidega seotud finantsdimensioonid registreeringutele kindlas järjekorras.</span><span class="sxs-lookup"><span data-stu-id="77e98-143">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

<span data-ttu-id="77e98-144">*Töö ja kulu registreeringud*: esimesena lisatakse finantsdimensioonid töölehe päisest, kui neid on.</span><span class="sxs-lookup"><span data-stu-id="77e98-144">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="77e98-145">Järgmisena lisatakse seotud töökäsu projekti finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="77e98-145">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="77e98-146">Viimasena lisatakse ressursi (töötaja) finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="77e98-146">Finally, financial dimensions from the resource (worker) are added.</span></span>

<span data-ttu-id="77e98-147">*Kauba registreeringud*: esimesena lisatakse finantsdimensioonid töölehe päisest, kui neid on.</span><span class="sxs-lookup"><span data-stu-id="77e98-147">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="77e98-148">Seejärel lisatakse seotud töökäsu projekti finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="77e98-148">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="77e98-149">Järgmisena lisatakse koha finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="77e98-149">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="77e98-150">Viimasena lisatakse kauba finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="77e98-150">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="77e98-151">Kõigi kolme registreerimise tüübi puhul on finantsdimensioonide kombinatsioon valideeritud ja kehtetud kombinatsioonid jäetakse tühjaks.</span><span class="sxs-lookup"><span data-stu-id="77e98-151">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="77e98-152">See on standardne seadistus Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="77e98-152">This is standard setup in Finance and Operations.</span></span>

