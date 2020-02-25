---
title: Kliendi ja toote tulususe hindamine
description: Selles artiklis selgitatakse, kuidas kasutada mälusisest ja reaalajas analüüsi kliendi ning toote kasumlikkuse vaatamiseks, uurimiseks ja selle kohta ülevaate saamiseks Dynamics 365 Commercei andmete põhjal.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
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
ms.openlocfilehash: 3218a29995791ce0d9a42d5b6d898d6e548f0f1d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022212"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="e9188-103">Kliendi ja toote tulususe hindamine</span><span class="sxs-lookup"><span data-stu-id="e9188-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e9188-104">Selles artiklis selgitatakse, kuidas kasutada mälusisest ja reaalajas analüüsi kliendi ning toote kasumlikkuse vaatamiseks, uurimiseks ja selle kohta ülevaate saamiseks Dynamics 365 Commercei andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="e9188-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="e9188-105">Commerce'i osana saavad kasutajad analüüsida parimate klientide (10–100) tulusust organisatsiooni hierarhia erinevatel tasemetel ühe alljärgneva kriteeriumi põhjal.</span><span class="sxs-lookup"><span data-stu-id="e9188-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="e9188-106">Müügisumma</span><span class="sxs-lookup"><span data-stu-id="e9188-106">Sales amount</span></span>
- <span data-ttu-id="e9188-107">Kogus</span><span class="sxs-lookup"><span data-stu-id="e9188-107">Quantity</span></span>
- <span data-ttu-id="e9188-108">Kogutulu marginaal</span><span class="sxs-lookup"><span data-stu-id="e9188-108">Gross profit margin</span></span>
- <span data-ttu-id="e9188-109">Marginaali protsent</span><span class="sxs-lookup"><span data-stu-id="e9188-109">Margin percentage</span></span>

<span data-ttu-id="e9188-110">Selle hinnangu jaoks saate kasutada **parimate klientide** valmisaruandeid, mille saate avada ühtest järgmistest asukohtadest:</span><span class="sxs-lookup"><span data-stu-id="e9188-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="e9188-111">Tööruum **Kaupluse haldus** &gt; **Jaemüük ja kaubandus** &gt; **Kanalid** &gt; **Kaupluse haldus** &gt; **Aruanded** &gt; **Parimate klientide aruanne**</span><span class="sxs-lookup"><span data-stu-id="e9188-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="e9188-112">**Päringud ja aruanded** jaotis &gt; **Jaemüük ja kaubandus** &gt; **Päringud ja aruanded** &gt; **Müügiaruanded** &gt; **Parimate klientide aruanne**</span><span class="sxs-lookup"><span data-stu-id="e9188-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="e9188-113">Samuti saavad kasutajad analüüsida peamiste toodete (10–100) tulusust organisatsiooni hierarhia erinevatel tasemetel ühe alljärgneva kriteeriumi põhjal:</span><span class="sxs-lookup"><span data-stu-id="e9188-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="e9188-114">Müügisumma</span><span class="sxs-lookup"><span data-stu-id="e9188-114">Sales amount</span></span>
- <span data-ttu-id="e9188-115">Kogus</span><span class="sxs-lookup"><span data-stu-id="e9188-115">Quantity</span></span>
- <span data-ttu-id="e9188-116">Kogutulu marginaal</span><span class="sxs-lookup"><span data-stu-id="e9188-116">Gross profit margin</span></span>
- <span data-ttu-id="e9188-117">Marginaali protsent</span><span class="sxs-lookup"><span data-stu-id="e9188-117">Margin percentage</span></span>

<span data-ttu-id="e9188-118">Selle hinnangu jaoks saate kasutada **peamiste toodete** valmisaruandeid, mille saate avada ühest järgmistest asukohtadest:</span><span class="sxs-lookup"><span data-stu-id="e9188-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="e9188-119">Tööruum **Kaupluse haldus** &gt; **Jaemüük ja kaubandus** &gt; **Kanalid** &gt; **Kaupluse haldus** &gt; **Aruanded** &gt; **Parimate toodete aruanne**</span><span class="sxs-lookup"><span data-stu-id="e9188-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="e9188-120">Tööruum **Kategooria ja toote haldus** &gt; **Jaemüük ja kaubandus** &gt; **Tooted ja kategooriad** &gt; **Kaupluse haldus** &gt; **Aruanded** &gt; **Peamiste toodete aruanne**</span><span class="sxs-lookup"><span data-stu-id="e9188-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="e9188-121">**Päringud ja aruanded** jaotis &gt; **Jaemüük ja kaubandus** &gt; **Päringud ja aruanded** &gt; **Müügiaruanded** &gt; **Parimate toodete aruanne**</span><span class="sxs-lookup"><span data-stu-id="e9188-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
