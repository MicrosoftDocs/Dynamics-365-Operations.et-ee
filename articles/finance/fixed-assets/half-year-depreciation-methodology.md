---
title: Poolaasta kulumiarvestuse konventsiooni metoodika
description: Selles teemas kirjeldatakse meetodit, mida põhivarad kasutavad kulumi arvestamiseks, kasutades poolaasta reeglit, mis arvutab kuue kuu kulumi vara esimesel ja viimasel kasutusaastal.
author: moaamer
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: d0e33128c37e970ebf5af87bd601ae30aef96952
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818579"
---
# <a name="half-year-depreciation-convention-methodology"></a><span data-ttu-id="cd2bc-103">Poolaasta kulumiarvestuse konventsiooni metoodika</span><span class="sxs-lookup"><span data-stu-id="cd2bc-103">Half-year depreciation convention methodology</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="cd2bc-104">Selles teemas kirjeldatakse meetodit, mida kasutatakse põhivarade korral kulumi arvestamiseks poolaasta konventsiooni kasutades.</span><span class="sxs-lookup"><span data-stu-id="cd2bc-104">This topic describes the method that is used in fixed assets to calculate depreciation using the half-year convention.</span></span> <span data-ttu-id="cd2bc-105">Poolaasta konventsioon arvestab kuue kuu kulumi vara esimese ja viimase kasutusaasta jooksul.</span><span class="sxs-lookup"><span data-stu-id="cd2bc-105">The half-year convention calculates six months of depreciation during an asset’s first and last year of service.</span></span> <span data-ttu-id="cd2bc-106">Lisateavet kulumiarvestuse konventsioonide kohta leiate jaotisest [Kulumimeetodid ja kulumiarvestusreeglid](Fixed-asset-depreciation-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="cd2bc-106">For more information about depreciation conventions, see [Depreciation methods and conventions](Fixed-asset-depreciation-conventions.md).</span></span> 

<span data-ttu-id="cd2bc-107">Kui kasutate kuue kuu kulumiarvestuse konventsiooni, kasutab süsteem soetusaastat või aastat, mil vara võeti kasutusse, seejärel arvestab viie aasta kulumi alates sellest aastast ja lisab seejärel kuus kuud.</span><span class="sxs-lookup"><span data-stu-id="cd2bc-107">When you use the six-month depreciation convention, the system uses the acquisition year or the year that the asset was placed in service, then calculates five years of depreciation from that year, and then adds six months.</span></span> <span data-ttu-id="cd2bc-108">Selle protsessi näitlikustamiseks kasutage vara, mis soetati hinnaga 50 000 ja võeti kasutusele 2020. aasta aprillis.</span><span class="sxs-lookup"><span data-stu-id="cd2bc-108">To illustrate this process, consider an asset that was acquired for the price of 50,000, and placed in service in April 2020.</span></span> <span data-ttu-id="cd2bc-109">Samuti eeldage, et varal on viieaastane tööiga.</span><span class="sxs-lookup"><span data-stu-id="cd2bc-109">Also assume that the asset has a five-year service life.</span></span>

<span data-ttu-id="cd2bc-110">Esimene kasutusaasta lõppes 2020. aasta detsembris, mis tähendab, et vara viieaastane tööiga lõppeb 2024. aasta detsembris.</span><span class="sxs-lookup"><span data-stu-id="cd2bc-110">The first year of service will conclude in December 2020, which means the end of the asset’s five-year service life will be December 2024.</span></span> <span data-ttu-id="cd2bc-111">Poolaasta kulumiarvestuse konventsioon lisab vara tööeale kuus kuud, mis tähendab, et selle tööiga lõpeb juunis 2025.</span><span class="sxs-lookup"><span data-stu-id="cd2bc-111">The half-year depreciation convention will add six months to the asset’s life, which means its service life will end in June 2025.</span></span> 

> <span data-ttu-id="cd2bc-112">Aastane kulum: 50 000:5 = 10 000; igakuine kulum: 10000:12 = 833,33</span><span class="sxs-lookup"><span data-stu-id="cd2bc-112">Yearly depreciation 50,000/5 = 10,000 monthly depreciation 10,000/12 = 833.33</span></span> <br>
> <span data-ttu-id="cd2bc-113">Esimese aasta kulum: 10 000:2 = 5 000; ja järgnev igakuine kulum: 5000:9 = 555,56</span><span class="sxs-lookup"><span data-stu-id="cd2bc-113">First year depreciation 10,000/2 = 5,000  and the subsequent monthly depreciation 5,000/9 = 555.56</span></span>

   <span data-ttu-id="cd2bc-114">[![Poolaasta kulumiarvestuse konventsiooni kulumiarvestuse ajakava](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span><span class="sxs-lookup"><span data-stu-id="cd2bc-114">[![Depreciation schedule for half-year depreciation convention](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span></span>

<span data-ttu-id="cd2bc-115">Pikendatud kulumiperioodid, mis on lisatud pooleaastase konventsiooniga, võimaldavad kulumi täpsemat jaotamist.</span><span class="sxs-lookup"><span data-stu-id="cd2bc-115">The extended depreciation periods that are added by the half-year convention provide more accurate allocation of depreciation.</span></span> <span data-ttu-id="cd2bc-116">Kuuekuuline konventsioon kajastab kulumiarvestuse kulusid võrdsemalt, mis on kasulik kasumiaruande koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="cd2bc-116">The six-month convention represents depreciation expenses more equally, which is useful for reporting on the profit and loss statement.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]