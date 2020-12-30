---
title: Jaemüügikanalite määratlemine ja haldamine
description: Selles teemas antakse ülevaade füüsilistele kaupluste, mida nimetatakse Dynamics 365 Commerce'is kauplusteks, seadistamise protsessist. See sisaldab teavet ülesannete kohta, mis tuleb lõpule viia enne ja pärast kaupluse seadistamist.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 0fbca2c9178cd372653287afdf72deaf75442604
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411591"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="1591b-104">Jaemüügikanalite määratlemine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="1591b-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1591b-105">Selles teemas antakse ülevaade füüsilistele kaupluste, mida nimetatakse Dynamics 365 Commerce'is kauplusteks, seadistamise protsessist.</span><span class="sxs-lookup"><span data-stu-id="1591b-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="1591b-106">See sisaldab teavet ülesannete kohta, mis tuleb lõpule viia enne ja pärast kaupluse seadistamist.</span><span class="sxs-lookup"><span data-stu-id="1591b-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="1591b-107">Commerce toetab mitmeid kanaleid, nagu võrgupoed, kõnekeskused ja traditsioonilised kauplused.</span><span class="sxs-lookup"><span data-stu-id="1591b-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="1591b-108">Traditsioonilist kauplust nimetatakse kaupluseks.</span><span class="sxs-lookup"><span data-stu-id="1591b-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="1591b-109">Igal kauplusel võivad olla oma makseviisid, hinnagrupid, kassaregistrid, tulu- ja kulukontod ning personal.</span><span class="sxs-lookup"><span data-stu-id="1591b-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="1591b-110">Enne kaupluse loomist tuleb seadistada kõik need elemendid.</span><span class="sxs-lookup"><span data-stu-id="1591b-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="1591b-111">Kui olete kaupluse loonud, saate määrata seal müüdavad tooted.</span><span class="sxs-lookup"><span data-stu-id="1591b-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="1591b-112">Saate kauplusele määrata ka töötajad, registrid ja kliendid.</span><span class="sxs-lookup"><span data-stu-id="1591b-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="1591b-113">Viimaks peate lisama uue kaupluse organisatsioonihierarhiasse.</span><span class="sxs-lookup"><span data-stu-id="1591b-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="1591b-114">Kaupluste seadistamine</span><span class="sxs-lookup"><span data-stu-id="1591b-114">Setting up stores</span></span>

<span data-ttu-id="1591b-115">Enne kui saate rakenduses Commerce kaupluse seadistada, peate täitma mõne eeltingimuseks oleva ülesande.</span><span class="sxs-lookup"><span data-stu-id="1591b-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="1591b-116">Seejärel saate luua kaupluse ja lisada üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="1591b-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="1591b-117">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="1591b-117">Prerequisites</span></span>

<span data-ttu-id="1591b-118">Enne kui saate kaupluse seadistada, peate tegema järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="1591b-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="1591b-119">Saate konfigureerida organisatsiooni struktuuri ja seadistada organisatsiooni hierarhiad jaemüügisortimendi, täiendamise ja aruannete jaoks.</span><span class="sxs-lookup"><span data-stu-id="1591b-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="1591b-120">Saate seadistada kauplust kajastava lao.</span><span class="sxs-lookup"><span data-stu-id="1591b-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="1591b-121">Kaupluste, kaupluse väljavõtete ja väljavõttekannete numbriseeriate seadistamine.</span><span class="sxs-lookup"><span data-stu-id="1591b-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="1591b-122">Commerce'i parameetrite konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="1591b-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="1591b-123">Kaupluses aktsepteeritavate makseviiside seadistamine.</span><span class="sxs-lookup"><span data-stu-id="1591b-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="1591b-124">Kassaregistrites krediitkaardikannete töötlemiseks saate seadistada ka makseteenused.</span><span class="sxs-lookup"><span data-stu-id="1591b-124">To process credit card transactions at POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="1591b-125">Käibemaksugruppide seadistamine.</span><span class="sxs-lookup"><span data-stu-id="1591b-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="1591b-126">Seadistage tooted.</span><span class="sxs-lookup"><span data-stu-id="1591b-126">Set up products.</span></span> <span data-ttu-id="1591b-127">Selle toimingu raames seadistate ka tootehierarhiad, tootevariandid ja tootesortimendid.</span><span class="sxs-lookup"><span data-stu-id="1591b-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="1591b-128">Toote hinnagruppide seadistamine.</span><span class="sxs-lookup"><span data-stu-id="1591b-128">Set up product price groups.</span></span>
10. <span data-ttu-id="1591b-129">Toote hinnakujunduse seadistamine.</span><span class="sxs-lookup"><span data-stu-id="1591b-129">Set up product pricing.</span></span> <span data-ttu-id="1591b-130">Selle toimingu raames seadistate ka hinnakorrektsioonid, allahindlused ja allahindluse perioodid.</span><span class="sxs-lookup"><span data-stu-id="1591b-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="1591b-131">Töötajate seadistamine.</span><span class="sxs-lookup"><span data-stu-id="1591b-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1591b-132">Peate määrama töötajatele ka vajalikud õigused, et nad saaksid sisse logida ja teha toiminguid, kasutades kassasüsteemi.</span><span class="sxs-lookup"><span data-stu-id="1591b-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="1591b-133">Kauplusele määratavate kassa profiilide konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="1591b-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="1591b-134">See toiming hõlmab mitmeid toiminguid, nagu registrite, ühenduseta profiilide ning kviitungivormingute ja -profiilide seadistamine.</span><span class="sxs-lookup"><span data-stu-id="1591b-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="1591b-135">Vaadake kõik eeltingimustes nimetatud toimingud üle ja tehke ainult teid puudutavad toimingud.</span><span class="sxs-lookup"><span data-stu-id="1591b-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="1591b-136">Kaupluse seadistamine</span><span class="sxs-lookup"><span data-stu-id="1591b-136">Set up a store</span></span>

