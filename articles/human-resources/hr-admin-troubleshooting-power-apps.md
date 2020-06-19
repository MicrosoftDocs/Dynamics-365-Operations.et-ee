---
title: Power Appsi halduskeskuses ei saa keskkonda luua
description: Selles artiklis selgitatakse, mida teha, kui administraator ei saa Microsoft Power Appsi halduskeskuses keskkonda luua.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: 68e6dbcbbc9811211570e968047f5faa8a2c8bd0
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431057"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="7c181-103">Power Appsi halduskeskuses ei saa keskkonda luua</span><span class="sxs-lookup"><span data-stu-id="7c181-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="7c181-104">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="7c181-104">**Issue**</span></span>

- <span data-ttu-id="7c181-105">Rentniku/keskkonna administraator ei saa Microsoft Power Appsi halduskeskuses keskkonda luua.</span><span class="sxs-lookup"><span data-stu-id="7c181-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="7c181-106">Litsents, mis annab kasutajatele õiguse teostada keskkonna loomise etappi, ei ole määratud otse seda etappi teostavale kasutajale.</span><span class="sxs-lookup"><span data-stu-id="7c181-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="7c181-107">**Lahendus**</span><span class="sxs-lookup"><span data-stu-id="7c181-107">**Solution**</span></span>

<span data-ttu-id="7c181-108">Veenduge, et rentniku administraator oleks määranud kehtiva Power Apps P2 litsentsi otse kasutajale, kes teostab keskkonna loomise etappi.</span><span class="sxs-lookup"><span data-stu-id="7c181-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="7c181-109">Siit leiate Microsoft Dynamicsi teenuseplaanid, mis annavad selle õiguse.</span><span class="sxs-lookup"><span data-stu-id="7c181-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="7c181-110">Üldine toote varude arvestusühik (SKU)</span><span class="sxs-lookup"><span data-stu-id="7c181-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="7c181-111">Power Apps P2 teenusepakett</span><span class="sxs-lookup"><span data-stu-id="7c181-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="7c181-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="7c181-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="7c181-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7c181-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="7c181-114">Microsoft Dynamics 365 plaan, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="7c181-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="7c181-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7c181-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="7c181-116">Pange tähele, et erinevad Microsoft Office’i SKU-d annavad samuti selle õiguse lisaks eraldiseisvatele Power Appsi plaani 2 SKU-dele.</span><span class="sxs-lookup"><span data-stu-id="7c181-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="7c181-117">Oluline on, et üks nendest SKU-dest oleks olemas.</span><span class="sxs-lookup"><span data-stu-id="7c181-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="7c181-118">Avage [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="7c181-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="7c181-119">Looge keskkondi, järgides juhiseid teemas [Rakenduse Human Resources ettevalmistamine](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="7c181-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
