---
title: Korduvate andmete ekspordi rakenduse loomine
description: See artikkel näitab, kuidas luua Microsoft Azure’i loogikarakendus, mis ekspordib rakendusest Microsoft Dynamics 365 Human Resources korduva graafiku alusel andmeid.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: edd4b999624a845fc145ed9ff348ae9cba782719
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008708"
---
# <a name="create-a-recurring-data-export-app"></a><span data-ttu-id="c9de4-103">Korduvate andmete ekspordi rakenduse loomine</span><span class="sxs-lookup"><span data-stu-id="c9de4-103">Create a recurring data export app</span></span>

<span data-ttu-id="c9de4-104">See artikkel näitab, kuidas luua Microsoft Azure’i loogikarakendus, mis ekspordib rakendusest Microsoft Dynamics 365 Human Resources korduva graafiku alusel andmeid.</span><span class="sxs-lookup"><span data-stu-id="c9de4-104">This article shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 Human Resources on a recurring schedule.</span></span> <span data-ttu-id="c9de4-105">Õpetus kasutab andmete eksportimiseks rakenduse Human Resources DMF-i paketi REST rakenduse programmeerimisliidest (API).</span><span class="sxs-lookup"><span data-stu-id="c9de4-105">The tutorial takes advantage of Human Resources' DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="c9de4-106">Pärast andmete eksportimist salvestab loogikarakendus eksporditud andmed Microsoft OneDrive for Businessi kausta.</span><span class="sxs-lookup"><span data-stu-id="c9de4-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="c9de4-107">Äristsenaarium</span><span class="sxs-lookup"><span data-stu-id="c9de4-107">Business scenario</span></span>

<span data-ttu-id="c9de4-108">Ühes tüüpilises Microsoft Dynamics 365 integreerimise äristsenaariumis tuleb andmeid eksportida allsüsteemi korduva graafiku alusel.</span><span class="sxs-lookup"><span data-stu-id="c9de4-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="c9de4-109">See õpetus näitab, kuidas eksportida kõik töötajate kirjed rakendusest Microsoft Dynamics 365 Human Resources ja salvestada töötajate loend OneDrive for Businessi kausta.</span><span class="sxs-lookup"><span data-stu-id="c9de4-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 Human Resources and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="c9de4-110">Selles õpetus eksporditavad konkreetsed andmed ja eksporditud andmete sihtkoht on ainult näited.</span><span class="sxs-lookup"><span data-stu-id="c9de4-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="c9de4-111">Saate neid oma ettevõtte vajadustele vastavalt hõlpalt muuta.</span><span class="sxs-lookup"><span data-stu-id="c9de4-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="c9de4-112">Kasutatud tehnoloogiad</span><span class="sxs-lookup"><span data-stu-id="c9de4-112">Technologies used</span></span>

<span data-ttu-id="c9de4-113">See õpetus kasutab järgmisi tehnoloogiaid.</span><span class="sxs-lookup"><span data-stu-id="c9de4-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="c9de4-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)**– eksporditavatele töötajatele mõeldud koondandmete allikas.</span><span class="sxs-lookup"><span data-stu-id="c9de4-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="c9de4-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – tehnoloogia, mis võimaldab korduva eksportimise korraldamist ja planeerimist.</span><span class="sxs-lookup"><span data-stu-id="c9de4-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="c9de4-116">**[Konnektorid](https://docs.microsoft.com/azure/connectors/apis-list)** – tehnoloogia, mida kasutatakse loogikarakenduse ühendamiseks vajalike lõpp-punktidega.</span><span class="sxs-lookup"><span data-stu-id="c9de4-116">**[Connectors](https://docs.microsoft.com/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="c9de4-117">Konnektor [HTTP koos Azure AD-ga](https://docs.microsoft.com/connectors/webcontents/)</span><span class="sxs-lookup"><span data-stu-id="c9de4-117">[HTTP with Azure AD](https://docs.microsoft.com/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="c9de4-118">Konnektor [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)</span><span class="sxs-lookup"><span data-stu-id="c9de4-118">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="c9de4-119">**[DMF-i pakett REST API](../dev-itpro/data-entities/data-management-api.md)** – tehnoloogia, mida kasutatakse eksportimise käivitamiseks ja selle edenemise jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="c9de4-119">**[DMF package REST API](../dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="c9de4-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – eksporditud töötajate sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="c9de4-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c9de4-121">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="c9de4-121">Prerequisites</span></span>

