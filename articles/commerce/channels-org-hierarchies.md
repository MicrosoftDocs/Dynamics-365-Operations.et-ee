---
title: Organisatsiooni hierarhiate seadistamine
description: Selle teema all kirjeldatakse organisatsiooni hierarhiate seadistust rakenduses Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 29d4b686cbb66715196fca06e4642fbb8a337ace
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411635"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="29abb-103">Organisatsiooni hierarhiate seadistamine</span><span class="sxs-lookup"><span data-stu-id="29abb-103">Set up organization hierarchies</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="29abb-104">Selle teema all kirjeldatakse organisatsiooni hierarhiate seadistust rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="29abb-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="29abb-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="29abb-105">Overview</span></span>

<span data-ttu-id="29abb-106">Enne kanalite loomist peate veenduma, et teie organisatsiooni hierarhiad on seadistatud.</span><span class="sxs-lookup"><span data-stu-id="29abb-106">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="29abb-107">Saate kasutada organisatsiooni hierarhiaid oma äri vaatamiseks ja selle aruandluse tegemiseks erinevatest aspektidest.</span><span class="sxs-lookup"><span data-stu-id="29abb-107">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="29abb-108">Näiteks saate seadistada ühe hierarhia maksu-, õigus- või seadusliku aruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="29abb-108">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="29abb-109">Seejärel saate seadistada teise hierarhia finantsteabe aruandluseks, mis ei ole õiguslikult vajalik, kuid mida kasutatakse sisemises aruandluses.</span><span class="sxs-lookup"><span data-stu-id="29abb-109">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="29abb-110">Enne organisatsiooni hierarhia loomist tuleb luua organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="29abb-110">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="29abb-111">Lisateabe saamiseks vaadake jaotist [Juriidiliste isikute loomine](channels-legal-entities.md) või [Tootmisüksuste loomine](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="29abb-111">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="29abb-112">Lisateavet vt järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="29abb-112">For more information, see the following topics.</span></span>
- [<span data-ttu-id="29abb-113">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="29abb-113">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="29abb-114">Organisatsiooni hierarhia kavandamine</span><span class="sxs-lookup"><span data-stu-id="29abb-114">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="29abb-115">Organisatsioonihierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="29abb-115">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="29abb-116">Organisatsioonihierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="29abb-116">Create an organizational hierarchy</span></span>

<span data-ttu-id="29abb-117">Organisatsiooni hierarhia loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="29abb-117">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="29abb-118">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Organisatsiooni hierarhiad**.</span><span class="sxs-lookup"><span data-stu-id="29abb-118">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="29abb-119">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="29abb-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="29abb-120">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="29abb-120">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="29abb-121">Jaotises **Eesmärk** valige **Määra eesmärk**.</span><span class="sxs-lookup"><span data-stu-id="29abb-121">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="29abb-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="29abb-122">In the list, find and select the desired record.</span></span> <span data-ttu-id="29abb-123">Valige organisatsiooni hierarhiale määratav eesmärk.</span><span class="sxs-lookup"><span data-stu-id="29abb-123">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="29abb-124">Jaotises **Määratud hierarhiad** valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="29abb-124">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="29abb-125">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="29abb-125">In the list, mark the selected row.</span></span> <span data-ttu-id="29abb-126">Otsige äsja loodud hierarhia üles.</span><span class="sxs-lookup"><span data-stu-id="29abb-126">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="29abb-127">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="29abb-127">Select **OK**.</span></span>

<span data-ttu-id="29abb-128">Järgmine pilt näitab organisatsiooni hierarhia näidet, mis on loodud fiktiivsete "Adventure Works" kauplusteketi jaoks.</span><span class="sxs-lookup"><span data-stu-id="29abb-128">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Organisatsiooni hierarhia näide](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="29abb-130">Organisatsioonide lisamine hierarhiasse</span><span class="sxs-lookup"><span data-stu-id="29abb-130">Add organizations to a hierarchy</span></span>

<span data-ttu-id="29abb-131">Hierarhiale organisatsioonide lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="29abb-131">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="29abb-132">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="29abb-132">In the list, find and select the desired record.</span></span> <span data-ttu-id="29abb-133">Valige hierarhia.</span><span class="sxs-lookup"><span data-stu-id="29abb-133">Select your hierarchy.</span></span>
1. <span data-ttu-id="29abb-134">Valige tegevuspaanil nupp **Kuva**.</span><span class="sxs-lookup"><span data-stu-id="29abb-134">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="29abb-135">Vajaduse korral lisage organisatsioone.</span><span class="sxs-lookup"><span data-stu-id="29abb-135">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="29abb-136">Organisatsiooni lisamiseks valige **Redigeerige** ja seejärel valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="29abb-136">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="29abb-137">Kui olete muudatuste tegemise lõpetanud, saate salvestada mustandi ja muudatused avaldada.</span><span class="sxs-lookup"><span data-stu-id="29abb-137">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="29abb-138">Järgmine pilt näitab hierarhia juurele lisatud juriidilist isikut nelja lisatud kulukeskusega kanalitele "Ostukeskus", "Outlet-pood", "Veeb" ja "Kõnekeskus".</span><span class="sxs-lookup"><span data-stu-id="29abb-138">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="29abb-139">Seejärel saab igale lisada erinevaid jaemüügi-, kõnekeskuse- ja veebikanaleid.</span><span class="sxs-lookup"><span data-stu-id="29abb-139">Various retail, call center and online channels can then be added to each.</span></span>

![Hierarhia kujundaja näide](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="29abb-141">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="29abb-141">Additional resources</span></span>

[<span data-ttu-id="29abb-142">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="29abb-142">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="29abb-143">Organisatsioonihierarhia kavandamine</span><span class="sxs-lookup"><span data-stu-id="29abb-143">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="29abb-144">Juriidiliste isikute loomine</span><span class="sxs-lookup"><span data-stu-id="29abb-144">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="29abb-145">Tootmisüksuste loomine</span><span class="sxs-lookup"><span data-stu-id="29abb-145">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="29abb-146">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="29abb-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="29abb-147">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="29abb-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)
