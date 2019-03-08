---
title: Jaemüügikanalite määratlemine ja haldamine
description: Selles teemas antakse ülevaade füüsilistele kaupluste (mida nimetatakse Microsoft Dynamics 365 for Retailis jaekauplusteks) seadistamise protsessist. See sisaldab teavet ülesannete kohta, mis tuleb lõpule viia enne ja pärast jaekaupluse seadistamist.
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 53ba6cdb2378ce9011c6e7e3ce4e67c789adb1e6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "318622"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="d1032-104">Jaemüügikanalite määratlemine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="d1032-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d1032-105">Selles teemas antakse ülevaade füüsilistele kaupluste (mida nimetatakse Microsoft Dynamics 365 for Retailis jaekauplusteks) seadistamise protsessist.</span><span class="sxs-lookup"><span data-stu-id="d1032-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="d1032-106">See sisaldab teavet ülesannete kohta, mis tuleb lõpule viia enne ja pärast jaekaupluse seadistamist.</span><span class="sxs-lookup"><span data-stu-id="d1032-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="d1032-107">Dynamics 365 for Retail toetab mitmeid jaemüügikanaleid, nagu võrgupoed, kõnekeskused ja traditsioonilised kauplused.</span><span class="sxs-lookup"><span data-stu-id="d1032-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="d1032-108">Traditsioonilist kauplust nimetatakse jaekaupluseks.</span><span class="sxs-lookup"><span data-stu-id="d1032-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="d1032-109">Igal kauplusel võivad olla oma makseviisid, hinnagrupid, kassaregistrid, tulu- ja kulukontod ning personal.</span><span class="sxs-lookup"><span data-stu-id="d1032-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="d1032-110">Enne kaupluse loomist tuleb seadistada kõik need elemendid.</span><span class="sxs-lookup"><span data-stu-id="d1032-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="d1032-111">Kui olete kaupluse loonud, saate määrata seal müüdavad tooted.</span><span class="sxs-lookup"><span data-stu-id="d1032-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="d1032-112">Saate kauplusele määrata ka töötajad, registrid ja kliendid.</span><span class="sxs-lookup"><span data-stu-id="d1032-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="d1032-113">Viimaks peate lisama uue kaupluse organisatsioonihierarhiasse.</span><span class="sxs-lookup"><span data-stu-id="d1032-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="d1032-114">Kaupluste seadistamine</span><span class="sxs-lookup"><span data-stu-id="d1032-114">Setting up retail stores</span></span>

<span data-ttu-id="d1032-115">Enne kui saate rakenduses Dynamics 365 for Retail kaupluse seadistada, peate täitma mõne eeltingimuseks oleva ülesande.</span><span class="sxs-lookup"><span data-stu-id="d1032-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="d1032-116">Seejärel saate luua kaupluse ja lisada üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="d1032-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="d1032-117">Eeltingimused </span><span class="sxs-lookup"><span data-stu-id="d1032-117">Prerequisites</span></span>

<span data-ttu-id="d1032-118">Enne kui saate kaupluse seadistada, peate tegema järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="d1032-118">You must complete the following tasks before you can set up a retail store:</span></span>

1. <span data-ttu-id="d1032-119">Saate konfigureerida organisatsiooni struktuuri ja seadistada organisatsiooni hierarhiad jaemüügisortimendi, täiendamise ja aruannete jaoks.</span><span class="sxs-lookup"><span data-stu-id="d1032-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="d1032-120">Saate seadistada kauplust kajastava lao.</span><span class="sxs-lookup"><span data-stu-id="d1032-120">Set up a warehouse that represents the retail store.</span></span>
3. <span data-ttu-id="d1032-121">Kaupluste, kaupluse väljavõtete ja väljavõttekannete numbriseeriate seadistamine.</span><span class="sxs-lookup"><span data-stu-id="d1032-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="d1032-122">Saate jaemüügi parameetreid konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="d1032-122">Configure parameters for Retail.</span></span>
5. <span data-ttu-id="d1032-123">Kaupluses aktsepteeritavate makseviiside seadistamine.</span><span class="sxs-lookup"><span data-stu-id="d1032-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="d1032-124">Jaemüügi kassaregistrites krediitkaardikannete töötlemiseks saate seadistada ka makseteenused.</span><span class="sxs-lookup"><span data-stu-id="d1032-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="d1032-125">Käibemaksugruppide seadistamine.</span><span class="sxs-lookup"><span data-stu-id="d1032-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="d1032-126">Jaemüügitoodete seadistamine.</span><span class="sxs-lookup"><span data-stu-id="d1032-126">Set up retail products.</span></span> <span data-ttu-id="d1032-127">Selle toimingu raames seadistate ka jaemüügihierarhiad, tootevariandid ja tootesortimendid.</span><span class="sxs-lookup"><span data-stu-id="d1032-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="d1032-128">Toote hinnagruppide seadistamine.</span><span class="sxs-lookup"><span data-stu-id="d1032-128">Set up product price groups.</span></span>
10. <span data-ttu-id="d1032-129">Jaemüügitoodete hinnakujunduse seadistamine.</span><span class="sxs-lookup"><span data-stu-id="d1032-129">Set up retail product pricing.</span></span> <span data-ttu-id="d1032-130">Selle toimingu raames seadistate ka hinnakorrektsioonid, allahindlused ja allahindluse perioodid.</span><span class="sxs-lookup"><span data-stu-id="d1032-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="d1032-131">Töötajate seadistamine.</span><span class="sxs-lookup"><span data-stu-id="d1032-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d1032-132">Peate määrama töötajatele ka vajalikud õigused, et nad saaksid sisse logida ja teha toiminguid, kasutades süsteemi Dynamics 365 for Retail for Retail POS.</span><span class="sxs-lookup"><span data-stu-id="d1032-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>

