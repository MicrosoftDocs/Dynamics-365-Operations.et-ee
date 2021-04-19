---
title: Partii atribuudid
description: Selles teemas antakse teavet partii atribuutide kohta. Partii atribuudid on toormaterjalide ja varude partiid moodustavate valmistoodete omadused. See teema selgitab ka partiiatribuutide määramist ja seda, kuidas neilt partiide reserveerimisel otsida saab.
author: ShylaThompson
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 064b3dc7f0209b5c81580d4eb80384df74155aee
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811842"
---
# <a name="batch-attributes"></a><span data-ttu-id="a2674-105">Partii atribuudid</span><span class="sxs-lookup"><span data-stu-id="a2674-105">Batch attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2674-106">Selles teemas antakse teavet partii atribuutide kohta.</span><span class="sxs-lookup"><span data-stu-id="a2674-106">This topic provides information about batch attributes.</span></span> <span data-ttu-id="a2674-107">Partii atribuudid on toormaterjalide ja varude partiid moodustavate valmistoodete omadused.</span><span class="sxs-lookup"><span data-stu-id="a2674-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="a2674-108">See teema selgitab ka partiiatribuutide määramist ja seda, kuidas neilt partiide reserveerimisel otsida saab.</span><span class="sxs-lookup"><span data-stu-id="a2674-108">The topic also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="a2674-109">Partii atribuudid on toormaterjalide ja varude partiid moodustavate valmistoodete omadused.</span><span class="sxs-lookup"><span data-stu-id="a2674-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="a2674-110">Partii atribuudid võivad erineda olenevalt teguritest, nagu keskkonnatingimused, partii tootmiseks kasutatavate toormaterjalide kvaliteet või valmistoote tulemus.</span><span class="sxs-lookup"><span data-stu-id="a2674-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="a2674-111">Kasutatavate partii atribuutide arv ja tüübid võivad valdkonniti olulisel määral erineda.</span><span class="sxs-lookup"><span data-stu-id="a2674-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="a2674-112">Siin on toodud kaks näidet partii atribuutide kasutamisest.</span><span class="sxs-lookup"><span data-stu-id="a2674-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="a2674-113">Juustutööstuses võivad piimal, mis on üks juustu tootmiseks kasutatavaid toormaterjale, olla atribuudid, nagu rasvasisaldus ja massiprotsent.</span><span class="sxs-lookup"><span data-stu-id="a2674-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="a2674-114">Piimast toodetud juustul võivad olla teised atribuudid, näiteks niiskus ja vanus.</span><span class="sxs-lookup"><span data-stu-id="a2674-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="a2674-115">Terasetööstuses võivad toodetud raual olla atribuudid, nagu magneesiumi-, hõbeda- ja tsingisisalduse protsendid.</span><span class="sxs-lookup"><span data-stu-id="a2674-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="a2674-116">Atribuutide arvu ja tüüpide paremini haldamiseks saate kasutada partii atribuudigruppe.</span><span class="sxs-lookup"><span data-stu-id="a2674-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="a2674-117">Nii ei pea te iga atribuuti eraldi lisama.</span><span class="sxs-lookup"><span data-stu-id="a2674-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="a2674-118">Partii atribuutide määramine</span><span class="sxs-lookup"><span data-stu-id="a2674-118">Assign batch attributes</span></span>
<span data-ttu-id="a2674-119">Saate määrata partii atribuudid varude partiides hoitavatele üksikutele toodetele või kindlate klientidega seostatud toodetele.</span><span class="sxs-lookup"><span data-stu-id="a2674-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="a2674-120">Enne partii atribuudi määramist peate määrama selle toote tasemel.</span><span class="sxs-lookup"><span data-stu-id="a2674-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="a2674-121">Tootel peab olema jälgimisdimensioonigrupis määratud partiidimensiooni väärtuseks **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="a2674-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="a2674-122">Partii atribuudi määramiseks üksikule tootele kasutage tootekohast lehte.</span><span class="sxs-lookup"><span data-stu-id="a2674-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="a2674-123">Kui atribuut on kliendi jaoks loodud toote kohane, kasutage kliendikohast lehte.</span><span class="sxs-lookup"><span data-stu-id="a2674-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="a2674-124">Tootele atribuudi lisamisel saate määratleda ka muud parameetrid.</span><span class="sxs-lookup"><span data-stu-id="a2674-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="a2674-125">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="a2674-125">Here are some examples:</span></span>

-   <span data-ttu-id="a2674-126">Atribuudi tüübiga **Täisarv** või **Murd** miinimum- ja maksimumvahemikud.</span><span class="sxs-lookup"><span data-stu-id="a2674-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="a2674-127">Atribuudi, mille tüüp on **Täisarv** või **Murd**, hälbetegevused.</span><span class="sxs-lookup"><span data-stu-id="a2674-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="a2674-128">Kui atribuudi väärtus jääb väljapoole miinimum- ja maksimumvahemikku, saab tegevus olla kas hoiatus- või tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="a2674-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="a2674-129">Atribuudi sihtväärtus.</span><span class="sxs-lookup"><span data-stu-id="a2674-129">The target value for the attribute.</span></span> <span data-ttu-id="a2674-130">See väärtus on atribuudi optimaalne väärtus ja see rakendub kõigile atribuuditüüpidele.</span><span class="sxs-lookup"><span data-stu-id="a2674-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="a2674-131">Pääsete juurde mooduli Tooteteabe haldus lehel **Väljastatud tooted** valitud toodete lehtedele.</span><span class="sxs-lookup"><span data-stu-id="a2674-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="a2674-132">Pärast tootele partii atribuutide määramist saate lehel **Varude partii atribuudid** lisada atribuutidele kindlad väärtused.</span><span class="sxs-lookup"><span data-stu-id="a2674-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="a2674-133">Partiide reserveerimine</span><span class="sxs-lookup"><span data-stu-id="a2674-133">Reserve batches</span></span>
<span data-ttu-id="a2674-134">Saate otsida partii atribuute, kui reserveerite partiisid müügitellimuse jaoks, et täita kliendi tellimust, või kui komplekteerite ja reserveerite partiisid tootmistellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="a2674-134">You can search on batch attributes when you do batch reservations for a sales order to fulfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="a2674-135">Otsing aitab leida varude partii, mis sisaldab teie soovitud partiiatribuutidega toodet.</span><span class="sxs-lookup"><span data-stu-id="a2674-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="a2674-136">Kui olete partii(de) asukoha(d) tuvastanud, saate reserveerida toote lähtevarude kandereale.</span><span class="sxs-lookup"><span data-stu-id="a2674-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]