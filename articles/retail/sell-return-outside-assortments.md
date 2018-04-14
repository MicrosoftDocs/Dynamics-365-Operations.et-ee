---
title: "Toodete müümine ja tagastamine väljaspool sortimenti"
description: "Dynamics 365 for Retaili puhul võite müüa ja tagastada tooteid väljaspool sortimente."
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8d2188ddac937ab373315759b89ecf85c0b7e007
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="sell-and-return-products-outside-of-an-assortment"></a><span data-ttu-id="83d6c-103">Toodete müümine ja tagastamine väljaspool sortimenti</span><span class="sxs-lookup"><span data-stu-id="83d6c-103">Sell and return products outside of an assortment</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="83d6c-104">Iga jaemüüja tavapärane stsenaarium on müüa tooteid oma klientidele või võtta vastu tagastusi oma klientidelt, isegi kui neil pole kaupluses neid kindlaid tooteid (teisisõnu tooteid pole kaupluse sortimendis).</span><span class="sxs-lookup"><span data-stu-id="83d6c-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don’t carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>
<span data-ttu-id="83d6c-105">Tüüpilised stsenaariumid on näiteks järgmised.</span><span class="sxs-lookup"><span data-stu-id="83d6c-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="83d6c-106">Jaemüüja ei hoia kõiki oma tooteid kindlas kaupluses.</span><span class="sxs-lookup"><span data-stu-id="83d6c-106">A retailer doesn’t carry all its products in a specific store.</span></span> <span data-ttu-id="83d6c-107">Ülejäänud tooteid hoitakse laos.</span><span class="sxs-lookup"><span data-stu-id="83d6c-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="83d6c-108">Kaupluse töötaja võib aidata klienti, otsides või sirvides laos tooteid, lisada neid ostukorvi ja maksta, valides tarneviisi, näiteks tarnimise laost teatud aadressile või lastes kliendil võtta toote peale sellest laost või teisest laost.</span><span class="sxs-lookup"><span data-stu-id="83d6c-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="83d6c-109">Jaemüüjal ei ole kindlaid tooteid kaupluses või tal pole neid varudes kaupluses, mida klient külastas, kuid tooted on saadaval teistes kauplustes.</span><span class="sxs-lookup"><span data-stu-id="83d6c-109">A retailer doesn’t carry specific products in the store or doesn’t have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="83d6c-110">Kaupluse töötaja saab aidata klienti, otsides või sirvides teises kaupluses olevaid tooteid, lisada neid ostukorvi ja teha maksmise, valides tarneviisi.</span><span class="sxs-lookup"><span data-stu-id="83d6c-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="83d6c-111">Jaemüüjal on konkreetses linnas või sihtnumbril ja nende ümbruses palju kauplusi ning ta ei soovi sundida kliente tagastama tooteid samasse kauplusse, kust need osteti.</span><span class="sxs-lookup"><span data-stu-id="83d6c-111">A retailer has many stores in and around a specific city or zip code and doesn’t want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="83d6c-112">Selle asemel võivad kliendid tagastada tooteid ükskõik millisesse kauplusse.</span><span class="sxs-lookup"><span data-stu-id="83d6c-112">Instead, customers can return products to any store.</span></span>


<span data-ttu-id="83d6c-113">Need üldised stsenaariumid on saadaval jaemüüjate puhul, kes kasutavad rakendust Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="83d6c-113">Those common scenarios are available for retailers using Dynamics 365 for Retail.</span></span> <span data-ttu-id="83d6c-114">Retailiga saab teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="83d6c-114">With Retail, you can:</span></span>
+ <span data-ttu-id="83d6c-115">Otsida või sirvida tooteid teistes kauplustes.</span><span class="sxs-lookup"><span data-stu-id="83d6c-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="83d6c-116">Otsida või sirvida kõiki väljastatud tooteid.</span><span class="sxs-lookup"><span data-stu-id="83d6c-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="83d6c-117">Koostada sularahatehinguid või kliendi tellimusi.</span><span class="sxs-lookup"><span data-stu-id="83d6c-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="83d6c-118">Valida kliendi tellimustele tarnevõimalusi.</span><span class="sxs-lookup"><span data-stu-id="83d6c-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="83d6c-119">Võtta tooteid peale praegusest või mõnest muust kauplusest.</span><span class="sxs-lookup"><span data-stu-id="83d6c-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="83d6c-120">Tühistada tellimuse praeguses kaupluses või mõnes muus kaupluses.</span><span class="sxs-lookup"><span data-stu-id="83d6c-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="83d6c-121">Tagastada tellimuse kviitungiga või ilma praegusesse või teise kauplusse.</span><span class="sxs-lookup"><span data-stu-id="83d6c-121">Return an order with or without the receipt at the current store or another store.</span></span>

