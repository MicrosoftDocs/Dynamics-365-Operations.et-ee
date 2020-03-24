---
title: Kohandatud lehtede seadistamine kasutajate sisselogimise jaoks
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce kohandatud lehti, mis käsitsevad Azure Active Directory (Azure AD) ettevõtte ja tarbija (B2C) rentnike kohandatud sisselogimisi.
author: brianshook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 210a7d1c2b0a9a9606723b48681cca3a50fcc05b
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096793"
---
# <a name="set-up-custom-pages-for-user-logins"></a><span data-ttu-id="65be2-103">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="65be2-103">Set up custom pages for user logins</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="65be2-104">Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce kohandatud lehti, mis käsitsevad Azure Active Directory (Azure AD) ettevõtte ja tarbija (B2C) rentnike kohandatud sisselogimisi.</span><span class="sxs-lookup"><span data-stu-id="65be2-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

## <a name="overview"></a><span data-ttu-id="65be2-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="65be2-105">Overview</span></span>

<span data-ttu-id="65be2-106">Kohandatud lehtede kasutamiseks, mis on rakenduses Dynamics 365 Commerce volitatud käsitsema kasutaja sisselogimise voogusid, peate seadistama Azure AD poliitikad, millele Commerce’i keskkonnas viidatakse.</span><span class="sxs-lookup"><span data-stu-id="65be2-106">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="65be2-107">Saate konfigureerida Azure AD B2C poliitikaid „Registreerimine ja sisselogimine”, „Profiili redigeerimine” ja „Parooli lähtestamine”, kasutades Azure AD B2C rakendust.</span><span class="sxs-lookup"><span data-stu-id="65be2-107">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="65be2-108">Azure AD B2C rentniku ja poliitika nimedele saab seejärel viidata ettevalmistamise protsessi käigus, mis on tehtud Commerce’i keskkonnas, kasutades Microsoft Dynamicsi teenust Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="65be2-108">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="65be2-109">Kohandatud Commerce’i lehti saab luua, kasutades sisselogimist, registreerumist, konto profiili redigeerimist või parooli lähtestamise moodulit.</span><span class="sxs-lookup"><span data-stu-id="65be2-109">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="65be2-110">Nendele kohandatud lehtede jaoks avaldatud lehe URL-idele tuleb seejärel viidata Azure AD B2C poliitika konfiguratsioonides Azure’i portaalis.</span><span class="sxs-lookup"><span data-stu-id="65be2-110">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="65be2-111">B2C poliitikate seadistamine</span><span class="sxs-lookup"><span data-stu-id="65be2-111">Set up B2C policies</span></span>

