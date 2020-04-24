---
title: Mis onuut või mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.6 (november 2019)
description: Selles teemas kirjeldatakse Dynamics 365 Supply Chain Management 10.0.6 uusi või muutunud funktsioone.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac1
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 319ba09184c087a194b664ca87076d57c6ba0c66
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201544"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="ff32c-103">Mis onuut või mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.6 (november 2019)</span><span class="sxs-lookup"><span data-stu-id="ff32c-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff32c-104">Selles teemas kirjeldatakse Microsoft Dynamics 365 Supply Chain Management 10.0.6 uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="ff32c-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="ff32c-105">Selle versioonijärgu number on 10.0.234.</span><span class="sxs-lookup"><span data-stu-id="ff32c-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="ff32c-106">Kuigi üldise kättesaadavuse kuupäev on plaanitud novembrisse, on uued funktsioonid saadaval ka varajases väljalaskes oktoobris.</span><span class="sxs-lookup"><span data-stu-id="ff32c-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="ff32c-107">Lisateabe saamiseks versiooni 10.0.6 kohta vt [Lisaressurssid](whats-new-scm-10-0-6.md#additional-resources).</span><span class="sxs-lookup"><span data-stu-id="ff32c-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="ff32c-108">Toote konfiguratsioonimudelite V2 andmeüksus</span><span class="sxs-lookup"><span data-stu-id="ff32c-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="ff32c-109">Antakse välja „Toote konfiguratsioonimudelite” andmeüksuse teine versioon (nn „toodete konfiguratsioonimudelid V2”).</span><span class="sxs-lookup"><span data-stu-id="ff32c-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="ff32c-110">Vaikemall „418-toote konfiguratsioonimudelid” peab olema nii, et see kasutaks importimise/eksportimise raamistiku mallides uut andmeüksust „toote konfiguratsioonimudelid V2”.</span><span class="sxs-lookup"><span data-stu-id="ff32c-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="ff32c-111">Malli ei uuendata automaatselt, see tuleb vaikemallist käsitsi laadida.</span><span class="sxs-lookup"><span data-stu-id="ff32c-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="ff32c-112">V2-üksus ekspordib ühe rea tekstisisese asemel eraldi manustatud failina, mis lahendab V1-üksuse suurusepiirangud.</span><span class="sxs-lookup"><span data-stu-id="ff32c-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="ff32c-113">Mida peate selle muudatuse hankimiseks tegema?</span><span class="sxs-lookup"><span data-stu-id="ff32c-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="ff32c-114">Kuna V1-üksus on aegunud, peaksite alustama V1 üleminekut V2-le.</span><span class="sxs-lookup"><span data-stu-id="ff32c-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="ff32c-115">Kui kasutate malli „418-toote konfiguratsioonimudelid”, saate klõpsata nuppu „laadi vaikemallid” ja laadida malli „418‑toote konfiguratsioonimudelid” uuesti</span><span class="sxs-lookup"><span data-stu-id="ff32c-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="ff32c-116">Kui teil on vaja säilitada ühilduvus olemasolevate süsteemidega, saate nüüd jätkata olemasoleva malli ja (aegunud) V1-üksuse kasutamist, kuni te teisaldate oma integratsiooni uuele mallile.</span><span class="sxs-lookup"><span data-stu-id="ff32c-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="ff32c-117">Funktsioonihalduse täiustused</span><span class="sxs-lookup"><span data-stu-id="ff32c-117">Feature management enhancements</span></span>
<span data-ttu-id="ff32c-118">Funktsioonide haldus võimaldab teil nüüd lubada kõik uued funktsioonid vaikimisi, nõuda funktsiooni lubamiseks kinnitust ja lubada kõik funktsioonid, mis pole veel lubatud.</span><span class="sxs-lookup"><span data-stu-id="ff32c-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="ff32c-119">Ostulepingu vastutav isik</span><span class="sxs-lookup"><span data-stu-id="ff32c-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="ff32c-120">Nüüd on teil võimalus määratleda esmased ja teisesed vastutavad osapooled ostulepingu klassifikatsioonivormil ja tulenevatel ostulepingutel.</span><span class="sxs-lookup"><span data-stu-id="ff32c-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="ff32c-121">See annab lepingute järelevalvet teostavale kasutajale juurdepääsu.</span><span class="sxs-lookup"><span data-stu-id="ff32c-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="ff32c-122">Pakkumiskutse link ostutellimuse real</span><span class="sxs-lookup"><span data-stu-id="ff32c-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="ff32c-123">Saate lisada ostutellimuse reale viitava lingi vastavale pakkumiskutse reale, kust need pärit on, võimaldades kasutajal hõlpsasti vaadata täiendavat pakkumiskutse dokumenti.</span><span class="sxs-lookup"><span data-stu-id="ff32c-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff32c-124">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ff32c-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ff32c-125">Veaparandused</span><span class="sxs-lookup"><span data-stu-id="ff32c-125">Bug fixes</span></span>
<span data-ttu-id="ff32c-126">Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.6 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span><span class="sxs-lookup"><span data-stu-id="ff32c-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="ff32c-127">Platvormivärskendus update 30</span><span class="sxs-lookup"><span data-stu-id="ff32c-127">Platform update 30</span></span>
<span data-ttu-id="ff32c-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 sisaldab Platform update'i 30.</span><span class="sxs-lookup"><span data-stu-id="ff32c-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="ff32c-129">Lisateavet Platform Update 30 kohta leiate teemast [Mis on uut või muudetud rakenduses Platform Update'is 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span><span class="sxs-lookup"><span data-stu-id="ff32c-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="ff32c-130">Dynamics 365 2019. aasta väljalaske 2. voo plaan</span><span class="sxs-lookup"><span data-stu-id="ff32c-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="ff32c-131">Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?</span><span class="sxs-lookup"><span data-stu-id="ff32c-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="ff32c-132">Vaadake teemat [Dynamics 365: 2019. aasta väljalaske 2. voo plaan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span><span class="sxs-lookup"><span data-stu-id="ff32c-132">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="ff32c-133">Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.</span><span class="sxs-lookup"><span data-stu-id="ff32c-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="ff32c-134">Eemaldatud ja aegunud Supply Chain Managementi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="ff32c-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="ff32c-135">Teemas [Eemaldatud või aegunud Dynamics 365 Supply Chain Managementi funktsioonid](removed-deprecated-features-scm-updates.md) kirjeldatakse funktsioone, mis on eemaldatud või aegunud või kavandatakse eemaldada Supply Chain Managementist.</span><span class="sxs-lookup"><span data-stu-id="ff32c-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="ff32c-136">*Eemaldatud* funktsioon pole tootes enam saadaval.</span><span class="sxs-lookup"><span data-stu-id="ff32c-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="ff32c-137">*Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.</span><span class="sxs-lookup"><span data-stu-id="ff32c-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="ff32c-138">Enne mis tahes funktsiooni eemaldamist tootest, teavitatakse aegumisest 12 kuud ette teemas [Eemaldatud või aegunud Dynamics 365 Supply Chain Managementi funktsioonid](removed-deprecated-features-scm-updates.md).</span><span class="sxs-lookup"><span data-stu-id="ff32c-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="ff32c-139">Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud.</span><span class="sxs-lookup"><span data-stu-id="ff32c-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="ff32c-140">Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.</span><span class="sxs-lookup"><span data-stu-id="ff32c-140">Typically, these are functional updates that need to be made to the compiler.</span></span>
