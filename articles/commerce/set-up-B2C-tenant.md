---
title: B2C rentniku seadistus Kaubanduses
description: Selles teemas kirjeldatakse kuidas seadistada Azure Active Directory (Azure AD) ettevõtja ja tarbija vahelisi (B2C) rentnikke kasutaja saidi autentimiseks rakenduses Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: f31f8898358626f2b008826aa69694dc16742aa0
ms.sourcegitcommit: 59a9e840989bc9f2c7004efa3499b69c09a91b06
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677900"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="45ff3-103">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="45ff3-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="45ff3-104">Selles teemas kirjeldatakse kuidas seadistada Azure Active Directory (Azure AD) ettevõtja ja tarbija vahelisi (B2C) rentnikke kasutaja saidi autentimiseks rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="45ff3-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="45ff3-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="45ff3-105">Overview</span></span>

<span data-ttu-id="45ff3-106">Dynamics 365 Commerce kasutab Azure AD B2C'd kasutaja mandaadi ja autentimise voogude toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="45ff3-106">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="45ff3-107">Kasutaja saab nende voogude kaudu registreeruda, sisse logida ja lähtestada parooli.</span><span class="sxs-lookup"><span data-stu-id="45ff3-107">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="45ff3-108">Azure AD B2C talletab kasutaja tundliku autentimisteabe, nt kasutajanime ja parooli.</span><span class="sxs-lookup"><span data-stu-id="45ff3-108">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="45ff3-109">B2C rentniku kasutajakirje salvestab kas kohaliku B2C kontokirje või B2C sotsiaalse identiteedi pakkuja kirje.</span><span class="sxs-lookup"><span data-stu-id="45ff3-109">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="45ff3-110">Need B2C kirjed lingitakse Commerce'i keskkonna kliendikirjetega.</span><span class="sxs-lookup"><span data-stu-id="45ff3-110">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="45ff3-111">Olemasoleva AAD B2C rentniku loomine või linkimine Azure'i portaalis</span><span class="sxs-lookup"><span data-stu-id="45ff3-111">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="45ff3-112">Logige sisse [Azure’i portaali](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="45ff3-112">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="45ff3-113">Valige Azure'i portaali menüüst käsk **Loo ressurss**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-113">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="45ff3-114">Veenduge, et kasutate tellimust ja kataloogi, mis on seotud teie Commerce'i keskkonnaga.</span><span class="sxs-lookup"><span data-stu-id="45ff3-114">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![Ressursi loomine Azure'i portaalis](./media/B2CImage_1.png)

1. <span data-ttu-id="45ff3-116">Avage **Identiteedi \> Azure Active Directory B2C**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-116">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="45ff3-117">Kui olete lehel **Uue B2C üürniku loomine või olemasoleva rentnikuga linkimine**, kasutage ühte valikutest, mis sobib kõige paremini teie ettevõtte vajadustega.</span><span class="sxs-lookup"><span data-stu-id="45ff3-117">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="45ff3-118">**Loo uus Azure AD B2C rentnik**: kasutage seda valikut uue AAD B2C rentniku loomiseks.</span><span class="sxs-lookup"><span data-stu-id="45ff3-118">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="45ff3-119">Valige käsk **Loo uus Azure AD B2C rentnik**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-119">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="45ff3-120">Sisestage organisatsiooni nimi jaotises **Organisatsiooni nimi**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-120">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="45ff3-121">Sisestage algne domeeninimi jaotises **Algne domeeninimi**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-121">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="45ff3-122">Valige riik ja piirkond jaotises **Riik või piirkond**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-122">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="45ff3-123">Rentniku loomiseks valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-123">Select **Create** to create the tenant.</span></span>

     ![Uue Azure AD rentniku loomine](./media/B2CImage_2.png)

     - <span data-ttu-id="45ff3-125">**Olemasoleva Azure AD B2C rentniku linkimine minu Azure'i tellimusega**: kasutage seda suvandit, kui teil on Azure AD B2C rentnik, mida soovite linkida.</span><span class="sxs-lookup"><span data-stu-id="45ff3-125">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="45ff3-126">Valige **Olemasoleva Azure AD B2C rentniku linkimine minu Azure'i tellimusega**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-126">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="45ff3-127">Jaotises **Azure AD B2C rentnik** valige sobiv B2C rentnik.</span><span class="sxs-lookup"><span data-stu-id="45ff3-127">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="45ff3-128">Kui valikukastis kuvatakse teade „Ei leitud ühtegi sobilikku B2C rentnikku”, pole teil kehtivat sobilikku B2C rentnikku ja teil on vaja luua uus.</span><span class="sxs-lookup"><span data-stu-id="45ff3-128">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="45ff3-129">Tehke jaotises **Ressursigrupp** valik **Loo uus**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-129">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="45ff3-130">Sisestage ressursirühmale **Nimi**, mis sisaldab rentnikku ja valige **Ressursigrupi asukoht** ning seejärel **Loo**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-130">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![Olemasoleva Azure AD B2C rentniku linkimine minu Azure'i tellimusega](./media/B2CImage_3.png)

