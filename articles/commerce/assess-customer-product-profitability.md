---
title: Kliendi ja toote tulususe hindamine
description: Selles artiklis selgitatakse, kuidas kasutada mälusisest ja reaalajas analüüsi kliendi ning toote kasumlikkuse vaatamiseks, uurimiseks ja selle kohta ülevaate saamiseks Dynamics 365 Commercei andmete põhjal.
author: ashishmsft
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 80a2f38f2b3f039b17556116d6aea738faa1db50
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797325"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="cc302-103">Kliendi ja toote tulususe hindamine</span><span class="sxs-lookup"><span data-stu-id="cc302-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cc302-104">Selles artiklis selgitatakse, kuidas kasutada mälusisest ja reaalajas analüüsi kliendi ning toote kasumlikkuse vaatamiseks, uurimiseks ja selle kohta ülevaate saamiseks Dynamics 365 Commercei andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="cc302-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="cc302-105">Commerce'i osana saavad kasutajad analüüsida parimate klientide (10–100) tulusust organisatsiooni hierarhia erinevatel tasemetel ühe alljärgneva kriteeriumi põhjal.</span><span class="sxs-lookup"><span data-stu-id="cc302-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="cc302-106">Müügisumma</span><span class="sxs-lookup"><span data-stu-id="cc302-106">Sales amount</span></span>
- <span data-ttu-id="cc302-107">Kogus</span><span class="sxs-lookup"><span data-stu-id="cc302-107">Quantity</span></span>
- <span data-ttu-id="cc302-108">Kogutulu marginaal</span><span class="sxs-lookup"><span data-stu-id="cc302-108">Gross profit margin</span></span>
- <span data-ttu-id="cc302-109">Marginaali protsent</span><span class="sxs-lookup"><span data-stu-id="cc302-109">Margin percentage</span></span>

<span data-ttu-id="cc302-110">Selle hinnangu jaoks saate kasutada **parimate klientide** valmisaruandeid, mille saate avada ühtest järgmistest asukohtadest:</span><span class="sxs-lookup"><span data-stu-id="cc302-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="cc302-111">Tööruum **Kaupluse haldus** &gt; **Jaemüük ja kaubandus** &gt; **Kanalid** &gt; **Kaupluse haldus** &gt; **Aruanded** &gt; **Parimate klientide aruanne**</span><span class="sxs-lookup"><span data-stu-id="cc302-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="cc302-112">**Päringud ja aruanded** jaotis &gt; **Jaemüük ja kaubandus** &gt; **Päringud ja aruanded** &gt; **Müügiaruanded** &gt; **Parimate klientide aruanne**</span><span class="sxs-lookup"><span data-stu-id="cc302-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="cc302-113">Samuti saavad kasutajad analüüsida peamiste toodete (10–100) tulusust organisatsiooni hierarhia erinevatel tasemetel ühe alljärgneva kriteeriumi põhjal:</span><span class="sxs-lookup"><span data-stu-id="cc302-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="cc302-114">Müügisumma</span><span class="sxs-lookup"><span data-stu-id="cc302-114">Sales amount</span></span>
- <span data-ttu-id="cc302-115">Kogus</span><span class="sxs-lookup"><span data-stu-id="cc302-115">Quantity</span></span>
- <span data-ttu-id="cc302-116">Kogutulu marginaal</span><span class="sxs-lookup"><span data-stu-id="cc302-116">Gross profit margin</span></span>
- <span data-ttu-id="cc302-117">Marginaali protsent</span><span class="sxs-lookup"><span data-stu-id="cc302-117">Margin percentage</span></span>

<span data-ttu-id="cc302-118">Selle hinnangu jaoks saate kasutada **peamiste toodete** valmisaruandeid, mille saate avada ühest järgmistest asukohtadest:</span><span class="sxs-lookup"><span data-stu-id="cc302-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="cc302-119">Tööruum **Kaupluse haldus** &gt; **Jaemüük ja kaubandus** &gt; **Kanalid** &gt; **Kaupluse haldus** &gt; **Aruanded** &gt; **Parimate toodete aruanne**</span><span class="sxs-lookup"><span data-stu-id="cc302-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="cc302-120">Tööruum **Kategooria ja toote haldus** &gt; **Jaemüük ja kaubandus** &gt; **Tooted ja kategooriad** &gt; **Kaupluse haldus** &gt; **Aruanded** &gt; **Peamiste toodete aruanne**</span><span class="sxs-lookup"><span data-stu-id="cc302-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="cc302-121">**Päringud ja aruanded** jaotis &gt; **Jaemüük ja kaubandus** &gt; **Päringud ja aruanded** &gt; **Müügiaruanded** &gt; **Parimate toodete aruanne**</span><span class="sxs-lookup"><span data-stu-id="cc302-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]