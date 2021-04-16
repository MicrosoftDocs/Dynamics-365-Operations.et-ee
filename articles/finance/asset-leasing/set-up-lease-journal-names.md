---
title: Renditöölehe nimede seadistamine
description: Selles teemas selgitatakse renditöölehe nimede määratlemist. Renditöölehe nimed määravad töölehed, millele vara rentimise kanded sisestatakse.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e45475530ae56ec51bbfb5642d351822c9abfd7b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822995"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="b0c8b-104">Renditöölehe nimede seadistamine</span><span class="sxs-lookup"><span data-stu-id="b0c8b-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0c8b-105">Renditöölehe nimed määravad töölehed, millele vara rentimise kanded sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="b0c8b-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="b0c8b-106">Ainult need töölehe nimed, mis on määratud töölehe tüübile **Vara rentimine** kuvatakse väljadel **Esialgne tuvastamine** ja **Kuu töölehe nimi** lehel **Vara rentimise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="b0c8b-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="b0c8b-107">Ainult töölehe tüüpi **hankija arve kirjendamine** saab määrata väljale **Arve töölehe nimi**.</span><span class="sxs-lookup"><span data-stu-id="b0c8b-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="b0c8b-108">Renditöölehe nimede konfigureerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b0c8b-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="b0c8b-109">Avage **Vara rentimine \> Seadistus \> Vara rentimise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="b0c8b-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="b0c8b-110">Valige tööleht vahekaardi **Üldine** väljal **Esialgse tuvastamise töölehe nimi**.</span><span class="sxs-lookup"><span data-stu-id="b0c8b-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="b0c8b-111">Kõik esialgse tuvastamise töölehe kirjed sisestatakse sellele töölehe nimele.</span><span class="sxs-lookup"><span data-stu-id="b0c8b-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="b0c8b-112">Valige tööleht väljal **Arve töölehe nimi**.</span><span class="sxs-lookup"><span data-stu-id="b0c8b-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="b0c8b-113">Kui rendiraamatu suvand **Maksa hankijale** on määratud olekusse **Jah**, siis sisestatakse rendi ja kulude maksete arved sellele töölehe nimele.</span><span class="sxs-lookup"><span data-stu-id="b0c8b-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="b0c8b-114">Valige tööleht väljal **Renditöölehe nimi**.</span><span class="sxs-lookup"><span data-stu-id="b0c8b-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="b0c8b-115">Kõik kulumi-, intressi- ja lühiajalise ümberklassifitseerimise kanded sisestatakse sellele töölehe nimele.</span><span class="sxs-lookup"><span data-stu-id="b0c8b-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="b0c8b-116">Kui rendiraamatu suvand **Maksa hankijale** on määratud olekusse **Ei**, siis sisestatakse rendimaksete ja kulude maksete kirjed samuti sellele töölehe nimele.</span><span class="sxs-lookup"><span data-stu-id="b0c8b-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]