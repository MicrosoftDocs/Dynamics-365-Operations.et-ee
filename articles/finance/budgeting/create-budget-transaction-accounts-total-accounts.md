---
title: Eelarve loomine kandekontodelt ja summakontodelt
description: Selles artiklis antakse ülevaade koondkontode alusel eelarvete loomise protsessist. Lisaks selgitatakse, kuidas koondkontode jaoks eelarve juhtimine sisse lülitada, kui eelarve juhtimine on nõutav.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f60963bee790737c85161dff03278df0572e3abc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177383"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="668a2-104">Eelarve loomine kandekontodelt ja summakontodelt</span><span class="sxs-lookup"><span data-stu-id="668a2-104">Create a budget from transaction accounts and total accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="668a2-105">Selles artiklis antakse ülevaade koondkontode alusel eelarvete loomise protsessist.</span><span class="sxs-lookup"><span data-stu-id="668a2-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="668a2-106">Lisaks selgitatakse, kuidas koondkontode jaoks eelarve juhtimine sisse lülitada, kui eelarve juhtimine on nõutav.</span><span class="sxs-lookup"><span data-stu-id="668a2-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="668a2-107">Nii eelarveplaani kui ka eelarveregistri kande dokumendid võimaldavad eelarve koostamist põhikontodel, mille põhikonto tüübiks on **Kogusumma**.</span><span class="sxs-lookup"><span data-stu-id="668a2-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="668a2-108">Tegelikud summad saab sisestada ainult ülekande põhikontodele.</span><span class="sxs-lookup"><span data-stu-id="668a2-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="668a2-109">Perioodilise protsessi **Eelarveplaani loomine pearaamatust** puhul saate vahekaardil **Allikas** määrata kriteeriumina põhikonto tüübi **Kogusumma**.</span><span class="sxs-lookup"><span data-stu-id="668a2-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="668a2-110">Sellisel juhul kaasatakse iga kogusumma põhikonto sihteelarveplaani ja summa on võrdne valitud põhikontode vahemiku kogusummaga.</span><span class="sxs-lookup"><span data-stu-id="668a2-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="668a2-111">Saate aktiveerida eelarve juhtimise tüübiga **Kogusumma** põhikontode puhul.</span><span class="sxs-lookup"><span data-stu-id="668a2-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="668a2-112">Seda funktsiooni toetatakse eelarvegruppide abil.</span><span class="sxs-lookup"><span data-stu-id="668a2-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="668a2-113">Iga kogusumma põhikonto puhul tuleb eelarvegrupi puhul juhitav eelarve luua lehel **Eelarve juhtimise konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="668a2-113">For each total main account, the budget that should be controlled for a budget group must be created on the \*\*Budget control configuration \*\*page.</span></span> <span data-ttu-id="668a2-114">Teie määratud kriteeriumid peavad sisaldama kogusumma põhikontot ja kontode vahemikku.</span><span class="sxs-lookup"><span data-stu-id="668a2-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="668a2-115">Eelarvegruppide loomise protsessi kiirendamiseks saate kasutada andmeüksust Eelarve juhtimise grupid.</span><span class="sxs-lookup"><span data-stu-id="668a2-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="668a2-116">Eelarve kasutamisel aruandluses (nt finantsaruandes) koosneb kogusummat kajastav eelarvesumma järgmistest summadest:</span><span class="sxs-lookup"><span data-stu-id="668a2-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="668a2-117">eelarvetest, mis on loodud igast kande pearaamatukontost summakonto intervalli jooksul;</span><span class="sxs-lookup"><span data-stu-id="668a2-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="668a2-118">eelarvesummast, mis on sisestatud otse summakontole.</span><span class="sxs-lookup"><span data-stu-id="668a2-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="668a2-119">Seega saate luua eraldi eelarved summakonto intervalli olulisimate kandekontode puhul ja lisada seejärel saadaoleva eelarvesumma summakontole.</span><span class="sxs-lookup"><span data-stu-id="668a2-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>


