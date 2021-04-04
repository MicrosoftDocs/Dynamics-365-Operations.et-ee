---
title: Analüütiliste aruannete tõrkeotsing
description: See artikkel selgitab, mida teha, kui kliendiandmete muudatusi ei kuvata kliendi tööruumides.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: e0befe1a35aa46b2eabb4516559fe07ce27e9f18
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466660"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="f8f39-103">Analüütiliste aruannete tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="f8f39-103">Troubleshoot analytic reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f8f39-104">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="f8f39-104">**Issue**</span></span>

<span data-ttu-id="f8f39-105">Kliendiandmete muudatusi ei kuvata kliendi tööruumide vahekaartidel **Analüütika**.</span><span class="sxs-lookup"><span data-stu-id="f8f39-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="f8f39-106">**Põhjus**</span><span class="sxs-lookup"><span data-stu-id="f8f39-106">**Cause**</span></span>

<span data-ttu-id="f8f39-107">Vaikimisi värskendatakse Microsoft Power BI aruandeid iga nelja tunni järel mõõtmete juurutamise pakett-töö graafiku kohaselt.</span><span class="sxs-lookup"><span data-stu-id="f8f39-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="f8f39-108">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="f8f39-108">**Resolution**</span></span>

<span data-ttu-id="f8f39-109">Probleem võib olla ainult ajastuse küsimus.</span><span class="sxs-lookup"><span data-stu-id="f8f39-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="f8f39-110">Järgige neid samme, et alustada pakett-tööd ja värskendada analüütika tööruume.</span><span class="sxs-lookup"><span data-stu-id="f8f39-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="f8f39-111">Avage leht **Pakett-tööd** valikus **Süsteemihaldus \> Lingid \> Pakett-töö \> Pakett-tööd**.</span><span class="sxs-lookup"><span data-stu-id="f8f39-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="f8f39-112">Teise võimalusena kasutage otsingut ja sisestage **Pakett-töö**.</span><span class="sxs-lookup"><span data-stu-id="f8f39-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="f8f39-113">Leidke loendist töö **Mõõtme juurutamine**.</span><span class="sxs-lookup"><span data-stu-id="f8f39-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="f8f39-114">Valige lehe ülaosas **Redigeeri** ja määrake planeeritud alguskuupäevaks/-kellaajaks väärtus, mis värskendab analüütika praegusele ajale lähemal.</span><span class="sxs-lookup"><span data-stu-id="f8f39-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Pakett-tööd](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]