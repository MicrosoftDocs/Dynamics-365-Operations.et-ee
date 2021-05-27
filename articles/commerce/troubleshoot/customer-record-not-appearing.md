---
title: Kliendikirjeid ei kuvata Commerce headquarters`is
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui kliendikirjeid ei kuvata kohe Commerce Headquarters`is.
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
ms.openlocfilehash: b8d065dd104df616ba8f10f7813e74c900fdcf77
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018478"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="e1d2f-103">Kliendikirjeid ei kuvata Commerce headquarters\`is</span><span class="sxs-lookup"><span data-stu-id="e1d2f-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1d2f-104">See teema annab tõrkeotsingu juhised, mis aitavad, kui kliendikirjeid ei kuvata kohe Commerce Headquarters\`is.</span><span class="sxs-lookup"><span data-stu-id="e1d2f-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="e1d2f-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e1d2f-105">Description</span></span>

<span data-ttu-id="e1d2f-106">Kui loote uue kliendi kirje kasutades registreerumisvoogu e-äris, ei kuvata vastavat kliendikirjet kohe Commerce Headquarters\`is.</span><span class="sxs-lookup"><span data-stu-id="e1d2f-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="e1d2f-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="e1d2f-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="e1d2f-108">Kliendi loomise keelamine asünkroonimisrežiimis</span><span class="sxs-lookup"><span data-stu-id="e1d2f-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e1d2f-109">Kui keelate asünkroonse kliendi loomise, võib see mõjutada süsteemi jõudlust, sest iga kirje loomine loob Commerce Headquarters\`ile reaalajas taotluse.</span><span class="sxs-lookup"><span data-stu-id="e1d2f-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="e1d2f-110">Kui Commerce headquarters ei püsi (nt voogude hooldamisel), luuakse iga uue kliendi loomise voogu tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="e1d2f-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="e1d2f-111">Kliendi loomise keelamiseks asükroonses režiimis Commerce headquarters\`is, järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="e1d2f-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e1d2f-112">Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Funktsiooniprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="e1d2f-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="e1d2f-113">Kui te ei kasuta juba oma võrgukanali jaoks funktsiooniprofiili, looge üks.</span><span class="sxs-lookup"><span data-stu-id="e1d2f-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="e1d2f-114">Veenduge, et suvand **Loo klient asünkroonses režiimis** oleks seatud väärtusele **Ei**.</span><span class="sxs-lookup"><span data-stu-id="e1d2f-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="e1d2f-115">Avage **Jaemüük ja kaubandus \> Kanalid \> Veebipoed**.</span><span class="sxs-lookup"><span data-stu-id="e1d2f-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="e1d2f-116">Valige võrgupood, mille asünkroonse kliendi loomise keelata.</span><span class="sxs-lookup"><span data-stu-id="e1d2f-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="e1d2f-117">Vahekaardil **Üldine** veenduge, et **Funktsiooniprofiil** väli on seadistatud funktsiooniprofiilile, mida kasutate oma võrgukanalil.</span><span class="sxs-lookup"><span data-stu-id="e1d2f-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1d2f-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e1d2f-118">Additional resources</span></span>

[<span data-ttu-id="e1d2f-119">B2C-rentniku häälestus Commerce'is</span><span class="sxs-lookup"><span data-stu-id="e1d2f-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