<span data-ttu-id="65be2-112">Pärast Azure AD B2C rentniku seadistamist ja selle seostamist oma Commerce’i keskkonnaga, avage Azure’i portaalis leht **Azure AD B2C** ja seejärel valige menüüs jaotises **poliitikad** suvand **Kasutaja vood (poliitikad)**.</span><span class="sxs-lookup"><span data-stu-id="65be2-112">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Kasutajavoogude (poliitikate) käsk menüüs](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="65be2-114">Nüüd saate konfigureerida kasutaja sisselogimise vood „Registreerimine ja sisselogimine”, „Profiili redigeerimine” ja „Parooli lähtestamine”.</span><span class="sxs-lookup"><span data-stu-id="65be2-114">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="65be2-115">Poliitika „Registreerimine ja sisselogimine” konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="65be2-115">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="65be2-116">Poliitika „Registreerimine ja sisselogimine” konfigureerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="65be2-116">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="65be2-117">Valige suvand **Uus kasutaja voog** ja seejärel valige vahekaardil **Soovitatav** poliitika **Registreerimine ja sisselogimine**.</span><span class="sxs-lookup"><span data-stu-id="65be2-117">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="65be2-118">Sisestage poliitika nimi (nt **B2C\_1\_SignInSignUp**).</span><span class="sxs-lookup"><span data-stu-id="65be2-118">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="65be2-119">Jaotises **Identiteedipakkujad** valige poliitika jaoks kasutatavad identiteedipakkujad.</span><span class="sxs-lookup"><span data-stu-id="65be2-119">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="65be2-120">Minimaalselt peab olema valitud **Registreerimine meili teel**.</span><span class="sxs-lookup"><span data-stu-id="65be2-120">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="65be2-121">Veerus **Atribuudi kogumine** märkige märkeruudud suvandite **Meiliaadressid**, **Eesnimi** ja **Perekonnanimi** juures.</span><span class="sxs-lookup"><span data-stu-id="65be2-121">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="65be2-122">Veerus **Tagastamise nõue** märkige märkeruudud suvandite **Meiliaadressid**, **Eesnimi**, **Identiteedipakkuja**, **Perekonnanimi** ja **Kasutaja objekti ID** juures.</span><span class="sxs-lookup"><span data-stu-id="65be2-122">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Valitud atribuudid ja nõuded](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="65be2-124">Poliitika loomiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="65be2-124">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="65be2-125">Topeltklõpsake uuel poliitika nimel ja seejärel valige navigeerimispaanil suvand **Atribuudid.**</span><span class="sxs-lookup"><span data-stu-id="65be2-125">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="65be2-126">Seadke suvand **JavaScripti lehe paigutuse (eelvaade) jõustamise lubamine** valikule **Sees**.</span><span class="sxs-lookup"><span data-stu-id="65be2-126">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Uue poliitika atribuutide leht](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="65be2-128">Poliitika nimi on Commerce’i keskkonnas täielikult viidatud.</span><span class="sxs-lookup"><span data-stu-id="65be2-128">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="65be2-129">(Viitesse kaasatakse eesliide **B2C\_1\_**.) Poliitikaid ei saa pärast loomist ümber nimetada.</span><span class="sxs-lookup"><span data-stu-id="65be2-129">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="65be2-130">Kui asendate oma Commerce’i keskkonna olemasoleva poliitika, saate kustutada algse poliitika ja luua uue poliitika, millel on sama nimi.</span><span class="sxs-lookup"><span data-stu-id="65be2-130">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="65be2-131">Teise võimalusena, kui keskkond on juba ette valmistatud, saate teenusetaotluse kaudu esitada uue poliitika nime.</span><span class="sxs-lookup"><span data-stu-id="65be2-131">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="65be2-132">Pärast kohandatud lehtede loomist naasete sellesse poliitikasse seadistuse lõpetamiseks.</span><span class="sxs-lookup"><span data-stu-id="65be2-132">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="65be2-133">Praegu sulgege poliitika, et naasta Azure’i portaali lehele **Kasutaja vood (poliitikad)**.</span><span class="sxs-lookup"><span data-stu-id="65be2-133">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="65be2-134">Poliitika „Profiili redigeerimine” konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="65be2-134">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="65be2-135">Poliitika „Profiili redigeerimine” konfigureerimiseks järgige allolevaid etappe.</span><span class="sxs-lookup"><span data-stu-id="65be2-135">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="65be2-136">Valige suvand **Uus kasutaja voog** ja seejärel valige vahekaardil **Soovitatav** poliitika **Profiili redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="65be2-136">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="65be2-137">Sisestage poliitika nimi (nt **B2C\_1\_EditProfile**).</span><span class="sxs-lookup"><span data-stu-id="65be2-137">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="65be2-138">Jaotises **Identiteedipakkujad** valige poliitika jaoks kasutatavad identiteedipakkujad.</span><span class="sxs-lookup"><span data-stu-id="65be2-138">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="65be2-139">Minimaalselt peab olema valitud**Kohaliku konto sisselogimine**.</span><span class="sxs-lookup"><span data-stu-id="65be2-139">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="65be2-140">Veerus **Atribuudi kogumine** märkige märkeruudud suvandite **Meiliaadressid** ja **Perekonnanimi** juures.</span><span class="sxs-lookup"><span data-stu-id="65be2-140">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="65be2-141">Veerus **Tagastamise nõue** märkige märkeruudud suvandite **Meiliaadressid**, **Eesnimi**, **Identiteedipakkuja**, **Perekonnanimi** ja **Kasutaja objekti ID** juures.</span><span class="sxs-lookup"><span data-stu-id="65be2-141">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="65be2-142">Poliitika loomiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="65be2-142">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="65be2-143">Topeltklõpsake uuel poliitika nimel ja seejärel valige navigeerimispaanil suvand **Atribuudid.**</span><span class="sxs-lookup"><span data-stu-id="65be2-143">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="65be2-144">Seadke suvand **JavaScripti lehe paigutuse (eelvaade) jõustamise lubamine** valikule **Sees**.</span><span class="sxs-lookup"><span data-stu-id="65be2-144">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="65be2-145">Pärast kohandatud lehtede loomist naasete sellesse poliitikasse seadistuse lõpetamiseks.</span><span class="sxs-lookup"><span data-stu-id="65be2-145">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="65be2-146">Praegu sulgege poliitika, et naasta Azure’i portaali lehele **Kasutaja vood (poliitikad)**.</span><span class="sxs-lookup"><span data-stu-id="65be2-146">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="65be2-147">Poliitika „Parooli lähtestamine” konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="65be2-147">Configure the "Password reset" policy</span></span>

<span data-ttu-id="65be2-148">Poliitika „Parooli lähtestamine” konfigureerimiseks järgige allolevaid etappe.</span><span class="sxs-lookup"><span data-stu-id="65be2-148">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="65be2-149">Valige suvand **Uus kasutaja voog** ja seejärel valige vahekaardil **Eelvaade** poliitika **Parooli lähtestamine v1.1**.</span><span class="sxs-lookup"><span data-stu-id="65be2-149">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Eelvaate vahekaardil on valitud poliitika Parooli lähtestamine v1.1.](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="65be2-151">Sisestage poliitika nimi (nt **B2C\_1\_ForgetPassword**).</span><span class="sxs-lookup"><span data-stu-id="65be2-151">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="65be2-152">Jaotises **Identiteedipakkujad** valige suvand **Parooli lähtestamine meiliaadressi kasutades**.</span><span class="sxs-lookup"><span data-stu-id="65be2-152">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="65be2-153">Veerus **Tagastamise nõue** märkige märkeruudud suvandite **Meiliaadressid**, **Eesnimi**, **Perekonnanimi** ja **Kasutaja objekti ID** juures.</span><span class="sxs-lookup"><span data-stu-id="65be2-153">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Valitud nõuded](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="65be2-155">Poliitika loomiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="65be2-155">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="65be2-156">Topeltklõpsake uuel poliitika nimel ja seejärel valige navigeerimispaanil suvand **Atribuudid.**</span><span class="sxs-lookup"><span data-stu-id="65be2-156">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="65be2-157">Seadke suvand **JavaScripti lehe paigutuse (eelvaade) jõustamise lubamine** valikule **Sees**.</span><span class="sxs-lookup"><span data-stu-id="65be2-157">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="65be2-158">Pärast kohandatud lehtede loomist naasete sellesse poliitikasse seadistuse lõpetamiseks.</span><span class="sxs-lookup"><span data-stu-id="65be2-158">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="65be2-159">Praegu sulgege poliitika, et naasta Azure’i portaali lehele **Kasutaja vood (poliitikad)**.</span><span class="sxs-lookup"><span data-stu-id="65be2-159">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="65be2-160">Kohandatud lehtede koostamine</span><span class="sxs-lookup"><span data-stu-id="65be2-160">Build the custom pages</span></span>

<span data-ttu-id="65be2-161">Kasutaja sisselogimiste käsitsemiseks kohandatud lehtede koostamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="65be2-161">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="65be2-162">Avage Commerce’i autorluse tööriistades oma sait.</span><span class="sxs-lookup"><span data-stu-id="65be2-162">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="65be2-163">Koostage järgmised viis malli ja viis lehte.</span><span class="sxs-lookup"><span data-stu-id="65be2-163">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="65be2-164">Mall **Sisselogimine** ja sisselogimise moodulit kasutav leht.</span><span class="sxs-lookup"><span data-stu-id="65be2-164">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="65be2-165">Mall **Registreerimine** ja registreerimise moodulit kasutav leht.</span><span class="sxs-lookup"><span data-stu-id="65be2-165">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="65be2-166">Mall **Parooli lähtestamine** ja parooli lähtestamise moodulit kasutav leht.</span><span class="sxs-lookup"><span data-stu-id="65be2-166">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="65be2-167">Mall **Parooli lähtestamise kinnitus** ja parooli lähtestamise kinnituse moodulit kasutav leht.</span><span class="sxs-lookup"><span data-stu-id="65be2-167">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="65be2-168">Mall **Profiili redigeerimine** ja konto profiili redigeerimise moodulit kasutav leht.</span><span class="sxs-lookup"><span data-stu-id="65be2-168">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="65be2-169">Lehtede loomisel järgige järgmisi juhiseid.</span><span class="sxs-lookup"><span data-stu-id="65be2-169">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="65be2-170">Kasutage iga lehe või mooduli jaoks paigutust ja stiili, mis vastab kõige paremini teie ettevõtte vajadustele.</span><span class="sxs-lookup"><span data-stu-id="65be2-170">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="65be2-171">Avaldage kõik lehed ja URL-id, mida tuleb Azure AD B2C seadistuses kasutada.</span><span class="sxs-lookup"><span data-stu-id="65be2-171">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="65be2-172">Pärast lehtede ja URL-ide avaldamist koguge URL-id, mida tuleb kasutada Azure AD B2C poliitika konfiguratsioonideks.</span><span class="sxs-lookup"><span data-stu-id="65be2-172">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="65be2-173">Igale URL-ile lisatakse selle kasutamisel järelliide **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="65be2-173">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65be2-174">Ärge korduvkasutage universaalseid päiseid ja jaluseid, millel on suhtelised lingid.</span><span class="sxs-lookup"><span data-stu-id="65be2-174">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="65be2-175">Kuna need lehed majutatakse kasutamisel Azure AD B2C domeenis, tuleks kõikide linkide jaoks kasutada ainult absoluutseid URL-e.</span><span class="sxs-lookup"><span data-stu-id="65be2-175">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="65be2-176">Azure AD B2C poliitikate konfigureerimine kohandatud lehe teabega</span><span class="sxs-lookup"><span data-stu-id="65be2-176">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="65be2-177">Naaske Azure’i portaalis lehele **Azure AD B2C** ja valige menüüs jaotises **Poliitikad** suvand **Kasutajavood (poliitikad)**.</span><span class="sxs-lookup"><span data-stu-id="65be2-177">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="65be2-178">Poliitika „Registreerimine ja sisselogimine” kohandatud lehe teabega värskendamine</span><span class="sxs-lookup"><span data-stu-id="65be2-178">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="65be2-179">Poliitika „Registreerimine ja sisselogimine” kohandatud lehe teabega värskendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="65be2-179">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="65be2-180">Valige varasemalt konfigureeritud poliitikas **Registreerimine ja sisselogimine** navigeerimispaanil suvand **Lehe paigutused**.</span><span class="sxs-lookup"><span data-stu-id="65be2-180">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="65be2-181">Valige paigutus **Ühendatud registreerimine või sisselogimise leht**.</span><span class="sxs-lookup"><span data-stu-id="65be2-181">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="65be2-182">Seadistage suvand **Kohandatud lehe sisu kasutamine** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="65be2-182">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="65be2-183">Sisestage väljal **Kohandatud lehe URL** täispikk sisselogimise URL.</span><span class="sxs-lookup"><span data-stu-id="65be2-183">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="65be2-184">Lisage järelliide **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="65be2-184">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="65be2-185">Sisestage näiteks ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="65be2-185">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="65be2-186">Valige väljal **Lehe paigutuse versioon (eelvaade)** suvand **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="65be2-186">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="65be2-187">Valige paigutus **Kohaliku konto registreerimise leht**.</span><span class="sxs-lookup"><span data-stu-id="65be2-187">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="65be2-188">Seadistage suvand **Kohandatud lehe sisu kasutamine** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="65be2-188">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="65be2-189">Sisestage väljal **Kohandatud lehe URL** täispikk registreerimise URL.</span><span class="sxs-lookup"><span data-stu-id="65be2-189">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="65be2-190">Lisage järelliide **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="65be2-190">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="65be2-191">Sisestage näiteks ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="65be2-191">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="65be2-192">Valige väljal **Lehe paigutuse versioon (eelvaade)** suvand **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="65be2-192">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="65be2-193">Järgige jaotises **Kasutaja atribuudid** järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="65be2-193">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="65be2-194">Atribuutide **Meiliaadressid**, **Eesnimi** ja **Perekonnanimi** jaoks valige suvand **Ei** väljal **Vajab kinnitamist**.</span><span class="sxs-lookup"><span data-stu-id="65be2-194">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="65be2-195">Atribuutide **Eesnimi** ja **Perekonnanimi** jaoks valige suvand **Ei** väljal **Valikuline**.</span><span class="sxs-lookup"><span data-stu-id="65be2-195">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Kohaliku konto lehe poliitika konfigureerimine](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="65be2-197">Poliitika „Profiili redigeerimine” kohandatud lehe teabega värskendamine</span><span class="sxs-lookup"><span data-stu-id="65be2-197">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="65be2-198">Poliitika „Profiili redigeerimine” kohandatud lehe teabega värskendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="65be2-198">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="65be2-199">Valige varasemalt konfigureeritud poliitikas **Profiili redigeerimine** navigeerimispaanil suvand **Lehe paigutused**.</span><span class="sxs-lookup"><span data-stu-id="65be2-199">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="65be2-200">Valige paigutus**Profiili redigeerimise leht**.</span><span class="sxs-lookup"><span data-stu-id="65be2-200">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="65be2-201">Seadistage suvand **Kohandatud lehe sisu kasutamine** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="65be2-201">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="65be2-202">Sisestage väljal **Kohandatud lehe URL** täispikk profiili redigeerimise URL.</span><span class="sxs-lookup"><span data-stu-id="65be2-202">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="65be2-203">Lisage järelliide **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="65be2-203">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="65be2-204">Sisestage näiteks ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="65be2-204">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="65be2-205">Valige väljal **Lehe paigutuse versioon (eelvaade)** suvand **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="65be2-205">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="65be2-206">Järgige jaotises **Kasutaja atribuudid** järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="65be2-206">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="65be2-207">Atribuutide **Meiliaadressid** ja **Eesnimi** jaoks valige suvand **Ei** väljal **Vajab kinnitamist**.</span><span class="sxs-lookup"><span data-stu-id="65be2-207">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="65be2-208">Atribuutide **Eesnimi** ja **Perekonnanimi** jaoks valige suvand **Ei** väljal **Valikuline**.</span><span class="sxs-lookup"><span data-stu-id="65be2-208">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="65be2-209">Poliitika „Parooli lähtestamine” kohandatud lehe teabega värskendamine</span><span class="sxs-lookup"><span data-stu-id="65be2-209">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="65be2-210">Poliitika „Parooli lähtestamine” kohandatud lehe teabega värskendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="65be2-210">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="65be2-211">Valige varasemalt konfigureeritud poliitikas **Parooli lähtestamine** navigeerimispaanil suvand **Lehe paigutused**.</span><span class="sxs-lookup"><span data-stu-id="65be2-211">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="65be2-212">Valige paigutus **Uue parooli leht**.</span><span class="sxs-lookup"><span data-stu-id="65be2-212">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="65be2-213">Seadistage suvand **Kohandatud lehe sisu kasutamine** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="65be2-213">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="65be2-214">Sisestage väljal **Kohandatud lehe URL** täispikk parooli lähtestamise URL.</span><span class="sxs-lookup"><span data-stu-id="65be2-214">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="65be2-215">Lisage järelliide **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="65be2-215">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="65be2-216">Sisestage näiteks ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="65be2-216">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="65be2-217">Valige väljal **Lehe paigutuse versioon (eelvaade)** suvand **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="65be2-217">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="65be2-218">Valige paigutus **Konto kinnitamise leht**.</span><span class="sxs-lookup"><span data-stu-id="65be2-218">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="65be2-219">Seadistage suvand **Kohandatud lehe sisu kasutamine** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="65be2-219">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="65be2-220">Sisestage väljal **Kohandatud lehe URL** täispikk parooli lähtestamise kinnitamise URL.</span><span class="sxs-lookup"><span data-stu-id="65be2-220">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="65be2-221">Lisage järelliide **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="65be2-221">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="65be2-222">Sisestage näiteks ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="65be2-222">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="65be2-223">Valige väljal **Lehe paigutuse versioon (eelvaade)** suvand **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="65be2-223">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="65be2-224">Siltide ja kirjelduste vaikimisi tekstistringide kohandamine</span><span class="sxs-lookup"><span data-stu-id="65be2-224">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="65be2-225">Alustuskomplektis on sisselogimise moodulid eeltäidetud siltide ja kirjelduste vaikimisi tekstistringidega.</span><span class="sxs-lookup"><span data-stu-id="65be2-225">In the starter kit, sign in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="65be2-226">Saate neid stringe tarkvara arenduskomplektis (SDK) kohandada, uuendades sisselogimise mooduli väärtusi failis global.json.</span><span class="sxs-lookup"><span data-stu-id="65be2-226">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="65be2-227">Näiteks unustatud parooli lingi vaiketekst on **Unustatud parool?**.</span><span class="sxs-lookup"><span data-stu-id="65be2-227">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="65be2-228">Järgnevalt on näidatud see vaiketekst sisselogimise lehel.</span><span class="sxs-lookup"><span data-stu-id="65be2-228">The following shows this default text on the sign-in page.</span></span>

![Sisselogimislehe ununenud parooli lingi vaiketekst](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="65be2-230">Samas alustuskomplekti sisselogimismooduli failis global.json saate muuta tekstiks **Kas unustasite parooli?**, nagu järgmises näites on näidatud.</span><span class="sxs-lookup"><span data-stu-id="65be2-230">However, in the global.json file for the starter kit sign in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Värskendatud lingi tekst logisse mooduli Global. JSON failis](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="65be2-232">Pärast faili global.json uuendamist ja muudatuste avaldamist ilmub sisselogimise moodulil uus tekst nii Commerce’is kui ka raalajas sisselogimise lehel.</span><span class="sxs-lookup"><span data-stu-id="65be2-232">After you update the global.json file and publish your changes, the new link text appears in the sign in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65be2-233">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="65be2-233">Additional resources</span></span>

[<span data-ttu-id="65be2-234">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="65be2-234">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="65be2-235">Uue e-kaubanduse saidi juurutamine</span><span class="sxs-lookup"><span data-stu-id="65be2-235">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="65be2-236">Võrgupoe kanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="65be2-236">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="65be2-237">e-Commerce saidi loomine</span><span class="sxs-lookup"><span data-stu-id="65be2-237">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="65be2-238">Veebisaidi seostamine kanaliga</span><span class="sxs-lookup"><span data-stu-id="65be2-238">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="65be2-239">robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="65be2-239">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="65be2-240">URL-i hulgiümbersuunamiste üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="65be2-240">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="65be2-241">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="65be2-241">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="65be2-242">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="65be2-242">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="65be2-243">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="65be2-243">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="65be2-244">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="65be2-244">Enable location-based store detection</span></span>](enable-store-detection.md)
