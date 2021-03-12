---
title: Dynamics 365 Commerce'i hindamiskeskkonna valikuliste funktsioonide konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida Microsoft Dynamics 365 Commerce’i hindamiskeskkond, kui see on ette valmistatud.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6639de250557ce9a25fc2cde3807abf64b0ddc18
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993446"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="14bc1-103">Dynamics 365 Commerce'i hindamiskeskkonna valikuliste funktsioonide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="14bc1-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="14bc1-104">Selles teemas selgitatakse, kuidas konfigureerida Microsoft Dynamics 365 Commerce’i hindamiskeskkond, kui see on ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="14bc1-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="14bc1-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="14bc1-105">Prerequisites</span></span>

<span data-ttu-id="14bc1-106">Kui soovite hinnata ülekande meilifunktsioone, peavad olema täidetud järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="14bc1-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="14bc1-107">Teil on meiliserver saadaval (Simple Mail Transfer Protocol \[SMTP\] server), mida saab kasutada Microsoft Azure'i tellimuses, kus te hindamiskeskkonda ette valmistate.</span><span class="sxs-lookup"><span data-stu-id="14bc1-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="14bc1-108">Teile on saadaval serveri täielikult kvalifitseeritud domeeni nimi (FQDN)/IP aadress, SMTP pordi number ja autentimise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="14bc1-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="14bc1-109">Kujutise konfigureerimine tagaserveris</span><span class="sxs-lookup"><span data-stu-id="14bc1-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="14bc1-110">Oma meedia baas-URL-i leidmine</span><span class="sxs-lookup"><span data-stu-id="14bc1-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="14bc1-111">Enne, kui saate selle protseduuri lõpule viia, peate täitma sammud [oma saidi häälestamiseks Commerce'iis](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="14bc1-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="14bc1-112">Logige Commerce'i saidiehitajasse sisse, kasutades URL-i, mille märkisite üles, kui te e-kaubanduse lähtestamist ette valmistasite (vt [e-kaubanduse lähtestamine](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="14bc1-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="14bc1-113">Avage sait **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="14bc1-114">Valige vasakpoolses menüüs **Meediumiteek**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="14bc1-115">Valige mis tahes üks pildi vara.</span><span class="sxs-lookup"><span data-stu-id="14bc1-115">Select any single image asset.</span></span>
1. <span data-ttu-id="14bc1-116">Paremal asuval atribuudi kontrollijal leiate **avaliku URL-i** atribuudi.</span><span class="sxs-lookup"><span data-stu-id="14bc1-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="14bc1-117">Väärtus on URL.</span><span class="sxs-lookup"><span data-stu-id="14bc1-117">The value is a URL.</span></span> <span data-ttu-id="14bc1-118">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="14bc1-118">Here is an example:</span></span>

    <span data-ttu-id="14bc1-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="14bc1-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="14bc1-120">Asendage viimane identifikaator URL-is (**MA1nQC** ülaltoodud näites) järgneva stringiga: **search?fileName=**. </span><span class="sxs-lookup"><span data-stu-id="14bc1-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="14bc1-121">Siin on näide URL-i väljanägemisest pärast seda muutust:</span><span class="sxs-lookup"><span data-stu-id="14bc1-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="14bc1-122">See URL on teie meedia baas-URL.</span><span class="sxs-lookup"><span data-stu-id="14bc1-122">This URL is your media base URL.</span></span> <span data-ttu-id="14bc1-123">Tehke selle kohta märge.</span><span class="sxs-lookup"><span data-stu-id="14bc1-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="14bc1-124">Meedia baas-URL-i värskendamine</span><span class="sxs-lookup"><span data-stu-id="14bc1-124">Update the media base URL</span></span>

