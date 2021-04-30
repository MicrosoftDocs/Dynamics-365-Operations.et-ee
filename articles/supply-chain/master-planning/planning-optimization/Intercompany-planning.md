---
title: Kontsernisisene planeerimine
description: Selles teemas kirjeldatakse kontsernisiseseid planeerimisi ja selgitatakse, kuidas konfigureerida kontsernisiseseid planeerimisi planeerimise optimeerimisega rakenduses Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e6fff06cb6194f17444025f7ea1f9dbb46e4f3ea
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907639"
---
# <a name="intercompany-planning"></a><span data-ttu-id="a690c-103">Kontsernisisene planeerimine</span><span class="sxs-lookup"><span data-stu-id="a690c-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a690c-104">Mõnede organisatsioonide puhul sõltuvad logistikatoimingud organisatsiooni muudest juriidilistest isikutest (ettevõtetest).</span><span class="sxs-lookup"><span data-stu-id="a690c-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="a690c-105">Neid toiminguid käsitletakse kontsernisiseste müügitehingute ja ostude abil, kuna igal juriidilisel isikul on eraldi kontoplaan.</span><span class="sxs-lookup"><span data-stu-id="a690c-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="a690c-106">Selles teemas kirjeldatakse kontsernisiseseid planeerimisi ja selgitatakse, kuidas konfigureerida kontsernisiseseid planeerimisi planeerimise optimeerimisega rakenduses Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a690c-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="a690c-107">Selles teemas kasutatakse järgmisi olulisi kontsernisiseseid termineid.</span><span class="sxs-lookup"><span data-stu-id="a690c-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="a690c-108">**Ülesvoolu** – suhteline viide firmas või tarneahelas.</span><span class="sxs-lookup"><span data-stu-id="a690c-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="a690c-109">See näitab liikumist toormaterjali tarnija suunas.</span><span class="sxs-lookup"><span data-stu-id="a690c-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="a690c-110">**Allavoolu** – suhteline viide firmas või tarneahelas.</span><span class="sxs-lookup"><span data-stu-id="a690c-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="a690c-111">See näitab liikumist kliendi suunas.</span><span class="sxs-lookup"><span data-stu-id="a690c-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="a690c-112">**Plaanitud kontsernisisene nõudlus** – plaanitud nõudlus toote järele ettevõttes, põhinedes plaanitud nõudlusel, mis on allavoolu ettevõttel toote järele.</span><span class="sxs-lookup"><span data-stu-id="a690c-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="a690c-113">Koondplaneerimise puhul võib ühe ettevõtte plaan sisaldada plaanitud kontsernisisest nõudlust, mis on seotud plaanitud tellimustega teises ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="a690c-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="a690c-114">See võimalus on kasulik, kuna see võimaldab ettevõtete plaanitud tellimuste täieliku nähtavuse.</span><span class="sxs-lookup"><span data-stu-id="a690c-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="a690c-115">See tagab ka, et kõik nõutavad plaanitud tarnetellimused on loodud, kuid eeldamata plaanitud tellimuste kinnitamist kontsernisisese nõudluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="a690c-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="a690c-116">Kui alustate koondplaneerimist põhiplaanist, mis sisaldab plaanitud allavoolu nõudlust, lisatakse plaanile nõudlusena seotud kontsernisiseste hankijate plaanitud ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="a690c-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="a690c-117">Nõutav häälestus</span><span class="sxs-lookup"><span data-stu-id="a690c-117">Required setup</span></span>

<span data-ttu-id="a690c-118">Kontsernisisese planeerimise kasutamiseks peate oma süsteemi ette valmistama järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="a690c-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="a690c-119">Asjaomased tooted tuleb vabastada kõikides asjaomastes ettevõtetes.</span><span class="sxs-lookup"><span data-stu-id="a690c-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="a690c-120">Lisateavet vt [Kontsernisisese kaubanduse konfigureerimine ja kasutamine rakenduses Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) saidil Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="a690c-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="a690c-121">Allavoolu nõudlus peab olema kaetud ostudega hankijalt, kellel on kontsernisisesed seosed ülesvoolu ettevõttega ja asjakohased vaikimisi varude dimensioonid (sait ja ladu) kliendi kohta.</span><span class="sxs-lookup"><span data-stu-id="a690c-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="a690c-122">Lisateavet vt [Kontsernisisese kaubanduse konfigureerimine ja kasutamine rakenduses Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) saidil Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="a690c-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="a690c-123">Ülesvoolu ettevõtte koondplaan peab sisaldama plaanitud allavooluetapi nõudlust ning allavoolu plaanides tuleb määrata vastav ettevõte ja koondplaan.</span><span class="sxs-lookup"><span data-stu-id="a690c-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="a690c-124">Kaasa plaanitud järgmise etapi nõudlus</span><span class="sxs-lookup"><span data-stu-id="a690c-124">Include planned downstream demand</span></span>