<span data-ttu-id="c9de4-122">Enne selle õpetuse harjutusega alustamist peavad teil olema järgmised üksused.</span><span class="sxs-lookup"><span data-stu-id="c9de4-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="c9de4-123">Inimressursside keskkond, millel on keskkonnas administraatori taseme load</span><span class="sxs-lookup"><span data-stu-id="c9de4-123">A Human Resources environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="c9de4-124">[Azure’i tellimus](https://azure.microsoft.com/free/) loogikarakenduse majutamiseks</span><span class="sxs-lookup"><span data-stu-id="c9de4-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="c9de4-125">Harjutus</span><span class="sxs-lookup"><span data-stu-id="c9de4-125">The exercise</span></span>

<span data-ttu-id="c9de4-126">Selle harjutuse lõpus on teil loogikarakendus, mis on ühendatud teie inimressursside keskkonna ja OneDrive for Businessi kontoga.</span><span class="sxs-lookup"><span data-stu-id="c9de4-126">At the end of this exercise, you will have a logic app that is connected to your Human Resources environment and your OneDrive for Business account.</span></span> <span data-ttu-id="c9de4-127">Loogikarakendus ekspordib rakendusest Human Resources andmepaketi, ootab eksportimise lõpule jõudmist, laadib eksporditud andmepaketi alla ja salvestab andmepaketi määratud OneDrive for Businessi kausta.</span><span class="sxs-lookup"><span data-stu-id="c9de4-127">The logic app will export a data package from Human Resources, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="c9de4-128">Lõpetatud loogikarakendus sarnaneb järgmisele joonisele.</span><span class="sxs-lookup"><span data-stu-id="c9de4-128">The completed logic app will resemble the following illustration.</span></span>