1. <span data-ttu-id="14bc1-125">Logige Commerce’i peakontorisse sisse.</span><span class="sxs-lookup"><span data-stu-id="14bc1-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="14bc1-126">Vasakul asuva menüü abil avage **Moodulid \> Jaemüük ja kaubandus \> Kanali häälestus \> Kanali profiilid**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="14bc1-127">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-127">Select **Edit**.</span></span>
1. <span data-ttu-id="14bc1-128">Suvandis **Profiili atribuudid** asendage atribuudi väärtus **Meedia serveri baas-URL** väärtusega Meedia baas-URL, mille enne lõite.</span><span class="sxs-lookup"><span data-stu-id="14bc1-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="14bc1-129">Valige muu kanal nimega **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="14bc1-130">Suvandil **Profiili atribuudid** klõpsake nuppu **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="14bc1-131">Lisatud atribuudi jaoks valige atribuudi võtmeks **Meedia serveri baas-URL**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="14bc1-132">Atribuudi väärtusena sisestage varem loodud meediumi aluse URL.</span><span class="sxs-lookup"><span data-stu-id="14bc1-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="14bc1-133">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="14bc1-134">Meiliserveri konfigureerimine ja testimine</span><span class="sxs-lookup"><span data-stu-id="14bc1-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="14bc1-135">Sisestatud SMTP-serveri või meiliteenus peab olema juurdepääsetav Azure'i kordustellimusest, mida keskkonna jaoks kasutate.</span><span class="sxs-lookup"><span data-stu-id="14bc1-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="14bc1-136">Logige Commerce’i peakontorisse sisse.</span><span class="sxs-lookup"><span data-stu-id="14bc1-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="14bc1-137">Avage vasakul oleva menüü abil **Moodulid \> Jaemüük ja kaubandus \> Peakontori häälestus \> Parameetrid \> Meiliparameetrid**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="14bc1-138">Sisestage vahekaardi **SMTP-** sätted väljale **Väljamineva meili server** oma SMTP-serveri või e-posti teenuse FQDN või IP-aadress.</span><span class="sxs-lookup"><span data-stu-id="14bc1-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="14bc1-139">Sisestage väljale **SMTP pordi number** SMTP pordi number.</span><span class="sxs-lookup"><span data-stu-id="14bc1-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="14bc1-140">(Kui te ei kasuta rakendust Secure Sockets Layer \[SSL\]-i, on vaikimisi pordi number **25**.)</span><span class="sxs-lookup"><span data-stu-id="14bc1-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="14bc1-141">Autentimise vajadusel sisestage väärtused väljadele **Kasutajanimi** ja **Prool**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="14bc1-142">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-142">Select **Save**.</span></span>
1. <span data-ttu-id="14bc1-143">Valige **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="14bc1-144">Vahekaardil **testi meili** väljal **e-posti pakkuja** valige **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="14bc1-145">Väljale **Saada** sisestage meiliaadress, millele soovite testmeili saata.</span><span class="sxs-lookup"><span data-stu-id="14bc1-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="14bc1-146">Valige **Saada testmeilisõnum**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="14bc1-147">Meilimallide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="14bc1-147">Configure email templates</span></span>

<span data-ttu-id="14bc1-148">Iga kandelise sündmuse jaoks, mille jaoks soovite meile saata, tuleb uuendada meilimalli kehtiva saatja meiliaadressiga.</span><span class="sxs-lookup"><span data-stu-id="14bc1-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="14bc1-149">Logige Commerce’i peakontorisse sisse.</span><span class="sxs-lookup"><span data-stu-id="14bc1-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="14bc1-150">Avage vasakul oleva menüü abil **Moodulid \> Jaemüük ja kaubandus \> Peakontori häälestus \> Parameetrid \> Organisatsiooni meilimallid**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="14bc1-151">Valige **Näita loendit**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-151">Select **Show list**.</span></span>
1. <span data-ttu-id="14bc1-152">Iga loetletud malli puhul toimige järgmiselt:</span><span class="sxs-lookup"><span data-stu-id="14bc1-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="14bc1-153">Väljale **Saatja meiliaadress** sisestage saatja meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="14bc1-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="14bc1-154">Valikuline: Sisestage väljale **saatja nimi** nimi, mida tuleks saatja nimena kasutada.</span><span class="sxs-lookup"><span data-stu-id="14bc1-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="14bc1-155">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="14bc1-156">Meilimallide kohandamine</span><span class="sxs-lookup"><span data-stu-id="14bc1-156">Customize email templates</span></span>

