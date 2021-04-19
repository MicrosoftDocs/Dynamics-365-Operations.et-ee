---
title: Hooldusgraafiku kulu
description: Selles teemas selgitatakse hooldusgraafiku kulu varahalduses.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 405fd7fbbbb8862446d09b9ea33ef14348e691f9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813769"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="8eac5-103">Hooldusgraafiku kulu</span><span class="sxs-lookup"><span data-stu-id="8eac5-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8eac5-104">Varahalduses saate arvutada hooldusgraafiku ridade eelarve kulusid.</span><span class="sxs-lookup"><span data-stu-id="8eac5-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="8eac5-105">See on kasulik, kui soovite saada ülevaadet oodatavatest kuludest, näiteks kulud seoses planeeritavate järgmise aasta ennetavate hooldustöödega.</span><span class="sxs-lookup"><span data-stu-id="8eac5-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="8eac5-106">Arvutused põhinevad olemasolevatel hooldusgraafiku ridadel, mille tüüp on "Hoolduskavad" ja "Hoolduskorrad" ja "Hooldusnõuded".</span><span class="sxs-lookup"><span data-stu-id="8eac5-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="8eac5-107">Klõpsake **Varahaldus** > **Päringud** > **Varad** > **Hooldusgraafiku kulu**.</span><span class="sxs-lookup"><span data-stu-id="8eac5-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="8eac5-108">Dialoogis **Hooldusgraafiku kulu** saate valida valiku **Finantsdimensioonikogum**, kui soovite näha kulusid finantsdimensioonidesse grupeerituna.</span><span class="sxs-lookup"><span data-stu-id="8eac5-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="8eac5-109">Finantsdimensioonikogumid seadistatakse jaotises **Pearaamat** > **Kontoplaan** > **Dimensioonid** > **Dinantsdimensioonikogumid**.</span><span class="sxs-lookup"><span data-stu-id="8eac5-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="8eac5-110">Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohaga seotud hooldusgraafiku ridu soovite.</span><span class="sxs-lookup"><span data-stu-id="8eac5-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="8eac5-111">Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha hooldusgraafiku read ning seetõttu võivad rea tunnid olla alumisel tasemel asuvate töö asukohtade summad.</span><span class="sxs-lookup"><span data-stu-id="8eac5-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="8eac5-112">Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki hooldusgraafiku ridu kõigi töö asukoha tasemete kohta, millega nad on seotud.</span><span class="sxs-lookup"><span data-stu-id="8eac5-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="8eac5-113">Kui soovite teha arvutusi konkreetsele varale, klõpsake kiirkaardil **Kaasatavad kirjed** nuppu **Filtreeri** ja valige asjakohased varad.</span><span class="sxs-lookup"><span data-stu-id="8eac5-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="8eac5-114">Vajadusel saate määrata kuluarvutusele ka **Oodatava alguse** kuupäeva või valida kulu arvutusele erineva **Oleku**</span><span class="sxs-lookup"><span data-stu-id="8eac5-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="8eac5-115">Kulu arvutuse alustamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="8eac5-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="8eac5-116">Klõpsake vahekaardi **Hooldusgraafiku kulu** > toimingupaani rühmas **Grupeerimisalus** asjakohastele nuppudele, et kuvada kuluarvutuse soovitud üksikasjade taset.</span><span class="sxs-lookup"><span data-stu-id="8eac5-116">On the **Maintenance schedule cost** tab > in the **Group by...** Action Pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="8eac5-117">Valitud toimingupaani grupi nupud on esile tõstetud.</span><span class="sxs-lookup"><span data-stu-id="8eac5-117">The selected Action Pane group buttons are highlighted.</span></span> <span data-ttu-id="8eac5-118">Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.</span><span class="sxs-lookup"><span data-stu-id="8eac5-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="8eac5-119">Klõpsake nuppu **Arvuta kulu**, kui soovite teha uue kuluarvutuse.</span><span class="sxs-lookup"><span data-stu-id="8eac5-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="8eac5-120">Alltoodud illustratsioonil kuvatakse näidet hooldusgraafiku kulu arvutuse tulemustest.</span><span class="sxs-lookup"><span data-stu-id="8eac5-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![Joonis 1](media/17-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]