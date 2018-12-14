---
title: "Talenti aruandlusvõimalused"
description: "Selles teemas selgitatakse, kuidas lahendada probleemi, mille käigus klient soovib kohandada rakenduse Microsoft Dynamics 365 for Talent aruandeid või luua uusi aruandeid."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.contentlocale: et-ee
ms.lasthandoff: 12/04/2018

---

# <a name="reporting-options-in-talent"></a><span data-ttu-id="c9ef1-103">Talenti aruandlusvõimalused</span><span class="sxs-lookup"><span data-stu-id="c9ef1-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c9ef1-104">**Keskkonna üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="c9ef1-104">**Environment details**</span></span>

<span data-ttu-id="c9ef1-105">Probeem kehtib kõigile keskkondadele.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-105">This issue applies to all environments.</span></span>

<span data-ttu-id="c9ef1-106">**Sümptom**</span><span class="sxs-lookup"><span data-stu-id="c9ef1-106">**Symptom**</span></span>

<span data-ttu-id="c9ef1-107">Klient soovib kohandada rakenduse Microsoft Dynamics 365 for Talent aruandeid või luua uusi aruandeid.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="c9ef1-108">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="c9ef1-108">**Issue**</span></span>

<span data-ttu-id="c9ef1-109">Kasutaja ei saa kohandada manustatud Microsoft Power BI aruandeid.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="c9ef1-110">**Lahendus**</span><span class="sxs-lookup"><span data-stu-id="c9ef1-110">**Solution**</span></span>

- <span data-ttu-id="c9ef1-111">Core HR-i andmete voogu teenusesse Common Data Service for Apps saab esitada rakendusse Power BI Desktop PowerAppsi CDS-konnektori kaudu.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="c9ef1-112">Pange tähele, et teenus Common Data Service for Apps sisaldab Core HR-i andmete alamkogumit.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="c9ef1-113">Lisateavet Power BI ja armatuurlaudade kohta vt jaotisest [Power BI aruannete ja armatuurlaudade loomine PowerAppsi teenusega Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="c9ef1-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="c9ef1-114">Mõnedele aruannetele on Talentis saadaval elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="c9ef1-115">Kliendi juhitud kohandamisi saab teha ER-i konfiguratsioonivalikute kaudu.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="c9ef1-116">Andmed saab eksportida Microsoft Excelisse või Microsoft Wordi kasutades eri andmeüksuseid, mida rakendus Talent pakub Microsoft Office’i integratsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="c9ef1-117">**Pikaajaline lahendus**</span><span class="sxs-lookup"><span data-stu-id="c9ef1-117">**Long-term solution**</span></span>

<span data-ttu-id="c9ef1-118">Saadaval on Power BI lisavalikud ning teenusesse Common Data Service for Apps kuulub rohkem andmeid ja üksuseid.</span><span class="sxs-lookup"><span data-stu-id="c9ef1-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>

