---
title: Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas
description: Selle teema all kirjeldatakse, millal ja kuidas seadistada kanali kohta mitme Microsoft Azure Active Directory (Azure AD) äri-tarbija (B2C) üürnikut kasutaja autentimiseks spetsiaalses Dynamics 365 Commerce keskkonnas .
author: BrianShook
manager: annbe
ms.date: 03/02/2020
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
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: da27e3ed0a0e50126590609d09575befe17a7aa2
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517115"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a><span data-ttu-id="b4e5b-103">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="b4e5b-103">Configure multiple B2C tenants in a Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b4e5b-104">Selle teema all kirjeldatakse, millal ja kuidas seadistada kanali kohta mitme Microsoft Azure Active Directory (Azure AD) äri-tarbija (B2C) üürnikut kasutaja autentimiseks spetsiaalses Dynamics 365 Commerce keskkonnas .</span><span class="sxs-lookup"><span data-stu-id="b4e5b-104">This topic describes when and how to set up multiple Microsoft Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants per channel for user authentication in a dedicated Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="b4e5b-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="b4e5b-105">Overview</span></span>

<span data-ttu-id="b4e5b-106">Dynamics 365 Commerce kasutab Azure AD B2C pilve identiteediteenust kasutaja mandaadi ja autentimisvoogude toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-106">Dynamics 365 Commerce uses the Azure AD B2C cloud identity service to support user credentials and authentication flows.</span></span> <span data-ttu-id="b4e5b-107">Kasutajad saavad kasutada autentimise voogusid, et registreeruda, sisse logida ja lähtestada oma parool.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-107">Users can use the authentication flows to sign up, sign in, and reset their password.</span></span> <span data-ttu-id="b4e5b-108">Azure AD B2C talletab kasutaja tundliku autentimisteabe, nt kasutajanime ja parooli.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-108">Azure AD B2C stores a user's sensitive authentication information, such as his or her user name and password.</span></span> <span data-ttu-id="b4e5b-109">Kasutajakirje on kordumatu iga B2C rentniku jaoks ja see kasutab kasutajanime (meiliaadressi) mandaate või sotsiaalse identiteedi pakkuja mandaati.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-109">The user record is unique to each B2C tenant, and it uses either user name (email address) credentials or social identity provider credentials.</span></span>

<span data-ttu-id="b4e5b-110">Enamikul juhtudel kasutatakse Kaubanduskeskkonnas Azure AD ühte B2C rentnikku.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-110">In most cases, a single Azure AD B2C tenant is used in a Commerce environment.</span></span> <span data-ttu-id="b4e5b-111">Kaubanduskliendid saavad seejärel luua ja avaldada mitu saiti samas Kaubanduskeskkonnas ja kõigil nendel saitidel kasutatakse sama kliendimandaati.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-111">Commerce customers can then create and publish multiple sites in the same Commerce environment, and the same customer credentials will be used across these sites.</span></span> <span data-ttu-id="b4e5b-112">Kui aga keskkonna saite käsitletakse erinevate kaubamärkidena ja need ilmuvad kasutajatele eraldiseisvate ettevõtetena, saab B2C rentnikku konfigureerida kanalile, mida kasutatakse saidi/kaubamärgi eristamiseks.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-112">However, if the sites in the environment should be treated as different brands and appear to users as separate businesses, a B2C tenant can be configured for the channel that is used for the site/brand separation.</span></span>

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a><span data-ttu-id="b4e5b-113">Kaalutlused mitme B2C rentniku seadistamiseks kanali kohta</span><span class="sxs-lookup"><span data-stu-id="b4e5b-113">Considerations when multiple B2C tenants are set up per channel</span></span>

<span data-ttu-id="b4e5b-114">Sageli, kui iga kanalit või saiti käsitletakse eraldiseisva ettevõttena, on parim valik, mis puudutab kasutaja autentimise voogusid Kaubanduses, kasutada eraldiseisvaid juriidilisi isikuid.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-114">Often, when each channel or site is being treated as a separate business, the best option with respect to user authentication flows in Commerce is to use separate legal entities.</span></span> <span data-ttu-id="b4e5b-115">Kui aga soovite hoida iga kanalit/saiti samas keskkonnas ja juriidilises isikus, kuid soovite iga saidi puhul eraldi kasutaja autentimist, peate enne jätkamist arvestama järgmiste punktidega:</span><span class="sxs-lookup"><span data-stu-id="b4e5b-115">However, if you want to keep each channel/site in the same environment and legal entity, but want to have separate user authentication for each site, it's important that you consider the following points before you proceed:</span></span>

