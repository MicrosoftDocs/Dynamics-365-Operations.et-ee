---
title: Pärast keskkonna kopeerimist puuduvad tooted ja kategooriad
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui tooted ja kategooriad puuduvad pärast saidi kopeerimist keskkondade vahel või samas keskkonnas.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 4964b9623a91286d4f8260bcae7941feb48f8962
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022394"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="bd8a4-103">Tooted ja kategooriad pärast keskkonna kopeerimist puuduvad</span><span class="sxs-lookup"><span data-stu-id="bd8a4-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd8a4-104">See teema annab tõrkeotsingu juhised, mis aitavad, kui tooted ja kategooriad puuduvad pärast saidi kopeerimist keskkondade vahel või samas keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="bd8a4-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="bd8a4-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="bd8a4-105">Description</span></span>

<span data-ttu-id="bd8a4-106">Kui sait on kopeeritud ühest keskkonnast või samas keskkonnas, puuduvad tooted ja kategooriad saidilt.</span><span class="sxs-lookup"><span data-stu-id="bd8a4-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="bd8a4-107">Tooted ja kategooriad puuduvad e-kaubanduse laost ja e-commerce'i saidilooja **tooted** vahekaardilt.</span><span class="sxs-lookup"><span data-stu-id="bd8a4-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="bd8a4-108">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="bd8a4-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="bd8a4-109">Kanali tootmisüksuse numbri vastendamine äsja kopeeritud saidiga Commerce'i saidi koostajas</span><span class="sxs-lookup"><span data-stu-id="bd8a4-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="bd8a4-110">Kanali tootmisüksuse numbri vastendamine äsja kopeeritud saidiga Commerce'i saidi koostajas, jälgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="bd8a4-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="bd8a4-111">Valige äsja kopeeritud sait.</span><span class="sxs-lookup"><span data-stu-id="bd8a4-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="bd8a4-112">Jaotises **Saidi sätted** valige **Kanalid**.</span><span class="sxs-lookup"><span data-stu-id="bd8a4-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="bd8a4-113">Kanali nime kõrval valige kolmikpunkt (**...**) ja seejärel valige suvand **Muuda võrgupoe kanalit**.</span><span class="sxs-lookup"><span data-stu-id="bd8a4-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="bd8a4-114">Dialoogiboksis **Võrgupoe kanali muutmine** valige kanal, mida vast kopeeritud saidiga vvastendada ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="bd8a4-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="bd8a4-115">Valige käsk **Salvesta ja avalda**.</span><span class="sxs-lookup"><span data-stu-id="bd8a4-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd8a4-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="bd8a4-116">Additional resources</span></span>

[<span data-ttu-id="bd8a4-117">Dynamics 365 Commerce'i saidi seostamine võrgukanaliga</span><span class="sxs-lookup"><span data-stu-id="bd8a4-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)
