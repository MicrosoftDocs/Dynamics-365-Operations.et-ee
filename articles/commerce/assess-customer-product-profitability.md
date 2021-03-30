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
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e0589748247cf9195116687cf70228b4ef36e29b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211542"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="f0066-103">Kliendi ja toote tulususe hindamine</span><span class="sxs-lookup"><span data-stu-id="f0066-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f0066-104">Selles artiklis selgitatakse, kuidas kasutada mälusisest ja reaalajas analüüsi kliendi ning toote kasumlikkuse vaatamiseks, uurimiseks ja selle kohta ülevaate saamiseks Dynamics 365 Commercei andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="f0066-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="f0066-105">Commerce'i osana saavad kasutajad analüüsida parimate klientide (10–100) tulusust organisatsiooni hierarhia erinevatel tasemetel ühe alljärgneva kriteeriumi põhjal.</span><span class="sxs-lookup"><span data-stu-id="f0066-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="f0066-106">Müügisumma</span><span class="sxs-lookup"><span data-stu-id="f0066-106">Sales amount</span></span>
- <span data-ttu-id="f0066-107">Kogus</span><span class="sxs-lookup"><span data-stu-id="f0066-107">Quantity</span></span>
- <span data-ttu-id="f0066-108">Kogutulu marginaal</span><span class="sxs-lookup"><span data-stu-id="f0066-108">Gross profit margin</span></span>
- <span data-ttu-id="f0066-109">Marginaali protsent</span><span class="sxs-lookup"><span data-stu-id="f0066-109">Margin percentage</span></span>

<span data-ttu-id="f0066-110">Selle hinnangu jaoks saate kasutada **parimate klientide** valmisaruandeid, mille saate avada ühtest järgmistest asukohtadest:</span><span class="sxs-lookup"><span data-stu-id="f0066-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="f0066-111">Tööruum **Kaupluse haldus** &gt; **Jaemüük ja kaubandus** &gt; **Kanalid** &gt; **Kaupluse haldus** &gt; **Aruanded** &gt; **Parimate klientide aruanne**</span><span class="sxs-lookup"><span data-stu-id="f0066-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="f0066-112">**Päringud ja aruanded** jaotis &gt; **Jaemüük ja kaubandus** &gt; **Päringud ja aruanded** &gt; **Müügiaruanded** &gt; **Parimate klientide aruanne**</span><span class="sxs-lookup"><span data-stu-id="f0066-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="f0066-113">Samuti saavad kasutajad analüüsida peamiste toodete (10–100) tulusust organisatsiooni hierarhia erinevatel tasemetel ühe alljärgneva kriteeriumi põhjal:</span><span class="sxs-lookup"><span data-stu-id="f0066-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="f0066-114">Müügisumma</span><span class="sxs-lookup"><span data-stu-id="f0066-114">Sales amount</span></span>
- <span data-ttu-id="f0066-115">Kogus</span><span class="sxs-lookup"><span data-stu-id="f0066-115">Quantity</span></span>
- <span data-ttu-id="f0066-116">Kogutulu marginaal</span><span class="sxs-lookup"><span data-stu-id="f0066-116">Gross profit margin</span></span>
- <span data-ttu-id="f0066-117">Marginaali protsent</span><span class="sxs-lookup"><span data-stu-id="f0066-117">Margin percentage</span></span>

<span data-ttu-id="f0066-118">Selle hinnangu jaoks saate kasutada **peamiste toodete** valmisaruandeid, mille saate avada ühest järgmistest asukohtadest:</span><span class="sxs-lookup"><span data-stu-id="f0066-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="f0066-119">Tööruum **Kaupluse haldus** &gt; **Jaemüük ja kaubandus** &gt; **Kanalid** &gt; **Kaupluse haldus** &gt; **Aruanded** &gt; **Parimate toodete aruanne**</span><span class="sxs-lookup"><span data-stu-id="f0066-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="f0066-120">Tööruum **Kategooria ja toote haldus** &gt; **Jaemüük ja kaubandus** &gt; **Tooted ja kategooriad** &gt; **Kaupluse haldus** &gt; **Aruanded** &gt; **Peamiste toodete aruanne**</span><span class="sxs-lookup"><span data-stu-id="f0066-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="f0066-121">**Päringud ja aruanded** jaotis &gt; **Jaemüük ja kaubandus** &gt; **Päringud ja aruanded** &gt; **Müügiaruanded** &gt; **Parimate toodete aruanne**</span><span class="sxs-lookup"><span data-stu-id="f0066-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]