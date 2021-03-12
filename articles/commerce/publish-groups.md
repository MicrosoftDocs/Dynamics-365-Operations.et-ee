---
title: Avaldamisrühmadega töötamine
description: Selles teemas kirjeldatakse avaldamisrühmade funktsiooni teenuses Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0a4f19af0cdf9c72add0ec18be84e36c807af9ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969872"
---
# <a name="work-with-publish-groups"></a><span data-ttu-id="e1da6-103">Avaldamisrühmadega töötamine</span><span class="sxs-lookup"><span data-stu-id="e1da6-103">Work with publish groups</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e1da6-104">Selles teemas kirjeldatakse avaldamisrühmade funktsiooni teenuses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e1da6-104">This topic describes the publish groups feature in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e1da6-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="e1da6-105">Overview</span></span>

<span data-ttu-id="e1da6-106">E-kaubanduse veebisaite uuendatakse pidevalt uue sisuga kogu aasta jooksul.</span><span class="sxs-lookup"><span data-stu-id="e1da6-106">E-commerce websites are constantly updated with new content throughout the year.</span></span> <span data-ttu-id="e1da6-107">Uuendused avaldatakse sageli partiidena kiirete e-kaubanduse sündmuste ajal, nagu pühad, hooajalised turunduskampaaniad või kampaania käivitamine.</span><span class="sxs-lookup"><span data-stu-id="e1da6-107">Updates are often published in batches around busy e-commerce events such as holidays, seasonal marketing campaigns, or promotional launches.</span></span> <span data-ttu-id="e1da6-108">Need uuendused nõuavad sageli, et veebisaitide sisu rümad (näiteks lehed, pildid, fragmendid ja mallid) oleksid ettevalmistatud, kontrollitud ja avaldatud samaaegselt ühe tegevusega.</span><span class="sxs-lookup"><span data-stu-id="e1da6-108">These updates often require that groups of website content (for examples, pages, images, fragments, and templates) be staged, validated, and published concurrently in a single action.</span></span>

<span data-ttu-id="e1da6-109">Üksuste koos avaldamiseks üksuste loogilistesse kogumitesse rühmitamise võimalus, kus igal kogumil on oma elutsükkel, pakub saidi autoritele palju eeliseid.</span><span class="sxs-lookup"><span data-stu-id="e1da6-109">The ability to group items into logical sets that publish items together, where each set has its own lifecycle, provides many advantages to site authors.</span></span> <span data-ttu-id="e1da6-110">Commerce’is on need loogilised kogumid tuntud kui avaldamisrühmad.</span><span class="sxs-lookup"><span data-stu-id="e1da6-110">In Commerce, these logical sets are known as publish groups.</span></span> <span data-ttu-id="e1da6-111">Nad võimaldavad saidi autoritel jälgida uuenduste kogumeid oma konfigureeritavate, testitavate ja avaldatavate üksustena.</span><span class="sxs-lookup"><span data-stu-id="e1da6-111">They let site authors track sets of updates as their own configurable, testable, and publishable entities.</span></span>

<span data-ttu-id="e1da6-112">Autorid saavad kuvada ettevalmistatud avaldamisrühma uuenduste eelvaate ilma reaalajas saiti ega teisi iseseisvaid avaldamisrühmi mõjutamata.</span><span class="sxs-lookup"><span data-stu-id="e1da6-112">Authors can preview updates in a staged publish group without affecting the live site or other self-contained publish groups.</span></span> <span data-ttu-id="e1da6-113">Autorid saavad seejärel ajastada avaldamistoimingu, et avaldada üheaegselt kõik avaldamisrühma üksused reaalajas saidil.</span><span class="sxs-lookup"><span data-stu-id="e1da6-113">Authors can then schedule the publish action to simultaneously publish all the items in the publish group to the live site.</span></span> <span data-ttu-id="e1da6-114">Avaldamiseks mõeldud uuenduste rühmitamine, eelvaate kuvamine ja ajastamine on oluline paljudele suurettevõtte tasemel ettevõtetele, mis saavad märkimisväärse iga-aastase tulu ettevõttepõhiste saidi uuenduste vahe-eesmärkide ajal.</span><span class="sxs-lookup"><span data-stu-id="e1da6-114">The ability to group, preview, and schedule updates for publishing is important for many enterprise-level companies that generate considerable annual revenue around event-based site update milestones.</span></span>

