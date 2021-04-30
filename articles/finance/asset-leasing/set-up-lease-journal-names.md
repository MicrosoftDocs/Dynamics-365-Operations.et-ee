---
title: Renditöölehe nimede seadistamine
description: Selles teemas selgitatakse renditöölehe nimede määratlemist. Renditöölehe nimed määravad töölehed, millele vara rentimise kanded sisestatakse.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c139df124b249ec9dc5d16096e6f45f22d435456
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880882"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="354d3-104">Renditöölehe nimede seadistamine</span><span class="sxs-lookup"><span data-stu-id="354d3-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="354d3-105">Renditöölehe nimed määravad töölehed, millele vara rentimise kanded sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="354d3-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="354d3-106">Ainult need töölehe nimed, mis on määratud töölehe tüübile **Vara rentimine** kuvatakse väljadel **Esialgne tuvastamine** ja **Kuu töölehe nimi** lehel **Vara rentimise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="354d3-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="354d3-107">Ainult töölehe tüüpi **hankija arve kirjendamine** saab määrata väljale **Arve töölehe nimi**.</span><span class="sxs-lookup"><span data-stu-id="354d3-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="354d3-108">Renditöölehe nimede konfigureerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="354d3-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="354d3-109">Avage **Vara rentimine \> Seadistus \> Vara rentimise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="354d3-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="354d3-110">Valige tööleht vahekaardi **Üldine** väljal **Esialgse tuvastamise töölehe nimi**.</span><span class="sxs-lookup"><span data-stu-id="354d3-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="354d3-111">Kõik esialgse tuvastamise töölehe kirjed sisestatakse sellele töölehe nimele.</span><span class="sxs-lookup"><span data-stu-id="354d3-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="354d3-112">Valige tööleht väljal **Arve töölehe nimi**.</span><span class="sxs-lookup"><span data-stu-id="354d3-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="354d3-113">Kui rendiraamatu suvand **Maksa hankijale** on määratud olekusse **Jah**, siis sisestatakse rendi ja kulude maksete arved sellele töölehe nimele.</span><span class="sxs-lookup"><span data-stu-id="354d3-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="354d3-114">Valige tööleht väljal **Renditöölehe nimi**.</span><span class="sxs-lookup"><span data-stu-id="354d3-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="354d3-115">Kõik kulumi-, intressi- ja lühiajalise ümberklassifitseerimise kanded sisestatakse sellele töölehe nimele.</span><span class="sxs-lookup"><span data-stu-id="354d3-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="354d3-116">Kui rendiraamatu suvand **Maksa hankijale** on määratud olekusse **Ei**, siis sisestatakse rendimaksete ja kulude maksete kirjed samuti sellele töölehe nimele.</span><span class="sxs-lookup"><span data-stu-id="354d3-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
