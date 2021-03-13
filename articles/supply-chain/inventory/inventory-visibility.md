---
title: Varude nähtavuse lisandmoodul
description: See teema kirjeldab varude nähtavuse lisandmooduli installimist ja konfigureerimist Dynamics 365 Supply Chain Managementi jaoks.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114666"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="60772-103">Varude nähtavuse lisandmoodul</span><span class="sxs-lookup"><span data-stu-id="60772-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="60772-104">Varude nähtavuse lisandmoodul on sõltumatu ja väga muutuv mikroteenus, mis võimaldab reaalajas vaba kaubavaru jälgimist, andes seega ülevaate varude nähtavuse kohta.</span><span class="sxs-lookup"><span data-stu-id="60772-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="60772-105">Kogu vaba kaubavaruga seotud teave eksporditakse teenusesse peaaegu reaalajas madalama taseme SQL-i integratsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="60772-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="60772-106">Välised süsteemid pääsevad teenusele juurde avatud API-de kaudu, et teha päringuid antud dimensioonide kogumi kohta, seega hankides saadaolevate vabade ametikohtade loendi.</span><span class="sxs-lookup"><span data-stu-id="60772-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="60772-107">Varude nähtavus on teenusel Microsoft Dataverse rajanev mikroteenus, mis tähendab, et saate seda laiendada, luues rakendusi Power Apps ja rakendades Power BI, et võimaldada ärivajaduste täitmiseks kohandatud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="60772-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="60772-108">Samuti on võimalik uuendada indeksit laopäringute tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="60772-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="60772-109">Varude nähtavus pakub konfigureerimisvõimalusi, mis võimaldavad seda integreerida mitme kolmanda osapoole süsteemidega.</span><span class="sxs-lookup"><span data-stu-id="60772-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="60772-110">See toetab standardset varude dimensiooni, kohandatud laiendatavust ning standardiseeritud konfigureeritavaid ja arvutatavaid koguseid.</span><span class="sxs-lookup"><span data-stu-id="60772-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="60772-111">Selles teemas kirjeldatakse, kuidas installida ja konfigureerida varude nähtavuse lisandmoodul Dynamics 365 Supply Chain Managementi jaoks ja kuidas kasutada rakenduse programmeerimise liidest (API).</span><span class="sxs-lookup"><span data-stu-id="60772-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="60772-112">Varude nähtavuse lisandmooduli installimine</span><span class="sxs-lookup"><span data-stu-id="60772-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="60772-113">Varude nähtavuse lisandmooduli saate installida, kasutades teenust Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="60772-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="60772-114">LCS on koostööportaal, mis pakub keskkonda ja regulaarselt värskendatud teenuseid, mis aitavad hallata Dynamics 365 Finance and Operationsi rakenduste töötsüklit.</span><span class="sxs-lookup"><span data-stu-id="60772-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="60772-115">Lisateabe saamiseks vt [Lifecycle Servicesi ressursid](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="60772-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="60772-116">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="60772-116">Prerequisites</span></span>

<span data-ttu-id="60772-117">Enne varude nähtavuse lisandmooduli installimist peate tegema järgmist.</span><span class="sxs-lookup"><span data-stu-id="60772-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="60772-118">Hankige LCS-i juurutamise projekt, millel on vähemalt üks juurutatud keskkond.</span><span class="sxs-lookup"><span data-stu-id="60772-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="60772-119">Looge oma LCS-i pakkumise beeta-võtmed.</span><span class="sxs-lookup"><span data-stu-id="60772-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="60772-120">Lubage oma pakkumise beeta-võtmeid oma kasutajale LCS-is.</span><span class="sxs-lookup"><span data-stu-id="60772-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="60772-121">Kontakteeruge Microsofti varude nähtavuse tootemeeskonnaga ja sisestage keskkonna ID, kus soovite varude nähtavuse lisandmoodulit kasutada.</span><span class="sxs-lookup"><span data-stu-id="60772-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="60772-122">Kui teil on küsimusi nende eeltingimuste kohta, võtke ühendust varude nähtavuse tootemeeskonnaga.</span><span class="sxs-lookup"><span data-stu-id="60772-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="60772-123">Lisandmooduli installimine</span><span class="sxs-lookup"><span data-stu-id="60772-123">Install the add-in</span></span>

