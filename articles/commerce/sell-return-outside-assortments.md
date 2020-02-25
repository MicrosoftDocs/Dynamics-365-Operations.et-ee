---
title: Kaupluse sortimenti mittekuuluvate toodete müümine ja tagastamine
description: Rakendusega Dynamics 365 Commerce saate müüa ja tagastada tooteid väljaspool sortimenti.
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 86c6ecf9ef67ca3ac4ed3c44d930acaa965112b6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022284"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a><span data-ttu-id="71151-103">Kaupluse sortimenti mittekuuluvate toodete müümine ja tagastamine</span><span class="sxs-lookup"><span data-stu-id="71151-103">Sell and return products that aren't part of a store's assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="71151-104">Iga jaemüüja tavapärane stsenaarium on müüa tooteid oma klientidele või võtta vastu tagastusi oma klientidelt, isegi, kui neil pole kaupluses neid kindlaid tooteid (teisisõnu tooted pole kaupluse sortimendis).</span><span class="sxs-lookup"><span data-stu-id="71151-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don't carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>

<span data-ttu-id="71151-105">Tüüpilised stsenaariumid on näiteks järgmised.</span><span class="sxs-lookup"><span data-stu-id="71151-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="71151-106">Jaemüüja ei hoia kõiki oma tooteid kindlas kaupluses.</span><span class="sxs-lookup"><span data-stu-id="71151-106">A retailer doesn't carry all its products in a specific store.</span></span> <span data-ttu-id="71151-107">Ülejäänud tooteid hoitakse laos.</span><span class="sxs-lookup"><span data-stu-id="71151-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="71151-108">Kaupluse töötaja võib aidata klienti, otsides või sirvides laos tooteid, lisada neid ostukorvi ja maksta, valides tarneviisi, näiteks tarnimise laost teatud aadressile või lastes kliendil võtta toote peale sellest laost või teisest laost.</span><span class="sxs-lookup"><span data-stu-id="71151-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="71151-109">Jaemüüjal ei ole kindlaid tooteid kaupluses või tal pole neid varudes kaupluses, mida klient külastas, kuid tooted on saadaval teistes kauplustes.</span><span class="sxs-lookup"><span data-stu-id="71151-109">A retailer doesn't carry specific products in the store or doesn't have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="71151-110">Kaupluse töötaja saab aidata klienti, otsides või sirvides teises kaupluses olevaid tooteid, lisada neid ostukorvi ja teha maksmise, valides tarneviisi.</span><span class="sxs-lookup"><span data-stu-id="71151-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="71151-111">Jaemüüjal on konkreetses linnas või sihtnumbril ja nende ümbruses palju kauplusi ning ta ei soovi sundida kliente tagastama tooteid samasse kauplusse, kust need osteti.</span><span class="sxs-lookup"><span data-stu-id="71151-111">A retailer has many stores in and around a specific city or zip code and doesn't want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="71151-112">Selle asemel võivad kliendid tagastada tooteid ükskõik millisesse kauplusse.</span><span class="sxs-lookup"><span data-stu-id="71151-112">Instead, customers can return products to any store.</span></span>

<span data-ttu-id="71151-113">Need üldised stsenaariumid on saadaval jaemüüjate puhul, kes kasutavad rakendust Commerce.</span><span class="sxs-lookup"><span data-stu-id="71151-113">Those common scenarios are available for retailers using Commerce.</span></span> <span data-ttu-id="71151-114">Commerce’iga saab teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="71151-114">With Commerce, you can:</span></span>

+ <span data-ttu-id="71151-115">Otsida või sirvida tooteid teistes kauplustes.</span><span class="sxs-lookup"><span data-stu-id="71151-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="71151-116">Otsida või sirvida kõiki väljastatud tooteid.</span><span class="sxs-lookup"><span data-stu-id="71151-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="71151-117">Koostada sularahatehinguid või kliendi tellimusi.</span><span class="sxs-lookup"><span data-stu-id="71151-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="71151-118">Valida kliendi tellimustele tarnevõimalusi.</span><span class="sxs-lookup"><span data-stu-id="71151-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="71151-119">Võtta tooteid peale praegusest või mõnest muust kauplusest.</span><span class="sxs-lookup"><span data-stu-id="71151-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="71151-120">Tühistada tellimuse praeguses kaupluses või mõnes muus kaupluses.</span><span class="sxs-lookup"><span data-stu-id="71151-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="71151-121">Tagastada tellimuse kviitungiga või ilma praegusesse või teise kauplusse.</span><span class="sxs-lookup"><span data-stu-id="71151-121">Return an order with or without the receipt at the current store or another store.</span></span>