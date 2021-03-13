---
title: Aruandlusvalikud
description: Selles artiklis selgitatakse, kuidas lahendada probleemi, mille käigus klient soovib kohandada rakenduse Microsoft Dynamics 365 Human Resources aruandeid või luua uusi aruandeid.
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
ms.openlocfilehash: 830c8c32128a8dfc1b009557afb272e48ae3a1ff
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112196"
---
# <a name="reporting-options"></a><span data-ttu-id="05309-103">Aruandlusvalikud</span><span class="sxs-lookup"><span data-stu-id="05309-103">Reporting options</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="05309-104">**Keskkonna üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="05309-104">**Environment details**</span></span>

<span data-ttu-id="05309-105">Probeem kehtib kõigile keskkondadele.</span><span class="sxs-lookup"><span data-stu-id="05309-105">This issue applies to all environments.</span></span>

<span data-ttu-id="05309-106">**Sümptom**</span><span class="sxs-lookup"><span data-stu-id="05309-106">**Symptom**</span></span>

<span data-ttu-id="05309-107">Klient soovib kohandada rakenduse Microsoft Dynamics 365 Human Resources aruandeid või luua uusi aruandeid.</span><span class="sxs-lookup"><span data-stu-id="05309-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="05309-108">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="05309-108">**Issue**</span></span>

<span data-ttu-id="05309-109">Kasutaja ei saa kohandada manustatud Microsoft Power BI aruandeid.</span><span class="sxs-lookup"><span data-stu-id="05309-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="05309-110">**Lahendus**</span><span class="sxs-lookup"><span data-stu-id="05309-110">**Solution**</span></span>

- <span data-ttu-id="05309-111">Rakenduse Human Resources andmete voogu teenusesse Dataverse saab esitada rakendusse Power Apps Dataverse’i konnektori kaudu Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="05309-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="05309-112">Pange tähele, et teenus Dataverse sisaldab rakenduse Human Resources andmete alamkogumit.</span><span class="sxs-lookup"><span data-stu-id="05309-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="05309-113">Lisateavet Power BI ja armatuurlaudade kohta vt teemast [Loo Power BI aruannete ja armatuurlaudade loomine teenuse Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) abil.</span><span class="sxs-lookup"><span data-stu-id="05309-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="05309-114">Mõnedele aruannetele on rakenduses Human Resources saadaval elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="05309-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="05309-115">Kliendi juhitud kohandamisi saab teha ER-i konfiguratsioonivalikute kaudu.</span><span class="sxs-lookup"><span data-stu-id="05309-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="05309-116">Andmed saab eksportida Microsoft Excelisse või Microsoft Wordi, kasutades mitmesuguseid andmeüksuseid, mida rakendus Human Resources pakub Microsoft Office’i integratsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="05309-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="05309-117">**Pikaajaline lahendus**</span><span class="sxs-lookup"><span data-stu-id="05309-117">**Long-term solution**</span></span>

<span data-ttu-id="05309-118">Saadaval on Power BI lisasuvandid ning teenusesse Dataverse kuulub rohkem andmeid ja üksuseid.</span><span class="sxs-lookup"><span data-stu-id="05309-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>
