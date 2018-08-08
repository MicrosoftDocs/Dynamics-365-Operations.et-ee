---
title: Korrigeeritud prognoosi autoriseerimine
description: "Kõiki prognoosi andmeid ei pea kohe autoriseerima. Selles artiklis selgitatakse, kuidas määrata perioodi, milleks prognoos on autoriseeritud. Samuti selgitatakse, kuidas autoriseerida prognoosiks kindlaid ettevõtteid ja prognoosimudeleid."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6c397329993bd3014b608cdc50d5002dcd5ed6a4
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---

# <a name="authorize-an-adjusted-forecast"></a><span data-ttu-id="ede71-105">Korrigeeritud prognoosi autoriseerimine</span><span class="sxs-lookup"><span data-stu-id="ede71-105">Authorize an adjusted forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ede71-106">Kõiki prognoosi andmeid ei pea kohe autoriseerima.</span><span class="sxs-lookup"><span data-stu-id="ede71-106">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="ede71-107">Selles artiklis selgitatakse, kuidas määrata perioodi, milleks prognoos on autoriseeritud.</span><span class="sxs-lookup"><span data-stu-id="ede71-107">This article explains how you can specify the period that a forecast is authorized for.</span></span> <span data-ttu-id="ede71-108">Samuti selgitatakse, kuidas autoriseerida prognoosiks kindlaid ettevõtteid ja prognoosimudeleid.</span><span class="sxs-lookup"><span data-stu-id="ede71-108">It also explains how you can authorize the forecast for specific companies and forecast models.</span></span>

<span data-ttu-id="ede71-109">Kõiki prognoosi andmeid ei pea kohe autoriseerima.</span><span class="sxs-lookup"><span data-stu-id="ede71-109">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="ede71-110">Prognoosi autoriseerimisele saate määrata algus- ja lõppkuupäevad.</span><span class="sxs-lookup"><span data-stu-id="ede71-110">You can specify the start and end dates of the period that the forecast is authorized for.</span></span> <span data-ttu-id="ede71-111">See funktsioon lubab kindlad vahemikud külmutada.</span><span class="sxs-lookup"><span data-stu-id="ede71-111">This functionality lets you freeze specific buckets.</span></span> 

<span data-ttu-id="ede71-112">Määratud algus- ja lõppkuupäevad peavad vastama loodud prognoosi vahemiku algus‑ ja lõppkuupäevadele.</span><span class="sxs-lookup"><span data-stu-id="ede71-112">The start and end dates that you specify must correspond to the start and end dates of the bucket that the forecast is generated in.</span></span> <span data-ttu-id="ede71-113">Süsteem rakendab seda piirangut ja korrigeerib automaatselt kuupäevi, kui see peaks vajalik olema.</span><span class="sxs-lookup"><span data-stu-id="ede71-113">The system enforces this restriction and automatically adjusts the dates, if adjustment is required.</span></span> 

<span data-ttu-id="ede71-114">Viimati loodud prognoosi üksikasju saate vaadata lehekülje **Autoriseerimine** vahekaardilt **Üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="ede71-114">On the **Details** tab of the **Authorization** page, you can view details about the forecast that was most recently generated.</span></span> 

<span data-ttu-id="ede71-115">Saate valida ettevõtted ja prognoosimudelid, mida prognoosi kasutama autoriseerida.</span><span class="sxs-lookup"><span data-stu-id="ede71-115">You can select the companies and the forecast models to authorize the forecast for use.</span></span> <span data-ttu-id="ede71-116">Ruudustik hõlmab vaikimisi kõiki ettevõtteid, millele prognoositud nõudlus on loodud.</span><span class="sxs-lookup"><span data-stu-id="ede71-116">By default, the grid includes all the companies that forecast demand has been created for.</span></span> <span data-ttu-id="ede71-117">Igale ettevõttele on eeltäidetud prognoosimudel, mis vastab praegusele koondplaneerimise parameetrites seadistatud prognoosiplaanile.</span><span class="sxs-lookup"><span data-stu-id="ede71-117">For each company, the forecast model that corresponds to the current forecast plan that is set up in the master planning parameters is prefilled.</span></span> <span data-ttu-id="ede71-118">Selle prognoosimudeli saate siiski vahetada ettevõttele kuuluva mistahes prognoosimudeli vastu.</span><span class="sxs-lookup"><span data-stu-id="ede71-118">However, you can change this forecast model to any forecast model that belongs to that company.</span></span> <span data-ttu-id="ede71-119">Kui valitud ettevõtte jaoks ei loodud prognoositud nõudluse andmeid, kuvatakse importimise ajal hoiatusteade.</span><span class="sxs-lookup"><span data-stu-id="ede71-119">If no forecast demand data has been generated for a selected company, you receive a warning message at import time.</span></span> 

<span data-ttu-id="ede71-120">Oluline on mõista, kuidas töötab ruut **Salvesta nõudluse alusprognoosis käsitsi tehtud korrigeerimised**.</span><span class="sxs-lookup"><span data-stu-id="ede71-120">It's very important that you understand how the **Save the manual adjustments made to the baseline demand forecast** check box works.</span></span> <span data-ttu-id="ede71-121">Kui olete statistilist alusprognoosi käsitsi korrigeerinud, lubatakse korrigeeritud väärtusi kasutada isegi juhul, kui see ruut on tühi.</span><span class="sxs-lookup"><span data-stu-id="ede71-121">If you've made manual adjustments to the statistical baseline forecast, the adjusted values are authorized for use, even if this check box is cleared.</span></span> <span data-ttu-id="ede71-122">Pärast autoriseerimist muudatusi siiski eiratakse.</span><span class="sxs-lookup"><span data-stu-id="ede71-122">However, the changes are discarded after the authorization.</span></span> <span data-ttu-id="ede71-123">Seepärast on järgmisel korral loodud prognoos ainult statistiline prognoos ega sisalda ühtki käsitsi tehtud korrigeerimist, isegi kui ruut **Kanna käsitsi tehtud korrigeerimised üle nõudluse prognoosi** on valitud.</span><span class="sxs-lookup"><span data-stu-id="ede71-123">Therefore, the next time that a forecast is generated, that forecast is only a statistical forecast and doesn't have any manual overrides, even if **Transfer manual adjustments to the demand forecast** is selected.</span></span> <span data-ttu-id="ede71-124">Seetõttu võite võtta ruutu **Salvesta nõudluse alusprognoosis käsitsi tehtud korrigeerimised** kui mehhanismi, mis laseb teil säilitada või hüljata kõik käsitsi tehtud muudatused.</span><span class="sxs-lookup"><span data-stu-id="ede71-124">Therefore, you can consider the **Save the manual adjustments made to the baseline demand forecast** check box a mechanism that lets you keep or discard all manual changes.</span></span>

<a name="additional-resources"></a><span data-ttu-id="ede71-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ede71-125">Additional resources</span></span>
--------

[<span data-ttu-id="ede71-126">Alusprognoosis käsitsi korrigeerimiste tegemine</span><span class="sxs-lookup"><span data-stu-id="ede71-126">Making manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="ede71-127">Prognoosi täpsuse jälgimine</span><span class="sxs-lookup"><span data-stu-id="ede71-127">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)




