---
title: Varude ajalise jaotuse aruanne
description: Selles teemas kirjeldatakse funktsiooni, mis võimaldab teil käitada varude ajalise jaotuse aruannet ja muuta tulemus kättesaadavaks nii vormi kui ka diagrammi kujul.
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810247"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="c3481-103">Varude ajalise jaotuse aruanne</span><span class="sxs-lookup"><span data-stu-id="c3481-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c3481-104">Rakenduses Microsoft Dynamics 365 Supply Chain Management saate käitada **Varude ajalise jaotuse** aruannet ja muuta tulemuse kättesaadavaks nii vormi kui ka diagrammi kujul.</span><span class="sxs-lookup"><span data-stu-id="c3481-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="c3481-105">Vormis reguleeritakse veerge ja koondsaldosid dünaamiliselt olenevalt konfigureeritud paigutusele.</span><span class="sxs-lookup"><span data-stu-id="c3481-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="c3481-106">Diagramm annab visuaalse ülevaate, mis toetab filtreerimist ja võimaldab teil üksikasjadesse süvitsi minna.</span><span class="sxs-lookup"><span data-stu-id="c3481-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="c3481-107">Lisaks võimaldab andmeüksus **Varude ajalise jaotuse aruanne** eksportida **Varude ajalise jaotuse** aruande käivitamise tulemusi vormingus, nagu Microsoft Exceli fail või PDF-fail.</span><span class="sxs-lookup"><span data-stu-id="c3481-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="c3481-108">Selline **Varude ajalise jaotuse** aruande käivitamise meetod on kasulik juhul, kui väljund sisaldab palju ridu.</span><span class="sxs-lookup"><span data-stu-id="c3481-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="c3481-109">Näiteks sisaldab väljund palju ridu, kui teil on 50 000 kaupa ja 300 poodi, mis on loodud ladudena, ning taotlete varude ajalist jaotumist kauba, tegevuskoha ja lao järgi.</span><span class="sxs-lookup"><span data-stu-id="c3481-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="c3481-110">Varude ajalise jaotuse aruande käivitamine</span><span class="sxs-lookup"><span data-stu-id="c3481-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="c3481-111">Avage **Kuluhaldus \> Päringud ja aruanded \> Lao varude ajalise jaotuse aruanne**.</span><span class="sxs-lookup"><span data-stu-id="c3481-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="c3481-112">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c3481-112">Select **New**.</span></span>
1. <span data-ttu-id="c3481-113">Väljale **Protsessi ID – nimi** sisestage aruandele kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="c3481-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="c3481-114">Valige aruanne **Identimine – ID** ja filtreerige seda vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="c3481-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="c3481-115">Aruande käivitamine toimub alati pakett-töös.</span><span class="sxs-lookup"><span data-stu-id="c3481-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="c3481-116">Pärast pakett-töö lõpetamist kuvatakse väljund lehel **Lao varude ajalise jaotuse aruanne**.</span><span class="sxs-lookup"><span data-stu-id="c3481-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="c3481-117">Kui soovite vaadata väljundit vormina, millel on traditsiooniline ruudustiku paigutus, valige **Kuva üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="c3481-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="c3481-118">Väljundi koonddiagrammina vaatamiseks valige **Kuva diagramm**.</span><span class="sxs-lookup"><span data-stu-id="c3481-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c3481-119">Vorm ei sisalda aruande paigutuses määratletud vahesummasid.</span><span class="sxs-lookup"><span data-stu-id="c3481-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="c3481-120">Andmeüksus **Varude ajalise jaotuse aruanne** võimaldab teil eksportida **Varude ajalise jaotuse** aruande väljundi, rakendades välja **Protsessi ID – nimi** filtri mis tahes vormile, mida andmehaldus toetab.</span><span class="sxs-lookup"><span data-stu-id="c3481-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
