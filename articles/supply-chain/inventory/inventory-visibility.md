---
title: Varude nähtavuse lisandmoodul
description: See teema kirjeldab varude nähtavuse lisandmooduli installimist ja konfigureerimist Dynamics 365 Supply Chain Managementi jaoks.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d09c7be5de75511b10d7a69d4b8ac12917b0dbe8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910421"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="e1806-103">Varude nähtavuse lisandmoodul</span><span class="sxs-lookup"><span data-stu-id="e1806-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="e1806-104">Varude nähtavuse lisandmoodul on sõltumatu ja väga muutuv mikroteenus, mis võimaldab reaalajas vaba kaubavaru jälgimist, andes seega ülevaate varude nähtavuse kohta.</span><span class="sxs-lookup"><span data-stu-id="e1806-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="e1806-105">Kogu vaba kaubavaruga seotud teave eksporditakse teenusesse peaaegu reaalajas madalama taseme SQL-i integratsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="e1806-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="e1806-106">Välised süsteemid pääsevad teenusele juurde avatud API-de kaudu, et teha päringuid antud dimensioonide kogumi kohta, seega hankides saadaolevate vabade ametikohtade loendi.</span><span class="sxs-lookup"><span data-stu-id="e1806-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="e1806-107">Varude nähtavus on teenusel Microsoft Dataverse rajanev mikroteenus, mis tähendab, et saate seda laiendada, luues rakendusi Power Apps ja rakendades Power BI, et võimaldada ärivajaduste täitmiseks kohandatud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="e1806-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="e1806-108">Samuti on võimalik uuendada indeksit laopäringute tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="e1806-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="e1806-109">Varude nähtavus pakub konfigureerimisvõimalusi, mis võimaldavad seda integreerida mitme kolmanda osapoole süsteemidega.</span><span class="sxs-lookup"><span data-stu-id="e1806-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="e1806-110">See toetab standardset varude dimensiooni, kohandatud laiendatavust ning standardiseeritud konfigureeritavaid ja arvutatavaid koguseid.</span><span class="sxs-lookup"><span data-stu-id="e1806-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="e1806-111">Selles teemas kirjeldatakse, kuidas installida ja konfigureerida varude nähtavuse lisandmoodul Dynamics 365 Supply Chain Managementi jaoks ja kuidas kasutada rakenduse programmeerimise liidest (API).</span><span class="sxs-lookup"><span data-stu-id="e1806-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="e1806-112">Varude nähtavuse lisandmooduli installimine</span><span class="sxs-lookup"><span data-stu-id="e1806-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="e1806-113">Varude nähtavuse lisandmooduli saate installida, kasutades teenust Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e1806-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e1806-114">LCS on koostööportaal, mis pakub keskkonda ja regulaarselt värskendatud teenuseid, mis aitavad hallata Dynamics 365 Finance and Operationsi rakenduste töötsüklit.</span><span class="sxs-lookup"><span data-stu-id="e1806-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="e1806-115">Lisateabe saamiseks vt [Lifecycle Servicesi ressursid](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="e1806-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e1806-116">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="e1806-116">Prerequisites</span></span>

