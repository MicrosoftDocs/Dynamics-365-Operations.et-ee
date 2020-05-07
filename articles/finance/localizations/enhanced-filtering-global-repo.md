---
title: Täiustatud RCS-i filtreerimine RCS-i/globaalses hoidlas
description: Selles teemas kirjeldatakse täiustatud filtreerimise võimalusi RCS-i globaalses hoidlas, mida on täiustatud täiendavate filtrite lisamisega.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1913b661c46af5e34da1a2939cb2a5d5b4e46411
ms.sourcegitcommit: 7df49a85de484d013518217ba8ada6c61da4b6e4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/24/2020
ms.locfileid: "3287935"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="f6193-103">Täiustatud RCS-i filtreerimise võimalused konfiguratsioonide leidmiseks RCS-i/globaalses hoidlas</span><span class="sxs-lookup"><span data-stu-id="f6193-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6193-104">Selles teemas kirjeldatakse täiustatud filtreerimise võimalusi teenuste Regulatory Configuration Services (RCS) globaalses hoidlas, mida on täiustatud järgmiste täiendavate filtreerimisvõimaluste lisamisega.</span><span class="sxs-lookup"><span data-stu-id="f6193-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="f6193-105">**Riik/piirkond** – ISO riigikoodide põhjal</span><span class="sxs-lookup"><span data-stu-id="f6193-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="f6193-106">**Siltide** tüübid järgmiste jaoks.</span><span class="sxs-lookup"><span data-stu-id="f6193-106">**Tags** types for:</span></span>
  - <span data-ttu-id="f6193-107">Funktsionaalne ala</span><span class="sxs-lookup"><span data-stu-id="f6193-107">Functional area</span></span>
  - <span data-ttu-id="f6193-108">Funktsiooniala</span><span class="sxs-lookup"><span data-stu-id="f6193-108">Feature area</span></span>
  - <span data-ttu-id="f6193-109">Majandusharu</span><span class="sxs-lookup"><span data-stu-id="f6193-109">Industry</span></span> 
  - <span data-ttu-id="f6193-110">Äridokument</span><span class="sxs-lookup"><span data-stu-id="f6193-110">Business document</span></span> 

<span data-ttu-id="f6193-111">Saate määrata filtreid nii eraldi kui ka grupina, et teha kindlate või seostatud konfiguratsioonide leidmine lihtsamaks.</span><span class="sxs-lookup"><span data-stu-id="f6193-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="f6193-112">Näiteks võiksite rakendada filtrit **Äridokumendi tüüp**, et leida hankija arvetega seostatud konfigureeritavate äridokumentide üks tüüp ja otsida seda tüüpi dokumente.</span><span class="sxs-lookup"><span data-stu-id="f6193-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="f6193-113">[![Globaalse hoidla jaotise filtreerimine](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="f6193-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="f6193-114">Otsingut saate täpsemalt piiritleda, valides dokumendi tüübi, näiteks „hankija arve”, ja klõpsates käsku **Rakenda filter**.</span><span class="sxs-lookup"><span data-stu-id="f6193-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="f6193-115">Järgmine näide kuvab tulemusi filtri **Äridokumendi tüüp** rakendamise korral koos lisatud dokumendi tüübiga.</span><span class="sxs-lookup"><span data-stu-id="f6193-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="f6193-116">[![Äridokumendi tüübi rakendatud filter ja importimine](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="f6193-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="f6193-117">Filtreeritud tulemusi saab importida kasutajate RCS-i hoidlasse või Dynamics 365 Finance'i keskkonda nii eraldi kui ka komplektina.</span><span class="sxs-lookup"><span data-stu-id="f6193-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="f6193-118">Selleks valige konfiguratsioonide grupp ja klõpsake käsku **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="f6193-118">To do this, select the group of configurations, and click **Import**.</span></span>
