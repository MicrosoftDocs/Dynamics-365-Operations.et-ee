---
title: Organisatsiooni hierarhiate seadistamine
description: Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce organisatsiooni hierarhiaid seadistada.
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
ms.openlocfilehash: 6c19542089526c1e17fb1133d52cf042f244fb80
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002331"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="ebcf5-103">Organisatsiooni hierarhiate seadistamine</span><span class="sxs-lookup"><span data-stu-id="ebcf5-103">Set up organization hierarchies</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ebcf5-104">Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce organisatsiooni hierarhiaid seadistada.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-104">This topic descibes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ebcf5-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="ebcf5-105">Overview</span></span>

<span data-ttu-id="ebcf5-106">Enne kanalite loomist peate veenduma, et teie organisatsiooni hierarhiad on seadistatud.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-106">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="ebcf5-107">Saate kasutada organisatsiooni hierarhiaid oma äri vaatamiseks ja selle aruandluse tegemiseks erinevatest aspektidest.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-107">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="ebcf5-108">Näiteks saate seadistada ühe hierarhia maksu-, õigus- või seadusliku aruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-108">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="ebcf5-109">Seejärel saate seadistada teise hierarhia finantsteabe aruandluseks, mis ei ole õiguslikult vajalik, kuid mida kasutatakse sisemises aruandluses.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-109">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="ebcf5-110">Enne organisatsiooni hierarhia loomist tuleb luua organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-110">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="ebcf5-111">Lisateabe saamiseks vaadake jaotist [Juriidiliste isikute loomine](channels-legal-entities.md) või [Tootmisüksuste loomine](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="ebcf5-111">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="ebcf5-112">Lisateavet vt järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-112">For more information, see the following topics.</span></span>
- [<span data-ttu-id="ebcf5-113">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="ebcf5-113">Organizations and organizational hierarchies overview</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies)
- [<span data-ttu-id="ebcf5-114">Organisatsiooni hierarhia kavandamine</span><span class="sxs-lookup"><span data-stu-id="ebcf5-114">Plan your organization hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="ebcf5-115">Organisatsioonihierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="ebcf5-115">Create an organization hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="ebcf5-116">Organisatsioonihierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="ebcf5-116">Create an organizational hierarchy</span></span>

<span data-ttu-id="ebcf5-117">Organisatsiooni hierarhia loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-117">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="ebcf5-118">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Organisatsiooni hierarhiad**.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-118">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="ebcf5-119">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ebcf5-120">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-120">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="ebcf5-121">Jaotises **Eesmärk** valige **Määra eesmärk**.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-121">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="ebcf5-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-122">In the list, find and select the desired record.</span></span> <span data-ttu-id="ebcf5-123">Valige organisatsiooni hierarhiale määratav eesmärk.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-123">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="ebcf5-124">Jaotises **Määratud hierarhiad** valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-124">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="ebcf5-125">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-125">In the list, mark the selected row.</span></span> <span data-ttu-id="ebcf5-126">Otsige äsja loodud hierarhia üles.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-126">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="ebcf5-127">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-127">Select **OK**.</span></span>

<span data-ttu-id="ebcf5-128">Järgmine pilt näitab organisatsiooni hierarhia näidet, mis on loodud fiktiivsete "Adventure Works" kauplusteketi jaoks.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-128">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Organisatsiooni hierarhia näide](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="ebcf5-130">Organisatsioonide lisamine hierarhiasse</span><span class="sxs-lookup"><span data-stu-id="ebcf5-130">Add organizations to a hierarchy</span></span>

<span data-ttu-id="ebcf5-131">Hierarhiale organisatsioonide lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-131">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="ebcf5-132">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-132">In the list, find and select the desired record.</span></span> <span data-ttu-id="ebcf5-133">Valige hierarhia.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-133">Select your hierarchy.</span></span>
1. <span data-ttu-id="ebcf5-134">Valige tegevuspaanil nupp **Kuva**.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-134">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="ebcf5-135">Vajaduse korral lisage organisatsioone.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-135">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="ebcf5-136">Organisatsiooni lisamiseks valige **Redigeerige** ja seejärel valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-136">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="ebcf5-137">Kui olete muudatuste tegemise lõpetanud, saate salvestada mustandi ja muudatused avaldada.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-137">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="ebcf5-138">Järgmine pilt näitab hierarhia juurele lisatud juriidilist isikut nelja lisatud kulukeskusega kanalitele "Ostukeskus", "Outlet-pood", "Veeb" ja "Kõnekeskus".</span><span class="sxs-lookup"><span data-stu-id="ebcf5-138">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="ebcf5-139">Seejärel saab igale lisada erinevaid jaemüügi-, kõnekeskuse- ja veebikanaleid.</span><span class="sxs-lookup"><span data-stu-id="ebcf5-139">Various retail, call center and online channels can then be added to each.</span></span>

![Hierarhia kujundaja näide](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="ebcf5-141">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ebcf5-141">Additional resources</span></span>

[<span data-ttu-id="ebcf5-142">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="ebcf5-142">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="ebcf5-143">Organisatsioonihierarhia kavandamine</span><span class="sxs-lookup"><span data-stu-id="ebcf5-143">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="ebcf5-144">Juriidiliste isikute loomine</span><span class="sxs-lookup"><span data-stu-id="ebcf5-144">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="ebcf5-145">Tootmisüksuste loomine</span><span class="sxs-lookup"><span data-stu-id="ebcf5-145">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="ebcf5-146">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="ebcf5-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ebcf5-147">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="ebcf5-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)
