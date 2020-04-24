---
title: Dynamics 365 Commerce’i eelvaatekeskkonna ettevalmistamine
description: Selles teemas selgitatakse, kuidas valmistada ette Microsoft Dynamics 365 Commerce’i eelvaatekeskkond.
author: psimolin
manager: annbe
ms.date: 04/10/2020
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
ms.openlocfilehash: d54db89372a0f9ef5b267d25e14067e3243a803c
ms.sourcegitcommit: 4254acb3cf8c6299fc2f3818ea6c499f058320d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/09/2020
ms.locfileid: "3254744"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="a9072-103">Dynamics 365 Commerce’i eelvaatekeskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="a9072-103">Provision a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a9072-104">Selles teemas selgitatakse, kuidas valmistada ette Dynamics 365 Commerce’i eelvaatekeskkond.</span><span class="sxs-lookup"><span data-stu-id="a9072-104">This topic explains how to provision a Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="a9072-105">Enne alustamist soovitame teil see teema kiiresti läbi vaadata, et saada protsessi nõudmistest aimu.</span><span class="sxs-lookup"><span data-stu-id="a9072-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="a9072-106">Kui te pole veel andnud juurdepääsu rakenduse Dynamics 365 Commerce eelvaatele, saate taotleda eelvaate juurdepääsu [Dynamics 365 Commerce’i veebisaidilt](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="a9072-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Dynamics 365 Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="a9072-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="a9072-107">Overview</span></span>

<span data-ttu-id="a9072-108">Oma Commerce’i eelvaatekeskkonna edukaks ettevalmistamiseks peate looma projekti, millel on kindel toote nimi ja tüüp.</span><span class="sxs-lookup"><span data-stu-id="a9072-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="a9072-109">Keskkonnal ja kaubanduse skaala üksusel (CSU) on samuti mõned konkreetsed parameetrid, mida peate kasutama, kui hiljem e-kaubandust ette valmistate.</span><span class="sxs-lookup"><span data-stu-id="a9072-109">The environment and commerce scale unit (CSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="a9072-110">Selle teema juhised kirjeldavad kõiki vajalikke etappe, mida peate ettevalmistamiseks täitma, ja milliseid parameetreid peate kasutada.</span><span class="sxs-lookup"><span data-stu-id="a9072-110">The instructions in this topic describe all the steps required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="a9072-111">Pärast seda, kui olete oma Commerce’i eelvaatekeskkonna edukat ette valmistanud, peate läbima ettevalmistamiseks mõned hilisemad etapid.</span><span class="sxs-lookup"><span data-stu-id="a9072-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="a9072-112">Mõned etapid on valikulised, olenevalt sellest, milliseid süsteemi aspekte soovite hinnata.</span><span class="sxs-lookup"><span data-stu-id="a9072-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="a9072-113">Võite valikulised etapid alati hiljem läbida.</span><span class="sxs-lookup"><span data-stu-id="a9072-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="a9072-114">Teavet selle kohta, kuidas Commerce’i eelvaatekeskkonda pärast ettevalmistamist konfigureerida, vaadake teemast [Commerce’i eelvaatekeskkonna konfigureerimine](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="a9072-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="a9072-115">Teavet selle kohta, kuidas Commerce’i eelvaatekeskkonna valikulisi funktsioone konfigureerida, vaadake teemast [Commerce’i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="a9072-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="a9072-116">Kui teil on küsimusi ettevalmistamise etappide kohta või esineb probleeme, andke Microsoftile sellest teada [rakenduse Microsoft Dynamics 365 Commerce eelvaate Yammeri grupis](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="a9072-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a9072-117">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="a9072-117">Prerequisites</span></span>

<span data-ttu-id="a9072-118">Enne Commerce’i eelvaatekeskkonna ettevalmistamist peavad olema kehtestatud järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="a9072-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="a9072-119">Teil on juurdepääs Microsoft Dynamicsi portaalile Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a9072-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="a9072-120">Olete olemasolev Microsoft Dynamics 365 partner või klient ja olete võimeline looma Dynamics 365 Commerce’i projekti.</span><span class="sxs-lookup"><span data-stu-id="a9072-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="a9072-121">Teid on rakenduse Dynamics 365 Commerce eelvaate programmi vastu võetud.</span><span class="sxs-lookup"><span data-stu-id="a9072-121">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="a9072-122">Teil on vajalikud õigused, et luua projekt suvandile **Migreerimine, lahenduste loomine ja teave**.</span><span class="sxs-lookup"><span data-stu-id="a9072-122">You have the required permissions to create a project for **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="a9072-123">Olete rolli **Keskkonnahaldur** või **Projekti omanik** liige projektis, kus te keskkonna ette valmistate.</span><span class="sxs-lookup"><span data-stu-id="a9072-123">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="a9072-124">Teil on administraatori juurdepääs oma Microsoft Azure’i tellimusele või olete ühenduses tellimise administraatoriga, kes saab teie nimel lõpetada kaks etappi, mis nõuavad administraatori õigusi.</span><span class="sxs-lookup"><span data-stu-id="a9072-124">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="a9072-125">Teie Azure Active Directory (Azure AD) rentniku ID on saadaval.</span><span class="sxs-lookup"><span data-stu-id="a9072-125">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="a9072-126">Olete loonud Azure AD turberühma, mida saab kasutada e-kaubanduse süsteemiadministraatorite grupina ja mille ID on saadaval.</span><span class="sxs-lookup"><span data-stu-id="a9072-126">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="a9072-127">Olete loonud Azure AD turberühma, mida saab kasutada hinnangute ja arvustuste moderaatori grupina ja mille ID on saadaval.</span><span class="sxs-lookup"><span data-stu-id="a9072-127">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="a9072-128">(See turberühm võib olla sama, mis e-kaubanduse süsteemiadministraatorite grupp.)</span><span class="sxs-lookup"><span data-stu-id="a9072-128">(This security group can be the same as the e-Commerce system admin group.)</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="a9072-129">Oma Commerce’i eelvaatekeskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="a9072-129">Provision your Commerce preview environment</span></span>

<span data-ttu-id="a9072-130">Need protseduurid selgitavad, kuidas valmistada ette Commerce’i eelvaatekeskkonda.</span><span class="sxs-lookup"><span data-stu-id="a9072-130">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="a9072-131">Pärast nende edukat lõpetamist on Commerce’i eelvaatekeskkond konfigureerimiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="a9072-131">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="a9072-132">Kõik siin kirjeldatud tegevused esinevad LCS portaalis.</span><span class="sxs-lookup"><span data-stu-id="a9072-132">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9072-133">Eelvaate juurdepääs on seotud LCS-i konto ja organisatsiooniga, mille määrasite oma Commerce’i eelvaate rakenduses.</span><span class="sxs-lookup"><span data-stu-id="a9072-133">Preview access is tied to the LCS account and organization that you specified in your Commerce preview application.</span></span> <span data-ttu-id="a9072-134">Peate kasutama Commerce’i eelvaatekeskkonna ettevalmistamiseks sama kontot.</span><span class="sxs-lookup"><span data-stu-id="a9072-134">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="a9072-135">Kui peate kasutama Commerce’i eelvaatekeskkonna jaoks erinevat LCS-i kontot või rentnikku, peate teavitama Microsofti nendest üksikasjadest.</span><span class="sxs-lookup"><span data-stu-id="a9072-135">If you need to use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="a9072-136">Kontaktandmete jaoks vaadake selles teema jaotist [Commerce’i eelvaatekeskkonna tugi](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="a9072-136">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="a9072-137">Kinnitamine, et eelvaate funktsioonid on saadaval ja LCS-is sisse lülitatud</span><span class="sxs-lookup"><span data-stu-id="a9072-137">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="a9072-138">Kinnitamaks, et eelvaate funktsioonid on saadaval ja LCS-is sisse lülitatud, tehke järgmist</span><span class="sxs-lookup"><span data-stu-id="a9072-138">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="a9072-139">Logige [LCS-i portaali](https://lcs.dynamics.com)sisse, kasutades sama LCS-i kontot, mida kasutasite eelvaatele juurdepääsu taotlemiseks.</span><span class="sxs-lookup"><span data-stu-id="a9072-139">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="a9072-140">Kerige LCS-i avalehel täielikult paremale ja valige paan **Eelvaate funktsiooni haldamine**.</span><span class="sxs-lookup"><span data-stu-id="a9072-140">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Eelvaate funktsiooni paan](./media/preview1.png)

1. <span data-ttu-id="a9072-142">Kerige alla jaotisesse **Privaatsed eelvaate funktsioonid** ja kinnitage, et järgmised funktsioonid oleksid saadaval ja sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="a9072-142">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="a9072-143">E-kaubanduse hindamine</span><span class="sxs-lookup"><span data-stu-id="a9072-143">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="a9072-144">Kaubanduse eelvaate programmi keskkonnad</span><span class="sxs-lookup"><span data-stu-id="a9072-144">Commerce Preview Program Environments</span></span>

    ![Privaatse eelvaate funktsioonid](./media/preview2.png)

1. <span data-ttu-id="a9072-146">Kui need funktsioonid loendis ei ilmu, võtke Microsoftiga ühendust ja andke oma töö meiliaadress, LCS-i konto ja rentniku üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="a9072-146">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="a9072-147">Kontaktandmete jaoks vaadake jaotist [Commerce’i eelvaatekeskkonna tugi](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="a9072-147">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="a9072-148">Loo uus projekt</span><span class="sxs-lookup"><span data-stu-id="a9072-148">Create a new project</span></span>

<span data-ttu-id="a9072-149">LCS-is uue projekti loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a9072-149">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="a9072-150">LCS-i avalehel valige projekti loomiseks plussmärk (**+**).</span><span class="sxs-lookup"><span data-stu-id="a9072-150">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="a9072-151">Parempoolsel paanil järgige ühte järgmistest etappidest.</span><span class="sxs-lookup"><span data-stu-id="a9072-151">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="a9072-152">Kui olete partner, valige suvand **Migreerimine, lahenduste loomine ja teave**.</span><span class="sxs-lookup"><span data-stu-id="a9072-152">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="a9072-153">Kui olete klient, valige suvand **Potentsiaalsed eelmüügid**.</span><span class="sxs-lookup"><span data-stu-id="a9072-153">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="a9072-154">Sisestage nimi, kirjeldus ja valdkond.</span><span class="sxs-lookup"><span data-stu-id="a9072-154">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="a9072-155">Valige väljal **Toote nimi** suvand **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="a9072-155">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="a9072-156">Valige väljal **Toote versioon** suvand **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="a9072-156">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="a9072-157">Väljal **Metoodika** valige **Dynamics Retail juurutamise metoodika**.</span><span class="sxs-lookup"><span data-stu-id="a9072-157">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="a9072-158">Valikuline: võite portida rollid ja kasutajad olemasolevast projektist.</span><span class="sxs-lookup"><span data-stu-id="a9072-158">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="a9072-159">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="a9072-159">Select **Create**.</span></span> <span data-ttu-id="a9072-160">Kuvatakse projekti vaade.</span><span class="sxs-lookup"><span data-stu-id="a9072-160">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="a9072-161">Azure’i konnektori lisamine</span><span class="sxs-lookup"><span data-stu-id="a9072-161">Add the Azure Connector</span></span>

<span data-ttu-id="a9072-162">Oma LCS-i projektile Azure’i konnektori lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a9072-162">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="a9072-163">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="a9072-163">Follow one of these steps:</span></span>

    - <span data-ttu-id="a9072-164">Kui olete partner, valige paan **Projekti sätted** kõige parempoolsemal küljel.</span><span class="sxs-lookup"><span data-stu-id="a9072-164">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="a9072-165">Kui olete klient, valige suvand **Projekti sätted** ülemisest menüüst.</span><span class="sxs-lookup"><span data-stu-id="a9072-165">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="a9072-166">Valige suvand **Azure’i konnektorid**.</span><span class="sxs-lookup"><span data-stu-id="a9072-166">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="a9072-167">Azure’i konnektori lisamiseks valige suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="a9072-167">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="a9072-168">Sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="a9072-168">Enter a name.</span></span>
1. <span data-ttu-id="a9072-169">Sisestage oma Azure’i tellimuse ID.</span><span class="sxs-lookup"><span data-stu-id="a9072-169">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="a9072-170">Lülitage suvand **Azureʼi ressursihalduri (ARM) kasutamise konfigureerimine** sisse</span><span class="sxs-lookup"><span data-stu-id="a9072-170">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="a9072-171">Veenduge, et väärtus **Azure’i kordustellimuse AAD rentniku domeen (või ID)** oleks õige.</span><span class="sxs-lookup"><span data-stu-id="a9072-171">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="a9072-172">Vajaduse korral konsulteerige oma Azure’i tellimuse administraatoriga.</span><span class="sxs-lookup"><span data-stu-id="a9072-172">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="a9072-173">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="a9072-173">Select **Next**.</span></span>
1. <span data-ttu-id="a9072-174">Järgige lehel kuvatavaid juhiseid, et anda nõutud rakendustele juurdepääs teie tellimusele.</span><span class="sxs-lookup"><span data-stu-id="a9072-174">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="a9072-175">Vajaduse korral konsulteerige oma Azure’i tellimuse administraatoriga.</span><span class="sxs-lookup"><span data-stu-id="a9072-175">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="a9072-176">Logige sisse [Azure’i portaali](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="a9072-176">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="a9072-177">Veenduge, et valitud oleks õige kaust, ja seejärel valige vasakpoolsel menüül suvand **Tellimused**</span><span class="sxs-lookup"><span data-stu-id="a9072-177">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="a9072-178">Leidke loendist õige tellimus ja valige see.</span><span class="sxs-lookup"><span data-stu-id="a9072-178">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="a9072-179">Vastavalt vajadusele kasutage otsingufunktsiooni.</span><span class="sxs-lookup"><span data-stu-id="a9072-179">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="a9072-180">Valige menüüs suvand **Juurdepääsu juhtelement (IAM)**.</span><span class="sxs-lookup"><span data-stu-id="a9072-180">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="a9072-181">Valige paremal küljel jaotises **Lisa rollimäärang** käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="a9072-181">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="a9072-182">Kuvatakse paan **Lisa rollimäärang**.</span><span class="sxs-lookup"><span data-stu-id="a9072-182">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="a9072-183">Valige väljalt **Roll** väärtus **Kaasautor**.</span><span class="sxs-lookup"><span data-stu-id="a9072-183">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="a9072-184">Jätke väljale **Määra juurdepääs** vaikeväärtus **Azure AD kasutaja, grupp või teenusesubjekt**.</span><span class="sxs-lookup"><span data-stu-id="a9072-184">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="a9072-185">Jaotisesse **Vali** sisestage **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="a9072-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="a9072-186">Valige loendist **Dynamicsi juurutamise teenused \[wsfed-enabled\]**.</span><span class="sxs-lookup"><span data-stu-id="a9072-186">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="a9072-187">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a9072-187">Select **Save**.</span></span>

1. <span data-ttu-id="a9072-188">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="a9072-188">Select **Next**.</span></span>
1. <span data-ttu-id="a9072-189">Järgige lehel kuvatavaid juhiseid, et anda nõutud rakendustele juurdepääs teie tellimusele.</span><span class="sxs-lookup"><span data-stu-id="a9072-189">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="a9072-190">Vajaduse korral konsulteerige oma Azure’i tellimuse administraatoriga.</span><span class="sxs-lookup"><span data-stu-id="a9072-190">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="a9072-191">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="a9072-191">Select **Next**.</span></span>
1. <span data-ttu-id="a9072-192">Väljal **Azure’i regioon** valige **Ida-USA**, **Ida-USA 2**, **Lääne-USA** või **Lääne-USA 2**.</span><span class="sxs-lookup"><span data-stu-id="a9072-192">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="a9072-193">Valige käsk **Ühenda**.</span><span class="sxs-lookup"><span data-stu-id="a9072-193">Select **Connect**.</span></span> <span data-ttu-id="a9072-194">Teie Azure'i konnektor peaks loendis ilmuma.</span><span class="sxs-lookup"><span data-stu-id="a9072-194">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="a9072-195">Commerce’i eelvaate demobaasi laiendi importimine</span><span class="sxs-lookup"><span data-stu-id="a9072-195">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="a9072-196">Commerce’i eelvaate demobaasi laiendi oma projekti importimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a9072-196">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="a9072-197">Avage oma projekti avaleht, valides ülaosas projekti nime.</span><span class="sxs-lookup"><span data-stu-id="a9072-197">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="a9072-198">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="a9072-198">Follow one of these steps:</span></span>

    - <span data-ttu-id="a9072-199">Kui olete partner, valige paan **Varateek** kõige parempoolsemal küljel.</span><span class="sxs-lookup"><span data-stu-id="a9072-199">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="a9072-200">Kui olete klient, valige suvand **Varateek** ülemisest menüüst.</span><span class="sxs-lookup"><span data-stu-id="a9072-200">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="a9072-201">Valige vasakpoolses loendis suvand **Tarkvara juurutatav pakett**.</span><span class="sxs-lookup"><span data-stu-id="a9072-201">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="a9072-202">Valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="a9072-202">Select **Import**.</span></span>
1. <span data-ttu-id="a9072-203">Jaotises **Jagatud varateek** valige varade loendist suvand **Commerce’i eelvaate demobaasi laiend**.</span><span class="sxs-lookup"><span data-stu-id="a9072-203">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="a9072-204">Valige käsk **Võta**.</span><span class="sxs-lookup"><span data-stu-id="a9072-204">Select **Pick**.</span></span> <span data-ttu-id="a9072-205">Naasete varateeki ja peaksite nägema laiendit loendis.</span><span class="sxs-lookup"><span data-stu-id="a9072-205">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="a9072-206">Järgmisel joonisel on näha tegevused, mis tuleb teha LCS-i lehel **Varateek**.</span><span class="sxs-lookup"><span data-stu-id="a9072-206">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Commerce’i eelvaate demobaasi laiendi importimine](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="a9072-208">Keskkonna juurutamine</span><span class="sxs-lookup"><span data-stu-id="a9072-208">Deploy the environment</span></span>

<span data-ttu-id="a9072-209">Keskkonna juurutamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a9072-209">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="a9072-210">Võimalik, et te ei pea samme 6, 7 ja/või 8 läbima, kuna ühe suvandi ekraanid jäetakse vahele.</span><span class="sxs-lookup"><span data-stu-id="a9072-210">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="a9072-211">Kui olete vaates **Keskkonna parameetrid**, kinnitage, et tekst **Dynamics 365 Commerce (eelvaade) – demo (10.0.* x* platvormi värskendus *xx*)\*\* kuvatakse otse välja **Keskkonna nimi** kohal.</span><span class="sxs-lookup"><span data-stu-id="a9072-211">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="a9072-212">Üksikasju vt jooniselt, mis kuvatakse pärast sammu 8.</span><span class="sxs-lookup"><span data-stu-id="a9072-212">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="a9072-213">Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="a9072-213">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="a9072-214">Valige suvand **Lisa** keskkonna lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="a9072-214">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="a9072-215">Väljal **Rakenduse versioon** valige uusim versioon.</span><span class="sxs-lookup"><span data-stu-id="a9072-215">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="a9072-216">Kui teil on konkreetne vajadus valida rakenduse versioon, mis ei ole kõige uuem versioon, ärge valige varasemat versiooni kui **10.0.8**.</span><span class="sxs-lookup"><span data-stu-id="a9072-216">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="a9072-217">Kasutage väljal **Platvormi versioon** platvormi versiooni, mis valitakse automaatselt valitud rakenduse versiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="a9072-217">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Rakenduse ja platvormi versioonide valimine](./media/project1.png)

1. <span data-ttu-id="a9072-219">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="a9072-219">Select **Next**.</span></span>
1. <span data-ttu-id="a9072-220">Valige keskkonna topoloogiaks **Demo**.</span><span class="sxs-lookup"><span data-stu-id="a9072-220">Select **Demo** as the environment topology.</span></span>

    ![Keskkonna topoloogia valimine 1](./media/project2.png)

1. <span data-ttu-id="a9072-222">Valige keskkonna topoloogiaks **Dynamics 365 Commerce – Demo**.</span><span class="sxs-lookup"><span data-stu-id="a9072-222">Select **Dynamics 365 Commerce - Demo** as the environment topology.</span></span> <span data-ttu-id="a9072-223">Kui olete varem konfigureerinud ühe Azure’i konnektori, kasutatakse seda selles keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="a9072-223">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="a9072-224">Mitme Azure’i konnektori konfigureerimisel saate valida, millist konnektorit kasutada: **Ida-USA**, **Ida-USA**2 **, Lääne-USA** või **Lääne-USA 2**.</span><span class="sxs-lookup"><span data-stu-id="a9072-224">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="a9072-225">(Parima lõppeesmärgini jõudluse saavutamiseks soovitame valida **Lääne-USA 2**.)</span><span class="sxs-lookup"><span data-stu-id="a9072-225">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Keskkonna topoloogia valimine 2](./media/project3.png)

1. <span data-ttu-id="a9072-227">Lehel **Keskkonna juurutamine** sisestage keskkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="a9072-227">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="a9072-228">Jätke täpsemad sätted nii nagu need on.</span><span class="sxs-lookup"><span data-stu-id="a9072-228">Leave the advanced settings as they are.</span></span>

    ![Keskkonna juurutamise leht](./media/project4.png)

1. <span data-ttu-id="a9072-230">Kohandage VM-i suurust vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="a9072-230">Adjust the VM size as required.</span></span> <span data-ttu-id="a9072-231">(Soovitame VM-i varude arvestusühikut \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="a9072-231">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="a9072-232">Vaadake üle hinnakujunduse ja litsentsimise tingimused ning märkige ruut, et näidata, et olete nendega nõus.</span><span class="sxs-lookup"><span data-stu-id="a9072-232">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="a9072-233">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="a9072-233">Select **Next**.</span></span>
1. <span data-ttu-id="a9072-234">Juurutamise kinnituse lehel kinnitage, et üksikasjad oleksid õiged ja valige seejärel nupp **Juuruta**.</span><span class="sxs-lookup"><span data-stu-id="a9072-234">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="a9072-235">Olete naasnud vaatesse **Pilve majutatud keskkonnad** ja teie keskkond peaks ilmuma loendis.</span><span class="sxs-lookup"><span data-stu-id="a9072-235">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="a9072-236">Teie soovitud keskkond ilmub järjekorras ja seejärel juurutatakse.</span><span class="sxs-lookup"><span data-stu-id="a9072-236">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="a9072-237">Keskkonna töövoogude lõpule viimine võtab aega.</span><span class="sxs-lookup"><span data-stu-id="a9072-237">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="a9072-238">Seetõttu kontrollige umbes kuue kuni üheksa tunni pärast uuesti.</span><span class="sxs-lookup"><span data-stu-id="a9072-238">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="a9072-239">Enne jätkamist veenduge, et teie keskkonna olek oleks **Juurutatud**.</span><span class="sxs-lookup"><span data-stu-id="a9072-239">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-csu"></a><span data-ttu-id="a9072-240">Kaubanduse skaala üksuse (Commerce Scale Unit, CSU) lähtestamine</span><span class="sxs-lookup"><span data-stu-id="a9072-240">Initialize the commerce scale unit (CSU)</span></span>

<span data-ttu-id="a9072-241">CSU-i lähtestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a9072-241">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="a9072-242">Vaates **Pilve majutatud keskkonnad** valige loendist oma keskkond.</span><span class="sxs-lookup"><span data-stu-id="a9072-242">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="a9072-243">Valige paremal olevast keskkonna vaatest **Täielik teave**.</span><span class="sxs-lookup"><span data-stu-id="a9072-243">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="a9072-244">Ilmub keskkonna üksikasjade vaade.</span><span class="sxs-lookup"><span data-stu-id="a9072-244">The environment details view appears.</span></span>
1. <span data-ttu-id="a9072-245">Jaotises **Keskkonna funktsioonid** valige käsk **Halda**.</span><span class="sxs-lookup"><span data-stu-id="a9072-245">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="a9072-246">Vahekaardil **Kaubandus** valige käsk **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="a9072-246">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="a9072-247">Ilmub CSU lähtestamise parameetrite vaade.</span><span class="sxs-lookup"><span data-stu-id="a9072-247">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="a9072-248">Väljal **Regioon** valige **Ida-USA**, **Ida-USA 2**, **Lääne-USA** või **Lääne-USA 2**.</span><span class="sxs-lookup"><span data-stu-id="a9072-248">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="a9072-249">Väljal **Versioon** valige loendist suvand **Määra versioon** ja määrake seejärel kuvataval väljal **9.18.20014.4**.</span><span class="sxs-lookup"><span data-stu-id="a9072-249">In the **Version** field, select **Specify a version** in the list, and then specify **9.18.20014.4** in the field that appears.</span></span> <span data-ttu-id="a9072-250">Määrake kindlasti siin näidatud täpne versioon.</span><span class="sxs-lookup"><span data-stu-id="a9072-250">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="a9072-251">Vastasel juhul peate uuendama RCSU hiljem õigele versioonile.</span><span class="sxs-lookup"><span data-stu-id="a9072-251">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="a9072-252">Lülitage suvand **Rakenda laiend** sisse.</span><span class="sxs-lookup"><span data-stu-id="a9072-252">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="a9072-253">Laiendite loendist valige suvand **Kaubanduse eelvaate demobaasi laiend**.</span><span class="sxs-lookup"><span data-stu-id="a9072-253">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="a9072-254">Valige **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="a9072-254">Select **Initialize**.</span></span>
1. <span data-ttu-id="a9072-255">Juurutamise kinnituse lehel kinnitage, et üksikasjad oleksid õiged ja valige seejärel nupp **Jah**.</span><span class="sxs-lookup"><span data-stu-id="a9072-255">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="a9072-256">Vaade **Kaubanduse haldus** kuvatakse uuesti, kus vahekaart **Kaubandus** on valitud.</span><span class="sxs-lookup"><span data-stu-id="a9072-256">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="a9072-257">Teie CSU on ettevalmistamiseks ootele pandud.</span><span class="sxs-lookup"><span data-stu-id="a9072-257">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="a9072-258">Enne jätkamist veenduge, et teie CSU olek oleks **Õnnestus**.</span><span class="sxs-lookup"><span data-stu-id="a9072-258">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="a9072-259">Lähtestamiseks kulub umbes kaks kuni viis tundi.</span><span class="sxs-lookup"><span data-stu-id="a9072-259">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="a9072-260">E-kaubanduse lähtestamine</span><span class="sxs-lookup"><span data-stu-id="a9072-260">Initialize e-Commerce</span></span>

<span data-ttu-id="a9072-261">E-kaubanduse lähtestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a9072-261">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="a9072-262">Vahekaardil **E-kaubandus** vaadake üle eelvaate nõusolek ja seejärel valige suvand **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="a9072-262">On the **e-Commerce** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="a9072-263">Väljale **E-kaubanduse rentniku nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="a9072-263">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="a9072-264">Võtke siiski arvesse, et see nimi on nähtav mõnes URL-is, mis viitavad teie e-kaubanduse eksemplarile.</span><span class="sxs-lookup"><span data-stu-id="a9072-264">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="a9072-265">Väljal **Kaubanduse skaala üksuse nimi** valige loendist oma CSU.</span><span class="sxs-lookup"><span data-stu-id="a9072-265">In the **Commerce scale unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="a9072-266">(Loendis peaks olema ainult üks valik.)</span><span class="sxs-lookup"><span data-stu-id="a9072-266">(The list should have only one option.)</span></span>

    <span data-ttu-id="a9072-267">Väli **E-kaubanduse geograafia** väli määratakse automaatselt ja väärtust ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="a9072-267">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="a9072-268">Jätkamiseks valige nupp **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="a9072-268">Select **Next** to continue.</span></span>
1. <span data-ttu-id="a9072-269">Väljale **Toetatud hostinimed** mis tahes kehtiv domeen, nt `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="a9072-269">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="a9072-270">Väljale **AAD süsteemi administraatori turberühm** sisestage selle turberühma nime esimesed tähed, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="a9072-270">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="a9072-271">Otsingutulemuste kuvamiseks valige suurendusklaasi ikoon.</span><span class="sxs-lookup"><span data-stu-id="a9072-271">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="a9072-272">Valige loendist õige turberühm.</span><span class="sxs-lookup"><span data-stu-id="a9072-272">Select the correct security group from the list.</span></span>
2.  <span data-ttu-id="a9072-273">Väljale **AAD hinnangute ja arvustuse moderaatori turberühm** sisestage selle turberühma nime esimesed tähed, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="a9072-273">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="a9072-274">Otsingutulemuste kuvamiseks valige suurendusklaasi ikoon.</span><span class="sxs-lookup"><span data-stu-id="a9072-274">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="a9072-275">Valige loendist õige turberühm.</span><span class="sxs-lookup"><span data-stu-id="a9072-275">Select the correct security group from the list.</span></span>
1. <span data-ttu-id="a9072-276">Jätke suvand **Hinnangute ja arvustuste teenuse häälestuse lubamine** sisselülitatuks.</span><span class="sxs-lookup"><span data-stu-id="a9072-276">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="a9072-277">Valige **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="a9072-277">Select **Initialize**.</span></span> <span data-ttu-id="a9072-278">Vaade **Kaubanduse haldus** kuvatakse uuesti, kus vahekaart **e-kaubandus** on valitud.</span><span class="sxs-lookup"><span data-stu-id="a9072-278">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="a9072-279">E-kaubanduse lähtestamine on käivitatud.</span><span class="sxs-lookup"><span data-stu-id="a9072-279">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="a9072-280">Enne jätkamist oodake, kuni teie e-kaubanduse lähtestamise olek on **Lähtestamine edukas**.</span><span class="sxs-lookup"><span data-stu-id="a9072-280">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="a9072-281">All paremal jaotises **Lingid** märkige järgmiste linkide URL-id:</span><span class="sxs-lookup"><span data-stu-id="a9072-281">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="a9072-282">**E-kaubanduse sait** – link teie e-kaubanduse saidi juurele.</span><span class="sxs-lookup"><span data-stu-id="a9072-282">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="a9072-283">**E-kaubanduse saidi haldustööriist** – link saidi halduse tööriistale.</span><span class="sxs-lookup"><span data-stu-id="a9072-283">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="a9072-284">Commerce’i eelvaatekeskkonna tugi</span><span class="sxs-lookup"><span data-stu-id="a9072-284">Commerce preview environment support</span></span>

<span data-ttu-id="a9072-285">Kui teil tekib ettevalmistuse etappide lõpetamisel probleeme, külastage abi saamiseks [Rakenduse Microsoft Dynamics 365 Commerce eelvaate Yammeri gruppi](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="a9072-285">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a9072-286">Järgmised etapid</span><span class="sxs-lookup"><span data-stu-id="a9072-286">Next steps</span></span>

<span data-ttu-id="a9072-287">Oma Commerce’i eelvaatekeskkonna ettevalmistamise ja konfigueerimise protsessi jätkamiseks vaadake teemat [Commerce’i eelvaatekeskkonna konfigureerimine](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="a9072-287">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a9072-288">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a9072-288">Additional resources</span></span>

[<span data-ttu-id="a9072-289">Dynamics 365 Commerce’i eelvaatekeskkonna ülevaade</span><span class="sxs-lookup"><span data-stu-id="a9072-289">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="a9072-290">Dynamics 365 Commerce’i eelvaatekeskkonna konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="a9072-290">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="a9072-291">Dynamics 365 Commerce’i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="a9072-291">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="a9072-292">Dynamics 365 Commerce eelvaatekeskkonna KKK</span><span class="sxs-lookup"><span data-stu-id="a9072-292">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="a9072-293">Microsofti elutsükli teenused (LCS)</span><span class="sxs-lookup"><span data-stu-id="a9072-293">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="a9072-294">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="a9072-294">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="a9072-295">Microsoft Azure'i portaal</span><span class="sxs-lookup"><span data-stu-id="a9072-295">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="a9072-296">Dynamics 365 Commerce veebisait</span><span class="sxs-lookup"><span data-stu-id="a9072-296">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

