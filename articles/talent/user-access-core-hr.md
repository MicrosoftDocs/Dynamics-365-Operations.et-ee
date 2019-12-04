---
title: Kasutaja pääseb ligi Core HR-ile, aga mitte rakendusele Onboard või Attract
description: Selles teemas selgitatakse, kuidas lahendada probleemi, mille käigus kasutajal on juurdepääs rakenduse Microsoft Dynamics 365 Talent Core HR-ile, aga mitte rakendusele Attract või Onboard.
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
ms.openlocfilehash: 1a86936d756d8375761ce50c9d9bf33dc638dfad
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772915"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a><span data-ttu-id="363f7-103">Kasutaja pääseb ligi Core HR-ile, aga mitte rakendusele Onboard või Attract</span><span class="sxs-lookup"><span data-stu-id="363f7-103">User can access Core HR but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="363f7-104">**Keskkonna üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="363f7-104">**Environment details**</span></span>

- <span data-ttu-id="363f7-105">Teenuse Microsoft Dynamics Lifecycle Services (LCS) juurutamise viis läbi kasutaja A.</span><span class="sxs-lookup"><span data-stu-id="363f7-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="363f7-106">Kasutaja A lisas kasutaja B kasutajana rakenduse Microsoft Dynamics 365 Talent: Core HR-i.</span><span class="sxs-lookup"><span data-stu-id="363f7-106">User A added user B as a user to Microsoft Dynamics 365 Talent: Core HR.</span></span>

<span data-ttu-id="363f7-107">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="363f7-107">**Issue**</span></span>

<span data-ttu-id="363f7-108">Kasutaja B-l on juurdepääs Core HR-ile, aga mitte rakendusele Talent: Attract või Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="363f7-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="363f7-109">Valiku **Kogemuse rakendused** tegemisel suunatakse kasutaja selle asemel proovikeskkonda.</span><span class="sxs-lookup"><span data-stu-id="363f7-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="363f7-110">**Lahendus**</span><span class="sxs-lookup"><span data-stu-id="363f7-110">**Solution**</span></span>

<span data-ttu-id="363f7-111">Kasutajale B peavad olema määratud õigused vaadata Microsoft Power Appsi keskkonda, mille kasutaja A ettevalmistusprotsessi ajal lõi.</span><span class="sxs-lookup"><span data-stu-id="363f7-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="363f7-112">Lisateavet vt jaotisest Keskkonnale juurdepääsu andmine lehel [Talenti ettevalmistamine](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="363f7-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="363f7-113">**Pikaajaline lahendus**</span><span class="sxs-lookup"><span data-stu-id="363f7-113">**Long-term solution**</span></span>

<span data-ttu-id="363f7-114">Kui Core HR-i lisatakse kasutaja, kaalub Microsoft rakendustele Onboard ja Attract asjakohaste õiguste automaatset määramist.</span><span class="sxs-lookup"><span data-stu-id="363f7-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
