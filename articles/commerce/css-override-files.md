---
title: CSS-i alistamisfailidega töötamine
description: See teema kirjeldab miks, millal ja kuidas kasutada Cascading Style Sheet (CSS) alistamisfaile rakendusega Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b5a50fc0c9060117cdddc0875446afc2edc12a11
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915435"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="51875-103">CSS-i alistamisfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="51875-103">Work with CSS override files</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="51875-104">See teema kirjeldab miks, millal ja kuidas kasutada Cascading Style Sheet (CSS) alistamisfaile rakendusega Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="51875-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="51875-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="51875-105">Overview</span></span>

<span data-ttu-id="51875-106">Püsiva tegevuskoha laade peaks tavaliselt käsitlema saidi kujunduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="51875-106">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="51875-107">Kujundused annavad teie saidi mis tahes leheküljel olevate moodulite jaoks CSS aluselise ja stiili sätted.</span><span class="sxs-lookup"><span data-stu-id="51875-107">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="51875-108">Kujundused luuakse Dynamics 365 Commerce’i veebitarkvara arenduse komplekti (SDK) abil ja need viiakse teie veebisaitide juurde teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu.</span><span class="sxs-lookup"><span data-stu-id="51875-108">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="51875-109">Kujunduse silumise võimalused ja mooduli liidese konfiguratsioonid SDK-spikri saidi arendajatel loovad kohandatavad ja sidusad saidi kujunduse paketid.</span><span class="sxs-lookup"><span data-stu-id="51875-109">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="51875-110">Kui need kujunduse paketid on saidile paigutatud, saavad saidi autorid keskenduda saidi arendamise asemel sisu loomisele, redigeerimisele ja avaldamisele.</span><span class="sxs-lookup"><span data-stu-id="51875-110">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="51875-111">Arvestades kujunduse tavalist elutsüklit, võib mõne stsenaariumi puhul olla keelatud arendajate poolne muudatus SDK ja LCS-i juurutamise torujuhtme kaudu.</span><span class="sxs-lookup"><span data-stu-id="51875-111">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="51875-112">Saidi prototüübid või kiirparandused võivad näida kohmakatena, kui SDK ei ole konigureeritud või kui teil pole aega LCS-i juurutamise ootamiseks.</span><span class="sxs-lookup"><span data-stu-id="51875-112">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="51875-113">Nende stsenaariumide korral võib abi olla CSS-i alistamisfailidest.</span><span class="sxs-lookup"><span data-stu-id="51875-113">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="51875-114">Commerce’i autorluse tööriistades saavad volitatud kasutajad CSS-faili üles laadida, kuvada selle eelvaate ja seejärel aktiveerida selle, et alistada saidi kujundus.</span><span class="sxs-lookup"><span data-stu-id="51875-114">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="51875-115">SDK või LCS-i juurutuse üldkulu pole nõutav.</span><span class="sxs-lookup"><span data-stu-id="51875-115">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="51875-116">CSS-i alistamisfailis määratletud alistamised võivad olla nii väikesed kui ühe teksi laadi muutmine, või nii laiaulatuslikud, kui kogu kaubamärgi uuendamine.</span><span class="sxs-lookup"><span data-stu-id="51875-116">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="51875-117">Enne CSS-i alistamisfailide kasutamist arvestage järgmiste piirangutega.</span><span class="sxs-lookup"><span data-stu-id="51875-117">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="51875-118">Korraga saab saidil olla ainult üks CSS-i alistumisfail.</span><span class="sxs-lookup"><span data-stu-id="51875-118">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="51875-119">Seetõttu peavad kõik aktiivsed alistamised olema ühes alistamisfailis.</span><span class="sxs-lookup"><span data-stu-id="51875-119">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="51875-120">Kuigi saate Commerce’i autorluse tööriistades kuvada alistamiste eelvaate, puuduvad spetsiaalsed silumise funktsioonid, mis aitaksid tuvastada mis tahes tõrkeid, mida alistamised tekitavad.</span><span class="sxs-lookup"><span data-stu-id="51875-120">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="51875-121">Teisisõnu kui kasutate CSS-i alistamisfaile, pole teil sama tööriistakogumit, mida SDK pakub mooduli ja autorluse kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="51875-121">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="51875-122">Sellegipoolest pakuvad CSS-i alistamisfailid kiiret viisi kujunduse prototüübi loomiseks või kiirparanduse rakendamiseks enne täieliku kujunduse uuenduse arendamist ja juurutamist.</span><span class="sxs-lookup"><span data-stu-id="51875-122">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="51875-123">CSS-i alistamisfaili loomine</span><span class="sxs-lookup"><span data-stu-id="51875-123">Create a CSS override file</span></span>

