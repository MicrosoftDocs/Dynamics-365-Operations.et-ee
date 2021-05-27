---
title: Prognoosiridadelt ei saa laojõudluse prognoosi mõõdet eemaldada
description: Prognoosiridadelt ei saa laojõudluse prognoosi mõõdet eemaldada.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026442"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="a6132-103">Prognoosiridadelt ei saa laojõudluse prognoosi mõõdet eemaldada</span><span class="sxs-lookup"><span data-stu-id="a6132-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="a6132-104">KB number: 4614408</span><span class="sxs-lookup"><span data-stu-id="a6132-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="a6132-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="a6132-105">Symptoms</span></span>

<span data-ttu-id="a6132-106">See probleem ilmneb, kui **Varude** dimensioon ei ole määratud vahekaardi **Prognoosi dimensioonid** **Nõudluse prognoosimise parameetri** lehel.</span><span class="sxs-lookup"><span data-stu-id="a6132-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="a6132-107">Sellest hoolimata kuvatakse **Lao** veerg **Nõudluse prognoosi** lehel (**Koondplaneerimise \> Prognoosimine \> Käsitsi prognoosi üksus \> Nõudluse prognoosi read**).</span><span class="sxs-lookup"><span data-stu-id="a6132-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="a6132-108">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="a6132-108">Resolution</span></span>

<span data-ttu-id="a6132-109">Sätted **Prognoosi dimensioonid** vahekaardil **Nõudluse prognoosimise parameetri** lehel ei mõjuta **Nõudluse prognoosi** lehte.</span><span class="sxs-lookup"><span data-stu-id="a6132-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="a6132-110">Need kontrollivad alusprognoosi, mis luuakse ja näidatakse korrigeeritud nõudluse prognoosis.</span><span class="sxs-lookup"><span data-stu-id="a6132-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="a6132-111">Kuid need ei kontrolli siiski "reaal"-nõudluse prognoosi jaoks nõutavaid dimensioone.</span><span class="sxs-lookup"><span data-stu-id="a6132-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="a6132-112">Muutes kirjeid, mis on kuvatud **Korrigeeritud nõudluse prognoosi** lehel, saate need teisendada prognoosimudeli "reaal"-prognoosi kirjeteks.</span><span class="sxs-lookup"><span data-stu-id="a6132-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="a6132-113">Seejärel saab seda mudelit kasutada koondplaneerimisel.</span><span class="sxs-lookup"><span data-stu-id="a6132-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="a6132-114">**Nõudluse prognoosi** lehel, "reaalse" prognoosi dimensioonid, mis kuvatakse nõudluse prognoosiridadel, on varude dimensioonide osa.</span><span class="sxs-lookup"><span data-stu-id="a6132-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="a6132-115">(Selline käitumine sarnaneb müügitellimuse ridade käitumisega.) Kui teie süsteem ei ole seadistatud kasutama **Ladu** kohustusliku varude dimensioonina, saate lehte veeru peitmiseks kohandada.</span><span class="sxs-lookup"><span data-stu-id="a6132-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