- <span data-ttu-id="b4e5b-116">Kasutajatel on igal kanalil/saidil eraldi mandaat.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-116">Users will have their own distinct credentials for each channel/site.</span></span>

    <span data-ttu-id="b4e5b-117">Ühel isikul võib olla kaks eraldi kontot kanali/saidi kohta, sest iga konto on kordumatu sisend eraldi B2C rentnikusse.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-117">The same person can have two separate accounts per channel/site, because each account will be a unique entry into a separate B2C tenant.</span></span>

- <span data-ttu-id="b4e5b-118">Keskkonnas Microsoft Dynamics tagastatakse globaalsete kirjete otsingutel eraldi kliendikirjed.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-118">In the Microsoft Dynamics environment, separate customer records will be returned for global record searches.</span></span>

    <span data-ttu-id="b4e5b-119">Kui kasutaja kasutab sama meiliaadressi kõigil kanalitel/saitidel, tagastavad globaalse kliendiotsingu tulemused iga kanali/saidi kohta.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-119">If a user uses the same email address across channels/sites, global customer searches will return results for each channel/site.</span></span> <span data-ttu-id="b4e5b-120">(Kuvatakse kanali indikaator.)</span><span class="sxs-lookup"><span data-stu-id="b4e5b-120">(A channel indicator will be shown.)</span></span>

- <span data-ttu-id="b4e5b-121">Aadressiraamatut saab kasutada kasutajate rühmitamiseks, nii et neid saab jälgida kanalite kaupa.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-121">The address book can be used to help group users, so that they can be tracked per channel.</span></span>
- <span data-ttu-id="b4e5b-122">Kliendi kirjete arv kanali kohta võib suureneda ja see suurenemine võib mõjutada globaalse kliendiotsingu jõudlust.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-122">The number of customer records per channel might increase, and this increase might affect the performance of global customer searches.</span></span>
- <span data-ttu-id="b4e5b-123">B2C rentnikud peavad olema kanaliga hoolikalt vastendatud, et aidata vältida olukordi, kus kliendid registreerivad vale rentniku.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-123">B2C tenants must be carefully mapped to a channel, to help prevent situations where customers sign up for an incorrect tenant.</span></span> <span data-ttu-id="b4e5b-124">Vastasel juhul võib tekkida segadus või jälgimisprobleem.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-124">Otherwise, confusion or tracking issues can occur.</span></span>

<span data-ttu-id="b4e5b-125">Järgmisel joonisel on kujutatud mitut B2C rentnikku Kaubanduskeskkonnas.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-125">The following illustration shows multiple B2C tenants in a Commerce environment.</span></span>

![Mitu B2C rentnikku Kaubanduskeskkonnas](media/MultiB2C_In_Environment.png)

<span data-ttu-id="b4e5b-127">Kui otsustate, et teie ettevõte vajab kanali kohta eraldiseisvaid B2C rentnikke samas Kaubanduskeskkonnas, täitke selle funktsiooni taotlemiseks järgmiste jaotiste protseduurid.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-127">If you decide that your business requires distinct B2C tenants per channel in the same Commerce environment, complete the procedures in the following sections to request this feature.</span></span>

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a><span data-ttu-id="b4e5b-128">Soovin, et teie keskkonnas oleks lubatud B2C kanali kohta</span><span class="sxs-lookup"><span data-stu-id="b4e5b-128">Request that B2C per channel be enabled in your environment</span></span>

<span data-ttu-id="b4e5b-129">Praegu, kui soovite, et erinevad B2C rentnikud kanali kohta oleksid saadaval samas Kaubanduskeskkonnas, tuleb esitada taotlus Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-129">Currently, if you want distinct B2C tenants per channel to be available in the same Commerce environment, you must submit a request to Dynamics 365 Commerce.</span></span> <span data-ttu-id="b4e5b-130">Lisateabe saamiseks vt teemat [Hangi Lifecycle Servicesi (LCS) tugiteenus](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) või arutage seda probleemi oma Kaubanduslahenduste kontaktiga.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-130">For more information, see [Get support for Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md), or discuss this issue with your Commerce solutions contact.</span></span>

