---
title: Veebitellimuse ja asünkroonse klienditellimuse kannete redigeerimine ning auditeerimine
description: Selles teemas kirjeldatakse, kuidas Microsoft Dynamics 365 Commerce'is veebitellimuse ja asünkroonse klienditellimuse kandeid redigeerida ning auditeerida.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9f2db25c8897662baa177752d0c5fc4ac6178a4
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458884"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="01264-103">Veebitellimuse ja asünkroonse klienditellimuse kannete redigeerimine ning auditeerimine</span><span class="sxs-lookup"><span data-stu-id="01264-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01264-104">Selles teemas kirjeldatakse, kuidas Microsoft Dynamics 365 Commerce'is veebitellimuse ja asünkroonse klienditellimuse kandeid redigeerida ning auditeerida.</span><span class="sxs-lookup"><span data-stu-id="01264-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="01264-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="01264-105">Overview</span></span>

<span data-ttu-id="01264-106">Commerce'i versioonide 10.0.5 ja 10.0.6 vahel lisati võimalus redigeerida selvehulgimüügikandeid (nt müük ja tagastused) ning kassahalduskandeid (nt sularaha sissemakse ja maksevahendi eemaldamine).</span><span class="sxs-lookup"><span data-stu-id="01264-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="01264-107">Commerce'i versioonis 10.0.7 lisati võimalus redigeerida veebitellimuse kandeid ja asünkroonse klienditellimuse kandeid.</span><span class="sxs-lookup"><span data-stu-id="01264-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="01264-108">Tellimuse kannete redigeerimine ja auditeerimine</span><span class="sxs-lookup"><span data-stu-id="01264-108">Edit and audit order transactions</span></span>

<span data-ttu-id="01264-109">Commerce'i peakontoris tellimuse kannete redigeerimiseks ja auditeerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="01264-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="01264-110">Installige [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span><span class="sxs-lookup"><span data-stu-id="01264-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="01264-111">Sisestage ootelolekukood lehe **Jaemüügi parameetrid** vahekaardi **Klienditellimused** kiirkaardi **Tellimus** lahtrisse **Tellimuse sünkroonimise tõrgete ootelolekukood**.</span><span class="sxs-lookup"><span data-stu-id="01264-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="01264-112">Avage tööruum **Kaupluse finantsandmed**.</span><span class="sxs-lookup"><span data-stu-id="01264-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="01264-113">Paanid **Veebitellimuse sünkroonimise tõrked** ja **Klienditellimuse sünkroonimise tõrked** pakuvad jaemüügikande lehe eelfiltreeritud vaadet.</span><span class="sxs-lookup"><span data-stu-id="01264-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="01264-114">Mõlemal paanil on kuvatud kandekirjed, mille sünkroonimine nurjus asjaomase tellimusetüübi korral.</span><span class="sxs-lookup"><span data-stu-id="01264-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="01264-115">Avage kas leht **Veebitellimuse sünkroonimise tõrked** või leht **Klienditellimuse sünkroonimise tõrked**.</span><span class="sxs-lookup"><span data-stu-id="01264-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="01264-116">Valige kirje sünkroonimistõrke üksikasjade vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="01264-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="01264-117">Kiirkaardil **Sünkroonimise olek** on järgmised tõrkeüksikasjad.</span><span class="sxs-lookup"><span data-stu-id="01264-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="01264-118">Ootel tellimuse olek</span><span class="sxs-lookup"><span data-stu-id="01264-118">Pending order status</span></span>
    - <span data-ttu-id="01264-119">Tellimuse tõrke üksikasjad</span><span class="sxs-lookup"><span data-stu-id="01264-119">Order error details</span></span>
    - <span data-ttu-id="01264-120">Muutmise kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="01264-120">Modified date and time</span></span>
    - <span data-ttu-id="01264-121">Uuesti proovimiste arv</span><span class="sxs-lookup"><span data-stu-id="01264-121">Retry count</span></span>