<span data-ttu-id="14bc1-157">Võite soovida kohandada meilimalle, et nad kasutaksid erinevaid pilte.</span><span class="sxs-lookup"><span data-stu-id="14bc1-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="14bc1-158">Võite ka värskendada linke mallides, et need sobiksid teie hindamiskeskkonda.</span><span class="sxs-lookup"><span data-stu-id="14bc1-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="14bc1-159">See protseduur selgitab, kuidas vaikimisi malle alla laadida, neid kohandada ja süsteemi malle värskendada.</span><span class="sxs-lookup"><span data-stu-id="14bc1-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="14bc1-160">Laadige brauserist alla kohalikku arvutisse [Microsoft Dynamics 365 Commerce'i hindamisee vaikimisi meilimallide zip-fail](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip).</span><span class="sxs-lookup"><span data-stu-id="14bc1-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="14bc1-161">See fail sisaldab järgmisi HTML-dokumente:</span><span class="sxs-lookup"><span data-stu-id="14bc1-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="14bc1-162">Tellimuse kinnituse mall</span><span class="sxs-lookup"><span data-stu-id="14bc1-162">Order confirmation template</span></span>
    - <span data-ttu-id="14bc1-163">Kinkekaardi väljastamise mall</span><span class="sxs-lookup"><span data-stu-id="14bc1-163">Issue gift card template</span></span>
    - <span data-ttu-id="14bc1-164">Uue tellimuse mall</span><span class="sxs-lookup"><span data-stu-id="14bc1-164">New order template</span></span>
    - <span data-ttu-id="14bc1-165">Pakketellimuse mall</span><span class="sxs-lookup"><span data-stu-id="14bc1-165">Pack order template</span></span>
    - <span data-ttu-id="14bc1-166">Tellimuse malli valimine</span><span class="sxs-lookup"><span data-stu-id="14bc1-166">Pick order template</span></span>

1. <span data-ttu-id="14bc1-167">Kohandage malle teksti või HTML-redaktori abil.</span><span class="sxs-lookup"><span data-stu-id="14bc1-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="14bc1-168">Vaadake selles teemas hiljem [toetatud märkide](#supported-tokens-in-the-email-template) loendit.</span><span class="sxs-lookup"><span data-stu-id="14bc1-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="14bc1-169">Logige Commerce’i sisse.</span><span class="sxs-lookup"><span data-stu-id="14bc1-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="14bc1-170">Vasakul asuva menüü abil avage **Moodulid \> Organisatsiooni haldus \> Häälestus \> Organisatsiooni meilimallid**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="14bc1-171">Kõigi mallide nägemiseks laiendage loendit vasakul.</span><span class="sxs-lookup"><span data-stu-id="14bc1-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="14bc1-172">Iga malli puhul, mida soovite kohandada, tehke järgmist:</span><span class="sxs-lookup"><span data-stu-id="14bc1-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="14bc1-173">Valige loendist mall.</span><span class="sxs-lookup"><span data-stu-id="14bc1-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="14bc1-174">Jaotises **Meilisõnumi sisu** valige loendist sobiva keele versioon.</span><span class="sxs-lookup"><span data-stu-id="14bc1-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="14bc1-175">(Vaikekeel on **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="14bc1-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="14bc1-176">Jaotises **e-kirja sisu** valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="14bc1-177">Kuvatakse paan **Laadi üles e-kirja mall**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="14bc1-178">Valige **Sirvi** ja leidke HTML-fail, millel on kohandatud sisu.</span><span class="sxs-lookup"><span data-stu-id="14bc1-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="14bc1-179">Valige nupp **Laadi üles**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-179">Select **Upload**.</span></span> <span data-ttu-id="14bc1-180">Teie mall laaditakse süsteemi ja kuvatakse eelvaade.</span><span class="sxs-lookup"><span data-stu-id="14bc1-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="14bc1-181">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-181">Select **OK**.</span></span>
    1. <span data-ttu-id="14bc1-182">Valikuline: kohandage malli atribuuti **Teema**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="14bc1-183">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="14bc1-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="14bc1-184">Toetatud märgid meilimallis</span><span class="sxs-lookup"><span data-stu-id="14bc1-184">Supported tokens in the email template</span></span>

