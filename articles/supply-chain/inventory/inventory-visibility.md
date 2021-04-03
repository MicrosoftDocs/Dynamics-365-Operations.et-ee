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
ms.openlocfilehash: 4e588be2ac5aae395ca66e3c9a743a67d71db7c0
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574218"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="a7fe1-103">Varude nähtavuse lisandmoodul</span><span class="sxs-lookup"><span data-stu-id="a7fe1-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="a7fe1-104">Varude nähtavuse lisandmoodul on sõltumatu ja väga muutuv mikroteenus, mis võimaldab reaalajas vaba kaubavaru jälgimist, andes seega ülevaate varude nähtavuse kohta.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="a7fe1-105">Kogu vaba kaubavaruga seotud teave eksporditakse teenusesse peaaegu reaalajas madalama taseme SQL-i integratsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="a7fe1-106">Välised süsteemid pääsevad teenusele juurde avatud API-de kaudu, et teha päringuid antud dimensioonide kogumi kohta, seega hankides saadaolevate vabade ametikohtade loendi.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="a7fe1-107">Varude nähtavus on teenusel Microsoft Dataverse rajanev mikroteenus, mis tähendab, et saate seda laiendada, luues rakendusi Power Apps ja rakendades Power BI, et võimaldada ärivajaduste täitmiseks kohandatud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="a7fe1-108">Samuti on võimalik uuendada indeksit laopäringute tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="a7fe1-109">Varude nähtavus pakub konfigureerimisvõimalusi, mis võimaldavad seda integreerida mitme kolmanda osapoole süsteemidega.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="a7fe1-110">See toetab standardset varude dimensiooni, kohandatud laiendatavust ning standardiseeritud konfigureeritavaid ja arvutatavaid koguseid.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="a7fe1-111">Selles teemas kirjeldatakse, kuidas installida ja konfigureerida varude nähtavuse lisandmoodul Dynamics 365 Supply Chain Managementi jaoks ja kuidas kasutada rakenduse programmeerimise liidest (API).</span><span class="sxs-lookup"><span data-stu-id="a7fe1-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="a7fe1-112">Varude nähtavuse lisandmooduli installimine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="a7fe1-113">Varude nähtavuse lisandmooduli saate installida, kasutades teenust Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a7fe1-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="a7fe1-114">LCS on koostööportaal, mis pakub keskkonda ja regulaarselt värskendatud teenuseid, mis aitavad hallata Dynamics 365 Finance and Operationsi rakenduste töötsüklit.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="a7fe1-115">Lisateabe saamiseks vt [Lifecycle Servicesi ressursid](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="a7fe1-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a7fe1-116">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="a7fe1-116">Prerequisites</span></span>

<span data-ttu-id="a7fe1-117">Enne varude nähtavuse lisandmooduli installimist peate tegema järgmist.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="a7fe1-118">Hankige LCS-i juurutamise projekt, millel on vähemalt üks juurutatud keskkond.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="a7fe1-119">Kontrollige, et eeltingimused lisandmoodulite seadistamiseks, mis on antud [Lisandmoodulite ülevaates](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) on täidetud.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="a7fe1-120">Varude nähtavus ei nõua topeltkirjutuse linkimist.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="a7fe1-121">Võtke ühendust varude nähtavuse töörühmaga [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) nende kolme nõutava faili saamiseks:</span><span class="sxs-lookup"><span data-stu-id="a7fe1-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="a7fe1-122">`Inventory Visibility Integration.zip` (Kui Supply Chain Management versioon, mida käitate, on varasem kui versioon 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="a7fe1-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>

> [!NOTE]
> <span data-ttu-id="a7fe1-123">Praegu toetatud riikide ja regioonide hulka kuuluvad Kanada, USA ja Euroopa Liit (EL).</span><span class="sxs-lookup"><span data-stu-id="a7fe1-123">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="a7fe1-124">Kui teil on küsimusi nende eeltingimuste kohta, võtke ühendust varude nähtavuse tootemeeskonnaga.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-124">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="a7fe1-125">Seadistamine Dataverse</span><span class="sxs-lookup"><span data-stu-id="a7fe1-125">Set up Dataverse</span></span>

