---
title: "Pearaamatupidaja tööruumile finantsdimensioonide lisamine"
description: "Selles teemas selgitatakse, kuidas lisada pearaamatupidaja tööruumi finantsdimensioonid, et neid saaks kasutada pearaamatu ja eelarvearuannetes."
author: aolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.2.0
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 05fd7ce5293b3a300aabc073a6e492c5804d1897
ms.contentlocale: et-ee
ms.lasthandoff: 08/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="9d47f-103">Pearaamatupidaja tööruumile finantsdimensioonide lisamine</span><span class="sxs-lookup"><span data-stu-id="9d47f-103">Add financial dimensions to the CFO workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9d47f-104">Selles teemas selgitatakse, kuidas lisada pearaamatupidaja tööruumi finantsdimensioone, et neid saaks kasutada pearaamatu- ja eelarvearuannetes.</span><span class="sxs-lookup"><span data-stu-id="9d47f-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="9d47f-105">Pearaamatupidaja tööruumil on vahekaart **Ülevaade** ja vahekaart **Finants**.</span><span class="sxs-lookup"><span data-stu-id="9d47f-105">The CFO workspace has an **Overview** tab and a **Financial** tab.</span></span> <span data-ttu-id="9d47f-106">Nendel vahekaartidel kuvatavad aruanded põhinevad kahel mõõdikul: LedgerActivityMeasure ja BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="9d47f-106">The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="9d47f-107">Rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition juuli 2017 uuenduses on nende mõõdikute ja DimensionCombinationEntity üksuse vahel seoste kogum.</span><span class="sxs-lookup"><span data-stu-id="9d47f-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="9d47f-108">Seega saate valida dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="9d47f-108">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="9d47f-109">Uuendage rakenduse Finance and Operations lehel **Üksuse pood** mõõdikud **LedgerActivityMeasure** ja **BudgetActivityMeasure**.</span><span class="sxs-lookup"><span data-stu-id="9d47f-109">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="9d47f-110">Avage rakenduses Microsoft Visual Studio rakenduste sirvija ja otsige rakendust **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="9d47f-110">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="9d47f-111">Jaotises **Ressursid** avage rakendus **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="9d47f-111">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="9d47f-112">Kui ressurss avaneb Microsoft Power BI töölaual, siis valige käsk **Too andmed**, seejärel valige käsk **SQL serveri andmebaas** ja siis klõpsake nuppu **Ühenda**.</span><span class="sxs-lookup"><span data-stu-id="9d47f-112">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="9d47f-113">Sisestage serveri nimi ja seejärel sisestage andmebaasi väljale **AxDW**.</span><span class="sxs-lookup"><span data-stu-id="9d47f-113">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="9d47f-114">Valige käsk **DirectQuery** ja seejärel valige käsk **OK**.</span><span class="sxs-lookup"><span data-stu-id="9d47f-114">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="9d47f-115">Otsige ja valige tulemiloendist **LedgerActivityMeasure\_DimensionCombination** ja seejärel valige käsk **Laadi**.</span><span class="sxs-lookup"><span data-stu-id="9d47f-115">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="9d47f-116">Loendis **Väljad** pange tabelile nimeks **Finantsdimensioonid**, et seda oleks lihtsam tuvastada.</span><span class="sxs-lookup"><span data-stu-id="9d47f-116">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="9d47f-117">Valige jaotis **Seoste haldamine** ja seejärel valige käsk **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9d47f-117">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="9d47f-118">Valige esimesel väljal väärtus **Pearaamatu toimingud** ja seejärel valige väärtus **LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="9d47f-118">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="9d47f-119">Teisel väljal valige väärtus **LedgerActivityMeasure\_DimensionCombination** (või **Finantsdimensioonid**, kui panite tabelile selle nime).</span><span class="sxs-lookup"><span data-stu-id="9d47f-119">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="9d47f-120">Valige päis **DimensionCombinationRECID**.</span><span class="sxs-lookup"><span data-stu-id="9d47f-120">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="9d47f-121">Väljal **Kardinaalsus** valige väärtus **Mitu ühele**.</span><span class="sxs-lookup"><span data-stu-id="9d47f-121">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="9d47f-122">Määrake välja **Ristfiltri suund** väärtuseks **Üks**.</span><span class="sxs-lookup"><span data-stu-id="9d47f-122">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="9d47f-123">Valige käsud **Muuda seos aktiivseks** ja **Eelda viiteterviklust**, klõpsake nuppu **OK** ja seejärel nuppu **Sule**.</span><span class="sxs-lookup"><span data-stu-id="9d47f-123">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="9d47f-124">[![Seose loomine](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="9d47f-124">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="9d47f-125">Loendis **Väljad** peaksite nägema tabelit ja saadaolevaid finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="9d47f-125">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="9d47f-126">Lohistage soovitud finantsdimensioonid aruandetaseme filtrite juurde.</span><span class="sxs-lookup"><span data-stu-id="9d47f-126">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="9d47f-127">Salvestage muudatused.</span><span class="sxs-lookup"><span data-stu-id="9d47f-127">Save your changes.</span></span>
15. <span data-ttu-id="9d47f-128">Paremklõpsake rakendusobjektide puul (AOT) projekti ja seejärel nuppu **Sünkrooni**.</span><span class="sxs-lookup"><span data-stu-id="9d47f-128">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="9d47f-129">Looge projekt ja seejärel avage tulemuste vaatamiseks rakendus.</span><span class="sxs-lookup"><span data-stu-id="9d47f-129">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="9d47f-130">[![Valmis tööruum](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="9d47f-130">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

