---
title: Dynamics 365 Commerce'i hindamiskeskkonna ettevalmistamine
description: Selles teemas selgitatakse, kuidas valmistada ette Microsoft Dynamics 365 Commerce’i hindamiskeskkond.
author: psimolin
manager: annbe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8cda79a6be1aca7ad3826b9409e110524e6560e3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969897"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="3b737-103">Dynamics 365 Commerce'i hindamiskeskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="3b737-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3b737-104">Selles teemas selgitatakse, kuidas valmistada ette Microsoft Dynamics 365 Commerce’i hindamiskeskkond.</span><span class="sxs-lookup"><span data-stu-id="3b737-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="3b737-105">Enne alustamist soovitame teil see teema kiiresti läbi vaadata, et saada protsessi nõudmistest aimu.</span><span class="sxs-lookup"><span data-stu-id="3b737-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="3b737-106">Commerce'i hindamiskeskkonnad pole üldiselt kättesaadavad ja antakse partneritele ning klientidele taotluse alusel.</span><span class="sxs-lookup"><span data-stu-id="3b737-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="3b737-107">Lisateabe saamiseks pöörduge oma Microsofti partneri kontakti poole.</span><span class="sxs-lookup"><span data-stu-id="3b737-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="3b737-108">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="3b737-108">Overview</span></span>

