---
title: ER-konfiguratsioonide loomine RCS-is ja üleslaadimine globaalsesse hoidlasse
description: Selles teemas selgitatakse, kuidas luua elektroonilise aruandluse (ER) konfiguratsiooni Microsoft Regulatory Configuration Servicesis (RCS) ja globaalsesse hoidlasse üles laadida.
author: JaneA07
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: a138fd4b525077f12f6575f4b10f682728b71203
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838715"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="90d02-103">ER-konfiguratsioonide loomine Regulatory Configuration Servicesis RCS ja üleslaadimine globaalsesse hoidlasse</span><span class="sxs-lookup"><span data-stu-id="90d02-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90d02-104">Saate kasutada Microsoft Regulatory Configuration Servicesi (RCS) elektroonilise aruandluse (ER) konfiguratsioonide loomiseks ja avaldamiseks, et neid saaks kasutada teie organisatsioonis.</span><span class="sxs-lookup"><span data-stu-id="90d02-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="90d02-105">Järgmistes protseduurides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolliga kasutaja saab luua RCS-i eksemplaris loodud ER-konfiguratsiooni tuletatud versiooni ja seejärel laadida tuletatud konfiguratsioon üles globaalsesse hoidlasse.</span><span class="sxs-lookup"><span data-stu-id="90d02-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="90d02-106">Enne nende protseduuride lõpule viimist peate esmalt viima lõpule järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="90d02-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="90d02-107">RCS-i eksemplarile juurde pääsemine.</span><span class="sxs-lookup"><span data-stu-id="90d02-107">Access an RCS instance.</span></span>
- <span data-ttu-id="90d02-108">Looge aktiivne konfiguratsioonipakkuja.</span><span class="sxs-lookup"><span data-stu-id="90d02-108">Create an active configuration provider.</span></span> <span data-ttu-id="90d02-109">Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="90d02-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="90d02-110">Samuti peate veenduma, et teie ettevõttele valmistatakse ette RCS-i keskkond.</span><span class="sxs-lookup"><span data-stu-id="90d02-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="90d02-111">Avage rakenduse Finance and Operations jaotis **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="90d02-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="90d02-112">Kui teie ettevõtte jaoks pole RCS-i keskkonda ette valmistatud, valige **Regulatory services – välise konfigureerimine** ja seejärel järgige juhiseid selle ettevalmistamiseks.</span><span class="sxs-lookup"><span data-stu-id="90d02-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="90d02-113">Kui teie ettevõtte jaoks juba RCS-i keskkond ette valmistatud, kasutage sellele juurde pääsemiseks lehe URL-i, valides sisselogimise suvandi.</span><span class="sxs-lookup"><span data-stu-id="90d02-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="90d02-114">Konfiguratsiooni tuletatud versiooni loomine RCS-is</span><span class="sxs-lookup"><span data-stu-id="90d02-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="90d02-115">Kinnitage tööruumis **Elektrooniline aruandlus**, et teie organisatsioonil on aktiivne konfiguratsiooni pakkuja.</span><span class="sxs-lookup"><span data-stu-id="90d02-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="90d02-116">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="90d02-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="90d02-117">Valige konfiguratsioon, millest soovite tuletada uut versiooni.</span><span class="sxs-lookup"><span data-stu-id="90d02-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="90d02-118">Otsingu kitsendamiseks saate kasutada puu kohal olevat filtri välja.</span><span class="sxs-lookup"><span data-stu-id="90d02-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="90d02-119">Valige **Konfiguratsiooni loomine** \> **Tuleta nimest**.</span><span class="sxs-lookup"><span data-stu-id="90d02-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="90d02-120">Sisestage nimi ja kirjeldus ning seejärel valige **Konfiguratsiooni loomine** uue tuletatud versiooni loomiseks.</span><span class="sxs-lookup"><span data-stu-id="90d02-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="90d02-121">Valige äsja tuletatud konfiguratsioon, lisage versiooni kirjeldus ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="90d02-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="90d02-122">Konfiguratsiooni olekuks muudetakse **Lõpetatud**.</span><span class="sxs-lookup"><span data-stu-id="90d02-122">The status of the configuration to is changed to **Completed**.</span></span>

