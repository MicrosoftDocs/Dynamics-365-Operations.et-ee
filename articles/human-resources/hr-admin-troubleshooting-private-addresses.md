---
title: Juurdepääs privaatsetele aadressidele turberolli järgi
description: Selles artiklis selgitatakse, kuidas lahendada probleemi, mille käigus kliendil puudub juurdepääs privaatsetele aadressidele.
author: andreabichsel
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2edcef338f0ff8fcf231d4314fc972284397d000
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053319"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="ed9bb-103">Juurdepääs privaatsetele aadressidele turberolli alusel</span><span class="sxs-lookup"><span data-stu-id="ed9bb-103">Access to private addresses by security role</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ed9bb-104">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="ed9bb-104">**Issue**</span></span>

<span data-ttu-id="ed9bb-105">Pärast turberolli paljundamist ja uue rollina sisselogimist ei näe klient privaatseks märgitud aadresse.</span><span class="sxs-lookup"><span data-stu-id="ed9bb-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="ed9bb-106">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="ed9bb-106">**Resolution**</span></span>

<span data-ttu-id="ed9bb-107">Probleemi lahendamiseks peab klient toimima topeltturberolli korral järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ed9bb-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="ed9bb-108">Minge jaotisse **Organisatsiooni haldamine \> Globaalne aadressiraamat \> Globaalse aadressiraamatu parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="ed9bb-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="ed9bb-109">Teisaldage vahekaardil **Privaatse asukoha turvalisus** uus turberoll loendist **Saadaolevad rollid** loendisse **Valitud rollid**.</span><span class="sxs-lookup"><span data-stu-id="ed9bb-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="ed9bb-110">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ed9bb-110">Select **Save**.</span></span>

![Globaalse aadressiraamatu parameetrite leht](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]