<span data-ttu-id="e1da6-115">Aeglane või kehtetuks muutunud sisu avaldamised, mis ei kulge sujuvalt, võivad tuua ettevõttele kaasa kulutusi.</span><span class="sxs-lookup"><span data-stu-id="e1da6-115">Companies can incur costs from slow or invalidated content rollouts that don't go smoothly.</span></span> <span data-ttu-id="e1da6-116">Avaldamisrühmad aitavad tagada, et käivitamised on korraldatud, kontrollitud ja õigeaegselt avaldatud.</span><span class="sxs-lookup"><span data-stu-id="e1da6-116">Publish groups help guarantee that launches are organized, validated, and published on time.</span></span> <span data-ttu-id="e1da6-117">Kas need on suured või väikesed, avaldamisrühmad pakuvad väärtuslikku tööriistakogumit, mis aitab autoritel korraldada ja lihtsustada jooksvaid saidi uuendamise ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="e1da6-117">Whether they are large or small, publish groups provide a valuable toolset that helps authors organize and simplify ongoing site update tasks.</span></span>

## <a name="when-to-use-publish-groups"></a><span data-ttu-id="e1da6-118">Millal avaldamisrühmasid kasutada?</span><span class="sxs-lookup"><span data-stu-id="e1da6-118">When to use publish groups</span></span>

<span data-ttu-id="e1da6-119">Saate kasutada avaldamisrühmasid, kui peate valmistama ette ja avaldama mitu dokumenti koos.</span><span class="sxs-lookup"><span data-stu-id="e1da6-119">You can use publish groups whenever you must stage and publish multiple documents together.</span></span> <span data-ttu-id="e1da6-120">Näiteks kui teie veebisait uuendab sisu igal hooajal, saate luua avaldamisrühmad nende hooajaliste turundusliigutuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="e1da6-120">For example, if your website updates content every season, you can create publish groups for these seasonal marketing motions.</span></span> <span data-ttu-id="e1da6-121">Teie avaldamisrühm „Sügise hooajalise uuendus” avaldamine võib sisaldada uusi hooajalisi pilte, hooajaliste turundussõnumitega fragmente, hooajaliste toodete kollektsioone sisaldavaid lehti ja teisi hooajalisi veebisaidi värskendusi.</span><span class="sxs-lookup"><span data-stu-id="e1da6-121">Your "Autumn Seasonal Update" publish group might contain new seasonal images, fragments that have seasonal marketing messages, pages that include seasonal product collections, or other seasonal website updates.</span></span>

<span data-ttu-id="e1da6-122">Avaldamisrühmade eeliseks on, et saate paralleelselt valmistada ette mitu uuendust.</span><span class="sxs-lookup"><span data-stu-id="e1da6-122">An advantage of publish groups is that you can stage multiple updates in parallel.</span></span> <span data-ttu-id="e1da6-123">Näiteks varsti pärast uuendust avaldamisrühmale „Sügise hooajaline uuendus” võib peagi järgneda konkreetse püha nädalavahetuse uuendus.</span><span class="sxs-lookup"><span data-stu-id="e1da6-123">For example, soon after the update for the "Autumn Seasonal Update" publish group, there might be a content update for a specific holiday weekend.</span></span> <span data-ttu-id="e1da6-124">Sel juhul saate avaldamisrühma „Sügise hooajaline uuendus” sisu valmistada ette samal ajal, kui valmistate ette järgnevat avaldamisrühma „Sügispuhkuse uuendus”</span><span class="sxs-lookup"><span data-stu-id="e1da6-124">In this case, you can stage content for the "Autumn Seasonal Update" publish group at the same time that you stage content for a subsequent "Autumn Holiday Update" publish group.</span></span> <span data-ttu-id="e1da6-125">Iga avaldamisrühm sisaldab oma ainulaadset lehtede, piltide, fragmentide, mallide jne komplekti.</span><span class="sxs-lookup"><span data-stu-id="e1da6-125">Each publish group contains its own unique set of pages, images, fragments, templates, and so on.</span></span> <span data-ttu-id="e1da6-126">Saate valmistada ette, kuvada eelvaade ja kinnitada need kaks avaldamisrühma sõltumatult, kuid samal aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="e1da6-126">You can stage, preview, and validate these two publish groups independently but on a concurrent timeline.</span></span> <span data-ttu-id="e1da6-127">Seejärel saab ajastada iga avaldamisrühma avaldamine teie saidil konkreetsetel kuupäevadel ja kellaaegadel.</span><span class="sxs-lookup"><span data-stu-id="e1da6-127">Each publish group can then be scheduled to go live on your site at specific dates and times.</span></span>

