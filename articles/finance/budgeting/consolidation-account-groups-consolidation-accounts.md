---
title: Konsolideerimiskontode grupid ja täiendavad konsolideerimiskontod
description: See teema annab teavet konsolideerimiskontode gruppide ja täiendavate konsolideerimiskontode kohta ning selgitab nende kasutamist Microsoft Dynamics 365 Finance'is.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8db7a60656434aafd8114b08c2c0e9493140f27b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177382"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="880b0-103">Konsolideerimiskontode grupid ja täiendavad konsolideerimiskontod</span><span class="sxs-lookup"><span data-stu-id="880b0-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="880b0-104">See teema annab teavet konsolideerimiskontode gruppide ja täiendavate konsolideerimiskontode kohta ning selgitab nende kasutamist Microsoft Dynamics 365 Finance'is.</span><span class="sxs-lookup"><span data-stu-id="880b0-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 Finance.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="880b0-105">Konsolideerimiskontode grupid</span><span class="sxs-lookup"><span data-stu-id="880b0-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="880b0-106">Konsolideerimiskontode grupid võimaldavad luua gruppe kontodest, mida soovite kasutada andmete konsolideerimiseks.</span><span class="sxs-lookup"><span data-stu-id="880b0-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="880b0-107">Enamasti kujutab konsolideerimiskontode grupp riiklikul tasandil kontoplaani või vastendab kontod grupiga, mille on määratlenud ettevõtte peakontorid.</span><span class="sxs-lookup"><span data-stu-id="880b0-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="880b0-108">Konsolideerimiskontode grupid leiate mooduli **Konsolideerimised** alast **Häälestus**.</span><span class="sxs-lookup"><span data-stu-id="880b0-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="880b0-109">Uue kontogrupi lisamisel sisestage selle jaoks kordumatu identifikaator ja nimi.</span><span class="sxs-lookup"><span data-stu-id="880b0-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="880b0-110">Täiendavad konsolideerimiskontod</span><span class="sxs-lookup"><span data-stu-id="880b0-110">Additional consolidation accounts</span></span>
<span data-ttu-id="880b0-111">Täiendavad konsolideerimiskontod võimaldavad määrata konto olemasolevast kontoplaanist konsolideerimiskontode gruppi.</span><span class="sxs-lookup"><span data-stu-id="880b0-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="880b0-112">Seejärel saate määrata konsolideerimiskonto väärtuse ja nime.</span><span class="sxs-lookup"><span data-stu-id="880b0-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="880b0-113">Täiendavad konsolideerimiskontod leiate mooduli **Konsolideerimised** alast **Häälestus**.</span><span class="sxs-lookup"><span data-stu-id="880b0-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="880b0-114">Uue konsolideerimiskonto loomisel peate määrama järgmise teabe.</span><span class="sxs-lookup"><span data-stu-id="880b0-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="880b0-115">**Põhikonto** – see väli on otsinguväli, millel kuvatakse kõik lehel valitud kontoplaanil põhinevad põhikontod.</span><span class="sxs-lookup"><span data-stu-id="880b0-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="880b0-116">Konto valimisel sisestatakse selle nimi automaatselt väljale **Põhikonto nimi**.</span><span class="sxs-lookup"><span data-stu-id="880b0-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="880b0-117">**Konsolideerimiskontode grupp** – selle väljaga saate valida grupi, millesse konto määrata.</span><span class="sxs-lookup"><span data-stu-id="880b0-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="880b0-118">Kahel erineval viisil konsolideerimisel peate lisama sama konto kõigisse nelja konsolideerimiskontode gruppi.</span><span class="sxs-lookup"><span data-stu-id="880b0-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="880b0-119">**Konsolideerimiskonto** – sisestage konsolideerimiskonto väärtus.</span><span class="sxs-lookup"><span data-stu-id="880b0-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="880b0-120">See väärtus ei pea olema konto kontoplaanilt.</span><span class="sxs-lookup"><span data-stu-id="880b0-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="880b0-121">See võib olla mis tahes teie nõutud väärtus.</span><span class="sxs-lookup"><span data-stu-id="880b0-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="880b0-122">**Konsolideerimiskonto nimi** – sisestage konto nimi kujul, nagu soovite seda kuvada päringutes ja aruannetes.</span><span class="sxs-lookup"><span data-stu-id="880b0-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="880b0-123">**SAT tase** – seda välja kasutatakse Mehhiko maksuasutustele kontoväljavõtete esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="880b0-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="880b0-124">Kui olete konsolideerimiskontode gruppide ja täiendavate konsolideerimiskontode loomise lõpule viinud, saate valida grupi jaotises Võrgus konsolideerimise protsess.</span><span class="sxs-lookup"><span data-stu-id="880b0-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="880b0-125">Lisateabe saamiseks vt [Konsolideerimisgruppide ja täiendavate konsolideerimiskontode loomine](../general-ledger/tasks/create-consolidation-groups.md)</span><span class="sxs-lookup"><span data-stu-id="880b0-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 


