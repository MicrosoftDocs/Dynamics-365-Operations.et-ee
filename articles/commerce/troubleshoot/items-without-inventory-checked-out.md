---
title: Laota kaupu saab välja registreerida
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui kliendid saavad lisada ostukorvi laost väljas kaupu ja jätkata väljaregistreerimist.
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
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018454"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="2c00a-103">Laota kaupu saab välja registreerida</span><span class="sxs-lookup"><span data-stu-id="2c00a-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c00a-104">See teema annab tõrkeotsingu juhised, mis aitavad, kui kliendid saavad lisada ostukorvi laost väljas kaupu ja jätkata väljaregistreerimist.</span><span class="sxs-lookup"><span data-stu-id="2c00a-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="2c00a-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2c00a-105">Description</span></span>

<span data-ttu-id="2c00a-106">Kasutajad saavad lisada ostukorvi kauba, kuigi kaupluses puudub vaba kaubavaru, ja siis siirduge väljaregistreerimise lehele.</span><span class="sxs-lookup"><span data-stu-id="2c00a-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="2c00a-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="2c00a-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="2c00a-108">Commerce'i saidi koostajas laotõrgete näitamise lubamine</span><span class="sxs-lookup"><span data-stu-id="2c00a-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="2c00a-109">Commerce'i saidi koostajas **laotõrgete näitamise** lubamine, jälgi neid samme.</span><span class="sxs-lookup"><span data-stu-id="2c00a-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2c00a-110">Valige sait, millel te töötate.</span><span class="sxs-lookup"><span data-stu-id="2c00a-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="2c00a-111">Valige vasakpoolsel navigeerimispaanil suvand **Lehed**.</span><span class="sxs-lookup"><span data-stu-id="2c00a-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="2c00a-112">Valige **CartPage** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="2c00a-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="2c00a-113">Valige ostukorvi **1 pesa**, sealt valige käsk **redigeeri** ja siis valige atribuutide paanil märkeruut **Näita laotõrkeid**.</span><span class="sxs-lookup"><span data-stu-id="2c00a-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="2c00a-114">Salvestage ja avaldage leht.</span><span class="sxs-lookup"><span data-stu-id="2c00a-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c00a-115">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2c00a-115">Additional resources</span></span>

[<span data-ttu-id="2c00a-116">Varude sätete rakendamine</span><span class="sxs-lookup"><span data-stu-id="2c00a-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="2c00a-117">Varude saadavuse arvutamine jaemüügikanalite jaoks</span><span class="sxs-lookup"><span data-stu-id="2c00a-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="2c00a-118">Varude puhvrite ja varude tasemete konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2c00a-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