## <a name="turn-on-the-publish-groups-feature"></a><span data-ttu-id="e1da6-128">Avaldamisrühmade funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="e1da6-128">Turn on the publish groups feature</span></span>

<span data-ttu-id="e1da6-129">Avaldamisrühmade funktsioon on valikuline ja see tuleb saidi jaoks sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="e1da6-129">The publish groups feature is optional and must be turned for your site.</span></span>

<span data-ttu-id="e1da6-130">Commerce’i autorluse tööriistades oma saidi avaldamisrühmade funktsiooni sisselülitamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e1da6-130">To turn on the publish groups feature for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="e1da6-131">Vasakpoolsel navigeerimispaanil valige suvand **Saidi sätted** selle laiendamiseks.</span><span class="sxs-lookup"><span data-stu-id="e1da6-131">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="e1da6-132">Jaotises **Saidi sätted** valige suvand **Funktsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-132">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="e1da6-133">Seadke valik **Avaldamisrühmad** väärtusele **Sees**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-133">Set the **Publish groups** option to **On**.</span></span>

## <a name="create-a-publish-group"></a><span data-ttu-id="e1da6-134">Avaldamisrühma loomine</span><span class="sxs-lookup"><span data-stu-id="e1da6-134">Create a publish group</span></span>

<span data-ttu-id="e1da6-135">Commerce’i autorluse tööriistades ma saidi jaoks avaldamisrühma loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e1da6-135">To create a publish group for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="e1da6-136">Valige vasakpoolsel navigeerimispaanilt suvand **Avaldamisrühmad**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-136">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="e1da6-137">Valige ülemisel käsuribal suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-137">In the top command bar, select **New**.</span></span>
1. <span data-ttu-id="e1da6-138">Dialoogiboksi **Avaldamisrühma loomine** jaotises **Avaldamisrühma nimi** sisestage kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="e1da6-138">In the **Create Publish Group** dialog box, under **Publish Group Name**, enter a descriptive name.</span></span> <span data-ttu-id="e1da6-139">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-139">Then select **OK**.</span></span>

## <a name="set-the-publish-group-authoring-context"></a><span data-ttu-id="e1da6-140">Avaldamisrühma autorluse konteksti seadmine</span><span class="sxs-lookup"><span data-stu-id="e1da6-140">Set the publish group authoring context</span></span>

<span data-ttu-id="e1da6-141">Commerce’is on vaikimisi autorluse kontekst reaalajas saidi kontekst.</span><span class="sxs-lookup"><span data-stu-id="e1da6-141">In Commerce, the default authoring context is the live site context.</span></span> <span data-ttu-id="e1da6-142">Reaalajas saidi autorluse kontekst on vaikevaade, kus saate vaadata ja teha muudatusi otse oma veebisaidil, ilma avaldamisrühma kasutamata.</span><span class="sxs-lookup"><span data-stu-id="e1da6-142">The live site authoring context is the default view where you can view and make changes directly to your website without using a publish group.</span></span> <span data-ttu-id="e1da6-143">See näitab teie saidi avaldatud versiooni värskeimaid otseseid uuendusi.</span><span class="sxs-lookup"><span data-stu-id="e1da6-143">It represents the latest direct updates to the published version of your site.</span></span> <span data-ttu-id="e1da6-144">Kui konteksti juhtelemendil vasakpoolse navigeerimispaani jaotises **Avaldamiserühmad** kuvatakse saidi nimi **Reaalajas sait**, töötate reaalajas saidi autorluse kontekstis.</span><span class="sxs-lookup"><span data-stu-id="e1da6-144">If the context control under **Publish Groups** in the left navigation pane shows the name **Live site**, you're working in the live site authoring context.</span></span> <span data-ttu-id="e1da6-145">**Reaalajas sait** on konteksti juhtelemendi vaikenimi.</span><span class="sxs-lookup"><span data-stu-id="e1da6-145">**Live site** is the default name of the context control.</span></span> <span data-ttu-id="e1da6-146">Vastasel juhul kuvab konteksti juhtelement avaldamisrühma nime.</span><span class="sxs-lookup"><span data-stu-id="e1da6-146">Otherwise, the context control shows the name of a publish group.</span></span>