<span data-ttu-id="14bc1-185">Need märgid asendatakse meili renderdamise ajal tegelike väärtustega, mis rakenduvad kliendile ja nende tellimusele.</span><span class="sxs-lookup"><span data-stu-id="14bc1-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="14bc1-186">Müügitellimus</span><span class="sxs-lookup"><span data-stu-id="14bc1-186">Sales order</span></span>

<span data-ttu-id="14bc1-187">Järgmised load rakenduvad üldisele müügitellimusele.</span><span class="sxs-lookup"><span data-stu-id="14bc1-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="14bc1-188">Märgi nimi</span><span class="sxs-lookup"><span data-stu-id="14bc1-188">Name of the token</span></span> | <span data-ttu-id="14bc1-189">Luba</span><span class="sxs-lookup"><span data-stu-id="14bc1-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="14bc1-190">Tellimuse kood</span><span class="sxs-lookup"><span data-stu-id="14bc1-190">Order number</span></span>      | <span data-ttu-id="14bc1-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="14bc1-191">%salesid%</span></span> |
| <span data-ttu-id="14bc1-192">Kliendi nimi</span><span class="sxs-lookup"><span data-stu-id="14bc1-192">Customer's name</span></span>   | <span data-ttu-id="14bc1-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="14bc1-193">%customername%</span></span> |
| <span data-ttu-id="14bc1-194">Tarneaadress</span><span class="sxs-lookup"><span data-stu-id="14bc1-194">Delivery address</span></span>  | <span data-ttu-id="14bc1-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="14bc1-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="14bc1-196">Arveaadress</span><span class="sxs-lookup"><span data-stu-id="14bc1-196">Billing address</span></span>   | <span data-ttu-id="14bc1-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="14bc1-197">%customeraddress%</span></span> |
| <span data-ttu-id="14bc1-198">Tellimuse kuupäev</span><span class="sxs-lookup"><span data-stu-id="14bc1-198">Order date</span></span>        | <span data-ttu-id="14bc1-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="14bc1-199">%shipdate%</span></span> |
| <span data-ttu-id="14bc1-200">Tarneviis</span><span class="sxs-lookup"><span data-stu-id="14bc1-200">Delivery mode</span></span>     | <span data-ttu-id="14bc1-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="14bc1-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="14bc1-202">Allahindlus</span><span class="sxs-lookup"><span data-stu-id="14bc1-202">Discount</span></span>          | <span data-ttu-id="14bc1-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="14bc1-203">%discount%</span></span> |
| <span data-ttu-id="14bc1-204">Käibemaks</span><span class="sxs-lookup"><span data-stu-id="14bc1-204">Sales tax</span></span>         | <span data-ttu-id="14bc1-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="14bc1-205">%tax%</span></span> |
| <span data-ttu-id="14bc1-206">Tellimuse kogusumma</span><span class="sxs-lookup"><span data-stu-id="14bc1-206">Order total</span></span>       | <span data-ttu-id="14bc1-207">%total%</span><span class="sxs-lookup"><span data-stu-id="14bc1-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="14bc1-208">Müügirida</span><span class="sxs-lookup"><span data-stu-id="14bc1-208">Sales line</span></span>

