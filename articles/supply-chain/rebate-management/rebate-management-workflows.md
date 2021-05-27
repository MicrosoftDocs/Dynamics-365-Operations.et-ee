---
title: Tagasimaksehalduse tehingu töövood
description: See teema kirjeldab, kuidas seadistada Tagasimaksehalduse tehingu töövoogu, et tehinguid kinnitada ja aktiveerida.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020382"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="cd2ac-103">Tagasimaksehalduse tehingu töövood</span><span class="sxs-lookup"><span data-stu-id="cd2ac-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd2ac-104">Tagasimaksete kinnitamiseks kasutab Tagasimaksehaldus sama töövoo platvorme kui teised Finance and Operations rakendused.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="cd2ac-105">Iga töövooga on seotud kaks tööprotsessi.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="cd2ac-106">Üks töövoo element aktiveerib tehingu, nii et kasutaja või töövoo protsess saab kanded kinnitada.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-106">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>
- <span data-ttu-id="cd2ac-107">Üks töövoo element kinnitab tehingu.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-107">One element of the workflow approves the deal.</span></span>

<span data-ttu-id="cd2ac-108">Enne tagasimakse tehingu kasutamist peab see olema aktiivne moodulis **Tagasimaksehaldus**.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="cd2ac-109">Tehingu aktiveerimiseks peate esmalt looma ja konfigureerima töövoo *Tagasimaksehalduse tehingu töövoog*.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="cd2ac-110">Pärast töövoo aktiveerimist Tagasimakse halduse jaoks ei saa kasutajad tehinguid käsitsi kinnitada.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-110">After a workflow is activated for Rebate management, users can't manually approve deals.</span></span> <span data-ttu-id="cd2ac-111">Töövoogu peab alati kasutama.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-111">The workflow must be always used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="cd2ac-112">Tagasimaksehalduse tehingu töövoogude loomine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="cd2ac-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="cd2ac-113">Tagasimaksehalduse tehingu töövoogudega töötamiseks minge **Tagasimaksehaldus \> Seadistamine \> Tagasimaksehalduse töövood**.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="cd2ac-114">Seal saate vajadusel töövooge vaadata, luua ja uuendada.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="cd2ac-115">Korraga saab olla aktiivne ainult üks seda tüüpi töövoog.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="cd2ac-116">Lisateavet töövoogude kohta, kuidas töötada lehega **Tagasimaksehalduse töövood** ja kuidas töövooge luua, vaadake [Töövoo süsteemi ülevaadet](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) ja selle seotud teemasid.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="cd2ac-117">Kasutage töövoogu tehingu aktiveerimiseks.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="cd2ac-118">Tehingu aktiveerimiseks töövoo kaudu avage tehing (nt lehel **Kõik tagasimaksehalduse tehingud**).</span><span class="sxs-lookup"><span data-stu-id="cd2ac-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="cd2ac-119">Seejärel valige toimingupaanil **Töövoog \> Edasta**.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="cd2ac-120">Kui uus tehing on töövoo kaudu töödeldud ja kinnitatud, on see aktiivne ja kasutamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="cd2ac-121">Pärast tehingu aktiveerimist ei saa te selle seadistust muuta.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-121">After a deal has been activated, you can't change its setup.</span></span> <span data-ttu-id="cd2ac-122">Kui peate aktiivset tehingut muutma, inaktiveerige see ja seejärel looge uus tehing.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-122">If you must change an active deal, inactivate it, and then create a new deal.</span></span> <span data-ttu-id="cd2ac-123">Kui uus tehing sarnaneb vana tehinguga, saate selle luua vana tehingut kopeerides.</span><span class="sxs-lookup"><span data-stu-id="cd2ac-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>