<span data-ttu-id="a690c-125">Järgige neid juhiseid, et konfigureerida oma koondplaan nii, et see hõlmaks plaanitud allavoolu nõudlust.</span><span class="sxs-lookup"><span data-stu-id="a690c-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="a690c-126">Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**.</span><span class="sxs-lookup"><span data-stu-id="a690c-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="a690c-127">Valige või looge koondplaan.</span><span class="sxs-lookup"><span data-stu-id="a690c-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="a690c-128">Määrake kiirkaardil **Kontsernisisene plaanimine** järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="a690c-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="a690c-129">**Lisa plaanitud allavooluetapi nõudlus** – määrake selle suvandi väärtuseks *Jah*, et võimaldada koondplaneerimise kontsernisisest plaanimist.</span><span class="sxs-lookup"><span data-stu-id="a690c-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="a690c-130">**Allavooluetapi plaanid** – kui määrate suvandi **Lisa plaanitud allavooluetapi nõudlus** väärtuseks *Jah*, kasutage teiste ettevõtete soovitud koondplaanide lisamiseks tööriistariba ja ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="a690c-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="a690c-131">Ettevõtete sidumine mitmetasandilise sidumise abil</span><span class="sxs-lookup"><span data-stu-id="a690c-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="a690c-132">Mitmetasandilise sidumise puhul saate kuvada seotuse kõigis ettevõtetes, et näha algset nõudluse allikat, mida tarne hõlmab.</span><span class="sxs-lookup"><span data-stu-id="a690c-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="a690c-133">Mitmetasandilise sidumise teabe vaatamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a690c-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="a690c-134">Avage **Koondplaneerimine \> Koondplaneerimine \> Plaanitud tellimused**.</span><span class="sxs-lookup"><span data-stu-id="a690c-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="a690c-135">Valige või avage plaanitud tellimus.</span><span class="sxs-lookup"><span data-stu-id="a690c-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="a690c-136">Seejärel valige toimingupaanil vahekaardi **Vaade** grupis **Nõuded** suvand **Mitmetasandiline sidumine**.</span><span class="sxs-lookup"><span data-stu-id="a690c-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="a690c-137">Kontsernisisene näide, mis hõlmab kaht ettevõtet</span><span class="sxs-lookup"><span data-stu-id="a690c-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="a690c-138">Selles näites luuakse plaanitud tootmistellimus ettevõttes USMF, et katta müügitellimus ettevõttes DEMF.</span><span class="sxs-lookup"><span data-stu-id="a690c-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="a690c-139">USMF-is on otsene nõudlus plaanitud kontsernisisene nõudlus.</span><span class="sxs-lookup"><span data-stu-id="a690c-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="a690c-140">Selle nõudluse kuvamiseks USMF-is käivitub koondplaneerimine esmalt DEMF-is ja seejärel USMF-is.</span><span class="sxs-lookup"><span data-stu-id="a690c-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="a690c-141">Järgmine illustratsioon näitab, kuidas see näide võidakse kuvada plaanitud tootmistellimuse lehel **Mitmetasandiline sidumine**.</span><span class="sxs-lookup"><span data-stu-id="a690c-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Kontsernisisene näide, mis hõlmab kaht ettevõtet](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="a690c-143">Kontsernisisene näide, mis hõlmab kolme ettevõtet</span><span class="sxs-lookup"><span data-stu-id="a690c-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="a690c-144">Selles näites luuakse plaanitud ostutellimus ettevõttes USMF, et katta müügitellimus ettevõttes FRRT.</span><span class="sxs-lookup"><span data-stu-id="a690c-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="a690c-145">Ettevõttes DEMF ja USMF on otsene nõudlus plaanitud kontsernisisene nõudlus.</span><span class="sxs-lookup"><span data-stu-id="a690c-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="a690c-146">Selle nõudluse kuvamiseks USMF-is käivitub koondplaneerimine esmalt FRRT-is, seejärel DEMF-is ja lõpuks USMF-is.</span><span class="sxs-lookup"><span data-stu-id="a690c-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="a690c-147">Järgmine illustratsioon näitab, kuidas see näide võidakse kuvada plaanitud tootmistellimuse lehel **Mitmetasandiline sidumine**.</span><span class="sxs-lookup"><span data-stu-id="a690c-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Kontsernisisene näide, mis hõlmab kolme ettevõtet](media/IntercompanyPlanning2.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]