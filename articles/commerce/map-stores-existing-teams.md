---
title: Kaupluste ja töörühmade vastendamine, kui töörühmad on olemas rakenduses Microsoft Teams
description: See teema käsitleb, kuidas vastendada gruppe ja vastavaid meeskondi Dynamics 365 Commerce peakontoris, kui teie organisatsioon on juba enne Microsoft Teams Commerce integratsioonimeeskondi loonud.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a711c1057b87bd792755ef91a84d1c28879c590
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908491"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="472dd-103">Kaupluste ja töörühmade vastendamine, kui töörühmad on olemas rakenduses Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="472dd-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="472dd-104">See teema käsitleb, kuidas vastendada gruppe ja vastavaid meeskondi Dynamics 365 Commerce peakontoris, kui teie organisatsioon on juba enne Microsoft Teams Commerce integratsioonimeeskondi loonud.</span><span class="sxs-lookup"><span data-stu-id="472dd-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="472dd-105">Organisatsioonil võib olla meeskondi, mis on loodud mõnede või kõigi oma poodide jaoks enne Dynamics 365 Commerce ja Microsoft Teams integreerimist.</span><span class="sxs-lookup"><span data-stu-id="472dd-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="472dd-106">Sel juhul peate Commerce POS-i vahel ülesannete sünkroonimise loomiseks vastendama kauplusi ja vastavaid meeskondi Microsoft Teams Commerce peakontoris.</span><span class="sxs-lookup"><span data-stu-id="472dd-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="472dd-107">Kaupluste ja vastavate töörühmade vastendamine Commerce peakontoris</span><span class="sxs-lookup"><span data-stu-id="472dd-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="472dd-108">Kaupluste ja vastavate töörühmade vastendamiseks Commerce peakontoris järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="472dd-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="472dd-109">Minge jaotisse **Süsteemihaldus \> Tööruum \> Andmehaldus**.</span><span class="sxs-lookup"><span data-stu-id="472dd-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="472dd-110">Valige **Ekspordi**.</span><span class="sxs-lookup"><span data-stu-id="472dd-110">Select **Export**.</span></span> 
1. <span data-ttu-id="472dd-111">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="472dd-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="472dd-112">Jaotises **Grupi nimi** sisestage "Ekspordi Teams vastendamine".</span><span class="sxs-lookup"><span data-stu-id="472dd-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="472dd-113">Valige kiirsakis **Valitud üksused** suvand **Lisa üksus**.</span><span class="sxs-lookup"><span data-stu-id="472dd-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="472dd-114">Ilmub dialoogiboks **Lisa üksus**.</span><span class="sxs-lookup"><span data-stu-id="472dd-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="472dd-115">Valige ripploendist **Üksuse nime** **Teams vastendamine allika ja töörühma vahel**.</span><span class="sxs-lookup"><span data-stu-id="472dd-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="472dd-116">Valige ripploendist **Sihtandmete vorming** suvand **CSV**.</span><span class="sxs-lookup"><span data-stu-id="472dd-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="472dd-117">Valige **Lisa** ja seejärel **Sulge**.</span><span class="sxs-lookup"><span data-stu-id="472dd-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="472dd-118">Tegevuspaanist üleval ja vasakul valige suvand **Ekspordi kohe**.</span><span class="sxs-lookup"><span data-stu-id="472dd-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="472dd-119">Valige **Üksuse töötlemise olek** alt **Lae fail alla**.</span><span class="sxs-lookup"><span data-stu-id="472dd-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="472dd-120">Eksporditud CSV-failis sisestage väärtused **SOURCETYPE**, **SOURCEID** ja **TEAMID** järgmiselt:</span><span class="sxs-lookup"><span data-stu-id="472dd-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="472dd-121">**SOURCETYPE** puhul "RetailStore".</span><span class="sxs-lookup"><span data-stu-id="472dd-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="472dd-122">**SOURCEID** puhul sisestage kaupluse number (nt San Francisco kaupluse puhul "000135").</span><span class="sxs-lookup"><span data-stu-id="472dd-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="472dd-123">Kaupluse numbrid leiate asukohast **Retail ja Commerce \> Kanalid \> Kauplused**.</span><span class="sxs-lookup"><span data-stu-id="472dd-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="472dd-124">**TEAMID** puhul sisestage vastav meeskonna ID Microsoft Teams asukohast (nt " 5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span><span class="sxs-lookup"><span data-stu-id="472dd-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="472dd-125">Meeskonna ID teavet võite leida veebilehelt [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="472dd-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="472dd-126">Salvestage CSV-fail oma kohalikku arvutisse.</span><span class="sxs-lookup"><span data-stu-id="472dd-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="472dd-127">Minge jaotisse **Süsteemihaldus \> Tööruum \> Andmehaldus** ja valige suvand **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="472dd-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="472dd-128">Valige kiirsakis **Valitud üksused** suvand **Lisa fail**.</span><span class="sxs-lookup"><span data-stu-id="472dd-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="472dd-129">Ilmub dialoogiboks **Lisa fail**.</span><span class="sxs-lookup"><span data-stu-id="472dd-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="472dd-130">Valige ripploendist **Üksuse nime** **Teams vastendamine allika ja töörühma vahel**.</span><span class="sxs-lookup"><span data-stu-id="472dd-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="472dd-131">Valige ripploendist **Algandmete vorming** suvand **CSV**.</span><span class="sxs-lookup"><span data-stu-id="472dd-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="472dd-132">Valige **Üleslaadimine ja lisamine**, seejärel valige eelnevalt salvestatud CSV-fail ja seejärel valige käsk **Ava**.</span><span class="sxs-lookup"><span data-stu-id="472dd-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="472dd-133">Valige dialoogiboksis **Lisa fail** suvand **Sulge**.</span><span class="sxs-lookup"><span data-stu-id="472dd-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="472dd-134">Valige toimingupaanil **Salvesta** ja seejärel **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="472dd-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="472dd-135">Järgmises näitepildis on näidatud Commerce-i **Ekspordi töörühmade vastendamise** grupp koos elementidega **Lisa üksus** ja eksporditud CSV-faili rõhutatud päistega.</span><span class="sxs-lookup"><span data-stu-id="472dd-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![Commerce-i töörühmade vastendamise grupi eksportimine koos üksuse lisamise elementidega ja eksporditud CSV-faili rõhutatud päistega.](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="472dd-137">Eeltoodud sammude järgselt järgige ülesandehalduse sünkroonimiseks jaotise [Microsoft Teams ja kassa vahelise toiminguhalduse ja sünkroonimine](synchronize-tasks-teams-pos.md) etappe.</span><span class="sxs-lookup"><span data-stu-id="472dd-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="472dd-138">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="472dd-138">Additional resources</span></span>

[<span data-ttu-id="472dd-139">Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülevaade</span><span class="sxs-lookup"><span data-stu-id="472dd-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="472dd-140">Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="472dd-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="472dd-141">Microsoft Teams sätted rakendusest Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="472dd-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="472dd-142">Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel</span><span class="sxs-lookup"><span data-stu-id="472dd-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="472dd-143">Kasutaja rollide haldamine rakenduses Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="472dd-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="472dd-144">Dynamics 365 Commerce ja Microsoft Teams integratsiooni KKK</span><span class="sxs-lookup"><span data-stu-id="472dd-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
