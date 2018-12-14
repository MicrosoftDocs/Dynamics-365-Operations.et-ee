---
title: "Kasutajal on juurdepääs Core HR-ile, aga mitte rakendusele Onboard või Attract"
description: "Selles teemas selgitatakse, kuidas lahendada probleemi, mille käigus kasutajal on juurdepääs rakenduse Microsoft Dynamics 365 for Talent Core HR-ile, aga mitte rakendusele Onboard või Attract."
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
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: et-ee
ms.lasthandoff: 12/04/2018

---

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="14711-103">Kasutajal on juurdepääs Core HR-ile, aga mitte rakendusele Onboard või Attract</span><span class="sxs-lookup"><span data-stu-id="14711-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="14711-104">**Keskkonna üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="14711-104">**Environment details**</span></span>

- <span data-ttu-id="14711-105">Microsoft Dynamicsi teenuse Lifecycle Services (LCS) juurutamise viis läbi kasutaja A.</span><span class="sxs-lookup"><span data-stu-id="14711-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="14711-106">Kasutaja A lisas kasutaja B kasutajana rakenduse Microsoft Dynamics 365 for Talent Core HR-i.</span><span class="sxs-lookup"><span data-stu-id="14711-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="14711-107">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="14711-107">**Issue**</span></span>

<span data-ttu-id="14711-108">Kasutaja B-l on juurdepääs Core HR-ile, aga mitte rakendusele Talent: Attract või Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="14711-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="14711-109">Valiku **Kogemuse rakendused** tegemisel suunatakse kasutaja selle asemel proovikeskkonda.</span><span class="sxs-lookup"><span data-stu-id="14711-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="14711-110">**Lahendus**</span><span class="sxs-lookup"><span data-stu-id="14711-110">**Solution**</span></span>

<span data-ttu-id="14711-111">Kasutajale B peavad olema määratud õigused vaadata Microsoft PowerAppsi keskkonda, mida kasutaja A ettevalmistusprotsessi ajal lõi.</span><span class="sxs-lookup"><span data-stu-id="14711-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="14711-112">Lisateavet vt jaotisest Keskkonnale juurdepääsu andmine lehel [Talenti ettevalmistamine](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="14711-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="14711-113">**Pikaajaline lahendus**</span><span class="sxs-lookup"><span data-stu-id="14711-113">**Long-term solution**</span></span>

<span data-ttu-id="14711-114">Kui Core HR-i lisatakse kasutaja, kaalub Microsoft rakendustele Onboard ja Attract asjakohaste õiguste automaatset määramist.</span><span class="sxs-lookup"><span data-stu-id="14711-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>