<span data-ttu-id="60772-124">Varude nähtavuse lisandmooduli installimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="60772-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="60772-125">Logige sisse [teenuse Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portaali.</span><span class="sxs-lookup"><span data-stu-id="60772-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="60772-126">Avalehel valige projekt, kus teie keskkond juurutati.</span><span class="sxs-lookup"><span data-stu-id="60772-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="60772-127">Projekti lehel valige keskkond, kuhu soovite lisandmooduli installida.</span><span class="sxs-lookup"><span data-stu-id="60772-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="60772-128">Liikuge keskkonna lehel kerides allapoole, kuni kuvatakse jaotis **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="60772-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="60772-129">Kui jaotist ei ole näha, veenduge, et eeltingimuseks olevad beeta-võtmed oleksid täielikult töödeldud.</span><span class="sxs-lookup"><span data-stu-id="60772-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="60772-130">Valige jaotises **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="60772-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="60772-131">![LCS-i keskkonna leht](media/inventory-visibility-environment.png "LCS-i keskkonna leht")</span><span class="sxs-lookup"><span data-stu-id="60772-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="60772-132">Valige link **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="60772-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="60772-133">Avaneb saadaolevate lisandmoodulite loend.</span><span class="sxs-lookup"><span data-stu-id="60772-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="60772-134">Valige loendist **Varude teenus**.</span><span class="sxs-lookup"><span data-stu-id="60772-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="60772-135">(Pidage meeles, et selle nimi loendis võib nüüd olla **Dynamics 365 Supply Chain Managementi varude nähtavuse lisandmoodul**.)</span><span class="sxs-lookup"><span data-stu-id="60772-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="60772-136">Sisestage oma keskkonna järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="60772-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="60772-137">**AAD Rakenduse ID**</span><span class="sxs-lookup"><span data-stu-id="60772-137">**AAD application ID**</span></span>
    - <span data-ttu-id="60772-138">**AAD Rentniku ID**</span><span class="sxs-lookup"><span data-stu-id="60772-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="60772-139">![Lisandmooduli häälestamise leht](media/inventory-visibility-setup.png "Lisandmooduli häälestamise leht")</span><span class="sxs-lookup"><span data-stu-id="60772-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="60772-140">Nõustuge tingimuste, märkides ruudu **Tingimused**.</span><span class="sxs-lookup"><span data-stu-id="60772-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="60772-141">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="60772-141">Select **Install**.</span></span> <span data-ttu-id="60772-142">Kuvatakse lisandmooduli olek **Installimine**.</span><span class="sxs-lookup"><span data-stu-id="60772-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="60772-143">Kui see on tehtud, värskendage lehte, et näha muutunud olekut **Installitud**.</span><span class="sxs-lookup"><span data-stu-id="60772-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="60772-144">Turbeteenusetõendi hankimine</span><span class="sxs-lookup"><span data-stu-id="60772-144">Get a security service token</span></span>

