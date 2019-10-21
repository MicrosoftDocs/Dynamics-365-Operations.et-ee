---
title: Töölehel hilinenud maksu arvutamise lubamine
description: See teema selgitab, kuidas kasutada funktsiooni **Töölehel hilinenud maksu arvutamise lubamine**, et parandada maksude arvutamise jõudlust töölehe ridade suure mahu korral.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177310"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="22103-103">Töölehel hilinenud maksu arvutamise lubamine</span><span class="sxs-lookup"><span data-stu-id="22103-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="22103-104">See teema selgitab, kuidas kasutada funktsiooni **Töölehel hilinenud maksu arvutamise lubamine**, et parandada maksude arvutamise jõudlust töölehe ridade suure mahu korral.</span><span class="sxs-lookup"><span data-stu-id="22103-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="22103-105">Praeguse käibemaksu arvutamise käitumine käivitatakse töölehel reaalajas, kui kasutaja uuendab maksuga seotud välju, nt käibemaksugrupp/kauba käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="22103-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="22103-106">Iga töölehe uuendamine rea tasemel, arvutab maksusumma uuesti kõigil töölehe ridadel.</span><span class="sxs-lookup"><span data-stu-id="22103-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="22103-107">See aitab kasutajal näha reaalajas arvutatud maksusummat, kuid see võib tekitada ka jõudluse probleemi töölehe ridade suure mahu korral.</span><span class="sxs-lookup"><span data-stu-id="22103-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="22103-108">See funktsioon annab võimaluse jõudluse probleemi lahendamiseks viivitada maksude arvutamisega.</span><span class="sxs-lookup"><span data-stu-id="22103-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="22103-109">Kui see funktsioon on sisse lülitatud, arvutatakse maksusumma ainult siis, kui kasutaja klõpsab käsku "Käibemaks" või sisestab töölehe.</span><span class="sxs-lookup"><span data-stu-id="22103-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="22103-110">Kasutaja saab parameetri sisse/välja lülitada kolmel tasandil.</span><span class="sxs-lookup"><span data-stu-id="22103-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="22103-111">Juriidilise isiku järgi</span><span class="sxs-lookup"><span data-stu-id="22103-111">By legal entity</span></span>
- <span data-ttu-id="22103-112">Töölehe nime järgi</span><span class="sxs-lookup"><span data-stu-id="22103-112">By journal name</span></span>
- <span data-ttu-id="22103-113">Töölehe päise järgi</span><span class="sxs-lookup"><span data-stu-id="22103-113">By journal header</span></span>

<span data-ttu-id="22103-114">Süsteem käsitleb töölehe päise parameetrit lõplikuna.</span><span class="sxs-lookup"><span data-stu-id="22103-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="22103-115">Töölehe päise parameetri väärtus tuletatakse vaikimisi töölehe nimest.</span><span class="sxs-lookup"><span data-stu-id="22103-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="22103-116">Töölehe nime parameetri väärtus tuletatakse töölehe nime loomisel vaikimisi pearaamatu parameetrist.</span><span class="sxs-lookup"><span data-stu-id="22103-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="22103-117">Töölehe väljad „Tegelik käibemaksusumma” ja „Arvutatud käibemaksu summa" peidetakse, kui see parameeter on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="22103-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="22103-118">Eesmärk on kasutajat mitte eksitada, kuna nende kahe välja väärtus näitab alati 0, enne kui kasutaja käivitab maksu arvutamise.</span><span class="sxs-lookup"><span data-stu-id="22103-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="22103-119">Hilinenud maksu arvutamise lubamine juriidilise isiku järgi</span><span class="sxs-lookup"><span data-stu-id="22103-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="22103-120">Avage **Pearaamat > Pearaamatu seadistamine > Pearaamatu parameetrid**</span><span class="sxs-lookup"><span data-stu-id="22103-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="22103-121">Klõpsake suvandit **Käibemaks**.</span><span class="sxs-lookup"><span data-stu-id="22103-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="22103-122">Leidke kiirkaardilt **Üldine** parameeter **Hilinenud maksu arvutamine**, lülitage see sisse/välja</span><span class="sxs-lookup"><span data-stu-id="22103-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="22103-123">Hilinenud maksu arvutamise lubamine töölehe nime järgi</span><span class="sxs-lookup"><span data-stu-id="22103-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="22103-124">Avage **Pearaamat > Töölehe seadistamine > Töölehtede nimed**</span><span class="sxs-lookup"><span data-stu-id="22103-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="22103-125">Leidke kiirkaardilt **Üldine** parameeter **Hilinenud maksu arvutamine**, lülitage see sisse/välja</span><span class="sxs-lookup"><span data-stu-id="22103-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="22103-126">Hilinenud maksu arvutamise lubamine töölehe järgi</span><span class="sxs-lookup"><span data-stu-id="22103-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="22103-127">Avage **Pearaamat > Töölehe kanded > Päevaraamatud**</span><span class="sxs-lookup"><span data-stu-id="22103-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="22103-128">Klõpsake valikut **Uus**</span><span class="sxs-lookup"><span data-stu-id="22103-128">Click **New**</span></span>
3. <span data-ttu-id="22103-129">Valige töölehe nimi.</span><span class="sxs-lookup"><span data-stu-id="22103-129">Select a journal name</span></span>
4. <span data-ttu-id="22103-130">Klõpsake **Häälestus**</span><span class="sxs-lookup"><span data-stu-id="22103-130">Click **Setup**</span></span>
5. <span data-ttu-id="22103-131">Leidke parameeter **Hilinenud maksu arvutamine**, lülitage see sisse/välja</span><span class="sxs-lookup"><span data-stu-id="22103-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