![Uus konfiguratsiooni versioon RCS-is](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="90d02-124">Kui konfiguratsiooni olekut muudetakse, võidakse kuvada ühendatud rakendustega seotud kinnitamise tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="90d02-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="90d02-125">Kinnitamise väljalülitamiseks valige Toimingupaani vahekaardil **Konfiguratsioonid** suvand **Kasutaja parameetrid** ja seadke seejärel suvandi **Konfiguratsiooni oleku muutmise ja lahendamise vahele jätmine** väärtuseks **Jah**</span><span class="sxs-lookup"><span data-stu-id="90d02-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="90d02-126">Konfiguratsiooni üleslaadimine globaalsesse hoidlasse</span><span class="sxs-lookup"><span data-stu-id="90d02-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="90d02-127">Uue või tuletatud konfiguratsiooni ühiskasutusse andmiseks oma organisatsioonis, saate selle üles laadida globaalsesse hoidlasse.</span><span class="sxs-lookup"><span data-stu-id="90d02-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="90d02-128">Valige konfiguratsiooni lõpule viidud versioon ja seejärel valige **Hoidlasse üleslaadimine**.</span><span class="sxs-lookup"><span data-stu-id="90d02-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="90d02-129">Valige suvand **Globaalne (Microsoft)** ja seejärel valige **Laadi üles**.</span><span class="sxs-lookup"><span data-stu-id="90d02-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Hoidlasse üleslaadimise suvandid](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="90d02-131">Valige kinnituse teateaknast **Jah**.</span><span class="sxs-lookup"><span data-stu-id="90d02-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="90d02-132">Värskendage versiooni kirjeldust vastavalt vajadusele ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="90d02-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="90d02-133">Konfiguratsiooni olekuks värskendatakse **Ühiskasutus** ja konfiguratsioon laaditakse üle globaalsesse hoidlasse.</span><span class="sxs-lookup"><span data-stu-id="90d02-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="90d02-134">Seal saate sellega töötada järgmistel viisidel.</span><span class="sxs-lookup"><span data-stu-id="90d02-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="90d02-135">Importige see oma Dynamics 365 eksemplari.</span><span class="sxs-lookup"><span data-stu-id="90d02-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="90d02-136">Lisateabe saamiseks vt teemat [(ER) konfiguratsioonide importimine RCS-ist](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="90d02-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="90d02-137">Kolmanda osapoolega või välise organisatsiooniga ühiskasutusse andmiseks vt teemat [RCS-i ühiskasutatava elektroonilise aruandluse (ER) konfiguratsioonid väliste organisatsioonidega](rcs-global-repo-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="90d02-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](rcs-global-repo-share-configuration.md)</span></span>

    ![Tuletatud intrastati Contoso konfiguratsiooni versioon globaalses hoidlas](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a><span data-ttu-id="90d02-139">Konfiguratsiooni kustutamine globaalsest hoidlast</span><span class="sxs-lookup"><span data-stu-id="90d02-139">Delete a configuration from the Global repository</span></span>
<span data-ttu-id="90d02-140">Organisatsiooni loodud konfiguratsiooni kustutamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="90d02-140">Complete the following steps to delete a configuration that your organization has created.</span></span>

1. <span data-ttu-id="90d02-141">Veenduge tööruumis **Elektrooniline aruandlus**, et teie konfiguratsioonipakkuja oleks **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="90d02-141">In the **Electronic reporting** workspace, verify that your configuration provider is **Active**.</span></span> <span data-ttu-id="90d02-142">Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="90d02-142">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
2. <span data-ttu-id="90d02-143">Valige oma aktiivse konfiguratsioonipakkuja juures **hoidla**.</span><span class="sxs-lookup"><span data-stu-id="90d02-143">On your active configuration provider, select **repository**.</span></span>
3. <span data-ttu-id="90d02-144">Valige hoidla tüüp **Globaalne** ja valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="90d02-144">Select the repository type **Global**, and select **Open**.</span></span>
4. <span data-ttu-id="90d02-145">Leidke kiirkaardil **Filter** konfiguratsioon, mida soovite kustutada funktsiooni **Filter** abil.</span><span class="sxs-lookup"><span data-stu-id="90d02-145">On the **Filter** FastTab, find the configuration that you want to delete by using the **Filter** functionality.</span></span>
5. <span data-ttu-id="90d02-146">Valige kiirkaardil **Versioon** konfiguratsiooni versioon, mida soovite kustutada, ja seejärel valige **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="90d02-146">On the **Version** FastTab, select the version of the configuration that you want to delete, and then select **Delete**:</span></span>

    ![Konfiguratsiooni kustutamine globaalsest hoidlast](media/RCS_Delete_from_GlobalRepo.JPG)

6. <span data-ttu-id="90d02-148">Valige kinnituse teateaknast **Jah**.</span><span class="sxs-lookup"><span data-stu-id="90d02-148">In the confirmation message box, select **Yes**.</span></span>

    ![Konfiguratsiooni versiooni kinnitusteate kustutamine](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
<span data-ttu-id="90d02-150">Konfiguratsiooni versioon kustutatakse ja kuvatakse kinnitusteade.</span><span class="sxs-lookup"><span data-stu-id="90d02-150">The configuration version is deleted, and confirmation message is shown.</span></span> 

> [!NOTE]
> <span data-ttu-id="90d02-151">Konfiguratsiooni saab kustutada ainult konfiguratsiooni loonud konfiguratsioonipakkuja.</span><span class="sxs-lookup"><span data-stu-id="90d02-151">Configurations can only be deleted by the Configuration provider that created them.</span></span> <span data-ttu-id="90d02-152">Kui konfiguratsiooni on jagatud mõne muu organisatsiooniga, tuleb jagamine enne konfiguratsiooni kustutamist tühistada.</span><span class="sxs-lookup"><span data-stu-id="90d02-152">If the configuration has been shared with another organization, the configuration will need to be unshared before you delete it.</span></span>
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]