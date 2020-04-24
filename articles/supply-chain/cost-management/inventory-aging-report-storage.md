---
title: Varude ajalise jaotuse aruanne
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
ms.openlocfilehash: 790c8fe3a52bce652227f1cef97eff6496476100
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201614"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="f2767-103">Varude ajalise jaotuse aruanne</span><span class="sxs-lookup"><span data-stu-id="f2767-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="f2767-104">Rakenduses Microsoft Dynamics 365 Supply Chain Management saate käitada **Varude ajalise jaotuse** aruannet ja muuta tulemuse kättesaadavaks nii vormi kui ka diagrammi kujul.</span><span class="sxs-lookup"><span data-stu-id="f2767-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="f2767-105">Vormis reguleeritakse veerge ja koondsaldosid dünaamiliselt olenevalt konfigureeritud paigutusele.</span><span class="sxs-lookup"><span data-stu-id="f2767-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="f2767-106">Diagramm annab visuaalse ülevaate, mis toetab filtreerimist ja võimaldab teil üksikasjadesse süvitsi minna.</span><span class="sxs-lookup"><span data-stu-id="f2767-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="f2767-107">Lisaks võimaldab andmeüksus **Varude ajalise jaotuse aruanne** eksportida **Varude ajalise jaotuse** aruande käivitamise tulemusi vormingus, nagu Microsoft Exceli fail või PDF-fail.</span><span class="sxs-lookup"><span data-stu-id="f2767-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="f2767-108">Selline **Varude ajalise jaotuse** aruande käivitamise meetod on kasulik juhul, kui väljund sisaldab palju ridu.</span><span class="sxs-lookup"><span data-stu-id="f2767-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="f2767-109">Näiteks sisaldab väljund palju ridu, kui teil on 50 000 kaupa ja 300 poodi, mis on loodud ladudena, ning taotlete varude ajalist jaotumist kauba, tegevuskoha ja lao järgi.</span><span class="sxs-lookup"><span data-stu-id="f2767-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="f2767-110">Varude ajalise jaotuse aruande käivitamine</span><span class="sxs-lookup"><span data-stu-id="f2767-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="f2767-111">Avage **Kuluhaldus \> Päringud ja aruanded \> Lao varude ajalise jaotuse aruanne**.</span><span class="sxs-lookup"><span data-stu-id="f2767-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="f2767-112">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f2767-112">Select **New**.</span></span>
1. <span data-ttu-id="f2767-113">Väljale **Protsessi ID – nimi** sisestage aruandele kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="f2767-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="f2767-114">Valige aruanne **Identimine – ID** ja filtreerige seda vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="f2767-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="f2767-115">Aruande käivitamine toimub alati pakett-töös.</span><span class="sxs-lookup"><span data-stu-id="f2767-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="f2767-116">Pärast pakett-töö lõpetamist kuvatakse väljund lehel **Lao varude ajalise jaotuse aruanne**.</span><span class="sxs-lookup"><span data-stu-id="f2767-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="f2767-117">Kui soovite vaadata väljundit vormina, millel on traditsiooniline ruudustiku paigutus, valige **Kuva üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="f2767-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="f2767-118">Väljundi koonddiagrammina vaatamiseks valige **Kuva diagramm**.</span><span class="sxs-lookup"><span data-stu-id="f2767-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f2767-119">Vorm ei sisalda aruande paigutuses määratletud vahesummasid.</span><span class="sxs-lookup"><span data-stu-id="f2767-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="f2767-120">Andmeüksus **Varude ajalise jaotuse aruanne** võimaldab teil eksportida **Varude ajalise jaotuse** aruande väljundi, rakendades välja **Protsessi ID – nimi** filtri mis tahes vormile, mida andmehaldus toetab.</span><span class="sxs-lookup"><span data-stu-id="f2767-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