<span data-ttu-id="e1da6-147">Avaldamisrühmas töötamiseks peate lülituma selleks avaldamisrühma autorluse konteksti.</span><span class="sxs-lookup"><span data-stu-id="e1da6-147">To work in a publish group, you must switch to the publish group authoring context for it.</span></span> <span data-ttu-id="e1da6-148">Avaldamisrühma konteksti määramiseks järgige ühte järgmistest sammudest.</span><span class="sxs-lookup"><span data-stu-id="e1da6-148">To set the publish group context, follow one of these steps.</span></span>

- <span data-ttu-id="e1da6-149">Vasakpoolsel navigeerimispaanil valige konteksti juhtelement otse suvandist **Avaldamisrühmad** ja valige seejärel kuvatavas valikute loendis avaldamisrühma nimi.</span><span class="sxs-lookup"><span data-stu-id="e1da6-149">In the left navigation pane, select the context control directly under **Publish Groups**, and then select the name of the publish group in the list of options that appears.</span></span> <span data-ttu-id="e1da6-150">Konteksti juhtelement nimetatakse ümber ja see kuvab avaldamisrühma nime.</span><span class="sxs-lookup"><span data-stu-id="e1da6-150">The context control is renamed and shows the name of the publish group.</span></span>
- <span data-ttu-id="e1da6-151">Valige vasakpoolsel navigeerimispaanil suvand **Avaldamisrühmad** ja seejärel jaotises **Avaldamisrühmad** valige avaldamisrühma nimi.</span><span class="sxs-lookup"><span data-stu-id="e1da6-151">In the left navigation pane, select **Publish Groups**, and then, under **Publish Groups**, select the name of the publish group.</span></span> <span data-ttu-id="e1da6-152">Konteksti juhtelement nimetatakse ümber ja see kuvab avaldamisrühma nime.</span><span class="sxs-lookup"><span data-stu-id="e1da6-152">The context control is renamed and shows the name of the publish group.</span></span>

<span data-ttu-id="e1da6-153">Pärast avaldamisrühma autorluse konteksti määramist töötate selles avaldamisrühma kontekstis, kui kuvate eelvaate ja redigeerite saidi sisu.</span><span class="sxs-lookup"><span data-stu-id="e1da6-153">After you set your publish group authoring context, you're working in that publish group context when you preview and edit site content.</span></span>

<span data-ttu-id="e1da6-154">Vaikimisi reaalajas saidi autorluse konteksti naasmiseks valige konteksti juhtelement ja valige seejärel **Reaalajas sait**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-154">To return to the default live site authoring context, select the context control, and then select **Live site**.</span></span>

## <a name="add-pages-or-other-items-to-a-publish-group"></a><span data-ttu-id="e1da6-155">Avaldamisrühma lehtede ja teiste üksuste lisamine</span><span class="sxs-lookup"><span data-stu-id="e1da6-155">Add pages or other items to a publish group</span></span>

<span data-ttu-id="e1da6-156">Pärast avaldamisrühma autorluse konteksti valimist ja konteksti juhtelement vasakpoolsel navigatsioonipaanil kuvab selle nime, saate luua sisu samamoodi, nagu vaikimisi reaalajas saidi kontekstis.</span><span class="sxs-lookup"><span data-stu-id="e1da6-156">After you've selected a publish group authoring context, and the context control in the left navigation pane shows its name, you can create content just as you do in the default live site context.</span></span> <span data-ttu-id="e1da6-157">Saate lisada ka olemasolevaid lehti või teisi üksusi teistelt avaldamisrühmadest või reaalajas saidi kontekstist.</span><span class="sxs-lookup"><span data-stu-id="e1da6-157">You can also add existing pages or other items from other publish groups, or from the live site context.</span></span>

