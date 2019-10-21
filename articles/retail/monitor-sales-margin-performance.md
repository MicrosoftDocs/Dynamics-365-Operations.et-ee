---
title: Müügi ja marginaali jõudluse jälgimine
description: Saate Dynamics 365 Retaili abil reaalajas müügi ja marginaali toimimist jälgida.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 46ecefdd15a3a208588aaf630571764047464cdb
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018060"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="9a6a5-103">Müügi ja marginaali jõudluse jälgimine</span><span class="sxs-lookup"><span data-stu-id="9a6a5-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9a6a5-104">Saate Dynamics 365 Retaili abil reaalajas müügi ja marginaali toimimist jälgida.</span><span class="sxs-lookup"><span data-stu-id="9a6a5-104">You can monitor sales and margin performance in real time using Dynamics 365 Retail.</span></span>

<span data-ttu-id="9a6a5-105">Retaili osana saavad kasutajad jälgida müügi ja marginaali toimimist reaalajas organisatsiooni hierarhia erinevate tasandite lõikes järgmiste dimensioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="9a6a5-105">As part of Retail, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="9a6a5-106">Tooted</span><span class="sxs-lookup"><span data-stu-id="9a6a5-106">Products</span></span>
- <span data-ttu-id="9a6a5-107">Kategooriad</span><span class="sxs-lookup"><span data-stu-id="9a6a5-107">Categories</span></span>
- <span data-ttu-id="9a6a5-108">Allahindlused</span><span class="sxs-lookup"><span data-stu-id="9a6a5-108">Discounts</span></span>
- <span data-ttu-id="9a6a5-109">Aastad ajavahemikuna</span><span class="sxs-lookup"><span data-stu-id="9a6a5-109">Years as time period</span></span>
- <span data-ttu-id="9a6a5-110">Registrid/terminalid</span><span class="sxs-lookup"><span data-stu-id="9a6a5-110">Registers/terminals</span></span>
- <span data-ttu-id="9a6a5-111">Personal/töötajad</span><span class="sxs-lookup"><span data-stu-id="9a6a5-111">Staff/employees</span></span>
- <span data-ttu-id="9a6a5-112">Kliendid</span><span class="sxs-lookup"><span data-stu-id="9a6a5-112">Customers</span></span>
- <span data-ttu-id="9a6a5-113">Tootmisüksused</span><span class="sxs-lookup"><span data-stu-id="9a6a5-113">Operating units</span></span>

<span data-ttu-id="9a6a5-114">Lisaks võimaldavad kaks ainulaadset aruannet, milles kasutatakse hierarhilist ruudustikustruktuuri, kasutajatel jälgida müügi ja marginaali toimimist, minnes ülemisest kategooriasõlmest süvitsi eraldi kategooria lehe sõlmede juurde jaetoote vaike-kategooriahierarhias.</span><span class="sxs-lookup"><span data-stu-id="9a6a5-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default retail product category hierarchy.</span></span> <span data-ttu-id="9a6a5-115">Kasutajad saavad minna ka ülemisest tootmisüksusest süvitsi organisatsioonihierarhia eraldi kanalisse, mis on määratletud organisatsiooni vaikehierarhiaks jaemüügi aruandlushierarhia tähenduses.</span><span class="sxs-lookup"><span data-stu-id="9a6a5-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for retail reporting hierarchy purposes.</span></span> <span data-ttu-id="9a6a5-116">Aruanded saab avada järgmistest asukohtadest.</span><span class="sxs-lookup"><span data-stu-id="9a6a5-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="9a6a5-117">Tööruum **Jaekaupluse haldus** &gt; **Jaemüük** &gt; **Kanalid** &gt; **Jaekaupluse haldus** &gt; **Aruanded**</span><span class="sxs-lookup"><span data-stu-id="9a6a5-117">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="9a6a5-118">Tööruum **Kategooria ja toote haldus** &gt; **Jaemüük** &gt; **Tooted ja kategooriad** &gt; **Jaekaupluse haldus** &gt; **Aruanded**</span><span class="sxs-lookup"><span data-stu-id="9a6a5-118">**Category and product management** workspace &gt; **Retail** &gt; **Product and categories** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="9a6a5-119">Tööruum **Hinnakujunduse ja allahindluste haldamine** &gt; **Jaemüük** &gt; **Hinnad ja allahindlused** &gt; **Jaekaupluse haldus** &gt; **Aruanded**</span><span class="sxs-lookup"><span data-stu-id="9a6a5-119">**Pricing and discount management** workspace &gt; **Retail** &gt; **Pricing and discounts** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="9a6a5-120">Jaotis **Päringud ja aruanded** &gt; **Jaemüük** &gt; **Päringud ja aruanded** &gt; **Müügiaruanded**</span><span class="sxs-lookup"><span data-stu-id="9a6a5-120">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>
