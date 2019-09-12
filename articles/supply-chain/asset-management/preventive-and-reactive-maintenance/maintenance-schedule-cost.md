---
title: Hooldusgraafiku kulu
description: Selles teemas selgitatakse hooldusgraafiku kulu varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 71b958839a914d90a86a0dcd16a09285ca6dcfa4
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875599"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="53a33-103">Hooldusgraafiku kulu</span><span class="sxs-lookup"><span data-stu-id="53a33-103">Maintenance schedule cost</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="53a33-104">Varahalduses saate arvutada hooldusgraafiku ridade eelarve kulusid.</span><span class="sxs-lookup"><span data-stu-id="53a33-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="53a33-105">See on kasulik, kui soovite saada ülevaadet oodatavatest kuludest, näiteks kulud seoses planeeritavate järgmise aasta ennetavate hooldustöödega.</span><span class="sxs-lookup"><span data-stu-id="53a33-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="53a33-106">Arvutused põhinevad olemasolevatel hooldusgraafiku ridadel, mille tüüp on "Hoolduskavad" ja "Hoolduskorrad" ja "Hooldusnõuded".</span><span class="sxs-lookup"><span data-stu-id="53a33-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="53a33-107">Klõpsake **Varahaldus** > **Päringud** > **Varad** > **Hooldusgraafiku kulu**.</span><span class="sxs-lookup"><span data-stu-id="53a33-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="53a33-108">Dialoogis **Hooldusgraafiku kulu** saate valida valiku **Finantsdimensioonikogum**, kui soovite näha kulusid finantsdimensioonidesse grupeerituna.</span><span class="sxs-lookup"><span data-stu-id="53a33-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="53a33-109">Finantsdimensioonikogumid seadistatakse jaotises **Pearaamat** > **Kontoplaan** > **Dimensioonid** > **Dinantsdimensioonikogumid**.</span><span class="sxs-lookup"><span data-stu-id="53a33-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="53a33-110">Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohaga seotud hooldusgraafiku ridu soovite.</span><span class="sxs-lookup"><span data-stu-id="53a33-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="53a33-111">Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha hooldusgraafiku read ning seetõttu võivad rea tunnid olla alumisel tasemel asuvate töö asukohtade summad.</span><span class="sxs-lookup"><span data-stu-id="53a33-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="53a33-112">Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki hooldusgraafiku ridu kõigi töö asukoha tasemete kohta, millega nad on seotud.</span><span class="sxs-lookup"><span data-stu-id="53a33-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="53a33-113">Kui soovite teha arvutusi konkreetsele varale, klõpsake kiirkaardil **Kaasatavad kirjed** nuppu **Filtreeri** ja valige asjakohased varad.</span><span class="sxs-lookup"><span data-stu-id="53a33-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="53a33-114">Vajadusel saate määrata kuluarvutusele ka **Oodatava alguse** kuupäeva või valida kulu arvutusele erineva **Oleku**</span><span class="sxs-lookup"><span data-stu-id="53a33-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="53a33-115">Kulu arvutuse alustamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="53a33-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="53a33-116">Klõpsake vahekaardi **Hooldusgraafiku kulu** > toimingupaani rühmas **Rühmitusalus...** asjakohastele nuppudele, et kuvada kuluarvutuse soovitud üksikasjade taset.</span><span class="sxs-lookup"><span data-stu-id="53a33-116">On the **Maintenance schedule cost** tab > in the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="53a33-117">Valitud toimingupaani grupi nupud on sinise värviga esile tõstetud.</span><span class="sxs-lookup"><span data-stu-id="53a33-117">The selected action pane group buttons are highlighted in blue color.</span></span> <span data-ttu-id="53a33-118">Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.</span><span class="sxs-lookup"><span data-stu-id="53a33-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="53a33-119">Klõpsake nuppu **Arvuta kulu**, kui soovite teha uue kuluarvutuse.</span><span class="sxs-lookup"><span data-stu-id="53a33-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>


![Joonis 1](media/17-preventive-maintenance.png)