<span data-ttu-id="e1da6-158">Olemasolevate lehtede avaldamisrühma kopeerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e1da6-158">To copy existing pages to a publish group, follow these steps.</span></span>

1. <span data-ttu-id="e1da6-159">Valige autorluse kontekst, kust kopeerida, ja seejärel valige vasakpoolsel navigeerimispaanil suvand **Lehed**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-159">Select the authoring context to copy from, and then, in the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="e1da6-160">Valige leht avaldamisrühma lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="e1da6-160">Select the page to add to a publish group.</span></span>
1. <span data-ttu-id="e1da6-161">Valige käsuribal käsk **Kopeeri avaldamisrühma**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-161">In the command bar, select **Copy to Publish group**.</span></span>
1. <span data-ttu-id="e1da6-162">Valige dialoogiboksis **Avaldamisrühma valimine** avaldamisrühm, millele leht lisada, ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-162">In the **Select a Publish Group** dialog box, select the publish group to add the page to, and then select **OK**.</span></span>

<span data-ttu-id="e1da6-163">Saate kasutada samu põhisamme, et luua kohandatud tootelehti, URL-e, malle, paigutusi, fragmente ja meediumiteegi ressursse, või lisada seda tüübi avaldamisrühmadesse olemasolevaid üksuseid.</span><span class="sxs-lookup"><span data-stu-id="e1da6-163">You can use the same basic steps to create customized product pages, URLs, templates, layouts, fragments, and media library assets, or to add existing items of these types to a publish group.</span></span>

## <a name="validate-a-publish-group"></a><span data-ttu-id="e1da6-164">Avaldamisrühma valideerimine</span><span class="sxs-lookup"><span data-stu-id="e1da6-164">Validate a publish group</span></span>

<span data-ttu-id="e1da6-165">Kindlustamaks, et kõik sõltuvused avaldamisrühma sisus oleksid täidetud ja et kõik valideerimised oleksid läbitud, saate käitada valideerimise, et tuvastada mis tahes probleemid, mis tuleb enne avaldamistoimingu ajastamist lahendada.</span><span class="sxs-lookup"><span data-stu-id="e1da6-165">To make sure that all dependencies in publish group content are satisfied, and that all validations are passed, you can run validation to identify any issues that must be addressed before you schedule a publish action.</span></span>

<span data-ttu-id="e1da6-166">Avaldamisrühma valideerimiseks enne selle ajastamist tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e1da6-166">To validate your publish group before you schedule it, follow these steps.</span></span>

1. <span data-ttu-id="e1da6-167">Valige vasakpoolsel navigeerimispaanilt suvand **Avaldamisrühmad**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-167">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="e1da6-168">Valige valideerimiseks avaldamisrühm.</span><span class="sxs-lookup"><span data-stu-id="e1da6-168">Select the publish group to validate.</span></span>
1. <span data-ttu-id="e1da6-169">Valige ülemisel käsuribal suvand **Valideeri**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-169">In the command bar, select **Validate**.</span></span>

<span data-ttu-id="e1da6-170">Valideerimine käitatakse avaldamisrühma kogu sisul.</span><span class="sxs-lookup"><span data-stu-id="e1da6-170">Validation is run on all content in the publish group.</span></span> <span data-ttu-id="e1da6-171">Kõik probleemid, mis takistavad edukat avaldamistoimingut, näidatakse üleval paremal kuvatavas teavitusaknas.</span><span class="sxs-lookup"><span data-stu-id="e1da6-171">Any issues that will prevent a successful publish action are shown in a notification box that appears in the upper right.</span></span>

