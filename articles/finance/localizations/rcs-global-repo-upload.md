---
title: ER-konfiguratsioonide loomine RCS-is ja üleslaadimine globaalsesse hoidlasse
description: Selles teemas selgitatakse, kuidas luua elektroonilise aruandluse (ER) konfiguratsiooni Microsoft Regulatory Configuration Servicesis (RCS) ja globaalsesse hoidlasse üles laadida.
author: JaneA07
manager: AnnBe
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 0e194a8b777f984412d81e315f92ab4bb8a3b0c9
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371241"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="7b8ea-103">ER-konfiguratsioonide loomine Regulatory Configuration Servicesis RCS ja üleslaadimine globaalsesse hoidlasse</span><span class="sxs-lookup"><span data-stu-id="7b8ea-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b8ea-104">Saate kasutada Microsoft Regulatory Configuration Servicesi (RCS) elektroonilise aruandluse (ER) konfiguratsioonide loomiseks ja avaldamiseks, et neid saaks kasutada teie organisatsioonis.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="7b8ea-105">Järgmistes protseduurides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolliga kasutaja saab luua RCS-i eksemplaris loodud ER-konfiguratsiooni tuletatud versiooni ja seejärel laadida tuletatud konfiguratsioon üles globaalsesse hoidlasse.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="7b8ea-106">Enne nende protseduuride lõpule viimist peate esmalt viima lõpule järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="7b8ea-107">RCS-i eksemplarile juurde pääsemine.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-107">Access an RCS instance.</span></span>
- <span data-ttu-id="7b8ea-108">Looge aktiivne konfiguratsioonipakkuja.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-108">Create an active configuration provider.</span></span> <span data-ttu-id="7b8ea-109">Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="7b8ea-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="7b8ea-110">Samuti peate veenduma, et teie ettevõttele valmistatakse ette RCS-i keskkond.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="7b8ea-111">Avage rakenduse Finance and Operations jaotis **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7b8ea-112">Kui teie ettevõtte jaoks pole RCS-i keskkonda ette valmistatud, valige **Regulatory services – välise konfigureerimine** ja seejärel järgige juhiseid selle ettevalmistamiseks.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="7b8ea-113">Kui teie ettevõtte jaoks juba RCS-i keskkond ette valmistatud, kasutage sellele juurde pääsemiseks lehe URL-i, valides sisselogimise suvandi.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="7b8ea-114">Konfiguratsiooni tuletatud versiooni loomine RCS-is</span><span class="sxs-lookup"><span data-stu-id="7b8ea-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="7b8ea-115">Kinnitage tööruumis **Elektrooniline aruandlus**, et teie organisatsioonil on aktiivne konfiguratsiooni pakkuja.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="7b8ea-116">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="7b8ea-117">Valige konfiguratsioon, millest soovite tuletada uut versiooni.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="7b8ea-118">Otsingu kitsendamiseks saate kasutada puu kohal olevat filtri välja.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="7b8ea-119">Valige **Konfiguratsiooni loomine** \> **Tuleta nimest**.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="7b8ea-120">Sisestage nimi ja kirjeldus ning seejärel valige **Konfiguratsiooni loomine** uue tuletatud versiooni loomiseks.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="7b8ea-121">Valige äsja tuletatud konfiguratsioon, lisage versiooni kirjeldus ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="7b8ea-122">Konfiguratsiooni olekuks muudetakse **Lõpetatud**.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-122">The status of the configuration to is changed to **Completed**.</span></span>

![Uus konfiguratsiooni versioon RCS-is](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="7b8ea-124">Kui konfiguratsiooni olekut muudetakse, võidakse kuvada ühendatud rakendustega seotud kinnitamise tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="7b8ea-125">Kinnitamise väljalülitamiseks valige Toimingupaani vahekaardil **Konfiguratsioonid** suvand **Kasutaja parameetrid** ja seadke seejärel suvandi **Konfiguratsiooni oleku muutmise ja lahendamise vahele jätmine** väärtuseks **Jah**</span><span class="sxs-lookup"><span data-stu-id="7b8ea-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="7b8ea-126">Konfiguratsiooni üleslaadimine globaalsesse hoidlasse</span><span class="sxs-lookup"><span data-stu-id="7b8ea-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="7b8ea-127">Uue või tuletatud konfiguratsiooni ühiskasutusse andmiseks oma organisatsioonis, saate selle üles laadida globaalsesse hoidlasse.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="7b8ea-128">Valige konfiguratsiooni lõpule viidud versioon ja seejärel valige **Hoidlasse üleslaadimine**.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="7b8ea-129">Valige suvand **Globaalne (Microsoft)** ja seejärel valige **Laadi üles**.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Hoidlasse üleslaadimise suvandid](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="7b8ea-131">Valige kinnituse teateaknast **Jah**.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="7b8ea-132">Värskendage versiooni kirjeldust vastavalt vajadusele ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="7b8ea-133">Konfiguratsiooni olekuks värskendatakse **Ühiskasutus** ja konfiguratsioon laaditakse üle globaalsesse hoidlasse.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="7b8ea-134">Seal saate sellega töötada järgmistel viisidel.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="7b8ea-135">Importige see oma Dynamics 365 eksemplari.</span><span class="sxs-lookup"><span data-stu-id="7b8ea-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="7b8ea-136">Lisateabe saamiseks vt teemat [(ER) konfiguratsioonide importimine RCS-ist](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="7b8ea-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="7b8ea-137">Kolmanda osapoolega või välise organisatsiooniga ühiskasutusse andmiseks vt teemat [RCS-i ühiskasutatava elektroonilise aruandluse (ER) konfiguratsioonid väliste organisatsioonidega](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="7b8ea-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span></span>

![Tuletatud intrastati Contoso konfiguratsiooni versioon globaalses hoidlas](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Config_upload_GlobalRepo.JPG)