## <a name="configure-b2c-tenants-in-your-environment"></a><span data-ttu-id="b4e5b-131">B2C rentnike konfigureerimine oma keskkonnas</span><span class="sxs-lookup"><span data-stu-id="b4e5b-131">Configure B2C tenants in your environment</span></span>

<span data-ttu-id="b4e5b-132">B2C rentnike konfigureerimiseks oma keskkonnas täitke selle jaotise vastavad protseduurid.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-132">To configure B2C tenants in your environment, complete the relevant procedures in this section.</span></span>

### <a name="add-an-azure-ad-b2c-tenant"></a><span data-ttu-id="b4e5b-133">Lisa Azure AD B2C rentnik</span><span class="sxs-lookup"><span data-stu-id="b4e5b-133">Add an Azure AD B2C tenant</span></span>

<span data-ttu-id="b4e5b-134">Et lisada Azure AD B2C rentnik oma keskkonda, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-134">To add an Azure AD B2C tenant to your environment, follow these steps.</span></span>

1. <span data-ttu-id="b4e5b-135">Logige sisse oma keskkonna Kaubanduse saidiehitusse süsteemi administraatorina. Azure AD B2C rentnike konfigureerimiseks peate olema Kaubanduskeskkonna süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-135">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="b4e5b-136">Vasakpoolsel navigeerimispaanil valige suvand **Rentniku sätted** selle laiendamiseks.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-136">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="b4e5b-137">Valige **B2C sätted** ja seejärel valige **Halda**.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-137">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="b4e5b-138">Valige **Lisa B2C rakendus** ja siis sisestage järgmine teave:</span><span class="sxs-lookup"><span data-stu-id="b4e5b-138">Select **Add B2C Application**, and then enter the following information:</span></span>

    - <span data-ttu-id="b4e5b-139">**Rakenduse nimi**: sisestage nimi, mida tuleks rakenduse Kaubandus haldamise kontekstis kasutada.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-139">**Application Name**: Enter the name that should be used for the application in the context of managing it in Commerce.</span></span> <span data-ttu-id="b4e5b-140">Soovitame kasutada rakenduse nime, mille valisite, kui seadistasite Azure AD B2C rakenduse portaalis Azure.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-140">We recommend that you use the application name that you chose when you set up the Azure AD B2C application in the Azure portal.</span></span> <span data-ttu-id="b4e5b-141">Sel viisil saate aidata vähendada segadust, kui te haldate B2C rentnikke Kaubanduses.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-141">In this way, you can help reduce confusion when you manage B2C tenants in Commerce.</span></span>
    - <span data-ttu-id="b4e5b-142">**Rentniku nimi**: sisestage B2C rentniku nimi, nagu see kuvatakse portaalis Azure.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-142">**Tenant Name**: Enter the B2C tenant name as it appears in the Azure portal.</span></span>
    - <span data-ttu-id="b4e5b-143">**Unustatud parooli poliitika ID**: sisestage poliitika ID (portaali Azure poliitika nimi).</span><span class="sxs-lookup"><span data-stu-id="b4e5b-143">**Forget Password Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="b4e5b-144">**Registreerumise poliitika ID**: sisestage poliitika ID (portaali Azure poliitika nimi).</span><span class="sxs-lookup"><span data-stu-id="b4e5b-144">**Signup Signin Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="b4e5b-145">**Kliendi GUID**: sisestage Azure AD B2C rentniku ID, nagu see kuvatakse portaalis Azure (mitte B2C rentniku rakenduse ID).</span><span class="sxs-lookup"><span data-stu-id="b4e5b-145">**Client GUID**: Enter the Azure AD B2C tenant ID as it appears in the Azure portal (not the application ID for the B2C tenant).</span></span>
    - <span data-ttu-id="b4e5b-146">**Profiili redigeerimise poliitika ID**: sisestage poliitika ID (portaali Azure poliitika nimi).</span><span class="sxs-lookup"><span data-stu-id="b4e5b-146">**Edit Profile Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>

