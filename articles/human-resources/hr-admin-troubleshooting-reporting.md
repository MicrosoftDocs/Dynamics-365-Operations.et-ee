---
title: Aruandlusvalikud
description: Selles artiklis selgitatakse, kuidas lahendada probleemi, mille käigus klient soovib kohandada rakenduse Microsoft Dynamics 365 Human Resources aruandeid või luua uusi aruandeid.
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
ms.openlocfilehash: 2d0fc6b2d4af6ad021943717645bfff7a27797a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803893"
---
# <a name="reporting-options"></a><span data-ttu-id="b9109-103">Aruandlusvalikud</span><span class="sxs-lookup"><span data-stu-id="b9109-103">Reporting options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b9109-104">**Keskkonna üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="b9109-104">**Environment details**</span></span>

<span data-ttu-id="b9109-105">Probeem kehtib kõigile keskkondadele.</span><span class="sxs-lookup"><span data-stu-id="b9109-105">This issue applies to all environments.</span></span>

<span data-ttu-id="b9109-106">**Sümptom**</span><span class="sxs-lookup"><span data-stu-id="b9109-106">**Symptom**</span></span>

<span data-ttu-id="b9109-107">Klient soovib kohandada rakenduse Microsoft Dynamics 365 Human Resources aruandeid või luua uusi aruandeid.</span><span class="sxs-lookup"><span data-stu-id="b9109-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="b9109-108">**Väljasta**</span><span class="sxs-lookup"><span data-stu-id="b9109-108">**Issue**</span></span>

<span data-ttu-id="b9109-109">Kasutaja ei saa manustatud Microsoft Power BI aruandeid kohandada.</span><span class="sxs-lookup"><span data-stu-id="b9109-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="b9109-110">**Lahendus**</span><span class="sxs-lookup"><span data-stu-id="b9109-110">**Solution**</span></span>

- <span data-ttu-id="b9109-111">Rakenduse Human Resources andmete voogu teenusesse Dataverse saab esitada rakendusse Power Apps Dataverse’i konnektori kaudu Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="b9109-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="b9109-112">Pange tähele, et teenus Dataverse sisaldab rakenduse Human Resources andmete alamkogumit.</span><span class="sxs-lookup"><span data-stu-id="b9109-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="b9109-113">Lisateavet Power BI ja armatuurlaudade kohta vt teemast [Loo Power BI aruannete ja armatuurlaudade loomine teenuse Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) abil.</span><span class="sxs-lookup"><span data-stu-id="b9109-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="b9109-114">Mõnedele aruannetele on rakenduses Human Resources saadaval elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="b9109-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="b9109-115">Kliendi juhitud kohandamisi saab teha ER-i konfiguratsioonivalikute kaudu.</span><span class="sxs-lookup"><span data-stu-id="b9109-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="b9109-116">Andmed saab eksportida Microsoft Excelisse või Microsoft Wordi, kasutades mitmesuguseid andmeüksuseid, mida rakendus Human Resources pakub Microsoft Office’i integratsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="b9109-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="b9109-117">**Pikaajaline lahendus**</span><span class="sxs-lookup"><span data-stu-id="b9109-117">**Long-term solution**</span></span>

<span data-ttu-id="b9109-118">Saadaval on Power BI lisasuvandid ning teenusesse Dataverse kuulub rohkem andmeid ja üksuseid.</span><span class="sxs-lookup"><span data-stu-id="b9109-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]