---
title: "Algandmete lähtestamine uutes Retaili keskkondades"
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
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 80fa443fc235496a111a8a866d2e703202721268
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="ebd87-103">Algandmete lähtestamine uutes Retaili keskkondades</span><span class="sxs-lookup"><span data-stu-id="ebd87-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ebd87-104">See artikkel kirjeldab andmeid, mis luuakse Microsoft Dynamics 365 for Retaili jaemüügimooduli lähtestamisprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="ebd87-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="ebd87-105">Pärast Microsoft Dynamicsi teenuse Lifecycle Services (LCS) kaudu lahenduse Jaemüük juurutamist peate lähtestama jaemüügi konfiguratsiooni, et luua põhilised konfigureerimise andmed.</span><span class="sxs-lookup"><span data-stu-id="ebd87-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span> <span data-ttu-id="ebd87-106">**Oluline.** Enne jaemüügi konfiguratsiooni lähtestamist veenduge, et olete määranud keele ja postiaadressi igale juriidilisele isikule, kus te jaemüügikaupluse seadistate.</span><span class="sxs-lookup"><span data-stu-id="ebd87-106">**Important:** Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="ebd87-107">See etapp tuleb läbida iga juriidilise isiku puhul, mida jaemüügiks kasutate.</span><span class="sxs-lookup"><span data-stu-id="ebd87-107">This step must be completed for each legal entity that you use for retail.</span></span> <span data-ttu-id="ebd87-108">Jaemüügikonfiguratsiooni lähtestamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ebd87-108">To initialize the retail configuration, follow these steps.</span></span>

1.  <span data-ttu-id="ebd87-109">Käivitage Dynamics 365 for Retaili klient.</span><span class="sxs-lookup"><span data-stu-id="ebd87-109">Start the Dynamics 365 for Retail client.</span></span>
2.  <span data-ttu-id="ebd87-110">Klõpsake valikuid **Jaemüük** &gt; **Peakontori seadistamine** &gt; **Parameetrid** &gt; **Jaemüügi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="ebd87-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3.  <span data-ttu-id="ebd87-111">Klõpsake suvandit **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="ebd87-111">Click **Initialize**.</span></span>

<span data-ttu-id="ebd87-112">Lähtestamine loob järgmised konfiguratsiooni vaikeandmed.</span><span class="sxs-lookup"><span data-stu-id="ebd87-112">Initialization creates the following default configuration data:</span></span>

-   <span data-ttu-id="ebd87-113">Kaupluse andmeedastaja tööd ja alamtööd</span><span class="sxs-lookup"><span data-stu-id="ebd87-113">Retail scheduler jobs and subjobs</span></span>
-   <span data-ttu-id="ebd87-114">Jaemüügikanali skeem</span><span class="sxs-lookup"><span data-stu-id="ebd87-114">Retail channel schema</span></span>
-   <span data-ttu-id="ebd87-115">Jaemüügi jaotusgraafikud</span><span class="sxs-lookup"><span data-stu-id="ebd87-115">Retail distribution schedules</span></span>
-   <span data-ttu-id="ebd87-116">Ekraani vaikepaigutused, mis hõlmavad nupupaneele, pilte ja kujundusi</span><span class="sxs-lookup"><span data-stu-id="ebd87-116">Default screen layouts, which include button grids, images, and themes</span></span>
-   <span data-ttu-id="ebd87-117">Ajavööndi teave</span><span class="sxs-lookup"><span data-stu-id="ebd87-117">Time zone information</span></span>
-   <span data-ttu-id="ebd87-118">Kassa (POS) toimingud</span><span class="sxs-lookup"><span data-stu-id="ebd87-118">Point-of-sale (POS) operations</span></span>
-   <span data-ttu-id="ebd87-119">Kassaload</span><span class="sxs-lookup"><span data-stu-id="ebd87-119">POS permissions</span></span>
-   <span data-ttu-id="ebd87-120">Kanali aruanded</span><span class="sxs-lookup"><span data-stu-id="ebd87-120">Channel reports</span></span>
-   <span data-ttu-id="ebd87-121">Atribuudi metaandmed</span><span class="sxs-lookup"><span data-stu-id="ebd87-121">Attribute metadata</span></span>
-   <span data-ttu-id="ebd87-122">Üksuse kinnitamise mallid</span><span class="sxs-lookup"><span data-stu-id="ebd87-122">Entity validation templates</span></span>
-   <span data-ttu-id="ebd87-123">Pakett-töö rakenduse Commerce Data Exchange seansi ajaloo kustutamiseks</span><span class="sxs-lookup"><span data-stu-id="ebd87-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="ebd87-124">Lisaks lubatakse Dynamics 365 for Retaili andmebaasi jaoks logimine, mis on seotud maksekaardi tööstusharuga (PCI).</span><span class="sxs-lookup"><span data-stu-id="ebd87-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span> <span data-ttu-id="ebd87-125">**Märkus.** On võimalus suvandi Kaupluse andmeedastaja eraldi konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="ebd87-125">**Note:** There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="ebd87-126">See võimalus võimaldab teil suvandi Kaupluse andmeedastaja konfiguratsiooni vaikesätetele lähtestada.</span><span class="sxs-lookup"><span data-stu-id="ebd87-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span> <span data-ttu-id="ebd87-127">Pärast lähtestamise lõpule viimist peate konfigureerima täiendavad jaemüügiandmed.</span><span class="sxs-lookup"><span data-stu-id="ebd87-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="ebd87-128">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="ebd87-128">Here are some examples:</span></span>

-   <span data-ttu-id="ebd87-129">Jaemüügi parameetrid</span><span class="sxs-lookup"><span data-stu-id="ebd87-129">Retail parameters</span></span>
-   <span data-ttu-id="ebd87-130">Kaupluse andmeedastaja parameetrid</span><span class="sxs-lookup"><span data-stu-id="ebd87-130">Retail scheduler parameters</span></span>
-   <span data-ttu-id="ebd87-131">Jaemüügikanalid</span><span class="sxs-lookup"><span data-stu-id="ebd87-131">Retail channels</span></span>
-   <span data-ttu-id="ebd87-132">Registrid ja seadmed</span><span class="sxs-lookup"><span data-stu-id="ebd87-132">Registers and devices</span></span>
-   <span data-ttu-id="ebd87-133">Sortimendid</span><span class="sxs-lookup"><span data-stu-id="ebd87-133">Assortments</span></span>