<span data-ttu-id="14bc1-209">Järgmised load on iga toote puhul tellimuses asendatud väärtustega.</span><span class="sxs-lookup"><span data-stu-id="14bc1-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="14bc1-210">Pange **toote nimekiri – alustage** luba HTML-ploki algusesse, mida korratakse iga toote puhul, ja asetage **toote loend-lõpp** -luba ploki lõppu.</span><span class="sxs-lookup"><span data-stu-id="14bc1-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="14bc1-211">Märgi nimi</span><span class="sxs-lookup"><span data-stu-id="14bc1-211">Name of the token</span></span>      | <span data-ttu-id="14bc1-212">Luba</span><span class="sxs-lookup"><span data-stu-id="14bc1-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="14bc1-213">Tooteloend - algus</span><span class="sxs-lookup"><span data-stu-id="14bc1-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="14bc1-214">Tooteloend - lõpp</span><span class="sxs-lookup"><span data-stu-id="14bc1-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="14bc1-215">Toote nimetus</span><span class="sxs-lookup"><span data-stu-id="14bc1-215">Product name</span></span>           | <span data-ttu-id="14bc1-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="14bc1-216">%lineproductname%</span></span> |
| <span data-ttu-id="14bc1-217">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="14bc1-217">Description</span></span>            | <span data-ttu-id="14bc1-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="14bc1-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="14bc1-219">Kogus</span><span class="sxs-lookup"><span data-stu-id="14bc1-219">Quantity</span></span>               | <span data-ttu-id="14bc1-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="14bc1-220">%linequantity%</span></span> |
| <span data-ttu-id="14bc1-221">Reaühiku hind</span><span class="sxs-lookup"><span data-stu-id="14bc1-221">Line unit price</span></span>        | <span data-ttu-id="14bc1-222">%lineprice% (kontrollige)</span><span class="sxs-lookup"><span data-stu-id="14bc1-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="14bc1-223">reaüksuse kogusumma</span><span class="sxs-lookup"><span data-stu-id="14bc1-223">line item total</span></span>        | <span data-ttu-id="14bc1-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="14bc1-224">%linenetamount%</span></span> |
| <span data-ttu-id="14bc1-225">rea allahindlus</span><span class="sxs-lookup"><span data-stu-id="14bc1-225">line discount</span></span>          | <span data-ttu-id="14bc1-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="14bc1-226">%linediscount%</span></span> |
| <span data-ttu-id="14bc1-227">Lähetuskuupäev</span><span class="sxs-lookup"><span data-stu-id="14bc1-227">Ship date</span></span>              | <span data-ttu-id="14bc1-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="14bc1-228">%lineshipdate%</span></span> |
| <span data-ttu-id="14bc1-229">Hanke meetod</span><span class="sxs-lookup"><span data-stu-id="14bc1-229">Procurement method</span></span>     | <span data-ttu-id="14bc1-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="14bc1-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="14bc1-231">tarneaadress</span><span class="sxs-lookup"><span data-stu-id="14bc1-231">delivery address</span></span>       | <span data-ttu-id="14bc1-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="14bc1-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="14bc1-233">Rea müügiüksus</span><span class="sxs-lookup"><span data-stu-id="14bc1-233">Sales unit of the line</span></span> | <span data-ttu-id="14bc1-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="14bc1-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="14bc1-235">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="14bc1-235">Additional resources</span></span>

[<span data-ttu-id="14bc1-236">Dynamics 365 Commerce'i hindamiskeskkonna ülevaade</span><span class="sxs-lookup"><span data-stu-id="14bc1-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="14bc1-237">Dynamics 365 Commerce'i hindamiskeskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="14bc1-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="14bc1-238">Dynamics 365 Commerce'i hindamiskeskkonna konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="14bc1-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="14bc1-239">BOPIS-e konfigureerimine Dynamics 365 Commerce'i hindamiskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="14bc1-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="14bc1-240">Dynamics 365 Commerce'i hindamiskeskkonna KKK</span><span class="sxs-lookup"><span data-stu-id="14bc1-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="14bc1-241">Microsofti elutsükli teenused (LCS)</span><span class="sxs-lookup"><span data-stu-id="14bc1-241">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="14bc1-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="14bc1-242">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="14bc1-243">Microsoft Azure'i portaal</span><span class="sxs-lookup"><span data-stu-id="14bc1-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="14bc1-244">Dynamics 365 Commerce veebisait</span><span class="sxs-lookup"><span data-stu-id="14bc1-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