> [!NOTE]
> <span data-ttu-id="e1da6-172">Valideerimine käitatakse alati automaatselt, kui avaldamisrühm ajastatakse.</span><span class="sxs-lookup"><span data-stu-id="e1da6-172">Validation is always run automatically when a publish group is scheduled.</span></span> <span data-ttu-id="e1da6-173">Samas on nupp **Kinnita** käsuribal kasulik, kuna see aitab tuvastada probleemid, mille peate enne avaldamisrühma avaldamise ajastamise proovimist lahendama.</span><span class="sxs-lookup"><span data-stu-id="e1da6-173">However, the **Validate** button in the command bar is useful because it helps identify issues that you must fix before you try to schedule a publish group to go live.</span></span>

## <a name="schedule-a-publish-group-to-go-live"></a><span data-ttu-id="e1da6-174">Avaldamisrühma avaldamise ajastamine</span><span class="sxs-lookup"><span data-stu-id="e1da6-174">Schedule a publish group to go live</span></span>

<span data-ttu-id="e1da6-175">Oma saidil avaldamisrühma avaldamise ajastamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e1da6-175">To schedule a publish group to go live on your site, follow these steps.</span></span>

1. <span data-ttu-id="e1da6-176">Valige vasakpoolsel navigeerimispaanilt suvand **Avaldamisrühmad**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-176">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="e1da6-177">Valige jaotises **Avaldamisrühmad** ajastamiseks avaldamisrühm.</span><span class="sxs-lookup"><span data-stu-id="e1da6-177">Under **Publish Groups**, select the publish group to schedule.</span></span>
1. <span data-ttu-id="e1da6-178">Valige ülemisel käsuribal suvand **Graafiku redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-178">In the command bar, select **Edit Schedule**.</span></span> <span data-ttu-id="e1da6-179">Ilmub dialoogiboks **Graafiku redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-179">The **Edit Schedule** dialog box appears.</span></span>
1. <span data-ttu-id="e1da6-180">Valige kuupäev ja kellaaeg, millal avaldamisrühm peaks avaldatama, ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-180">Select the date and time when your publish group should go live, and then select **OK**.</span></span>

<span data-ttu-id="e1da6-181">Avaldamisrühma graafikust eemaldamiseks järgige samu etappe, kuid valige käsk **Eemalda avaldamisrühm ajakavast** dialoogiboksis **Ajakava redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="e1da6-181">To unschedule a publish group, follow the same steps, but select **Unschedule publish group** in the **Edit Schedule** dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="e1da6-182">Väga suurtel avaldamiserühmadel võib kuluda üks kuni kaks minutit, et need planeeritud aja kättejõudmisel avaldataks.</span><span class="sxs-lookup"><span data-stu-id="e1da6-182">Very large publish groups might take up to a minute or two to be published when their scheduled time arrives.</span></span> <span data-ttu-id="e1da6-183">Arvestage, et avaldamistoiming ei ole hetkeline ja väiksemad avaldamisrühmad avaldatakse kiiremini.</span><span class="sxs-lookup"><span data-stu-id="e1da6-183">Be aware that a publish action isn't instantaneous, and that smaller publish groups will be published faster.</span></span>

## <a name="publish-groups-faq"></a><span data-ttu-id="e1da6-184">Avaldamisrühmade KKK</span><span class="sxs-lookup"><span data-stu-id="e1da6-184">Publish groups FAQ</span></span>

<span data-ttu-id="e1da6-185">**Mitu üksust võib avaldamisrühmas olla?**</span><span class="sxs-lookup"><span data-stu-id="e1da6-185">**How many items can be in a publish group?**</span></span>

<span data-ttu-id="e1da6-186">Praegu on piir 2000 üksust avaldamisrühma kohta.</span><span class="sxs-lookup"><span data-stu-id="e1da6-186">Currently, there is a limit of 2,000 items per publish group.</span></span> <span data-ttu-id="e1da6-187">Arvestage, et väga suurtel avaldamiserühmadel võib kuluda kuni mitu minutit, et need planeeritud aja kättejõudmisel avaldataks.</span><span class="sxs-lookup"><span data-stu-id="e1da6-187">Be aware that very large publish groups might take several minutes to be published when their scheduled time arrives.</span></span>

<span data-ttu-id="e1da6-188">**Kas avaldamisrühmad on tarkvaraarenduse terminoloogias nagu koodi nn harud?**</span><span class="sxs-lookup"><span data-stu-id="e1da6-188">**Are publish groups like code "branches" in software development terminology?**</span></span>