<span data-ttu-id="e1806-117">Enne varude nähtavuse lisandmooduli installimist peate tegema järgmist.</span><span class="sxs-lookup"><span data-stu-id="e1806-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="e1806-118">Hankige LCS-i juurutamise projekt, millel on vähemalt üks juurutatud keskkond.</span><span class="sxs-lookup"><span data-stu-id="e1806-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="e1806-119">Kontrollige, et eeltingimused lisandmoodulite seadistamiseks, mis on antud [Lisandmoodulite ülevaates](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) on täidetud.</span><span class="sxs-lookup"><span data-stu-id="e1806-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="e1806-120">Varude nähtavus ei nõua topeltkirjutuse linkimist.</span><span class="sxs-lookup"><span data-stu-id="e1806-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="e1806-121">Võtke ühendust varude nähtavuse töörühmaga [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) nende kolme nõutava faili saamiseks:</span><span class="sxs-lookup"><span data-stu-id="e1806-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="e1806-122">`Inventory Visibility Integration.zip` (Kui Supply Chain Management versioon, mida käitate, on varasem kui versioon 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="e1806-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="e1806-123">Järgige juhiseid, mis on toodud teemas [Kiirstart: registreerige rakendus Microsofti identiteediplatvormil](/azure/active-directory/develop/quickstart-register-app), et registreerida rakendus ja lisada Azure'i tellimuse all AAD-le kliendi saladus.</span><span class="sxs-lookup"><span data-stu-id="e1806-123">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
    - [<span data-ttu-id="e1806-124">Rakenduse registreerimine</span><span class="sxs-lookup"><span data-stu-id="e1806-124">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
    - [<span data-ttu-id="e1806-125">Kliendi saladuse lisamine</span><span class="sxs-lookup"><span data-stu-id="e1806-125">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
    - <span data-ttu-id="e1806-126">Väljasid **Rakenduse(kliendi) ID**, **Kliendi saladus** ja **Rentniku ID** kasutatakse järgmistes juhistes.</span><span class="sxs-lookup"><span data-stu-id="e1806-126">The **Application(Client) Id**, **Client Secret** and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="e1806-127">Praegu toetatud riikide ja regioonide hulka kuuluvad Kanada, USA ja Euroopa Liit (EL).</span><span class="sxs-lookup"><span data-stu-id="e1806-127">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="e1806-128">Kui teil on küsimusi nende eeltingimuste kohta, võtke ühendust varude nähtavuse tootemeeskonnaga.</span><span class="sxs-lookup"><span data-stu-id="e1806-128">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="e1806-129">Seadistamine Dataverse</span><span class="sxs-lookup"><span data-stu-id="e1806-129">Set up Dataverse</span></span>

<span data-ttu-id="e1806-130">Läbige need etapid, et seadistada Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e1806-130">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="e1806-131">Lisage teenuse põhimõtted oma rentnikule:</span><span class="sxs-lookup"><span data-stu-id="e1806-131">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="e1806-132">Installige Azure AD PowerShell Module v2, nagu on kirjeldatud [Instalige Azure Active Directory PowerShell Graph'ile](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="e1806-132">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="e1806-133">Käivitage järgmine PowerShell käsk.</span><span class="sxs-lookup"><span data-stu-id="e1806-133">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="e1806-134">Looge rakenduse kasutaja varude nähtavuse jaoks platvormil Dataverse:</span><span class="sxs-lookup"><span data-stu-id="e1806-134">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="e1806-135">Avage oma Dataverse keskkonna URL.</span><span class="sxs-lookup"><span data-stu-id="e1806-135">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="e1806-136">Minge **Lisaseaded \> Süsteem \> Turvalisus \> Kasutajad** ja looge rakenduse kasutaja.</span><span class="sxs-lookup"><span data-stu-id="e1806-136">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="e1806-137">Kasutage Vaade menüüd, et muuta lehe vaade **Rakenduse kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="e1806-137">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="e1806-138">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e1806-138">Select **New**.</span></span> <span data-ttu-id="e1806-139">Määrake välja Rakenduse ID väärtuseks *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="e1806-139">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="e1806-140">(Objekti ID laaditakse muudatuste salvestamisel automaatselt.) Nime saate kohandada.</span><span class="sxs-lookup"><span data-stu-id="e1806-140">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="e1806-141">Näiteks saate muuta selle *Varude nähtavus*.</span><span class="sxs-lookup"><span data-stu-id="e1806-141">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="e1806-142">Kui olete lõpetanud, valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e1806-142">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="e1806-143">Valige **Määra roll** ja seejärel valige **Süsteemiadministraator**.</span><span class="sxs-lookup"><span data-stu-id="e1806-143">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="e1806-144">Kui rolli nimi on **Common Data Service Kasutaja**, valige ka see.</span><span class="sxs-lookup"><span data-stu-id="e1806-144">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="e1806-145">Lisateavet leiate teemast [Rakenduse kasutaja loomine](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="e1806-145">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="e1806-146">Kui teie Dataverse vaikekeel ei ole **inglise keel**:</span><span class="sxs-lookup"><span data-stu-id="e1806-146">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="e1806-147">Avage **Täpsemad seadistused \>Administreerimine \> Keeled**,</span><span class="sxs-lookup"><span data-stu-id="e1806-147">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="e1806-148">Valige **Inglise keel (LanguageCode=1033)** ja valige **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="e1806-148">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="e1806-149">Importige `Inventory Visibility Dataverse Solution.zip` fail, mis sisaldab Dataverse konfiguratsiooniga seotud üksusi ja tööriista Power Apps:</span><span class="sxs-lookup"><span data-stu-id="e1806-149">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="e1806-150">Minge **Lahendused** lehele.</span><span class="sxs-lookup"><span data-stu-id="e1806-150">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="e1806-151">Valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="e1806-151">Select **Import**.</span></span>

1. <span data-ttu-id="e1806-152">Importige konfiguratsioonitäienduse käivitusvoog:</span><span class="sxs-lookup"><span data-stu-id="e1806-152">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="e1806-153">Minge Microsoft Flow lehele.</span><span class="sxs-lookup"><span data-stu-id="e1806-153">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="e1806-154">Veenduge, et ühendus nimega *Dataverse (pärand)* on olemas.</span><span class="sxs-lookup"><span data-stu-id="e1806-154">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="e1806-155">(Kui seda pole olemas, looge see.)</span><span class="sxs-lookup"><span data-stu-id="e1806-155">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="e1806-156">Importige `Inventory Visibility Configuration Trigger.zip` fail.</span><span class="sxs-lookup"><span data-stu-id="e1806-156">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="e1806-157">Pärast importimist kuvatakse päästik jaotises **Minu vood**.</span><span class="sxs-lookup"><span data-stu-id="e1806-157">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="e1806-158">Keskkonna teabe põhjal käivitage järgmised neli muutujat:</span><span class="sxs-lookup"><span data-stu-id="e1806-158">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="e1806-159">Azure'i rentniku ID</span><span class="sxs-lookup"><span data-stu-id="e1806-159">Azure Tenant ID</span></span>
        - <span data-ttu-id="e1806-160">Azure Rakenduse (klient) ID</span><span class="sxs-lookup"><span data-stu-id="e1806-160">Azure Application Client ID</span></span>
        - <span data-ttu-id="e1806-161">Azure Rakenduse (klient) Secret</span><span class="sxs-lookup"><span data-stu-id="e1806-161">Azure Application Client Secret</span></span>
        - <span data-ttu-id="e1806-162">Varude nähtavus lõpp-punkt</span><span class="sxs-lookup"><span data-stu-id="e1806-162">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="e1806-163">Lisateavet selle muutuja kohta vaadake [Seadistage Varude nähtavuse integreerimine](#setup-inventory-visibility-integration) osas selles teemas edaspidi.</span><span class="sxs-lookup"><span data-stu-id="e1806-163">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="e1806-164">![Konfiguratsiooni päästik](media/configuration-trigger.png "Konfiguratsiooni päästik")</span><span class="sxs-lookup"><span data-stu-id="e1806-164">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="e1806-165">Valige **lülita sisse**.</span><span class="sxs-lookup"><span data-stu-id="e1806-165">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="e1806-166">Lisandmooduli installimine</span><span class="sxs-lookup"><span data-stu-id="e1806-166">Install the add-in</span></span>

<span data-ttu-id="e1806-167">Varude nähtavuse lisandmooduli installimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e1806-167">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="e1806-168">Logige sisse [teenuse Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portaali.</span><span class="sxs-lookup"><span data-stu-id="e1806-168">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="e1806-169">Avalehel valige projekt, kus teie keskkond juurutati.</span><span class="sxs-lookup"><span data-stu-id="e1806-169">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="e1806-170">Projekti lehel valige keskkond, kuhu soovite lisandmooduli installida.</span><span class="sxs-lookup"><span data-stu-id="e1806-170">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="e1806-171">Keskkonna leheküljel kerige alla, kuni näete **Keskkonna lisandmoodulid** jaotist **Power Platform integratsiooni** jaotises, kust leiate Dataverse keskkonna nime.</span><span class="sxs-lookup"><span data-stu-id="e1806-171">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="e1806-172">Valige jaotises **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="e1806-172">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="e1806-173">![LCS-i keskkonna leht](media/inventory-visibility-environment.png "LCS-i keskkonna leht")</span><span class="sxs-lookup"><span data-stu-id="e1806-173">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="e1806-174">Valige link **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="e1806-174">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="e1806-175">Avaneb saadaolevate lisandmoodulite loend.</span><span class="sxs-lookup"><span data-stu-id="e1806-175">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="e1806-176">Valige suvand **Varude nähtavus** menüüde loendist.</span><span class="sxs-lookup"><span data-stu-id="e1806-176">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="e1806-177">Sisestage oma keskkonna järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="e1806-177">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="e1806-178">**AAD rakenduse (klient) ID**</span><span class="sxs-lookup"><span data-stu-id="e1806-178">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="e1806-179">**AAD Rentniku ID**</span><span class="sxs-lookup"><span data-stu-id="e1806-179">**AAD tenant ID**</span></span>

    <span data-ttu-id="e1806-180">![Lisandmooduli häälestamise leht](media/inventory-visibility-setup.png "Lisandmooduli häälestamise leht")</span><span class="sxs-lookup"><span data-stu-id="e1806-180">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="e1806-181">Nõustuge tingimuste, märkides ruudu **Tingimused**.</span><span class="sxs-lookup"><span data-stu-id="e1806-181">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="e1806-182">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="e1806-182">Select **Install**.</span></span> <span data-ttu-id="e1806-183">Kuvatakse lisandmooduli olek **Installimine**.</span><span class="sxs-lookup"><span data-stu-id="e1806-183">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="e1806-184">Kui see on tehtud, värskendage lehte, et näha muutunud olekut **Installitud**.</span><span class="sxs-lookup"><span data-stu-id="e1806-184">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="e1806-185">Lisandmooduli desinstallimine</span><span class="sxs-lookup"><span data-stu-id="e1806-185">Uninstall the add-in</span></span>

<span data-ttu-id="e1806-186">Lisandmooduli desinstallimiseks valige nupp **Desinstalli**.</span><span class="sxs-lookup"><span data-stu-id="e1806-186">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="e1806-187">Kui te värskendate LCS-i, varude nähtavuse lisandmoodul eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="e1806-187">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="e1806-188">Desinstallimise käigus eemaldatakse lisandmoodul ja samuti käivitatakse töö, et kustutada kõik teenuses talletatud äriandmed.</span><span class="sxs-lookup"><span data-stu-id="e1806-188">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="e1806-189">Laoseisu andmete saamine teenuses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e1806-189">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="e1806-190">Juuruta varude nähtavuse integreerimispakett</span><span class="sxs-lookup"><span data-stu-id="e1806-190">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="e1806-191">Kui käitate teenuse Supply Chain Management versiooni 10.0.17 või varasemat, võtke ühendust varude nähtavuse tugimeeskonnaga [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) paketifaili saamiseks.</span><span class="sxs-lookup"><span data-stu-id="e1806-191">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="e1806-192">Seejärel juurutage pakett LCS-i.</span><span class="sxs-lookup"><span data-stu-id="e1806-192">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="e1806-193">Kui juurutamisel ilmneb versiooni lahknevuse tõrge, peate käsitsi importima X++ projekti oma arenduskeskkonda.</span><span class="sxs-lookup"><span data-stu-id="e1806-193">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="e1806-194">Seejärel looge juurutatav pakett oma arenduskeskkonnas ja juurutage see oma tootmiskeskkonnas.</span><span class="sxs-lookup"><span data-stu-id="e1806-194">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="e1806-195">Kood sisaldub teenuse Supply Chain Management versioonis 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="e1806-195">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="e1806-196">Kui käitate seda või hilisemat versiooni, pole juurutamine vajalik.</span><span class="sxs-lookup"><span data-stu-id="e1806-196">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="e1806-197">Veenduge, et järgmised funktsioonid on sisse lülitatud teenuse Supply Chain Management keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="e1806-197">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="e1806-198">(Vaikimisi on need sisse lülitatud.)</span><span class="sxs-lookup"><span data-stu-id="e1806-198">(By default, they are turned on.)</span></span>

| <span data-ttu-id="e1806-199">Funktsiooni kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e1806-199">Feature description</span></span> | <span data-ttu-id="e1806-200">Koodi versioon</span><span class="sxs-lookup"><span data-stu-id="e1806-200">Code version</span></span> | <span data-ttu-id="e1806-201">Ümberlülituse klass</span><span class="sxs-lookup"><span data-stu-id="e1806-201">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="e1806-202">Varude dimensioonide kasutamise lubamine või keelamine InventSum tabelis</span><span class="sxs-lookup"><span data-stu-id="e1806-202">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="e1806-203">10.0.11</span><span class="sxs-lookup"><span data-stu-id="e1806-203">10.0.11</span></span> | <span data-ttu-id="e1806-204">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="e1806-204">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="e1806-205">Varude dimensioonide kasutamise lubamine või keelamine InventSumDelta tabelis</span><span class="sxs-lookup"><span data-stu-id="e1806-205">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="e1806-206">10.0.12</span><span class="sxs-lookup"><span data-stu-id="e1806-206">10.0.12</span></span> | <span data-ttu-id="e1806-207">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="e1806-207">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="e1806-208">Inventory Visibility integratsiooni seadistamine</span><span class="sxs-lookup"><span data-stu-id="e1806-208">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="e1806-209">Teenuses Supply Chain Management avage **[funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** tööruum ja lülitage sisse **varude nähtavuse integreerimise** funktsioon.</span><span class="sxs-lookup"><span data-stu-id="e1806-209">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="e1806-210">Minge **Varude haldamine \> Seadistamine \> Varude nähtavuse intergratsiooni parameetrid** ja sisestage selle keskkonna URL, kus käitate Varude nähtavust.</span><span class="sxs-lookup"><span data-stu-id="e1806-210">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="e1806-211">Leidke LCS-i keskkonna Azure'i regioon ja sisestage seejärel URL.</span><span class="sxs-lookup"><span data-stu-id="e1806-211">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="e1806-212">URL-il on järgmine vorm:</span><span class="sxs-lookup"><span data-stu-id="e1806-212">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="e1806-213">Näiteks kui te olete Euroopas, on teie keskkonnas üks järgmistest URL-dest:</span><span class="sxs-lookup"><span data-stu-id="e1806-213">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="e1806-214">Hetkel on saadaval järgmised regioonid.</span><span class="sxs-lookup"><span data-stu-id="e1806-214">The following regions are currently available.</span></span>

    | <span data-ttu-id="e1806-215">Azure’i regioon</span><span class="sxs-lookup"><span data-stu-id="e1806-215">Azure region</span></span> | <span data-ttu-id="e1806-216">Regiooni lühinimi</span><span class="sxs-lookup"><span data-stu-id="e1806-216">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="e1806-217">Ida-Austraalia</span><span class="sxs-lookup"><span data-stu-id="e1806-217">Australia east</span></span> | <span data-ttu-id="e1806-218">Eau</span><span class="sxs-lookup"><span data-stu-id="e1806-218">eau</span></span> |
    | <span data-ttu-id="e1806-219">Kagu-Austraalia</span><span class="sxs-lookup"><span data-stu-id="e1806-219">Australia southeast</span></span> | <span data-ttu-id="e1806-220">seau</span><span class="sxs-lookup"><span data-stu-id="e1806-220">seau</span></span> |
    | <span data-ttu-id="e1806-221">Kesk-Kanada</span><span class="sxs-lookup"><span data-stu-id="e1806-221">Canada central</span></span> | <span data-ttu-id="e1806-222">cca</span><span class="sxs-lookup"><span data-stu-id="e1806-222">cca</span></span> |
    | <span data-ttu-id="e1806-223">Ida-Kanada</span><span class="sxs-lookup"><span data-stu-id="e1806-223">Canada east</span></span> | <span data-ttu-id="e1806-224">eca</span><span class="sxs-lookup"><span data-stu-id="e1806-224">eca</span></span> |
    | <span data-ttu-id="e1806-225">Põhja-Euroopa</span><span class="sxs-lookup"><span data-stu-id="e1806-225">North Europe</span></span> | <span data-ttu-id="e1806-226">neu</span><span class="sxs-lookup"><span data-stu-id="e1806-226">neu</span></span> |
    | <span data-ttu-id="e1806-227">Lääne-Euroopa</span><span class="sxs-lookup"><span data-stu-id="e1806-227">West Europe</span></span> | <span data-ttu-id="e1806-228">weu</span><span class="sxs-lookup"><span data-stu-id="e1806-228">weu</span></span> |
    | <span data-ttu-id="e1806-229">Ida-USA</span><span class="sxs-lookup"><span data-stu-id="e1806-229">East US</span></span> | <span data-ttu-id="e1806-230">eus</span><span class="sxs-lookup"><span data-stu-id="e1806-230">eus</span></span> |
    | <span data-ttu-id="e1806-231">Lääne-USA</span><span class="sxs-lookup"><span data-stu-id="e1806-231">West US</span></span> | <span data-ttu-id="e1806-232">wus</span><span class="sxs-lookup"><span data-stu-id="e1806-232">wus</span></span> |

1. <span data-ttu-id="e1806-233">Minge **Varude halduse \> Perioodiline \> Varude nähtavuse integratsioon** ja lubage töö.</span><span class="sxs-lookup"><span data-stu-id="e1806-233">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="e1806-234">Kõik varude muutmise sündmused teenusest Supply Chain Management sisestatakse nüüd Varude nähtavusse.</span><span class="sxs-lookup"><span data-stu-id="e1806-234">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="e1806-235">Varude nähtavuse lisandmooduli avalik API</span><span class="sxs-lookup"><span data-stu-id="e1806-235">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="e1806-236">Varude nähtavuse lisandmooduli avalik REST API esitab integreerimiseks mitu kindlat lõpp-punkti.</span><span class="sxs-lookup"><span data-stu-id="e1806-236">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="e1806-237">See toetab kolme peamist suhtlustüüpi.</span><span class="sxs-lookup"><span data-stu-id="e1806-237">It supports three main interaction types:</span></span>

- <span data-ttu-id="e1806-238">Lisandmoodulisse välise süsteemi kaudu vaba kaubavaru muudatuste sisestamine</span><span class="sxs-lookup"><span data-stu-id="e1806-238">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="e1806-239">Ajakohase vaba kaubavaru päring välisest süsteemist</span><span class="sxs-lookup"><span data-stu-id="e1806-239">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="e1806-240">Automaatne sünkroonimine teenuse Supply Chain Management kaubavarudega</span><span class="sxs-lookup"><span data-stu-id="e1806-240">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="e1806-241">Automaatne sünkroonimine ei ole avaliku API osa.</span><span class="sxs-lookup"><span data-stu-id="e1806-241">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="e1806-242">Selle asemel käsitsetakse seda taustal keskkondades, kus varude nähtavuse lisandmoodul on lubatud.</span><span class="sxs-lookup"><span data-stu-id="e1806-242">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="e1806-243">Autentimine</span><span class="sxs-lookup"><span data-stu-id="e1806-243">Authentication</span></span>

<span data-ttu-id="e1806-244">Platvormi turbeluba kasutatakse laovarude nähtavuse lisandmoodulile helistamiseks.</span><span class="sxs-lookup"><span data-stu-id="e1806-244">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="e1806-245">Seepärast peate *Azure Active Directory (Azure AD) loa* genereerima kasutades Azure AD rakendust.</span><span class="sxs-lookup"><span data-stu-id="e1806-245">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="e1806-246">Seejärel peate kasutama Azure AD luba, et saada *pääsutõend* turvateenusest.</span><span class="sxs-lookup"><span data-stu-id="e1806-246">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="e1806-247">Hankige turbeteenusetõend, tehes järgmist.</span><span class="sxs-lookup"><span data-stu-id="e1806-247">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="e1806-248">Logige Azure’i portaali sisse ja kasutage seda rakenduse Supply Chain Management atribuutide `clientId` ja `clientSecret` leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="e1806-248">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="e1806-249">Tooge Azure Active Directory luba (`aadToken`), edastades HTTP-taotluse järgmiste atribuutidega:</span><span class="sxs-lookup"><span data-stu-id="e1806-249">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="e1806-250">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="e1806-250">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="e1806-251">**Meetod** - `GET`</span><span class="sxs-lookup"><span data-stu-id="e1806-251">**Method** - `GET`</span></span>
    - <span data-ttu-id="e1806-252">**Sisu (vormi andmed)**:</span><span class="sxs-lookup"><span data-stu-id="e1806-252">**Body content (form data)**:</span></span>

        | <span data-ttu-id="e1806-253">key</span><span class="sxs-lookup"><span data-stu-id="e1806-253">key</span></span> | <span data-ttu-id="e1806-254">väärtus</span><span class="sxs-lookup"><span data-stu-id="e1806-254">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="e1806-255">client_id</span><span class="sxs-lookup"><span data-stu-id="e1806-255">client_id</span></span> | <span data-ttu-id="e1806-256">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="e1806-256">${aadAppId}</span></span> |
        | <span data-ttu-id="e1806-257">client_secret</span><span class="sxs-lookup"><span data-stu-id="e1806-257">client_secret</span></span> | <span data-ttu-id="e1806-258">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="e1806-258">${aadAppSecret}</span></span> |
        | <span data-ttu-id="e1806-259">grant_type</span><span class="sxs-lookup"><span data-stu-id="e1806-259">grant_type</span></span> | <span data-ttu-id="e1806-260">client_credentials</span><span class="sxs-lookup"><span data-stu-id="e1806-260">client_credentials</span></span> |
        | <span data-ttu-id="e1806-261">resource</span><span class="sxs-lookup"><span data-stu-id="e1806-261">resource</span></span> | <span data-ttu-id="e1806-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="e1806-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="e1806-263">Peaksite saama vastuseks atribuudi `aadToken`, mis sarnaneb järgmise näitega.</span><span class="sxs-lookup"><span data-stu-id="e1806-263">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="e1806-264">Vormindage JSON-i taotlus, mis sarnaneb järgmisele:</span><span class="sxs-lookup"><span data-stu-id="e1806-264">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="e1806-265">Kus</span><span class="sxs-lookup"><span data-stu-id="e1806-265">Where:</span></span>
    - <span data-ttu-id="e1806-266">Väärtus `client_assertion` peab olema `aadToken`, mille eelmises sammus saite.</span><span class="sxs-lookup"><span data-stu-id="e1806-266">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="e1806-267">Väärtus `context` peab olema keskkonna ID, kus soovite lisandmooduli juurutada.</span><span class="sxs-lookup"><span data-stu-id="e1806-267">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="e1806-268">Häälestage kõik muud väärtused, nagu näites näidatud.</span><span class="sxs-lookup"><span data-stu-id="e1806-268">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="e1806-269">Edastage HTTP-taotlus järgmiste atribuutidega:</span><span class="sxs-lookup"><span data-stu-id="e1806-269">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="e1806-270">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="e1806-270">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="e1806-271">**Meetod** - `POST`</span><span class="sxs-lookup"><span data-stu-id="e1806-271">**Method** - `POST`</span></span>
    - <span data-ttu-id="e1806-272">**HTTP päis** – lisage API versioon (võti on `Api-Version` ja väärtus on`1.0`)</span><span class="sxs-lookup"><span data-stu-id="e1806-272">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="e1806-273">**Sisu** – lisage eelmises sammus loodud JSON-i taotlus.</span><span class="sxs-lookup"><span data-stu-id="e1806-273">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="e1806-274">Saate vastuseks tõendi `access_token`.</span><span class="sxs-lookup"><span data-stu-id="e1806-274">You will get an `access_token` in response.</span></span> <span data-ttu-id="e1806-275">Seda on teil vaja juurepääsuloaks, et kutsuda nähtavuse API.</span><span class="sxs-lookup"><span data-stu-id="e1806-275">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="e1806-276">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="e1806-276">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="e1806-277">Näidispäring</span><span class="sxs-lookup"><span data-stu-id="e1806-277">Sample Request</span></span>

<span data-ttu-id="e1806-278">Teie viite jaoks on siin näidis http-taotlus, saate selle taotluse saatmiseks kasutada mis tahes tööriistu või kodeerimiskeelt, näiteks``Postman``.</span><span class="sxs-lookup"><span data-stu-id="e1806-278">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="e1806-279">Varude nähtavuse API konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e1806-279">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="e1806-280">Enne teenuse kasutamist peate tegema järgmistes jaotistes kirjeldatud konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="e1806-280">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="e1806-281">Konfiguratsioon võib teie keskkonna üksikasjade põhjal erineda.</span><span class="sxs-lookup"><span data-stu-id="e1806-281">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="e1806-282">See hõlmab peamiselt nelja osa.</span><span class="sxs-lookup"><span data-stu-id="e1806-282">It primarily includes four parts:</span></span>

- [<span data-ttu-id="e1806-283">Eraldamine</span><span class="sxs-lookup"><span data-stu-id="e1806-283">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="e1806-284">Dimensioonide konfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="e1806-284">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="e1806-285">Indekseerimine</span><span class="sxs-lookup"><span data-stu-id="e1806-285">Indexing</span></span>](#indexing)
- [<span data-ttu-id="e1806-286">Kohandatud mõõtmine</span><span class="sxs-lookup"><span data-stu-id="e1806-286">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="e1806-287">Sektsioonimine</span><span class="sxs-lookup"><span data-stu-id="e1806-287">Partitioning</span></span>

<span data-ttu-id="e1806-288">Sektsioonimine võib oluliselt mõjutada varude nähtavuse API jõudlust.</span><span class="sxs-lookup"><span data-stu-id="e1806-288">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="e1806-289">Mõistlik on määratleda skeem, mis võimaldab väikseid andmegruppe, aga samas ka sisukaid andmepäringuid.</span><span class="sxs-lookup"><span data-stu-id="e1806-289">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="e1806-290">`organizationId` (Supply Chain Managementis `dataAreaId`) on alati osa sektsioonimisest ja varude nähtavuse vaikeväärtuseks on määratud sektsioonid, mille dimensioonid on *Sait +asukoht*.</span><span class="sxs-lookup"><span data-stu-id="e1806-290">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="e1806-291">See tähendab, et teenusepäringu esitamiseks peab need dimensioonid alati filtreerima.</span><span class="sxs-lookup"><span data-stu-id="e1806-291">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="e1806-292">*Sait* ja *asukoht* on varude nähtavuses kaks üldist vaikedimensiooni.</span><span class="sxs-lookup"><span data-stu-id="e1806-292">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="e1806-293">Supply Chain Managementis nimetatakse neid dimensioone *saidiks* (`InventSiteId`) ja *laoks* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="e1806-293">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="e1806-294">Dimensioonide konfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="e1806-294">Dimension configurations</span></span>

<span data-ttu-id="e1806-295">Varude nähtavus annab loendi üldistest dimensioonidest, et lubada mitme allika süsteemi integreerimist.</span><span class="sxs-lookup"><span data-stu-id="e1806-295">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="e1806-296">Järgmises tabelis loetletakse varude dimensioonid, mis on varude nähtavuse dimensioonide nimed.</span><span class="sxs-lookup"><span data-stu-id="e1806-296">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="e1806-297">Dimensiooni tüüp</span><span class="sxs-lookup"><span data-stu-id="e1806-297">Dimension type</span></span> | <span data-ttu-id="e1806-298">Dimensiooni nimi</span><span class="sxs-lookup"><span data-stu-id="e1806-298">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="e1806-299">Toode</span><span class="sxs-lookup"><span data-stu-id="e1806-299">Product</span></span> | `ColorId` |
| <span data-ttu-id="e1806-300">Toode</span><span class="sxs-lookup"><span data-stu-id="e1806-300">Product</span></span> | `SizeId` |
| <span data-ttu-id="e1806-301">Toode</span><span class="sxs-lookup"><span data-stu-id="e1806-301">Product</span></span> | `StyleId` |
| <span data-ttu-id="e1806-302">Toode</span><span class="sxs-lookup"><span data-stu-id="e1806-302">Product</span></span> | `ConfigId` |
| <span data-ttu-id="e1806-303">Jälitamine</span><span class="sxs-lookup"><span data-stu-id="e1806-303">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="e1806-304">Jälitamine</span><span class="sxs-lookup"><span data-stu-id="e1806-304">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="e1806-305">Koht</span><span class="sxs-lookup"><span data-stu-id="e1806-305">Location</span></span> | `LocationId` |
| <span data-ttu-id="e1806-306">Koht</span><span class="sxs-lookup"><span data-stu-id="e1806-306">Location</span></span> | `SiteId` |
| <span data-ttu-id="e1806-307">Varude olek</span><span class="sxs-lookup"><span data-stu-id="e1806-307">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="e1806-308">Laopõhine</span><span class="sxs-lookup"><span data-stu-id="e1806-308">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="e1806-309">Laopõhine</span><span class="sxs-lookup"><span data-stu-id="e1806-309">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="e1806-310">Laopõhine</span><span class="sxs-lookup"><span data-stu-id="e1806-310">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="e1806-311">Eelmises tabelis loetletud dimensiooni tüüp on ainult teave.</span><span class="sxs-lookup"><span data-stu-id="e1806-311">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="e1806-312">Varude nähtavuses ei ole vaja määratleda dimensiooni tüüpi.</span><span class="sxs-lookup"><span data-stu-id="e1806-312">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="e1806-313">Kui on olemas kohandatud dimensioon ja see peab muutuma vaikeväärtuseks, kui varude nähtavus seda kasutab, saate **kohandatud dimensiooni** nime varude nähtavuses konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="e1806-313">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="e1806-314">Väliste süsteemide juurdepääs varude nähtavusele läbi RESTfuli API-de, mis võimaldavad esitada teavet antud dimensioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="e1806-314">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="e1806-315">Integratsiooni jaoks võimaldab varude nähtavus teil konfigureerida *väliskanali andmeallika* ja lähtedimensiooni vastavalt *sihtdimensioonile* varude nähtavuse korral.</span><span class="sxs-lookup"><span data-stu-id="e1806-315">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="e1806-316">Sihtdimensioonid peavad hõlmama ühte järgmistest.</span><span class="sxs-lookup"><span data-stu-id="e1806-316">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="e1806-317">Varude nähtavuse vaikedimensioonid</span><span class="sxs-lookup"><span data-stu-id="e1806-317">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="e1806-318">Kohandatud dimensioonid</span><span class="sxs-lookup"><span data-stu-id="e1806-318">Custom dimensions</span></span>

<span data-ttu-id="e1806-319">Dimensioonide konfigureerimise eesmärk on ühtlustada mitme süsteemi integreerimist vastavalt päringule dimensioonide ja sisestamise sündmuse dimensioonidega.</span><span class="sxs-lookup"><span data-stu-id="e1806-319">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="e1806-320">Indekseerimine</span><span class="sxs-lookup"><span data-stu-id="e1806-320">Indexing</span></span>

<span data-ttu-id="e1806-321">Enamiku ajast ei ole vaba kaubavaru päring mitte ainult kõrgeimal „kogutasemel“, kuid soovi korral saate vaadata varude dimensioonide alusel summeeritud tulemusi.</span><span class="sxs-lookup"><span data-stu-id="e1806-321">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="e1806-322">Varude nähtavus annab paindlikkuse, lubades teil häälestada indekseid, mis põhinevad dimensioonil või dimensioonide kombinatsioonil.</span><span class="sxs-lookup"><span data-stu-id="e1806-322">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="e1806-323">Praegu saate indekseid konfigureerida ainult kuni viieni.</span><span class="sxs-lookup"><span data-stu-id="e1806-323">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="e1806-324">Peate hoolikalt kaaluma, millist dimensiooni või dimensioonide kombinatsiooni kasutate enne rakendamist, et tagada selle vastavus teie ettevõtte vajadustele.</span><span class="sxs-lookup"><span data-stu-id="e1806-324">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="e1806-325">Näiteks kui soovite teha päringuid toodete kohta järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e1806-325">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="e1806-326">Päring saadaval oleva summeeritud toote kohta *värvi* ja *suuruse* dimensioonide kaupa.</span><span class="sxs-lookup"><span data-stu-id="e1806-326">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="e1806-327">Mõnel juhul soovite ainult toote kohta päringut esitada.</span><span class="sxs-lookup"><span data-stu-id="e1806-327">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="e1806-328">Teil oleks kaks indeksit, mis on määratletud järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e1806-328">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="e1806-329">Tühi sulg summeeritakse sektsioonis toote ID põhjal.</span><span class="sxs-lookup"><span data-stu-id="e1806-329">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="e1806-330">Indekseerimine määratleb, kuidas saate oma tulemusi grupeerida päringusätte `groupBy` alusel.</span><span class="sxs-lookup"><span data-stu-id="e1806-330">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="e1806-331">Sel juhul, kui te ei määratle ühtegi sätte `groupBy` väärtust, saate kogusummad `productid` kaupa.</span><span class="sxs-lookup"><span data-stu-id="e1806-331">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="e1806-332">Vastasel juhul, kui määrate `groupBy` väärtuseks `groupBy=ColorId&groupBy=SizeId`, saadetakse teile mitu rida, mis põhinevad süsteemi erinevate värvide ja suuruse kombinatsioonidel.</span><span class="sxs-lookup"><span data-stu-id="e1806-332">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="e1806-333">Saate esitada päringu kriteeriumid päringu sisus.</span><span class="sxs-lookup"><span data-stu-id="e1806-333">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="e1806-334">Siin on näide päringust toote värvi ja suuruse kombinatsiooniga.</span><span class="sxs-lookup"><span data-stu-id="e1806-334">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
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

<span data-ttu-id="e1806-335">Välja `filters` puhul toetab see praegu ainult mitut `ProductId` väärtust.</span><span class="sxs-lookup"><span data-stu-id="e1806-335">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="e1806-336">Kui `ProductId` on tühi massiiv, esitatakse päring kõikidele toodetele.</span><span class="sxs-lookup"><span data-stu-id="e1806-336">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="e1806-337">Kohandatud mõõtmine</span><span class="sxs-lookup"><span data-stu-id="e1806-337">Custom measurement</span></span>

<span data-ttu-id="e1806-338">Vaikimisi antud mõõdukogused on seotud teenusega Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e1806-338">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="e1806-339">Soovi korral võite siiski saada koguse, mis on valmistatud vaikemõõtude kombinatsioonis.</span><span class="sxs-lookup"><span data-stu-id="e1806-339">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="e1806-340">Selleks võib olla kohandatud koguste konfiguratsioon, mis lisatakse vabade päringute väljundile.</span><span class="sxs-lookup"><span data-stu-id="e1806-340">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="e1806-341">Funktsioon võimaldab teil kohandatud mõõtmiseks määratleda lisatavate mõõtude kogumi ja/või meetmete kogumi, mis on kohandatud mõõtmisest lahutatud.</span><span class="sxs-lookup"><span data-stu-id="e1806-341">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="e1806-342">Näiteks järgmise päringu tingimusega konfigureerite kohandatud mõõtmise koguse üksusena `MyCustomAvailableforReservation`, mida tarbib tarbimise süsteem.</span><span class="sxs-lookup"><span data-stu-id="e1806-342">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="e1806-343">Tarbimise süsteem</span><span class="sxs-lookup"><span data-stu-id="e1806-343">Consumption system</span></span> | <span data-ttu-id="e1806-344">Arvutatud mõõdikud</span><span class="sxs-lookup"><span data-stu-id="e1806-344">Calculated measurers</span></span> | <span data-ttu-id="e1806-345">Andmeallikas</span><span class="sxs-lookup"><span data-stu-id="e1806-345">Data source</span></span> | <span data-ttu-id="e1806-346">Muutuja</span><span class="sxs-lookup"><span data-stu-id="e1806-346">Modifier</span></span> | <span data-ttu-id="e1806-347">Muutuja arvutustüüp</span><span class="sxs-lookup"><span data-stu-id="e1806-347">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="e1806-348">Lisa</span><span class="sxs-lookup"><span data-stu-id="e1806-348">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="e1806-349">Lisa</span><span class="sxs-lookup"><span data-stu-id="e1806-349">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="e1806-350">Lahutamine</span><span class="sxs-lookup"><span data-stu-id="e1806-350">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="e1806-351">Lisa</span><span class="sxs-lookup"><span data-stu-id="e1806-351">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="e1806-352">Lahutamine</span><span class="sxs-lookup"><span data-stu-id="e1806-352">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="e1806-353">Lisa</span><span class="sxs-lookup"><span data-stu-id="e1806-353">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="e1806-354">Lisa</span><span class="sxs-lookup"><span data-stu-id="e1806-354">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="e1806-355">Lahutamine</span><span class="sxs-lookup"><span data-stu-id="e1806-355">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="e1806-356">Lahutamine</span><span class="sxs-lookup"><span data-stu-id="e1806-356">Subtraction</span></span> |

<span data-ttu-id="e1806-357">Sellega tagastatakse kohandatud mõõtmise koguse päring järgmise väljundina.</span><span class="sxs-lookup"><span data-stu-id="e1806-357">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="e1806-358">Üksuse `MyCustomAvailableforReservation` väljundi aluseks on kohandatud mõõtmiste arvutamise säte.</span><span class="sxs-lookup"><span data-stu-id="e1806-358">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="e1806-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="e1806-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="e1806-360">Vaba kaubavaru muudatuste sisestamine</span><span class="sxs-lookup"><span data-stu-id="e1806-360">Posting on-hand changes</span></span>

<span data-ttu-id="e1806-361">Sündmuse sisestamise täpne URL sõltub geograafilisest piirkonnast.</span><span class="sxs-lookup"><span data-stu-id="e1806-361">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="e1806-362">See on järgmises vormis.</span><span class="sxs-lookup"><span data-stu-id="e1806-362">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="e1806-363">Kui see on autenditud, saab seda URL-i kasutada koos HTTP `POST`-meetodiga, et saata teenusele vaba kaubavaru muudatuste sündmusi.</span><span class="sxs-lookup"><span data-stu-id="e1806-363">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="e1806-364">Dynamics 365 teenustega suhtlemiseks HTTP-taotluste kaudu kasutatakse spetsiaalset päist, mis tähistab Supply Chain Managementi eksemplari keskkonna ID-d, millega andmed on lingitud.</span><span class="sxs-lookup"><span data-stu-id="e1806-364">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="e1806-365">Näide:</span><span class="sxs-lookup"><span data-stu-id="e1806-365">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="e1806-366">Vaba kaubavaru muudatuste päringu sisestamise näide 1</span><span class="sxs-lookup"><span data-stu-id="e1806-366">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="e1806-367">See näide näitab olukorda, kus häälestate dimensiooni konfiguratsiooni Power Appsis.</span><span class="sxs-lookup"><span data-stu-id="e1806-367">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="e1806-368">Kasutage järgmist päringut dimensioonide vastenduste konfigureerimiseks Power Appsis.</span><span class="sxs-lookup"><span data-stu-id="e1806-368">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="e1806-369">Nüüd saate päringus määrata väärtuse `dimensionDataSource` ja kasutada kohandatud dimensioone.</span><span class="sxs-lookup"><span data-stu-id="e1806-369">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="e1806-370">Süsteem teisendab kohandatud dimensioonid automaatselt põhidimensioonideks.</span><span class="sxs-lookup"><span data-stu-id="e1806-370">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="e1806-371">Vaba kaubavaru muudatuste päringu sisestamise näide 2</span><span class="sxs-lookup"><span data-stu-id="e1806-371">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="e1806-372">Selles näites kuvatakse stsenaarium, kus dimensioonide konfigureerimise jaoks pole vastendusi Power Appsis vastendusi häälestatud, nii et sisestamisel tuleks samuti põhidimensioone kasutada.</span><span class="sxs-lookup"><span data-stu-id="e1806-372">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="e1806-373">Kõik dimensioonid peavad olema põhidimensioonid, kui väli `dimensionDataSource` on väärtusega null, tühi või seal on tühik.</span><span class="sxs-lookup"><span data-stu-id="e1806-373">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="e1806-374">JSON-dokumendi väljade atribuudid</span><span class="sxs-lookup"><span data-stu-id="e1806-374">JSON document field properties</span></span>

<span data-ttu-id="e1806-375">Eespool antud JSON-päringu näidete väljadel on järgmises tabelis loetletud atribuudid.</span><span class="sxs-lookup"><span data-stu-id="e1806-375">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="e1806-376">Välja kood</span><span class="sxs-lookup"><span data-stu-id="e1806-376">Field ID</span></span> | <span data-ttu-id="e1806-377">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e1806-377">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="e1806-378">Konkreetse muudatuse sündmuse kordumatu ID.</span><span class="sxs-lookup"><span data-stu-id="e1806-378">A unique ID for the specific change event.</span></span> <span data-ttu-id="e1806-379">Seda ID-d kasutatakse tagamaks, et kui suhtlus teenusega nurjub sisestamise ajal, ei põhjustaks sündmuse taasesitamine süsteemis sama sündmuse topeltloendamist.</span><span class="sxs-lookup"><span data-stu-id="e1806-379">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="e1806-380">Sündmusega lingitud organisatsiooni identifikaator.</span><span class="sxs-lookup"><span data-stu-id="e1806-380">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="e1806-381">See vastendab Supply Chain Managementi organisatsioonide või andmepiirkonna ID-sid.</span><span class="sxs-lookup"><span data-stu-id="e1806-381">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="e1806-382">Kõnealuse toote identifikaator.</span><span class="sxs-lookup"><span data-stu-id="e1806-382">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="e1806-383">Kogus, mille võrra laoseisu tuleb muuta.</span><span class="sxs-lookup"><span data-stu-id="e1806-383">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="e1806-384">Kui riiulile lisati näiteks kümme uut saiakest, oleks see väärtus 10.</span><span class="sxs-lookup"><span data-stu-id="e1806-384">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="e1806-385">Kui riiulilt eemaldati või müüdi kolm saiakest, oleks see väärtus -3.</span><span class="sxs-lookup"><span data-stu-id="e1806-385">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="e1806-386">See on sisestatud muudatuse sündmuses ja päringus kasutatud andmeallikas.</span><span class="sxs-lookup"><span data-stu-id="e1806-386">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="e1806-387">Andmeallika määramisel saate kasutada määratud andmeallika kohandatud dimensioone.</span><span class="sxs-lookup"><span data-stu-id="e1806-387">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="e1806-388">Dimensiooni konfigureerimisega saab varude nähtavus vastendada kohandatud dimensioonid üldiste vaikedimensioonidega.</span><span class="sxs-lookup"><span data-stu-id="e1806-388">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="e1806-389">Kui väärtust `dimensionDataSource` pole määratud, saate päringutes kasutada ainult üldisi vaikedimensioone.</span><span class="sxs-lookup"><span data-stu-id="e1806-389">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="e1806-390">Dünaamiline võtme-/väärtusepaari mapp.</span><span class="sxs-lookup"><span data-stu-id="e1806-390">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="e1806-391">Need vastendavad mõned dimensioonid Supply Chain Managementis, kuid võite lisada ka kohandatud dimensioone (nt *Allikas*), mis võib tähistada sündmuse pärinemist Supply Chain Managementist või välisest süsteemist.</span><span class="sxs-lookup"><span data-stu-id="e1806-391">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="e1806-392">Praeguse vaba kaubavaru päring</span><span class="sxs-lookup"><span data-stu-id="e1806-392">Querying current on-hand</span></span>

<span data-ttu-id="e1806-393">Praeguse laoseisu päringute puhul on lõpp-punktil sarnane URL.</span><span class="sxs-lookup"><span data-stu-id="e1806-393">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="e1806-394">See on päringus meetodiga HTTP `POST`.</span><span class="sxs-lookup"><span data-stu-id="e1806-394">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="e1806-395">Praeguse vaba kaubavaru päringu näide 1</span><span class="sxs-lookup"><span data-stu-id="e1806-395">Current on-hand query example 1</span></span>

<span data-ttu-id="e1806-396">See näide näitab olukorda, kus olete Power Appsis dimensioonide konfigureerimise juba lõpule viinud.</span><span class="sxs-lookup"><span data-stu-id="e1806-396">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="e1806-397">Kasutage järgmist päringut dimensioonide vastenduste konfigureerimiseks Power Appsis.</span><span class="sxs-lookup"><span data-stu-id="e1806-397">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="e1806-398">Nüüd saate päringus määrata väärtuse `dimensionDataSource` ja kasutada kohandatud dimensioone.</span><span class="sxs-lookup"><span data-stu-id="e1806-398">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="e1806-399">Süsteem teisendab kohandatud dimensioonid automaatselt põhidimensioonideks.</span><span class="sxs-lookup"><span data-stu-id="e1806-399">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="e1806-400">Saate määrata väärtuse `DimensionDataSource` üksusel `filters` ja määrata kohandatud dimensioonid nii üksuse `filters` kui ka `groupByValues` jaoks.</span><span class="sxs-lookup"><span data-stu-id="e1806-400">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="e1806-401">Süsteem teisendab kohandatud dimensioonid automaatselt põhidimensioonideks.</span><span class="sxs-lookup"><span data-stu-id="e1806-401">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="e1806-402">Praeguse vaba kaubavaru päringu näide 2</span><span class="sxs-lookup"><span data-stu-id="e1806-402">Current on-hand query example 2</span></span>

<span data-ttu-id="e1806-403">Selles näites kuvatakse stsenaarium, kus dimensioonide konfigureerimise jaoks pole vastendusi Power Appsis vastendusi häälestatud, nii et sisestamisel tuleks samuti põhidimensioone kasutada.</span><span class="sxs-lookup"><span data-stu-id="e1806-403">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="e1806-404">Kõik dimensioonid peavad olema põhidimensioonid, kui väli `dimensionDataSource` jaotises `filters` on väärtusega null, tühi või seal on tühik.</span><span class="sxs-lookup"><span data-stu-id="e1806-404">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="e1806-405">Näide tagastatud tulemusest</span><span class="sxs-lookup"><span data-stu-id="e1806-405">Example return result</span></span>

<span data-ttu-id="e1806-406">Eelmistes näidetes kuvatud päringud võivad tagastada sellise tulemuse.</span><span class="sxs-lookup"><span data-stu-id="e1806-406">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="e1806-407">Võtke arvesse, et koguseväljad on struktuurilt justkui meetmete ja nendega seotud väärtuste sõnastikud.</span><span class="sxs-lookup"><span data-stu-id="e1806-407">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]