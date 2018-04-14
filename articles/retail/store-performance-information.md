---
title: "Kaupluse jõudluse analüüsimine"
description: "Selles artiklis selgitatakse, kuidas kasutada mälusisest ja reaalajas analüüsi, et Microsoft Dynamics 365 for Retaili andmete põhjal kaupluse jõudlusele juurdepääs saada, seda uurida ja selle kohta ülevaadet saada."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailChannelReport, SysOperationTemplateForm, RetailChannelManagementWorkspace
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
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 76ae826024f6ef351fa3535cd0cb1c86f7aafdb4
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="analyze-store-performance"></a><span data-ttu-id="e0de2-103">Kaupluse jõudluse analüüsimine</span><span class="sxs-lookup"><span data-stu-id="e0de2-103">Analyze store performance</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="e0de2-104">Selles artiklis selgitatakse, kuidas kasutada mälusisest ja reaalajas analüüsi, et Microsoft Dynamics 365 for Retaili andmete põhjal kaupluse jõudlusele juurdepääs saada, seda uurida ja selle kohta ülevaadet saada.</span><span class="sxs-lookup"><span data-stu-id="e0de2-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Microsoft Dynamics 365 for Retail data.</span></span> 

<span data-ttu-id="e0de2-105">Kasutajad saavad Dynamics 365 for Retaili osana uurida kaupluse jõudlust valitud perioodil reaalajas organisatsiooni hierarhia erinevatel tasanditel, avades valmisaruande **Kanali kokkuvõte** ühest järgmistest asukohtadest.</span><span class="sxs-lookup"><span data-stu-id="e0de2-105">As part of Dynamics 365 for Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

-   <span data-ttu-id="e0de2-106">Tööruum **Jaekaupluse haldus** &gt; **Jaemüük** &gt; **Kanalid** &gt; **Jaekaupluse haldus** &gt; **Aruanded** &gt; **Kanali koondaruanne**</span><span class="sxs-lookup"><span data-stu-id="e0de2-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
-   <span data-ttu-id="e0de2-107">Tööruum **Jaekaupluse rahandus** &gt; **Jaemüük** &gt; **Kanalid** &gt; **Jaekaupluse rahandus** &gt; **Aruanded** &gt; **Kanali koondaruanne**</span><span class="sxs-lookup"><span data-stu-id="e0de2-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
-   <span data-ttu-id="e0de2-108">Jaotis **Päringud ja aruanded** &gt; **Jaemüük** &gt; **Päringud ja aruanded** &gt; **Müügiaruanded** &gt; **Kanali koondaruanne**</span><span class="sxs-lookup"><span data-stu-id="e0de2-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="e0de2-109">See aruanne pakub kaupluse jõudluse osana järgmiste kokkuvõtete hetketõmmiseid:</span><span class="sxs-lookup"><span data-stu-id="e0de2-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

-   <span data-ttu-id="e0de2-110">Müügi brutokokkuvõte</span><span class="sxs-lookup"><span data-stu-id="e0de2-110">Gross sales summary</span></span>
-   <span data-ttu-id="e0de2-111">Maksevahendi tüübi kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="e0de2-111">Tender type summary</span></span>
-   <span data-ttu-id="e0de2-112">Maksu kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="e0de2-112">Tax summary</span></span>
-   <span data-ttu-id="e0de2-113">hinna tühistamiste kokkuvõte,</span><span class="sxs-lookup"><span data-stu-id="e0de2-113">Price overrides summary</span></span>
-   <span data-ttu-id="e0de2-114">allahindluste kokkuvõte.</span><span class="sxs-lookup"><span data-stu-id="e0de2-114">Discounts summary</span></span>