1. <span data-ttu-id="b4e5b-147">Kui olete selle teabe sisestamise lõpetanud, valige muudatuste salvestamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-147">When you've finished entering this information, select **OK** to save your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="b4e5b-148">Peaksite jätma tühjaks väljad **Ulatus**, **Mitteinteraktiivse poliitika ID**, **Mitteinteraktiivse kliendi ID**, **Sisselogimise kohandatud domeeni** ja **Registreerimise poliitika ID**, kui Dynamics 365 Commerce meeskond ei käsi teil neid seada.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-148">You should leave fields such as **Scope**, **Non Interactive Policy ID**, **Non Interactive Client ID**, **Login Custom Domain**, and **Sign Up Policy ID** blank unless the Dynamics 365 Commerce team instructs you to set them.</span></span>
<span data-ttu-id="b4e5b-149">Teie uus Azure AD B2C rentnik peaks nüüd ilmuma loendisse **B2C rakenduste haldamine**.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-149">Your new Azure AD B2C tenant should now appear in the list under **Manage B2C Applications**.</span></span>

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a><span data-ttu-id="b4e5b-150">Azure AD B2C rentniku haldamine või kustutamine</span><span class="sxs-lookup"><span data-stu-id="b4e5b-150">Manage or delete an Azure AD B2C tenant</span></span>

1. <span data-ttu-id="b4e5b-151">Logige sisse oma keskkonna Kaubanduse saidiehitusse süsteemi administraatorina. Azure AD B2C rentnike konfigureerimiseks peate olema Kaubanduskeskkonna süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-151">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="b4e5b-152">Vasakpoolsel navigeerimispaanil valige suvand **Rentniku sätted** selle laiendamiseks.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-152">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="b4e5b-153">Valige **B2C sätted** ja seejärel valige **Halda**.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-153">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="b4e5b-154">B2C rentniku redigeerimiseks valige selle kõrval olev pliiatsisümbol.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-154">To edit a B2C tenant, select the pencil symbol next to it.</span></span> <span data-ttu-id="b4e5b-155">B2C üürniku kustutamiseks valige selle kõrval prügikastisümbol.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-155">To delete a B2C tenant, select the trash can symbol next to it.</span></span>
1. <span data-ttu-id="b4e5b-156">Valige **Salvesta** ja seejärel valige muudatuste aktiveerimiseks käsk **Avalda** .</span><span class="sxs-lookup"><span data-stu-id="b4e5b-156">Select **Save**, and then select **Publish** to activate your changes.</span></span>

> [!WARNING]
> <span data-ttu-id="b4e5b-157">Kui B2C rentnik on konfigureeritud aktiivse/avaldatud saidi jaoks, võivad kasutajad olla registreerunud, kasutades rentniku kontosid.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-157">When a B2C tenant is configured for a live/published site, users might have signed up by using accounts that are present on the tenant.</span></span> <span data-ttu-id="b4e5b-158">Kui kustutate konfigureeritud rentniku **Rentniku sätete \> B2C rentniku** menüüs, eemaldate selle B2C rentniku seose saitidega, mis on seotud mis tahes selle rentniku kanalitega.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-158">If you delete a configured tenant on the **Tenant Settings \> B2C Tenant** menu, you remove the association of that B2C tenant from sites that are associated with any channels of the tenant.</span></span> <span data-ttu-id="b4e5b-159">Sel juhul ei saa teie kasutajad enam oma kontodele sisse logida.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-159">In this case, your users might no longer be able to sign in to their accounts.</span></span> <span data-ttu-id="b4e5b-160">Seetõttu olge äärmiselt ettevaatlikud, kui kustutate konfigureeritud rentniku.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-160">Therefore, use extreme caution when you delete a configured tenant.</span></span>
>
> <span data-ttu-id="b4e5b-161">Kui konfigureeritud rentnik on kustutatud, jätkatakse B2C rentniku ja kirjete säilitamist, kuid selle rentniku Kaubandussüsteemi konfiguratsioon muutub või eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-161">When a configured tenant is deleted, the B2C tenant and records will continue to be maintained, but the Commerce system configuration of that tenant will be changed or removed.</span></span> <span data-ttu-id="b4e5b-162">Kasutajad, kes proovivad registreeruda või saidile sisse logida, loovad uue kontokirje vaikimisi või äsja seotud B2C rentnikule, kes on konfigureeritud saidi kanalile.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-162">Users who try to sign up or sign in to the site will create a new account record in the default or newly associated B2C tenant that is configured for the channel of the site.</span></span>
## <a name="configure-your-channel-with-a-b2c-tenant"></a><span data-ttu-id="b4e5b-163">Kanali konfigureerimine B2C rentnikuga</span><span class="sxs-lookup"><span data-stu-id="b4e5b-163">Configure your channel with a B2C tenant</span></span>

