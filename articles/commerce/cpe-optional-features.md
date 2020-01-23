---
title: Commerce'i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida Microsoft Dynamics 365 Commerce’i eelvaatekeskkond, kui see on ette valmistatud.
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2c4872cdebc414eaa865af025237bd9e1d14bfd2
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906112"
---
# <a name="configure-optional-features-for-a-commerce-preview-environment"></a><span data-ttu-id="ba6d3-103">Commerce'i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ba6d3-103">Configure optional features for a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ba6d3-104">Selles teemas selgitatakse, kuidas konfigureerida Microsoft Dynamics 365 Commerce’i eelvaatekeskkond, kui see on ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ba6d3-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="ba6d3-105">Prerequisites</span></span>

<span data-ttu-id="ba6d3-106">Kui soovite hinnata ülekande meilifunktsioone, peavad olema täidetud järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="ba6d3-107">Teil on meili server saadaval \[SMTP\], mida saab kasutada Microsoft Azure'i tellimusel, kus te eelvaate keskkonda ette valmistate.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="ba6d3-108">Teile on saadaval serveri täielikult kvalifitseeritud domeeni nimi (FQDN)/IP aadress, SMTP pordi number ja autentimise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="ba6d3-109">Kui soovite hinnata digitaalse varahalduse funktsioone uusi omni-kanali pilte lisades, peab teil olema oma sisu haldamise süsteemi (CMS) üürniku nimi saadaval.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="ba6d3-110">Selle nime leidmise juhised on toodud hiljem selles teemas.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="ba6d3-111">>>>(Q: kus on juhised?)</span><span class="sxs-lookup"><span data-stu-id="ba6d3-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="ba6d3-112">Kujutise konfigureerimine tagaserveris</span><span class="sxs-lookup"><span data-stu-id="ba6d3-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="ba6d3-113">Oma meedia baas-URL-i leidmine</span><span class="sxs-lookup"><span data-stu-id="ba6d3-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="ba6d3-114">Enne, kui saate selle protseduuri lõpule viia, peate täitma sammud [oma saidi häälestamiseks Commerce'iis](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="ba6d3-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="ba6d3-115">Logige saidi halduse tööriista sisse, kasutades URL-i, mis te tegite, kui te e-kaubanduse lähtestamist ette valmistasite (vt [e-kaubanduse lähtestamine](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="ba6d3-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="ba6d3-116">Avage sait **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="ba6d3-117">Valige vasakpoolses menüüs **Varud**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="ba6d3-118">Valige mis tahes üks pildi vara.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-118">Select any single image asset.</span></span>
1. <span data-ttu-id="ba6d3-119">Paremal asuval atribuudi kontrollijal leiate **avaliku URL-i** atribuudi.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="ba6d3-120">Väärtus on URL.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-120">The value is a URL.</span></span> <span data-ttu-id="ba6d3-121">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-121">Here is an example:</span></span>

    <span data-ttu-id="ba6d3-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="ba6d3-123">Asendage viimane identifikaator URL-is (**MA1nQC** ülaltoodud näites) järgneva stringiga: **search?fileName=**. </span><span class="sxs-lookup"><span data-stu-id="ba6d3-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="ba6d3-124">Siin on näide URL-i väljanägemisest pärast seda muutust:</span><span class="sxs-lookup"><span data-stu-id="ba6d3-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="ba6d3-125">See URL on teie meedia baas-URL.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-125">This URL is your media base URL.</span></span> <span data-ttu-id="ba6d3-126">Tehke selle kohta märge.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="ba6d3-127">Meedia baas-URL-i värskendamine</span><span class="sxs-lookup"><span data-stu-id="ba6d3-127">Update the media base URL</span></span>

1. <span data-ttu-id="ba6d3-128">Logige sisse rakendusse Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-128">Sign in to Dynamics 365 Retail.</span></span>
1. <span data-ttu-id="ba6d3-129">Vasakul asuva menüü abil avage **Moodulid \> Jaemüük \> Kanali häälestus \> Kanali profiilid**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-129">Use the menu on the left to go to **Modules \> Retail \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="ba6d3-130">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-130">Select **Edit**.</span></span>
1. <span data-ttu-id="ba6d3-131">Suvandis **Profiili atribuudid** asendage atribuudi väärtus **Meedia serveri baas-URL** väärtusega Meedia baas-URL, mille enne lõite.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="ba6d3-132">Valige vasakult loendist teine kanal, mis on kanali **Vaikimisi** all.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="ba6d3-133">Suvandil **Profiili atribuudid** klõpsake nuppu **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="ba6d3-134">Lisatud atribuudi jaoks valige atribuudi võtmeks **Meedia serveri baas-URL**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="ba6d3-135">Atribuudi väärtusena sisestage varem loodud meediumi aluse URL.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="ba6d3-136">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="ba6d3-137">Meiliserveri konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ba6d3-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="ba6d3-138">Sisestatud SMTP-serveri või meiliteenus peab olema juurdepääsetav Azure'i kordustellimusest, mida keskkonna jaoks kasutate.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="ba6d3-139">Jaemüüki sisselogimine</span><span class="sxs-lookup"><span data-stu-id="ba6d3-139">Sign in to Retail.</span></span>
1. <span data-ttu-id="ba6d3-140">Vasakul asuva menüü abil avage **Moodulid \> Süsteemi haldus \> Häälestus \> Meil \> Meili parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="ba6d3-141">Sisestage vahekaardi **SMTP-** sätted väljale **Väljamineva meili server** oma SMTP-serveri või e-posti teenuse FQDN või IP-aadress.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="ba6d3-142">Sisestage väljale **SMTP pordi number** SMTP pordi number.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="ba6d3-143">(Kui te ei kasuta rakendust Secure Sockets Layer \[SSL\]-i, on vaikimisi pordi number **25**.)</span><span class="sxs-lookup"><span data-stu-id="ba6d3-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="ba6d3-144">Autentimise vajadusel sisestage väärtused väljadele **Kasutajanimi** ja **Prool**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="ba6d3-145">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-145">Select **Save**.</span></span>
1. <span data-ttu-id="ba6d3-146">Valige **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="ba6d3-147">Vahekaardil **testi meili** väljal **e-posti pakkuja** valige **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="ba6d3-148">Väljale **Saada** sisestage meiliaadress, millele soovite testmeili saata.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="ba6d3-149">Valige **Saada testmeilisõnum**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="ba6d3-150">Meilimallide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ba6d3-150">Configure email templates</span></span>

<span data-ttu-id="ba6d3-151">Iga kandelise sündmuse jaoks, mille jaoks soovite meile saata, tuleb uuendada meilimalli kehtiva saatja meiliaadressiga.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="ba6d3-152">Jaemüüki sisselogimine</span><span class="sxs-lookup"><span data-stu-id="ba6d3-152">Sign in to Retail.</span></span>
1. <span data-ttu-id="ba6d3-153">Vasakul asuva menüü abil avage **Moodulid \> Organisatsiooni haldus \> Häälestus \> Organisatsiooni meilimallid**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="ba6d3-154">Valige **Näita loendit**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-154">Select **Show list**.</span></span>
1. <span data-ttu-id="ba6d3-155">Iga loetletud malli puhul toimige järgmiselt:</span><span class="sxs-lookup"><span data-stu-id="ba6d3-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="ba6d3-156">Väljale **Saatja meiliaadress** sisestage saatja meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="ba6d3-157">Valikuline: Sisestage väljale **saatja nimi** nimi, mida tuleks saatja nimena kasutada.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="ba6d3-158">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="ba6d3-159">Meilimallide kohandamine</span><span class="sxs-lookup"><span data-stu-id="ba6d3-159">Customize email templates</span></span>

<span data-ttu-id="ba6d3-160">Võite soovida kohandada meilimalle, et nad kasutaksid erinevaid pilte.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="ba6d3-161">Võite ka värskendada linke mallides, et need läheksid teie eelvaate keskkonda.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="ba6d3-162">See protseduur selgitab, kuidas vaikimisi malle alla laadida, neid kohandada ja süsteemi malle värskendada.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="ba6d3-163">Brauseri abil laadige kohalikku arvutisse [Microsoft Dynamics 365 Commerce eelvaate vaikimisi meilimallide zip-fail](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip).</span><span class="sxs-lookup"><span data-stu-id="ba6d3-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="ba6d3-164">See fail sisaldab järgmisi HTML-dokumente:</span><span class="sxs-lookup"><span data-stu-id="ba6d3-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="ba6d3-165">Tellimuse kinnituse mall</span><span class="sxs-lookup"><span data-stu-id="ba6d3-165">Order confirmation template</span></span>
    - <span data-ttu-id="ba6d3-166">Kinkekaardi väljastamise mall</span><span class="sxs-lookup"><span data-stu-id="ba6d3-166">Issue gift card template</span></span>
    - <span data-ttu-id="ba6d3-167">Uue tellimuse mall</span><span class="sxs-lookup"><span data-stu-id="ba6d3-167">New order template</span></span>
    - <span data-ttu-id="ba6d3-168">Pakketellimuse mall</span><span class="sxs-lookup"><span data-stu-id="ba6d3-168">Pack order template</span></span>
    - <span data-ttu-id="ba6d3-169">Tellimuse malli valimine</span><span class="sxs-lookup"><span data-stu-id="ba6d3-169">Pick order template</span></span>

1. <span data-ttu-id="ba6d3-170">Kohandage malle teksti või HTML-redaktori abil.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="ba6d3-171">Vaadake selles teemas hiljem [toetatud märkide](#supported-tokens-in-the-email-template) loendit.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="ba6d3-172">Jaemüüki sisselogimine</span><span class="sxs-lookup"><span data-stu-id="ba6d3-172">Sign in to Retail.</span></span>
1. <span data-ttu-id="ba6d3-173">Vasakul asuva menüü abil avage **Moodulid \> Organisatsiooni haldus \> Häälestus \> Organisatsiooni meilimallid**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="ba6d3-174">Kõigi mallide nägemiseks laiendage loendit vasakul.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="ba6d3-175">Iga malli puhul, mida soovite kohandada, tehke järgmist:</span><span class="sxs-lookup"><span data-stu-id="ba6d3-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="ba6d3-176">Valige loendist mall.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="ba6d3-177">Jaotises **Meilisõnumi sisu** valige loendist sobiva keele versioon.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="ba6d3-178">(Vaikekeel on **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="ba6d3-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="ba6d3-179">Jaotises **e-kirja sisu** valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="ba6d3-180">Kuvatakse paan **Laadi üles e-kirja mall**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="ba6d3-181">Valige **Sirvi**ja leidke HTML-fail, millel on kohandatud sisu.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="ba6d3-182">Valige nupp **Laadi üles**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-182">Select **Upload**.</span></span> <span data-ttu-id="ba6d3-183">Teie mall laaditakse süsteemi ja kuvatakse eelvaade.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="ba6d3-184">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-184">Select **OK**.</span></span>
    1. <span data-ttu-id="ba6d3-185">Valikuline: kohandage malli atribuuti **Teema**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="ba6d3-186">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="ba6d3-187">Toetatud märgid meilimallis</span><span class="sxs-lookup"><span data-stu-id="ba6d3-187">Supported tokens in the email template</span></span>

<span data-ttu-id="ba6d3-188">Need märgid asendatakse meili renderdamise ajal tegelike väärtustega, mis rakenduvad kliendile ja nende tellimusele.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="ba6d3-189">Müügitellimus</span><span class="sxs-lookup"><span data-stu-id="ba6d3-189">Sales order</span></span>

<span data-ttu-id="ba6d3-190">Järgmised load rakenduvad üldisele müügitellimusele.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="ba6d3-191">Märgi nimi</span><span class="sxs-lookup"><span data-stu-id="ba6d3-191">Name of the token</span></span> | <span data-ttu-id="ba6d3-192">Luba</span><span class="sxs-lookup"><span data-stu-id="ba6d3-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="ba6d3-193">Tellimuse kood</span><span class="sxs-lookup"><span data-stu-id="ba6d3-193">Order number</span></span>      | <span data-ttu-id="ba6d3-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-194">%salesid%</span></span> |
| <span data-ttu-id="ba6d3-195">Kliendi nimi</span><span class="sxs-lookup"><span data-stu-id="ba6d3-195">Customer's name</span></span>   | <span data-ttu-id="ba6d3-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-196">%customername%</span></span> |
| <span data-ttu-id="ba6d3-197">Tarneaadress</span><span class="sxs-lookup"><span data-stu-id="ba6d3-197">Delivery address</span></span>  | <span data-ttu-id="ba6d3-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="ba6d3-199">Arveaadress</span><span class="sxs-lookup"><span data-stu-id="ba6d3-199">Billing address</span></span>   | <span data-ttu-id="ba6d3-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-200">%customeraddress%</span></span> |
| <span data-ttu-id="ba6d3-201">Tellimuse kuupäev</span><span class="sxs-lookup"><span data-stu-id="ba6d3-201">Order date</span></span>        | <span data-ttu-id="ba6d3-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-202">%shipdate%</span></span> |
| <span data-ttu-id="ba6d3-203">Tarneviis</span><span class="sxs-lookup"><span data-stu-id="ba6d3-203">Delivery mode</span></span>     | <span data-ttu-id="ba6d3-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="ba6d3-205">Allahindlus</span><span class="sxs-lookup"><span data-stu-id="ba6d3-205">Discount</span></span>          | <span data-ttu-id="ba6d3-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-206">%discount%</span></span> |
| <span data-ttu-id="ba6d3-207">Käibemaks</span><span class="sxs-lookup"><span data-stu-id="ba6d3-207">Sales tax</span></span>         | <span data-ttu-id="ba6d3-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-208">%tax%</span></span> |
| <span data-ttu-id="ba6d3-209">Tellimuse kogusumma</span><span class="sxs-lookup"><span data-stu-id="ba6d3-209">Order total</span></span>       | <span data-ttu-id="ba6d3-210">%total%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="ba6d3-211">Müügirida</span><span class="sxs-lookup"><span data-stu-id="ba6d3-211">Sales line</span></span>

<span data-ttu-id="ba6d3-212">Järgmised load on iga toote puhul tellimuses asendatud väärtustega.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="ba6d3-213">Pange **toote nimekiri – alustage** luba HTML-ploki algusesse, mida korratakse iga toote puhul, ja asetage **toote loend-lõpp** -luba ploki lõppu.</span><span class="sxs-lookup"><span data-stu-id="ba6d3-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="ba6d3-214">Märgi nimi</span><span class="sxs-lookup"><span data-stu-id="ba6d3-214">Name of the token</span></span>      | <span data-ttu-id="ba6d3-215">Luba</span><span class="sxs-lookup"><span data-stu-id="ba6d3-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="ba6d3-216">Tooteloend - algus</span><span class="sxs-lookup"><span data-stu-id="ba6d3-216">Product list - start</span></span>   | <span data-ttu-id="ba6d3-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="ba6d3-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="ba6d3-218">Tooteloend - lõpp</span><span class="sxs-lookup"><span data-stu-id="ba6d3-218">Product list - end</span></span>     | <span data-ttu-id="ba6d3-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="ba6d3-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="ba6d3-220">Toote nimi</span><span class="sxs-lookup"><span data-stu-id="ba6d3-220">Product name</span></span>           | <span data-ttu-id="ba6d3-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-221">%lineproductname%</span></span> |
| <span data-ttu-id="ba6d3-222">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ba6d3-222">Description</span></span>            | <span data-ttu-id="ba6d3-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="ba6d3-224">Kogus</span><span class="sxs-lookup"><span data-stu-id="ba6d3-224">Quantity</span></span>               | <span data-ttu-id="ba6d3-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-225">%linequantity%</span></span> |
| <span data-ttu-id="ba6d3-226">Reaühiku hind</span><span class="sxs-lookup"><span data-stu-id="ba6d3-226">Line unit price</span></span>        | <span data-ttu-id="ba6d3-227">%lineprice% (kontrollige)</span><span class="sxs-lookup"><span data-stu-id="ba6d3-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="ba6d3-228">reaüksuse kogusumma</span><span class="sxs-lookup"><span data-stu-id="ba6d3-228">line item total</span></span>        | <span data-ttu-id="ba6d3-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-229">%linenetamount%</span></span> |
| <span data-ttu-id="ba6d3-230">rea allahindlus</span><span class="sxs-lookup"><span data-stu-id="ba6d3-230">line discount</span></span>          | <span data-ttu-id="ba6d3-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-231">%linediscount%</span></span> |
| <span data-ttu-id="ba6d3-232">Lähetuskuupäev</span><span class="sxs-lookup"><span data-stu-id="ba6d3-232">Ship date</span></span>              | <span data-ttu-id="ba6d3-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-233">%lineshipdate%</span></span> |
| <span data-ttu-id="ba6d3-234">Hanke meetod</span><span class="sxs-lookup"><span data-stu-id="ba6d3-234">Procurement method</span></span>     | <span data-ttu-id="ba6d3-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="ba6d3-236">tarneaadress</span><span class="sxs-lookup"><span data-stu-id="ba6d3-236">delivery address</span></span>       | <span data-ttu-id="ba6d3-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="ba6d3-238">Rea müügiüksus</span><span class="sxs-lookup"><span data-stu-id="ba6d3-238">Sales unit of the line</span></span> | <span data-ttu-id="ba6d3-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="ba6d3-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="ba6d3-240">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ba6d3-240">Additional resources</span></span>

[<span data-ttu-id="ba6d3-241">Commerce'i eelvaatekeskkonna ülevaade</span><span class="sxs-lookup"><span data-stu-id="ba6d3-241">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="ba6d3-242">Commerce'i eelvaatekeskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="ba6d3-242">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="ba6d3-243">Commerce'i eelvaatekeskkonna konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ba6d3-243">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="ba6d3-244">Commerce'i eelvaatekeskkonna KKK</span><span class="sxs-lookup"><span data-stu-id="ba6d3-244">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="ba6d3-245">Microsofti elutsükli teenused (LCS)</span><span class="sxs-lookup"><span data-stu-id="ba6d3-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="ba6d3-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="ba6d3-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="ba6d3-247">Microsoft Azure'i portaal</span><span class="sxs-lookup"><span data-stu-id="ba6d3-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="ba6d3-248">Dynamics 365 Commerce veebisait</span><span class="sxs-lookup"><span data-stu-id="ba6d3-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="ba6d3-249">Abiressursid rakenduse Dynamics 365 Retail jaoks</span><span class="sxs-lookup"><span data-stu-id="ba6d3-249">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
