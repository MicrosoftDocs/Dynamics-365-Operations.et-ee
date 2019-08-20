---
title: Pearaamatupidaja tööruumile finantsdimensioonide lisamine
description: Selles teemas selgitatakse, kuidas lisada pearaamatupidaja tööruumi finantsdimensioonid, et neid saaks kasutada pearaamatu ja eelarvearuannetes.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 508b491218ee0a09794371aeccd2d190735b3ab9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839685"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="6b964-103">Pearaamatupidaja tööruumile finantsdimensioonide lisamine</span><span class="sxs-lookup"><span data-stu-id="6b964-103">Add financial dimensions to the CFO workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b964-104">Selles teemas selgitatakse, kuidas lisada pearaamatupidaja tööruumi finantsdimensioone, et neid saaks kasutada pearaamatu- ja eelarvearuannetes.</span><span class="sxs-lookup"><span data-stu-id="6b964-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="6b964-105">Pearaamatupidaja tööruumis on vahekaart **Ülevaade** ja vahekaart **Finants**. Nendel vahekaartidel kuvatavad aruanded põhinevad kahel mõõdikul: LedgerActivityMeasure ja BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="6b964-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="6b964-106">Rakenduses Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juuli 2017) on nende mõõtude ja üksuse DimensionCombinationEntity vahel seos.</span><span class="sxs-lookup"><span data-stu-id="6b964-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="6b964-107">Seega saate valida dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="6b964-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="6b964-108">Uuendage rakenduse Finance and Operations lehel **Üksuse pood** mõõdikud **LedgerActivityMeasure** ja **BudgetActivityMeasure**.</span><span class="sxs-lookup"><span data-stu-id="6b964-108">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="6b964-109">Avage rakenduses Microsoft Visual Studio rakenduste sirvija ja otsige rakendust **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="6b964-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="6b964-110">Jaotises **Ressursid** avage rakendus **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="6b964-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="6b964-111">Kui ressurss avaneb Microsoft Power BI töölaual, siis valige käsk **Too andmed**, seejärel valige suvand **SQL serveri andmebaas** ja seejärel suvand **Ühenda**.</span><span class="sxs-lookup"><span data-stu-id="6b964-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="6b964-112">Sisestage serveri nimi ja seejärel sisestage andmebaasi väljale **AxDW**.</span><span class="sxs-lookup"><span data-stu-id="6b964-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="6b964-113">Valige käsk **DirectQuery** ja seejärel valige käsk **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b964-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="6b964-114">Otsige ja valige tulemiloendist **LedgerActivityMeasure\_DimensionCombination** ja seejärel valige käsk **Laadi**.</span><span class="sxs-lookup"><span data-stu-id="6b964-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="6b964-115">Loendis **Väljad** pange tabelile nimeks **Finantsdimensioonid**, et seda oleks lihtsam tuvastada.</span><span class="sxs-lookup"><span data-stu-id="6b964-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="6b964-116">Valige jaotis **Seoste haldamine** ja seejärel valige käsk **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6b964-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="6b964-117">Valige esimesel väljal väärtus **Pearaamatu toimingud** ja seejärel valige väärtus **LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="6b964-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="6b964-118">Teisel väljal valige väärtus **LedgerActivityMeasure\_DimensionCombination** (või **Finantsdimensioonid**, kui panite tabelile selle nime).</span><span class="sxs-lookup"><span data-stu-id="6b964-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="6b964-119">Valige päis **DimensionCombinationRECID**.</span><span class="sxs-lookup"><span data-stu-id="6b964-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="6b964-120">Väljal **Kardinaalsus** valige väärtus **Mitu ühele**.</span><span class="sxs-lookup"><span data-stu-id="6b964-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="6b964-121">Määrake välja **Ristfiltri suund** väärtuseks **Üks**.</span><span class="sxs-lookup"><span data-stu-id="6b964-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="6b964-122">Valige käsud **Muuda seos aktiivseks** ja **Eelda viiteterviklust**, klõpsake nuppu **OK** ja seejärel nuppu **Sule**.</span><span class="sxs-lookup"><span data-stu-id="6b964-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="6b964-123">[![Seose loomine](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="6b964-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="6b964-124">Loendis **Väljad** peaksite nägema tabelit ja saadaolevaid finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="6b964-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="6b964-125">Lohistage soovitud finantsdimensioonid aruandetaseme filtrite juurde.</span><span class="sxs-lookup"><span data-stu-id="6b964-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="6b964-126">Salvestage muudatused.</span><span class="sxs-lookup"><span data-stu-id="6b964-126">Save your changes.</span></span>
15. <span data-ttu-id="6b964-127">Paremklõpsake rakendusobjektide puul (AOT) projekti ja seejärel nuppu **Sünkrooni**.</span><span class="sxs-lookup"><span data-stu-id="6b964-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="6b964-128">Looge projekt ja seejärel avage tulemuste vaatamiseks rakendus.</span><span class="sxs-lookup"><span data-stu-id="6b964-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="6b964-129">[![Valmis tööruum](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="6b964-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>
