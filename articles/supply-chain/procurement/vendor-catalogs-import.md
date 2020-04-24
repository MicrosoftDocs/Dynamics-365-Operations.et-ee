---
title: Hankija kataloogide importimine
description: Selles teemas kirjeldatakse hankija kataloogi andmete importimise protsessi.
author: mkirknel
manager: tfehr
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 35b8e2a87708c88b12c5c7605a7977712a35a0f4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207367"
---
# <a name="import-vendor-catalogs"></a><span data-ttu-id="10b46-103">Hankija kataloogide importimine</span><span class="sxs-lookup"><span data-stu-id="10b46-103">Import vendor catalogs</span></span>
[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="10b46-104">Hankija kataloogide importimine</span><span class="sxs-lookup"><span data-stu-id="10b46-104">Vendor catalogs import</span></span>

<span data-ttu-id="10b46-105">Dynamics 365 Supply Chain Managementis saavad ostuspetsialistid luua ja hallata katalooge, mida ettevõtte töötajad saavad kaupade ning teenuste sisemiseks kasutamiseks tellimisel kasutada.</span><span class="sxs-lookup"><span data-stu-id="10b46-105">In Dynamics 365 Supply Chain Management, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="10b46-106">Hankekataloogi loomiseks saate lisada kaupu ja teenuseid, mille soovite töötajatele kättesaadavaks teha, importides tootekataloogi andmed või lisades tootekataloogi andmed käsitsi tooteetaloni.</span><span class="sxs-lookup"><span data-stu-id="10b46-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="10b46-107">Saate laadida üles kataloogiandmed, mille hankija on edastanud Microsoft Dynamics 365 kliendist.</span><span class="sxs-lookup"><span data-stu-id="10b46-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="10b46-108">Tooteandmed, mille hankija edastab teile kataloogihoolduse nõude (CMR) faili kujul, peavad olema XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="10b46-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="10b46-109">CMR-fail peab sisaldama nende toodete andmeid, mida hankija teie ettevõttele tarnib.</span><span class="sxs-lookup"><span data-stu-id="10b46-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>
<span data-ttu-id="10b46-110">„”</span><span class="sxs-lookup"><span data-stu-id="10b46-110">''''</span></span>
## <a name="import-vendor-catalog-data"></a><span data-ttu-id="10b46-111">Hankija kataloogi andmete importimine</span><span class="sxs-lookup"><span data-stu-id="10b46-111">Import vendor catalog data</span></span>
<span data-ttu-id="10b46-112">„Hankija kataloogi andmete importimiseks peate täitma järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="10b46-112">'' To import vendor catalog data, you must complete the following tasks:</span></span>

1.  <span data-ttu-id="10b46-113">Seadistage andmehalduse tööruumis projekt, kus olete määratlenud andmete vastandamise reeglid.</span><span class="sxs-lookup"><span data-stu-id="10b46-113">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="10b46-114">Valige **Andmehaldus** ja seejärel valige **Andmeprojektide jaoks vajalike rollide seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="10b46-114">Select **Data management** and then select **Set up roles for data projects**.</span></span> 
    <span data-ttu-id="10b46-115">”</span><span class="sxs-lookup"><span data-stu-id="10b46-115">''</span></span>
2.  <span data-ttu-id="10b46-116">Seadistage hankekategooria hierarhia ja määrake oma hankijad hankekategooriatesse.</span><span class="sxs-lookup"><span data-stu-id="10b46-116">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="10b46-117">Artiklikoodide kasutamisel lisage artiklikoodid hankekategooriatesse.</span><span class="sxs-lookup"><span data-stu-id="10b46-117">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="10b46-118">Hankekategooria hierarhia seadistamise kohta lisateabe saamiseks vt jaotist [Hankekategooria hierarhia seadistamine](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="10b46-118">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>
    <span data-ttu-id="10b46-119">”</span><span class="sxs-lookup"><span data-stu-id="10b46-119">''</span></span>
3.  <span data-ttu-id="10b46-120">Konfigureerige kataloogi impordi jaoks hankija.</span><span class="sxs-lookup"><span data-stu-id="10b46-120">Configure the vendor for catalog import.</span></span> <span data-ttu-id="10b46-121">Valige hankija ja seejärel valige **Hange** > **Seadista** > **Kataloogi importimiseks hankija konfigureerimine**.</span><span class="sxs-lookup"><span data-stu-id="10b46-121">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>
<span data-ttu-id="10b46-122">„”</span><span class="sxs-lookup"><span data-stu-id="10b46-122">''''</span></span>
4.  <span data-ttu-id="10b46-123">Konfigureerige töövoogu kataloogi importimiseks.</span><span class="sxs-lookup"><span data-stu-id="10b46-123">Configure workflow for catalog import.</span></span> <span data-ttu-id="10b46-124">Looge CMR-faili mall ja jagage seda oma hankijaga.</span><span class="sxs-lookup"><span data-stu-id="10b46-124">Create a CMR file template and share this with your vendor.</span></span>

5.  <span data-ttu-id="10b46-125">Valige **Hanked** \> **Ühine** \> **Kataloogid** \> **Hankija kataloogid**, et luua hankija kataloog.</span><span class="sxs-lookup"><span data-stu-id="10b46-125">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="10b46-126">Selles kataloogis on grupeeritud kataloogihoolduse nõude (CMR) failid, mille saate oma hankijalt.</span><span class="sxs-lookup"><span data-stu-id="10b46-126">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6.  <span data-ttu-id="10b46-127">Laadige üles CRM-fail.</span><span class="sxs-lookup"><span data-stu-id="10b46-127">Upload the CMR file.</span></span>

7.  <span data-ttu-id="10b46-128">Vaadake üle, kinnitage või lükake hankija kataloogis olevad tooted tagasi.</span><span class="sxs-lookup"><span data-stu-id="10b46-128">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="10b46-129">Tooted vastendatakse automaatselt hankekategooriatega.</span><span class="sxs-lookup"><span data-stu-id="10b46-129">The products are automatically mapped to the procurement categories.</span></span> 
    
<span data-ttu-id="10b46-130">Kinnitatud tooted lisatakse tooteetaloni ja väljastatakse valitud juriidilistele isikutele.</span><span class="sxs-lookup"><span data-stu-id="10b46-130">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="10b46-131">Hankekataloogi saab lisada ainult kinnitatud tooteid.</span><span class="sxs-lookup"><span data-stu-id="10b46-131">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="10b46-132">Kataloogi importimisfaili malli loomine</span><span class="sxs-lookup"><span data-stu-id="10b46-132">Generate a catalog import file template</span></span>

<span data-ttu-id="10b46-133">Kataloogi impordifaili mall on XSD-fail, mille abil saate luua hankija toodete CMR-faili.</span><span class="sxs-lookup"><span data-stu-id="10b46-133">The catalog import file template is an XSD file that you use to create a CMR file for a vendor's products.</span></span> <span data-ttu-id="10b46-134">Saate kasutada CMR-faili uue kataloogi loomiseks, olemasoleva kataloogi asendamiseks või muutmiseks.</span><span class="sxs-lookup"><span data-stu-id="10b46-134">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1.  <span data-ttu-id="10b46-135">Valige **Hanked** \> **Kataloogid** \> **Hankija kataloogid** ja topeltklõpsake kataloogil, millega soovite töötada.</span><span class="sxs-lookup"><span data-stu-id="10b46-135">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor catalogs** and double-click the catalog that you want to work with.</span></span>

2.  <span data-ttu-id="10b46-136">Laadige alla kehtiv kataloogi importimise mall (XSD-fail).</span><span class="sxs-lookup"><span data-stu-id="10b46-136">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="10b46-137">Lehel **Kataloogi värskendamine** valikus **Tegumiriba** vahekaardil **Kataloogid** grupis **Seostuv teave** klõpsake suvandil **Kataloogi malli loomine** ja valige **Hankekategooria**.</span><span class="sxs-lookup"><span data-stu-id="10b46-137">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    -   <span data-ttu-id="10b46-138">Suvandiga **Hankekategooria** saate luua kataloogimalli, mis sisaldab hankekategooriaid, milles hankijal on lubatud tooteid pakkuda.</span><span class="sxs-lookup"><span data-stu-id="10b46-138">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="10b46-139">Valige dialoogikastis **Salvesta nimega** asukoht, kus soovite kataloogifaili malli talletada ja salvestage fail.</span><span class="sxs-lookup"><span data-stu-id="10b46-139">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="10b46-140">Lisateavet ja näiteid vt ajaveebipostitusest [Hankija kataloogid rakenduses Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span><span class="sxs-lookup"><span data-stu-id="10b46-140">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>
