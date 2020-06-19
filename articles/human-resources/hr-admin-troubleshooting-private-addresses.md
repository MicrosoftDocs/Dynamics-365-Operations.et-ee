---
title: Juurdepääs privaatsetele aadressidele turberolli järgi
description: Selles artiklis selgitatakse, kuidas lahendada probleemi, mille käigus kliendil puudub juurdepääs privaatsetele aadressidele.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
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
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fbe0e8acc1b879e4d7982b33413236432f25f630
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431034"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="64590-103">Juurdepääs privaatsetele aadressidele turberolli alusel</span><span class="sxs-lookup"><span data-stu-id="64590-103">Access to private addresses by security role</span></span>

<span data-ttu-id="64590-104">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="64590-104">**Issue**</span></span>

<span data-ttu-id="64590-105">Pärast turberolli paljundamist ja uue rollina sisselogimist ei näe klient privaatseks märgitud aadresse.</span><span class="sxs-lookup"><span data-stu-id="64590-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="64590-106">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="64590-106">**Resolution**</span></span>

<span data-ttu-id="64590-107">Probleemi lahendamiseks peab klient toimima topeltturberolli korral järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="64590-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="64590-108">Minge jaotisse **Organisatsiooni haldamine \> Globaalne aadressiraamat \> Globaalse aadressiraamatu parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="64590-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="64590-109">Teisaldage vahekaardil **Privaatse asukoha turvalisus** uus turberoll loendist **Saadaolevad rollid** loendisse **Valitud rollid**.</span><span class="sxs-lookup"><span data-stu-id="64590-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="64590-110">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="64590-110">Select **Save**.</span></span>

![Globaalse aadressiraamatu parameetrite leht](media/GAD-parameters.png)
