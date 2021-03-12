---
title: Saate häälestada hooldustellimuse etappe.
description: Seadistage hooldustellimuse etappe.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 9aca699283a9de6ea551bd02184498aed88143e9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991636"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="978de-103">Saate häälestada hooldustellimuse etappe.</span><span class="sxs-lookup"><span data-stu-id="978de-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="978de-104">Klõpsake valikut **Teenuste haldus** \> **Häälestus** \> **Hooldustellimused** \> **Teenuseetapid**.</span><span class="sxs-lookup"><span data-stu-id="978de-104">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="978de-105">Uue kirje loomiseks vajutage klahve CTRL+N.</span><span class="sxs-lookup"><span data-stu-id="978de-105">Press CTRL+N to create a new record.</span></span>

3.  <span data-ttu-id="978de-106">Määrake väljades **Teenuse etapp** ja **Kirjeldus** teenuse etapi ID ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="978de-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="978de-107">Valige etapile vastavad parameetrid.</span><span class="sxs-lookup"><span data-stu-id="978de-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="978de-108">Valige praeguse etapi jaoks ülemetapp või jätke väli **Ülem** tühjaks, kui etapp on etapi seadistuses algetapp.</span><span class="sxs-lookup"><span data-stu-id="978de-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="978de-109">Pärast etapi salvestamist ei saa välja <STRONG>Ülem</STRONG> muuta.</span><span class="sxs-lookup"><span data-stu-id="978de-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="978de-110">Selle asemel saate kirje kustutada ja luua uue kirje erineva valikuga väljal <STRONG>Ülem</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="978de-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="978de-111">Peale selle saate luua üksnes ühe etapi tühja väljaga <STRONG>Ülem</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="978de-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="978de-112">See tähendab, et lubatud on ainult üks algetapp.</span><span class="sxs-lookup"><span data-stu-id="978de-112">That is, only one initial stage is permitted.</span></span></P>


  