<span data-ttu-id="51875-124">CSS-i alistufaili loomiseks sate kasutada mis tahes integreeritud arenduskeskkonda (IDE), tekstiredaktorit või lähtekoodi redaktorit.</span><span class="sxs-lookup"><span data-stu-id="51875-124">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="51875-125">Tüüpiline lähenemine on kasutada brauseris standardseid veebisilurit, et tuvastada teie olemasoleval saidil laadi valijad, atribuudid ja väärtused.</span><span class="sxs-lookup"><span data-stu-id="51875-125">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="51875-126">Enamik brausereid võimaldavadb teil muuta väärtusi ja kuvada siluris nende eelvaade.</span><span class="sxs-lookup"><span data-stu-id="51875-126">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="51875-127">Kui olete tuvastanud muudatused, mida soovite teha, saate need salvestada oma CSS-i faili.</span><span class="sxs-lookup"><span data-stu-id="51875-127">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="51875-128">CSS-i alistamisfaili üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="51875-128">Upload a CSS override file</span></span>

<span data-ttu-id="51875-129">CSS-i alistamisfaili Commerce’is üleslaadimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="51875-129">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="51875-130">Avage autorluse tööriistades oma sait.</span><span class="sxs-lookup"><span data-stu-id="51875-130">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="51875-131">Valige navigeerimispaanilt vasakult suvand **Kujundus**.</span><span class="sxs-lookup"><span data-stu-id="51875-131">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="51875-132">Sõltuvalt kasutatavast Commerce’i autorluse tööriistade versioonist, peate võib-olla laiendama navigeerimispaani suvandit **Sätted**, enne kui saate valida suvandi **Kujundus**.</span><span class="sxs-lookup"><span data-stu-id="51875-132">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="51875-133">Kui see ei ole juba valitud, valige põhidisaini vahekaardil **CSS-i alistamine**.</span><span class="sxs-lookup"><span data-stu-id="51875-133">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="51875-134">Jaotises **Saadaolevad CSS-i alistamised** valige käsk **Laadi CSS-fail üles**.</span><span class="sxs-lookup"><span data-stu-id="51875-134">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="51875-135">Kuvatakse File Exploreri aken.</span><span class="sxs-lookup"><span data-stu-id="51875-135">A File Explorer window appears.</span></span>
1. <span data-ttu-id="51875-136">File Exploreris sirvige ja valige CSS-fail ning seejärel valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="51875-136">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="51875-137">Üleslaaditud CSS-fail kuvatakse nüüd asukohas **Saadaolevad CSS-i alistamised**.</span><span class="sxs-lookup"><span data-stu-id="51875-137">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="51875-138">CSS-i alistamisfaili eelvaade</span><span class="sxs-lookup"><span data-stu-id="51875-138">Preview a CSS override file</span></span>

