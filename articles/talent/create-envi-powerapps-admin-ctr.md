---
title: PowerAppsi halduskeskuses ei saa keskkonda luua
description: Selles teemas selgitatakse, mida teha, kui administraator ei saa Microsoft PowerAppsi halduskeskuses keskkonda luua.
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
ms.openlocfilehash: 97d44dc034cb8097fc0ecf9ac4e485425f097102
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517763"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="b5251-103">Ei saa luua keskkonda PowerAppsi halduskeskuses</span><span class="sxs-lookup"><span data-stu-id="b5251-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b5251-104">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="b5251-104">**Issue**</span></span>

- <span data-ttu-id="b5251-105">Rentniku/keskkonna administraator ei saa Microsoft PowerAppsi halduskeskuses keskkonda luua.</span><span class="sxs-lookup"><span data-stu-id="b5251-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="b5251-106">Litsents, mis annab kasutajatele õiguse teostada keskkonna loomise etappi, ei ole määratud otse seda etappi teostavale kasutajale.</span><span class="sxs-lookup"><span data-stu-id="b5251-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="b5251-107">**Lahendus**</span><span class="sxs-lookup"><span data-stu-id="b5251-107">**Solution**</span></span>

<span data-ttu-id="b5251-108">Veenduge, et rentniku administraator oleks määranud kehtiva PowerApps P2 litsentsi otse kasutajale, kes teostab keskkonna loomise etappi.</span><span class="sxs-lookup"><span data-stu-id="b5251-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="b5251-109">Siit leiate Microsoft Dynamicsi teenuseplaanid, mis annavad selle õiguse.</span><span class="sxs-lookup"><span data-stu-id="b5251-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="b5251-110">Üldine toote varude arvestusühik (SKU)</span><span class="sxs-lookup"><span data-stu-id="b5251-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="b5251-111">PowerApps P2 teenuseplaan</span><span class="sxs-lookup"><span data-stu-id="b5251-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="b5251-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="b5251-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="b5251-113">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b5251-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="b5251-114">Microsoft Dynamics 365 plaan, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="b5251-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="b5251-115">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b5251-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="b5251-116">Pange tähele, et erinevad Microsoft Office’i SKU-d annavad samuti selle õiguse lisaks eraldiseisvatele PowerAppsi plaani 2 SKU-dele.</span><span class="sxs-lookup"><span data-stu-id="b5251-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="b5251-117">Oluline on, et üks nendest SKU-dest oleks olemas.</span><span class="sxs-lookup"><span data-stu-id="b5251-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="b5251-118">Avage [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="b5251-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="b5251-119">Looge keskkondi, järgides juhiseid jaotises [Talenti ettevalmistamine](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="b5251-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
