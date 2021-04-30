---
title: Microsoft Teams ettevalmistamine rakendusest Dynamics 365 Commerce
description: See teema kirjeldab, kuidas ette valmistada Microsoft Teams kasutades Dynamics 365 Commerce organisatsiooni andmeid.
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
ms.openlocfilehash: ba7c74942735b723d1015dc4da0068fbb631bc6b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908900"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="32df6-103">Microsoft Teams ettevalmistamine rakendusest Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="32df6-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="32df6-104">See teema kirjeldab, kuidas ette valmistada Microsoft Teams kasutades Dynamics 365 Commerce organisatsiooni andmeid.</span><span class="sxs-lookup"><span data-stu-id="32df6-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="32df6-105">Kui te ei ole veel jaekaupluste meeskondi seadistanud, on töörühmade ettevalmistamine rakenduses Dynamics 365 Commerce lihtne.</span><span class="sxs-lookup"><span data-stu-id="32df6-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="32df6-106">Kasutades Commerce'is hästi määratletud teavet, mida soovite Teamsis kasutada, saate aidata oma kaupluse töötajatel Teamsis alustada.</span><span class="sxs-lookup"><span data-stu-id="32df6-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="32df6-107">See teave sisaldab organisatsiooni hierarhiat, kaupluse nimesid, töötaja teavet ja Azure Active Directory (Azure AD) kontosid.</span><span class="sxs-lookup"><span data-stu-id="32df6-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="32df6-108">Teamsi ettevalmistamiseks on kaks peamist sammu:</span><span class="sxs-lookup"><span data-stu-id="32df6-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="32df6-109">Looge Teamsis igale kauplusele meeskond ja lisage sobiva töörühma liikmetena kaupluse töötajad.</span><span class="sxs-lookup"><span data-stu-id="32df6-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="32df6-110">Kui töötaja on seostatud rohkem kui ühe kauplusega, on seda näha töörühma liikmelisuses.</span><span class="sxs-lookup"><span data-stu-id="32df6-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="32df6-111">Luuakse kommunikatsioonimeeskond, mis kaasab piirkonna haldurid liikmetena, et aidata avaldada ülesandeid Teamsis.</span><span class="sxs-lookup"><span data-stu-id="32df6-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="32df6-112">Laadige oma organisatsioonihierarhia Teamsi üles rakendusest Commerce.</span><span class="sxs-lookup"><span data-stu-id="32df6-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="32df6-113">Teamsi ettevalmistamine Commerce'i peakontoris</span><span class="sxs-lookup"><span data-stu-id="32df6-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="32df6-114">Enne Microsoft Teams ettevalmistamist viige lõpule järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="32df6-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="32df6-115">Kinnitage, et kõik piirkonnajuhid oleksid tehtud kommunikatsioonijuhtideks.</span><span class="sxs-lookup"><span data-stu-id="32df6-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="32df6-116">Kinnitage, et iga kaupluse juhataja ja töötaja Azure'i konto oleks seostatud juhataja või töötaja kirjega Commerce'i peakontoris.</span><span class="sxs-lookup"><span data-stu-id="32df6-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="32df6-117">Teamsi ettevalmistamiseks Commerce'i peakontoris toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="32df6-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="32df6-118">Valige suvandid **Retail ja Commerce \> Kanali häälestus \> Microsoft Teams integratsiooni konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="32df6-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="32df6-119">Klõpsake toimingupaanil suvandit **Töörühmade ettevalmistamine**.</span><span class="sxs-lookup"><span data-stu-id="32df6-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="32df6-120">Luuakse partiitöö nimega **Töörühmade ettevalmistamine**.</span><span class="sxs-lookup"><span data-stu-id="32df6-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="32df6-121">Minge **Süsteemihaldus \> Päringud \> Partiitööd** ja leidke viimane töö, mille kirjeldus on **Teamsi ettevalmistamine**.</span><span class="sxs-lookup"><span data-stu-id="32df6-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="32df6-122">Oodake, kuni töö on lõpuni viidud.</span><span class="sxs-lookup"><span data-stu-id="32df6-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="32df6-123">Kui ükski teie piirkonna halduritest, kaupluste juhatajatest ja kaupluse töötajatest pole seotud Teams litsentsiga, võidakse kuvada järgmine tõrketeade: "Määratud SKU-kategooriate päring kasutajale nurjus."</span><span class="sxs-lookup"><span data-stu-id="32df6-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="32df6-124">Probleemi lahendamiseks valige tegevuspaanil suvand **Sünkrooni töörühmad ja liikmed**.</span><span class="sxs-lookup"><span data-stu-id="32df6-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="32df6-125">Teams ettevalmistamise valideerimine Teamsi halduskeskuses</span><span class="sxs-lookup"><span data-stu-id="32df6-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="32df6-126">Microsoft Teams halduskeskuses Microsoft Teams andmete ettevalmistamise kinnitamiseks järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="32df6-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="32df6-127">Minge [Teams halduskeskusesse](https://admin.teams.microsoft.com/) ja logige sisse oma e-äri rentniku administraatorina.</span><span class="sxs-lookup"><span data-stu-id="32df6-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="32df6-128">Selle laiendamiseks valige vasakul navigeerimispaanil **Teams** ja seejärel valige suvand **Halda töörühmasid**.</span><span class="sxs-lookup"><span data-stu-id="32df6-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="32df6-129">Veenduge, et iga Commerce'i jaemüügikaupluse jaoks oleks loodud üks meeskond.</span><span class="sxs-lookup"><span data-stu-id="32df6-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="32df6-130">Valige meeskond ja kinnitage, et kaupluse töötajad on sellele liikmeteks lisatud.</span><span class="sxs-lookup"><span data-stu-id="32df6-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="32df6-131">Valige vasakul navigeerimispaanil **Kasutajad** ja kinnitage, et kõik kaupluse töötajad on kasutajateks lisatud.</span><span class="sxs-lookup"><span data-stu-id="32df6-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="32df6-132">Järgmine näide on lehe **Töörühmade haldamine** kohta Teams halduskeskuses.</span><span class="sxs-lookup"><span data-stu-id="32df6-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![Töörühmade haldamise lehe näide Teams halduskeskuses](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="32df6-134">Laadige Commerce'i organisatsioonihierarhia Teamsi</span><span class="sxs-lookup"><span data-stu-id="32df6-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="32df6-135">Commerce hierarhiat saab kasutada ülesannete avaldamiseks rakenduses Microsoft Teams kõigile või valitud kauplustesse, mis kasutavad sama hierarhia struktuuri.</span><span class="sxs-lookup"><span data-stu-id="32df6-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="32df6-136">Faili üleslaadimiseks Commerce'i organisatsiooni hierarhiast Teamsi toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="32df6-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="32df6-137">Commerce'i peakontoris minge asukohta **Jaemüük ja kaubandus \> Kanali seadistamine \> Microsoft Teams integratsiooni konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="32df6-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="32df6-138">Valige **Allalaadimise sihthierarhia** ja valige seejärel **Jaemüügikauplused regiooni järgi**, et laadida alla organisatsiooni hierarhia komaeraldusega väärtused (CSV).</span><span class="sxs-lookup"><span data-stu-id="32df6-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="32df6-139">Installige Microsoft Teams PowerShelli moodul, järgides etappie jaotises [Microsoft TeamsPowerShelli installimine](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="32df6-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="32df6-140">Kui ilmub aknas Teams PowerShell teade, logige sisse, kasutades oma rentniku Azure AD administraatori kontot.</span><span class="sxs-lookup"><span data-stu-id="32df6-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="32df6-141">Järgige samme jaotises [Meeskonna sihthierarhia seadistamine](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) CSV-faili üleslaadimiseks sihthierarhia jaoks.</span><span class="sxs-lookup"><span data-stu-id="32df6-141">Follow the steps in [Set up your team targeting hierarchy](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="32df6-142">Veenduge, et organisatsiooni hierarhia oleks Teamsi üles laaditud.</span><span class="sxs-lookup"><span data-stu-id="32df6-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="32df6-143">Veendumaks, et organisatsiooni hierarhia on Microsoft Teams üles laaditud toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="32df6-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="32df6-144">Logige Teami suhtlushaldurina sisse.</span><span class="sxs-lookup"><span data-stu-id="32df6-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="32df6-145">Valige vasakul navigeerimispaanil **Planner ülesanded** alusel.</span><span class="sxs-lookup"><span data-stu-id="32df6-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="32df6-146">Looge vahekaardil **Avaldatud loendid** uus loend, mis sisaldab fiktiivset ülesannet.</span><span class="sxs-lookup"><span data-stu-id="32df6-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="32df6-147">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="32df6-147">Select **Publish**.</span></span> <span data-ttu-id="32df6-148">Organisatsioonihierarhia peaks ilmuma dialoogiboksis **Vali, kellele avaldada**, nagu näha järgmises näites.</span><span class="sxs-lookup"><span data-stu-id="32df6-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![Organisatsioonihierarhia näide dialoogiaknas Vali, kellele avaldada](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="32df6-150">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="32df6-150">Additional resources</span></span>

[<span data-ttu-id="32df6-151">Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülevaade</span><span class="sxs-lookup"><span data-stu-id="32df6-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="32df6-152">Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="32df6-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="32df6-153">Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel</span><span class="sxs-lookup"><span data-stu-id="32df6-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="32df6-154">Kasutaja rollide haldamine rakenduses Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="32df6-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="32df6-155">Kaupluste ja töörühmade vastendamine, kui töörühmad on olemas rakenduses Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="32df6-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="32df6-156">Dynamics 365 Commerce ja Microsoft Teams integratsiooni KKK</span><span class="sxs-lookup"><span data-stu-id="32df6-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
