---
title: Algandmete lähtestamine uutes Commerce'i keskkondades
description: See artikkel kirjeldab andmeid, mis luuakse Dynamics 365 Commercei jaemüügimooduli lähtestamisprotsessi käigus.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9f534410b21fd97554f4e038bb14eebd5f887130
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792579"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a><span data-ttu-id="08387-103">Algandmete lähtestamine uutes Commerce'i keskkondades</span><span class="sxs-lookup"><span data-stu-id="08387-103">Initialize seed data in new Commerce environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="08387-104">See artikkel kirjeldab andmeid, mis luuakse Dynamics 365 Commercei jaemüügimooduli lähtestamisprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="08387-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="08387-105">Pärast teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu lahenduse Kaubandus juurutamist peate lähtestama kaubanduse konfiguratsiooni, et luua põhilised konfigureerimise andmed.</span><span class="sxs-lookup"><span data-stu-id="08387-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08387-106">Enne kaubanduse konfiguratsiooni lähtestamist veenduge, et olete määranud keele ja postiaadressi igale juriidilisele isikule, kus te kaupluse seadistate.</span><span class="sxs-lookup"><span data-stu-id="08387-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="08387-107">See etapp tuleb läbida iga juriidilise isiku puhul, mida kaubanduses kasutate.</span><span class="sxs-lookup"><span data-stu-id="08387-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="08387-108">Konfiguratsiooni lähtestamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="08387-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="08387-109">Käivitage rakenduse Kaubandus klient.</span><span class="sxs-lookup"><span data-stu-id="08387-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="08387-110">Minge jaotisse **Jaemüük ja kaubandus** &gt; **Peakontori seadistamine** &gt; **Parameetrid** &gt; **Kaubanduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="08387-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="08387-111">Klõpsake suvandit **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="08387-111">Click **Initialize**.</span></span>

<span data-ttu-id="08387-112">Lähtestamine loob järgmised konfiguratsiooni vaikeandmed.</span><span class="sxs-lookup"><span data-stu-id="08387-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="08387-113">Kaubanduse andmeedastaja tööd ja alamtööd</span><span class="sxs-lookup"><span data-stu-id="08387-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="08387-114">Kaubanduse kanaliskeem</span><span class="sxs-lookup"><span data-stu-id="08387-114">Commerce channel schema</span></span>
- <span data-ttu-id="08387-115">Kaubanduse jaotuse graafikud</span><span class="sxs-lookup"><span data-stu-id="08387-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="08387-116">Ekraani vaikepaigutused, mis hõlmavad nupupaneele, pilte ja kujundusi</span><span class="sxs-lookup"><span data-stu-id="08387-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="08387-117">Ajavööndi teave</span><span class="sxs-lookup"><span data-stu-id="08387-117">Time zone information</span></span>
- <span data-ttu-id="08387-118">Kassa (POS) toimingud</span><span class="sxs-lookup"><span data-stu-id="08387-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="08387-119">Kassaload</span><span class="sxs-lookup"><span data-stu-id="08387-119">POS permissions</span></span>
- <span data-ttu-id="08387-120">Kanali aruanded</span><span class="sxs-lookup"><span data-stu-id="08387-120">Channel reports</span></span>
- <span data-ttu-id="08387-121">Atribuudi metaandmed</span><span class="sxs-lookup"><span data-stu-id="08387-121">Attribute metadata</span></span>
- <span data-ttu-id="08387-122">Üksuse kinnitamise mallid</span><span class="sxs-lookup"><span data-stu-id="08387-122">Entity validation templates</span></span>
- <span data-ttu-id="08387-123">Pakett-töö rakenduse Commerce Data Exchange seansiajaloo kustutamiseks</span><span class="sxs-lookup"><span data-stu-id="08387-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="08387-124">Peale selle lubatakse Kaubanduse andmebaasi jaoks logimine, mis on seotud maksekaardi tööstusharuga (PCI).</span><span class="sxs-lookup"><span data-stu-id="08387-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="08387-125">On võimalus suvandi Kaubanduse andmeedastaja eraldi konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="08387-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="08387-126">See võimalus võimaldab teil suvandi Kaubandus andmeedastaja konfiguratsiooni vaikesätetele lähtestada.</span><span class="sxs-lookup"><span data-stu-id="08387-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="08387-127">Pärast lähtestamise lõpule viimist peate konfigureerima täiendavad kaubandusandmed.</span><span class="sxs-lookup"><span data-stu-id="08387-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="08387-128">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="08387-128">Here are some examples:</span></span>

- <span data-ttu-id="08387-129">Kaubanduse parameetrid</span><span class="sxs-lookup"><span data-stu-id="08387-129">Commerce parameters</span></span>
- <span data-ttu-id="08387-130">Kaubanduse andmeedastaja parameetrid</span><span class="sxs-lookup"><span data-stu-id="08387-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="08387-131">Kaubanduse kanalid</span><span class="sxs-lookup"><span data-stu-id="08387-131">Commerce channels</span></span>
- <span data-ttu-id="08387-132">Registrid ja seadmed</span><span class="sxs-lookup"><span data-stu-id="08387-132">Registers and devices</span></span>
- <span data-ttu-id="08387-133">Sortimendid</span><span class="sxs-lookup"><span data-stu-id="08387-133">Assortments</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]