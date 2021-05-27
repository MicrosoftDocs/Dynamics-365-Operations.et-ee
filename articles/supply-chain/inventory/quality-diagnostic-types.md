---
title: Mittevastavuste diagnostika tüübid
description: See teema kirjeldab, kuidas kasutada ja luua diagnostika tüüpe, mida mittevastavuste puhul kasutada saab.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7a5c593f1d9e8f7a77f693f6e652e9355a985fb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022272"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="2f254-103">Mittevastavuste diagnostika tüübid</span><span class="sxs-lookup"><span data-stu-id="2f254-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f254-104">See teema kirjeldab, kuidas kasutada ja luua diagnostika tüüpe, mida mittevastavuste puhul kasutada saab.</span><span class="sxs-lookup"><span data-stu-id="2f254-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="2f254-105">Kasutage lehte **Diagnostika tüübid** diagnostikatoimingute klassifikatsiooni määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="2f254-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="2f254-106">Seejärel, kui loote mittevastavuse paranduse, valite diagnostika.</span><span class="sxs-lookup"><span data-stu-id="2f254-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="2f254-107">Parandus määratleb, mis tüüpi diagnostilist tegevust tuleks kinnitatud mittevastavuse korral kasutada ja kes peaks seda tegema.</span><span class="sxs-lookup"><span data-stu-id="2f254-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="2f254-108">Samuti määratleb see nõutava lõpetamise kuupäeva ja plaanitud lõpetamise kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="2f254-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="2f254-109">Diagnostikatüüpide näited</span><span class="sxs-lookup"><span data-stu-id="2f254-109">Examples of diagnostic types</span></span>

<span data-ttu-id="2f254-110">Te töötate tootmisettevõttes ja mitmel kaubal on kvaliteeditestid nurjunud.</span><span class="sxs-lookup"><span data-stu-id="2f254-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="2f254-111">Need kaubad teisaldatakse vahelattu ja märgitakse mittevastavateks toodeteks.</span><span class="sxs-lookup"><span data-stu-id="2f254-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="2f254-112">Luuakse mittevastavuse kirje Microsoft Dynamics 365 Supply Chain Management, et jälgida üksikasju probleemi lahendamise kaudu.</span><span class="sxs-lookup"><span data-stu-id="2f254-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="2f254-113">Sel juhul tekivad kvaliteediprobleemid, kuna esemeid pakkiva masina laagrid on kulunud ja kuumenevad üle.</span><span class="sxs-lookup"><span data-stu-id="2f254-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="2f254-114">Selle probleemi parandus on asendada masina osad.</span><span class="sxs-lookup"><span data-stu-id="2f254-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="2f254-115">Kui konfigureerite diagnostika tüüpe, saate luua mitmeid kirjeid, millest igaüks esindab erinevat tüüpi probleeme, mis masinal võivad olla.</span><span class="sxs-lookup"><span data-stu-id="2f254-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="2f254-116">Võite luua ka ühe üldise diagnostika tüübi, mis esindab masina parandamist.</span><span class="sxs-lookup"><span data-stu-id="2f254-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="2f254-117">Looge diagnostika tüüp</span><span class="sxs-lookup"><span data-stu-id="2f254-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="2f254-118">Avage **Laohaldus \> Seadistus \> Kvaliteedijuhtimine \> Diagnostika tüübid**.</span><span class="sxs-lookup"><span data-stu-id="2f254-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="2f254-119">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="2f254-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="2f254-120">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="2f254-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="2f254-121">**Diagnostika** – Sisestage meediumitüübi kordumatu ID või nimi.</span><span class="sxs-lookup"><span data-stu-id="2f254-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="2f254-122">**Kirjeldus** – Sisestage diagnostika tüübi detailne kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="2f254-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="2f254-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2f254-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f254-124">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2f254-124">Additional resources</span></span>

- [<span data-ttu-id="2f254-125">Kvaliteedijuhtimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="2f254-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="2f254-126">Kvaliteedi ja mittevastavuse haldamise lubamine</span><span class="sxs-lookup"><span data-stu-id="2f254-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="2f254-127">Mittevastavuste kinnitamise eest vastutavad töötajad</span><span class="sxs-lookup"><span data-stu-id="2f254-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="2f254-128">Mittevastavuste garantiitsoonid</span><span class="sxs-lookup"><span data-stu-id="2f254-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="2f254-129">Mittevastavuste probleemitüübid</span><span class="sxs-lookup"><span data-stu-id="2f254-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="2f254-130">Kvaliteeditasud mittevastavustele</span><span class="sxs-lookup"><span data-stu-id="2f254-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="2f254-131">MIttevastavuste toimingud</span><span class="sxs-lookup"><span data-stu-id="2f254-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="2f254-132">Laoprotsesside kvaliteedijuhtimine</span><span class="sxs-lookup"><span data-stu-id="2f254-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