1. <span data-ttu-id="01264-122">Kui tõrkeüksikasjade järgi tuleb kirje parandada, valige **Office'i lisandmoodul** ja seejärel **Redigeeri valitud kannet**.</span><span class="sxs-lookup"><span data-stu-id="01264-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="01264-123">Avatakse Exceli fail, milles on valitud kande üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="01264-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="01264-124">Kui redigeeritav kanne on veebitellimuse kanne, sisaldab Exceli fail järgmisi töölehti.</span><span class="sxs-lookup"><span data-stu-id="01264-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="01264-125">**Kanne** – sellel töölehel on kande päiseüksikasjad.</span><span class="sxs-lookup"><span data-stu-id="01264-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="01264-126">**Müügikanne** – sellel töölehel on kande reaüksikasjad.</span><span class="sxs-lookup"><span data-stu-id="01264-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="01264-127">**Maksekanded** – sellel töölehel on kande makseridade üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="01264-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="01264-128">**Allahindluse kanded** – sellel töölehel on kande allahindlusega seotud üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="01264-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="01264-129">**Maksukanded** – sellel töölehel on kande maksudega seotud üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="01264-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="01264-130">**Tasukanded** – sellel töölehel on kande tasudega seotud andmed.</span><span class="sxs-lookup"><span data-stu-id="01264-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="01264-131">Kui redigeeritav kanne on asünkroonne klienditellimuse kanne, sisaldab Exceli fail järgmisi töölehti.</span><span class="sxs-lookup"><span data-stu-id="01264-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="01264-132">**Read** – sellel töölehel on kande päise- ja reaüksikasjad.</span><span class="sxs-lookup"><span data-stu-id="01264-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="01264-133">**Maksed** – sellel töölehel on kande makseridade üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="01264-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="01264-134">**Allahindlused** – sellel töölehel on kande allahindlusega seotud üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="01264-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="01264-135">**Maksud** – sellel töölehel on kande maksudega seotud üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="01264-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="01264-136">**Tasud** – sellel töölehel on kande tasudega seotud andmed.</span><span class="sxs-lookup"><span data-stu-id="01264-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="01264-137">Sisestage Exceli failis väljale **Ootel tellimuse olek** tekst **Redigeerimine** ja seejärel avaldage muudatus.</span><span class="sxs-lookup"><span data-stu-id="01264-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="01264-138">Sel viisil ei jäta pakktöötlusrežiimi käigus käitatav töö **Tellimuse sünkroonimine** seda kirjet töötluse ajal vahele.</span><span class="sxs-lookup"><span data-stu-id="01264-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="01264-139">Muutke Exceli failis asjakohaseid välju ja seejärel laadige andmed uuesti üles Commerce'i peakontorisse, kasutades Dynamics Exceli lisandmooduli avaldamisfunktsiooni.</span><span class="sxs-lookup"><span data-stu-id="01264-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="01264-140">Pärast andmete avaldamist kajastatakse muudatused süsteemis.</span><span class="sxs-lookup"><span data-stu-id="01264-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="01264-141">Avaldamise ajal ei üritata ühtegi kasutajate tehtud muudatust kinnitada.</span><span class="sxs-lookup"><span data-stu-id="01264-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="01264-142">Muudatuste täieliku kontrolljälje vaatamiseks valige päises **Jaemüügikanne** (päisetaseme muudatuste nägemiseks) ning asjakohase kande lehe asjakohases jaotises ja kirjes suvand **Kuva kontrolljälg**.</span><span class="sxs-lookup"><span data-stu-id="01264-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="01264-143">Näiteks kuvatakse kõik müügiridadega seotud muudatused lehel **Müügikanded** ja kõik maksetega seotud muudatused lehel **Maksekanded**.</span><span class="sxs-lookup"><span data-stu-id="01264-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="01264-144">Muudatuste korral säilitatakse järgmised auditiüksikasjad.</span><span class="sxs-lookup"><span data-stu-id="01264-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="01264-145">Muutmise kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="01264-145">Modified date and time</span></span>
    - <span data-ttu-id="01264-146">Väli</span><span class="sxs-lookup"><span data-stu-id="01264-146">Field</span></span>
    - <span data-ttu-id="01264-147">Varasem väärtus</span><span class="sxs-lookup"><span data-stu-id="01264-147">Old value</span></span>
    - <span data-ttu-id="01264-148">Uus väärtus</span><span class="sxs-lookup"><span data-stu-id="01264-148">New value</span></span>
    - <span data-ttu-id="01264-149">Muutja</span><span class="sxs-lookup"><span data-stu-id="01264-149">Modified by</span></span>

1. <span data-ttu-id="01264-150">Pärast muudatuste tegemist ja avaldamist valige **Sünkrooni tellimus**, et sünkroonimisprotsess kohe käivitada.</span><span class="sxs-lookup"><span data-stu-id="01264-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="01264-151">Teise võimalusena võite lasta pakktöötlusrežiimis käitataval sünkroonimisprotsessil kannet töödelda.</span><span class="sxs-lookup"><span data-stu-id="01264-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="01264-152">Vaikimisi pannakse tellimused pärast nende edukat sünkroonimist ootele ootelolekukoodi põhjal, mis on määratletud Commerce'i parameetrites.</span><span class="sxs-lookup"><span data-stu-id="01264-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="01264-153">Tellimuste ootelolek tuleb eemaldada, enne kui tellimusi saab täitmise või muude toimingute jaoks edasi töödelda.</span><span class="sxs-lookup"><span data-stu-id="01264-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01264-154">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="01264-154">Additional resources</span></span>

[<span data-ttu-id="01264-155">Selvehulgimüügi- ja kassahalduskannete redigeerimine ning auditeerimine</span><span class="sxs-lookup"><span data-stu-id="01264-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="01264-156">Jaemüügikannete finantsdimensioonide redigeerimine</span><span class="sxs-lookup"><span data-stu-id="01264-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="01264-157">Exceli töövihiku loomine jaemüügikannete redigeerimiseks</span><span class="sxs-lookup"><span data-stu-id="01264-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="01264-158">Väljade lisamine Exceli töövihikusse jaemüügikannete redigeerimiseks</span><span class="sxs-lookup"><span data-stu-id="01264-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
