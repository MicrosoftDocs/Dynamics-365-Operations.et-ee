---
title: Talenti aruandlusvõimalused
description: Selles teemas selgitatakse, kuidas lahendada probleemi, mille käigus klient soovib kohandada rakenduse Microsoft Dynamics 365 for Talent aruandeid või luua uusi aruandeid.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304108"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="47be9-103">Talenti aruandlusvõimalused</span><span class="sxs-lookup"><span data-stu-id="47be9-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="47be9-104">**Keskkonna üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="47be9-104">**Environment details**</span></span>

<span data-ttu-id="47be9-105">Probeem kehtib kõigile keskkondadele.</span><span class="sxs-lookup"><span data-stu-id="47be9-105">This issue applies to all environments.</span></span>

<span data-ttu-id="47be9-106">**Sümptom**</span><span class="sxs-lookup"><span data-stu-id="47be9-106">**Symptom**</span></span>

<span data-ttu-id="47be9-107">Klient soovib kohandada rakenduse Microsoft Dynamics 365 for Talent aruandeid või luua uusi aruandeid.</span><span class="sxs-lookup"><span data-stu-id="47be9-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="47be9-108">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="47be9-108">**Issue**</span></span>

<span data-ttu-id="47be9-109">Kasutaja ei saa kohandada manustatud Microsoft Power BI aruandeid.</span><span class="sxs-lookup"><span data-stu-id="47be9-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="47be9-110">**Lahendus**</span><span class="sxs-lookup"><span data-stu-id="47be9-110">**Solution**</span></span>

- <span data-ttu-id="47be9-111">Core HR-i andmete voogu teenusesse Common Data Service for Apps saab esitada rakendusse Power BI Desktop PowerAppsi CDS-konnektori kaudu.</span><span class="sxs-lookup"><span data-stu-id="47be9-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="47be9-112">Pange tähele, et teenus Common Data Service for Apps sisaldab Core HR-i andmete alamkogumit.</span><span class="sxs-lookup"><span data-stu-id="47be9-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="47be9-113">Lisateavet Power BI ja armatuurlaudade kohta vt teemast [Power BI aruannete ja armatuurlaudade loomine teenuse PowerApps Common Data Service abil](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="47be9-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="47be9-114">Mõnedele aruannetele on Talentis saadaval elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="47be9-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="47be9-115">Kliendi juhitud kohandamisi saab teha ER-i konfiguratsioonivalikute kaudu.</span><span class="sxs-lookup"><span data-stu-id="47be9-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="47be9-116">Andmed saab eksportida Microsoft Excelisse või Microsoft Wordi, kasutades mitmesuguseid andmeüksuseid, mida rakendus Talent pakub Microsoft Office’i integratsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="47be9-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="47be9-117">**Pikaajaline lahendus**</span><span class="sxs-lookup"><span data-stu-id="47be9-117">**Long-term solution**</span></span>

<span data-ttu-id="47be9-118">Saadaval on Power BI lisasuvandid ning teenusesse Common Data Service for Apps kuulub rohkem andmeid ja üksuseid.</span><span class="sxs-lookup"><span data-stu-id="47be9-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>
