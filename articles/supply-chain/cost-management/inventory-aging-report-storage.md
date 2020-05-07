---
title: Varude ajalise jaotuse aruande talletamine
description: Selles teemas kirjeldatakse funktsiooni, mis võimaldab teil käitada varude ajalise jaotuse aruannet ja muuta tulemus kättesaadavaks nii vormi kui ka diagrammi kujul.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9148a9032615222a1fdfe453488e716bacadbabc
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275575"
---
# <a name="inventory-aging-report-storage"></a><span data-ttu-id="ca83d-103">Varude ajalise jaotuse aruande talletamine</span><span class="sxs-lookup"><span data-stu-id="ca83d-103">Inventory aging report storage</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="ca83d-104">Rakenduses Microsoft Dynamics 365 Supply Chain Management saate käitada **Varude ajalise jaotuse aruande talletamise** aruande ja muuta tulemuse kättesaadavaks nii vormi kui ka diagrammi kujul.</span><span class="sxs-lookup"><span data-stu-id="ca83d-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging report storage** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="ca83d-105">Vormis reguleeritakse veerge ja koondsaldosid dünaamiliselt olenevalt konfigureeritud paigutusele.</span><span class="sxs-lookup"><span data-stu-id="ca83d-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="ca83d-106">Diagramm annab visuaalse ülevaate, mis toetab filtreerimist ja võimaldab teil üksikasjadesse süvitsi minna.</span><span class="sxs-lookup"><span data-stu-id="ca83d-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="ca83d-107">Lisaks võimaldab andmeüksus **Varude ajalise jaotuse aruanne** eksportida **Varude ajalise jaotuse aruande talletamise** aruande käivitamise tulemusi vormingus, nagu Microsoft Exceli fail või PDF-fail.</span><span class="sxs-lookup"><span data-stu-id="ca83d-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging report storage** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="ca83d-108">Selline **Varude ajalise jaotuse aruande talletamise** aruande käivitamise meetod on kasulik juhul, kui väljund sisaldab palju ridu.</span><span class="sxs-lookup"><span data-stu-id="ca83d-108">This method of running an **Inventory aging report storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="ca83d-109">Näiteks sisaldab väljund palju ridu, kui teil on 50 000 kaupa ja 300 poodi, mis on loodud ladudena, ning taotlete varude ajalist jaotumist kauba, tegevuskoha ja lao järgi.</span><span class="sxs-lookup"><span data-stu-id="ca83d-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="enable-the-inventory-value-storage-report-feature"></a><span data-ttu-id="ca83d-110">Lubage funktsioon „Varude väärtuse talletuse aruanne”</span><span class="sxs-lookup"><span data-stu-id="ca83d-110">Enable the Inventory value storage report feature</span></span>

<span data-ttu-id="ca83d-111">Enne selle funktsiooni kasutamist peate selle oma süsteemis lubama.</span><span class="sxs-lookup"><span data-stu-id="ca83d-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="ca83d-112">Administraatorid saavad kasutada [funktsioonide halduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajaduse korral see lubada.</span><span class="sxs-lookup"><span data-stu-id="ca83d-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="ca83d-113">Siin on funktsioon loetletud järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ca83d-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="ca83d-114">**Moodul** – kuluhaldus</span><span class="sxs-lookup"><span data-stu-id="ca83d-114">**Module** - Cost management</span></span>
- <span data-ttu-id="ca83d-115">**Funktsiooni nimi** – varude ajalise jaotuse aruande talletamine</span><span class="sxs-lookup"><span data-stu-id="ca83d-115">**Feature name** - Inventory aging report storage</span></span>

## <a name="run-an-inventory-aging-report-storage"></a><span data-ttu-id="ca83d-116">Varude ajalise jaotuse aruande talletamise käitamine</span><span class="sxs-lookup"><span data-stu-id="ca83d-116">Run an Inventory aging report storage</span></span>

1. <span data-ttu-id="ca83d-117">Avage **Kuluhaldus \> Päringud ja aruanded \> Lao varude ajalise jaotuse aruanne**.</span><span class="sxs-lookup"><span data-stu-id="ca83d-117">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="ca83d-118">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ca83d-118">Select **New**.</span></span>
1. <span data-ttu-id="ca83d-119">Väljale **Protsessi ID – nimi** sisestage aruandele kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="ca83d-119">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="ca83d-120">Valige aruanne **Identimine – ID** ja filtreerige seda vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="ca83d-120">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="ca83d-121">Aruande käivitamine toimub alati pakett-töös.</span><span class="sxs-lookup"><span data-stu-id="ca83d-121">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="ca83d-122">Pärast pakett-töö lõpetamist kuvatakse väljund lehel **Lao varude ajalise jaotuse aruanne**.</span><span class="sxs-lookup"><span data-stu-id="ca83d-122">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="ca83d-123">Kui soovite vaadata väljundit vormina, millel on traditsiooniline ruudustiku paigutus, valige **Kuva üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="ca83d-123">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="ca83d-124">Väljundi koonddiagrammina vaatamiseks valige **Kuva diagramm**.</span><span class="sxs-lookup"><span data-stu-id="ca83d-124">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ca83d-125">Vorm ei sisalda aruande paigutuses määratletud vahesummasid.</span><span class="sxs-lookup"><span data-stu-id="ca83d-125">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="ca83d-126">Andmeüksus **Varude ajalise jaotuse aruanne** võimaldab teil eksportida **Varude ajalise jaotuse aruande talletamise** aruande väljundi, rakendades välja **Protsessi ID – nimi** filtri mis tahes vormile, mida andmehaldus toetab.</span><span class="sxs-lookup"><span data-stu-id="ca83d-126">The **Inventory aging report** data entity lets you export the output of an **Inventory aging report storage** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
