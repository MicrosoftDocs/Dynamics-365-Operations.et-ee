---
title: Hooldustaotluste tüübid
description: Selles teemas selgitatakse, kuidas luua hooldustaotlust tüüpe varahalduses.
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ff80b2f3e23f46467b8a2fe7a2abd805e5e3a20
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808492"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="389ea-103">Hooldustaotluste tüübid</span><span class="sxs-lookup"><span data-stu-id="389ea-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="389ea-104">Hooldustaotluse tüüpe kasutatakse hooldustaotluste kategoriseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="389ea-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="389ea-105">Näiteks võib teil olla hooldustaotluse tüüpe, mis on seotud ennetava hoolduse ja parandava hooldusega.</span><span class="sxs-lookup"><span data-stu-id="389ea-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="389ea-106">Või teil võib olla spetsiaalne hooldustaotluse tüüp, mida kasutatakse varade remondi haldamiseks (depooparandus).</span><span class="sxs-lookup"><span data-stu-id="389ea-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="389ea-107">’Hooldustaotluse tüüp määratleb kuuluvuse hooldustaotluse elutsükli oleku rühma (hooldustaotluse elutsükli mudelisse).</span><span class="sxs-lookup"><span data-stu-id="389ea-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="389ea-108">Hooldustaotluse elutsükli mudelid määratlevad elutsükli olekud, mida saab hooldustaotlusele seada.</span><span class="sxs-lookup"><span data-stu-id="389ea-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="389ea-109">(Hooldustaotluse elutsükli oleku näited: **Loodud**, **Aktiivne** ja **Lõpetatud**.)</span><span class="sxs-lookup"><span data-stu-id="389ea-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="389ea-110">Valige **Varahaldus**\>**Häälestus**\>**Hooldustaotlused**\>**Hooldustaotluse tüübid**.</span><span class="sxs-lookup"><span data-stu-id="389ea-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="389ea-111">Uue hooldustaotluse tüübi loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="389ea-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="389ea-112">Sisestage väljale **Hooldustaotluse tüüp** hooldustaotluse tüübi ID.</span><span class="sxs-lookup"><span data-stu-id="389ea-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="389ea-113">Väljale **Nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="389ea-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="389ea-114">Kiirkaardil **Üldine** väljal **Hooldustaotluse elutsükli mudel** väljal valige hooldustaotluse elutsükli mudel.</span><span class="sxs-lookup"><span data-stu-id="389ea-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="389ea-115">Väljal **Töökäsu tüüp** valige töökäsu tüüp.</span><span class="sxs-lookup"><span data-stu-id="389ea-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="389ea-116">Kui hooldustaotlus teisendatakse töökäsuks, saab töökäsu automaatselt töökäsu tüübi, mis on seotud hooldustaotluse tüübiga.</span><span class="sxs-lookup"><span data-stu-id="389ea-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="389ea-117">Järgnev illustratsioon näitab lehe **Hooldustaotluse tüübid** näidet.</span><span class="sxs-lookup"><span data-stu-id="389ea-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Hooldusnõuete tüüpide leht](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]