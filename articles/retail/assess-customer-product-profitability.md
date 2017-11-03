---
title: Kliendi ja toote tulususe hindamine
description: "See artikkel selgitab, kuidas kasutada mälusisest ja reaalajas analüüsi kliendi ja toote kasumlikkuse vaatamiseks, uurimiseks ja selle kohta ülevaate saamiseks Microsoft Dynamics 365 for Retaili andmetest."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 04ebc624212e6909eda7589b71cd84a22010e721
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="1c4bd-103">Kliendi ja toote tulususe hindamine</span><span class="sxs-lookup"><span data-stu-id="1c4bd-103">Assess customer and product profitability</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="1c4bd-104">See artikkel selgitab, kuidas kasutada mälusisest ja reaalajas analüüsi kliendi ja toote kasumlikkuse vaatamiseks, uurimiseks ja selle kohta ülevaate saamiseks Microsoft Dynamics 365 for Retaili andmetest.</span><span class="sxs-lookup"><span data-stu-id="1c4bd-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span> 

<span data-ttu-id="1c4bd-105">Microsoft Dynamics 365 for Retaili osana saavad kasutajad analüüsida parimate klientide (10–100) tulusust organisatsiooni hierarhia erinevatel tasemetel ühe alljärgneva kriteeriumi põhjal:</span><span class="sxs-lookup"><span data-stu-id="1c4bd-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="1c4bd-106">Müügisumma</span><span class="sxs-lookup"><span data-stu-id="1c4bd-106">Sales amount</span></span>
-   <span data-ttu-id="1c4bd-107">Kogus</span><span class="sxs-lookup"><span data-stu-id="1c4bd-107">Quantity</span></span>
-   <span data-ttu-id="1c4bd-108">Kogutulu marginaal</span><span class="sxs-lookup"><span data-stu-id="1c4bd-108">Gross profit margin</span></span>
-   <span data-ttu-id="1c4bd-109">Marginaali protsent</span><span class="sxs-lookup"><span data-stu-id="1c4bd-109">Margin percentage</span></span>

<span data-ttu-id="1c4bd-110">Selle hinnangu jaoks saate kasutada **parimate klientide** valmisaruandeid, mille saate avada ühtest järgmistest asukohtadest:</span><span class="sxs-lookup"><span data-stu-id="1c4bd-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="1c4bd-111">Tööruum **Jaekaupluse haldus** &gt; **Jaemüük** &gt; **Kanalid** &gt; **Jaekaupluse haldus** &gt; **Aruanded** &gt; **Parimate klientide aruanne**</span><span class="sxs-lookup"><span data-stu-id="1c4bd-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
-   <span data-ttu-id="1c4bd-112">Jaotis **Päringud ja aruanded** &gt; **Jaemüük** &gt; **Päringud ja aruanded** &gt; **Müügiaruanded** &gt; **Parimate klientide aruanne**</span><span class="sxs-lookup"><span data-stu-id="1c4bd-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="1c4bd-113">Samuti saavad kasutajad analüüsida peamiste toodete (10–100) tulusust organisatsiooni hierarhia erinevatel tasemetel ühe alljärgneva kriteeriumi põhjal:</span><span class="sxs-lookup"><span data-stu-id="1c4bd-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="1c4bd-114">Müügisumma</span><span class="sxs-lookup"><span data-stu-id="1c4bd-114">Sales amount</span></span>
-   <span data-ttu-id="1c4bd-115">Kogus</span><span class="sxs-lookup"><span data-stu-id="1c4bd-115">Quantity</span></span>
-   <span data-ttu-id="1c4bd-116">Kogutulu marginaal</span><span class="sxs-lookup"><span data-stu-id="1c4bd-116">Gross profit margin</span></span>
-   <span data-ttu-id="1c4bd-117">Marginaali protsent</span><span class="sxs-lookup"><span data-stu-id="1c4bd-117">Margin percentage</span></span>

<span data-ttu-id="1c4bd-118">Selle hinnangu jaoks saate kasutada **peamiste toodete** valmisaruandeid, mille saate avada ühest järgmistest asukohtadest:</span><span class="sxs-lookup"><span data-stu-id="1c4bd-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="1c4bd-119">Tööruum **Jaekaupluse haldus** &gt; **Jaemüük** &gt; **Kanalid** &gt; **Jaekaupluse haldus** &gt; **Aruanded** &gt; **Peamiste toodete aruanne**</span><span class="sxs-lookup"><span data-stu-id="1c4bd-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="1c4bd-120">Tööruum **Kategooria ja toote haldus** &gt; **Jaemüük** &gt; **Tooted ja kategooriad** &gt; **Jaekaupluse haldus** &gt; **Aruanded** &gt; **Peamiste toodete aruanne**</span><span class="sxs-lookup"><span data-stu-id="1c4bd-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="1c4bd-121">Jaotis **Päringud ja aruanded** &gt; **Jaemüük** &gt; **Päringud ja aruanded** &gt; **Müügiaruanded** &gt; **Peamiste toodete aruanne**</span><span class="sxs-lookup"><span data-stu-id="1c4bd-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>