<span data-ttu-id="60772-145">Hankige turbeteenusetõend, tehes järgmist.</span><span class="sxs-lookup"><span data-stu-id="60772-145">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="60772-146">Logige Azure’i portaali sisse ja kasutage seda rakenduse Supply Chain Management atribuutide `clientId` ja `clientSecret` leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="60772-146">Sign in to Azure Portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="60772-147">Tooge Azure Active Directory luba (`aadToken`), edastades HTTP-taotluse järgmiste atribuutidega:</span><span class="sxs-lookup"><span data-stu-id="60772-147">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="60772-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="60772-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="60772-149">**Meetod** - `GET`</span><span class="sxs-lookup"><span data-stu-id="60772-149">**Method** - `GET`</span></span>
    - <span data-ttu-id="60772-150">**Sisu (vormi andmed)**:</span><span class="sxs-lookup"><span data-stu-id="60772-150">**Body content (form data)**:</span></span>

        | <span data-ttu-id="60772-151">key</span><span class="sxs-lookup"><span data-stu-id="60772-151">key</span></span> | <span data-ttu-id="60772-152">väärtus</span><span class="sxs-lookup"><span data-stu-id="60772-152">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="60772-153">client_id</span><span class="sxs-lookup"><span data-stu-id="60772-153">client_id</span></span> | <span data-ttu-id="60772-154">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="60772-154">${aadAppId}</span></span> |
        | <span data-ttu-id="60772-155">client_secret</span><span class="sxs-lookup"><span data-stu-id="60772-155">client_secret</span></span> | <span data-ttu-id="60772-156">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="60772-156">${aadAppSecret}</span></span> |
        | <span data-ttu-id="60772-157">grant_type</span><span class="sxs-lookup"><span data-stu-id="60772-157">grant_type</span></span> | <span data-ttu-id="60772-158">client_credentials</span><span class="sxs-lookup"><span data-stu-id="60772-158">client_credentials</span></span> |
        | <span data-ttu-id="60772-159">resource</span><span class="sxs-lookup"><span data-stu-id="60772-159">resource</span></span> | <span data-ttu-id="60772-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="60772-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="60772-161">Peaksite saama vastuseks atribuudi `aadToken`, mis sarnaneb järgmise näitega.</span><span class="sxs-lookup"><span data-stu-id="60772-161">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="60772-162">Vormindage JSON-i taotlus, mis sarnaneb järgmisele:</span><span class="sxs-lookup"><span data-stu-id="60772-162">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="60772-163">Kus</span><span class="sxs-lookup"><span data-stu-id="60772-163">Where:</span></span>
    - <span data-ttu-id="60772-164">Väärtus `client_assertion` peab olema `aadToken`, mille eelmises sammus saite.</span><span class="sxs-lookup"><span data-stu-id="60772-164">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="60772-165">Väärtus `context` peab olema keskkonna ID, kus soovite lisandmooduli juurutada.</span><span class="sxs-lookup"><span data-stu-id="60772-165">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="60772-166">Häälestage kõik muud väärtused, nagu näites näidatud.</span><span class="sxs-lookup"><span data-stu-id="60772-166">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="60772-167">Edastage HTTP-taotlus järgmiste atribuutidega:</span><span class="sxs-lookup"><span data-stu-id="60772-167">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="60772-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="60772-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="60772-169">**Meetod** - `POST`</span><span class="sxs-lookup"><span data-stu-id="60772-169">**Method** - `POST`</span></span>
    - <span data-ttu-id="60772-170">**HTTP päis** – lisage API versioon (võti on `Api-Version` ja väärtus on`1.0`)</span><span class="sxs-lookup"><span data-stu-id="60772-170">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="60772-171">**Sisu** – lisage eelmises sammus loodud JSON-i taotlus.</span><span class="sxs-lookup"><span data-stu-id="60772-171">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="60772-172">Saate vastuseks tõendi `access_token`.</span><span class="sxs-lookup"><span data-stu-id="60772-172">You will get an `access_token` in response.</span></span> <span data-ttu-id="60772-173">Seda on teil vaja juurepääsuloaks, et kutsuda nähtavuse API.</span><span class="sxs-lookup"><span data-stu-id="60772-173">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="60772-174">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="60772-174">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="60772-175">Lisandmooduli desinstallimine</span><span class="sxs-lookup"><span data-stu-id="60772-175">Uninstall the add-in</span></span>

<span data-ttu-id="60772-176">Lisandmooduli desinstallimiseks valige nupp **Desinstalli**.</span><span class="sxs-lookup"><span data-stu-id="60772-176">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="60772-177">Värskendage LCS-i ja varude nähtavuse lisandmoodul eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="60772-177">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="60772-178">Desinstallimise käigus eemaldatakse lisandmoodul ja käivitatakse ka töö, et kustutada kõik teenuses talletatud äriandmed.</span><span class="sxs-lookup"><span data-stu-id="60772-178">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="60772-179">Varude nähtavuse lisandmooduli avalik API</span><span class="sxs-lookup"><span data-stu-id="60772-179">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="60772-180">Varude nähtavuse lisandmooduli avalik REST API esitab integreerimiseks mitu kindlat lõpp-punkti.</span><span class="sxs-lookup"><span data-stu-id="60772-180">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="60772-181">See toetab kolme peamist suhtlustüüpi.</span><span class="sxs-lookup"><span data-stu-id="60772-181">It supports three main interaction types:</span></span>

- <span data-ttu-id="60772-182">Lisandmoodulisse vaba kaubavaru muudatuste sisestamine välise süsteemi kaudu.</span><span class="sxs-lookup"><span data-stu-id="60772-182">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="60772-183">Praegu vaba kaubavaru päring välisest süsteemist.</span><span class="sxs-lookup"><span data-stu-id="60772-183">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="60772-184">Saadaval on automaatne sünkroonimine Supply Chain Managementiga.</span><span class="sxs-lookup"><span data-stu-id="60772-184">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="60772-185">Automaatne sünkroonimine ei ole osa avalikust API-st, aga see toimub taustal keskkonnas, kus on lubatud laovarude nähtavuse lisandmoodul.</span><span class="sxs-lookup"><span data-stu-id="60772-185">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="60772-186">Autentimine</span><span class="sxs-lookup"><span data-stu-id="60772-186">Authentication</span></span>

