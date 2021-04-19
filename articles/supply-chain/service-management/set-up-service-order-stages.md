---
title: Saate häälestada hooldustellimuse etappe.
description: Seadistage hooldustellimuse etappe.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b6e245b351b66724eedf8e0d1a0ebf0202df857
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824410"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="3a1e4-103">Saate häälestada hooldustellimuse etappe.</span><span class="sxs-lookup"><span data-stu-id="3a1e4-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="3a1e4-104">Avage **Teenuste haldus** \> **Seadistamine** \> **Teenuse tellimused** \> **Teenuseetapid**.</span><span class="sxs-lookup"><span data-stu-id="3a1e4-104">Go to **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="3a1e4-105">Uue kirje loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="3a1e4-105">Select **New** to create a new record.</span></span>

3.  <span data-ttu-id="3a1e4-106">Määrake väljades **Teenuse etapp** ja **Kirjeldus** teenuse etapi ID ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="3a1e4-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="3a1e4-107">Valige etapile vastavad parameetrid.</span><span class="sxs-lookup"><span data-stu-id="3a1e4-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="3a1e4-108">Valige praeguse etapi jaoks ülemetapp või jätke väli **Ülem** tühjaks, kui etapp on etapi seadistuses algetapp.</span><span class="sxs-lookup"><span data-stu-id="3a1e4-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3a1e4-109">Pärast etapi salvestamist ei saa välja <STRONG>Ülem</STRONG> muuta.</span><span class="sxs-lookup"><span data-stu-id="3a1e4-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="3a1e4-110">Selle asemel saate kirje kustutada ja luua uue kirje erineva valikuga väljal <STRONG>Ülem</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="3a1e4-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="3a1e4-111">Peale selle saate luua üksnes ühe etapi tühja väljaga <STRONG>Ülem</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="3a1e4-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="3a1e4-112">See tähendab, et lubatud on ainult üks algetapp.</span><span class="sxs-lookup"><span data-stu-id="3a1e4-112">That is, only one initial stage is permitted.</span></span></P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]