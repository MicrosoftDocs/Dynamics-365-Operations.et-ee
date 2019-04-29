---
title: Analüüsiaruanded on värskendamata
description: See teema selgitab, mida teha, kui kliendiandmete muudatusi ei kuvata kliendi tööruumides.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6a6487b50908093f876237ffef840a3144b3fe6
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/19/2019
ms.locfileid: "857449"
---
# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="c7e15-103">Analüüsiaruanded on värskendamata</span><span class="sxs-lookup"><span data-stu-id="c7e15-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c7e15-104">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="c7e15-104">**Issue**</span></span>

<span data-ttu-id="c7e15-105">Kliendiandmete muudatusi ei kuvata kliendi tööruumide vahekaartidel **Analüütika**.</span><span class="sxs-lookup"><span data-stu-id="c7e15-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="c7e15-106">**Põhjus**</span><span class="sxs-lookup"><span data-stu-id="c7e15-106">**Cause**</span></span>

<span data-ttu-id="c7e15-107">Vaikimisi värskendatakse Microsoft Power BI aruandeid iga nelja tunni järel mõõtmete juurutamise pakett-töö graafiku kohaselt.</span><span class="sxs-lookup"><span data-stu-id="c7e15-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="c7e15-108">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="c7e15-108">**Resolution**</span></span>

<span data-ttu-id="c7e15-109">Probleem võib olla ainult ajastuse küsimus.</span><span class="sxs-lookup"><span data-stu-id="c7e15-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="c7e15-110">Järgige neid samme, et alustada pakett-tööd ja värskendada analüütika tööruume.</span><span class="sxs-lookup"><span data-stu-id="c7e15-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="c7e15-111">Avage leht **Pakett-tööd** valikus **Süsteemihaldus \> Lingid \> Pakett-töö \> Pakett-tööd**.</span><span class="sxs-lookup"><span data-stu-id="c7e15-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="c7e15-112">Teise võimalusena kasutage otsingut ja sisestage **Pakett-töö**.</span><span class="sxs-lookup"><span data-stu-id="c7e15-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="c7e15-113">Leidke loendist töö **Mõõtme juurutamine**.</span><span class="sxs-lookup"><span data-stu-id="c7e15-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="c7e15-114">Valige lehe ülaosas **Redigeeri** ja määrake planeeritud alguskuupäevaks/-kellaajaks väärtus, mis värskendab analüütika praegusele ajale lähemal.</span><span class="sxs-lookup"><span data-stu-id="c7e15-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Pakett-tööd](media/batch-jobs.png)