<span data-ttu-id="3b737-109">Oma Commerce’i hindamiskeskkonna edukaks ettevalmistamiseks peate looma projekti, millel on kindel toote nimi ja tüüp.</span><span class="sxs-lookup"><span data-stu-id="3b737-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="3b737-110">Keskkonnal ja Commerce Scale Unitil (CSU) on samuti mõned konkreetsed parameetrid, mida peate kasutama, kui loodate hiljem e-kaubandust ette valmistada.</span><span class="sxs-lookup"><span data-stu-id="3b737-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="3b737-111">Selle teema juhised kirjeldavad kõiki vajalikke etappe, mida on vaja ettevalmistamise lõpuleviimiseks, ja milliseid parameetreid peate kasutama.</span><span class="sxs-lookup"><span data-stu-id="3b737-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="3b737-112">Pärast seda, kui olete oma Commerce’i hindamiskeskkonna edukalt ette valmistanud, peate viima lõpule mõned ettevalmistamisjärgsed etapid selle kasutamiseks valmistumiseks.</span><span class="sxs-lookup"><span data-stu-id="3b737-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="3b737-113">Mõned etapid on valikulised, olenevalt sellest, milliseid süsteemi aspekte soovite hinnata.</span><span class="sxs-lookup"><span data-stu-id="3b737-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="3b737-114">Võite valikulised etapid alati hiljem läbida.</span><span class="sxs-lookup"><span data-stu-id="3b737-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="3b737-115">Teavet selle kohta, kuidas Commerce’i hindamiskeskkonda pärast ettevalmistamist konfigureerida, vaadake teemast [Commerce’i hindamiskeskkonna konfigureerimine](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="3b737-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="3b737-116">Teavet selle kohta, kuidas Commerce’i hindamiskeskkonna valikulisi funktsioone konfigureerida, vaadake teemast [Commerce’i hindamiskeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="3b737-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3b737-117">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="3b737-117">Prerequisites</span></span>

<span data-ttu-id="3b737-118">Enne Commerce’i hindamiskeskkonna ettevalmistamist peavad olema kehtestatud järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="3b737-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="3b737-119">Teid on teavitatud hindamisprogrammist ja teile on antud hindamiskeskkonna suutlikkus.</span><span class="sxs-lookup"><span data-stu-id="3b737-119">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="3b737-120">Teil on juurdepääs Microsoft Dynamicsi portaalile Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3b737-120">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="3b737-121">Olete olemasolev Microsoft Dynamics 365 partner või klient ja olete võimeline looma Dynamics 365 Commerce’i projekti.</span><span class="sxs-lookup"><span data-stu-id="3b737-121">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="3b737-122">Teil on administraatori juurdepääs Microsoft Azure'i kordustellimusele või teil on võimalik võtta ühendust kordustellimuse administraatoriga, kes saab vajadusel teid abistada.</span><span class="sxs-lookup"><span data-stu-id="3b737-122">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="3b737-123">Teie Azure Active Directory (Azure AD) rentniku ID on saadaval.</span><span class="sxs-lookup"><span data-stu-id="3b737-123">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="3b737-124">Olete loonud Azure AD turberühma, mida saab kasutada e-kaubanduse süsteemiadministraatorite grupina ja mille ID on saadaval.</span><span class="sxs-lookup"><span data-stu-id="3b737-124">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="3b737-125">Olete loonud Azure AD turberühma, mida saab kasutada hinnangute ja arvustuste moderaatori grupina ja mille ID on saadaval.</span><span class="sxs-lookup"><span data-stu-id="3b737-125">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="3b737-126">(See turberühm võib olla sama, mis e-kaubanduse süsteemiadministraatorite grupp.)</span><span class="sxs-lookup"><span data-stu-id="3b737-126">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="3b737-127">Pange tähele, et see loend pole ammendav.</span><span class="sxs-lookup"><span data-stu-id="3b737-127">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="3b737-128">Kui teil ilmneb mõni probleem, peaksite abi saamiseks pöörduma oma Microsofti partneri kontakti poole.</span><span class="sxs-lookup"><span data-stu-id="3b737-128">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="3b737-129">Oma Commerce’i hindamiskeskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="3b737-129">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="3b737-130">Need protseduurid selgitavad, kuidas valmistada ette Commerce’i hindamiskeskkonda.</span><span class="sxs-lookup"><span data-stu-id="3b737-130">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="3b737-131">Pärast nende edukat lõpule viimist on Commerce’i hindamiskeskkond konfigureerimiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="3b737-131">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="3b737-132">Kõik siin kirjeldatud tegevused esinevad LCS portaalis.</span><span class="sxs-lookup"><span data-stu-id="3b737-132">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="3b737-133">Loo uus projekt</span><span class="sxs-lookup"><span data-stu-id="3b737-133">Create a new project</span></span>

<span data-ttu-id="3b737-134">LCS-is uue projekti loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="3b737-134">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="3b737-135">LCS-i avalehel valige projekti loomiseks plussmärk (**+**).</span><span class="sxs-lookup"><span data-stu-id="3b737-135">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="3b737-136">Parempoolsel paanil järgige ühte järgmistest etappidest.</span><span class="sxs-lookup"><span data-stu-id="3b737-136">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="3b737-137">Kui olete partner, valige suvand **Migreerimine, lahenduste loomine ja teave**.</span><span class="sxs-lookup"><span data-stu-id="3b737-137">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="3b737-138">Kui olete klient, valige suvand **Potentsiaalsed eelmüügid**.</span><span class="sxs-lookup"><span data-stu-id="3b737-138">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="3b737-139">Sisestage nimi, kirjeldus ja valdkond.</span><span class="sxs-lookup"><span data-stu-id="3b737-139">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="3b737-140">Valige väljal **Toote nimi** suvand **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="3b737-140">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="3b737-141">Valige väljal **Toote versioon** suvand **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="3b737-141">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="3b737-142">Väljal **Metoodika** valige **Dynamics Retail juurutamise metoodika**.</span><span class="sxs-lookup"><span data-stu-id="3b737-142">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="3b737-143">Valikuline: võite portida rollid ja kasutajad olemasolevast projektist.</span><span class="sxs-lookup"><span data-stu-id="3b737-143">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="3b737-144">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="3b737-144">Select **Create**.</span></span> <span data-ttu-id="3b737-145">Kuvatakse projekti vaade.</span><span class="sxs-lookup"><span data-stu-id="3b737-145">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="3b737-146">Azure’i konnektori lisamine</span><span class="sxs-lookup"><span data-stu-id="3b737-146">Add the Azure Connector</span></span>

<span data-ttu-id="3b737-147">Azure'i konnektori lisamiseks oma LCS-i projekti, järgige etappe teemas [Azure Resource Manageri (ARM) sisseelamisprotsessi lõpule viimine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="3b737-147">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="3b737-148">Keskkonna juurutamine</span><span class="sxs-lookup"><span data-stu-id="3b737-148">Deploy the environment</span></span>

<span data-ttu-id="3b737-149">Keskkonna juurutamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3b737-149">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="3b737-150">Võimalik, et te ei pea samme 6, 7 ja/või 8 läbima, kuna ühe suvandi ekraanid jäetakse vahele.</span><span class="sxs-lookup"><span data-stu-id="3b737-150">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="3b737-151">Kui olete vaates **Keskkonna parameetrid**, kinnitage, et tekst **Dynamics 365 Commerce (eelvaade) – demo (10.0.* x* platvormi värskendus *xx*)\*\* kuvatakse otse välja **Keskkonna nimi** kohal.</span><span class="sxs-lookup"><span data-stu-id="3b737-151">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="3b737-152">Üksikasju vt jooniselt, mis kuvatakse pärast sammu 8.</span><span class="sxs-lookup"><span data-stu-id="3b737-152">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="3b737-153">Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="3b737-153">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="3b737-154">Valige suvand **Lisa** keskkonna lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="3b737-154">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="3b737-155">Väljal **Rakenduse versioon** valige uusim versioon.</span><span class="sxs-lookup"><span data-stu-id="3b737-155">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="3b737-156">Kui teil on konkreetne vajadus valida rakenduse versioon, mis ei ole kõige uuem versioon, ärge valige varasemat versiooni kui **10.0.14**.</span><span class="sxs-lookup"><span data-stu-id="3b737-156">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="3b737-157">Kasutage väljal **Platvormi versioon** platvormi versiooni, mis valitakse automaatselt valitud rakenduse versiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="3b737-157">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Rakenduse ja platvormi versioonide valimine](./media/project1.png)

1. <span data-ttu-id="3b737-159">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="3b737-159">Select **Next**.</span></span>
1. <span data-ttu-id="3b737-160">Valige keskkonna topoloogiaks **Demo**.</span><span class="sxs-lookup"><span data-stu-id="3b737-160">Select **Demo** as the environment topology.</span></span>

    ![Keskkonna topoloogia valimine 1](./media/project2.png)

1. <span data-ttu-id="3b737-162">Lehel **Keskkonna juurutamine** sisestage keskkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="3b737-162">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="3b737-163">Jätke täpsemad sätted nii nagu need on.</span><span class="sxs-lookup"><span data-stu-id="3b737-163">Leave the advanced settings as they are.</span></span>

    ![Keskkonna juurutamise leht](./media/project4.png)

1. <span data-ttu-id="3b737-165">Kohandage VM-i suurust vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="3b737-165">Adjust the VM size as required.</span></span> <span data-ttu-id="3b737-166">(Soovitame VM-i varude arvestusühikut \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="3b737-166">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="3b737-167">Vaadake üle hinnakujunduse ja litsentsimise tingimused ning märkige ruut, et näidata, et olete nendega nõus.</span><span class="sxs-lookup"><span data-stu-id="3b737-167">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="3b737-168">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="3b737-168">Select **Next**.</span></span>
1. <span data-ttu-id="3b737-169">Juurutamise kinnituse lehel kinnitage, et üksikasjad oleksid õiged ja valige seejärel nupp **Juuruta**.</span><span class="sxs-lookup"><span data-stu-id="3b737-169">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="3b737-170">Olete naasnud vaatesse **Pilve majutatud keskkonnad** ja teie keskkond peaks ilmuma loendis.</span><span class="sxs-lookup"><span data-stu-id="3b737-170">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="3b737-171">Teie soovitud keskkond ilmub järjekorras ja seejärel juurutatakse.</span><span class="sxs-lookup"><span data-stu-id="3b737-171">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="3b737-172">Keskkonna töövoogude lõpule viimine võtab aega.</span><span class="sxs-lookup"><span data-stu-id="3b737-172">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="3b737-173">Seetõttu kontrollige umbes kuue kuni üheksa tunni pärast uuesti.</span><span class="sxs-lookup"><span data-stu-id="3b737-173">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="3b737-174">Enne jätkamist veenduge, et teie keskkonna olek oleks **Juurutatud**.</span><span class="sxs-lookup"><span data-stu-id="3b737-174">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="3b737-175">Commerce Scale Uniti (pilv) lähtestamine</span><span class="sxs-lookup"><span data-stu-id="3b737-175">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="3b737-176">CSU lähtestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3b737-176">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="3b737-177">Vaates **Pilve majutatud keskkonnad** valige loendist oma keskkond.</span><span class="sxs-lookup"><span data-stu-id="3b737-177">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="3b737-178">Valige paremal olevast keskkonna vaatest **Täielik teave**.</span><span class="sxs-lookup"><span data-stu-id="3b737-178">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="3b737-179">Ilmub keskkonna üksikasjade vaade.</span><span class="sxs-lookup"><span data-stu-id="3b737-179">The environment details view appears.</span></span>
1. <span data-ttu-id="3b737-180">Jaotises **Keskkonna funktsioonid** valige käsk **Halda**.</span><span class="sxs-lookup"><span data-stu-id="3b737-180">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="3b737-181">Vahekaardil **Kaubandus** valige käsk **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="3b737-181">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="3b737-182">Ilmub CSU lähtestamise parameetrite vaade.</span><span class="sxs-lookup"><span data-stu-id="3b737-182">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="3b737-183">Valige väljal **Piirkond** see piirkond, mis on sama või asub selle piirkonna lähedal, kuhu te keskkonna juurutasite.</span><span class="sxs-lookup"><span data-stu-id="3b737-183">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="3b737-184">Ärge muutke välja **Versioon**.</span><span class="sxs-lookup"><span data-stu-id="3b737-184">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="3b737-185">Valige **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="3b737-185">Select **Initialize**.</span></span>
1. <span data-ttu-id="3b737-186">Juurutamise kinnituse lehel kinnitage, et üksikasjad oleksid õiged ja valige seejärel nupp **Jah**.</span><span class="sxs-lookup"><span data-stu-id="3b737-186">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="3b737-187">Vaade **Kaubanduse haldus** kuvatakse uuesti, kus vahekaart **Kaubandus** on valitud.</span><span class="sxs-lookup"><span data-stu-id="3b737-187">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="3b737-188">Teie CSU on ettevalmistamiseks ootele pandud.</span><span class="sxs-lookup"><span data-stu-id="3b737-188">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="3b737-189">Enne jätkamist veenduge, et teie CSU olek oleks **Õnnestus**.</span><span class="sxs-lookup"><span data-stu-id="3b737-189">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="3b737-190">Lähtestamiseks kulub umbes kaks kuni viis tundi.</span><span class="sxs-lookup"><span data-stu-id="3b737-190">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="3b737-191">Kui te ei leia keskkonna üksikasjade vaates linki **Halda**, võtke abi saamiseks ühendust oma Microsofti kontaktiga.</span><span class="sxs-lookup"><span data-stu-id="3b737-191">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="3b737-192">Juurutamisprotsessi käigus võite saada järgmise tõrketeate.</span><span class="sxs-lookup"><span data-stu-id="3b737-192">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="3b737-193">Hindamiskeskkonnad (demo/test) peavad peakontoris registreerima skaalaüksuse konnektori rakenduse \<application ID\>.</span><span class="sxs-lookup"><span data-stu-id="3b737-193">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="3b737-194">Kui CSU lähtestamine nurjub ja te saate selle tõrketeate, tehke märkus rakenduse ID kohta, mis on globaalne ainuidentifikaator (GUID) ja seejärel järgige järgmise jaotise etappe CSU juurutamise rakenduse registreerimiseks Commerce'i peakontoris.</span><span class="sxs-lookup"><span data-stu-id="3b737-194">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="3b737-195">CSU juurutuse rakenduse registreerimine Commerce peakontoris (vajadusel)</span><span class="sxs-lookup"><span data-stu-id="3b737-195">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="3b737-196">CSU juurutuse rakenduse registreerimiseks Commerce'i peakontoris toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="3b737-196">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="3b737-197">Avage Commerce'i peakontoris **Süsteemihaldus \> Seadistus \> Azure Active Directory rakendused**.</span><span class="sxs-lookup"><span data-stu-id="3b737-197">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="3b737-198">Sisestage veergu **Kliendi ID** rakenduse ID saadud CSU lähtestamise tõrketeatest.</span><span class="sxs-lookup"><span data-stu-id="3b737-198">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="3b737-199">Sisestage veergu **Nimi** mistahes kirjeldav tekst (nt **CSU hinnang**).</span><span class="sxs-lookup"><span data-stu-id="3b737-199">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="3b737-200">Sisestage veergu **Kasutaja ID** väärtus **RetailServiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="3b737-200">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="3b737-201">Proovige CSU lähtestamist ja LCS-i juurutamist uuesti.</span><span class="sxs-lookup"><span data-stu-id="3b737-201">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="3b737-202">E-kaubanduse lähtestamine</span><span class="sxs-lookup"><span data-stu-id="3b737-202">Initialize e-Commerce</span></span>

<span data-ttu-id="3b737-203">E-kaubanduse lähtestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3b737-203">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="3b737-204">Vahekaardil **E-kaubandus** vaadake üle hindamise nõusolek ja seejärel valige suvand **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="3b737-204">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="3b737-205">Sisestage nimi väljale **E-kaubanduse keskkonna nimi**.</span><span class="sxs-lookup"><span data-stu-id="3b737-205">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="3b737-206">Võtke arvesse, et see nimi on nähtav mõnes URL-is, mis viitavad teie e-kaubanduse eksemplarile.</span><span class="sxs-lookup"><span data-stu-id="3b737-206">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="3b737-207">Väljal **Commerce Scale Uniti nimi** valige loendist oma CSU.</span><span class="sxs-lookup"><span data-stu-id="3b737-207">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="3b737-208">(Loendis peaks olema ainult üks valik.)</span><span class="sxs-lookup"><span data-stu-id="3b737-208">(The list should have only one option.)</span></span>

    <span data-ttu-id="3b737-209">Väli **E-kaubanduse geograafia** määratakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="3b737-209">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="3b737-210">Jätkamiseks valige nupp **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="3b737-210">Select **Next** to continue.</span></span>
1. <span data-ttu-id="3b737-211">Väljale **Toetatud hostinimed** mis tahes kehtiv domeen, nt `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="3b737-211">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="3b737-212">Sisestage väljale **AAD turberühm süsteemiadministraatorile** turberühma nime paar esimest tähemärki, mida soovite kasutada, ja seejärel valige suurendusklaasi sümbol otsingutulemuste kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="3b737-212">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="3b737-213">Valige loendist õige turberühm.</span><span class="sxs-lookup"><span data-stu-id="3b737-213">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="3b737-214">Sisestage väljale **AAD turberühm hinnangute ja arvustuse moderaatorile** turberühma nime paar esimest tähemärki, mida soovite kasutada, ja seejärel valige suurendusklaasi sümbol otsingutulemuste kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="3b737-214">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="3b737-215">Valige loendist õige turberühm.</span><span class="sxs-lookup"><span data-stu-id="3b737-215">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="3b737-216">Jätke suvandi **Hinnangute ja arvustuse teenuse lubamine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="3b737-216">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="3b737-217">Valige **Lähtesta**.</span><span class="sxs-lookup"><span data-stu-id="3b737-217">Select **Initialize**.</span></span> <span data-ttu-id="3b737-218">Vaade **Kaubanduse haldus** kuvatakse uuesti, kus vahekaart **e-kaubandus** on valitud.</span><span class="sxs-lookup"><span data-stu-id="3b737-218">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="3b737-219">E-kaubanduse lähtestamine on käivitatud.</span><span class="sxs-lookup"><span data-stu-id="3b737-219">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="3b737-220">Enne jätkamist oodake, kuni teie e-kaubanduse lähtestamise olek on **Lähtestamine edukas**.</span><span class="sxs-lookup"><span data-stu-id="3b737-220">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="3b737-221">All paremal jaotises **Lingid** märkige järgmiste linkide URL-id:</span><span class="sxs-lookup"><span data-stu-id="3b737-221">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="3b737-222">**E-kaubanduse sait** – link teie e-kaubanduse saidi juurele.</span><span class="sxs-lookup"><span data-stu-id="3b737-222">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="3b737-223">**E-kaubanduse saidiehitaja** – link saidi halduse tööriistale.</span><span class="sxs-lookup"><span data-stu-id="3b737-223">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3b737-224">Järgmised etapid</span><span class="sxs-lookup"><span data-stu-id="3b737-224">Next steps</span></span>

<span data-ttu-id="3b737-225">Oma Commerce’i hindamiskeskkonna ettevalmistamise ja konfigueerimise protsessi jätkamiseks vaadake teemat [Commerce’i hindamiskeskkonna konfigureerimine](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="3b737-225">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b737-226">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3b737-226">Additional resources</span></span>

[<span data-ttu-id="3b737-227">Dynamics 365 Commerce'i hindamiskeskkonna ülevaade</span><span class="sxs-lookup"><span data-stu-id="3b737-227">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="3b737-228">Dynamics 365 Commerce'i hindamiskeskkonna konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="3b737-228">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="3b737-229">BOPIS-e konfigureerimine Dynamics 365 Commerce'i hindamiskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="3b737-229">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="3b737-230">Dynamics 365 Commerce'i hindamiskeskkonna valikuliste funktsioonide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="3b737-230">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="3b737-231">Dynamics 365 Commerce'i hindamiskeskkonna KKK</span><span class="sxs-lookup"><span data-stu-id="3b737-231">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="3b737-232">Microsofti elutsükli teenused (LCS)</span><span class="sxs-lookup"><span data-stu-id="3b737-232">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="3b737-233">Commerce Scale Unit (pilv)</span><span class="sxs-lookup"><span data-stu-id="3b737-233">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="3b737-234">Microsoft Azure'i portaal</span><span class="sxs-lookup"><span data-stu-id="3b737-234">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="3b737-235">Dynamics 365 Commerce veebisait</span><span class="sxs-lookup"><span data-stu-id="3b737-235">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
