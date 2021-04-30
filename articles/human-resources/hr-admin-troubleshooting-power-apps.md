---
title: Power Appsi halduskeskuses ei saa keskkonda luua
description: Selles artiklis selgitatakse, mida teha, kui administraator ei saa Microsoft Power Appsi halduskeskuses keskkonda luua.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 26a228229a09e74809a048675a3ff90025f2a26c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892223"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="7f65a-103">Power Appsi halduskeskuses ei saa keskkonda luua</span><span class="sxs-lookup"><span data-stu-id="7f65a-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7f65a-104">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="7f65a-104">**Issue**</span></span>

- <span data-ttu-id="7f65a-105">Rentniku/keskkonna administraator ei saa Microsoft Power Appsi halduskeskuses keskkonda luua.</span><span class="sxs-lookup"><span data-stu-id="7f65a-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="7f65a-106">Kasutajal pole litsentsi, mis annab õiguse keskkondi luua.</span><span class="sxs-lookup"><span data-stu-id="7f65a-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="7f65a-107">**Lahendus**</span><span class="sxs-lookup"><span data-stu-id="7f65a-107">**Solution**</span></span>

<span data-ttu-id="7f65a-108">Veenduge, et rentniku administraator on keskkonda loovale kasutajale määranud kehtiva Power Apps P2 litsentsi.</span><span class="sxs-lookup"><span data-stu-id="7f65a-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="7f65a-109">Keskkondade loomiseks pakuvad õigusi järgmised Microsoft Dynamicsi teenuseplaanid.</span><span class="sxs-lookup"><span data-stu-id="7f65a-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="7f65a-110">Üldine toote varude arvestusühik (SKU)</span><span class="sxs-lookup"><span data-stu-id="7f65a-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="7f65a-111">Power Apps P2 teenusepakett</span><span class="sxs-lookup"><span data-stu-id="7f65a-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="7f65a-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="7f65a-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="7f65a-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7f65a-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="7f65a-114">Microsoft Dynamics 365 plaan, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="7f65a-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="7f65a-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7f65a-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="7f65a-116">Pange tähele, et erinevad Microsoft Office’i SKU-d annavad samuti selle õiguse lisaks eraldiseisvatele Power Appsi plaani 2 SKU-dele.</span><span class="sxs-lookup"><span data-stu-id="7f65a-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="7f65a-117">Oluline on, et üks nendest SKU-dest oleks olemas.</span><span class="sxs-lookup"><span data-stu-id="7f65a-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="7f65a-118">Avage [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="7f65a-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="7f65a-119">Looge keskkondi, järgides juhiseid teemas [Rakenduse Human Resources ettevalmistamine](/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="7f65a-119">Create the environments by following the instructions in [Provision Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]