---
title: Plaanitud ostutellimus luuakse ostu olemasolul negatiivsete päevade jooksul
description: Kui laovarude kood on miinimum/maksimum, loob Planning Optimization plaanitud ostutellimuse, kui ost on negatiivsete päevade jooksul olemas.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026445"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="18820-103">Plaanitud ostutellimus luuakse ostu olemasolul negatiivsete päevade jooksul</span><span class="sxs-lookup"><span data-stu-id="18820-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="18820-104">KB number: 4614298</span><span class="sxs-lookup"><span data-stu-id="18820-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="18820-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="18820-105">Symptoms</span></span>

<span data-ttu-id="18820-106">Kui laovarude kood on *miinimum/maksimum*, loob Planning Optimization plaanitud ostutellimuse, kui ost on negatiivsete päevade jooksul olemas.</span><span class="sxs-lookup"><span data-stu-id="18820-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="18820-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="18820-107">Resolution</span></span>

<span data-ttu-id="18820-108">Planning Optimization ei toeta negatiivseid päevi.</span><span class="sxs-lookup"><span data-stu-id="18820-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="18820-109">Kuid see tagab alati, et plaanitud tellimusi ei planeerita täitmisaja jooksul praeguse kuupäevaga võrreldes.</span><span class="sxs-lookup"><span data-stu-id="18820-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="18820-110">Näiteks ostu täitmisaeg on 10 päeva ning ostutellimus peaks saabuma kaheksa päeva jooksul tänasest.</span><span class="sxs-lookup"><span data-stu-id="18820-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="18820-111">Sel juhul kasutatakse ostutellimust pakkumisena nõudlusele, mis on viis päeva alates tänasest.</span><span class="sxs-lookup"><span data-stu-id="18820-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="18820-112">Seetõttu on soovitatav täitmisajad korrigeerida nii, et see hõlmaks kõiki (või peaaegu kõiki) oma stsenaariume.</span><span class="sxs-lookup"><span data-stu-id="18820-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
