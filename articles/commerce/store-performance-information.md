---
title: Kaupluse jõudluse analüüsimine
description: See artikkel selgitab, kuidas kasutada mälusisest ja reaalajas analüüsi kaupluse tulemuste vaatamiseks, uurimiseks ja nende kohta ülevaate saamiseks Dynamics 365 Commercei andmete põhjal.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, RetailChannelManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8d95bb0927de5a1906efe180cb9e725c380a724f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411744"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="bf5b6-103">Kaupluse jõudluse analüüsimine</span><span class="sxs-lookup"><span data-stu-id="bf5b6-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bf5b6-104">See artikkel selgitab, kuidas kasutada mälusisest ja reaalajas analüüsi kaupluse tulemuste vaatamiseks, uurimiseks ja nende kohta ülevaate saamiseks Dynamics 365 Commercei andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="bf5b6-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="bf5b6-105">Kasutajad saavadi osana uurida kaupluse jõudlust reaalajas organisatsiooni hierarhia erinevatel tasanditel valitud perioodil, avades valmisaruande **Kanali kokkuvõte** ühest järgmistest asukohtadest.</span><span class="sxs-lookup"><span data-stu-id="bf5b6-105">As part of Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="bf5b6-106">Tööruum **Jaekaupluse haldus** &gt; **Jaemüük** &gt; **Kanalid** &gt; **Jaekaupluse haldus** &gt; **Aruanded** &gt; **Kanali koondaruanne**</span><span class="sxs-lookup"><span data-stu-id="bf5b6-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="bf5b6-107">Tööruum **Jaekaupluse rahandus** &gt; **Jaemüük** &gt; **Kanalid** &gt; **Jaekaupluse rahandus** &gt; **Aruanded** &gt; **Kanali koondaruanne**</span><span class="sxs-lookup"><span data-stu-id="bf5b6-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="bf5b6-108">Jaotis **Päringud ja aruanded** &gt; **Jaemüük** &gt; **Päringud ja aruanded** &gt; **Müügiaruanded** &gt; **Kanali koondaruanne**</span><span class="sxs-lookup"><span data-stu-id="bf5b6-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="bf5b6-109">See aruanne pakub kaupluse jõudluse osana järgmiste kokkuvõtete hetketõmmiseid:</span><span class="sxs-lookup"><span data-stu-id="bf5b6-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="bf5b6-110">Müügi brutokokkuvõte</span><span class="sxs-lookup"><span data-stu-id="bf5b6-110">Gross sales summary</span></span>
- <span data-ttu-id="bf5b6-111">Maksevahendi tüübi kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="bf5b6-111">Tender type summary</span></span>
- <span data-ttu-id="bf5b6-112">Maksu kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="bf5b6-112">Tax summary</span></span>
- <span data-ttu-id="bf5b6-113">hinna tühistamiste kokkuvõte,</span><span class="sxs-lookup"><span data-stu-id="bf5b6-113">Price overrides summary</span></span>
- <span data-ttu-id="bf5b6-114">allahindluste kokkuvõte.</span><span class="sxs-lookup"><span data-stu-id="bf5b6-114">Discounts summary</span></span>
