---
title: Kaupluset ei kuvata kaupluste loendis, kuhu saab järele minna
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui kaupluset ei kuvata kaupluste loendis, kust kaubad saab peale võtta.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9974b3e10bbdcd2e8a8723a3be4b70401bb9e546
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801599"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="245db-103">Kaupluset ei kuvata kaupluste loendis, kuhu saab järele minna</span><span class="sxs-lookup"><span data-stu-id="245db-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="245db-104">See teema annab tõrkeotsingu juhised, mis aitavad, kui kaupluset ei kuvata kaupluste loendis, kust kaubad saab peale võtta.</span><span class="sxs-lookup"><span data-stu-id="245db-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="245db-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="245db-105">Description</span></span>

<span data-ttu-id="245db-106">Jaekauplust ei kuvata kaupluste loendis, kust kaubad saab peale võtta.</span><span class="sxs-lookup"><span data-stu-id="245db-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="245db-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="245db-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="245db-108">Konfigureerige poe aadressi pikkus- ja laiuskraad Commerce Headquarters\`is</span><span class="sxs-lookup"><span data-stu-id="245db-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="245db-109">Konfigureerige poe aadressi pikkus- ja laiuskraadid Commerce Headquarters\`is, järgides järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="245db-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="245db-110">Minge jaotisse **Jaemüük ja kaubandus \> Kanalid \> Kauplused \> Kõik kauplused**.</span><span class="sxs-lookup"><span data-stu-id="245db-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="245db-111">Otsige kauplust, mida soovite kuvada e-ärisaidil järele minemise kohana.</span><span class="sxs-lookup"><span data-stu-id="245db-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="245db-112">Tehke märkus selle **tootmisüksuse numbri** väärtuse kohta.</span><span class="sxs-lookup"><span data-stu-id="245db-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="245db-113">Avage **Organisatsiooni haldamine \> Organisatsioonid \> Tootmisüksused**.</span><span class="sxs-lookup"><span data-stu-id="245db-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="245db-114">Otsige varem märgitud tootmisüksuse numbrit ja seejärel valige otsingutulemustest tootmisüksus.</span><span class="sxs-lookup"><span data-stu-id="245db-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="245db-115">Valige **Aadressid** kiirkaardil suvand **Veel võimalusi** ja siis valige **Täpsem**.</span><span class="sxs-lookup"><span data-stu-id="245db-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="245db-116">Veenduge, et **Üldine** kiirkaardil oleks **Pikkuskraad** ja **Laiuskraad** õigesti seadistatud.</span><span class="sxs-lookup"><span data-stu-id="245db-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="245db-117">Selle sammu osana veenduge, et väärtused on õigesti määratud positiivsete või negatiivsete numbritena.</span><span class="sxs-lookup"><span data-stu-id="245db-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="245db-118">Täitmisgruppide konfigureerimine Commerce Headquarters\`is</span><span class="sxs-lookup"><span data-stu-id="245db-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="245db-119">Commerce headquarters\`is kannete redigeerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="245db-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="245db-120">Avage **Jaemüük ja kaubandus \> Kanalid \> Veebipoed**.</span><span class="sxs-lookup"><span data-stu-id="245db-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="245db-121">Valige konfigureerimiseks võrgupood.</span><span class="sxs-lookup"><span data-stu-id="245db-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="245db-122">Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Täitmisgrupi määramine**.</span><span class="sxs-lookup"><span data-stu-id="245db-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="245db-123">Lehel **Täitmisgrupi määramine** valige veebipoe jaoks täitmisgrupp.</span><span class="sxs-lookup"><span data-stu-id="245db-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="245db-124">Veenduge et jaotises **Seadista** oleks jaekauplus õigesti konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="245db-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="245db-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="245db-125">Additional resources</span></span> 

[<span data-ttu-id="245db-126">Tootmisüksuse loomine</span><span class="sxs-lookup"><span data-stu-id="245db-126">Create an operating unit</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[<span data-ttu-id="245db-127">Võrgukanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="245db-127">Set up an online channel</span></span>](../channel-setup-online.md)
