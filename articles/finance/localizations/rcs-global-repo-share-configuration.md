---
title: ER-konfiguratsioonide jagamine RCS-is / globaalses hoidlas väliste organisatsioonidega
description: Selles teemas selgitatakse, kuidas anda elektroonilise aruandluse (ER) konfiguratsioone ühiskasutusse Microsoft Regulatory Configuration Servicesis (RCS) / globaalses hoidlas väliste organisatsioonidega otse.
author: JaneA07
ms.date: 05/04/2020
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
ms.openlocfilehash: ace62319bbfa38bcf4be7157882dd0c8989e25bc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838741"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="4a875-103">Elektroonilise aruandluse (ER) konfiguratsioonide ühiskasutusse andmine Regulatory Configuration Servicesi (RCS) globaalses hoidlas väliste organisatsioonidega</span><span class="sxs-lookup"><span data-stu-id="4a875-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a875-104">Saate kasutada Microsoft Regulatory Configuration Servicesi (RCS) elektroonilise aruandluse (ER) konfiguratsioonide ühiskasutusse andmiseks ja välistesse organisatsioonidesse avaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="4a875-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="4a875-105">Järgmistes protseduurides selgitatakse, kuidas RCS-i kasutaja saab anda ühiskasutusse ER-konfiguratsiooni versiooni, mis on konfigureeritud RCS-i eksemplaris välise organisatsiooniga.</span><span class="sxs-lookup"><span data-stu-id="4a875-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="4a875-106">Enne nende protseduuride lõpule viimist peate esmalt viima lõpule järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="4a875-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="4a875-107">RCS-i eksemplarile juurde pääsemine.</span><span class="sxs-lookup"><span data-stu-id="4a875-107">Access an RCS instance.</span></span>
- <span data-ttu-id="4a875-108">Looge aktiivne konfiguratsioonipakkuja.</span><span class="sxs-lookup"><span data-stu-id="4a875-108">Create an active configuration provider.</span></span> <span data-ttu-id="4a875-109">Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="4a875-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="4a875-110">Looge ja laadige üles ER-konfiguratsiooni uus versioon.</span><span class="sxs-lookup"><span data-stu-id="4a875-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="4a875-111">Lisateabe saamiseks vaadake teemat [Elektroonilise aruandluse (ER) konfiguratsiooni uue versiooni loomine ja üleslaadimine](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="4a875-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="4a875-112">Samuti peate veenduma, et teie ettevõttele valmistatakse ette RCS-i keskkond.</span><span class="sxs-lookup"><span data-stu-id="4a875-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="4a875-113">Avage rakenduse Finance and Operations jaotis **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="4a875-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="4a875-114">Kui teie ettevõtte jaoks pole RCS-i keskkonda ette valmistatud, valige **Regulatory services – välise konfigureerimine** ja seejärel järgige juhiseid selle ettevalmistamiseks.</span><span class="sxs-lookup"><span data-stu-id="4a875-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="4a875-115">Kui teie ettevõtte jaoks juba RCS-i keskkond ette valmistatud, kasutage sellele juurde pääsemiseks lehe URL-i, valides sisselogimise suvandi.</span><span class="sxs-lookup"><span data-stu-id="4a875-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="4a875-116">Kinnitage konfiguratsioon, mida soovite ühiskasutusse anda</span><span class="sxs-lookup"><span data-stu-id="4a875-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="4a875-117">Järgige neid etappe, et kinnitada, kas konfiguratsioon, mida soovite ühiskasutusse anda, on juba üles laaditud globaalsesse hoidlasse.</span><span class="sxs-lookup"><span data-stu-id="4a875-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="4a875-118">Valige tööruumis **Elektrooniline aruandlus** suvand **Hoidlad** oma konfiguratsioonipakkuja jaoks.</span><span class="sxs-lookup"><span data-stu-id="4a875-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![Konfiguratsiooni pakkujad](media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="4a875-120">Valige **Globaalne hoidla** \> **Ava**.</span><span class="sxs-lookup"><span data-stu-id="4a875-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="4a875-121">Otsige konfiguratsiooni, mida soovite ühiskasutusse anda.</span><span class="sxs-lookup"><span data-stu-id="4a875-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="4a875-122">Otsingu kitsendamiseks saate kasutada filtri välja.</span><span class="sxs-lookup"><span data-stu-id="4a875-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="4a875-123">Kui konfiguratsiooni ei kuvata globaalses hoidlas, järgige juhiseid teemas [Elektroonilise aruandluse (ER) konfiguratsiooni uue versiooni loomine ja üleslaadimine](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="4a875-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="4a875-124">ER-konfiguratsioonide ühiskasutusse andmine väliste organisatsioonidega</span><span class="sxs-lookup"><span data-stu-id="4a875-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="4a875-125">Pärast konfiguratsiooni loomist teie konfiguratsioonipakkujas, saate anda seda otse väliste organisatsioonidega ühiskasutusse lehe **Globaalne konfiguratsiooni hoidla** kiirkaardi **Ühiskasutuses kasutajaga** abil.</span><span class="sxs-lookup"><span data-stu-id="4a875-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="4a875-126">Valige tööruumis **Elektrooniline aruandlus** suvand **Hoidlad** oma konfiguratsioonipakkuja jaoks.</span><span class="sxs-lookup"><span data-stu-id="4a875-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="4a875-127">Valige **Globaalne hoidla** \> **Ava**.</span><span class="sxs-lookup"><span data-stu-id="4a875-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="4a875-128">Valige konfiguratsioon, mida soovite ühiskasutusse anda.</span><span class="sxs-lookup"><span data-stu-id="4a875-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="4a875-129">Valige kiirkaardil **Ühiskasutuses kasutajaga** suvand **Organisatsioon**.</span><span class="sxs-lookup"><span data-stu-id="4a875-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![Kiirkaart Ühiskasutuses kasutajaga](media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="4a875-131">Sisestage dialoogiboksis välise organisatsiooni domeeninimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a875-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![Konfiguratsiooni versiooni ühiskasutusse andmine välise organisatsiooni dialoogiboksiga](media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="4a875-133">Konfiguratsioon on antud ühiskasutusse välise organisatsiooniga ja saadaval globaalses hoidlas selle organisatsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="4a875-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="4a875-134">Sealt saab importida selle organisatsiooni RCS-i eksemplari või rakenduste Finance and Operations eksemplaridesse.</span><span class="sxs-lookup"><span data-stu-id="4a875-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

6. <span data-ttu-id="4a875-135">Välise organisatsiooniga varasemalt ühiskasutusse antud konfiguratsiooni ühiskasutusest eemaldamiseks, valige see konfiguratsioon ja klõpsake suvandit **Eemalda ühiskasutusest** ning seejärel valige **OK**</span><span class="sxs-lookup"><span data-stu-id="4a875-135">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]