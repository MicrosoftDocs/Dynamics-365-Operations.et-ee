---
title: Põhivara seostamine rendiga
description: See teema selgitab, kuidas seostada olemasolev põhivara uue rendikirjega.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d627633e43c2e6f5cad90dfe4100ff95a71541f7
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442571"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="04fcb-103">Põhivara seostamine rendiga</span><span class="sxs-lookup"><span data-stu-id="04fcb-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04fcb-104">See teema selgitab, kuidas seostada olemasolev põhivara uue rendikirjega.</span><span class="sxs-lookup"><span data-stu-id="04fcb-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="04fcb-105">Kui seostate põhivara rendikirjega, on põhivara soetusmaksumuseks kasutamisõiguse esemeks oleva vara väärtus esialgsel tuvastamisel.</span><span class="sxs-lookup"><span data-stu-id="04fcb-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="04fcb-106">Enne põhivara rendiga seostamist peate looma põhivara jaoks suvandis Põhivarad kirje.</span><span class="sxs-lookup"><span data-stu-id="04fcb-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="04fcb-107">Seejärel peate looma lehel **Rendi kokkuvõte** rendikirje ja seostama vara selle rendiga.</span><span class="sxs-lookup"><span data-stu-id="04fcb-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="04fcb-108">Lisage rendikirje, järgides samme teemas [Rendikirjete lisamine või kopeerimine](add-lease.md).</span><span class="sxs-lookup"><span data-stu-id="04fcb-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="04fcb-109">Valige lehel **Rendikirje lisamine** väljale **Põhivara number** vara, mis ei ole veel soetatud.</span><span class="sxs-lookup"><span data-stu-id="04fcb-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="04fcb-110">Valige suvand **Raamatud** ja kinnitage maksegraafik.</span><span class="sxs-lookup"><span data-stu-id="04fcb-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="04fcb-111">Valige suvand **Esialgne tuvastamine**.</span><span class="sxs-lookup"><span data-stu-id="04fcb-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="04fcb-112">Valige suvand **Vara rentimise tööleht**.</span><span class="sxs-lookup"><span data-stu-id="04fcb-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="04fcb-113">Rendikirje algse tuvastamise töölehe kirje debiteerib põhivara summas, mis on tavaliselt debiteeritud kasutamisõiguse esemeks oleva vara kontoga.</span><span class="sxs-lookup"><span data-stu-id="04fcb-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="04fcb-114">Saate nüüd kuvada põhiraamatu tehingu tüübi ja raamatu.</span><span class="sxs-lookup"><span data-stu-id="04fcb-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="04fcb-115">Valige **Töölehe üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="04fcb-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="04fcb-116">Valige **Read**, et vaadata töölehe kirje üksikuid ridu.</span><span class="sxs-lookup"><span data-stu-id="04fcb-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="04fcb-117">Valige vara sisaldav töölehe rida ja valige seejärel vahekaart **Põhivarad**.</span><span class="sxs-lookup"><span data-stu-id="04fcb-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="04fcb-118">Vahekaart **Põhivarad** kuvab kande tüübi ja raamatu.</span><span class="sxs-lookup"><span data-stu-id="04fcb-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="04fcb-119">Vaikimisi on väli **Tehingu tüüp** määratud valikule **Omandamine** ja väli **Raamat** on määratud põhivara praegusele raamatule.</span><span class="sxs-lookup"><span data-stu-id="04fcb-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="04fcb-120">Pärast esialgse tuvastuse töölehe kirje sisestamist kuvatakse kanne põhivara soetamise kandena.</span><span class="sxs-lookup"><span data-stu-id="04fcb-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="04fcb-121">Kannete tabeli vaatamiseks avage jaotis **Põhivarad \> Põhivarad \> Põhivarad**, valige vastav vara ja valige seejärel **Hindamised**.</span><span class="sxs-lookup"><span data-stu-id="04fcb-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="04fcb-122">Peaksite nägema, et esialgse tuvastuse töölehe kirje sisestamine on loonud määratud põhivara jaoks soetamise kande.</span><span class="sxs-lookup"><span data-stu-id="04fcb-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="04fcb-123">Põhivara saab nüüd amortiseerida põhivarade standardse kulumi funktsiooni abil.</span><span class="sxs-lookup"><span data-stu-id="04fcb-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="04fcb-124">Lisateavet kulumiarvestuse kohta leiate jaotisest [Kulumimeetodid ja kulumiarvestusreeglid](../fixed-assets/depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="04fcb-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="04fcb-125">Kui seostate põhivara rendiga, on nupud **Vara kulum** ja **Rendi väärtuse langus** põhivara rentimises keelatud.</span><span class="sxs-lookup"><span data-stu-id="04fcb-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="04fcb-126">Vara kulumist ja rendi väärtuse languse tehinguid saate vaadata püsivaradest.</span><span class="sxs-lookup"><span data-stu-id="04fcb-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="04fcb-127">Nupp **Vara kanded**, mis avab päringu vormi, on samuti keelatud.</span><span class="sxs-lookup"><span data-stu-id="04fcb-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="04fcb-128">Saate avada päringu **Vara tehingud** ka põhivaradest.</span><span class="sxs-lookup"><span data-stu-id="04fcb-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  
