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
ms.openlocfilehash: 58f3322ad64f7de07e17d193ff665bd6536a4070
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897093"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="1a1f0-103">Juurdepääs privaatsetele aadressidele turberolli alusel</span><span class="sxs-lookup"><span data-stu-id="1a1f0-103">Access to private addresses by security role</span></span>

<span data-ttu-id="1a1f0-104">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="1a1f0-104">**Issue**</span></span>

<span data-ttu-id="1a1f0-105">Pärast turberolli paljundamist ja uue rollina sisselogimist ei näe klient privaatseks märgitud aadresse.</span><span class="sxs-lookup"><span data-stu-id="1a1f0-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="1a1f0-106">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="1a1f0-106">**Resolution**</span></span>

<span data-ttu-id="1a1f0-107">Probleemi lahendamiseks peab klient toimima topeltturberolli korral järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1a1f0-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="1a1f0-108">Minge jaotisse **Organisatsiooni haldamine \> Globaalne aadressiraamat \> Globaalse aadressiraamatu parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1a1f0-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="1a1f0-109">Teisaldage vahekaardil **Privaatse asukoha turvalisus** uus turberoll loendist **Saadaolevad rollid** loendisse **Valitud rollid**.</span><span class="sxs-lookup"><span data-stu-id="1a1f0-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="1a1f0-110">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1a1f0-110">Select **Save**.</span></span>

![Globaalse aadressiraamatu parameetrite leht](media/GAD-parameters.png)
