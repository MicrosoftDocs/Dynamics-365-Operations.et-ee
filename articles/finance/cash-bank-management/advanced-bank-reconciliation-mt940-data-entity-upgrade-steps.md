---
title: Täpsem panga vastavusseviimise MT940 import – liitandmeüksuse täiendamise etapid
description: Järjekorranumber tuleb lisada pangaväljavõtte impordiüksusele, et toetada MT940 vormingut.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 91100c3e3c33462e5b19ca239a784cdb720210ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772003"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="31c3f-103">Täpsem panga vastavusseviimise MT940 import – liitandmeüksuse täiendamise etapid</span><span class="sxs-lookup"><span data-stu-id="31c3f-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31c3f-104">Järjekorranumber tuleb lisada pangaväljavõtte impordiüksusele, et toetada MT940 vormingut.</span><span class="sxs-lookup"><span data-stu-id="31c3f-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="31c3f-105">Kasutage järgmiseid etappe, et lisada pangaväljavõtte impordiüksus MT940 vormingu toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="31c3f-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="31c3f-106">Kompileerige ja sünkroonige järgmine:</span><span class="sxs-lookup"><span data-stu-id="31c3f-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="31c3f-107">Liitüksus\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="31c3f-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="31c3f-108">Üksus\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="31c3f-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="31c3f-109">Üksus\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="31c3f-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="31c3f-110">Üksus\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="31c3f-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="31c3f-111">Üksus\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="31c3f-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="31c3f-112">Tabelid\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="31c3f-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="31c3f-113">Andmehaldus\\andmeprojektid.</span><span class="sxs-lookup"><span data-stu-id="31c3f-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="31c3f-114">MT940 importimisprojekti(de) laadimine</span><span class="sxs-lookup"><span data-stu-id="31c3f-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="31c3f-115">Muutke XSLT-d.</span><span class="sxs-lookup"><span data-stu-id="31c3f-115">Change XSLT.</span></span>
            -   <span data-ttu-id="31c3f-116">Klõpsake suvandit **Kuva kaart**.</span><span class="sxs-lookup"><span data-stu-id="31c3f-116">Click **View map**.</span></span>
            -   <span data-ttu-id="31c3f-117">Klõpsake pangaväljavõtte dokumendi valikut **Kuva kaart**.</span><span class="sxs-lookup"><span data-stu-id="31c3f-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="31c3f-118">Klõpsake valikut **Teisendused**</span><span class="sxs-lookup"><span data-stu-id="31c3f-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="31c3f-119">Kustutage fail BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="31c3f-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="31c3f-120">Lisage faili BankReconiliation-to-Composite.xsl uus versioon.</span><span class="sxs-lookup"><span data-stu-id="31c3f-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="31c3f-121">Avage valik **Seerianumber** paigutuses **Lähteandmed**.</span><span class="sxs-lookup"><span data-stu-id="31c3f-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="31c3f-122">Lähteandmete vorming = XML-Element.</span><span class="sxs-lookup"><span data-stu-id="31c3f-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="31c3f-123">Üksuse nimetus = Pangaväljavõtted.</span><span class="sxs-lookup"><span data-stu-id="31c3f-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="31c3f-124">Andmefaili üleslaadimise = uus faili SampleBankCompositeEntity.xml versioon.</span><span class="sxs-lookup"><span data-stu-id="31c3f-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="31c3f-125">Klõpsake valikut **Jah**, et olemasolev fail üle kirjutada.</span><span class="sxs-lookup"><span data-stu-id="31c3f-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="31c3f-126">Klõpsake valikut **Jah**, et luua uus vastendus.</span><span class="sxs-lookup"><span data-stu-id="31c3f-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="31c3f-127">Kontrollige, kas **Seerianumber** on vastendatud.</span><span class="sxs-lookup"><span data-stu-id="31c3f-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="31c3f-128">Klõpsake väljavõtte üksust **Kuva kaart**.</span><span class="sxs-lookup"><span data-stu-id="31c3f-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="31c3f-129">Kontrollige, kas **SequenceNumber** on vastendatud valikult Allikas valikule Ajastamine.</span><span class="sxs-lookup"><span data-stu-id="31c3f-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="31c3f-130">Importige uus väljavõte.</span><span class="sxs-lookup"><span data-stu-id="31c3f-130">Import the new statement.</span></span>




