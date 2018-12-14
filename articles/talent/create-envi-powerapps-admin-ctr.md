---
title: PowerAppsi halduskeskuses ei saa keskkonda luua
description: See teema selgitab, mida teha, kui administraator ei saa Microsoft PowerAppsi halduskeskuses keskkonda luua.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.contentlocale: et-ee
ms.lasthandoff: 12/04/2018

---

# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="c32b9-103">PowerAppsi halduskeskuses ei saa keskkonda luua</span><span class="sxs-lookup"><span data-stu-id="c32b9-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c32b9-104">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="c32b9-104">**Issue**</span></span>

- <span data-ttu-id="c32b9-105">Rentniku/keskkonna administraator ei saa Microsoft PowerAppsi halduskeskuses keskkonda luua.</span><span class="sxs-lookup"><span data-stu-id="c32b9-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="c32b9-106">Litsents, mis annab kasutajatele õiguse teostada keskkonna loomise etappi, ei ole määratud otse seda etappi teostavale kasutajale.</span><span class="sxs-lookup"><span data-stu-id="c32b9-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="c32b9-107">**Lahendus**</span><span class="sxs-lookup"><span data-stu-id="c32b9-107">**Solution**</span></span>

<span data-ttu-id="c32b9-108">Veenduge, et rentniku administraator oleks määranud kehtiva PowerApps P2 litsentsi otse kasutajale, kes teostab keskkonna loomise etappi.</span><span class="sxs-lookup"><span data-stu-id="c32b9-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="c32b9-109">Siit leiate Microsoft Dynamicsi teenuseplaanid, mis annavad selle õiguse.</span><span class="sxs-lookup"><span data-stu-id="c32b9-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="c32b9-110">Üldine toote varude arvestusühik (SKU)</span><span class="sxs-lookup"><span data-stu-id="c32b9-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="c32b9-111">PowerApps P2 teenuseplaan</span><span class="sxs-lookup"><span data-stu-id="c32b9-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="c32b9-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="c32b9-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="c32b9-113">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c32b9-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="c32b9-114">Microsoft Dynamics 365 plaan, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="c32b9-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="c32b9-115">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c32b9-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="c32b9-116">Pange tähele, et erinevad Microsoft Office’i SKU-d annavad samuti selle õiguse, lisaks eraldiseisvatele PowerAppsi plaani 2 SKU-dele.</span><span class="sxs-lookup"><span data-stu-id="c32b9-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="c32b9-117">Oluline on, et üks nendest SKU-dest oleks olemas.</span><span class="sxs-lookup"><span data-stu-id="c32b9-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="c32b9-118">Avage [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="c32b9-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="c32b9-119">Looge keskkondi, järgides juhiseid jaotises [Talenti ettevalmistamine](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="c32b9-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

