---
title: Regulatory Configuration Services (RCS) – globaliseerimise funktsioonid
description: Selles teemas selgitatakse, kuidas kasutada rakendust Microsoft Regulatory Configuration Services (RCS) ja globaalset hoidlat globaliseerimise funktsioonide loomiseks ja kasutamiseks.
author: JaneA07
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: cbb1d9a53a7a09ab525532f08553898c4e40223a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822777"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="1130c-103">Regulatory Configuration Services (RCS) – globaliseerimise funktsioonid</span><span class="sxs-lookup"><span data-stu-id="1130c-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1130c-104">Te saate kasutada rakendust Microsoft Regulatory Configuration Services (RCS) sellise globaliseerimise funktsiooni loomiseks, mida saab kasutada globaliseerimise teenuste raames, nagu näiteks e-arvete teenus.</span><span class="sxs-lookup"><span data-stu-id="1130c-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="1130c-105">RCS võimaldab teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="1130c-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="1130c-106">Saate määratleda funktsiooniga seotud komponendid.</span><span class="sxs-lookup"><span data-stu-id="1130c-106">Define related components of a feature.</span></span>
- <span data-ttu-id="1130c-107">Saate funktsiooni oleku kaudu hallata funktsiooni töötsüklit.</span><span class="sxs-lookup"><span data-stu-id="1130c-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="1130c-108">Saate luua määratletud keskkondadele kättesaadava funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="1130c-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="1130c-109">Saate jagada funktsiooni teiste organisatsioonidega.</span><span class="sxs-lookup"><span data-stu-id="1130c-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="1130c-110">Järgmised protseduurid selgitavad, kuidas kasutaja saab RCS-is lisada globaliseerimise funktsioone ja seotud komponente, uuendada funktsiooni olekut ja muuta funktsiooni kättesaadavaks, et seda saaks kasutada globaliseerimise teenustes.</span><span class="sxs-lookup"><span data-stu-id="1130c-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="1130c-111">Enne protseduuride lõpule viimist peate lõpule viima järgmiste toimingutega seotud etapid.</span><span class="sxs-lookup"><span data-stu-id="1130c-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="1130c-112">Juurdepääs RCS-i eksemplarile.</span><span class="sxs-lookup"><span data-stu-id="1130c-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="1130c-113">Konfiguratsioonipakkuja loomine ja aktiveerimine.</span><span class="sxs-lookup"><span data-stu-id="1130c-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="1130c-114">Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="1130c-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="1130c-115">Toimige Finance and Operations-i rakenduste eksemplaris järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1130c-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="1130c-116">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="1130c-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="1130c-117">Kui teie ettevõtte jaoks pole RCS-i keskkonda ette valmistatud, valige **Regulatory services – konfiguratsioon** ja seejärel järgige juhised selle ettevalmistamiseks.</span><span class="sxs-lookup"><span data-stu-id="1130c-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="1130c-118">Kui teie ettevõtte jaoks on RCS-i keskkond juba ette valmistatud, kasutage keskkonnale juurde pääsemiseks lehe URL-i, valides sisselogimise suvandi.</span><span class="sxs-lookup"><span data-stu-id="1130c-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="1130c-119">Globaliseerimise funktsioonide sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="1130c-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="1130c-120">Valige oma RCS-i eksemplaris paan **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="1130c-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="1130c-121">Valige tööruumis **Funktsioonihaldus** loendist suvand **Globaliseerimise funktsioonid** ja seejärel valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="1130c-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![Globaliseerimise funktsioonid funktsioonihalduses](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="1130c-123">Globaliseerimisfunktsioonid</span><span class="sxs-lookup"><span data-stu-id="1130c-123">Globalization features</span></span>

<span data-ttu-id="1130c-124">Globaliseerimise funktsioonide kasutamiseks peate selle esmalt importima globaalsest hoidlast ja looma sellest enda versiooni.</span><span class="sxs-lookup"><span data-stu-id="1130c-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="1130c-125">Globaliseerimise funktsioonide lisamiseks on kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="1130c-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="1130c-126">Saate lisada avaldatud või jagatud olemasoleva funktsiooni alusel tuletatud funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="1130c-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="1130c-127">Saate lisada uue funktsiooni, mille olete loonud nullist.</span><span class="sxs-lookup"><span data-stu-id="1130c-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="1130c-128">Juurdepääs globaliseerimise funktsioonidele</span><span class="sxs-lookup"><span data-stu-id="1130c-128">Access Globalization features</span></span>

1. <span data-ttu-id="1130c-129">Veenduge, et funktsioon **Globaliseerimise funktsioonid** on funktsioonihalduses sisse lülitatud, nagu varasemalt käesolevas teemas kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="1130c-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="1130c-130">Avage uus tööruum **Globaliseerimise funktsioonid** ja valige seejärel jaotisest **Funktsioonid** paan **E-arved**.</span><span class="sxs-lookup"><span data-stu-id="1130c-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![Globaalsete funktsioonide tööruum](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="1130c-132">Leht **E-arvete funktsioonid** on avatud.</span><span class="sxs-lookup"><span data-stu-id="1130c-132">The **e-Invoicing Features** page is opened.</span></span>

    ![E-arvete funktsioonide leht](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="1130c-134">Tuletatud globaliseerimise funktsiooni lisamine</span><span class="sxs-lookup"><span data-stu-id="1130c-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="1130c-135">Saate lisada uue globaliseerimise funktsiooni, tuletades selle juba avaldatud või jagatud olemasolevast funktsioonist.</span><span class="sxs-lookup"><span data-stu-id="1130c-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="1130c-136">Valige lehe **Globaalsest hoidlast funktsiooni importimine** avamiseks suvand **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="1130c-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![Globaalse hoidla lehelt funktsiooni importimine](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="1130c-138">Uusimate funktsioonide toomiseks valige **Sünkrooni**.</span><span class="sxs-lookup"><span data-stu-id="1130c-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="1130c-139">Sünkroonitud loetelu hõlmab funktsioone, mis on teile saadaval seetõttu, et need avaldati Microsofti poolt, või seetõttu, et neid jagas teiega mõni teine konfiguratsioonipakkuja.</span><span class="sxs-lookup"><span data-stu-id="1130c-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![Funktsioonide sünkroonitud loetelu](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="1130c-141">Valige loetelus imporditavad funktsioonid ja seejärel **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="1130c-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="1130c-142">Te saate teate, kui valitud funktsioonid on edukalt imporditud.</span><span class="sxs-lookup"><span data-stu-id="1130c-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![Teade eduka importimise kohta](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="1130c-144">Valige **Lisa** ja seejärel valige dialoogiakna ripploendist suvand **Olemasoleval versioonil põhinev**.</span><span class="sxs-lookup"><span data-stu-id="1130c-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="1130c-145">Sisestage funktsiooni nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="1130c-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="1130c-146">Valige saadaolevate funktsioonide loetelust funktsiooni alusversioon ja seejärel valige **Loo funktsioon**.</span><span class="sxs-lookup"><span data-stu-id="1130c-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![Tuletatud funktsiooni lisamine](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="1130c-148">Lisatud funktsioon on loodud ja selle olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="1130c-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![Mustandi olekuga tuletatud funktsioon](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="1130c-150">Vaadake üle funktsiooni komponendid, et teha kindlaks, kas värskendused on vajalikud.</span><span class="sxs-lookup"><span data-stu-id="1130c-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="1130c-151">Vaadake üle konfiguratsioonid, juhuks kui peate kohandama elektroonilise aruandluse vorminguid ja nende seotust funktsiooniversiooni vorminguvastendustega.</span><span class="sxs-lookup"><span data-stu-id="1130c-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="1130c-152">Vaadake seadistused üle, juhuks kui peate kohandama funktsiooniversiooni vahekaarti **Tegevused**, vahekaarti **Rakendatavuse reeglid** või vahekaarti **Muutujad**.</span><span class="sxs-lookup"><span data-stu-id="1130c-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="1130c-153">Valige vahekaardil **Versioonid** kuupäev **Kehtiv alates** ja sisestage kirjeldus, kui väli **Kirjeldus** on tühi.</span><span class="sxs-lookup"><span data-stu-id="1130c-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="1130c-154">Valige funktsiooni lõpule viimiseks suvand **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="1130c-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="1130c-155">Lõpule viidud funktsioonid saab muuta kättesaadavaks konkreetsele keskkonnale, et seda saaks kasutada globaliseerimise teenustes, või neid saab avaldada globaalses hoidlas.</span><span class="sxs-lookup"><span data-stu-id="1130c-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="1130c-156">Funktsioone, mille suvandi **Funktsiooniversiooni olek** on **Avaldatud**, saab jagada väliste organisatsioonidega.</span><span class="sxs-lookup"><span data-stu-id="1130c-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="1130c-157">Uue globaliseerimise funktsiooni lisamine</span><span class="sxs-lookup"><span data-stu-id="1130c-157">Add a new Globalization feature</span></span>

<span data-ttu-id="1130c-158">Saate lisada uue globaliseerimise funktsiooni, luues selle nullist.</span><span class="sxs-lookup"><span data-stu-id="1130c-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="1130c-159">Valige lehel **Globaalsest hoidlast funktsiooni importimine** suvand **Lisa** ja seejärel valige dialoogiakna ripploendis suvand **Uus funktsioon**.</span><span class="sxs-lookup"><span data-stu-id="1130c-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="1130c-160">Sisestage funktsiooni nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="1130c-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="1130c-161">Valige **Loo funktsioon**.</span><span class="sxs-lookup"><span data-stu-id="1130c-161">Select **Create feature**.</span></span>

    ![Uue funktsiooni lisamine](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="1130c-163">Valige vahekaardil **Versioonid** suvandi **Kehtiv alates** kuupäev ja seejärel valige funktsiooni lõpule viimiseks suvand **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="1130c-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="1130c-164">Lõpule viidud funktsioonid saab muuta kättesaadavaks konkreetsele keskkonnale, et seda saaks kasutada globaliseerimise teenustes, või neid saab avaldada globaalses hoidlas.</span><span class="sxs-lookup"><span data-stu-id="1130c-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="1130c-165">Funktsioone, mille suvandi **Funktsiooniversiooni olek** on **Avaldatud**, saab jagada väliste organisatsioonidega.</span><span class="sxs-lookup"><span data-stu-id="1130c-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="1130c-166">Funktsiooni komponendi ülevaade</span><span class="sxs-lookup"><span data-stu-id="1130c-166">Feature component overview</span></span>

<span data-ttu-id="1130c-167">Globaliseerimise funktsioonidel on mitu komponenti.</span><span class="sxs-lookup"><span data-stu-id="1130c-167">Globalization features have several components:</span></span>

- <span data-ttu-id="1130c-168">**Versioon** – see komponent toetab funktsiooni töötsükli haldust ja võimaldab kasutajatel hallata funktsiooni erinevate versioonide olekut.</span><span class="sxs-lookup"><span data-stu-id="1130c-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="1130c-169">**Konfiguratsioonid** – see komponent võimaldab kasutajatel hallata, kuvada ja redigeerida seotud elektroonilise aruandluse vorminguid ja vorminguvastendusi.</span><span class="sxs-lookup"><span data-stu-id="1130c-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="1130c-170">**Seadistused** – see komponent võimaldab globaliseerimise teenuste, nt e-arvete teenus, kasutajatel hallata seotud funktsiooni versiooni seadistusi.</span><span class="sxs-lookup"><span data-stu-id="1130c-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="1130c-171">Seega toetab see paindlike suhtlemise ja vastuste reeglite ülesehitamist.</span><span class="sxs-lookup"><span data-stu-id="1130c-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="1130c-172">**Keskkond** – see komponent võimaldab globaliseerumise teenuste, nt e-arvete teenus, kasutajatel hallata keskkonda, kus funktsiooni versiooni seadistust kasutatakse, ja annab volituse kasutajatele, kellel saab olema sellele juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="1130c-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="1130c-173">**Organisatsioonid** – see komponent võimaldab kasutajatel jagada funktsiooni väliste organisatsioonidega.</span><span class="sxs-lookup"><span data-stu-id="1130c-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="1130c-174">Funktsiooni komponentide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1130c-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="1130c-175">Versioon ja olek</span><span class="sxs-lookup"><span data-stu-id="1130c-175">Version and status</span></span>

<span data-ttu-id="1130c-176">Versiooni kasutatakse globaliseerimise funktsiooni töötsükli haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="1130c-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="1130c-177">Olekut saab muuta vahekaardi **Versioon** väljal **Olek**. Saadaval on järgmised olekud.</span><span class="sxs-lookup"><span data-stu-id="1130c-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="1130c-178">**Mustand** – funktsiooni saab muuta vaid selles olekus.</span><span class="sxs-lookup"><span data-stu-id="1130c-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="1130c-179">**Lõpule viidud** – funktsioon ja kõik seotud komponendid on lõpetatud (lõpule viidud) ja neid ei saa redigeerida.</span><span class="sxs-lookup"><span data-stu-id="1130c-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="1130c-180">**Avaldatud** – funktsioon ja kõik seotud komponendid on avaldatud globaalses hoidlas.</span><span class="sxs-lookup"><span data-stu-id="1130c-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="1130c-181">**Ühiskasutuses** – funktsioon ja kõik seotud komponendid on ühiskasutuses väliste organisatsioonidega.</span><span class="sxs-lookup"><span data-stu-id="1130c-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="1130c-182">**Lubatud** – funktsioon ja kõik seotud komponendid on globaliseerimise teenuses, nt e-arvete teenus, kasutamiseks lubatud.</span><span class="sxs-lookup"><span data-stu-id="1130c-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="1130c-183">Mõnest olekust peavad funktsioonid järjekorras läbi liikuma.</span><span class="sxs-lookup"><span data-stu-id="1130c-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="1130c-184">Seega ei pruugi iga olek igas elutsükli etapis saadaval olla.</span><span class="sxs-lookup"><span data-stu-id="1130c-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="1130c-185">Konfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="1130c-185">Configurations</span></span>

<span data-ttu-id="1130c-186">Konfiguratsioonide puhul on saadaval järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="1130c-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="1130c-187">**Kuvamine** – saate kuvada aluseks olevaid funktsiooni konfiguratsioone, mis ei vaja uuendamist.</span><span class="sxs-lookup"><span data-stu-id="1130c-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="1130c-188">**Redigeerimine** – saate valitud konfiguratsioonist mustandiversiooni, et saaksite redigeerida vormingut ja vorminguvastendust vormingukujundajas.</span><span class="sxs-lookup"><span data-stu-id="1130c-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="1130c-189">**Kustutamine** – saate kustutada funktsioonist valitud konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="1130c-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="1130c-190">**Aluse muutmine** – saate muuta funktsiooni alust.</span><span class="sxs-lookup"><span data-stu-id="1130c-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="1130c-191">Lisateabe saamiseks vaadake allpool käesoleva teema jaotises [Tuletatud globaliseerimise funktsioonide aluse muutmine](#rebase).</span><span class="sxs-lookup"><span data-stu-id="1130c-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="1130c-192">Seadistused</span><span class="sxs-lookup"><span data-stu-id="1130c-192">Setups</span></span>

<span data-ttu-id="1130c-193">Funktsioonide seadistuste puhul on saadaval järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="1130c-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="1130c-194">**Lisamine** – saate luua uue funktsiooni seadistuse.</span><span class="sxs-lookup"><span data-stu-id="1130c-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="1130c-195">Selle funktsiooni seadistuse saab tuletada olemasolevast funktsiooni seadistusest või luua nullist.</span><span class="sxs-lookup"><span data-stu-id="1130c-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="1130c-196">**Kustutamine** – saate kustutada valitud funktsiooni seadistuse.</span><span class="sxs-lookup"><span data-stu-id="1130c-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="1130c-197">**Kuvamine** – saate kuvada aluseks olevat funktsiooni seadistust, mis ei vaja muudatusi.</span><span class="sxs-lookup"><span data-stu-id="1130c-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="1130c-198">**Redigeerimine** – saate luua, kustutada või muuta funktsiooni seadistuse kolme põhikomponendi atribuute.</span><span class="sxs-lookup"><span data-stu-id="1130c-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="1130c-199">Tegevused ja nende parameetrid</span><span class="sxs-lookup"><span data-stu-id="1130c-199">Actions and their parameters</span></span>
    - <span data-ttu-id="1130c-200">Kohaldatavusreeglid</span><span class="sxs-lookup"><span data-stu-id="1130c-200">Applicability rules</span></span>
    - <span data-ttu-id="1130c-201">Muutujad</span><span class="sxs-lookup"><span data-stu-id="1130c-201">Variables</span></span>

![Funktsiooni versiooni seadistamise leht](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="1130c-203">Keskkonnad</span><span class="sxs-lookup"><span data-stu-id="1130c-203">Environments</span></span>

<span data-ttu-id="1130c-204">Keskkondade puhul on saadaval järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="1130c-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="1130c-205">**Lubamine** – valige valitud funktsiooniversiooni jaoks avaldatud keskkond ja valige **Kehtiv alates** kuupäev, millest alates see peaks olema kättesaadav.</span><span class="sxs-lookup"><span data-stu-id="1130c-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="1130c-206">Lisateabe saamiseks vaadake allpool käesoleva teema jaotises [Lubamise jaoks keskkondade konfigureerimine](#configureenvironment).</span><span class="sxs-lookup"><span data-stu-id="1130c-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="1130c-207">**Tühistamine** – saate eemaldada funktsiooni seadistuse keskkonna.</span><span class="sxs-lookup"><span data-stu-id="1130c-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="1130c-208">Organisatsioonid</span><span class="sxs-lookup"><span data-stu-id="1130c-208">Organizations</span></span>

<span data-ttu-id="1130c-209">Globaliseerimise funktsiooni välisele organisatsioonile ühiskasutuseks andmiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1130c-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="1130c-210">Valige lehel **E-arvete funktsioonid** ühiskasutusse antav funktsioon ja funktsiooniversioon.</span><span class="sxs-lookup"><span data-stu-id="1130c-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="1130c-211">Valige vahekaardil **Organisatsioonid** suvand **Anna ühiskasutusse** ja seejärel sisestage dialoogiakna rippmenüüs organisatsiooni domeeninimi.</span><span class="sxs-lookup"><span data-stu-id="1130c-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="1130c-212">Valige **Anna ühiskasutusse**.</span><span class="sxs-lookup"><span data-stu-id="1130c-212">Select **Share**.</span></span>

    ![Funktsiooni organisatsiooni jaoks ühiskasutusse andmine](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="1130c-214">Funktsioon on antud ühiskasutusse valitud organisatsiooniga ja on selle organisatsiooni jaoks globaalses hoidlas kättesaadav.</span><span class="sxs-lookup"><span data-stu-id="1130c-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="1130c-215">Sealt saab funktsiooni importida kasutamiseks organisatsiooni RCS-i või Dynamics 365 Finance'i eksemplari.</span><span class="sxs-lookup"><span data-stu-id="1130c-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="1130c-216">Tuletatud globaliseerimise funktsioonide aluse muutmine</span><span class="sxs-lookup"><span data-stu-id="1130c-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="1130c-217">Saate võtta tuletatud globaliseerimise funktsiooni aluseks uue või uuendatud põhifunktsiooni versiooni.</span><span class="sxs-lookup"><span data-stu-id="1130c-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="1130c-218">Sel moel saab põhiversioonis aset leidnud muutusi automaatselt uuendada.</span><span class="sxs-lookup"><span data-stu-id="1130c-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="1130c-219">Uuendatud põhifunktsiooni versiooni loob esialgne konfiguratsioonipakkuja ning seejärel see avaldatakse või antakse ühiskasutusse.</span><span class="sxs-lookup"><span data-stu-id="1130c-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![Uuendatud põhifunktsiooni versioon](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="1130c-221">Näiteks kui soovite muuta teie loodud funktsiooni tuletatud versiooni alust, peate esmalt hankima funktsiooni uusima versiooni, importides selle globaalsest hoidlast.</span><span class="sxs-lookup"><span data-stu-id="1130c-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="1130c-222">Valige lehelt **E-arvete funktsioonid** suvand **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="1130c-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="1130c-223">Uusimate funktsioonide toomiseks valige **Sünkrooni**.</span><span class="sxs-lookup"><span data-stu-id="1130c-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="1130c-224">Valige funktsioonide loetelus imporditavad funktsioonid ja seejärel **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="1130c-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![Funktsiooni uusima versiooni importimine](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="1130c-226">Valige funktsioonide loetelust funktsioon, mille alust soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="1130c-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="1130c-227">Valige vahekaardil **Versioon** suvand **Uus**, et luua mustandversioon.</span><span class="sxs-lookup"><span data-stu-id="1130c-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![Uus mustandversioon loodud](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="1130c-229">Valige **Aluse muutmine**.</span><span class="sxs-lookup"><span data-stu-id="1130c-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="1130c-230">Valige dialoogiaknas **Aluse muutmine** funktsiooni uusim versioon, millele vastavalt alust muudetakse.</span><span class="sxs-lookup"><span data-stu-id="1130c-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![Dialoogiakna aluse muutmine](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="1130c-232">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="1130c-232">Select **OK**.</span></span>
9. <span data-ttu-id="1130c-233">Vaadake üle funktsiooni komponendid ja tehke vajalikud muudatused.</span><span class="sxs-lookup"><span data-stu-id="1130c-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="1130c-234">Valige funktsiooni, mille alus on muudetud, lõpule viimiseks suvand **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="1130c-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="1130c-235">Kui aluse muutmine on lõpule viidud, saate teostada täiendavaid toiminguid.</span><span class="sxs-lookup"><span data-stu-id="1130c-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="1130c-236">Näiteks saate funktsiooni avaldada ja teha selle kasutamise globaliseerimise teenuste raames kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="1130c-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![Funktsiooni olek on muudetud lõpule viiduks](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="1130c-238">Globaliseerimise funktsioonide jaoks keskkondade konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1130c-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="1130c-239">Globaliseerimise teenuste kasutajad saavad hallata keskkonda, et seadistada globaliseerimise funktsioon ja anda volitus kasutajatele, kes sellele ligi pääsevad.</span><span class="sxs-lookup"><span data-stu-id="1130c-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="1130c-240">Valige tööruumis **Globaliseerimise funktsioonid** jaotisest **Keskkonnad** paan **E-arved**.</span><span class="sxs-lookup"><span data-stu-id="1130c-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![Globaliseerimise funktsioonide tööruum](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="1130c-242">Valige **Võtmehoidla parameetrid** ja seejärel valige **Uus**, et luua Azure'i võtmehoidla saladus.</span><span class="sxs-lookup"><span data-stu-id="1130c-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="1130c-243">Sisestage võtmehoidla nimi ja kirjeldus ning seejärel sisestage väljal **Võtmehoidla URI** URL, mis tuvastab Azure'is võtmehoidla ressursi.</span><span class="sxs-lookup"><span data-stu-id="1130c-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="1130c-244">Valige kiirkaardil **Serdid** serdi lisamiseks suvand **Lisa** ja sisestage iga serdi nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="1130c-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![Sert on lisatud](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="1130c-246">Valige uue keskkonna loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1130c-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="1130c-247">Sisestage nimi, kirjeldus ja salvestamiseks nõutud ühiskasutusele juurdepääsu allkirjaloa saladus.</span><span class="sxs-lookup"><span data-stu-id="1130c-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="1130c-248">Valige kiirkaardil **Kasutajad** suvand **Uus**, et lisada kasutaja, kellel on juurdepääsuõigus sellele keskkonnale.</span><span class="sxs-lookup"><span data-stu-id="1130c-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="1130c-249">Sisestage kasutaja ID ja e-posti aadress.</span><span class="sxs-lookup"><span data-stu-id="1130c-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="1130c-250">Kasutajate lisamiseks korrake samme 7 ja 8.</span><span class="sxs-lookup"><span data-stu-id="1130c-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="1130c-251">Keskkonna avaldamiseks valige suvand **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="1130c-251">Select **Publish** to publish the environment.</span></span>

    ![Avaldatud keskkond](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]