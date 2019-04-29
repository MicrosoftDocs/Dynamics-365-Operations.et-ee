---
title: Juurdepääs privaatsetele aadressidele turberolli alusel
description: Selles teemas selgitatakse, kuidas lahendada probleemi, mille käigus kliendil puudub juurdepääs privaatsetele aadressidele.
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
ms.openlocfilehash: f8aaa33e5fda404b48548f9a57977dd0ccd53dc1
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/19/2019
ms.locfileid: "859478"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="623a1-103">Juurdepääs privaatsetele aadressidele turberolli alusel</span><span class="sxs-lookup"><span data-stu-id="623a1-103">Access to private addresses by security role</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="623a1-104">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="623a1-104">**Issue**</span></span>

<span data-ttu-id="623a1-105">Pärast turberolli paljundamist ja uue rollina sisselogimist ei näe klient privaatseks märgitud aadresse.</span><span class="sxs-lookup"><span data-stu-id="623a1-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="623a1-106">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="623a1-106">**Resolution**</span></span>

<span data-ttu-id="623a1-107">Probleemi lahendamiseks peab klient toimima topeltturberolli korral järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="623a1-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="623a1-108">Minge jaotisse **Organisatsiooni haldamine \> Globaalne aadressiraamat \> Globaalse aadressiraamatu parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="623a1-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="623a1-109">Teisaldage vahekaardil **Privaatse asukoha turvalisus** uus turberoll loendist **Saadaolevad rollid** loendisse **Valitud rollid**.</span><span class="sxs-lookup"><span data-stu-id="623a1-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="623a1-110">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="623a1-110">Select **Save**.</span></span>

![Globaalse aadressiraamatu parameetrite leht](media/GAD-parameters.png)