<span data-ttu-id="a7fe1-126">Läbige need etapid, et seadistada Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-126">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="a7fe1-127">Lisage teenuse põhimõtted oma rentnikule:</span><span class="sxs-lookup"><span data-stu-id="a7fe1-127">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="a7fe1-128">Installige Azure AD PowerShell Module v2, nagu on kirjeldatud [Instalige Azure Active Directory PowerShell Graph'ile](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="a7fe1-128">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="a7fe1-129">Käivitage järgmine PowerShell käsk.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-129">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="a7fe1-130">Looge rakenduse kasutaja varude nähtavuse jaoks platvormil Dataverse:</span><span class="sxs-lookup"><span data-stu-id="a7fe1-130">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="a7fe1-131">Avage oma Dataverse keskkonna URL.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-131">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="a7fe1-132">Minge **Lisaseaded \> Süsteem \> Turvalisus \> Kasutajad** ja looge rakenduse kasutaja.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-132">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="a7fe1-133">Kasutage Vaade menüüd, et muuta lehe vaade **Rakenduse kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-133">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="a7fe1-134">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-134">Select **New**.</span></span> <span data-ttu-id="a7fe1-135">Määrake välja Rakenduse ID väärtuseks *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-135">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="a7fe1-136">(Objekti ID laaditakse muudatuste salvestamisel automaatselt.) Nime saate kohandada.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-136">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="a7fe1-137">Näiteks saate muuta selle *Varude nähtavus*.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-137">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="a7fe1-138">Kui olete lõpetanud, valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-138">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="a7fe1-139">Valige **Määra roll** ja seejärel valige **Süsteemiadministraator**.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-139">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="a7fe1-140">Kui rolli nimi on **Common Data Service Kasutaja**, valige ka see.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-140">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="a7fe1-141">Lisateavet leiate teemast [Rakenduse kasutaja loomine](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="a7fe1-141">For more information, see [Create an application user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="a7fe1-142">Importige `Inventory Visibility Dataverse Solution.zip` fail, mis sisaldab Dataverse konfiguratsiooniga seotud üksusi ja tööriista Power Apps:</span><span class="sxs-lookup"><span data-stu-id="a7fe1-142">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="a7fe1-143">Minge **Lahendused** lehele.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-143">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="a7fe1-144">Valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-144">Select **Import**.</span></span>

1. <span data-ttu-id="a7fe1-145">Importige konfiguratsioonitäienduse käivitusvoog:</span><span class="sxs-lookup"><span data-stu-id="a7fe1-145">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="a7fe1-146">Minge Microsoft Flow lehele.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-146">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="a7fe1-147">Veenduge, et ühendus nimega *Dataverse (pärand)* on olemas.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-147">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="a7fe1-148">(Kui seda pole olemas, looge see.)</span><span class="sxs-lookup"><span data-stu-id="a7fe1-148">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="a7fe1-149">Importige `Inventory Visibility Configuration Trigger.zip` fail.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-149">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="a7fe1-150">Pärast importimist kuvatakse päästik jaotises **Minu vood**.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-150">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="a7fe1-151">Keskkonna teabe põhjal käivitage järgmised neli muutujat:</span><span class="sxs-lookup"><span data-stu-id="a7fe1-151">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="a7fe1-152">Azure'i rentniku ID</span><span class="sxs-lookup"><span data-stu-id="a7fe1-152">Azure Tenant ID</span></span>
        - <span data-ttu-id="a7fe1-153">Azure Rakenduse (klient) ID</span><span class="sxs-lookup"><span data-stu-id="a7fe1-153">Azure Application Client ID</span></span>
        - <span data-ttu-id="a7fe1-154">Azure Rakenduse (klient) Secret</span><span class="sxs-lookup"><span data-stu-id="a7fe1-154">Azure Application Client Secret</span></span>
        - <span data-ttu-id="a7fe1-155">Varude nähtavus lõpp-punkt</span><span class="sxs-lookup"><span data-stu-id="a7fe1-155">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="a7fe1-156">Lisateavet selle muutuja kohta vaadake [Seadistage Varude nähtavuse integreerimine](#setup-inventory-visibility-integration) osas selles teemas edaspidi.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-156">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="a7fe1-157">![Konfiguratsiooni päästik](media/configuration-trigger.png "Konfiguratsiooni päästik")</span><span class="sxs-lookup"><span data-stu-id="a7fe1-157">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="a7fe1-158">Valige **lülita sisse**.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-158">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="a7fe1-159">Lisandmooduli installimine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-159">Install the add-in</span></span>

<span data-ttu-id="a7fe1-160">Varude nähtavuse lisandmooduli installimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-160">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="a7fe1-161">Logige sisse [teenuse Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portaali.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-161">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="a7fe1-162">Avalehel valige projekt, kus teie keskkond juurutati.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-162">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="a7fe1-163">Projekti lehel valige keskkond, kuhu soovite lisandmooduli installida.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-163">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="a7fe1-164">Keskkonna leheküljel kerige alla, kuni näete **Keskkonna lisandmoodulid** jaotist **Power Platform integratsiooni** jaotises, kust leiate Dataverse keskkonna nime.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-164">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="a7fe1-165">Valige jaotises **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-165">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="a7fe1-166">![LCS-i keskkonna leht](media/inventory-visibility-environment.png "LCS-i keskkonna leht")</span><span class="sxs-lookup"><span data-stu-id="a7fe1-166">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="a7fe1-167">Valige link **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-167">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="a7fe1-168">Avaneb saadaolevate lisandmoodulite loend.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-168">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="a7fe1-169">Valige suvand **Varude nähtavus** menüüde loendist.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-169">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="a7fe1-170">Sisestage oma keskkonna järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-170">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="a7fe1-171">**AAD rakenduse (klient) ID**</span><span class="sxs-lookup"><span data-stu-id="a7fe1-171">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="a7fe1-172">**AAD Rentniku ID**</span><span class="sxs-lookup"><span data-stu-id="a7fe1-172">**AAD tenant ID**</span></span>

    <span data-ttu-id="a7fe1-173">![Lisandmooduli häälestamise leht](media/inventory-visibility-setup.png "Lisandmooduli häälestamise leht")</span><span class="sxs-lookup"><span data-stu-id="a7fe1-173">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="a7fe1-174">Nõustuge tingimuste, märkides ruudu **Tingimused**.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-174">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="a7fe1-175">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-175">Select **Install**.</span></span> <span data-ttu-id="a7fe1-176">Kuvatakse lisandmooduli olek **Installimine**.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-176">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="a7fe1-177">Kui see on tehtud, värskendage lehte, et näha muutunud olekut **Installitud**.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-177">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="a7fe1-178">Lisandmooduli desinstallimine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-178">Uninstall the add-in</span></span>

<span data-ttu-id="a7fe1-179">Lisandmooduli desinstallimiseks valige nupp **Desinstalli**.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-179">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="a7fe1-180">Kui te värskendate LCS-i, varude nähtavuse lisandmoodul eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-180">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="a7fe1-181">Desinstallimise käigus eemaldatakse lisandmoodul ja samuti käivitatakse töö, et kustutada kõik teenuses talletatud äriandmed.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-181">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="a7fe1-182">Laoseisu andmete saamine teenuses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a7fe1-182">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="a7fe1-183">Juuruta varude nähtavuse integreerimispakett</span><span class="sxs-lookup"><span data-stu-id="a7fe1-183">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="a7fe1-184">Kui käitate teenuse Supply Chain Management versiooni 10.0.17 või varasemat, võtke ühendust varude nähtavuse tugimeeskonnaga [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) paketifaili saamiseks.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-184">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="a7fe1-185">Seejärel juurutage pakett LCS-i.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-185">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="a7fe1-186">Kui juurutamisel ilmneb versiooni lahknevuse tõrge, peate käsitsi importima X++ projekti oma arenduskeskkonda.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-186">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="a7fe1-187">Seejärel looge juurutatav pakett oma arenduskeskkonnas ja juurutage see oma tootmiskeskkonnas.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-187">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="a7fe1-188">Kood sisaldub teenuse Supply Chain Management versioonis 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-188">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="a7fe1-189">Kui käitate seda või hilisemat versiooni, pole juurutamine vajalik.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-189">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="a7fe1-190">Veenduge, et järgmised funktsioonid on sisse lülitatud teenuse Supply Chain Management keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-190">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="a7fe1-191">(Vaikimisi on need sisse lülitatud.)</span><span class="sxs-lookup"><span data-stu-id="a7fe1-191">(By default, they are turned on.)</span></span>

| <span data-ttu-id="a7fe1-192">Funktsiooni kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a7fe1-192">Feature description</span></span> | <span data-ttu-id="a7fe1-193">Koodi versioon</span><span class="sxs-lookup"><span data-stu-id="a7fe1-193">Code version</span></span> | <span data-ttu-id="a7fe1-194">Ümberlülituse klass</span><span class="sxs-lookup"><span data-stu-id="a7fe1-194">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="a7fe1-195">Varude dimensioonide kasutamise lubamine või keelamine InventSum tabelis</span><span class="sxs-lookup"><span data-stu-id="a7fe1-195">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="a7fe1-196">10.0.11</span><span class="sxs-lookup"><span data-stu-id="a7fe1-196">10.0.11</span></span> | <span data-ttu-id="a7fe1-197">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="a7fe1-197">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="a7fe1-198">Varude dimensioonide kasutamise lubamine või keelamine InventSumDelta tabelis</span><span class="sxs-lookup"><span data-stu-id="a7fe1-198">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="a7fe1-199">10.0.12</span><span class="sxs-lookup"><span data-stu-id="a7fe1-199">10.0.12</span></span> | <span data-ttu-id="a7fe1-200">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="a7fe1-200">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="a7fe1-201">Inventory Visibility integratsiooni seadistamine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-201">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="a7fe1-202">Teenuses Supply Chain Management avage **[funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** tööruum ja lülitage sisse **varude nähtavuse integreerimise** funktsioon.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-202">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="a7fe1-203">Minge **Varude haldamine \> Seadistamine \> Varude nähtavuse intergratsiooni parameetrid** ja sisestage selle keskkonna URL, kus käitate Varude nähtavust.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-203">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="a7fe1-204">Leidke LCS-i keskkonna Azure'i regioon ja sisestage seejärel URL.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-204">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="a7fe1-205">URL-il on järgmine vorm:</span><span class="sxs-lookup"><span data-stu-id="a7fe1-205">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="a7fe1-206">Näiteks kui te olete Euroopas, on teie keskkonnas üks järgmistest URL-dest:</span><span class="sxs-lookup"><span data-stu-id="a7fe1-206">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="a7fe1-207">Hetkel on saadaval järgmised regioonid.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-207">The following regions are currently available.</span></span>

    | <span data-ttu-id="a7fe1-208">Azure’i regioon</span><span class="sxs-lookup"><span data-stu-id="a7fe1-208">Azure region</span></span> | <span data-ttu-id="a7fe1-209">Regiooni lühinimi</span><span class="sxs-lookup"><span data-stu-id="a7fe1-209">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="a7fe1-210">Ida-Austraalia</span><span class="sxs-lookup"><span data-stu-id="a7fe1-210">Australia east</span></span> | <span data-ttu-id="a7fe1-211">Eau</span><span class="sxs-lookup"><span data-stu-id="a7fe1-211">eau</span></span> |
    | <span data-ttu-id="a7fe1-212">Kagu-Austraalia</span><span class="sxs-lookup"><span data-stu-id="a7fe1-212">Australia southeast</span></span> | <span data-ttu-id="a7fe1-213">seau</span><span class="sxs-lookup"><span data-stu-id="a7fe1-213">seau</span></span> |
    | <span data-ttu-id="a7fe1-214">Kesk-Kanada</span><span class="sxs-lookup"><span data-stu-id="a7fe1-214">Canada central</span></span> | <span data-ttu-id="a7fe1-215">cca</span><span class="sxs-lookup"><span data-stu-id="a7fe1-215">cca</span></span> |
    | <span data-ttu-id="a7fe1-216">Ida-Kanada</span><span class="sxs-lookup"><span data-stu-id="a7fe1-216">Canada east</span></span> | <span data-ttu-id="a7fe1-217">eca</span><span class="sxs-lookup"><span data-stu-id="a7fe1-217">eca</span></span> |
    | <span data-ttu-id="a7fe1-218">Põhja-Euroopa</span><span class="sxs-lookup"><span data-stu-id="a7fe1-218">North Europe</span></span> | <span data-ttu-id="a7fe1-219">neu</span><span class="sxs-lookup"><span data-stu-id="a7fe1-219">neu</span></span> |
    | <span data-ttu-id="a7fe1-220">Lääne-Euroopa</span><span class="sxs-lookup"><span data-stu-id="a7fe1-220">West Europe</span></span> | <span data-ttu-id="a7fe1-221">weu</span><span class="sxs-lookup"><span data-stu-id="a7fe1-221">weu</span></span> |
    | <span data-ttu-id="a7fe1-222">Ida-USA</span><span class="sxs-lookup"><span data-stu-id="a7fe1-222">East US</span></span> | <span data-ttu-id="a7fe1-223">eus</span><span class="sxs-lookup"><span data-stu-id="a7fe1-223">eus</span></span> |
    | <span data-ttu-id="a7fe1-224">Lääne-USA</span><span class="sxs-lookup"><span data-stu-id="a7fe1-224">West US</span></span> | <span data-ttu-id="a7fe1-225">wus</span><span class="sxs-lookup"><span data-stu-id="a7fe1-225">wus</span></span> |

1. <span data-ttu-id="a7fe1-226">Minge **Varude halduse \> Perioodiline \> Varude nähtavuse integratsioon** ja lubage töö.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-226">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="a7fe1-227">Kõik varude muutmise sündmused teenusest Supply Chain Management sisestatakse nüüd Varude nähtavusse.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-227">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="a7fe1-228">Varude nähtavuse lisandmooduli avalik API</span><span class="sxs-lookup"><span data-stu-id="a7fe1-228">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="a7fe1-229">Varude nähtavuse lisandmooduli avalik REST API esitab integreerimiseks mitu kindlat lõpp-punkti.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-229">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="a7fe1-230">See toetab kolme peamist suhtlustüüpi.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-230">It supports three main interaction types:</span></span>

- <span data-ttu-id="a7fe1-231">Lisandmoodulisse välise süsteemi kaudu vaba kaubavaru muudatuste sisestamine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-231">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="a7fe1-232">Ajakohase vaba kaubavaru päring välisest süsteemist</span><span class="sxs-lookup"><span data-stu-id="a7fe1-232">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="a7fe1-233">Automaatne sünkroonimine teenuse Supply Chain Management kaubavarudega</span><span class="sxs-lookup"><span data-stu-id="a7fe1-233">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="a7fe1-234">Automaatne sünkroonimine ei ole avaliku API osa.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-234">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="a7fe1-235">Selle asemel käsitsetakse seda taustal keskkondades, kus varude nähtavuse lisandmoodul on lubatud.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-235">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="a7fe1-236">Autentimine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-236">Authentication</span></span>

<span data-ttu-id="a7fe1-237">Platvormi turbeluba kasutatakse laovarude nähtavuse lisandmoodulile helistamiseks.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-237">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="a7fe1-238">Seepärast peate *Azure Active Directory (Azure AD) loa* genereerima kasutades Azure AD rakendust.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-238">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="a7fe1-239">Seejärel peate kasutama Azure AD luba, et saada *pääsutõend* turvateenusest.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-239">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="a7fe1-240">Hankige turbeteenusetõend, tehes järgmist.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-240">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="a7fe1-241">Logige Azure’i portaali sisse ja kasutage seda rakenduse Supply Chain Management atribuutide `clientId` ja `clientSecret` leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-241">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="a7fe1-242">Tooge Azure Active Directory luba (`aadToken`), edastades HTTP-taotluse järgmiste atribuutidega:</span><span class="sxs-lookup"><span data-stu-id="a7fe1-242">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="a7fe1-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="a7fe1-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="a7fe1-244">**Meetod** - `GET`</span><span class="sxs-lookup"><span data-stu-id="a7fe1-244">**Method** - `GET`</span></span>
    - <span data-ttu-id="a7fe1-245">**Sisu (vormi andmed)**:</span><span class="sxs-lookup"><span data-stu-id="a7fe1-245">**Body content (form data)**:</span></span>

        | <span data-ttu-id="a7fe1-246">key</span><span class="sxs-lookup"><span data-stu-id="a7fe1-246">key</span></span> | <span data-ttu-id="a7fe1-247">väärtus</span><span class="sxs-lookup"><span data-stu-id="a7fe1-247">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="a7fe1-248">client_id</span><span class="sxs-lookup"><span data-stu-id="a7fe1-248">client_id</span></span> | <span data-ttu-id="a7fe1-249">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="a7fe1-249">${aadAppId}</span></span> |
        | <span data-ttu-id="a7fe1-250">client_secret</span><span class="sxs-lookup"><span data-stu-id="a7fe1-250">client_secret</span></span> | <span data-ttu-id="a7fe1-251">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="a7fe1-251">${aadAppSecret}</span></span> |
        | <span data-ttu-id="a7fe1-252">grant_type</span><span class="sxs-lookup"><span data-stu-id="a7fe1-252">grant_type</span></span> | <span data-ttu-id="a7fe1-253">client_credentials</span><span class="sxs-lookup"><span data-stu-id="a7fe1-253">client_credentials</span></span> |
        | <span data-ttu-id="a7fe1-254">resource</span><span class="sxs-lookup"><span data-stu-id="a7fe1-254">resource</span></span> | <span data-ttu-id="a7fe1-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="a7fe1-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="a7fe1-256">Peaksite saama vastuseks atribuudi `aadToken`, mis sarnaneb järgmise näitega.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-256">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="a7fe1-257">Vormindage JSON-i taotlus, mis sarnaneb järgmisele:</span><span class="sxs-lookup"><span data-stu-id="a7fe1-257">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="a7fe1-258">Kus</span><span class="sxs-lookup"><span data-stu-id="a7fe1-258">Where:</span></span>
    - <span data-ttu-id="a7fe1-259">Väärtus `client_assertion` peab olema `aadToken`, mille eelmises sammus saite.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-259">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="a7fe1-260">Väärtus `context` peab olema keskkonna ID, kus soovite lisandmooduli juurutada.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-260">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="a7fe1-261">Häälestage kõik muud väärtused, nagu näites näidatud.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-261">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="a7fe1-262">Edastage HTTP-taotlus järgmiste atribuutidega:</span><span class="sxs-lookup"><span data-stu-id="a7fe1-262">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="a7fe1-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="a7fe1-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="a7fe1-264">**Meetod** - `POST`</span><span class="sxs-lookup"><span data-stu-id="a7fe1-264">**Method** - `POST`</span></span>
    - <span data-ttu-id="a7fe1-265">**HTTP päis** – lisage API versioon (võti on `Api-Version` ja väärtus on`1.0`)</span><span class="sxs-lookup"><span data-stu-id="a7fe1-265">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="a7fe1-266">**Sisu** – lisage eelmises sammus loodud JSON-i taotlus.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-266">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="a7fe1-267">Saate vastuseks tõendi `access_token`.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-267">You will get an `access_token` in response.</span></span> <span data-ttu-id="a7fe1-268">Seda on teil vaja juurepääsuloaks, et kutsuda nähtavuse API.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-268">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="a7fe1-269">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-269">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="a7fe1-270">Varude nähtavuse API konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-270">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="a7fe1-271">Enne teenuse kasutamist peate tegema järgmistes jaotistes kirjeldatud konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-271">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="a7fe1-272">Konfiguratsioon võib teie keskkonna üksikasjade põhjal erineda.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-272">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="a7fe1-273">See hõlmab peamiselt nelja osa.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-273">It primarily includes four parts:</span></span>

- [<span data-ttu-id="a7fe1-274">Eraldamine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-274">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="a7fe1-275">Dimensioonide konfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="a7fe1-275">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="a7fe1-276">Indekseerimine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-276">Indexing</span></span>](#indexing)
- [<span data-ttu-id="a7fe1-277">Kohandatud mõõtmine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-277">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="a7fe1-278">Sektsioonimine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-278">Partitioning</span></span>

<span data-ttu-id="a7fe1-279">Sektsioonimine võib oluliselt mõjutada varude nähtavuse API jõudlust.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-279">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="a7fe1-280">Mõistlik on määratleda skeem, mis võimaldab väikseid andmegruppe, aga samas ka sisukaid andmepäringuid.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-280">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="a7fe1-281">`organizationId` (Supply Chain Managementis `dataAreaId`) on alati osa sektsioonimisest ja varude nähtavuse vaikeväärtuseks on määratud sektsioonid, mille dimensioonid on *Sait +asukoht*.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-281">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="a7fe1-282">See tähendab, et teenusepäringu esitamiseks peab need dimensioonid alati filtreerima.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-282">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="a7fe1-283">*Sait* ja *asukoht* on varude nähtavuses kaks üldist vaikedimensiooni.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-283">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="a7fe1-284">Supply Chain Managementis nimetatakse neid dimensioone *saidiks* (`InventSiteId`) ja *laoks* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="a7fe1-284">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="a7fe1-285">Dimensioonide konfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="a7fe1-285">Dimension configurations</span></span>

<span data-ttu-id="a7fe1-286">Varude nähtavus annab loendi üldistest dimensioonidest, et lubada mitme allika süsteemi integreerimist.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-286">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="a7fe1-287">Järgmises tabelis loetletakse varude dimensioonid, mis on varude nähtavuse dimensioonide nimed.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-287">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="a7fe1-288">Dimensiooni tüüp</span><span class="sxs-lookup"><span data-stu-id="a7fe1-288">Dimension type</span></span> | <span data-ttu-id="a7fe1-289">Dimensiooni nimi</span><span class="sxs-lookup"><span data-stu-id="a7fe1-289">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="a7fe1-290">Toode</span><span class="sxs-lookup"><span data-stu-id="a7fe1-290">Product</span></span> | `ColorId` |
| <span data-ttu-id="a7fe1-291">Toode</span><span class="sxs-lookup"><span data-stu-id="a7fe1-291">Product</span></span> | `SizeId` |
| <span data-ttu-id="a7fe1-292">Toode</span><span class="sxs-lookup"><span data-stu-id="a7fe1-292">Product</span></span> | `StyleId` |
| <span data-ttu-id="a7fe1-293">Toode</span><span class="sxs-lookup"><span data-stu-id="a7fe1-293">Product</span></span> | `ConfigId` |
| <span data-ttu-id="a7fe1-294">Jälitamine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-294">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="a7fe1-295">Jälitamine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-295">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="a7fe1-296">Koht</span><span class="sxs-lookup"><span data-stu-id="a7fe1-296">Location</span></span> | `LocationId` |
| <span data-ttu-id="a7fe1-297">Koht</span><span class="sxs-lookup"><span data-stu-id="a7fe1-297">Location</span></span> | `SiteId` |
| <span data-ttu-id="a7fe1-298">Varude olek</span><span class="sxs-lookup"><span data-stu-id="a7fe1-298">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="a7fe1-299">Laopõhine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-299">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="a7fe1-300">Laopõhine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-300">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="a7fe1-301">Laopõhine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-301">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="a7fe1-302">Eelmises tabelis loetletud dimensiooni tüüp on ainult teave.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-302">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="a7fe1-303">Varude nähtavuses ei ole vaja määratleda dimensiooni tüüpi.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-303">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="a7fe1-304">Kui on olemas kohandatud dimensioon ja see peab muutuma vaikeväärtuseks, kui varude nähtavus seda kasutab, saate **kohandatud dimensiooni** nime varude nähtavuses konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-304">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="a7fe1-305">Väliste süsteemide juurdepääs varude nähtavusele läbi RESTfuli API-de, mis võimaldavad esitada teavet antud dimensioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-305">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="a7fe1-306">Integratsiooni jaoks võimaldab varude nähtavus teil konfigureerida *väliskanali andmeallika* ja lähtedimensiooni vastavalt *sihtdimensioonile* varude nähtavuse korral.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-306">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="a7fe1-307">Sihtdimensioonid peavad hõlmama ühte järgmistest.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-307">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="a7fe1-308">Varude nähtavuse vaikedimensioonid</span><span class="sxs-lookup"><span data-stu-id="a7fe1-308">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="a7fe1-309">Kohandatud dimensioonid</span><span class="sxs-lookup"><span data-stu-id="a7fe1-309">Custom dimensions</span></span>

<span data-ttu-id="a7fe1-310">Dimensioonide konfigureerimise eesmärk on ühtlustada mitme süsteemi integreerimist vastavalt päringule dimensioonide ja sisestamise sündmuse dimensioonidega.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-310">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="a7fe1-311">Indekseerimine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-311">Indexing</span></span>

<span data-ttu-id="a7fe1-312">Enamiku ajast ei ole vaba kaubavaru päring mitte ainult kõrgeimal „kogutasemel“, kuid soovi korral saate vaadata varude dimensioonide alusel summeeritud tulemusi.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-312">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="a7fe1-313">Varude nähtavus annab paindlikkuse, lubades teil häälestada indekseid, mis põhinevad dimensioonil või dimensioonide kombinatsioonil.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-313">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="a7fe1-314">Praegu saate indekseid konfigureerida ainult kuni viieni.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-314">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="a7fe1-315">Peate hoolikalt kaaluma, millist dimensiooni või dimensioonide kombinatsiooni kasutate enne rakendamist, et tagada selle vastavus teie ettevõtte vajadustele.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-315">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="a7fe1-316">Näiteks kui soovite teha päringuid toodete kohta järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-316">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="a7fe1-317">Päring saadaval oleva summeeritud toote kohta *värvi* ja *suuruse* dimensioonide kaupa.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-317">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="a7fe1-318">Mõnel juhul soovite ainult toote kohta päringut esitada.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-318">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="a7fe1-319">Teil oleks kaks indeksit, mis on määratletud järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-319">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="a7fe1-320">Tühi sulg summeeritakse sektsioonis toote ID põhjal.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-320">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="a7fe1-321">Indekseerimine määratleb, kuidas saate oma tulemusi grupeerida päringusätte `groupBy` alusel.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-321">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="a7fe1-322">Sel juhul, kui te ei määratle ühtegi sätte `groupBy` väärtust, saate kogusummad `productid` kaupa.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-322">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="a7fe1-323">Vastasel juhul, kui määrate `groupBy` väärtuseks `groupBy=ColorId&groupBy=SizeId`, saadetakse teile mitu rida, mis põhinevad süsteemi erinevate värvide ja suuruse kombinatsioonidel.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-323">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="a7fe1-324">Saate esitada päringu kriteeriumid päringu sisus.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-324">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="a7fe1-325">Siin on näide päringust toote värvi ja suuruse kombinatsiooniga.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-325">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="a7fe1-326">Kohandatud mõõtmine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-326">Custom measurement</span></span>

<span data-ttu-id="a7fe1-327">Vaikimisi antud mõõdukogused on seotud teenusega Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-327">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="a7fe1-328">Soovi korral võite siiski saada koguse, mis on valmistatud vaikemõõtude kombinatsioonis.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-328">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="a7fe1-329">Selleks võib olla kohandatud koguste konfiguratsioon, mis lisatakse vabade päringute väljundile.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-329">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="a7fe1-330">Funktsioon võimaldab teil kohandatud mõõtmiseks määratleda lisatavate mõõtude kogumi ja/või meetmete kogumi, mis on kohandatud mõõtmisest lahutatud.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-330">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="a7fe1-331">Näiteks järgmise päringu tingimusega konfigureerite kohandatud mõõtmise koguse üksusena `MyCustomAvailableforReservation`, mida tarbib tarbimise süsteem.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-331">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="a7fe1-332">Tarbimise süsteem</span><span class="sxs-lookup"><span data-stu-id="a7fe1-332">Consumption system</span></span> | <span data-ttu-id="a7fe1-333">Arvutatud mõõdikud</span><span class="sxs-lookup"><span data-stu-id="a7fe1-333">Calculated measurers</span></span> | <span data-ttu-id="a7fe1-334">Andmeallikas</span><span class="sxs-lookup"><span data-stu-id="a7fe1-334">Data source</span></span> | <span data-ttu-id="a7fe1-335">Muutuja</span><span class="sxs-lookup"><span data-stu-id="a7fe1-335">Modifier</span></span> | <span data-ttu-id="a7fe1-336">Muutuja arvutustüüp</span><span class="sxs-lookup"><span data-stu-id="a7fe1-336">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="a7fe1-337">Lisa</span><span class="sxs-lookup"><span data-stu-id="a7fe1-337">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="a7fe1-338">Lisa</span><span class="sxs-lookup"><span data-stu-id="a7fe1-338">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="a7fe1-339">Lahutamine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-339">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="a7fe1-340">Lisa</span><span class="sxs-lookup"><span data-stu-id="a7fe1-340">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="a7fe1-341">Lahutamine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-341">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="a7fe1-342">Lisa</span><span class="sxs-lookup"><span data-stu-id="a7fe1-342">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="a7fe1-343">Lisa</span><span class="sxs-lookup"><span data-stu-id="a7fe1-343">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="a7fe1-344">Lahutamine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-344">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="a7fe1-345">Lahutamine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-345">Subtraction</span></span> |

<span data-ttu-id="a7fe1-346">Sellega tagastatakse kohandatud mõõtmise koguse päring järgmise väljundina.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-346">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="a7fe1-347">Üksuse `MyCustomAvailableforReservation` väljundi aluseks on kohandatud mõõtmiste arvutamise säte.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-347">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="a7fe1-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="a7fe1-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="a7fe1-349">Vaba kaubavaru muudatuste sisestamine</span><span class="sxs-lookup"><span data-stu-id="a7fe1-349">Posting on-hand changes</span></span>

<span data-ttu-id="a7fe1-350">Sündmuse sisestamise täpne URL sõltub geograafilisest piirkonnast.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-350">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="a7fe1-351">See on järgmises vormis.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-351">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="a7fe1-352">Kui see on autenditud, saab seda URL-i kasutada koos HTTP `POST`-meetodiga, et saata teenusele vaba kaubavaru muudatuste sündmusi.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-352">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="a7fe1-353">Dynamics 365 teenustega suhtlemiseks HTTP-taotluste kaudu kasutatakse spetsiaalset päist, mis tähistab Supply Chain Managementi eksemplari keskkonna ID-d, millega andmed on lingitud.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-353">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="a7fe1-354">Näide:</span><span class="sxs-lookup"><span data-stu-id="a7fe1-354">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="a7fe1-355">Vaba kaubavaru muudatuste päringu sisestamise näide 1</span><span class="sxs-lookup"><span data-stu-id="a7fe1-355">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="a7fe1-356">See näide näitab olukorda, kus häälestate dimensiooni konfiguratsiooni Power Appsis.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-356">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="a7fe1-357">Kasutage järgmist päringut dimensioonide vastenduste konfigureerimiseks Power Appsis.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-357">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="a7fe1-358">Nüüd saate päringus määrata väärtuse `dimensionDataSource` ja kasutada kohandatud dimensioone.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-358">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="a7fe1-359">Süsteem teisendab kohandatud dimensioonid automaatselt põhidimensioonideks.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-359">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="a7fe1-360">Vaba kaubavaru muudatuste päringu sisestamise näide 2</span><span class="sxs-lookup"><span data-stu-id="a7fe1-360">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="a7fe1-361">Selles näites kuvatakse stsenaarium, kus dimensioonide konfigureerimise jaoks pole vastendusi Power Appsis vastendusi häälestatud, nii et sisestamisel tuleks samuti põhidimensioone kasutada.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-361">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="a7fe1-362">Kõik dimensioonid peavad olema põhidimensioonid, kui väli `dimensionDataSource` on väärtusega null, tühi või seal on tühik.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-362">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="a7fe1-363">JSON-dokumendi väljade atribuudid</span><span class="sxs-lookup"><span data-stu-id="a7fe1-363">JSON document field properties</span></span>

<span data-ttu-id="a7fe1-364">Eespool antud JSON-päringu näidete väljadel on järgmises tabelis loetletud atribuudid.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-364">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="a7fe1-365">Välja kood</span><span class="sxs-lookup"><span data-stu-id="a7fe1-365">Field ID</span></span> | <span data-ttu-id="a7fe1-366">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a7fe1-366">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="a7fe1-367">Konkreetse muudatuse sündmuse kordumatu ID.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-367">A unique ID for the specific change event.</span></span> <span data-ttu-id="a7fe1-368">Seda ID-d kasutatakse tagamaks, et kui suhtlus teenusega nurjub sisestamise ajal, ei põhjustaks sündmuse taasesitamine süsteemis sama sündmuse topeltloendamist.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-368">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="a7fe1-369">Sündmusega lingitud organisatsiooni identifikaator.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-369">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="a7fe1-370">See vastendab Supply Chain Managementi organisatsioonide või andmepiirkonna ID-sid.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-370">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="a7fe1-371">Kõnealuse toote identifikaator.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-371">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="a7fe1-372">Kogus, mille võrra laoseisu tuleb muuta.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-372">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="a7fe1-373">Kui riiulile lisati näiteks kümme uut saiakest, oleks see väärtus 10.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-373">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="a7fe1-374">Kui riiulilt eemaldati või müüdi kolm saiakest, oleks see väärtus -3.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-374">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="a7fe1-375">See on sisestatud muudatuse sündmuses ja päringus kasutatud andmeallikas.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-375">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="a7fe1-376">Andmeallika määramisel saate kasutada määratud andmeallika kohandatud dimensioone.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-376">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="a7fe1-377">Dimensiooni konfigureerimisega saab varude nähtavus vastendada kohandatud dimensioonid üldiste vaikedimensioonidega.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-377">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="a7fe1-378">Kui väärtust `dimensionDataSource` pole määratud, saate päringutes kasutada ainult üldisi vaikedimensioone.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-378">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="a7fe1-379">Dünaamiline võtme-/väärtusepaari mapp.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-379">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="a7fe1-380">Need vastendavad mõned dimensioonid Supply Chain Managementis, kuid võite lisada ka kohandatud dimensioone (nt *Allikas*), mis võib tähistada sündmuse pärinemist Supply Chain Managementist või välisest süsteemist.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-380">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="a7fe1-381">Praeguse vaba kaubavaru päring</span><span class="sxs-lookup"><span data-stu-id="a7fe1-381">Querying current on-hand</span></span>

<span data-ttu-id="a7fe1-382">Praeguse laoseisu päringute puhul on lõpp-punktil sarnane URL.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-382">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="a7fe1-383">See on päringus meetodiga HTTP `POST`.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-383">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="a7fe1-384">Praeguse vaba kaubavaru päringu näide 1</span><span class="sxs-lookup"><span data-stu-id="a7fe1-384">Current on-hand query example 1</span></span>

<span data-ttu-id="a7fe1-385">See näide näitab olukorda, kus olete Power Appsis dimensioonide konfigureerimise juba lõpule viinud.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-385">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="a7fe1-386">Kasutage järgmist päringut dimensioonide vastenduste konfigureerimiseks Power Appsis.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-386">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="a7fe1-387">Nüüd saate päringus määrata väärtuse `dimensionDataSource` ja kasutada kohandatud dimensioone.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-387">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="a7fe1-388">Süsteem teisendab kohandatud dimensioonid automaatselt põhidimensioonideks.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-388">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="a7fe1-389">Saate määrata väärtuse `DimensionDataSource` üksusel `filters` ja määrata kohandatud dimensioonid nii üksuse `filters` kui ka `groupByValues` jaoks.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-389">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="a7fe1-390">Süsteem teisendab kohandatud dimensioonid automaatselt põhidimensioonideks.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-390">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="a7fe1-391">Praeguse vaba kaubavaru päringu näide 2</span><span class="sxs-lookup"><span data-stu-id="a7fe1-391">Current on-hand query example 2</span></span>

<span data-ttu-id="a7fe1-392">Selles näites kuvatakse stsenaarium, kus dimensioonide konfigureerimise jaoks pole vastendusi Power Appsis vastendusi häälestatud, nii et sisestamisel tuleks samuti põhidimensioone kasutada.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-392">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="a7fe1-393">Kõik dimensioonid peavad olema põhidimensioonid, kui väli `dimensionDataSource` jaotises `filters` on väärtusega null, tühi või seal on tühik.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-393">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="a7fe1-394">Näide tagastatud tulemusest</span><span class="sxs-lookup"><span data-stu-id="a7fe1-394">Example return result</span></span>

<span data-ttu-id="a7fe1-395">Eelmistes näidetes kuvatud päringud võivad tagastada sellise tulemuse.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-395">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="a7fe1-396">Võtke arvesse, et koguseväljad on struktuurilt justkui meetmete ja nendega seotud väärtuste sõnastikud.</span><span class="sxs-lookup"><span data-stu-id="a7fe1-396">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