1. <span data-ttu-id="45ff3-132">Kui uus Azure AD B2C kaust on loodud (see võib võtta mõne hetke), kuvatakse armatuurlaual link uuele kaustale.</span><span class="sxs-lookup"><span data-stu-id="45ff3-132">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="45ff3-133">See link juhatab teid lehele „Tere tulemast Azure Active Directory B2C-sse”.</span><span class="sxs-lookup"><span data-stu-id="45ff3-133">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![Uue AAD kausta link](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="45ff3-135">Kui teie Azure'i kontol on mitu tellimust või olete seadistanud B2C rentniku aktiivsele tellimusele linkimata, suunab ribareklaam **Tõrkeotsing** rentnikku tellimusega linkima.</span><span class="sxs-lookup"><span data-stu-id="45ff3-135">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="45ff3-136">Valige tõrkeotsingu teade ja järgige tellimuse probleemi lahendamiseks juhiseid.</span><span class="sxs-lookup"><span data-stu-id="45ff3-136">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="45ff3-137">Järgmine pilt on Azure AD B2C ribareklaami **Tõrkeotsing** näide.</span><span class="sxs-lookup"><span data-stu-id="45ff3-137">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![Kuvatav hoiatus Kataloogist puudub aktiivne tellimus](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="45ff3-139">B2C rakenduse loomine</span><span class="sxs-lookup"><span data-stu-id="45ff3-139">Create the B2C application</span></span>

<span data-ttu-id="45ff3-140">Kui B2C rentnik on loodud, tuleb rentnikus luua B2C rakendus Commerce'i toimingutega suhtlemiseks.</span><span class="sxs-lookup"><span data-stu-id="45ff3-140">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="45ff3-141">B2C rakenduse loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="45ff3-141">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="45ff3-142">Tehke Azure'i portaalis valik **Rakendused (pärand)** ja seejärel **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-142">In the Azure portal, select **Applications(Legacy)** and then select **Add**.</span></span>
1. <span data-ttu-id="45ff3-143">Jaotises **Nimi** sisestage soovitud AAD B2C rakenduse nimi.</span><span class="sxs-lookup"><span data-stu-id="45ff3-143">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="45ff3-144">Jaotises **Veebirakendus/veebi-API** valige parameetrile **Veebirakenduse/veebi-API kaasamine** väärtus **Jah**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-144">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="45ff3-145">Määrake aarameetri **Varjatud voo lubamine** väärtuseks **Jah** (vaikeväärtus).</span><span class="sxs-lookup"><span data-stu-id="45ff3-145">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="45ff3-146">Jaotises **Vastuse URL** sisestage oma sihtotstarbelised vastuse URL-id.</span><span class="sxs-lookup"><span data-stu-id="45ff3-146">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="45ff3-147">Vaadake allpool teemat [Vastuse URL-id](#reply-urls) vastuse URL-ide ja nende vormindamise kohta lisateabe saamiseks.</span><span class="sxs-lookup"><span data-stu-id="45ff3-147">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="45ff3-148">Määrake parameetri **Algse kliendi kaasamine** väärtuseks **Ei** (vaikeväärtus).</span><span class="sxs-lookup"><span data-stu-id="45ff3-148">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="45ff3-149">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-149">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="45ff3-150">Vastuse URL-id</span><span class="sxs-lookup"><span data-stu-id="45ff3-150">Reply URLs</span></span>

<span data-ttu-id="45ff3-151">Vastuse URL-id on olulised, kuna need tagavad tagastusdomeenide lubatud üksuste loendi, kui teie sait küsib Azure AD B2C kasutaja autentimist.</span><span class="sxs-lookup"><span data-stu-id="45ff3-151">Reply URLs are important as they provide an allow list of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="45ff3-152">See lubab autenditud kasutajal pöörduda tagasi domeeni, kuhu ta sisse logib (teie saidi domeen).</span><span class="sxs-lookup"><span data-stu-id="45ff3-152">This permits the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="45ff3-153">Akna **Azure AD B2C - Rakendused \> Uus rakendus** kastis **Vastuse URL** tuleb lisada eraldi read nii saidi domeenile kui ka (kui teie keskkond on ette valmistatud) Commerce'i loodud URL-ile.</span><span class="sxs-lookup"><span data-stu-id="45ff3-153">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="45ff3-154">Need URL-id peavad alati kasutama kehtivat URL-vormingut ja need peavad olema ainult alus-URL-id (neile ei järgne kaldkriipse ega teid).</span><span class="sxs-lookup"><span data-stu-id="45ff3-154">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="45ff3-155">Seejärel tuleb lisada string ``/_msdyn365/authresp`` alus-URL-idele, nagu järgnevates näidetes illustreeritud.</span><span class="sxs-lookup"><span data-stu-id="45ff3-155">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- <span data-ttu-id="45ff3-156">``https://www.fabrikam.com/_msdyn365/authresp`` (Domeen peab vastama täielikult e-kaubanduse domeenile.</span><span class="sxs-lookup"><span data-stu-id="45ff3-156">``https://www.fabrikam.com/_msdyn365/authresp`` (The domain should match the e-commerce domain completely.</span></span> <span data-ttu-id="45ff3-157">Kui teil on mitu domeeni, peate selle URL-i lisama igale domeenile.)</span><span class="sxs-lookup"><span data-stu-id="45ff3-157">If you have multiple domains, you need to add this URL for each domain.)</span></span>
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="45ff3-158">Kasutajavoo poliitikate loomine</span><span class="sxs-lookup"><span data-stu-id="45ff3-158">Create user flow policies</span></span>

<span data-ttu-id="45ff3-159">Kasutajavood on poliitikad, mida Azure AD B2C kasutab turvalise sisselogimise, registreerimise, profiili muutmise ja unustatud parooli kasutajakogemuste tagamiseks.</span><span class="sxs-lookup"><span data-stu-id="45ff3-159">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="45ff3-160">Dynamics 365 Commerce kasutab neid voogusid et poliitikaga seonduvate toimingute tegemiseks Azure AD B2C rentnikuga suhtlemisel.</span><span class="sxs-lookup"><span data-stu-id="45ff3-160">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="45ff3-161">Kui kasutaja suhtleb nende poliitikatega, suunatakse ta nende toimingute sooritamiseks Azure AD B2C rentnikku.</span><span class="sxs-lookup"><span data-stu-id="45ff3-161">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="45ff3-162">Azure AD B2C pakub kolme peamist kasutajavoo tüüpi.</span><span class="sxs-lookup"><span data-stu-id="45ff3-162">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="45ff3-163">Registreerimine ja sisselogimine</span><span class="sxs-lookup"><span data-stu-id="45ff3-163">Sign up and sign in</span></span>
- <span data-ttu-id="45ff3-164">Profiili redigeerimine</span><span class="sxs-lookup"><span data-stu-id="45ff3-164">Profile editing</span></span>
- <span data-ttu-id="45ff3-165">Parooli lähtestamine</span><span class="sxs-lookup"><span data-stu-id="45ff3-165">Password reset</span></span>

<span data-ttu-id="45ff3-166">Saate valida, kas soovite kasutada Azure AD pakutavaid vaikimisi kasutajavooge, mis kuvavad AAD B2C poolt hallatavat lehekülge.</span><span class="sxs-lookup"><span data-stu-id="45ff3-166">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="45ff3-167">Saate ka luua HTML-lehe, et juhtida nende kasutajavoo kogemuste välimust ja olemust.</span><span class="sxs-lookup"><span data-stu-id="45ff3-167">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="45ff3-168">Kasutajapoliitika lehtede kohandamiseks Dynamics 365 Commerce'is vaadake teemat [Kohandatud lehtede häälestamine kasutaja sisselogimisteks](custom-pages-user-logins.md).</span><span class="sxs-lookup"><span data-stu-id="45ff3-168">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="45ff3-169">Lisateavet leiate teemast [Azure Active Directory B2C kasutuskogemuse liidese kohandamine](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="45ff3-169">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="45ff3-170">Registreerumise ja sisselogimise kasutajavoo poliitika loomine</span><span class="sxs-lookup"><span data-stu-id="45ff3-170">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="45ff3-171">Registreerimise ja sisselogimise kasutajavoo poliitika loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="45ff3-171">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="45ff3-172">Tehke Azure'i portaali vasakpoolsel navigeerimispaanil valik **Kasutajavood (poliitikad)**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-172">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="45ff3-173">Lehel **Azure AD B2C – kasutajavood (poliitikad)** valige **Uus kasutajavoog**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-173">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="45ff3-174">Vahekaardil **Soovitatav** valige **Registreeru ja logi sisse**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-174">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="45ff3-175">Sisestage poliitika nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-175">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="45ff3-176">See nimi kuvatakse hiljem koos eesliitega, mille portaal määrab (nt „B2C_1_”).</span><span class="sxs-lookup"><span data-stu-id="45ff3-176">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="45ff3-177">Märkige sobiv ruut jaotises **Identiteedipakkujad**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-177">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="45ff3-178">Valige sobiv ettevõtte valik jaotises **Mitmikautentimine**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-178">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="45ff3-179">Jaotises **Kasutaja atribuudid ja nõuded** valige suvandid atribuutide kogumiseks või nõuete tagastamiseks vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="45ff3-179">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="45ff3-180">Commerce nõuab järgmisi vaikesätteid.</span><span class="sxs-lookup"><span data-stu-id="45ff3-180">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="45ff3-181">**Atribuudi kogumine**</span><span class="sxs-lookup"><span data-stu-id="45ff3-181">**Collect  attribute**</span></span> | <span data-ttu-id="45ff3-182">**Nõude tagastamine**</span><span class="sxs-lookup"><span data-stu-id="45ff3-182">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    | <span data-ttu-id="45ff3-183">Meiliaadress</span><span class="sxs-lookup"><span data-stu-id="45ff3-183">Email Address</span></span>          | <span data-ttu-id="45ff3-184">Meiliaadressid</span><span class="sxs-lookup"><span data-stu-id="45ff3-184">Email Addresses</span></span>   |
    | <span data-ttu-id="45ff3-185">Eesnimi</span><span class="sxs-lookup"><span data-stu-id="45ff3-185">Given Name</span></span>             | <span data-ttu-id="45ff3-186">Eesnimi</span><span class="sxs-lookup"><span data-stu-id="45ff3-186">Given Name</span></span>        |
    |                        | <span data-ttu-id="45ff3-187">Identiteedipakkuja</span><span class="sxs-lookup"><span data-stu-id="45ff3-187">Identity Provider</span></span> |
    | <span data-ttu-id="45ff3-188">Perekonnanimi</span><span class="sxs-lookup"><span data-stu-id="45ff3-188">Surname</span></span>                | <span data-ttu-id="45ff3-189">Perekonnanimi</span><span class="sxs-lookup"><span data-stu-id="45ff3-189">Surname</span></span>           |
    |                        | <span data-ttu-id="45ff3-190">Kasutaja objekti ID</span><span class="sxs-lookup"><span data-stu-id="45ff3-190">User’s Object ID</span></span>  |

1. <span data-ttu-id="45ff3-191">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-191">Select **Create**.</span></span>

<span data-ttu-id="45ff3-192">Järgmine pilt on Azure AD B2C registreerumise ja sisselogimise kasutajavoo näide.</span><span class="sxs-lookup"><span data-stu-id="45ff3-192">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![Registreerimise ja sisselogimise poliitika sätted](./media/B2CImage_11.png)

<span data-ttu-id="45ff3-194">Järgmine pilt näitab valikut **Kasutajavoo käitamine** Azure AD B2C registreerumise ja sisselogimise kasutajavoos.</span><span class="sxs-lookup"><span data-stu-id="45ff3-194">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![Kasutajavoo suvandi käitamine poliitika voos](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="45ff3-196">Profiili loomine kasutajavoo poliitika redigeerimisel</span><span class="sxs-lookup"><span data-stu-id="45ff3-196">Create a profile editing user flow policy</span></span>

<span data-ttu-id="45ff3-197">Profiili redigeerimise kasutajavoo poliitika loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="45ff3-197">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="45ff3-198">Tehke Azure'i portaali vasakpoolsel navigeerimispaanil valik **Kasutajavood (poliitikad)**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-198">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="45ff3-199">Lehel **Azure AD B2C – kasutajavood (poliitikad)** valige **Uus kasutajavoog**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-199">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="45ff3-200">Vahekaardil **Soovitatav** valige **Profiili redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-200">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="45ff3-201">Jaotises **Nimi** sisestage profiil kasutajavoogu redigeerides.</span><span class="sxs-lookup"><span data-stu-id="45ff3-201">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="45ff3-202">See nimi kuvatakse hiljem koos eesliitega, mille portaal määrab (nt „B2C_1_”).</span><span class="sxs-lookup"><span data-stu-id="45ff3-202">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="45ff3-203">Valige jaotises **Identiteedipakkujad** suvand **Kohaliku konto sisselogimine**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-203">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="45ff3-204">Jaotises **Kasutaja atribuudid** märkige järgmised ruudud.</span><span class="sxs-lookup"><span data-stu-id="45ff3-204">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="45ff3-205">**Meiliaadress** (ainult **Tagastuse nõue**)</span><span class="sxs-lookup"><span data-stu-id="45ff3-205">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="45ff3-206">**Eesnimi** (**Atribuudi kogumine** ja **Tagastuse nõue**)</span><span class="sxs-lookup"><span data-stu-id="45ff3-206">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="45ff3-207">**Identiteedipakkuja** (ainult **Tagastuse nõue**)</span><span class="sxs-lookup"><span data-stu-id="45ff3-207">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="45ff3-208">**Perekonnanimi** (**Atribuudi kogumine** ja **Tagastuse nõue**)</span><span class="sxs-lookup"><span data-stu-id="45ff3-208">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="45ff3-209">**Kasutaja objekti ID** (ainult **Tagastuse nõue**)</span><span class="sxs-lookup"><span data-stu-id="45ff3-209">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="45ff3-210">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-210">Select **Create**.</span></span>

<span data-ttu-id="45ff3-211">Järgmine pilt on Azure AD B2C profiili redigeerimise kasutajavoo näide.</span><span class="sxs-lookup"><span data-stu-id="45ff3-211">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![Profiili redigeerimise kasutajavoo loomine](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="45ff3-213">Parooli lähtestamise kasutajavoo poliitika loomine</span><span class="sxs-lookup"><span data-stu-id="45ff3-213">Create a password reset user flow policy</span></span>

<span data-ttu-id="45ff3-214">Parooli lähtestamiseks kasutajavoo poliitikas toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="45ff3-214">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="45ff3-215">Tehke Azure'i portaali vasakpoolsel navigeerimispaanil valik **Kasutajavood (poliitikad)**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-215">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="45ff3-216">Lehel **Azure AD B2C – kasutajavood (poliitikad)** valige **Uus kasutajavoog**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-216">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="45ff3-217">Vahekaardil **Soovitatav** valige **Parooli lähtestamine**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-217">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="45ff3-218">Jaotises **Nimi** sisestage parooli lähtestamise kasutajavoo nimi.</span><span class="sxs-lookup"><span data-stu-id="45ff3-218">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="45ff3-219">Jaotises **Identiteedipakkujad** valige suvand **Parooli lähtestamine meiliaadressi kasutades**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-219">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="45ff3-220">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-220">Select **Create**.</span></span>
1. <span data-ttu-id="45ff3-221">Jaotises **Rakenduse nõuded** märkige järgmised ruudud.</span><span class="sxs-lookup"><span data-stu-id="45ff3-221">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="45ff3-222">**Meiliaadressid**</span><span class="sxs-lookup"><span data-stu-id="45ff3-222">**Email addresses**</span></span>
    - <span data-ttu-id="45ff3-223">**Eesnimi**</span><span class="sxs-lookup"><span data-stu-id="45ff3-223">**Given Name**</span></span>
    - <span data-ttu-id="45ff3-224">**Perekonnanimi**</span><span class="sxs-lookup"><span data-stu-id="45ff3-224">**Surname**</span></span>
    - <span data-ttu-id="45ff3-225">**Kasutaja objekti ID**</span><span class="sxs-lookup"><span data-stu-id="45ff3-225">**User's Object ID**</span></span>
1. <span data-ttu-id="45ff3-226">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-226">Select **Create**.</span></span>

<span data-ttu-id="45ff3-227">Järgmisel pildil näidatakse, kuhu seada **Lähtesta parool meiliaadressi abil** Azure AD B2C parooli lähtestamise kasutajavoos.</span><span class="sxs-lookup"><span data-stu-id="45ff3-227">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![„Lähtesta parool meiliaadressi abil” sätestamine parooli lähtestamise poliitikas](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="45ff3-229">Sotsiaalstete identiteedipakkujate lisamine (valikuline)</span><span class="sxs-lookup"><span data-stu-id="45ff3-229">Add social identity providers (Optional)</span></span>

<span data-ttu-id="45ff3-230">Sotsiaalsed identiteedipakkujad lubavad kasutajatel autentimiseks sotsiaalmeedia kontosid kasutada.</span><span class="sxs-lookup"><span data-stu-id="45ff3-230">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="45ff3-231">Sotsiaalse identiteedipakkuja autentimise lisamine on Dynamics 365 Commerce'i rakenduses valikuline.</span><span class="sxs-lookup"><span data-stu-id="45ff3-231">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="45ff3-232">Kui sotsiaalse identiteedipakkuja autentimist ei lisata, on Azure AD B2C vaikeprofiilid teie kasutajate põhilised profiilid.</span><span class="sxs-lookup"><span data-stu-id="45ff3-232">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="45ff3-233">Kasutajad valivad oma kasutajanime (eelistatud meiliaadressi) ja määravad parooli.</span><span class="sxs-lookup"><span data-stu-id="45ff3-233">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="45ff3-234">Azure AD B2C autendib kasutajaid otse.</span><span class="sxs-lookup"><span data-stu-id="45ff3-234">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="45ff3-235">Kui on sotsiaalse identiteedipakkuja autentimine lisatakse ja kasutaja valib ühe pakutava sotsiaalse identiteedipakkuja, luuakse ikkagi üksus Azure AD B2C rentniku jaoks.</span><span class="sxs-lookup"><span data-stu-id="45ff3-235">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="45ff3-236">Azure AD B2C autendib seejärel kasutaja mandaadi sotsiaalse identiteedipakkuja juures.</span><span class="sxs-lookup"><span data-stu-id="45ff3-236">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="45ff3-237">Identiteedipakkujaga sisselogimine loob kirje B2C rentnikku, kuidkohalikest kontodest erinevas vormingus, kuna see nõuab autentimiseks välise sotsiaalse identiteedipakkuja viidet.</span><span class="sxs-lookup"><span data-stu-id="45ff3-237">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="45ff3-238">Kasutaja saab kasutada sama meiliaadressi kõigis sotsiaalsetes identiteedipakkujates, mis tähendab, et autentimiseks kasutatav meili kasutajanimi ei pruugi olla rentniku jaoks kordumatu.</span><span class="sxs-lookup"><span data-stu-id="45ff3-238">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="45ff3-239">Azure AD B2C nõuab kasutajatelt on kordumatu meiliaadress kasutamist kohalikel B2C kontodel.</span><span class="sxs-lookup"><span data-stu-id="45ff3-239">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="45ff3-240">Enne autentimiseks sotsiaalse identiteedipakkuja lisamist, peate pöörduma identiteedipakkuja portaali poole ja häälestama identiteedipakkuja rakenduse Azure AD B2C dokumentatsioonis kirjeldatud juhiste järgi.</span><span class="sxs-lookup"><span data-stu-id="45ff3-240">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="45ff3-241">Allpool on esitatud linkide loend dokumentidele juurde pääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="45ff3-241">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="45ff3-242">Amazon</span><span class="sxs-lookup"><span data-stu-id="45ff3-242">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="45ff3-243">Azure AD (Üksik rentnik)</span><span class="sxs-lookup"><span data-stu-id="45ff3-243">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="45ff3-244">Microsofti konto</span><span class="sxs-lookup"><span data-stu-id="45ff3-244">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="45ff3-245">Facebook</span><span class="sxs-lookup"><span data-stu-id="45ff3-245">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="45ff3-246">GitHub</span><span class="sxs-lookup"><span data-stu-id="45ff3-246">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="45ff3-247">Google</span><span class="sxs-lookup"><span data-stu-id="45ff3-247">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="45ff3-248">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="45ff3-248">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="45ff3-249">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="45ff3-249">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="45ff3-250">Twitter</span><span class="sxs-lookup"><span data-stu-id="45ff3-250">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="45ff3-251">Sotsiaalse identiteedipakkuja lisamine ja seadistamine</span><span class="sxs-lookup"><span data-stu-id="45ff3-251">Add and set up a social identity provider</span></span>

<span data-ttu-id="45ff3-252">Sotsiaalse identiteedipakkuja lisamiseks ja seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="45ff3-252">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="45ff3-253">Azure'i portaalis liikuge jaotisesse **Identiteedipakkujad**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-253">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="45ff3-254">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-254">Select **Add**.</span></span> <span data-ttu-id="45ff3-255">Kuvatakse aken **Identiteedipakkuja lisamine**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-255">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="45ff3-256">Jaotises **Nimi** sisestage kasutajatele kuvatav nimi teie sisselogimisaknas.</span><span class="sxs-lookup"><span data-stu-id="45ff3-256">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="45ff3-257">Valige jaotises **Identiteedipakkuja tüüp** loendist identiteedipakkuja.</span><span class="sxs-lookup"><span data-stu-id="45ff3-257">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="45ff3-258">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-258">Select **OK**.</span></span>
1. <span data-ttu-id="45ff3-259">Valige **Selle identiteedipakkuja häälestamine** aknale **Sotsiaalse identiteedipakkuja häälestamine** juurde pääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="45ff3-259">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="45ff3-260">Jaotises **Kliendi ID** sisestage kliendi ID, mille saite identiteedipakkuja rakenduse häälestamisel.</span><span class="sxs-lookup"><span data-stu-id="45ff3-260">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="45ff3-261">Jaotises **Kliendi saladus** sisestage kliendi saladus, mille saite identiteedipakkuja rakenduse häälestamisel.</span><span class="sxs-lookup"><span data-stu-id="45ff3-261">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="45ff3-262">Kasutajavoo lisamine sisselogimise registreerumise poliitika jaoks.</span><span class="sxs-lookup"><span data-stu-id="45ff3-262">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="45ff3-263">Avage jaotis **Azure AD B2C – kasutajavood (poliitikad) \> {teie sisselogimise registreerumise poliitika} \> Identiteedipakkujad**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-263">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="45ff3-264">Sisselogimise/registreerumise kasutajavoo poliitika manustamiseks valige kõik identiteedipakkujad, mille olete oma kontole seadistanud.</span><span class="sxs-lookup"><span data-stu-id="45ff3-264">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="45ff3-265">Nende testimiseks valige käsk **Kasutajavoo käitamine** igale identiteedipakkujale.</span><span class="sxs-lookup"><span data-stu-id="45ff3-265">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="45ff3-266">Uus vahekaart kuvab sisselogimisakna, kus kuvatakse uus identiteedipakkuja valikuväli.</span><span class="sxs-lookup"><span data-stu-id="45ff3-266">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="45ff3-267">Järgmisel pildil kuvatakse näited akende **Identiteedipakkuja lisamine** ja **Sotsiaalse identiteedipakkuja häälestamine** kohta Azure AD B2C-s.</span><span class="sxs-lookup"><span data-stu-id="45ff3-267">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![Sotsiaalse identiteedipakkuja lisamine rakendusse](./media/B2CImage_14.png)

<span data-ttu-id="45ff3-269">Järgmisel pildil kuvatakse näide, kuidas valida identiteedipakkujaid Azure AD B2C lehel **Identiteedipakkujad**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-269">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![Valige kõik enda poliitika jaoks lubatavad sotsiaalse identiteedipakkujad](./media/B2CImage_16.png)

<span data-ttu-id="45ff3-271">Järgmisel pildil kuvatakse näide vaikimisi sisselogimisaken, millel on sotsiaalse identiteedipakkuja sisselogimisnupp.</span><span class="sxs-lookup"><span data-stu-id="45ff3-271">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![Näide vaikimisi sisselogimisaknast sotsiaalse identiteedipakkuja sisselogimisnupuga](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="45ff3-273">Commerce'i peakontori värskendamine uue Azure AD B2C teabega</span><span class="sxs-lookup"><span data-stu-id="45ff3-273">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="45ff3-274">Kui eelpool loetletud Azure AD B2C ettevalmistavad etapid on lõpule viidud, peab Azure AD B2C rakendus olema registreeritud teie Dynamics 365 Commerce'i keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="45ff3-274">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="45ff3-275">Peakontori väsrkendamiseks uue Azure AD B2C teabega toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="45ff3-275">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="45ff3-276">Avage Commerce'i jaotis **Commerce'i jagatud parameetrid** ja valige vasakpoolsest menüüst **Identiteedipakkujad**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-276">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="45ff3-277">Jaotises **Identiteedipakkujad** toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="45ff3-277">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="45ff3-278">Sisestage identiteedipakkuja väljaandja URL lahtrisse **Väljaandja**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-278">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="45ff3-279">Oma väljaandja URL-i saamiseks avage teema [Väljaandja URL-i hankimine](#obtain-issuer-url).</span><span class="sxs-lookup"><span data-stu-id="45ff3-279">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="45ff3-280">Sisestageoma väljaandja kirje nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-280">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="45ff3-281">Väljale **Tüüp** sisestage **Azure AD B2C (id_token)**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-281">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="45ff3-282">Jaotises **Sõltuvad osapooled**, kui eelpool mainitud B2C identiteedipakkuja üksus on valitud, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="45ff3-282">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="45ff3-283">Sisestage oma B2C rakenduse ID väljale **ClientID**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-283">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="45ff3-284">Leiate selle oma B2C rakenduse atribuutide lehe väljalt **Rakenduse ID**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-284">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="45ff3-285">Väljale **Tüüp** sisestage **Avalik**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-285">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="45ff3-286">Väljale **Kasutajatüüp** sisestage **Klient**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-286">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="45ff3-287">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-287">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="45ff3-288">Sisestage Commerce'i otsingulahtrisse **Jaotusegraafik**</span><span class="sxs-lookup"><span data-stu-id="45ff3-288">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="45ff3-289">Lehe **Jaotusegraafik** vasakpoolses navigeerimismenüüs valige töö **1110 globaalne konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-289">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="45ff3-290">Valige toimingupaanil käsk **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-290">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="45ff3-291">Väljaandja URL-i hankimine</span><span class="sxs-lookup"><span data-stu-id="45ff3-291">Obtain issuer URL</span></span>

<span data-ttu-id="45ff3-292">Oma identiteedipakkuja väljaandja URL-i hankimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="45ff3-292">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="45ff3-293">Looge metaandmete aadressi URL järgmises vormingus, kasutades oma B2C rentnikku ja poliitikat: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="45ff3-293">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="45ff3-294">Näide: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="45ff3-294">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="45ff3-295">Sisestage metaandmete aadressi URL brauseri aadressiribale.</span><span class="sxs-lookup"><span data-stu-id="45ff3-295">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="45ff3-296">Kopeerige metaandmetest identiteedipakkuja väljaandja URL (väärtus **„väljaandja”**).</span><span class="sxs-lookup"><span data-stu-id="45ff3-296">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="45ff3-297">Näide: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="45ff3-297">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="45ff3-298">B2C rentniku konfigureerimine kaubanduse saidiehitajas</span><span class="sxs-lookup"><span data-stu-id="45ff3-298">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="45ff3-299">Kui teie Azure AD B2C rentniku häälestus on lõpule viidud, tuleb konfigureerida B2C rentnik kaubanduse saidiehitajas.</span><span class="sxs-lookup"><span data-stu-id="45ff3-299">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="45ff3-300">Konfiguratsioonietapid hõlmavad B2C rakenduse teabe kogumist Azure'i portaalist, selle B2C rakenduse teabe sisestamist saidiehitajasse ja seejärel B2C rakenduse seostamist teie saidi ja kanaliga.</span><span class="sxs-lookup"><span data-stu-id="45ff3-300">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="45ff3-301">Nõutava rakenduseteabe kogumine</span><span class="sxs-lookup"><span data-stu-id="45ff3-301">Collect the required application information</span></span>

<span data-ttu-id="45ff3-302">Nõutava rakenduseteabe kogumiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="45ff3-302">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="45ff3-303">Avage Azure'i portaalis jaotis **Avaleht \> Azure AD B2C - rakendused**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-303">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="45ff3-304">Valige oma rakendus ja seejärel valige valige vasakpoolsel navigeerimispaanil **Atribuudid** rakenduse üksikasjade hankimiseks.</span><span class="sxs-lookup"><span data-stu-id="45ff3-304">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="45ff3-305">Väljalt **Rakenduse ID** hankige rakenduse ID oma B2C rentnikus loodud B2C rakendusest.</span><span class="sxs-lookup"><span data-stu-id="45ff3-305">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="45ff3-306">See sisestatakse hiljem saidiehitajas väärtuseks **Kliendi GUID**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-306">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="45ff3-307">Hankige vastuse URL jaotisest **Vastuse URL**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-307">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="45ff3-308">Avage jaotis **Avaleht \> Azure AD B2C – kasutajavood (poliitikad)** ja seejärel hankige kõigi kasutajavoo poliitikate nimed.</span><span class="sxs-lookup"><span data-stu-id="45ff3-308">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="45ff3-309">Järgmisel pildil kuvatakse näide lehest **Azure AD B2C – rakendused**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-309">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![Oma rentnikus B2C rakendusse liikumine](./media/B2CImage_19.png)

<span data-ttu-id="45ff3-311">Järgmisel pildil kuvatakse näide rakenduse lehest **Atribuudid** Azure AD B2C-s.</span><span class="sxs-lookup"><span data-stu-id="45ff3-311">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![Rakenduse ID kopeerimine B2C rakenduse atribuutidest](./media/B2CImage_21.png)

<span data-ttu-id="45ff3-313">Järgmisel pildil kuvatakse näide kasutajavoo poliitikatest lehel **Azure AD B2C – kasutajavood (poliitikad)**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-313">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![Kõigi B2C poliitikavoo nimede kogumine](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="45ff3-315">Oma AAD B2C üürniku rakenduse teabe sisestamine Commerce'i</span><span class="sxs-lookup"><span data-stu-id="45ff3-315">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="45ff3-316">Enne B2C rentniku seostamist oma saitidega, peate sisestama Azure AD B2C rentniku andmed kaubanduse saidiehitajasse.</span><span class="sxs-lookup"><span data-stu-id="45ff3-316">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="45ff3-317">AAD B2C rentniku rakenduse teabe lisamiseks Commerce'i toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="45ff3-317">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="45ff3-318">Logige sisse administraatorina oma keskkonna kaubanduse saidiehitajasse.</span><span class="sxs-lookup"><span data-stu-id="45ff3-318">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="45ff3-319">Vasakpoolsel navigeerimispaanil valige suvand **Rentniku sätted** selle laiendamiseks.</span><span class="sxs-lookup"><span data-stu-id="45ff3-319">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="45ff3-320">Jaotises **Rentniku sätted** valige suvand **B2C sätted**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-320">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="45ff3-321">Valige põhiaknas **B2C rakendused** kõrvalt jaotis **Halda**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-321">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="45ff3-322">(Kui teie rentnik kuvatakse B2C rakenduste loendis, siis on administraator selle juba lisanud.</span><span class="sxs-lookup"><span data-stu-id="45ff3-322">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="45ff3-323">Veenduge, et etapis 6 olevad üksused vastaksid teie B2C rakendusele.)</span><span class="sxs-lookup"><span data-stu-id="45ff3-323">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="45ff3-324">Valige **Lisa B2C rakendus**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-324">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="45ff3-325">Sisestage järgmised nõutavad üksused kuvatud vormile, kasutades oma B2C rentniku ja rakenduse väärtusi.</span><span class="sxs-lookup"><span data-stu-id="45ff3-325">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="45ff3-326">Väljad, mis ei ole kohustuslikud (ilma tärnita), võivad jääda tühjaks.</span><span class="sxs-lookup"><span data-stu-id="45ff3-326">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="45ff3-327">**Rakenduse nimi**: teie B2C rakenduse nimi, näiteks „Fabrikam B2C”.</span><span class="sxs-lookup"><span data-stu-id="45ff3-327">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="45ff3-328">**Rentniku nimi**: teie B2C rentniku nimi (nt „fabrikam“, kui domeen kuvatakse B2C rentnikule kui „fabrikam.onmicrosoft.com“).</span><span class="sxs-lookup"><span data-stu-id="45ff3-328">**Tenant Name**: The name of your B2C tenant (for example, use "fabrikam" if the domain appears as "fabrikam.onmicrosoft.com" for the B2C tenant).</span></span> 
    - <span data-ttu-id="45ff3-329">**Poliitika ID parooli unustamise korral**: kasutajavoo poliitika ID parooli unustamise korral, näiteks „B2C_1_PasswordReset”.</span><span class="sxs-lookup"><span data-stu-id="45ff3-329">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="45ff3-330">**Registreerumise sisselogimise poliitika ID**: kasutajavoo poliitika ID registreerumiseks ja sisselogimiseks, näiteks „B2C_1_signup_signin”.</span><span class="sxs-lookup"><span data-stu-id="45ff3-330">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="45ff3-331">**Kliendi GUID**: B2C rakenduse ID, näiteks „22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6”.</span><span class="sxs-lookup"><span data-stu-id="45ff3-331">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="45ff3-332">**Profiilipoliitika ID redigeerimine**: kasutajavoo poliitika ID profiili redigeerimiseks, näiteks „B2C_1A_ProfileEdit”.</span><span class="sxs-lookup"><span data-stu-id="45ff3-332">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="45ff3-333">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-333">Select **OK**.</span></span> <span data-ttu-id="45ff3-334">Nüüd peaks olema teie B2C rakenduse nimi loendis kuvatud.</span><span class="sxs-lookup"><span data-stu-id="45ff3-334">You should now see the name of your B2C application appear in the list.</span></span>
1. <span data-ttu-id="45ff3-335">Oma muudatuste salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-335">Select **Save** to save your changes.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="45ff3-336">B2C rakenduse seostamine teie saidi ja kanaliga</span><span class="sxs-lookup"><span data-stu-id="45ff3-336">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="45ff3-337">Kui teie sait on juba seostatud B2C rakendusega, siis teise B2C rakendusse üleminekul eemaldatakse praegused juba sellesse keskkonda registreerunud kasutajatele loodud viited.</span><span class="sxs-lookup"><span data-stu-id="45ff3-337">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="45ff3-338">Kui seda muudetakse, ei ole kasutajatele saadaval ükski praegu määratud B2C rakendusega seotud mandaat.</span><span class="sxs-lookup"><span data-stu-id="45ff3-338">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="45ff3-339">Uuendage B2C rakendust ainult siis, kui seadistate kanali B2C rakendust esimest korda või kui soovite, et kasutajad registreeriksid selle kanali uue B2C rakendusega oma mandaadid uuesti.</span><span class="sxs-lookup"><span data-stu-id="45ff3-339">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="45ff3-340">Olge ettevaatlik kanalite seostamisel B2C rakendustega ja nimetage rakendusi selgelt.</span><span class="sxs-lookup"><span data-stu-id="45ff3-340">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="45ff3-341">Kui kanal ei ole seostatud B2C rakendusega alljärgnevate etappidega, on sisestatakse kasutajad teie saidi kanalisse siselogimisel B2C rakendusse olekuga **vaikimisi** B2C rakenduste loendis **Rentniku sätted \> B2C sätted**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-341">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="45ff3-342">B2C rakenduse seostamiseks teie saidi ja kanaliga toimige järgnevalt.</span><span class="sxs-lookup"><span data-stu-id="45ff3-342">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="45ff3-343">Liikuge oma saidile kaubanduse saidiehitajas.</span><span class="sxs-lookup"><span data-stu-id="45ff3-343">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="45ff3-344">Vasakpoolsel navigeerimispaanil valige suvand **Saidi sätted** selle laiendamiseks.</span><span class="sxs-lookup"><span data-stu-id="45ff3-344">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="45ff3-345">Jaotises **Saidi sätted**valige **Kanalid**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-345">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="45ff3-346">Valige oma kanal põhiakna jaotises **Kanalid**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-346">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="45ff3-347">Parempoolsel kanali atribuutide paanil valige oma B2C rakenduse nimi rippmenüüst **B2C rakenduse valimine**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-347">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="45ff3-348">Valige **Sule** ja seejärel valige **Salvesta ja avalda**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-348">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="45ff3-349">Lisateave B2C kohta</span><span class="sxs-lookup"><span data-stu-id="45ff3-349">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="45ff3-350">Kliendi migreerimine</span><span class="sxs-lookup"><span data-stu-id="45ff3-350">Customer migration</span></span>

<span data-ttu-id="45ff3-351">Kui soovite migreerida kliendikirjeid eelmisest identiteedipakkuja platvormist, siis tehke koostööd Dynamics 365 Commerce meeskonnaga oma klientide migratsiooni vajaduste ülevaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="45ff3-351">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="45ff3-352">Täiendava Azure AD B2C dokumentatsiooni hankimiseks klientide migratsiooni kohta vaadake teemat [Kasutajate migreerimine Azure Active Directory B2C-sse](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span><span class="sxs-lookup"><span data-stu-id="45ff3-352">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="45ff3-353">Kohandatud poliitikad</span><span class="sxs-lookup"><span data-stu-id="45ff3-353">Custom policies</span></span>

<span data-ttu-id="45ff3-354">Täiendava teabe saamiseks Azure AD B2C suhtlus- ja poliitikavoogude kohandamise kohta, mis ei kuulu B2C standardpoliitikasse, vaadake teemat [Kohandatud poliitikad Azure Active Directory B2C-s](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="45ff3-354">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="45ff3-355">Teisene administraator</span><span class="sxs-lookup"><span data-stu-id="45ff3-355">Secondary admin</span></span>

<span data-ttu-id="45ff3-356">Teie B2C rentnikku on valikuliselt võimalik lisada teisene administraatorikonto jaotises **Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="45ff3-356">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="45ff3-357">See võib olla otsene või üldine konto.</span><span class="sxs-lookup"><span data-stu-id="45ff3-357">This can be a direct account or a general account.</span></span> <span data-ttu-id="45ff3-358">Kui teil on vaja jagada kontot meeskonnaressursside üleselt, saate luua ka ühise konto.</span><span class="sxs-lookup"><span data-stu-id="45ff3-358">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="45ff3-359">Azure AD B2C-s talletatavate andmete tundlikkuse tõttu tuleb ühist kontot hoolikalt jälgida vastavalt teie ettevõtte turvalisuse tavadele.</span><span class="sxs-lookup"><span data-stu-id="45ff3-359">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45ff3-360">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="45ff3-360">Additional resources</span></span>

[<span data-ttu-id="45ff3-361">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="45ff3-361">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="45ff3-362">Uue e-kaubanduse saidi juurutamine</span><span class="sxs-lookup"><span data-stu-id="45ff3-362">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="45ff3-363">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="45ff3-363">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="45ff3-364">Veebisaidi seostamine kanaliga</span><span class="sxs-lookup"><span data-stu-id="45ff3-364">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="45ff3-365">robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="45ff3-365">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="45ff3-366">URL-i hulgiümbersuunamiste üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="45ff3-366">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="45ff3-367">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="45ff3-367">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="45ff3-368">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="45ff3-368">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="45ff3-369">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="45ff3-369">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="45ff3-370">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="45ff3-370">Enable location-based store detection</span></span>](enable-store-detection.md)