<span data-ttu-id="60772-187">Platvormi turbetõendit kasutatakse varude nähtavuse lisandmooduli kutsumiseks, seega tuleb teil Azure Active Directory rakenduse abil luua luba Azure Active Directory tõend.</span><span class="sxs-lookup"><span data-stu-id="60772-187">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="60772-188">Lisateavet selle kohta, kuidas saada turbetõend, leiate teemast [Varude nähtavuse lisandmooduli installimine](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="60772-188">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="60772-189">Varude nähtavuse API konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="60772-189">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="60772-190">Enne teenuse kasutamist peate tegema järgmistes jaotistes kirjeldatud konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="60772-190">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="60772-191">Konfiguratsioon võib teie keskkonna üksikasjade põhjal erineda.</span><span class="sxs-lookup"><span data-stu-id="60772-191">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="60772-192">See hõlmab peamiselt nelja osa.</span><span class="sxs-lookup"><span data-stu-id="60772-192">It primarily includes four parts:</span></span>

- [<span data-ttu-id="60772-193">Eraldamine</span><span class="sxs-lookup"><span data-stu-id="60772-193">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="60772-194">Dimensioonide konfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="60772-194">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="60772-195">Indekseerimine</span><span class="sxs-lookup"><span data-stu-id="60772-195">Indexing</span></span>](#indexing)
- [<span data-ttu-id="60772-196">Kohandatud mõõtmine</span><span class="sxs-lookup"><span data-stu-id="60772-196">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="60772-197">Sektsioonimine</span><span class="sxs-lookup"><span data-stu-id="60772-197">Partitioning</span></span>

<span data-ttu-id="60772-198">Sektsioonimine võib oluliselt mõjutada varude nähtavuse API jõudlust.</span><span class="sxs-lookup"><span data-stu-id="60772-198">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="60772-199">Mõistlik on määratleda skeem, mis võimaldab väikseid andmegruppe, aga samas ka sisukaid andmepäringuid.</span><span class="sxs-lookup"><span data-stu-id="60772-199">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="60772-200">`organizationId` (Supply Chain Managementis `dataAreaId`) on alati osa sektsioonimisest ja varude nähtavuse vaikeväärtuseks on määratud sektsioonid, mille dimensioonid on *Sait +asukoht*.</span><span class="sxs-lookup"><span data-stu-id="60772-200">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="60772-201">See tähendab, et teenusepäringu esitamiseks peab need dimensioonid alati filtreerima.</span><span class="sxs-lookup"><span data-stu-id="60772-201">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="60772-202">*Sait* ja *asukoht* on varude nähtavuses kaks üldist vaikedimensiooni.</span><span class="sxs-lookup"><span data-stu-id="60772-202">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="60772-203">Supply Chain Managementis nimetatakse neid dimensioone *saidiks* (`InventSiteId`) ja *laoks* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="60772-203">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="60772-204">Dimensioonide konfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="60772-204">Dimension configurations</span></span>

<span data-ttu-id="60772-205">Varude nähtavus annab loendi üldistest dimensioonidest, et lubada mitme allika süsteemi integreerimist.</span><span class="sxs-lookup"><span data-stu-id="60772-205">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="60772-206">Järgmises tabelis loetletakse varude dimensioonid, mis on varude nähtavuse dimensioonide nimed.</span><span class="sxs-lookup"><span data-stu-id="60772-206">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="60772-207">Dimensiooni tüüp</span><span class="sxs-lookup"><span data-stu-id="60772-207">Dimension type</span></span> | <span data-ttu-id="60772-208">Dimensiooni nimi</span><span class="sxs-lookup"><span data-stu-id="60772-208">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="60772-209">Toode</span><span class="sxs-lookup"><span data-stu-id="60772-209">Product</span></span> | `ColorId` |
| <span data-ttu-id="60772-210">Toode</span><span class="sxs-lookup"><span data-stu-id="60772-210">Product</span></span> | `SizeId` |
| <span data-ttu-id="60772-211">Toode</span><span class="sxs-lookup"><span data-stu-id="60772-211">Product</span></span> | `StyleId` |
| <span data-ttu-id="60772-212">Toode</span><span class="sxs-lookup"><span data-stu-id="60772-212">Product</span></span> | `ConfigId` |
| <span data-ttu-id="60772-213">Jälitamine</span><span class="sxs-lookup"><span data-stu-id="60772-213">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="60772-214">Jälitamine</span><span class="sxs-lookup"><span data-stu-id="60772-214">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="60772-215">Koht</span><span class="sxs-lookup"><span data-stu-id="60772-215">Location</span></span> | `LocationId` |
| <span data-ttu-id="60772-216">Koht</span><span class="sxs-lookup"><span data-stu-id="60772-216">Location</span></span> | `SiteId` |
| <span data-ttu-id="60772-217">Varude olek</span><span class="sxs-lookup"><span data-stu-id="60772-217">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="60772-218">Laopõhine</span><span class="sxs-lookup"><span data-stu-id="60772-218">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="60772-219">Laopõhine</span><span class="sxs-lookup"><span data-stu-id="60772-219">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="60772-220">Laopõhine</span><span class="sxs-lookup"><span data-stu-id="60772-220">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="60772-221">Eelmises tabelis loetletud dimensiooni tüüp on ainult teave.</span><span class="sxs-lookup"><span data-stu-id="60772-221">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="60772-222">Varude nähtavuses ei ole vaja määratleda dimensiooni tüüpi.</span><span class="sxs-lookup"><span data-stu-id="60772-222">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="60772-223">Kui on olemas kohandatud dimensioon ja see peab muutuma vaikeväärtuseks, kui varude nähtavus seda kasutab, saate **kohandatud dimensiooni** nime varude nähtavuses konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="60772-223">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="60772-224">Väliste süsteemide juurdepääs varude nähtavusele läbi RESTfuli API-de, mis võimaldavad esitada teavet antud dimensioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="60772-224">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="60772-225">Integratsiooni jaoks võimaldab varude nähtavus teil konfigureerida *väliskanali andmeallika* ja lähtedimensiooni vastavalt *sihtdimensioonile* varude nähtavuse korral.</span><span class="sxs-lookup"><span data-stu-id="60772-225">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="60772-226">Sihtdimensioonid peavad hõlmama ühte järgmistest.</span><span class="sxs-lookup"><span data-stu-id="60772-226">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="60772-227">Varude nähtavuse vaikedimensioonid</span><span class="sxs-lookup"><span data-stu-id="60772-227">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="60772-228">Kohandatud dimensioonid</span><span class="sxs-lookup"><span data-stu-id="60772-228">Custom dimensions</span></span>

<span data-ttu-id="60772-229">Dimensioonide konfigureerimise eesmärk on ühtlustada mitme süsteemi integreerimist vastavalt päringule dimensioonide ja sisestamise sündmuse dimensioonidega.</span><span class="sxs-lookup"><span data-stu-id="60772-229">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="60772-230">Indekseerimine</span><span class="sxs-lookup"><span data-stu-id="60772-230">Indexing</span></span>

<span data-ttu-id="60772-231">Enamiku ajast ei ole vaba kaubavaru päring mitte ainult kõrgeimal „kogutasemel“, kuid soovi korral saate vaadata varude dimensioonide alusel summeeritud tulemusi.</span><span class="sxs-lookup"><span data-stu-id="60772-231">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="60772-232">Varude nähtavus annab paindlikkuse, lubades teil häälestada indekseid, mis põhinevad dimensioonil või dimensioonide kombinatsioonil.</span><span class="sxs-lookup"><span data-stu-id="60772-232">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="60772-233">Praegu saate indekseid konfigureerida ainult kuni viieni.</span><span class="sxs-lookup"><span data-stu-id="60772-233">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="60772-234">Peate hoolikalt kaaluma, millist dimensiooni või dimensioonide kombinatsiooni kasutate enne rakendamist, et tagada selle vastavus teie ettevõtte vajadustele.</span><span class="sxs-lookup"><span data-stu-id="60772-234">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="60772-235">Näiteks kui soovite teha päringuid toodete kohta järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="60772-235">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="60772-236">Päring saadaval oleva summeeritud toote kohta *värvi* ja *suuruse* dimensioonide kaupa.</span><span class="sxs-lookup"><span data-stu-id="60772-236">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="60772-237">Mõnel juhul soovite ainult toote kohta päringut esitada.</span><span class="sxs-lookup"><span data-stu-id="60772-237">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="60772-238">Teil oleks kaks indeksit, mis on määratletud järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="60772-238">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="60772-239">Tühi sulg summeeritakse sektsioonis toote ID põhjal.</span><span class="sxs-lookup"><span data-stu-id="60772-239">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="60772-240">Indekseerimine määratleb, kuidas saate oma tulemusi grupeerida päringusätte `groupBy` alusel.</span><span class="sxs-lookup"><span data-stu-id="60772-240">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="60772-241">Sel juhul, kui te ei määratle ühtegi sätte `groupBy` väärtust, saate kogusummad `productid` kaupa.</span><span class="sxs-lookup"><span data-stu-id="60772-241">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="60772-242">Vastasel juhul, kui määrate `groupBy` väärtuseks `groupBy=ColorId&groupBy=SizeId`, saadetaks teile mitu rida, mis põhinevad süsteemi erinevate värvide ja suuruse kombinatsioonidel.</span><span class="sxs-lookup"><span data-stu-id="60772-242">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="60772-243">Saate esitada päringu kriteeriumid päringu sisus.</span><span class="sxs-lookup"><span data-stu-id="60772-243">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="60772-244">Siin on näide päringust toote värvi ja suuruse kombinatsiooniga.</span><span class="sxs-lookup"><span data-stu-id="60772-244">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="60772-245">Kohandatud mõõtmine</span><span class="sxs-lookup"><span data-stu-id="60772-245">Custom measurement</span></span>

<span data-ttu-id="60772-246">Vaikimisi mõõtmiskogused on seotud Supply Chain Managementiga, kuid soovi korral võib olla kogus, mis koosneb vaikimisi mõõtmiste kombinatsioonist.</span><span class="sxs-lookup"><span data-stu-id="60772-246">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="60772-247">Selleks võib olla kohandatud koguste konfiguratsioon, mis lisatakse vabade päringute väljundile.</span><span class="sxs-lookup"><span data-stu-id="60772-247">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="60772-248">Funktsioon võimaldab teil kohandatud mõõtmiseks määratleda lisatavate mõõtude kogumi ja/või meetmete kogumi, mis on kohandatud mõõtmisest lahutatud.</span><span class="sxs-lookup"><span data-stu-id="60772-248">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="60772-249">Näiteks järgmise päringu tingimusega konfigureerite kohandatud mõõtmise koguse üksusena `MyCustomAvailableforReservation`, mida tarbib tarbimise süsteem.</span><span class="sxs-lookup"><span data-stu-id="60772-249">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="60772-250">Tarbimise süsteem</span><span class="sxs-lookup"><span data-stu-id="60772-250">Consumption system</span></span> | <span data-ttu-id="60772-251">Arvutatud mõõdikud</span><span class="sxs-lookup"><span data-stu-id="60772-251">Calculated measurers</span></span> | <span data-ttu-id="60772-252">Andmeallikas</span><span class="sxs-lookup"><span data-stu-id="60772-252">Data source</span></span> | <span data-ttu-id="60772-253">Muutuja</span><span class="sxs-lookup"><span data-stu-id="60772-253">Modifier</span></span> | <span data-ttu-id="60772-254">Muutuja arvutustüüp</span><span class="sxs-lookup"><span data-stu-id="60772-254">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="60772-255">Lisa</span><span class="sxs-lookup"><span data-stu-id="60772-255">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="60772-256">Lisa</span><span class="sxs-lookup"><span data-stu-id="60772-256">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="60772-257">Lahutamine</span><span class="sxs-lookup"><span data-stu-id="60772-257">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="60772-258">Lisa</span><span class="sxs-lookup"><span data-stu-id="60772-258">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="60772-259">Lahutamine</span><span class="sxs-lookup"><span data-stu-id="60772-259">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="60772-260">Lisa</span><span class="sxs-lookup"><span data-stu-id="60772-260">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="60772-261">Lisa</span><span class="sxs-lookup"><span data-stu-id="60772-261">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="60772-262">Lahutamine</span><span class="sxs-lookup"><span data-stu-id="60772-262">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="60772-263">Lahutamine</span><span class="sxs-lookup"><span data-stu-id="60772-263">Subtraction</span></span> |

<span data-ttu-id="60772-264">Sellega tagastatakse kohandatud mõõtmise koguse päring järgmise väljundina.</span><span class="sxs-lookup"><span data-stu-id="60772-264">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="60772-265">Üksuse `MyCustomAvailableforReservation` väljundi aluseks on kohandatud mõõtmiste arvutamise säte.</span><span class="sxs-lookup"><span data-stu-id="60772-265">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="60772-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="60772-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="60772-267">Vaba kaubavaru muudatuste sisestamine</span><span class="sxs-lookup"><span data-stu-id="60772-267">Posting on-hand changes</span></span>

<span data-ttu-id="60772-268">Sündmuse sisestamise täpne URL sõltub geograafilisest piirkonnast.</span><span class="sxs-lookup"><span data-stu-id="60772-268">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="60772-269">See on järgmises vormis.</span><span class="sxs-lookup"><span data-stu-id="60772-269">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="60772-270">Kui see on autenditud, saab seda URL-i kasutada koos HTTP `POST`-meetodiga, et saata teenusele vaba kaubavaru muudatuste sündmusi.</span><span class="sxs-lookup"><span data-stu-id="60772-270">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="60772-271">Dynamics 365 teenustega suhtlemiseks HTTP-taotluste kaudu kasutatakse spetsiaalset päist, mis tähistab Supply Chain Managementi eksemplari keskkonna ID-d, millega andmed on lingitud.</span><span class="sxs-lookup"><span data-stu-id="60772-271">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="60772-272">Näide:</span><span class="sxs-lookup"><span data-stu-id="60772-272">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="60772-273">Vaba kaubavaru muudatuste päringu sisestamise näide 1</span><span class="sxs-lookup"><span data-stu-id="60772-273">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="60772-274">See näide näitab olukorda, kus häälestate dimensiooni konfiguratsiooni Power Appsis.</span><span class="sxs-lookup"><span data-stu-id="60772-274">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="60772-275">Kasutage järgmist päringut dimensioonide vastenduste konfigureerimiseks Power Appsis.</span><span class="sxs-lookup"><span data-stu-id="60772-275">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="60772-276">Nüüd saate päringus määrata väärtuse `dimensionDataSource` ja kasutada kohandatud dimensioone.</span><span class="sxs-lookup"><span data-stu-id="60772-276">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="60772-277">Süsteem teisendab kohandatud dimensioonid automaatselt põhidimensioonideks.</span><span class="sxs-lookup"><span data-stu-id="60772-277">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="60772-278">Vaba kaubavaru muudatuste päringu sisestamise näide 2</span><span class="sxs-lookup"><span data-stu-id="60772-278">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="60772-279">Selles näites kuvatakse stsenaarium, kus dimensioonide konfigureerimise jaoks pole vastendusi Power Appsis vastendusi häälestatud, nii et sisestamisel tuleks samuti põhidimensioone kasutada.</span><span class="sxs-lookup"><span data-stu-id="60772-279">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="60772-280">Kõik dimensioonid peavad olema põhidimensioonid, kui väli `dimensionDataSource` on väärtusega null, tühi või seal on tühik.</span><span class="sxs-lookup"><span data-stu-id="60772-280">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="60772-281">JSON-dokumendi väljade atribuudid</span><span class="sxs-lookup"><span data-stu-id="60772-281">JSON document field properties</span></span>

<span data-ttu-id="60772-282">Eespool antud JSON-päringu näidete väljadel on järgmises tabelis loetletud atribuudid.</span><span class="sxs-lookup"><span data-stu-id="60772-282">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="60772-283">Välja kood</span><span class="sxs-lookup"><span data-stu-id="60772-283">Field ID</span></span> | <span data-ttu-id="60772-284">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="60772-284">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="60772-285">Konkreetse muudatuse sündmuse kordumatu ID.</span><span class="sxs-lookup"><span data-stu-id="60772-285">A unique ID for the specific change event.</span></span> <span data-ttu-id="60772-286">Seda ID-d kasutatakse tagamaks, et kui suhtlus teenusega nurjub sisestamise ajal, ei põhjustaks sündmuse taasesitamine süsteemis sama sündmuse topeltloendamist.</span><span class="sxs-lookup"><span data-stu-id="60772-286">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="60772-287">Sündmusega lingitud organisatsiooni identifikaator.</span><span class="sxs-lookup"><span data-stu-id="60772-287">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="60772-288">See vastendab Supply Chain Managementi organisatsioonide või andmepiirkonna ID-sid.</span><span class="sxs-lookup"><span data-stu-id="60772-288">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="60772-289">Kõnealuse toote identifikaator.</span><span class="sxs-lookup"><span data-stu-id="60772-289">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="60772-290">Kogus, mille võrra laoseisu tuleb muuta.</span><span class="sxs-lookup"><span data-stu-id="60772-290">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="60772-291">Kui riiulile lisati näiteks kümme uut saiakest, oleks see väärtus 10.</span><span class="sxs-lookup"><span data-stu-id="60772-291">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="60772-292">Kui riiulilt eemaldati või müüdi kolm saiakest, oleks see väärtus -3.</span><span class="sxs-lookup"><span data-stu-id="60772-292">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="60772-293">See on sisestatud muudatuse sündmuses ja päringus kasutatud andmeallikas.</span><span class="sxs-lookup"><span data-stu-id="60772-293">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="60772-294">Andmeallika määramisel saate kasutada määratud andmeallika kohandatud dimensioone.</span><span class="sxs-lookup"><span data-stu-id="60772-294">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="60772-295">Dimensiooni konfigureerimisega saab varude nähtavus vastendada kohandatud dimensioonid üldiste vaikedimensioonidega.</span><span class="sxs-lookup"><span data-stu-id="60772-295">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="60772-296">Kui väärtust `dimensionDataSource` pole määratud, saate päringutes kasutada ainult üldisi vaikedimensioone.</span><span class="sxs-lookup"><span data-stu-id="60772-296">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="60772-297">Dünaamiline võtme-/väärtusepaari mapp.</span><span class="sxs-lookup"><span data-stu-id="60772-297">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="60772-298">Need vastendavad mõned dimensioonid Supply Chain Managementis, kuid võite lisada ka kohandatud dimensioone (nt *Allikas*), mis võib tähistada sündmuse pärinemist Supply Chain Managementist või välisest süsteemist.</span><span class="sxs-lookup"><span data-stu-id="60772-298">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="60772-299">Praeguse vaba kaubavaru päring</span><span class="sxs-lookup"><span data-stu-id="60772-299">Querying current on-hand</span></span>

<span data-ttu-id="60772-300">Praeguse laoseisu päringute puhul on lõpp-punktil sarnane URL.</span><span class="sxs-lookup"><span data-stu-id="60772-300">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="60772-301">See on päringus meetodiga HTTP `POST`.</span><span class="sxs-lookup"><span data-stu-id="60772-301">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="60772-302">Praeguse vaba kaubavaru päringu näide 1</span><span class="sxs-lookup"><span data-stu-id="60772-302">Current on-hand query example 1</span></span>

<span data-ttu-id="60772-303">See näide näitab olukorda, kus olete Power Appsis dimensioonide konfigureerimise juba lõpule viinud.</span><span class="sxs-lookup"><span data-stu-id="60772-303">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="60772-304">Kasutage järgmist päringut dimensioonide vastenduste konfigureerimiseks Power Appsis.</span><span class="sxs-lookup"><span data-stu-id="60772-304">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="60772-305">Nüüd saate päringus määrata väärtuse `dimensionDataSource` ja kasutada kohandatud dimensioone.</span><span class="sxs-lookup"><span data-stu-id="60772-305">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="60772-306">Süsteem teisendab kohandatud dimensioonid automaatselt põhidimensioonideks.</span><span class="sxs-lookup"><span data-stu-id="60772-306">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="60772-307">Saate määrata väärtuse `DimensionDataSource` üksusel `filters` ja määrata kohandatud dimensioonid nii üksuse `filters` kui ka `groupByValues` jaoks.</span><span class="sxs-lookup"><span data-stu-id="60772-307">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="60772-308">Süsteem teisendab kohandatud dimensioonid automaatselt põhidimensioonideks.</span><span class="sxs-lookup"><span data-stu-id="60772-308">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="60772-309">Praeguse vaba kaubavaru päringu näide 2</span><span class="sxs-lookup"><span data-stu-id="60772-309">Current on-hand query example 2</span></span>

<span data-ttu-id="60772-310">Selles näites kuvatakse stsenaarium, kus dimensioonide konfigureerimise jaoks pole vastendusi Power Appsis vastendusi häälestatud, nii et sisestamisel tuleks samuti põhidimensioone kasutada.</span><span class="sxs-lookup"><span data-stu-id="60772-310">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="60772-311">Kõik dimensioonid peavad olema põhidimensioonid, kui väli `dimensionDataSource` jaotises `filters` on väärtusega null, tühi või seal on tühik.</span><span class="sxs-lookup"><span data-stu-id="60772-311">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="60772-312">Näide tagastatud tulemusest</span><span class="sxs-lookup"><span data-stu-id="60772-312">Example return result</span></span>

<span data-ttu-id="60772-313">Eelmistes näidetes kuvatud päringud võivad tagastada sellise tulemuse.</span><span class="sxs-lookup"><span data-stu-id="60772-313">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="60772-314">Võtke arvesse, et koguseväljad on struktuurilt justkui meetmete ja nendega seotud väärtuste sõnastikud.</span><span class="sxs-lookup"><span data-stu-id="60772-314">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
