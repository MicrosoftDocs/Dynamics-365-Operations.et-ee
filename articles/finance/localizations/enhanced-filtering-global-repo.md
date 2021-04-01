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
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 87ada5a97d2b716145082b3845fa87a12df57ef7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235593"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="2b92d-103">Täiustatud RCS-i filtreerimise võimalused konfiguratsioonide leidmiseks RCS-i/globaalses hoidlas</span><span class="sxs-lookup"><span data-stu-id="2b92d-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b92d-104">Selles teemas kirjeldatakse täiustatud filtreerimise võimalusi teenuste Regulatory Configuration Services (RCS) globaalses hoidlas, mida on täiustatud järgmiste täiendavate filtreerimisvõimaluste lisamisega.</span><span class="sxs-lookup"><span data-stu-id="2b92d-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="2b92d-105">**Riik/piirkond** – ISO riigikoodide põhjal</span><span class="sxs-lookup"><span data-stu-id="2b92d-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="2b92d-106">**Siltide** tüübid järgmiste jaoks.</span><span class="sxs-lookup"><span data-stu-id="2b92d-106">**Tags** types for:</span></span>
  - <span data-ttu-id="2b92d-107">Funktsionaalne ala</span><span class="sxs-lookup"><span data-stu-id="2b92d-107">Functional area</span></span>
  - <span data-ttu-id="2b92d-108">Funktsiooniala</span><span class="sxs-lookup"><span data-stu-id="2b92d-108">Feature area</span></span>
  - <span data-ttu-id="2b92d-109">Majandusharu</span><span class="sxs-lookup"><span data-stu-id="2b92d-109">Industry</span></span> 
  - <span data-ttu-id="2b92d-110">Äridokument</span><span class="sxs-lookup"><span data-stu-id="2b92d-110">Business document</span></span> 

<span data-ttu-id="2b92d-111">Saate määrata filtreid nii eraldi kui ka grupina, et teha kindlate või seostatud konfiguratsioonide leidmine lihtsamaks.</span><span class="sxs-lookup"><span data-stu-id="2b92d-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="2b92d-112">Näiteks võiksite rakendada filtrit **Äridokumendi tüüp**, et leida hankija arvetega seostatud konfigureeritavate äridokumentide üks tüüp ja otsida seda tüüpi dokumente.</span><span class="sxs-lookup"><span data-stu-id="2b92d-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="2b92d-113">[![Globaalse hoidla jaotise filtreerimine](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="2b92d-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="2b92d-114">Otsingut saate täpsemalt piiritleda, valides dokumendi tüübi, näiteks „hankija arve”, ja klõpsates käsku **Rakenda filter**.</span><span class="sxs-lookup"><span data-stu-id="2b92d-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="2b92d-115">Järgmine näide kuvab tulemusi filtri **Äridokumendi tüüp** rakendamise korral koos lisatud dokumendi tüübiga.</span><span class="sxs-lookup"><span data-stu-id="2b92d-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="2b92d-116">[![Äridokumendi tüübi rakendatud filter ja importimine](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="2b92d-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="2b92d-117">Filtreeritud tulemusi saab importida kasutajate RCS-i hoidlasse või Dynamics 365 Finance'i keskkonda nii eraldi kui ka komplektina.</span><span class="sxs-lookup"><span data-stu-id="2b92d-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="2b92d-118">Selleks valige konfiguratsioonide grupp ja klõpsake käsku **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="2b92d-118">To do this, select the group of configurations, and click **Import**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]