<span data-ttu-id="1591b-137">Kui eeltingimuseks olevad ülesanded on täidetud, täitke kaupluse üksikasjade seadistamiseks järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="1591b-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="1591b-138">Looge kauplus.</span><span class="sxs-lookup"><span data-stu-id="1591b-138">Create a store.</span></span>
2. <span data-ttu-id="1591b-139">Kauplusele käibemaksugrupi määramine.</span><span class="sxs-lookup"><span data-stu-id="1591b-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="1591b-140">Kauplusele aktsepteeritavate makseviiside määramine.</span><span class="sxs-lookup"><span data-stu-id="1591b-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="1591b-141">Üksikasjade lisamine oma kauplustes pakutavatele toodete kirjeldusse.</span><span class="sxs-lookup"><span data-stu-id="1591b-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="1591b-142">Näiteks saate lisada rtf-teksti ja pilte.</span><span class="sxs-lookup"><span data-stu-id="1591b-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="1591b-143">Toote üksikasjad kuvatakse erinevates kontekstides, nt kassaregistri või prinditud siltidel.</span><span class="sxs-lookup"><span data-stu-id="1591b-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="1591b-144">Lisage kauplus organisatsiooni vaikehierarhiasse, mis on määratud eesmärgile **Jaemüügi sortiment**, **Jaemüügi täiendamine** või **Jaemüügi aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="1591b-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="1591b-145">Pärast kaupluse seadistamist</span><span class="sxs-lookup"><span data-stu-id="1591b-145">After you set up a store</span></span>

<span data-ttu-id="1591b-146">Kui kaupluse üksikasjad on sisestatud, täitke uue kaupluse andmete kassasse saatmised järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="1591b-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="1591b-147">Kaupluse kassaregistrite konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="1591b-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="1591b-148">Tootesortimentide määramine kauplusele.</span><span class="sxs-lookup"><span data-stu-id="1591b-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="1591b-149">Sortimentide töötlemine, et luua sortimenti kaasatav tooteloend ja teha tooted kaupluses kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="1591b-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="1591b-150">Andmete (numbriseeriad, riistvaraprofiilid ja kassaekraanide paigutus) saatmine kassa registritesse.</span><span class="sxs-lookup"><span data-stu-id="1591b-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="1591b-151">Kaupluse avaldamine kaupluse andmete saatmiseks kassasse.</span><span class="sxs-lookup"><span data-stu-id="1591b-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="1591b-152">Tööde käivitamine kaupluse andmete saatmiseks kassasse.</span><span class="sxs-lookup"><span data-stu-id="1591b-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="1591b-153">Organisatsiooni hierarhiad</span><span class="sxs-lookup"><span data-stu-id="1591b-153">Organization hierarchies</span></span>

<span data-ttu-id="1591b-154">Commerce kasutab organisatsiooni hierarhiaid kanalite struktureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="1591b-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="1591b-155">Organisatsiooni hierarhia kajastab ettevõttesse kuuluvate organisatsioonide vahelisi seoseid.</span><span class="sxs-lookup"><span data-stu-id="1591b-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="1591b-156">Kaupluste seadistamisel saate need lisada organisatsiooni hierarhiasse.</span><span class="sxs-lookup"><span data-stu-id="1591b-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="1591b-157">Seejärel on sortimentide, täiendamise ja aruandluse jaoks kasutatavad andmed kaupluste vahel ühiskasutuses.</span><span class="sxs-lookup"><span data-stu-id="1591b-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="1591b-158">Commerce’i müügifunktsiooni kasutamiseks peab suvandi **Mitu saajat** konfiguratsioonivõti olema lubatud.</span><span class="sxs-lookup"><span data-stu-id="1591b-158">To use Commerce sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="1591b-159">Selle konfiguratsioonivõtme leiate **Kaubanduse konfiguratsiooni** võtmetest asukohas **Süsteemihaldus**\> **Seadistus** \> **Litsentsi konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="1591b-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="1591b-160">See on nõutav erinevate valideerimiste tõttu, mis põhinevad müügitellimuse rea tasemel konfigureeritud tarneaadressil.</span><span class="sxs-lookup"><span data-stu-id="1591b-160">This is required due to various validations based on the delivery address configured at the sales order line level.</span></span>

