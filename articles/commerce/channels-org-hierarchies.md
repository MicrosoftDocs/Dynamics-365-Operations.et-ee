---
title: Organisatsiooni hierarhiate seadistamine
description: Selle teema all kirjeldatakse organisatsiooni hierarhiate seadistust rakenduses Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4238d1aa277bf2f1df30825ef20dbf3095d13ebc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800563"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="f1577-103">Organisatsiooni hierarhiate häälestus</span><span class="sxs-lookup"><span data-stu-id="f1577-103">Set up organization hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1577-104">Selle teema all kirjeldatakse organisatsiooni hierarhiate seadistust rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f1577-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f1577-105">Enne kanalite loomist peate veenduma, et teie organisatsiooni hierarhiad on seadistatud.</span><span class="sxs-lookup"><span data-stu-id="f1577-105">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="f1577-106">Saate kasutada organisatsiooni hierarhiaid oma äri vaatamiseks ja selle aruandluse tegemiseks erinevatest aspektidest.</span><span class="sxs-lookup"><span data-stu-id="f1577-106">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="f1577-107">Näiteks saate seadistada ühe hierarhia maksu-, õigus- või seadusliku aruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="f1577-107">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="f1577-108">Seejärel saate seadistada teise hierarhia finantsteabe aruandluseks, mis ei ole õiguslikult vajalik, kuid mida kasutatakse sisemises aruandluses.</span><span class="sxs-lookup"><span data-stu-id="f1577-108">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="f1577-109">Enne organisatsiooni hierarhia loomist tuleb luua organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="f1577-109">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="f1577-110">Lisateabe saamiseks vaadake jaotist [Juriidiliste isikute loomine](channels-legal-entities.md) või [Tootmisüksuste loomine](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="f1577-110">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="f1577-111">Lisateavet vt järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="f1577-111">For more information, see the following topics.</span></span>
- [<span data-ttu-id="f1577-112">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="f1577-112">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="f1577-113">Organisatsiooni hierarhia kavandamine</span><span class="sxs-lookup"><span data-stu-id="f1577-113">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="f1577-114">Organisatsioonihierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="f1577-114">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="f1577-115">Organisatsioonihierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="f1577-115">Create an organizational hierarchy</span></span>

<span data-ttu-id="f1577-116">Organisatsiooni hierarhia loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="f1577-116">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="f1577-117">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Organisatsiooni hierarhiad**.</span><span class="sxs-lookup"><span data-stu-id="f1577-117">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="f1577-118">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f1577-118">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f1577-119">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="f1577-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="f1577-120">Jaotises **Eesmärk** valige **Määra eesmärk**.</span><span class="sxs-lookup"><span data-stu-id="f1577-120">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="f1577-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f1577-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="f1577-122">Valige organisatsiooni hierarhiale määratav eesmärk.</span><span class="sxs-lookup"><span data-stu-id="f1577-122">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="f1577-123">Jaotises **Määratud hierarhiad** valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="f1577-123">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="f1577-124">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f1577-124">In the list, mark the selected row.</span></span> <span data-ttu-id="f1577-125">Otsige äsja loodud hierarhia üles.</span><span class="sxs-lookup"><span data-stu-id="f1577-125">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="f1577-126">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1577-126">Select **OK**.</span></span>

<span data-ttu-id="f1577-127">Järgmine pilt näitab organisatsiooni hierarhia näidet, mis on loodud fiktiivsete "Adventure Works" kauplusteketi jaoks.</span><span class="sxs-lookup"><span data-stu-id="f1577-127">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Organisatsiooni hierarhia näide](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="f1577-129">Organisatsioonide lisamine hierarhiasse</span><span class="sxs-lookup"><span data-stu-id="f1577-129">Add organizations to a hierarchy</span></span>

<span data-ttu-id="f1577-130">Hierarhiale organisatsioonide lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="f1577-130">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="f1577-131">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f1577-131">In the list, find and select the desired record.</span></span> <span data-ttu-id="f1577-132">Valige hierarhia.</span><span class="sxs-lookup"><span data-stu-id="f1577-132">Select your hierarchy.</span></span>
1. <span data-ttu-id="f1577-133">Valige tegevuspaanil nupp **Kuva**.</span><span class="sxs-lookup"><span data-stu-id="f1577-133">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="f1577-134">Vajaduse korral lisage organisatsioone.</span><span class="sxs-lookup"><span data-stu-id="f1577-134">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="f1577-135">Organisatsiooni lisamiseks valige **Redigeerige** ja seejärel valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="f1577-135">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="f1577-136">Kui olete muudatuste tegemise lõpetanud, saate salvestada mustandi ja muudatused avaldada.</span><span class="sxs-lookup"><span data-stu-id="f1577-136">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="f1577-137">Järgmine pilt näitab hierarhia juurele lisatud juriidilist isikut nelja lisatud kulukeskusega kanalitele "Ostukeskus", "Outlet-pood", "Veeb" ja "Kõnekeskus".</span><span class="sxs-lookup"><span data-stu-id="f1577-137">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="f1577-138">Seejärel saab igale lisada erinevaid jaemüügi-, kõnekeskuse- ja veebikanaleid.</span><span class="sxs-lookup"><span data-stu-id="f1577-138">Various retail, call center and online channels can then be added to each.</span></span>

![Hierarhia kujundaja näide](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="f1577-140">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f1577-140">Additional resources</span></span>

[<span data-ttu-id="f1577-141">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="f1577-141">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="f1577-142">Organisatsioonihierarhia kavandamine</span><span class="sxs-lookup"><span data-stu-id="f1577-142">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="f1577-143">Juriidiliste isikute loomine</span><span class="sxs-lookup"><span data-stu-id="f1577-143">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="f1577-144">Tootmisüksuste loomine</span><span class="sxs-lookup"><span data-stu-id="f1577-144">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="f1577-145">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="f1577-145">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="f1577-146">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="f1577-146">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
