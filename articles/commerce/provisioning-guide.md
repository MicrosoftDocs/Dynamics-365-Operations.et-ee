---
title: Commerce’i eelvaatekeskkonna ettevalmistamine
description: Selles teemas selgitatakse, kuidas valmistada ette Microsoft Dynamics 365 Commerce’i eelvaatekeskkond.
author: psimolin
manager: annbe
ms.date: 01/06/2020
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
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934744"
---
# <a name="provision-a-commerce-preview-environment"></a><span data-ttu-id="441ef-103">Commerce’i eelvaatekeskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="441ef-103">Provision a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="441ef-104">Selles teemas selgitatakse, kuidas valmistada ette Microsoft Dynamics 365 Commerce’i eelvaatekeskkond.</span><span class="sxs-lookup"><span data-stu-id="441ef-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="441ef-105">Enne alustamist soovitame teil kogu see teema vähemalt läbi sirvida, et saada aimu, mida protsess hõlmab ja mida see teema sisaldab.</span><span class="sxs-lookup"><span data-stu-id="441ef-105">Before you begin, we recommend that you at least skim through this whole topic to get an idea of what the process entails and what this topic contains.</span></span>

> [!NOTE]
> <span data-ttu-id="441ef-106">Kui te pole veel andnud juurdepääsu rakenduse Dynamics 365 Commerce eelvaatele, saate taotleda eelvaate juurdepääsu [Commerce’i veebisaidilt](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="441ef-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="441ef-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="441ef-107">Overview</span></span>

<span data-ttu-id="441ef-108">Oma Commerce’i eelvaatekeskkonna edukaks ettevalmistamiseks peate looma projekti, millel on kindel toote nimi ja tüüp.</span><span class="sxs-lookup"><span data-stu-id="441ef-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="441ef-109">Keskkonnal ja teenusel Retail Cloud Scale Unit (RCSU) on samuti mõned konkreetsed parameetrid, mida peate kasutama, kui hiljem e-kaubandust ette valmistate.</span><span class="sxs-lookup"><span data-stu-id="441ef-109">The environment and Retail Cloud Scale Unit (RCSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="441ef-110">Selle teema juhised kirjeldavad kõiki vajalikke etappe, mida peate täitma ja millised parameetreid peate kasutada.</span><span class="sxs-lookup"><span data-stu-id="441ef-110">The instructions in this topic describe all the required steps that you must complete and the parameters that you must use.</span></span>

<span data-ttu-id="441ef-111">Pärast seda, kui olete oma Commerce’i eelvaatekeskkonna edukat ette valmistanud, peate läbima ettevalmistamiseks mõned hilisemad etapid.</span><span class="sxs-lookup"><span data-stu-id="441ef-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="441ef-112">Mõned etapid on valikulised, olenevalt sellest, milliseid süsteemi aspekte soovite hinnata.</span><span class="sxs-lookup"><span data-stu-id="441ef-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="441ef-113">Võite valikulised etapid alati hiljem läbida.</span><span class="sxs-lookup"><span data-stu-id="441ef-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="441ef-114">Teavet selle kohta, kuidas Commerce’i eelvaatekeskkonda pärast ettevalmistamist konfigureerida, vaadake teemast [Commerce’i eelvaatekeskkonna konfigureerimine](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="441ef-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="441ef-115">Teavet selle kohta, kuidas Commerce’i eelvaatekeskkonna valikulisi funktsioone konfigureerida, vaadake teemast [Commerce’i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="441ef-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="441ef-116">Kui teil on küsimusi ettevalmistamise etappide kohta või esineb probleeme, andke Microsoftile sellest teada [rakenduse Microsoft Dynamics 365 Commerce eelvaate Yammeri grupis](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="441ef-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="441ef-117">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="441ef-117">Prerequisites</span></span>

<span data-ttu-id="441ef-118">Enne Commerce’i eelvaatekeskkonna ettevalmistamist peavad olema kehtestatud järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="441ef-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="441ef-119">Teil on juurdepääs Microsoft Dynamicsi portaalile Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="441ef-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="441ef-120">Teid on rakenduse Dynamics 365 Commerce eelvaate programmi vastu võetud.</span><span class="sxs-lookup"><span data-stu-id="441ef-120">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="441ef-121">Teil on vajalikud õigused, et luua projekt suvandile **Potentsiaalsed eelmüügid** või **Migreerimine, lahenduste loomine ja teave**.</span><span class="sxs-lookup"><span data-stu-id="441ef-121">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="441ef-122">Olete rolli **Keskkonnahaldur** või **Projekti omanik** liige projektis, kus te keskkonna ette valmistate.</span><span class="sxs-lookup"><span data-stu-id="441ef-122">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="441ef-123">Teil on administraatori juurdepääs oma Microsoft Azure’i tellimusele või olete ühenduses tellimise administraatoriga, kes saab teie nimel lõpetada kaks etappi, mis nõuavad administraatori õigusi.</span><span class="sxs-lookup"><span data-stu-id="441ef-123">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="441ef-124">Teie Azure Active Directory (Azure AD) rentniku ID on saadaval.</span><span class="sxs-lookup"><span data-stu-id="441ef-124">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="441ef-125">Olete loonud Azure AD turberühma, mida saab kasutada e-kaubanduse süsteemiadministraatorite grupina ja mille ID on saadaval.</span><span class="sxs-lookup"><span data-stu-id="441ef-125">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="441ef-126">Olete loonud Azure AD turberühma, mida saab kasutada hinnangute ja arvustuste moderaatori grupina ja mille ID on saadaval.</span><span class="sxs-lookup"><span data-stu-id="441ef-126">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="441ef-127">(See turberühm võib olla sama, mis e-kaubanduse süsteemiadministraatorite grupp.)</span><span class="sxs-lookup"><span data-stu-id="441ef-127">(This security group can be the same as the e-Commerce system admin group.)</span></span>

### <a name="find-your-azure-ad-tenant-id"></a><span data-ttu-id="441ef-128">Oma Azure AD rentniku ID leidmine</span><span class="sxs-lookup"><span data-stu-id="441ef-128">Find your Azure AD tenant ID</span></span>

<span data-ttu-id="441ef-129">Teie Azure AD rentniku ID on globaalne ainuidentifikaator (GUID), mis meenutab järgmist näidet **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span><span class="sxs-lookup"><span data-stu-id="441ef-129">Your Azure AD tenant ID is a globally unique identifier (GUID) that resembles this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a><span data-ttu-id="441ef-130">Oma Azure AD rentniku ID leidmine Azure’i portaali kasutades</span><span class="sxs-lookup"><span data-stu-id="441ef-130">Find your Azure AD tenant ID by using the Azure portal</span></span>

1. <span data-ttu-id="441ef-131">Logige sisse [Azure’i portaali](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="441ef-131">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="441ef-132">Veenduge, et valitud oleks õige kataloog.</span><span class="sxs-lookup"><span data-stu-id="441ef-132">Make sure that the correct directory is selected.</span></span>
1. <span data-ttu-id="441ef-133">Valige vasakpoolses menüüs **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="441ef-133">On the menu on the left, select **Azure Active Directory**.</span></span>
1. <span data-ttu-id="441ef-134">Jaotises **Haldus** valige **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="441ef-134">Under **Manage**, select **Properties**.</span></span> <span data-ttu-id="441ef-135">Teie Azure AD rentniku ID kuvatakse jaotises **Kausta ID**.</span><span class="sxs-lookup"><span data-stu-id="441ef-135">Your Azure AD tenant ID appears under **Directory ID**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a><span data-ttu-id="441ef-136">Oma Azure AD rentniku ID leidmine OpenID ühenduse metaandmeid kasutades</span><span class="sxs-lookup"><span data-stu-id="441ef-136">Find your Azure AD tenant ID by using OpenID Connect metadata</span></span>

<span data-ttu-id="441ef-137">Looge OpenID URL, asendades **\{YOUR\_DOMAIN\}** oma domeeniga, nagu `microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="441ef-137">Create an OpenID URL by replacing **\{YOUR\_DOMAIN\}** with your domain, such as `microsoft.com`.</span></span> <span data-ttu-id="441ef-138">Näiteks `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` saab olema `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span><span class="sxs-lookup"><span data-stu-id="441ef-138">For example, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` will become `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span></span>

1. <span data-ttu-id="441ef-139">Avage OpenID URL, mis sisaldab teie domeeni.</span><span class="sxs-lookup"><span data-stu-id="441ef-139">Go to the OpenID URL that contains your domain.</span></span>

    <span data-ttu-id="441ef-140">Võite oma Azure AD rentniku ID leida mitme atribuudi väärtuses.</span><span class="sxs-lookup"><span data-stu-id="441ef-140">You can find you Azure AD tenant ID in multiple property values.</span></span>

1. <span data-ttu-id="441ef-141">Leidke **authorization\_endpoint** ja ekstraktige ilmuv GUID otse pärast `login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="441ef-141">Find **authorization\_endpoint**, and extract the GUID that appears immediately after `login.microsoftonline.com/`.</span></span>

### <a name="find-your-azure-ad-security-group-id"></a><span data-ttu-id="441ef-142">Oma Azure AD turberühma ID leidmine</span><span class="sxs-lookup"><span data-stu-id="441ef-142">Find your Azure AD security group ID</span></span>

<span data-ttu-id="441ef-143">Teie Azure AD turberühma ID on GUID, mis meenutab järgmist näidet **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span><span class="sxs-lookup"><span data-stu-id="441ef-143">The ID of your Azure AD security group is a GUID that resembles this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span></span>

<span data-ttu-id="441ef-144">See protseduur eeldab, et olete grupi liige, mille jaoks soovite ID-d leida.</span><span class="sxs-lookup"><span data-stu-id="441ef-144">This procedure assumes that you're a member of the group that you're trying to find the ID for.</span></span>

1. <span data-ttu-id="441ef-145">Avage [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span><span class="sxs-lookup"><span data-stu-id="441ef-145">Open the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span></span>
1. <span data-ttu-id="441ef-146">Valige suvand **Logi sisse Microsoftiga** ja logige oma identimisteavet kasutades sisse.</span><span class="sxs-lookup"><span data-stu-id="441ef-146">Select **Sign In with Microsoft**, and sign in by using your credentials.</span></span>
1. <span data-ttu-id="441ef-147">Vasakul valige suvand **Kuva rohkem näiteid**.</span><span class="sxs-lookup"><span data-stu-id="441ef-147">On the left, select **show more samples**.</span></span>
1. <span data-ttu-id="441ef-148">Lubage parempoolsel paanil valik **Grupid**.</span><span class="sxs-lookup"><span data-stu-id="441ef-148">In the right pane, enable **Groups**.</span></span>
1. <span data-ttu-id="441ef-149">Sulgege õige paan.</span><span class="sxs-lookup"><span data-stu-id="441ef-149">Close the right pane.</span></span>
1. <span data-ttu-id="441ef-150">Valige suvand **Kõik grupid, kuhu kuulun**.</span><span class="sxs-lookup"><span data-stu-id="441ef-150">Select **all groups I belong to**.</span></span>
1. <span data-ttu-id="441ef-151">Leidke väljal **Vastuse eelvaade** oma grupp.</span><span class="sxs-lookup"><span data-stu-id="441ef-151">In the **Response Preview** field, find your group.</span></span> <span data-ttu-id="441ef-152">Atribuudi ID all kuvatakse turberühma **id**.</span><span class="sxs-lookup"><span data-stu-id="441ef-152">The security group ID appears under the **id** property.</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="441ef-153">Oma Commerce’i eelvaatekeskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="441ef-153">Provision your Commerce preview environment</span></span>

<span data-ttu-id="441ef-154">Need protseduurid selgitavad, kuidas valmistada ette Commerce’i eelvaatekeskkonda.</span><span class="sxs-lookup"><span data-stu-id="441ef-154">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="441ef-155">Pärast nende edukat lõpetamist on Commerce’i eelvaatekeskkond konfigureerimiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="441ef-155">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="441ef-156">Kõik siin kirjeldatud tegevused esinevad LCS portaalis.</span><span class="sxs-lookup"><span data-stu-id="441ef-156">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="441ef-157">Eelvaate juurdepääs on seotud LCS konto ja organisatsiooniga, mille määrasite oma eelvaate rakenduses.</span><span class="sxs-lookup"><span data-stu-id="441ef-157">Preview access is tied to the LCS account and organization that you specified in your preview application.</span></span> <span data-ttu-id="441ef-158">Peate kasutama Commerce’i eelvaatekeskkonna ettevalmistamiseks sama kontot.</span><span class="sxs-lookup"><span data-stu-id="441ef-158">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="441ef-159">Kui peate kasutama Commerce’i eelvaatekeskkonna jaoks erinevat LCS kontot või rentnikku, peate teavitama Microsofti nendest üksikasjadest.</span><span class="sxs-lookup"><span data-stu-id="441ef-159">If you must use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="441ef-160">Kontaktandmete jaoks vaadake selles teema jaotist [Commerce’i eelvaatekeskkonna tugi](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="441ef-160">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="441ef-161">Juurdepääsu andmine e-kaubanduse rakendustele</span><span class="sxs-lookup"><span data-stu-id="441ef-161">Grant access to e-Commerce applications</span></span>

> [!IMPORTANT]
> <span data-ttu-id="441ef-162">Isik, kes logib sisse, peab olema Azure AD rentniku administraator, kellel on Azure AD rentniku ID.</span><span class="sxs-lookup"><span data-stu-id="441ef-162">The person who signs in must be an Azure AD tenant admin who has the Azure AD tenant ID.</span></span> <span data-ttu-id="441ef-163">Kui seda etappi edukalt lõpule ei viida, siis ülejäänud ettevalmistamise etapid ei õnnestu.</span><span class="sxs-lookup"><span data-stu-id="441ef-163">If this step isn't successfully completed, the remaining provisioning steps will fail.</span></span>

<span data-ttu-id="441ef-164">E-kaubanduse rakenduste autoriseerimiseks Azure’i tellimusele juurdepääsuks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="441ef-164">To authorize e-Commerce applications to access your Azure subscription, follow these steps.</span></span>

1. <span data-ttu-id="441ef-165">Koostage URL järgmises vormingus.</span><span class="sxs-lookup"><span data-stu-id="441ef-165">Assemble a URL in the following format:</span></span>

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. <span data-ttu-id="441ef-166">Kopeerige ja kleepige URL brauserisse või tekstiredaktorisse ning asendage **\{AAD\_TENANT\_ID\}** oma Azure AD rentniku ID-ga.</span><span class="sxs-lookup"><span data-stu-id="441ef-166">Copy and paste the URL into your browser or text editor, and replace **\{AAD\_TENANT\_ID\}** with your Azure AD tenant ID.</span></span> <span data-ttu-id="441ef-167">Seejärel avage URL.</span><span class="sxs-lookup"><span data-stu-id="441ef-167">Then open the URL.</span></span>
1. <span data-ttu-id="441ef-168">Logige Azure AD sisselogimise dialoogiboksis sisse ja kinnitage, et soovite anda teenusele **Dynamics 365 Commerce (eelvaade)** juurdepääsu oma tellimusele.</span><span class="sxs-lookup"><span data-stu-id="441ef-168">In the Azure AD sign-in dialog box, sign in, and confirm that you want to grant **Dynamics 365 Commerce (Preview)** access to your subscription.</span></span> <span data-ttu-id="441ef-169">Teid suunatakse lehele, mis näitab, kas toiming õnnestus.</span><span class="sxs-lookup"><span data-stu-id="441ef-169">You're redirected to a page that indicates whether the operation was successful.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="441ef-170">Kinnitamine, et eelvaate funktsioonid on saadaval ja LCS-is sisse lülitatud</span><span class="sxs-lookup"><span data-stu-id="441ef-170">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="441ef-171">Kinnitamaks, et eelvaate funktsioonid on saadaval ja LCS-is sisse lülitatud, tehke järgmist</span><span class="sxs-lookup"><span data-stu-id="441ef-171">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="441ef-172">Logige [LCS-i portaali](https://lcs.dynamics.com)sisse, kasutades sama LCS-i kontot, mida kasutasite eelvaatele juurdepääsu taotlemiseks.</span><span class="sxs-lookup"><span data-stu-id="441ef-172">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="441ef-173">Kerige LCS-i avalehel täielikult paremale ja valige paan **Eelvaate funktsiooni haldamine**.</span><span class="sxs-lookup"><span data-stu-id="441ef-173">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Eelvaate funktsiooni paan](./media/preview1.png)

1. <span data-ttu-id="441ef-175">Kerige alla jaotisesse **Privaatsed eelvaate funktsioonid** ja kinnitage, et järgmised funktsioonid oleksid saadaval ja sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="441ef-175">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="441ef-176">E-kaubanduse hindamine</span><span class="sxs-lookup"><span data-stu-id="441ef-176">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="441ef-177">Kaubanduse eelvaate programmi keskkonnad</span><span class="sxs-lookup"><span data-stu-id="441ef-177">Commerce Preview Program Environments</span></span>

    ![Privaatse eelvaate funktsioonid](./media/preview2.png)

1. <span data-ttu-id="441ef-179">Kui need funktsioonid loendis ei ilmu, võtke Microsoftiga ühendust ja andke oma töö meiliaadress, LCS-i konto ja rentniku üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="441ef-179">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="441ef-180">Kontaktandmete jaoks vaadake jaotist [Commerce’i eelvaatekeskkonna tugi](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="441ef-180">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="441ef-181">Loo uus projekt</span><span class="sxs-lookup"><span data-stu-id="441ef-181">Create a new project</span></span>

<span data-ttu-id="441ef-182">LCS-is uue projekti loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="441ef-182">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="441ef-183">LCS-i avalehel valige projekti loomiseks plussmärk (**+**).</span><span class="sxs-lookup"><span data-stu-id="441ef-183">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="441ef-184">Parempoolsel paanil järgige ühte järgmistest etappidest.</span><span class="sxs-lookup"><span data-stu-id="441ef-184">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="441ef-185">Kui olete partner, valige suvand **Migreerimine, lahenduste loomine ja teave**.</span><span class="sxs-lookup"><span data-stu-id="441ef-185">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="441ef-186">Kui olete klient, valige suvand **Potentsiaalsed eelmüügid**.</span><span class="sxs-lookup"><span data-stu-id="441ef-186">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="441ef-187">Sisestage nimi, kirjeldus ja valdkond.</span><span class="sxs-lookup"><span data-stu-id="441ef-187">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="441ef-188">Valige väljal **Toote nimi** suvand **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="441ef-188">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="441ef-189">Valige väljal **Toote versioon** suvand **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="441ef-189">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="441ef-190">Väljal **Metoodika** valige **Dynamics Retail juurutamise metoodika**.</span><span class="sxs-lookup"><span data-stu-id="441ef-190">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="441ef-191">Valikuline: võite portida rollid ja kasutajad olemasolevast projektist.</span><span class="sxs-lookup"><span data-stu-id="441ef-191">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="441ef-192">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="441ef-192">Select **Create**.</span></span> <span data-ttu-id="441ef-193">Kuvatakse projekti vaade.</span><span class="sxs-lookup"><span data-stu-id="441ef-193">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="441ef-194">Azure’i konnektori lisamine</span><span class="sxs-lookup"><span data-stu-id="441ef-194">Add the Azure Connector</span></span>

<span data-ttu-id="441ef-195">Oma LCS-i projektile Azure’i konnektori lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="441ef-195">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="441ef-196">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="441ef-196">Follow one of these steps:</span></span>

    - <span data-ttu-id="441ef-197">Kui olete partner, valige paan **Projekti sätted** kõige parempoolsemal küljel.</span><span class="sxs-lookup"><span data-stu-id="441ef-197">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="441ef-198">Kui olete klient, valige suvand **Projekti sätted** ülemisest menüüst.</span><span class="sxs-lookup"><span data-stu-id="441ef-198">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="441ef-199">Valige suvand **Azure’i konnektorid**.</span><span class="sxs-lookup"><span data-stu-id="441ef-199">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="441ef-200">Azure’i konnektori lisamiseks valige suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="441ef-200">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="441ef-201">Sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="441ef-201">Enter a name.</span></span>
1. <span data-ttu-id="441ef-202">Sisestage oma Azure’i tellimuse ID.</span><span class="sxs-lookup"><span data-stu-id="441ef-202">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="441ef-203">Lülitage suvand **Azureʼi ressursihalduri (ARM) kasutamise konfigureerimine** sisse</span><span class="sxs-lookup"><span data-stu-id="441ef-203">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="441ef-204">Veenduge, et väärtus **Azure’i kordustellimuse AAD rentniku domeen (või ID)** oleks õige.</span><span class="sxs-lookup"><span data-stu-id="441ef-204">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="441ef-205">Vajaduse korral konsulteerige oma Azure’i tellimuse administraatoriga.</span><span class="sxs-lookup"><span data-stu-id="441ef-205">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="441ef-206">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="441ef-206">Select **Next**.</span></span>
1. <span data-ttu-id="441ef-207">Järgige lehel kuvatavaid juhiseid, et anda nõutud rakendustele juurdepääs teie tellimusele.</span><span class="sxs-lookup"><span data-stu-id="441ef-207">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="441ef-208">Vajaduse korral konsulteerige oma Azure’i tellimuse administraatoriga.</span><span class="sxs-lookup"><span data-stu-id="441ef-208">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="441ef-209">Logige sisse [Azure’i portaali](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="441ef-209">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="441ef-210">Veenduge, et valitud oleks õige kaust, ja seejärel valige vasakpoolsel menüül suvand **Tellimused**</span><span class="sxs-lookup"><span data-stu-id="441ef-210">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="441ef-211">Leidke loendist õige tellimus ja valige see.</span><span class="sxs-lookup"><span data-stu-id="441ef-211">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="441ef-212">Vastavalt vajadusele kasutage otsingufunktsiooni.</span><span class="sxs-lookup"><span data-stu-id="441ef-212">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="441ef-213">Valige menüüs suvand **Juurdepääsu juhtelement (IAM)**.</span><span class="sxs-lookup"><span data-stu-id="441ef-213">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="441ef-214">Valige paremal küljel jaotises **Lisa rollimäärang** käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="441ef-214">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="441ef-215">Kuvatakse paan **Lisa rollimäärang**.</span><span class="sxs-lookup"><span data-stu-id="441ef-215">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="441ef-216">Valige väljalt **Roll** väärtus **Kaasautor**.</span><span class="sxs-lookup"><span data-stu-id="441ef-216">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="441ef-217">Jätke väljale **Määra juurdepääs** vaikeväärtus **Azure AD kasutaja, grupp või teenusesubjekt**.</span><span class="sxs-lookup"><span data-stu-id="441ef-217">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="441ef-218">Jaotisesse **Vali** sisestage **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="441ef-218">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="441ef-219">Valige loendist **Dynamicsi juurutamise teenused \[wsfed-enabled\]**.</span><span class="sxs-lookup"><span data-stu-id="441ef-219">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="441ef-220">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="441ef-220">Select **Save**.</span></span>

1. <span data-ttu-id="441ef-221">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="441ef-221">Select **Next**.</span></span>
1. <span data-ttu-id="441ef-222">Järgige lehel kuvatavaid juhiseid, et anda nõutud rakendustele juurdepääs teie tellimusele.</span><span class="sxs-lookup"><span data-stu-id="441ef-222">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="441ef-223">Vajaduse korral konsulteerige oma Azure’i tellimuse administraatoriga.</span><span class="sxs-lookup"><span data-stu-id="441ef-223">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="441ef-224">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="441ef-224">Select **Next**.</span></span>
1. <span data-ttu-id="441ef-225">Väljal **Azure’i regioon** valige **Ida-USA**, **Ida-USA 2**, **Lääne-USA** või **Lääne-USA 2**.</span><span class="sxs-lookup"><span data-stu-id="441ef-225">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="441ef-226">Valige käsk **Ühenda**.</span><span class="sxs-lookup"><span data-stu-id="441ef-226">Select **Connect**.</span></span> <span data-ttu-id="441ef-227">Teie Azure'i konnektor peaks loendis ilmuma.</span><span class="sxs-lookup"><span data-stu-id="441ef-227">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="441ef-228">Commerce’i eelvaate demobaasi laiendi importimine</span><span class="sxs-lookup"><span data-stu-id="441ef-228">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="441ef-229">Commerce’i eelvaate demobaasi laiendi oma projekti importimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="441ef-229">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="441ef-230">Avage oma projekti avaleht, valides ülaosas projekti nime.</span><span class="sxs-lookup"><span data-stu-id="441ef-230">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="441ef-231">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="441ef-231">Follow one of these steps:</span></span>

    - <span data-ttu-id="441ef-232">Kui olete partner, valige paan **Varateek** kõige parempoolsemal küljel.</span><span class="sxs-lookup"><span data-stu-id="441ef-232">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="441ef-233">Kui olete klient, valige suvand **Varateek** ülemisest menüüst.</span><span class="sxs-lookup"><span data-stu-id="441ef-233">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="441ef-234">Valige vasakpoolses loendis suvand **Tarkvara juurutatav pakett**.</span><span class="sxs-lookup"><span data-stu-id="441ef-234">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="441ef-235">Valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="441ef-235">Select **Import**.</span></span>
1. <span data-ttu-id="441ef-236">Jaotises **Jagatud varateek** valige varade loendist suvand **Commerce’i eelvaate demobaasi laiend**.</span><span class="sxs-lookup"><span data-stu-id="441ef-236">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="441ef-237">Valige käsk **Võta**.</span><span class="sxs-lookup"><span data-stu-id="441ef-237">Select **Pick**.</span></span> <span data-ttu-id="441ef-238">Naasete varateeki ja peaksite nägema laiendit loendis.</span><span class="sxs-lookup"><span data-stu-id="441ef-238">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="441ef-239">Järgmisel joonisel on näha tegevused, mis tuleb teha LCS-i lehel **Varateek**.</span><span class="sxs-lookup"><span data-stu-id="441ef-239">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Commerce’i eelvaate demobaasi laiendi importimine](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="441ef-241">Keskkonna juurutamine</span><span class="sxs-lookup"><span data-stu-id="441ef-241">Deploy the environment</span></span>

<span data-ttu-id="441ef-242">Keskkonna juurutamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="441ef-242">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="441ef-243">Võimalik, et te ei pea samme 6, 7 ja/või 8 läbima, kuna ühe suvandi ekraanid jäetakse vahele.</span><span class="sxs-lookup"><span data-stu-id="441ef-243">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="441ef-244">Kui olete vaates **Keskkonna parameetrid** kinnitage, et teil on tekst **Dynamics 365 Commerce (eelvaade) – demo (10.0.6 platvormi värskendus 30)** otse välja **Keskkonna nimi** kohal.</span><span class="sxs-lookup"><span data-stu-id="441ef-244">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)** appears directly above the **Environment name** field.</span></span> <span data-ttu-id="441ef-245">Vt joonist, mis kuvatakse pärast sammu 8.</span><span class="sxs-lookup"><span data-stu-id="441ef-245">See the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="441ef-246">Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="441ef-246">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="441ef-247">Valige suvand **Lisa** keskkonna lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="441ef-247">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="441ef-248">Valige väljal **Rakenduse versioon** suvand **10.0.6**.</span><span class="sxs-lookup"><span data-stu-id="441ef-248">In the **Application version** field, select **10.0.6**.</span></span>
1. <span data-ttu-id="441ef-249">Väljal **Platvormi versioon** valige **Platvormi värskendus 30**.</span><span class="sxs-lookup"><span data-stu-id="441ef-249">In the **Platform version** field, select **Platform Update 30**.</span></span>

    ![Rakenduse ja platvormi versioonide valimine](./media/project1.png)

1. <span data-ttu-id="441ef-251">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="441ef-251">Select **Next**.</span></span>
1. <span data-ttu-id="441ef-252">Valige keskkonna topoloogiaks **Demo**.</span><span class="sxs-lookup"><span data-stu-id="441ef-252">Select **Demo** as the environment topology.</span></span>

    ![Keskkonna topoloogia valimine 1](./media/project2.png)

1. <span data-ttu-id="441ef-254">Valige keskkonna topoloogiaks **Dynamics 365 Commerce (eelvaade) – demo**.</span><span class="sxs-lookup"><span data-stu-id="441ef-254">Select **Dynamics 365 Commerce (Preview) - Demo** as the environment topology.</span></span> <span data-ttu-id="441ef-255">Kui olete varem konfigureerinud ühe Azure’i konnektori, kasutatakse seda selles keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="441ef-255">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="441ef-256">Mitme Azure’i konnektori konfigureerimisel saate valida, millist konnektorit kasutada: **Ida-USA**, **Ida-USA**2 **, Lääne-USA** või **Lääne-USA 2**.</span><span class="sxs-lookup"><span data-stu-id="441ef-256">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="441ef-257">(Parima lõppeesmärgini jõudluse saavutamiseks soovitame valida **Lääne-USA 2**.)</span><span class="sxs-lookup"><span data-stu-id="441ef-257">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Keskkonna topoloogia valimine 2](./media/project3.png)

1. <span data-ttu-id="441ef-259">Lehel **Keskkonna juurutamine** sisestage keskkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="441ef-259">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="441ef-260">Jätke täpsemad sätted nii nagu need on.</span><span class="sxs-lookup"><span data-stu-id="441ef-260">Leave the advanced settings as they are.</span></span>

    ![Keskkonna juurutamise leht](./media/project4.png)

1. <span data-ttu-id="441ef-262">Kohandage VM-i suurust vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="441ef-262">Adjust the VM size as required.</span></span> <span data-ttu-id="441ef-263">(Soovitame VM-i varude arvestusühikut \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="441ef-263">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="441ef-264">Vaadake üle hinnakujunduse ja litsentsimise tingimused ning märkige ruut, et näidata, et olete nendega nõus.</span><span class="sxs-lookup"><span data-stu-id="441ef-264">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="441ef-265">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="441ef-265">Select **Next**.</span></span>
1. <span data-ttu-id="441ef-266">Juurutamise kinnituse lehel kinnitage, et üksikasjad oleksid õiged ja valige seejärel nupp **Juuruta**.</span><span class="sxs-lookup"><span data-stu-id="441ef-266">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="441ef-267">Olete naasnud vaatesse **Pilve majutatud keskkonnad** ja teie keskkond peaks ilmuma loendis.</span><span class="sxs-lookup"><span data-stu-id="441ef-267">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="441ef-268">Teie soovitud keskkond ilmub järjekorras ja seejärel juurutatakse.</span><span class="sxs-lookup"><span data-stu-id="441ef-268">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="441ef-269">Keskkonna töövoogude lõpule viimine võtab aega.</span><span class="sxs-lookup"><span data-stu-id="441ef-269">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="441ef-270">Seetõttu kontrollige umbes kuue kuni üheksa tunni pärast uuesti.</span><span class="sxs-lookup"><span data-stu-id="441ef-270">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="441ef-271">Enne jätkamist veenduge, et teie keskkonna olek oleks **Juurutatud**.</span><span class="sxs-lookup"><span data-stu-id="441ef-271">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-rcsu"></a><span data-ttu-id="441ef-272">RCSU lähtestamine</span><span class="sxs-lookup"><span data-stu-id="441ef-272">Initialize RCSU</span></span>

<span data-ttu-id="441ef-273">RCSU-i lähtestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="441ef-273">To initialize RCSU, follow these steps.</span></span>

1. <span data-ttu-id="441ef-274">Vaates **Pilve majutatud keskkonnad** valige loendist oma keskkond.</span><span class="sxs-lookup"><span data-stu-id="441ef-274">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="441ef-275">Valige paremal olevast keskkonna vaatest **Täielik teave**.</span><span class="sxs-lookup"><span data-stu-id="441ef-275">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="441ef-276">Ilmub keskkonna üksikasjade vaade.</span><span class="sxs-lookup"><span data-stu-id="441ef-276">The environment details view appears.</span></span>
1. <span data-ttu-id="441ef-277">Jaotises **Keskkonna funktsioonid** valige käsk **Halda**.</span><span class="sxs-lookup"><span data-stu-id="441ef-277">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="441ef-278">Vahekaardil **Jaemüük** valige **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="441ef-278">On the **Retail** tab, select **Initialize**.</span></span> <span data-ttu-id="441ef-279">Ilmub RCSU lähtestamise parameetrite vaade.</span><span class="sxs-lookup"><span data-stu-id="441ef-279">The RCSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="441ef-280">Väljal **Regioon** valige **Ida-USA**, **Ida-USA 2**, **Lääne-USA** või **Lääne-USA 2**.</span><span class="sxs-lookup"><span data-stu-id="441ef-280">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="441ef-281">Väljal **Versioon** valige loendist suvand **Määra versioon** ja määrake seejärel kuvataval väljal **9.16.19262.5**.</span><span class="sxs-lookup"><span data-stu-id="441ef-281">In the **Version** field, select **Specify a version** in the list, and then specify **9.16.19262.5** in the field that appears.</span></span> <span data-ttu-id="441ef-282">Määrake kindlasti siin näidatud täpne versioon.</span><span class="sxs-lookup"><span data-stu-id="441ef-282">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="441ef-283">Vastasel juhul peate uuendama RCSU hiljem õigele versioonile.</span><span class="sxs-lookup"><span data-stu-id="441ef-283">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="441ef-284">Lülitage suvand **Rakenda laiend** sisse.</span><span class="sxs-lookup"><span data-stu-id="441ef-284">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="441ef-285">Laiendite loendist valige suvand **Kaubanduse eelvaate demobaasi laiend**.</span><span class="sxs-lookup"><span data-stu-id="441ef-285">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="441ef-286">Valige **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="441ef-286">Select **Initialize**.</span></span>
1. <span data-ttu-id="441ef-287">Juurutamise kinnituse lehel kinnitage, et üksikasjad oleksid õiged ja valige seejärel nupp **Jah**.</span><span class="sxs-lookup"><span data-stu-id="441ef-287">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="441ef-288">Olete naasnud vaatesse **Jaemüügi haldus**, kus vahekaart **Jaemüük** on valitud.</span><span class="sxs-lookup"><span data-stu-id="441ef-288">You're returned to the **Retail management** view, where the **Retail** tab is selected.</span></span> <span data-ttu-id="441ef-289">Teie RCSU on ettevalmistamiseks ootele pandud.</span><span class="sxs-lookup"><span data-stu-id="441ef-289">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="441ef-290">Enne jätkamist veenduge, et teie RCSU olek oleks **Õnnestus**.</span><span class="sxs-lookup"><span data-stu-id="441ef-290">Before you continue, make sure that the status of your RCSU is **Success**.</span></span> <span data-ttu-id="441ef-291">Lähtestamiseks kulub umbes kaks kuni viis tundi.</span><span class="sxs-lookup"><span data-stu-id="441ef-291">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="441ef-292">E-kaubanduse lähtestamine</span><span class="sxs-lookup"><span data-stu-id="441ef-292">Initialize e-Commerce</span></span>

<span data-ttu-id="441ef-293">E-kaubanduse lähtestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="441ef-293">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="441ef-294">Vahekaardil **E-kaubandus (eelvaade)** vaadake üle eelvaate nõusolek ja seejärel valige **Häälestus**.</span><span class="sxs-lookup"><span data-stu-id="441ef-294">On the **e-Commerce (Preview)** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="441ef-295">Väljale **E-kaubanduse rentniku nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="441ef-295">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="441ef-296">Võtke siiski arvesse, et see nimi on nähtav mõnes URL-is, mis viitavad teie e-kaubanduse eksemplarile.</span><span class="sxs-lookup"><span data-stu-id="441ef-296">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="441ef-297">Väljal **Komponendi Retail Cloud Scale Unit nimi** valige loendist oma RCSU.</span><span class="sxs-lookup"><span data-stu-id="441ef-297">In the **Retail cloud scale unit name** field, select your RCSU in the list.</span></span> <span data-ttu-id="441ef-298">(Loendis peaks olema ainult üks valik.)</span><span class="sxs-lookup"><span data-stu-id="441ef-298">(The list should have only one option.)</span></span>

    <span data-ttu-id="441ef-299">Väli **E-kaubanduse geograafia** väli määratakse automaatselt ja väärtust ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="441ef-299">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="441ef-300">Jätkamiseks valige nupp **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="441ef-300">Select **Next** to continue.</span></span>
1. <span data-ttu-id="441ef-301">Väljale **Toetatud hostinimed** mis tahes kehtiv domeen, nt `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="441ef-301">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="441ef-302">Väljale **AAD süsteemi administraatori turberühm** sisestage selle turberühma nime esimesed tähed, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="441ef-302">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="441ef-303">Otsingutulemuste kuvamiseks valige suurendusklaasi ikoon.</span><span class="sxs-lookup"><span data-stu-id="441ef-303">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="441ef-304">Valige loendist turberühm.</span><span class="sxs-lookup"><span data-stu-id="441ef-304">Select a security group from the list.</span></span>
2.  <span data-ttu-id="441ef-305">Väljale **AAD hinnangute ja arvustuse moderaatori turberühm** sisestage selle turberühma nime esimesed tähed, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="441ef-305">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="441ef-306">Otsingutulemuste kuvamiseks valige suurendusklaasi ikoon.</span><span class="sxs-lookup"><span data-stu-id="441ef-306">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="441ef-307">Valige loendist turberühm.</span><span class="sxs-lookup"><span data-stu-id="441ef-307">Select a security group from the list.</span></span>
1. <span data-ttu-id="441ef-308">Jätke suvand **Hinnangute ja arvustuste teenuse häälestuse lubamine** sisselülitatuks.</span><span class="sxs-lookup"><span data-stu-id="441ef-308">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="441ef-309">Kui olete juba Microsoft Azure Active Directory (Azure AD) nõusoleku etapi lõpetanud, nagu on kirjeldatud jaotises „Juurdepääsu andmine e-kaubanduse rakendustele”, märkige oma nõusoleku kinnitamiseks ruut.</span><span class="sxs-lookup"><span data-stu-id="441ef-309">If you have already completed the Microsoft Azure Active Directory (Azure AD) consent step as described in the "Grant access to e-Commerce applications" section, select the check box to confirm your consent.</span></span> <span data-ttu-id="441ef-310">Kui te pole seda etappi veel lõpetanud, peate seda tegema enne lähtestamise jätkamist.</span><span class="sxs-lookup"><span data-stu-id="441ef-310">If you have not yet completed this step, you need to do that before proceeding with the initialization.</span></span> <span data-ttu-id="441ef-311">Valige märkeruudu kõrval tekstis link, et avada nõusoleku dialoogiboks ja lõpetada samm.</span><span class="sxs-lookup"><span data-stu-id="441ef-311">Select the link within the text next to the check box to open the consent dialog box and complete the step.</span></span>
1. <span data-ttu-id="441ef-312">Valige **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="441ef-312">Select **Initialize**.</span></span> <span data-ttu-id="441ef-313">Olete naasnud vaatesse **Jaemüügi haldus**, kus vahekaart **E-kaubandus (eelvaade)** on valitud.</span><span class="sxs-lookup"><span data-stu-id="441ef-313">You're returned to the **Retail management** view, where the **e-Commerce (Preview)** tab is selected.</span></span> <span data-ttu-id="441ef-314">E-kaubanduse lähtestamine on käivitatud.</span><span class="sxs-lookup"><span data-stu-id="441ef-314">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="441ef-315">Enne jätkamist oodake, kuni teie e-kaubanduse lähtestamise olek on **Lähtestamine edukas**.</span><span class="sxs-lookup"><span data-stu-id="441ef-315">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="441ef-316">All paremal jaotises **Lingid** märkige järgmiste linkide URL-id:</span><span class="sxs-lookup"><span data-stu-id="441ef-316">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="441ef-317">**E-kaubanduse sait** – link teie e-kaubanduse saidi juurele.</span><span class="sxs-lookup"><span data-stu-id="441ef-317">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="441ef-318">**E-kaubanduse saidi haldustööriist** – link saidi halduse tööriistale.</span><span class="sxs-lookup"><span data-stu-id="441ef-318">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="441ef-319">Commerce’i eelvaatekeskkonna tugi</span><span class="sxs-lookup"><span data-stu-id="441ef-319">Commerce preview environment support</span></span>

<span data-ttu-id="441ef-320">Kui teil tekib ettevalmistuse etappide lõpetamisel probleeme, külastage abi saamiseks [Rakenduse Microsoft Dynamics 365 Commerce eelvaate Yammeri gruppi](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="441ef-320">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="441ef-321">Kui teil tekib probleeme Yammer-grupile juurdepääsu loomisel, saate Microsoftiga ühendust võtta e-postiaadressil <Dynamics365Commerce@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="441ef-321">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="441ef-322">Seda meiliaadressi ei jälgita aktiivselt.</span><span class="sxs-lookup"><span data-stu-id="441ef-322">This email address isn't actively monitored.</span></span> <span data-ttu-id="441ef-323">Seetõttu oodata viivitust vastuses.</span><span class="sxs-lookup"><span data-stu-id="441ef-323">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="441ef-324">Järgmised etapid</span><span class="sxs-lookup"><span data-stu-id="441ef-324">Next steps</span></span>

<span data-ttu-id="441ef-325">Oma Commerce’i eelvaatekeskkonna ettevalmistamise ja konfigueerimise protsessi jätkamiseks vaadake teemat [Commerce’i eelvaatekeskkonna konfigureerimine](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="441ef-325">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="441ef-326">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="441ef-326">Additional resources</span></span>

[<span data-ttu-id="441ef-327">Commerce'i eelvaatekeskkonna ülevaade</span><span class="sxs-lookup"><span data-stu-id="441ef-327">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="441ef-328">Commerce'i eelvaatekeskkonna konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="441ef-328">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="441ef-329">Commerce'i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="441ef-329">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="441ef-330">Commerce'i eelvaatekeskkonna KKK</span><span class="sxs-lookup"><span data-stu-id="441ef-330">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="441ef-331">Microsofti elutsükli teenused (LCS)</span><span class="sxs-lookup"><span data-stu-id="441ef-331">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="441ef-332">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="441ef-332">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="441ef-333">Microsoft Azure'i portaal</span><span class="sxs-lookup"><span data-stu-id="441ef-333">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="441ef-334">Dynamics 365 Commerce veebisait</span><span class="sxs-lookup"><span data-stu-id="441ef-334">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="441ef-335">Abiressursid rakenduse Dynamics 365 Retail jaoks</span><span class="sxs-lookup"><span data-stu-id="441ef-335">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
