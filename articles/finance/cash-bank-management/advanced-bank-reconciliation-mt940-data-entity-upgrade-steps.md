---
title: Täpsem panga vastavusseviimise MT940 import – liitandmeüksuse täiendamise etapid
description: Järjekorranumber tuleb lisada pangaväljavõtte impordiüksusele, et toetada MT940 vormingut.
author: panolte
manager: AnnBe
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ee5ad476b10077592c61f6827b5596a1b3e66cd6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217430"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="d2b85-103">Täpsem panga vastavusseviimise MT940 import – liitandmeüksuse täiendamise etapid</span><span class="sxs-lookup"><span data-stu-id="d2b85-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2b85-104">Järjekorranumber tuleb lisada pangaväljavõtte impordiüksusele, et toetada MT940 vormingut.</span><span class="sxs-lookup"><span data-stu-id="d2b85-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="d2b85-105">Kasutage järgmiseid etappe, et lisada pangaväljavõtte impordiüksus MT940 vormingu toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="d2b85-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="d2b85-106">Kompileerige ja sünkroonige järgmine:</span><span class="sxs-lookup"><span data-stu-id="d2b85-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="d2b85-107">Liitüksus\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="d2b85-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="d2b85-108">Üksus\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="d2b85-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="d2b85-109">Üksus\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="d2b85-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="d2b85-110">Üksus\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="d2b85-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="d2b85-111">Üksus\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="d2b85-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="d2b85-112">Tabelid\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="d2b85-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="d2b85-113">Andmehaldus\\andmeprojektid.</span><span class="sxs-lookup"><span data-stu-id="d2b85-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="d2b85-114">MT940 importimisprojekti(de) laadimine</span><span class="sxs-lookup"><span data-stu-id="d2b85-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="d2b85-115">Muutke XSLT-d.</span><span class="sxs-lookup"><span data-stu-id="d2b85-115">Change XSLT.</span></span>
            -   <span data-ttu-id="d2b85-116">Klõpsake suvandit **Kuva kaart**.</span><span class="sxs-lookup"><span data-stu-id="d2b85-116">Click **View map**.</span></span>
            -   <span data-ttu-id="d2b85-117">Klõpsake pangaväljavõtte dokumendi valikut **Kuva kaart**.</span><span class="sxs-lookup"><span data-stu-id="d2b85-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="d2b85-118">Klõpsake valikut **Teisendused**</span><span class="sxs-lookup"><span data-stu-id="d2b85-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="d2b85-119">Kustutage fail BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="d2b85-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="d2b85-120">Lisage faili BankReconiliation-to-Composite.xsl uus versioon.</span><span class="sxs-lookup"><span data-stu-id="d2b85-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="d2b85-121">Avage valik **Seerianumber** paigutuses **Lähteandmed**.</span><span class="sxs-lookup"><span data-stu-id="d2b85-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="d2b85-122">Lähteandmete vorming = XML-Element.</span><span class="sxs-lookup"><span data-stu-id="d2b85-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="d2b85-123">Üksuse nimetus = Pangaväljavõtted.</span><span class="sxs-lookup"><span data-stu-id="d2b85-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="d2b85-124">Andmefaili üleslaadimise = uus faili SampleBankCompositeEntity.xml versioon.</span><span class="sxs-lookup"><span data-stu-id="d2b85-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="d2b85-125">Klõpsake valikut **Jah**, et olemasolev fail üle kirjutada.</span><span class="sxs-lookup"><span data-stu-id="d2b85-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="d2b85-126">Klõpsake valikut **Jah**, et luua uus vastendus.</span><span class="sxs-lookup"><span data-stu-id="d2b85-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="d2b85-127">Kontrollige, kas **Seerianumber** on vastendatud.</span><span class="sxs-lookup"><span data-stu-id="d2b85-127">Verify that S **equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="d2b85-128">Klõpsake väljavõtte üksust **Kuva kaart**.</span><span class="sxs-lookup"><span data-stu-id="d2b85-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="d2b85-129">Kontrollige, kas **SequenceNumber** on vastendatud valikult Allikas valikule Ajastamine.</span><span class="sxs-lookup"><span data-stu-id="d2b85-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="d2b85-130">Importige uus väljavõte.</span><span class="sxs-lookup"><span data-stu-id="d2b85-130">Import the new statement.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]