12. <span data-ttu-id="d1032-133">Kauplusele määratavate Retail POS-i profiilide konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="d1032-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="d1032-134">See toiming hõlmab mitmeid toiminguid, nagu registrite, ühenduseta profiilide ning kviitungivormingute ja -profiilide seadistamine.</span><span class="sxs-lookup"><span data-stu-id="d1032-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="d1032-135">Vaadake kõik eelduses nimetatud toimingud üle ja tehke ainult teid puudutavad toimingud.</span><span class="sxs-lookup"><span data-stu-id="d1032-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="d1032-136">Jaemüügikaupluse häälestus</span><span class="sxs-lookup"><span data-stu-id="d1032-136">Set up a retail store</span></span>

<span data-ttu-id="d1032-137">Kui eeltingimuseks olevad ülesanded on täidetud, täitke kaupluse üksikasjade seadistamiseks järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="d1032-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1. <span data-ttu-id="d1032-138">Jaemüügikaupluse loomine.</span><span class="sxs-lookup"><span data-stu-id="d1032-138">Create a retail store.</span></span>
2. <span data-ttu-id="d1032-139">Kauplusele käibemaksugrupi määramine.</span><span class="sxs-lookup"><span data-stu-id="d1032-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="d1032-140">Kauplusele aktsepteeritavate makseviiside määramine.</span><span class="sxs-lookup"><span data-stu-id="d1032-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="d1032-141">Üksikasjade lisamine oma kauplustes pakutavatele toodete kirjeldusse.</span><span class="sxs-lookup"><span data-stu-id="d1032-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="d1032-142">Näiteks saate lisada rtf-teksti ja pilte.</span><span class="sxs-lookup"><span data-stu-id="d1032-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="d1032-143">Toote üksikasjad kuvatakse erinevates kontekstides, nt kassaregistri või prinditud siltidel.</span><span class="sxs-lookup"><span data-stu-id="d1032-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="d1032-144">Lisage kauplus organisatsiooni vaikehierarhiasse, mis on määratud eesmärgile **Jaemüügi sortiment**, **Jaemüügi täiendamine** või **Jaemüügi aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="d1032-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="d1032-145">Pärast kaupluse seadistamist</span><span class="sxs-lookup"><span data-stu-id="d1032-145">After you set up a retail store</span></span>

<span data-ttu-id="d1032-146">Kui kaupluse üksikasjad on sisestatud, täitke uue kaupluse andmete saatmiseks rakendusse Retail POS järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="d1032-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1. <span data-ttu-id="d1032-147">Kaupluse kassaregistrite konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="d1032-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="d1032-148">Tootesortimentide määramine kauplusele.</span><span class="sxs-lookup"><span data-stu-id="d1032-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="d1032-149">Sortimentide töötlemine, et luua sortimenti kaasatav tooteloend ja teha tooted kaupluses kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="d1032-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4. <span data-ttu-id="d1032-150">Andmete (numbriseeriad, riistvaraprofiilid ja kassaekraanide paigutus) saatmine rakenduse Retail POS registritesse.</span><span class="sxs-lookup"><span data-stu-id="d1032-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5. <span data-ttu-id="d1032-151">Kaupluse avaldamine kaupluse andmete saatmiseks rakendusse Retail POS.</span><span class="sxs-lookup"><span data-stu-id="d1032-151">Publish the retail store to send store data to Retail POS.</span></span>
6. <span data-ttu-id="d1032-152">Tööde käivitamine kaupluse andmete saatmiseks rakendusse Retail POS.</span><span class="sxs-lookup"><span data-stu-id="d1032-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="d1032-153">Organisatsiooni hierarhiad</span><span class="sxs-lookup"><span data-stu-id="d1032-153">Organization hierarchies</span></span>

<span data-ttu-id="d1032-154">Retail kasutab organisatsiooni hierarhiaid jaemüügikanalite struktureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="d1032-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="d1032-155">Organisatsiooni hierarhia kajastab ettevõttesse kuuluvate organisatsioonide vahelisi seoseid.</span><span class="sxs-lookup"><span data-stu-id="d1032-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="d1032-156">Kaupluste seadistamisel saate need lisada organisatsiooni hierarhiasse.</span><span class="sxs-lookup"><span data-stu-id="d1032-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="d1032-157">Seejärel on sortimentide, täiendamise ja aruandluse jaoks kasutatavad andmed kaupluste vahel ühiskasutuses.</span><span class="sxs-lookup"><span data-stu-id="d1032-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>
