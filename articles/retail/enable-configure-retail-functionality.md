---
title: "Algandmete lähtestamine uues jaemüügikeskkonnas"
description: "See artikkel kirjeldab andmeid, mis luuakse Microsoft Dynamics 365 for Retaili jaemüügimooduli lähtestamisprotsessi käigus."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: af2d01dcfddc11559c6c5b046dcac8cd8dc95e76
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a><span data-ttu-id="bdb14-103">Algandmete lähtestamine uues jaemüügikeskkonnas</span><span class="sxs-lookup"><span data-stu-id="bdb14-103">Initialize seed data in a new Retail environment</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="bdb14-104">See artikkel kirjeldab andmeid, mis luuakse Microsoft Dynamics 365 for Retaili jaemüügimooduli lähtestamisprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="bdb14-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="bdb14-105">Pärast Microsoft Dynamicsi teenuse Lifecycle Services (LCS) kaudu lahenduse Jaemüük juurutamist peate lähtestama jaemüügi konfiguratsiooni, et luua põhilised konfigureerimise andmed.</span><span class="sxs-lookup"><span data-stu-id="bdb14-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span> <span data-ttu-id="bdb14-106">**Oluline.** Enne jaemüügi konfiguratsiooni lähtestamist veenduge, et olete määranud keele ja postiaadressi igale juriidilisele isikule, kus te jaemüügikaupluse seadistate.</span><span class="sxs-lookup"><span data-stu-id="bdb14-106">**Important:** Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="bdb14-107">See etapp tuleb läbida iga juriidilise isiku puhul, mida jaemüügiks kasutate.</span><span class="sxs-lookup"><span data-stu-id="bdb14-107">This step must be completed for each legal entity that you use for retail.</span></span> <span data-ttu-id="bdb14-108">Jaemüügikonfiguratsiooni lähtestamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="bdb14-108">To initialize the retail configuration, follow these steps.</span></span>

1.  <span data-ttu-id="bdb14-109">Käivitage Dynamics 365 for Retaili klient.</span><span class="sxs-lookup"><span data-stu-id="bdb14-109">Start the Dynamics 365 for Retail client.</span></span>
2.  <span data-ttu-id="bdb14-110">Klõpsake valikuid **Jaemüük** &gt; **Peakontori seadistamine** &gt; **Parameetrid** &gt; **Jaemüügi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="bdb14-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3.  <span data-ttu-id="bdb14-111">Klõpsake suvandit **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="bdb14-111">Click **Initialize**.</span></span>

<span data-ttu-id="bdb14-112">Lähtestamine loob järgmised konfiguratsiooni vaikeandmed.</span><span class="sxs-lookup"><span data-stu-id="bdb14-112">Initialization creates the following default configuration data:</span></span>

-   <span data-ttu-id="bdb14-113">Kaupluse andmeedastaja tööd ja alamtööd</span><span class="sxs-lookup"><span data-stu-id="bdb14-113">Retail scheduler jobs and subjobs</span></span>
-   <span data-ttu-id="bdb14-114">Jaemüügikanali skeem</span><span class="sxs-lookup"><span data-stu-id="bdb14-114">Retail channel schema</span></span>
-   <span data-ttu-id="bdb14-115">Jaemüügi jaotusgraafikud</span><span class="sxs-lookup"><span data-stu-id="bdb14-115">Retail distribution schedules</span></span>
-   <span data-ttu-id="bdb14-116">Ekraani vaikepaigutused, mis hõlmavad nupupaneele, pilte ja kujundusi</span><span class="sxs-lookup"><span data-stu-id="bdb14-116">Default screen layouts, which include button grids, images, and themes</span></span>
-   <span data-ttu-id="bdb14-117">Ajavööndi teave</span><span class="sxs-lookup"><span data-stu-id="bdb14-117">Time zone information</span></span>
-   <span data-ttu-id="bdb14-118">Kassa (POS) toimingud</span><span class="sxs-lookup"><span data-stu-id="bdb14-118">Point-of-sale (POS) operations</span></span>
-   <span data-ttu-id="bdb14-119">Kassaload</span><span class="sxs-lookup"><span data-stu-id="bdb14-119">POS permissions</span></span>
-   <span data-ttu-id="bdb14-120">Kanali aruanded</span><span class="sxs-lookup"><span data-stu-id="bdb14-120">Channel reports</span></span>
-   <span data-ttu-id="bdb14-121">Atribuudi metaandmed</span><span class="sxs-lookup"><span data-stu-id="bdb14-121">Attribute metadata</span></span>
-   <span data-ttu-id="bdb14-122">Üksuse kinnitamise mallid</span><span class="sxs-lookup"><span data-stu-id="bdb14-122">Entity validation templates</span></span>
-   <span data-ttu-id="bdb14-123">Pakett-töö rakenduse Commerce Data Exchange seansi ajaloo kustutamiseks</span><span class="sxs-lookup"><span data-stu-id="bdb14-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="bdb14-124">Lisaks lubatakse Dynamics 365 for Retaili andmebaasi jaoks logimine, mis on seotud maksekaardi tööstusharuga (PCI).</span><span class="sxs-lookup"><span data-stu-id="bdb14-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span> <span data-ttu-id="bdb14-125">**Märkus.** On võimalus suvandi Kaupluse andmeedastaja eraldi konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="bdb14-125">**Note:** There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="bdb14-126">See võimalus võimaldab teil suvandi Kaupluse andmeedastaja konfiguratsiooni vaikesätetele lähtestada.</span><span class="sxs-lookup"><span data-stu-id="bdb14-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span> <span data-ttu-id="bdb14-127">Pärast lähtestamise lõpule viimist peate konfigureerima täiendavad jaemüügiandmed.</span><span class="sxs-lookup"><span data-stu-id="bdb14-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="bdb14-128">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="bdb14-128">Here are some examples:</span></span>

-   <span data-ttu-id="bdb14-129">Jaemüügi parameetrid</span><span class="sxs-lookup"><span data-stu-id="bdb14-129">Retail parameters</span></span>
-   <span data-ttu-id="bdb14-130">Kaupluse andmeedastaja parameetrid</span><span class="sxs-lookup"><span data-stu-id="bdb14-130">Retail scheduler parameters</span></span>
-   <span data-ttu-id="bdb14-131">Jaemüügikanalid</span><span class="sxs-lookup"><span data-stu-id="bdb14-131">Retail channels</span></span>
-   <span data-ttu-id="bdb14-132">Registrid ja seadmed</span><span class="sxs-lookup"><span data-stu-id="bdb14-132">Registers and devices</span></span>
-   <span data-ttu-id="bdb14-133">Sortimendid</span><span class="sxs-lookup"><span data-stu-id="bdb14-133">Assortments</span></span>