<span data-ttu-id="e1da6-189">Jah ja ei.</span><span class="sxs-lookup"><span data-stu-id="e1da6-189">Yes and no.</span></span> <span data-ttu-id="e1da6-190">Avaldamisrühmi võib vaadelda kui teie saidi haralisi versioone.</span><span class="sxs-lookup"><span data-stu-id="e1da6-190">Publish groups can be thought of as forked versions of your site.</span></span> <span data-ttu-id="e1da6-191">Sel viisil käituvad need nagu harud.</span><span class="sxs-lookup"><span data-stu-id="e1da6-191">In that way, they do act like branches.</span></span> <span data-ttu-id="e1da6-192">Samas üksikute üksuste tasandil liitumise konseptsioon puudub.</span><span class="sxs-lookup"><span data-stu-id="e1da6-192">However, there is no concept of a merge at the level of individual items.</span></span> <span data-ttu-id="e1da6-193">Viimati avaldatud üksus lihtsalt kirjutab üle varem eksisteerinu ja kõige viimane avaldamistoiming alati alistab eelmised avaldamistoimingud.</span><span class="sxs-lookup"><span data-stu-id="e1da6-193">The item that is published last just overwrites what previously existed, and the most recent publish action always supersedes previous publish actions.</span></span>

<span data-ttu-id="e1da6-194">**Kas ma saan planeerida kahe avaldamisrühma avaldamise samal ajal?**</span><span class="sxs-lookup"><span data-stu-id="e1da6-194">**Can I schedule two publish groups to go live at the same time?**</span></span>

<span data-ttu-id="e1da6-195">Ei.</span><span class="sxs-lookup"><span data-stu-id="e1da6-195">No.</span></span> <span data-ttu-id="e1da6-196">Jõudluse ja konflikti tõttu sunnib süsteem teid jätma kahe avaldamisrühma vahele vähemalt viis minutit aega.</span><span class="sxs-lookup"><span data-stu-id="e1da6-196">For performance and conflict reasons, the system will force you to stagger scheduled publish groups at least five minutes apart.</span></span>

<span data-ttu-id="e1da6-197">**Kas ma saan kasutada avaldamisrühmi, et ajasada omnikanali arveldusüksuseid, nagu allahindlused ja toote uuendused?**</span><span class="sxs-lookup"><span data-stu-id="e1da6-197">**Can I use publish groups to schedule omnichannel back-office items, such as discounts and product updates?**</span></span>

<span data-ttu-id="e1da6-198">Praegu toetab avaldamisrühmade funktsioon ainult veebisaidi sisu.</span><span class="sxs-lookup"><span data-stu-id="e1da6-198">Currently, the publish groups feature supports only website content.</span></span> <span data-ttu-id="e1da6-199">Kuid Microsoft on teadlik, et kontorikaupade stsenaariumitega integreerimine võib olla väärtuslik omnikanali kampaania käivitamiste koordineerimiseks ja automatiseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="e1da6-199">However, Microsoft is aware that integration with back-office merchandising scenarios could be valuable for the coordination and automation of omnichannel campaign launches.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1da6-200">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e1da6-200">Additional resources</span></span>

[<span data-ttu-id="e1da6-201">Sisu lisamise viisid</span><span class="sxs-lookup"><span data-stu-id="e1da6-201">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="e1da6-202">Lehemudeli sõnastik</span><span class="sxs-lookup"><span data-stu-id="e1da6-202">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="e1da6-203">Dokumendi olekud ja töötsükkel</span><span class="sxs-lookup"><span data-stu-id="e1da6-203">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="e1da6-204">Kanaliülese ühiskasutuse lubamine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="e1da6-204">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="e1da6-205">Moodulitega töötamine</span><span class="sxs-lookup"><span data-stu-id="e1da6-205">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="e1da6-206">Fragmentidega töötamine</span><span class="sxs-lookup"><span data-stu-id="e1da6-206">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="e1da6-207">Mallide ja paigutuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="e1da6-207">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="e1da6-208">Saidil navigeerimise kohandamine</span><span class="sxs-lookup"><span data-stu-id="e1da6-208">Customize site navigation</span></span>](customize-site-navigation.md)
