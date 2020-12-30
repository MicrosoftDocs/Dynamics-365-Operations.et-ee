---
title: Plahvatuse jaoks jälgimise kasutamine
description: Selles artiklis selgitatakse, kuidas kasutada jälgimist tellimuse koosnevusarvutuse tulemuse põhjuste uurimiseks.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e777d69c9da8a19c186bca3ca591e59af232f0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426032"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="2effe-103">Plahvatuse jaoks jälgimise kasutamine</span><span class="sxs-lookup"><span data-stu-id="2effe-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2effe-104">Selles artiklis selgitatakse, kuidas kasutada jälgimist tellimuse koosnevusarvutuse tulemuse põhjuste uurimiseks.</span><span class="sxs-lookup"><span data-stu-id="2effe-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="2effe-105">Jälgimise lubamisega saate vaadata teavet tegurite kohta, mis konkreetse tellimuse koosnevusarvutuse tulemust mõjutasid.</span><span class="sxs-lookup"><span data-stu-id="2effe-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="2effe-106">Järgmised näited näitavad, kuidas jälgimisteavet kasutada saab.</span><span class="sxs-lookup"><span data-stu-id="2effe-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="2effe-107">Saate kuvada plaanitud tellimuste tegevuste seosed, et optimeerida tarneahelat ja varude reserveerimisi.</span><span class="sxs-lookup"><span data-stu-id="2effe-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="2effe-108">Saate kuvada juba kinnitatud tellimuste seosed.</span><span class="sxs-lookup"><span data-stu-id="2effe-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="2effe-109">Saate keskenduda tuletatud nõuete automaatsele kinnitamisele ja siis tellimustele täpsemaid prioriteete seada.</span><span class="sxs-lookup"><span data-stu-id="2effe-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="2effe-110">Saate simuleerida plaanimistulemusi, et määrata, kas plaanimise parameetrid on optimaalsed.</span><span class="sxs-lookup"><span data-stu-id="2effe-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="2effe-111">Saate tuvastada, kuidas andmed nagu tootmiskuupäevad, kogused ja prioriteedid tellimuse puhul määrati.</span><span class="sxs-lookup"><span data-stu-id="2effe-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="2effe-112">Saate vaadata tulevaste üksuste üksikasju ja valitud tellimuse toiminguid.</span><span class="sxs-lookup"><span data-stu-id="2effe-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="2effe-113">Lehel **Koosnevus** on jälgimisteave saadaval ülemisel paanil asuval vahekaardil **Selgitus**.</span><span class="sxs-lookup"><span data-stu-id="2effe-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="2effe-114">Jälgimine toimub tellimuse koosnevuse kuvamisel.</span><span class="sxs-lookup"><span data-stu-id="2effe-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="2effe-115">Tellimuse jälgimise alustamiseks klõpsake käsku **Uuenda** ja märkige siis ruut **Luba jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="2effe-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="2effe-116">Logist konkreetse teabe otsimiseks saab kasutada välja **Teksti otsimine**.</span><span class="sxs-lookup"><span data-stu-id="2effe-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="2effe-117">Otsingutulemused tõstetakse puul esile.</span><span class="sxs-lookup"><span data-stu-id="2effe-117">Search results are highlighted in the tree.</span></span>

<a name="additional-resources"></a><span data-ttu-id="2effe-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2effe-118">Additional resources</span></span>
--------

[<span data-ttu-id="2effe-119">Koondplaanide ülevaade</span><span class="sxs-lookup"><span data-stu-id="2effe-119">Master plans overview</span></span>](master-plans.md)