![Loogikarakenduse ülevaade](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a><span data-ttu-id="c9de4-130">1. etapp: andmete eksportimise projekti loomine rakenduses Human Resources</span><span class="sxs-lookup"><span data-stu-id="c9de4-130">Step 1: Create a data export project in Human Resources</span></span>

<span data-ttu-id="c9de4-131">Looge rakenduses Human Resources andmete eksportimise projekt, mis ekspordib töötajaid.</span><span class="sxs-lookup"><span data-stu-id="c9de4-131">In Human Resources, create a data export project that exports workers.</span></span> <span data-ttu-id="c9de4-132">Pange sellele nimi **Töötajate eksportimine** ja veenduge, et suvand **Andmepaketi loomine** oleks seatud valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="c9de4-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="c9de4-133">Lisage projektile üks üksus (**Töötaja**) ja valige eksportimiseks vorming.</span><span class="sxs-lookup"><span data-stu-id="c9de4-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="c9de4-134">(Selles õpetuses on kasutatud Microsoft Exceli vormingut.)</span><span class="sxs-lookup"><span data-stu-id="c9de4-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![Töötajate eksportimise andmeprojekt](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="c9de4-136">Jätke andmete eksportimise projekti nimi meelde.</span><span class="sxs-lookup"><span data-stu-id="c9de4-136">Remember the name of the data export project.</span></span> <span data-ttu-id="c9de4-137">Seda on vaja, kui loote järgmises etapis loogikarakenduse.</span><span class="sxs-lookup"><span data-stu-id="c9de4-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="c9de4-138">2. etapp: loogikarakenduse loomine</span><span class="sxs-lookup"><span data-stu-id="c9de4-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="c9de4-139">Suur osa harjutusest hõlmab loogikarakenduse loomist.</span><span class="sxs-lookup"><span data-stu-id="c9de4-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="c9de4-140">Looge Azure’i portaalis loogikarakendus.</span><span class="sxs-lookup"><span data-stu-id="c9de4-140">In the Azure portal, create a logic app.</span></span>

    ![Loogikarakenduse loomise leht](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="c9de4-142">Alustage Logic Apps Designeris tühja loogikarakendusega.</span><span class="sxs-lookup"><span data-stu-id="c9de4-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="c9de4-143">Lisage [kordumise graafiku päästik](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence), et käivitada loogikarakendus iga 24 tunni järel (või vastavalt teie valitud graafikule).</span><span class="sxs-lookup"><span data-stu-id="c9de4-143">Add a [Recurrence Schedule trigger](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![Kordumise dialoogiaken](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="c9de4-145">Kutsuge DMF-i REST API [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage), et ajastada teie andmepaketi eksportimine.</span><span class="sxs-lookup"><span data-stu-id="c9de4-145">Call the [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="c9de4-146">Kasutage tegevust **HTTP-päringu kutsumine** konnektorist HTTP koos Azure AD-ga.</span><span class="sxs-lookup"><span data-stu-id="c9de4-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="c9de4-147">**Põhiressursi URL:** teie inimressursside keskkonna URL (ärge lisage tee/nimeruumi teavet.)</span><span class="sxs-lookup"><span data-stu-id="c9de4-147">**Base Resource URL:** The URL of your Human Resources environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="c9de4-148">**Azure AD ressursi URI:** `http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="c9de4-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="c9de4-149">Teenus Human Resources ei paku veel konnektorit, mis näitab kõiki API-sid, millest DMF-i paketi REST API koosneb, näiteks **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="c9de4-149">The Human Resources service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="c9de4-150">Selle asemel peate kutsuma API-d, kasutades HTTPS-i toortaotlusi läbi konnektori HTTP koos Azure AD-ga.</span><span class="sxs-lookup"><span data-stu-id="c9de4-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="c9de4-151">See konnektor kasutab autentimiseks ja autoriseerimiseks rakendusele Human Resources Azure Active Directoryt (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="c9de4-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Human Resources.</span></span>

        ![Konnektor HTTP koos Azure AD-ga](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="c9de4-153">Logige oma inimressursside keskkonda läbi konnektori HTTP koos Azure AD-ga sisse.</span><span class="sxs-lookup"><span data-stu-id="c9de4-153">Sign in to your Human Resources environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="c9de4-154">Seadistage HTTP **POST-i** taotlus kutsuma DMF-i REST API **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="c9de4-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="c9de4-155">**Meetod:** POST</span><span class="sxs-lookup"><span data-stu-id="c9de4-155">**Method:** POST</span></span>
        - <span data-ttu-id="c9de4-156">**Taotluse URL:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="c9de4-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="c9de4-157">**Taotluse keha:**</span><span class="sxs-lookup"><span data-stu-id="c9de4-157">**Body of the request:**</span></span>

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Tegevuse HTTP-päring käivitamine](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > <span data-ttu-id="c9de4-159">Võite soovida iga sammu ümber nimetada, et see oleks tähendusrikkam kui vaikenimi **HTTP-päringu käivitamine**.</span><span class="sxs-lookup"><span data-stu-id="c9de4-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="c9de4-160">Näiteks võite panna sellele etapile nimeks **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="c9de4-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="c9de4-161">[Lähtestage muutuja](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) salvestama taotluse **ExportToPackage** käivitamisoleku.</span><span class="sxs-lookup"><span data-stu-id="c9de4-161">[Initialize a variable](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![Muutuja tegevuse lähtestamine](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="c9de4-163">Oodake, kuni andmete ekspordi käivitamisolek on **Õnnestunud**.</span><span class="sxs-lookup"><span data-stu-id="c9de4-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="c9de4-164">Lisage [silmus Kuni](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop), mis kordub, kuni muutuja **ExecutionStatus** väärtus on **Õnnestunud**.</span><span class="sxs-lookup"><span data-stu-id="c9de4-164">Add an [Until loop](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="c9de4-165">Lisage tegevus **Viivitus**, mis ootab viis sekundit enne kui pollib eksportimise praegust käivitamisolekut.</span><span class="sxs-lookup"><span data-stu-id="c9de4-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![Silmuse Kuni konteiner](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="c9de4-167">Määrake limiidi arvuks **15**, et oodata ekspordi lõpetamiseks maksimaalselt 75 sekundit (15 iteratsiooni × 5 sekundit).</span><span class="sxs-lookup"><span data-stu-id="c9de4-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="c9de4-168">Kui teie eksportimisele kulub rohkem aega, reguleerige limiidi arvu vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="c9de4-168">If your export takes more time, adjust the limit count as appropriate.</span></span>        

    3. <span data-ttu-id="c9de4-169">Lisage tegevus **Käivita HTTP-päring**, er kutsuda DMF-i REST API [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) ja määrata muutuja **ExecutionStatus** vastuse **GetExecutionSummaryStatus** tulemusele.</span><span class="sxs-lookup"><span data-stu-id="c9de4-169">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="c9de4-170">See näide ei tee veakontrolli.</span><span class="sxs-lookup"><span data-stu-id="c9de4-170">This sample doesn't do error checking.</span></span> <span data-ttu-id="c9de4-171">API **GetExecutionSummaryStatus** võib tagastada ebaõnnestunud lõplikke olekuid (s.t muud olekud kui **Õnnestunud**).</span><span class="sxs-lookup"><span data-stu-id="c9de4-171">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="c9de4-172">Lisateabe saamiseks vt [API-i dokumentatsiooni](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span><span class="sxs-lookup"><span data-stu-id="c9de4-172">For more information, see the [API documentation](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

        - <span data-ttu-id="c9de4-173">**Meetod:** POST</span><span class="sxs-lookup"><span data-stu-id="c9de4-173">**Method:** POST</span></span>
        - <span data-ttu-id="c9de4-174">**Taotluse URL:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="c9de4-174">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="c9de4-175">**Taotluse keha:** body('Invoke\_an\_HTTP\_request')?['value']</span><span class="sxs-lookup"><span data-stu-id="c9de4-175">**Body of the request:** body('Invoke\_an\_HTTP\_request')?['value']</span></span>

            > [!NOTE]
            > <span data-ttu-id="c9de4-176">Võimalik, et peate sisestama väärtuse **Taotluse keha** kas koodi vaates või kujundaja funktsioonide redaktoris.</span><span class="sxs-lookup"><span data-stu-id="c9de4-176">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![Tegevuse HTTP-päring 2 käivitamine](media/integration-logic-app-get-execution-status-step.png)

        ![Muutuva tegevuse määramine](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="c9de4-179">Tegevuse **Muutuja määramine** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) väärtus erineb keha **HTTP-päringu 2 käivitamine** väärtusest, isegi kui kujundaja näitab väärtuseid samamoodi.</span><span class="sxs-lookup"><span data-stu-id="c9de4-179">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="c9de4-180">Hankige eksporditud paketi allalaadimise URL.</span><span class="sxs-lookup"><span data-stu-id="c9de4-180">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="c9de4-181">Lisake tegevus **HTTP-päringu käivitamine** DMF-i REST API [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) kutsumiseks.</span><span class="sxs-lookup"><span data-stu-id="c9de4-181">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="c9de4-182">**Meetod:** POST</span><span class="sxs-lookup"><span data-stu-id="c9de4-182">**Method:** POST</span></span>
        - <span data-ttu-id="c9de4-183">**Taotluse URL:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="c9de4-183">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="c9de4-184">**Taotluse keha:** {"executionId": body('GetExportedPackageURL')?['value']}</span><span class="sxs-lookup"><span data-stu-id="c9de4-184">**Body of the request:** {"executionId": body('GetExportedPackageURL')?['value']}</span></span>

        ![Tegevus GetExportedPackageURL](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="c9de4-186">Laadige eksporditud pakett alla.</span><span class="sxs-lookup"><span data-stu-id="c9de4-186">Download the exported package.</span></span>

    - <span data-ttu-id="c9de4-187">Lisage HTTP taotlus **GET** (sisseehitatud [HTTP konnektori tegevus](https://docs.microsoft.com/azure/connectors/connectors-native-http)), et laadida pakett alla URL-ilt, mis eelmises etapis tagastati.</span><span class="sxs-lookup"><span data-stu-id="c9de4-187">Add an HTTP **GET** request (a built-in [HTTP connector action](https://docs.microsoft.com/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="c9de4-188">**Meetod:** GET</span><span class="sxs-lookup"><span data-stu-id="c9de4-188">**Method:** GET</span></span>
        - <span data-ttu-id="c9de4-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="c9de4-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="c9de4-190">Võimalik, et peate sisestama väärtuse **URI** kas koodi vaates või kujundaja funktsioonide redaktoris.</span><span class="sxs-lookup"><span data-stu-id="c9de4-190">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![HTTP tegevus GET](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="c9de4-192">See taotlus ei nõua ühtegi täiendavat autentimist, kuna API **GetExportedPackageUrl** tagastatav URL sisaldab ühiskasutusega juurdepääsu allkirja luba, mis annab juurdepääsu faili allalaadimisele.</span><span class="sxs-lookup"><span data-stu-id="c9de4-192">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="c9de4-193">Salvestage allalaaditud pakett, kasutades konnektorit [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness).</span><span class="sxs-lookup"><span data-stu-id="c9de4-193">Save the downloaded package by using the [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="c9de4-194">Lisage OneDrive for Businessi tegevus [Loo fail](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file).</span><span class="sxs-lookup"><span data-stu-id="c9de4-194">Add a OneDrive for Business [Create File](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="c9de4-195">Ühendage vastavalt vajadusele oma OneDrive for Businessi konto.</span><span class="sxs-lookup"><span data-stu-id="c9de4-195">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="c9de4-196">**Kausta tee:** teie valitud kaust</span><span class="sxs-lookup"><span data-stu-id="c9de4-196">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="c9de4-197">**Failinimi:** worker\_package.zip</span><span class="sxs-lookup"><span data-stu-id="c9de4-197">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="c9de4-198">**Faili sisu:** keha eelmisest etapist (dünaamiline sisu)</span><span class="sxs-lookup"><span data-stu-id="c9de4-198">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![Faili loomise tegevus](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="c9de4-200">3. etapp: loogikarakenduse testimine</span><span class="sxs-lookup"><span data-stu-id="c9de4-200">Step 3: Test the logic app</span></span>

<span data-ttu-id="c9de4-201">Oma loogikarakenduse testimiseks valige kujundajas nupp **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="c9de4-201">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="c9de4-202">Näete, et loogikarakenduse etapid algavad.</span><span class="sxs-lookup"><span data-stu-id="c9de4-202">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="c9de4-203">Pärast 30 kuni 40 sekundit peaks loogikarakendus lõpetama töötamise ja teie OneDrive for Businessi kaust peaks sisaldama uut pakettfali, mis sisaldab eksporditud töötajaid.</span><span class="sxs-lookup"><span data-stu-id="c9de4-203">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="c9de4-204">Kui mõnes etapis esitatakse tõrge, valige kujundajas nurjunud etapp ja kontrollige selle väljasid **Sisendid** ja **Väljundid**.</span><span class="sxs-lookup"><span data-stu-id="c9de4-204">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="c9de4-205">Siluge ja reguleerige etappi tõrgete kõrvaldamiseks vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="c9de4-205">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="c9de4-206">Järgmisel joonisel on näha, kuidas Logic Apps Designer välja näeb, kui kõik loogikarakenduse etapid töötavad edukalt.</span><span class="sxs-lookup"><span data-stu-id="c9de4-206">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![Edukas loogikarakenduse töötamine](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="c9de4-208">Kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="c9de4-208">Summary</span></span>

<span data-ttu-id="c9de4-209">Selles õpetuses saite teada, kuidas kasutada loogikarakendusi, et eksportida andmeid rakendusest Human Resources, ja salvestada eksporditud andmed OneDrive for Businessi kausta.</span><span class="sxs-lookup"><span data-stu-id="c9de4-209">In this tutorial, you learned how to use a logic app to export data from Human Resources and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="c9de4-210">Saate selle õpetuse etappe vastavalt vajadusele muuta, et need vastaksid teie ettevõtte vajadustele.</span><span class="sxs-lookup"><span data-stu-id="c9de4-210">You can modify the steps of this tutorial as required to suit your business needs.</span></span>


