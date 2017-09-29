---
title: "Plahvatuse jaoks jälgimise kasutamine"
description: "Selles artiklis selgitatakse, kuidas kasutada jälgimist tellimuse koosnevusarvutuse tulemuse põhjuste uurimiseks."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4e7f765f31ba34481cca78155e77eca61b106d50
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="use-tracing-for-explosion"></a><span data-ttu-id="58cda-103">Plahvatuse jaoks jälgimise kasutamine</span><span class="sxs-lookup"><span data-stu-id="58cda-103">Use tracing for explosion</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="58cda-104">Selles artiklis selgitatakse, kuidas kasutada jälgimist tellimuse koosnevusarvutuse tulemuse põhjuste uurimiseks.</span><span class="sxs-lookup"><span data-stu-id="58cda-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="58cda-105">Jälgimise lubamisega saate vaadata teavet tegurite kohta, mis konkreetse tellimuse koosnevusarvutuse tulemust mõjutasid.</span><span class="sxs-lookup"><span data-stu-id="58cda-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="58cda-106">Järgmised näited näitavad, kuidas jälgimisteavet kasutada saab.</span><span class="sxs-lookup"><span data-stu-id="58cda-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="58cda-107">Saate kuvada plaanitud tellimuste tegevuste seosed, et optimeerida tarneahelat ja varude reserveerimisi.</span><span class="sxs-lookup"><span data-stu-id="58cda-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="58cda-108">Saate kuvada juba kinnitatud tellimuste seosed.</span><span class="sxs-lookup"><span data-stu-id="58cda-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="58cda-109">Saate keskenduda tuletatud nõuete automaatsele kinnitamisele ja siis tellimustele täpsemaid prioriteete seada.</span><span class="sxs-lookup"><span data-stu-id="58cda-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="58cda-110">Saate simuleerida plaanimistulemusi, et määrata, kas plaanimise parameetrid on optimaalsed.</span><span class="sxs-lookup"><span data-stu-id="58cda-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="58cda-111">Saate tuvastada, kuidas andmed nagu tootmiskuupäevad, kogused ja prioriteedid tellimuse puhul määrati.</span><span class="sxs-lookup"><span data-stu-id="58cda-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="58cda-112">Saate vaadata tulevaste üksuste üksikasju ja valitud tellimuse toiminguid.</span><span class="sxs-lookup"><span data-stu-id="58cda-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="58cda-113">Lehel **Koosnevus** on jälgimisteave saadaval ülemisel paanil asuval vahekaardil **Selgitus**.</span><span class="sxs-lookup"><span data-stu-id="58cda-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="58cda-114">Jälgimine toimub tellimuse koosnevuse kuvamisel.</span><span class="sxs-lookup"><span data-stu-id="58cda-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="58cda-115">Tellimuse jälgimise alustamiseks klõpsake käsku **Uuenda** ja märkige siis ruut **Luba jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="58cda-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="58cda-116">Logist konkreetse teabe otsimiseks saab kasutada välja **Teksti otsimine**.</span><span class="sxs-lookup"><span data-stu-id="58cda-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="58cda-117">Otsingutulemused tõstetakse puul esile.</span><span class="sxs-lookup"><span data-stu-id="58cda-117">Search results are highlighted in the tree.</span></span>

<a name="see-also"></a><span data-ttu-id="58cda-118">Vt ka</span><span class="sxs-lookup"><span data-stu-id="58cda-118">See also</span></span>
--------

[<span data-ttu-id="58cda-119">Koondplaanid</span><span class="sxs-lookup"><span data-stu-id="58cda-119">Master plans</span></span>](master-plans.md)




