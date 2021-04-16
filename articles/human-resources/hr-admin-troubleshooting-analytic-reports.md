---
title: Analüütiliste aruannete tõrkeotsing
description: See artikkel selgitab, mida teha, kui kliendiandmete muudatusi ei kuvata kliendi tööruumides.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b500d519d61edfd20456355376e3fc81f16517a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794969"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="6fd4f-103">Analüütiliste aruannete tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="6fd4f-103">Troubleshoot analytic reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6fd4f-104">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="6fd4f-104">**Issue**</span></span>

<span data-ttu-id="6fd4f-105">Kliendiandmete muudatusi ei kuvata kliendi tööruumide vahekaartidel **Analüütika**.</span><span class="sxs-lookup"><span data-stu-id="6fd4f-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="6fd4f-106">**Põhjus**</span><span class="sxs-lookup"><span data-stu-id="6fd4f-106">**Cause**</span></span>

<span data-ttu-id="6fd4f-107">Vaikimisi värskendatakse Microsoft Power BI aruandeid iga nelja tunni järel mõõtmete juurutamise pakett-töö graafiku kohaselt.</span><span class="sxs-lookup"><span data-stu-id="6fd4f-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="6fd4f-108">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="6fd4f-108">**Resolution**</span></span>

<span data-ttu-id="6fd4f-109">Probleem võib olla ainult ajastuse küsimus.</span><span class="sxs-lookup"><span data-stu-id="6fd4f-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="6fd4f-110">Järgige neid samme, et alustada pakett-tööd ja värskendada analüütika tööruume.</span><span class="sxs-lookup"><span data-stu-id="6fd4f-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="6fd4f-111">Avage leht **Pakett-tööd** valikus **Süsteemihaldus \> Lingid \> Pakett-töö \> Pakett-tööd**.</span><span class="sxs-lookup"><span data-stu-id="6fd4f-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="6fd4f-112">Teise võimalusena kasutage otsingut ja sisestage **Pakett-töö**.</span><span class="sxs-lookup"><span data-stu-id="6fd4f-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="6fd4f-113">Leidke loendist töö **Mõõtme juurutamine**.</span><span class="sxs-lookup"><span data-stu-id="6fd4f-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="6fd4f-114">Valige lehe ülaosas **Redigeeri** ja määrake planeeritud alguskuupäevaks/-kellaajaks väärtus, mis värskendab analüütika praegusele ajale lähemal.</span><span class="sxs-lookup"><span data-stu-id="6fd4f-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Pakett-tööd](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]