---
title: Aruandlusvalikud
description: Selles artiklis selgitatakse, kuidas lahendada probleemi, mille käigus klient soovib kohandada rakenduse Microsoft Dynamics 365 Human Resources aruandeid või luua uusi aruandeid.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 5d47524033bf39a1db6b22b28ee3fcc65348829c
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431011"
---
# <a name="reporting-options"></a><span data-ttu-id="ef7a8-103">Aruandlusvalikud</span><span class="sxs-lookup"><span data-stu-id="ef7a8-103">Reporting options</span></span>

<span data-ttu-id="ef7a8-104">**Keskkonna üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="ef7a8-104">**Environment details**</span></span>

<span data-ttu-id="ef7a8-105">Probeem kehtib kõigile keskkondadele.</span><span class="sxs-lookup"><span data-stu-id="ef7a8-105">This issue applies to all environments.</span></span>

<span data-ttu-id="ef7a8-106">**Sümptom**</span><span class="sxs-lookup"><span data-stu-id="ef7a8-106">**Symptom**</span></span>

<span data-ttu-id="ef7a8-107">Klient soovib kohandada rakenduse Microsoft Dynamics 365 Human Resources aruandeid või luua uusi aruandeid.</span><span class="sxs-lookup"><span data-stu-id="ef7a8-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="ef7a8-108">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="ef7a8-108">**Issue**</span></span>

<span data-ttu-id="ef7a8-109">Kasutaja ei saa kohandada manustatud Microsoft Power BI aruandeid.</span><span class="sxs-lookup"><span data-stu-id="ef7a8-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="ef7a8-110">**Lahendus**</span><span class="sxs-lookup"><span data-stu-id="ef7a8-110">**Solution**</span></span>

- <span data-ttu-id="ef7a8-111">Rakenduse Human Resources andmete voogu teenusesse Common Data Service saab esitada rakendusse Power Apps Common Data Service’i konnektori kaudu Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="ef7a8-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="ef7a8-112">Pange tähele, et teenus Common Data Service sisaldab rakenduse Human Resources andmete alamkogumit.</span><span class="sxs-lookup"><span data-stu-id="ef7a8-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="ef7a8-113">Lisateavet Power BI ja armatuurlaudade kohta vt teemast [Loo Power BI aruannete ja armatuurlaudade loomine teenuse Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) abil.</span><span class="sxs-lookup"><span data-stu-id="ef7a8-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="ef7a8-114">Mõnedele aruannetele on rakenduses Human Resources saadaval elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="ef7a8-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="ef7a8-115">Kliendi juhitud kohandamisi saab teha ER-i konfiguratsioonivalikute kaudu.</span><span class="sxs-lookup"><span data-stu-id="ef7a8-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="ef7a8-116">Andmed saab eksportida Microsoft Excelisse või Microsoft Wordi, kasutades mitmesuguseid andmeüksuseid, mida rakendus Human Resources pakub Microsoft Office’i integratsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="ef7a8-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="ef7a8-117">**Pikaajaline lahendus**</span><span class="sxs-lookup"><span data-stu-id="ef7a8-117">**Long-term solution**</span></span>

<span data-ttu-id="ef7a8-118">Saadaval on Power BI lisasuvandid ning teenusesse Common Data Service kuulub rohkem andmeid ja üksuseid.</span><span class="sxs-lookup"><span data-stu-id="ef7a8-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
