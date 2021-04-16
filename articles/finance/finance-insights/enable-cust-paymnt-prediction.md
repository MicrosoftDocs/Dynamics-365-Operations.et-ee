---
title: Kliendimaksete prognoosimise lubamine (eelversioon)
description: Selles teemas selgitatakse, kuidas lülitada sisse ja konfigureerida finantsülevaadetes kliendimakse prognooside funktsioon.
author: ShivamPandey-msft
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ecc3851cc91c8fe17a7582f2be06e84cf9bc2d83
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818652"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="1e590-103">Kliendimaksete prognoosimise lubamine (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="1e590-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="1e590-104">Selles teemas selgitatakse, kuidas lülitada sisse ja konfigureerida finantsülevaadetes kliendimakse prognooside funktsioon.</span><span class="sxs-lookup"><span data-stu-id="1e590-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="1e590-105">Te lülitate funktsiooni tööruumis **Funktsioonihaldus** sisse ja sisestate konfiguratsiooni sätted lehel **Finantsülevaadete parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1e590-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="1e590-106">See teema sisaldab ka teavet, mis võib aidata teil funktsiooni tõhusalt kasutada.</span><span class="sxs-lookup"><span data-stu-id="1e590-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="1e590-107">Enne järgmiste etappide täitmist täitke kindlasti eeltingimuse etapid jaotises [Finantsülevaadete konfigureerimine](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="1e590-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="1e590-108">Kasutage teavet teenuse Microsoft Dynamics Lifecycle Services (LCS) lehelt, et ühendada Azure SQL-i esmane eksemplar selle keskkonnaga.</span><span class="sxs-lookup"><span data-stu-id="1e590-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="1e590-109">Käivitage järgmine Transact-SQL (T-SQL) käsk, et lülitada liivakasti keskkonna eelväljaanded sisse.</span><span class="sxs-lookup"><span data-stu-id="1e590-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="1e590-110">(Enne rakendusobjekti serveriga \[AOS\] eemalt ühenduse loomist võib olla vajalik, et peate LCS-is lülitama oma IP-aadressi juurdepääsu sisse.)</span><span class="sxs-lookup"><span data-stu-id="1e590-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > <span data-ttu-id="1e590-111">Kui teie Microsoft Dynamics 365 Finance on Service Fabricu juurutus, saate selle sammu vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="1e590-111">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="1e590-112">Finantsülevaadete meeskond peaks olema väljaande juba teie jaoks sisse lülitanud.</span><span class="sxs-lookup"><span data-stu-id="1e590-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="1e590-113">Kui te funktsiooni tööruumis **Funktsioonihaldus** ei näe või kui selle sisselülitamisel esineb probleeme, võtke ühendust aadressil <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="1e590-113">If you don't see the feature in the **Feature management** workspace, or if experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="1e590-114">Kliendimaksete ülevaadete funktsiooni sisselülitamine.</span><span class="sxs-lookup"><span data-stu-id="1e590-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="1e590-115">Avage **Süsteemihaldus \> Tööruumid \> Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="1e590-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="1e590-116">Leidke funktsioon, mille nimi on **Kliendimakse ülevaated (eelversioon)**.</span><span class="sxs-lookup"><span data-stu-id="1e590-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="1e590-117">Valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="1e590-117">Select **Enable now**.</span></span>

    <span data-ttu-id="1e590-118">Kliendimakse ülevaadete funktsioon on nüüd sisse lülitatud ja konfigureerimiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="1e590-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="1e590-119">Kliendimaksete ülevaadete funktsiooni konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="1e590-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="1e590-120">Avage suvand **Krediidihaldus ja võlanõuded \> Seadistamine \> Finantsülevaated \> Finantsülevaadete parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1e590-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="1e590-121">[![Finantsteabe parameetrite leht enne funktsiooni konfigureerimist](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="1e590-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="1e590-122">Valige lehel **Finantsülevaadete parameetrid** vahekaardil **Kliendimaksete ülevaated** link **Prognoosimudelis kasutatavate andmeväljade kuvamine**, et avada leht **Prognoosimudeli andmeväljad**.</span><span class="sxs-lookup"><span data-stu-id="1e590-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="1e590-123">Siin saate vaadata väljade vaikeloendit, mida kasutatakse kliendimaksete prognooside jaoks tehisintellekti (AI) prognoosimismudeli loomiseks.</span><span class="sxs-lookup"><span data-stu-id="1e590-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="1e590-124">Prognoosimudeli loomiseks väljade vaikeloendi kasutamiseks sulgege leht **Prognoosimudeli andmeväljad** ja määrake seejärel lehel **Finantsülevaadete parameetrid** suvand **Funktsiooni lubamine** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1e590-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="1e590-125">Määrake väga hilise kande periood, et määratleda, mida tähendab teie ettevõtte jaoks prognoosisalv **Väga hilja**.</span><span class="sxs-lookup"><span data-stu-id="1e590-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="1e590-126">Iga avatud arve puhul ennustab süsteem makse tõenäosuse kolme salve seast: **õigel ajal**, **hilja** ja **väga hilja**.</span><span class="sxs-lookup"><span data-stu-id="1e590-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="1e590-127">**Õigel ajal** – see salv hõlmab makseid, mida prognoositakse, et makstakse kande tähtajal või enne seda.</span><span class="sxs-lookup"><span data-stu-id="1e590-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="1e590-128">**Hilja** – see salv hõlmab makseid, mille maksmine prognoositakse pärast kande tähtaega, kuid enne kande perioodi „väga hilja” algamist.</span><span class="sxs-lookup"><span data-stu-id="1e590-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="1e590-129">**Väga hilja** – see salv hõlmab makseid, mille maksmine prognoositakse pärast kande perioodi „väga hilja” algamist.</span><span class="sxs-lookup"><span data-stu-id="1e590-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="1e590-130">Kui muudate kande perioodi „väga hilja” ja valite suvandi **Hilise lävendi muutmine** pärast seda, kui tehisintellekti prognoosimise mudel on kliendimaksete jaoks on loodud, olemasolev prognoosimise mudel kustutatakse ja luuakse uus mudel.</span><span class="sxs-lookup"><span data-stu-id="1e590-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="1e590-131">Uus prognoosimise mudel teisaldab kanded perioodile „väga hilja”, mis põhineb selle määratlemiseks sisestatud sätetel.</span><span class="sxs-lookup"><span data-stu-id="1e590-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="1e590-132">Kui olete tehingu perioodi „väga hilja” määratlenud, valige prognoosimise mudeli loomiseks suvand **Prognoosimise mudeli loomine**.</span><span class="sxs-lookup"><span data-stu-id="1e590-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="1e590-133">Jaotis **Prognoosimise mudel** lehel **Finantsülevaadete parameetrid** näitab prognoosimise mudeli olekut.</span><span class="sxs-lookup"><span data-stu-id="1e590-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="1e590-134">Prognoosimise mudeli loomise ajal saate igal ajal protsessi taaskäivitamiseks valida suvandi **Lähtesta mudeli loomine**.</span><span class="sxs-lookup"><span data-stu-id="1e590-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="1e590-135">Funktsioon on nüüd konfigureeritud ja kasutamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="1e590-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="1e590-136">Pärast seda, kui funktsioon on sisse lülitatud ja konfigureeritud ning prognoosimise mudel on loodud ja töötab, kuvab jaotise **Prognoosimise mudel** leht **Finantsülevaadete parameetrid** mudeli täpsuse, nagu järgmisel illustratsioonil on näidatud.</span><span class="sxs-lookup"><span data-stu-id="1e590-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="1e590-137">[![Prognoosimise mudeli täpsus finantsülevaadete parameetrite lehel](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="1e590-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="1e590-138">Väljastuse üksikasjad</span><span class="sxs-lookup"><span data-stu-id="1e590-138">Release details</span></span>

<span data-ttu-id="1e590-139">Finantsülevaadete avalik eelversioon on prooviversioonina juurutamiseks saadaval Ameerika Ühendriikides, Euroopas ja Ühendkuningriigis.</span><span class="sxs-lookup"><span data-stu-id="1e590-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="1e590-140">Microsoft lisab astmeliselt juurde täiendavate piirkondade tuge.</span><span class="sxs-lookup"><span data-stu-id="1e590-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="1e590-141">Avaliku eelvaate funktsioone saab ja tuleb sisse lülitada ainult Järgu 2 liivakasti keskkondades.</span><span class="sxs-lookup"><span data-stu-id="1e590-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="1e590-142">Liivakasti keskkonnas loodud seadistust ja AI mudeleid ei saa migreerida töökeskkonda.</span><span class="sxs-lookup"><span data-stu-id="1e590-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="1e590-143">Lisateavet leiate teemast [Microsoft Dynamics 365 eelversioonide täiendavad kasutustingimused](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span><span class="sxs-lookup"><span data-stu-id="1e590-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="1e590-144">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="1e590-144">Privacy notice</span></span>

<span data-ttu-id="1e590-145">Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.</span><span class="sxs-lookup"><span data-stu-id="1e590-145">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]