1. <span data-ttu-id="b4e5b-164">Logige sisse oma keskkonna Kaubanduse saidiehitusse süsteemi administraatorina. Azure AD B2C rentnike konfigureerimiseks peate olema Kaubanduskeskkonna süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-164">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="b4e5b-165">Vasakpoolsel navigeerimispaanil valige suvand **Saidi sätted** selle laiendamiseks.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-165">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="b4e5b-166">Valige **Kanalid** ja siis valige konfigureerimiseks kanal.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-166">Select **Channels**, and then select the channel to configure.</span></span>
1. <span data-ttu-id="b4e5b-167">Valige parempoolsel omaduste paanil väljal **Vali B2C rakendus** selle kanali jaoks konfigureeritud Azure AD B2C rentnik.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-167">In the properties pane on the right, in the **Select B2C Application** field, select the configured Azure AD B2C tenant to use for this channel.</span></span>
1. <span data-ttu-id="b4e5b-168">Valige tegumiribal **Salvesta ja avalda**, et kinnitada uus või värskendatud konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-168">On the command bar, select **Save and Publish** to commit the new or updated configuration.</span></span>

> [!WARNING]
> <span data-ttu-id="b4e5b-169">Kui muudate kanalile määratud B2C rakendust, eemaldate praegused viited, mis on loodud kõigile kasutajatele, kes on juba keskkonda sisse loginud.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-169">If you change the B2C application that is assigned to the channel, you remove the current references that have been established for any users who have already signed up in the environment.</span></span> <span data-ttu-id="b4e5b-170">Sellisel juhul ei ole kasutajatele saadaval ükski praegu määratud B2C rakendusega seotud mandaat.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-170">In this case, any credentials that are associated with the currently assigned B2C application won't be available to users.</span></span> <span data-ttu-id="b4e5b-171">Seetõttu muutke kanali Azure AD B2C konfiguratsiooni ainult siis, kui seadistate kanalit esimest korda ja kasutajad ei ole saanud registreeruda.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-171">Therefore, change a channel Azure AD B2C configuration only if you're setting up the channel for the first time, and no users have been able to sign up.</span></span> <span data-ttu-id="b4e5b-172">Vastasel juhul võib juhtuda, et kasutajad peavad uue Azure AD B2C rentniku kirje loomiseks uuesti sisse logima.</span><span class="sxs-lookup"><span data-stu-id="b4e5b-172">Otherwise, users might have to sign up again to establish a record in the new Azure AD B2C tenant.</span></span>
## <a name="additional-resources"></a><span data-ttu-id="b4e5b-173">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b4e5b-173">Additional resources</span></span>

[<span data-ttu-id="b4e5b-174">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b4e5b-174">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="b4e5b-175">Uue e-kaubanduse rentniku juurutamine</span><span class="sxs-lookup"><span data-stu-id="b4e5b-175">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="b4e5b-176">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="b4e5b-176">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="b4e5b-177">Dynamics 365 Commerce'i saidi seostamine võrgukanaliga</span><span class="sxs-lookup"><span data-stu-id="b4e5b-177">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="b4e5b-178">robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="b4e5b-178">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="b4e5b-179">Üleslaadimise URL suunab ümber hulgi</span><span class="sxs-lookup"><span data-stu-id="b4e5b-179">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="b4e5b-180">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="b4e5b-180">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="b4e5b-181">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="b4e5b-181">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="b4e5b-182">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="b4e5b-182">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="b4e5b-183">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="b4e5b-183">Enable location-based store detection</span></span>](enable-store-detection.md)
