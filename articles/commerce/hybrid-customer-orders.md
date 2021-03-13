---
title: Hübriid-klienditellimused
description: Hübriid-klienditellimus on üksik tellimus, mis sisaldab tooteid, mille klient saab kauplusest kaasa võtta, ja tooteid, mis hiljem peale võetakse või välja saadetakse.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bec8389645a06a8287e51195341909ec71a8af2b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009689"
---
# <a name="hybrid-customer-orders"></a><span data-ttu-id="22679-103">Hübriid-klienditellimused</span><span class="sxs-lookup"><span data-stu-id="22679-103">Hybrid customer orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="22679-104">Hübriid-klienditellimus on üksik tellimus, mis sisaldab tooteid, mille klient saab kauplusest kaasa võtta, ja tooteid, mis hiljem peale võetakse või välja saadetakse.</span><span class="sxs-lookup"><span data-stu-id="22679-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="22679-105">Commerce'is saate valida kas klienditellimuse kõigi toodete tarnimise või kliendi tellimuse valitud toodete tarnimise.</span><span class="sxs-lookup"><span data-stu-id="22679-105">In Commerce, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="22679-106">Tarnimiseks märgitud tooteridade eest esitatakse arve pärast tellimuse loomist automaatselt, sama toimub ka tellimuse puhul, mis võetakse peale pärast tellimuse loomist.</span><span class="sxs-lookup"><span data-stu-id="22679-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="22679-107">Hübriidtellimuste eest tasumisele kuuluv summa määratakse, lisades deposiidiprotsendi komplekteeritavate ja lähetatavate toodete ridadele koos tarneridade täieliku summaga.</span><span class="sxs-lookup"><span data-stu-id="22679-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="22679-108">Hübriid-tellimuste puhul vahetab süsteem kliendi tellimuse režiimi ja sularaharežiimi järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="22679-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

- <span data-ttu-id="22679-109">Kui kõigi ostukorvis olevate toodete puhul on tarneviisiks määratud **Sularahatarne**, siis käsitletakse kannet sularahakandena.</span><span class="sxs-lookup"><span data-stu-id="22679-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
- <span data-ttu-id="22679-110">Kui mõnele ostukorvi reale on määratud **Komplekteeri** või **läheta tarne**, siis käsitletakse tellimust kliendi tellimuse kandena.</span><span class="sxs-lookup"><span data-stu-id="22679-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="22679-111">Kui on valitud ostukorvi rida ja **Komplekteeri valitud**, **Saada valitud** või **Tarni valitud**, siis määratakse selle tarneviisiga ainult konkreetne ostukorvi rida.</span><span class="sxs-lookup"><span data-stu-id="22679-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="22679-112">Sellisel juhul jätkub toimingu allavoolu voog tavalisel viisil.</span><span class="sxs-lookup"><span data-stu-id="22679-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="22679-113">Kuid kui on valitud **Komplekteeri valitud**, **Saada valitud** või **Tarni valitud** ja ostukorvi rida ei valita, siis avaneb uus leht, millel on loetletud kõik ostukorvi read.</span><span class="sxs-lookup"><span data-stu-id="22679-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="22679-114">Sellel ekraanil saate valida korraga mitu rida tarneviisi määramiseks.</span><span class="sxs-lookup"><span data-stu-id="22679-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="22679-115">Kui kasutate ridade valimiseks seda meetodit, siis tühistatakse mis tahes reale eelnevalt määratud tarneviis.</span><span class="sxs-lookup"><span data-stu-id="22679-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22679-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="22679-116">Additional resources</span></span>

[<span data-ttu-id="22679-117">Kliendi tellimused Modern POS-is (MPOS-is)</span><span class="sxs-lookup"><span data-stu-id="22679-117">Customer orders in Modern POS (MPOS)</span></span>](customer-orders-overview.md)