<span data-ttu-id="51875-139">CSS-i alistamisfaili eelvaate kuvamiseks enne, kui selle oma avaldatud saidil aktiveerite, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="51875-139">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="51875-140">Valige vasakpoolsel navigeerimispaanil suvand **Kujundus**ja seejärel otsige vahekaardil **CSS-i alistamine** jaotises **Saadaolevad CSS-i alistamised** üles CSS-fail, mille eelvaate soovite kuvada.</span><span class="sxs-lookup"><span data-stu-id="51875-140">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="51875-141">CSS-faili nime kõrval valige suvand **Saidi eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="51875-141">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="51875-142">Valige dialoogiaknas **URL-i valimine** saidi URL, mille suhtes soovite alistused rakendada, ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="51875-142">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="51875-143">Kui valitud URL-il on mitu varianti, valige kuvatavas dialoogiaknas **Eelvaate variatsioonid** soovitud variant.</span><span class="sxs-lookup"><span data-stu-id="51875-143">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="51875-144">Avatakse uus brauseri vahekaart või aken, kus saate kinnitada oma saidi laadi alistused.</span><span class="sxs-lookup"><span data-stu-id="51875-144">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="51875-145">Seejärel saate jagada URL-i teiste autenditud Commerce’i kasutajatega ülevaatamiseks ja tagasisideks.</span><span class="sxs-lookup"><span data-stu-id="51875-145">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="51875-146">CSS-i alistamisfailide avaldatud saidil aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="51875-146">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="51875-147">Kui olete vaadanud ja kinnitanud CSS-i alistamisfaili, saate selle oma avaldatud saidil aktiveerida.</span><span class="sxs-lookup"><span data-stu-id="51875-147">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="51875-148">Korraga saab teie saidil olla ainult üks CSS-i alistamisfail.</span><span class="sxs-lookup"><span data-stu-id="51875-148">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="51875-149">Kui aktiveerite uue alistamisfaili, eelmine alistamisfail desaktiveeritakse.</span><span class="sxs-lookup"><span data-stu-id="51875-149">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="51875-150">Seetõttu veenduge, et kõik nõutavad alistamised on olemas ühes CSS-i alistamisfailis.</span><span class="sxs-lookup"><span data-stu-id="51875-150">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="51875-151">CSS-i alistamisfaili aktiveerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="51875-151">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="51875-152">Valige vasakpoolsel navigeerimispaanil suvand **Kujundus** ja seejärel otsige vahekaardi **CSS-i alistamine** jaotises **Saadaolevad CSS-i alistamised**üles CSS-fail, mille soovite aktiveerida.</span><span class="sxs-lookup"><span data-stu-id="51875-152">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="51875-153">CSS-faili nime all valige **Aktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="51875-153">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="51875-154">Alistamisfail muutub kohe teie avaldatud saidil aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="51875-154">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="51875-155">CSS-i alistamisfailide avaldatud saidil desaktiveerimine</span><span class="sxs-lookup"><span data-stu-id="51875-155">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="51875-156">Oma saidil CSS-i alistamisfaili desaktiveerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="51875-156">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="51875-157">Valige vasakpoolsel navigeerimispaanil suvand **Kujundus** ja seejärel otsige vahekaardi **CSS-i alistamine** jaotises **Saadaolevad CSS-i alistamised** üles CSS-fail, mille soovite desaktiveerida.</span><span class="sxs-lookup"><span data-stu-id="51875-157">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="51875-158">CSS-faili nime all valige **Desaktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="51875-158">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="51875-159">Alistamisfail muutub kohe teie avaldatud saidil passiivseks.</span><span class="sxs-lookup"><span data-stu-id="51875-159">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="51875-160">CSS-i alistamisfailide täiendavate suvanditele juurdepääsuks valige kolmikpunkt (**...**) CSS-faili nime kõrval.</span><span class="sxs-lookup"><span data-stu-id="51875-160">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="51875-161">Suvandid **Laadi alla**, **Nimeta ümber** ja **Asenda** on kasulikud olemasoleva CSS-i alistamisfaili kiireks muutmiseks.</span><span class="sxs-lookup"><span data-stu-id="51875-161">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51875-162">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="51875-162">Additional resources</span></span>

[<span data-ttu-id="51875-163">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="51875-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="51875-164">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="51875-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="51875-165">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="51875-165">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="51875-166">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="51875-166">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="51875-167">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="51875-167">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="51875-168">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="51875-168">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="51875-169">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="51875-169">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
