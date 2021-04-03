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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 490d466c10cfe0640f8fbcf8fe2298536e499d9b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477992"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="c6d9e-103">Organisatsiooni hierarhiate häälestus</span><span class="sxs-lookup"><span data-stu-id="c6d9e-103">Set up organization hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c6d9e-104">Selle teema all kirjeldatakse organisatsiooni hierarhiate seadistust rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c6d9e-105">Enne kanalite loomist peate veenduma, et teie organisatsiooni hierarhiad on seadistatud.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-105">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="c6d9e-106">Saate kasutada organisatsiooni hierarhiaid oma äri vaatamiseks ja selle aruandluse tegemiseks erinevatest aspektidest.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-106">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="c6d9e-107">Näiteks saate seadistada ühe hierarhia maksu-, õigus- või seadusliku aruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-107">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="c6d9e-108">Seejärel saate seadistada teise hierarhia finantsteabe aruandluseks, mis ei ole õiguslikult vajalik, kuid mida kasutatakse sisemises aruandluses.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-108">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="c6d9e-109">Enne organisatsiooni hierarhia loomist tuleb luua organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-109">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="c6d9e-110">Lisateabe saamiseks vaadake jaotist [Juriidiliste isikute loomine](channels-legal-entities.md) või [Tootmisüksuste loomine](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="c6d9e-110">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="c6d9e-111">Lisateavet vt järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-111">For more information, see the following topics.</span></span>
- [<span data-ttu-id="c6d9e-112">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="c6d9e-112">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="c6d9e-113">Organisatsiooni hierarhia kavandamine</span><span class="sxs-lookup"><span data-stu-id="c6d9e-113">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="c6d9e-114">Organisatsioonihierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="c6d9e-114">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="c6d9e-115">Organisatsioonihierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="c6d9e-115">Create an organizational hierarchy</span></span>

<span data-ttu-id="c6d9e-116">Organisatsiooni hierarhia loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-116">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="c6d9e-117">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Organisatsiooni hierarhiad**.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-117">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="c6d9e-118">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-118">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c6d9e-119">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="c6d9e-120">Jaotises **Eesmärk** valige **Määra eesmärk**.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-120">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="c6d9e-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="c6d9e-122">Valige organisatsiooni hierarhiale määratav eesmärk.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-122">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="c6d9e-123">Jaotises **Määratud hierarhiad** valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-123">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="c6d9e-124">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-124">In the list, mark the selected row.</span></span> <span data-ttu-id="c6d9e-125">Otsige äsja loodud hierarhia üles.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-125">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="c6d9e-126">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-126">Select **OK**.</span></span>

<span data-ttu-id="c6d9e-127">Järgmine pilt näitab organisatsiooni hierarhia näidet, mis on loodud fiktiivsete "Adventure Works" kauplusteketi jaoks.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-127">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Organisatsiooni hierarhia näide](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="c6d9e-129">Organisatsioonide lisamine hierarhiasse</span><span class="sxs-lookup"><span data-stu-id="c6d9e-129">Add organizations to a hierarchy</span></span>

<span data-ttu-id="c6d9e-130">Hierarhiale organisatsioonide lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-130">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="c6d9e-131">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-131">In the list, find and select the desired record.</span></span> <span data-ttu-id="c6d9e-132">Valige hierarhia.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-132">Select your hierarchy.</span></span>
1. <span data-ttu-id="c6d9e-133">Valige tegevuspaanil nupp **Kuva**.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-133">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="c6d9e-134">Vajaduse korral lisage organisatsioone.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-134">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="c6d9e-135">Organisatsiooni lisamiseks valige **Redigeerige** ja seejärel valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-135">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="c6d9e-136">Kui olete muudatuste tegemise lõpetanud, saate salvestada mustandi ja muudatused avaldada.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-136">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="c6d9e-137">Järgmine pilt näitab hierarhia juurele lisatud juriidilist isikut nelja lisatud kulukeskusega kanalitele "Ostukeskus", "Outlet-pood", "Veeb" ja "Kõnekeskus".</span><span class="sxs-lookup"><span data-stu-id="c6d9e-137">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="c6d9e-138">Seejärel saab igale lisada erinevaid jaemüügi-, kõnekeskuse- ja veebikanaleid.</span><span class="sxs-lookup"><span data-stu-id="c6d9e-138">Various retail, call center and online channels can then be added to each.</span></span>

![Hierarhia kujundaja näide](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="c6d9e-140">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c6d9e-140">Additional resources</span></span>

[<span data-ttu-id="c6d9e-141">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="c6d9e-141">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c6d9e-142">Organisatsioonihierarhia kavandamine</span><span class="sxs-lookup"><span data-stu-id="c6d9e-142">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c6d9e-143">Juriidiliste isikute loomine</span><span class="sxs-lookup"><span data-stu-id="c6d9e-143">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="c6d9e-144">Tootmisüksuste loomine</span><span class="sxs-lookup"><span data-stu-id="c6d9e-144">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c6d9e-145">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="c6d9e-145">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="c6d9e-146">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="c6d9e-146">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
