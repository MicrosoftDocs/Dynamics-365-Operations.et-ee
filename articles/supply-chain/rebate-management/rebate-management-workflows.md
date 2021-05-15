---
title: Tagasimaksehalduse tehingu töövood
description: See teema kirjeldab, kuidas seadistada Tagasimaksehalduse tehingu töövoogu, et tehinguid kinnitada ja aktiveerida.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 16f1c56ecd69f4dc7bfd80e74d3f35147cc173d6
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5919815"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="b5941-103">Tagasimaksehalduse tehingu töövood</span><span class="sxs-lookup"><span data-stu-id="b5941-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5941-104">Tagasimaksete kinnitamiseks kasutab Tagasimaksehaldus sama töövoo platvorme kui teised Finance and Operations rakendused.</span><span class="sxs-lookup"><span data-stu-id="b5941-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="b5941-105">Iga töövooga on seotud kaks tööprotsessi.</span><span class="sxs-lookup"><span data-stu-id="b5941-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="b5941-106">Üks töövoo element aktiveerib tehingu, nii et kasutaja või töövoo protsess saab kanded kinnitada.</span><span class="sxs-lookup"><span data-stu-id="b5941-106">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>
- <span data-ttu-id="b5941-107">Üks töövoo element kinnitab tehingu.</span><span class="sxs-lookup"><span data-stu-id="b5941-107">One element of the workflow approves the deal.</span></span>

<span data-ttu-id="b5941-108">Enne tagasimakse tehingu kasutamist peab see olema aktiivne moodulis **Tagasimaksehaldus**.</span><span class="sxs-lookup"><span data-stu-id="b5941-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="b5941-109">Tehingu aktiveerimiseks peate esmalt looma ja konfigureerima töövoo *Tagasimaksehalduse tehingu töövoog*.</span><span class="sxs-lookup"><span data-stu-id="b5941-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="b5941-110">Pärast töövoo aktiveerimist Tagasimakse halduse jaoks ei saa kasutajad tehinguid käsitsi kinnitada.</span><span class="sxs-lookup"><span data-stu-id="b5941-110">After a workflow is activated for Rebate management, users can't manually approve deals.</span></span> <span data-ttu-id="b5941-111">Töövoogu peab alati kasutama.</span><span class="sxs-lookup"><span data-stu-id="b5941-111">The workflow must be always used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="b5941-112">Tagasimaksehalduse tehingu töövoogude loomine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="b5941-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="b5941-113">Tagasimaksehalduse tehingu töövoogudega töötamiseks minge **Tagasimaksehaldus \> Seadistamine \> Tagasimaksehalduse töövood**.</span><span class="sxs-lookup"><span data-stu-id="b5941-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="b5941-114">Seal saate vajadusel töövooge vaadata, luua ja uuendada.</span><span class="sxs-lookup"><span data-stu-id="b5941-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="b5941-115">Korraga saab olla aktiivne ainult üks seda tüüpi töövoog.</span><span class="sxs-lookup"><span data-stu-id="b5941-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="b5941-116">Lisateavet töövoogude kohta, kuidas töötada lehega **Tagasimaksehalduse töövood** ja kuidas töövooge luua, vaadake [Töövoo süsteemi ülevaadet](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) ja selle seotud teemasid.</span><span class="sxs-lookup"><span data-stu-id="b5941-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="b5941-117">Kasutage töövoogu tehingu aktiveerimiseks.</span><span class="sxs-lookup"><span data-stu-id="b5941-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="b5941-118">Tehingu aktiveerimiseks töövoo kaudu avage tehing (nt lehel **Kõik tagasimaksehalduse tehingud**).</span><span class="sxs-lookup"><span data-stu-id="b5941-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="b5941-119">Seejärel valige toimingupaanil **Töövoog \> Edasta**.</span><span class="sxs-lookup"><span data-stu-id="b5941-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="b5941-120">Kui uus tehing on töövoo kaudu töödeldud ja kinnitatud, on see aktiivne ja kasutamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="b5941-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="b5941-121">Pärast tehingu aktiveerimist ei saa te selle seadistust muuta.</span><span class="sxs-lookup"><span data-stu-id="b5941-121">After a deal has been activated, you can't change its setup.</span></span> <span data-ttu-id="b5941-122">Kui peate aktiivset tehingut muutma, inaktiveerige see ja seejärel looge uus tehing.</span><span class="sxs-lookup"><span data-stu-id="b5941-122">If you must change an active deal, inactivate it, and then create a new deal.</span></span> <span data-ttu-id="b5941-123">Kui uus tehing sarnaneb vana tehinguga, saate selle luua vana tehingut kopeerides.</span><span class="sxs-lookup"><span data-stu-id="b5941-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>
