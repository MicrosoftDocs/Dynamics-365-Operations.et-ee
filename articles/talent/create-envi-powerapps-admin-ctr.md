---
title: Power Appsi halduskeskuses ei saa keskkonda luua
description: Selles teemas selgitatakse, mida teha, kui administraator ei saa Microsoft Power Appsi halduskeskuses keskkonda luua.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5923c59ab5dde13fed0483972e76634031404fd8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773215"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="2311e-103">Power Appsi halduskeskuses ei saa keskkonda luua</span><span class="sxs-lookup"><span data-stu-id="2311e-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2311e-104">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="2311e-104">**Issue**</span></span>

- <span data-ttu-id="2311e-105">Rentniku/keskkonna administraator ei saa Microsoft Power Appsi halduskeskuses keskkonda luua.</span><span class="sxs-lookup"><span data-stu-id="2311e-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="2311e-106">Litsents, mis annab kasutajatele õiguse teostada keskkonna loomise etappi, ei ole määratud otse seda etappi teostavale kasutajale.</span><span class="sxs-lookup"><span data-stu-id="2311e-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="2311e-107">**Lahendus**</span><span class="sxs-lookup"><span data-stu-id="2311e-107">**Solution**</span></span>

<span data-ttu-id="2311e-108">Veenduge, et rentniku administraator oleks määranud kehtiva Power Apps P2 litsentsi otse kasutajale, kes teostab keskkonna loomise etappi.</span><span class="sxs-lookup"><span data-stu-id="2311e-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="2311e-109">Siit leiate Microsoft Dynamicsi teenuseplaanid, mis annavad selle õiguse.</span><span class="sxs-lookup"><span data-stu-id="2311e-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="2311e-110">Üldine toote varude arvestusühik (SKU)</span><span class="sxs-lookup"><span data-stu-id="2311e-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="2311e-111">Power Apps P2 teenusepakett</span><span class="sxs-lookup"><span data-stu-id="2311e-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="2311e-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="2311e-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="2311e-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="2311e-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="2311e-114">Microsoft Dynamics 365 plaan, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="2311e-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="2311e-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="2311e-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="2311e-116">Pange tähele, et erinevad Microsoft Office’i SKU-d annavad samuti selle õiguse lisaks eraldiseisvatele Power Appsi plaani 2 SKU-dele.</span><span class="sxs-lookup"><span data-stu-id="2311e-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="2311e-117">Oluline on, et üks nendest SKU-dest oleks olemas.</span><span class="sxs-lookup"><span data-stu-id="2311e-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="2311e-118">Avage [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="2311e-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="2311e-119">Looge keskkondi, järgides juhiseid jaotises [Talenti ettevalmistamine](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="2311e-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
