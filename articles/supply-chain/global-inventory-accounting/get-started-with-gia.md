---
title: Global Inventory Accounting kasutamise alustamine
description: See teema kirjeldab, kuidas alustada Global Inventory Accounting kasutamist.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301694"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="0619c-103">Global Inventory Accounting kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="0619c-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="0619c-104">Global Inventory Accounting võimaldab teil teha mitut laoarvestust teie seadistatud Global Inventory Accounting pearaamatutes.</span><span class="sxs-lookup"><span data-stu-id="0619c-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="0619c-105">Te seostate iga Global Inventory Accounting pearaamatu *reegliga*.</span><span class="sxs-lookup"><span data-stu-id="0619c-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="0619c-106">Reegel on järgmist tüüpi raamatupidamispoliitikate kogumik.</span><span class="sxs-lookup"><span data-stu-id="0619c-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="0619c-107">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="0619c-107">Cost object</span></span>
- <span data-ttu-id="0619c-108">Sisendi mõõtmise alus</span><span class="sxs-lookup"><span data-stu-id="0619c-108">Input measurement basis</span></span>
- <span data-ttu-id="0619c-109">Kuluvoo eeldus</span><span class="sxs-lookup"><span data-stu-id="0619c-109">Cost flow assumption</span></span>
- <span data-ttu-id="0619c-110">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="0619c-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="0619c-111">Isegi kui olete Global Inventory Accounting laoarvestuse sisse lülitanud, saate jätkuvalt samamoodi Microsoft Dynamics 365 Supply Chain Managementis laoarvestust teha.</span><span class="sxs-lookup"><span data-stu-id="0619c-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="0619c-112">Global Inventory Accounting on lisandmoodul.</span><span class="sxs-lookup"><span data-stu-id="0619c-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="0619c-113">Selle funktsioonide kättesaadavaks tegemiseks peate selle installima teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu.</span><span class="sxs-lookup"><span data-stu-id="0619c-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="0619c-114">Saate valida, kas hinnata seda testimiskeskkonnas enne selle sisselülitamist töökeskkondades.</span><span class="sxs-lookup"><span data-stu-id="0619c-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="0619c-115">Global Inventory Accounting laoarvestus ei toeta praegu kõiki Supply Chain Management integreeritud kuluhalduse funktsioone.</span><span class="sxs-lookup"><span data-stu-id="0619c-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="0619c-116">Seega on oluline, et hindaksite, kas hetkel saadaolev funktsioonide komplekt vastab teie nõuetele.</span><span class="sxs-lookup"><span data-stu-id="0619c-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="0619c-117">Global Inventory Accounting avaliku eelvaate saamine</span><span class="sxs-lookup"><span data-stu-id="0619c-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0619c-118">Global Inventory Accounting laoarvestuse kasutamiseks peab teil olema LCS-iga lubatud kõrge saadavuskeskkond (mitte OneBoxi keskkond).</span><span class="sxs-lookup"><span data-stu-id="0619c-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="0619c-119">Lisaks peate käitama Supply Chain Management versiooni 10.0.19 või uuema.</span><span class="sxs-lookup"><span data-stu-id="0619c-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="0619c-120">Global Inventory Accounting avalikku eelvaatesse registreerumiseks saatke oma LCS-i keskkonna ID meiliga [Global Inventory Accounting töörühmale](mailto:GlobalInventoryAccounting@service.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="0619c-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="0619c-121">Kui olete programmi heaks kiidetud, saadab meeskond teile järeltegevuse meili, mis sisaldab Global Inventory Accounting beetavõtit ja teie teenuse lõpp-punkte.</span><span class="sxs-lookup"><span data-stu-id="0619c-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="0619c-122">Pärast beetavõtme saamist saate [installida lisandmooduli](#install).</span><span class="sxs-lookup"><span data-stu-id="0619c-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="0619c-123">Litsentsimine</span><span class="sxs-lookup"><span data-stu-id="0619c-123">Licensing</span></span>

<span data-ttu-id="0619c-124">Global Inventory Accounting laoarvestus litsentsitakse koos standardsete laoarvestuse funktsioonidega, mis on saadaval teenuse Supply Chain Management jaoks.</span><span class="sxs-lookup"><span data-stu-id="0619c-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="0619c-125">Te ei pea Global Inventory Accounting kasutamiseks ostma täiendavat litsentsi.</span><span class="sxs-lookup"><span data-stu-id="0619c-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0619c-126">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="0619c-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="0619c-127">Saate häälestada Microsoft Power Platformi integratsiooni.</span><span class="sxs-lookup"><span data-stu-id="0619c-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="0619c-128">Enne lisandfunktsiooni lubamist tuleb teil need sammud Microsoft Power Platform järgmiste sammudega integreerida.</span><span class="sxs-lookup"><span data-stu-id="0619c-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="0619c-129">Avage LCS-i keskkond, kuhu soovite teenuse lisada.</span><span class="sxs-lookup"><span data-stu-id="0619c-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="0619c-130">Avage **Kõik üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="0619c-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="0619c-131">Valige **Power Platform\`i integratsioon** jaotises nupp **Seadistused**.</span><span class="sxs-lookup"><span data-stu-id="0619c-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="0619c-132">Märkige ruut **Power Platform platvormi keskkonna seadistus** dialoogiboksis ja valige seejärel **Seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="0619c-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="0619c-133">Tavaliselt võtab seadistus aega 60 kuni 90 minutit.</span><span class="sxs-lookup"><span data-stu-id="0619c-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="0619c-134">Pärast Microsoft Power Platform keskkonna seadistuse lõpuleviimist kuvatakse lehel teie keskkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="0619c-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="0619c-135">Lisaks kuvatakse jaotises **Power Platform integratsioon** lause "Power Platform keskkonna seadistus on lõpule viidud."</span><span class="sxs-lookup"><span data-stu-id="0619c-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="0619c-136">Global Inventory Accounting laoarvestus ei nõua topeltkirjutuse rakendust.</span><span class="sxs-lookup"><span data-stu-id="0619c-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="0619c-137">Lisateavet vt teemast [Häälestamine peale keskkonna juurutamist](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span><span class="sxs-lookup"><span data-stu-id="0619c-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="0619c-138">Dataverse'i häälestamine</span><span class="sxs-lookup"><span data-stu-id="0619c-138">Set up Dataverse</span></span>

<span data-ttu-id="0619c-139">Enne Dataverse seadistamist järgmiste sammude abil lisage oma rentnikule Global Inventory Accounting laoarvestuse põhimõtted.</span><span class="sxs-lookup"><span data-stu-id="0619c-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="0619c-140">Installige Azure AD Windows PowerShell Module v2, nagu on kirjeldatud [Instalige Azure Active Directory PowerShell Graph'ile](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="0619c-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="0619c-141">Käivitage järgmine PowerShell käsk.</span><span class="sxs-lookup"><span data-stu-id="0619c-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="0619c-142">Järgmisena looge rakenduse kasutajad Global Inventory Accounting laoarvestuse jaoks Dataverse'is järgmiste sammude abil.</span><span class="sxs-lookup"><span data-stu-id="0619c-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="0619c-143">Avage oma Dataverse keskkonna URL.</span><span class="sxs-lookup"><span data-stu-id="0619c-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="0619c-144">Minge **Lisaseaded \> Süsteem \> Turvalisus \> Kasutajad** ja looge rakenduse kasutaja.</span><span class="sxs-lookup"><span data-stu-id="0619c-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="0619c-145">Kasutage **Vaade** välja, et muuta lehe vaade *Rakenduse kasutajad*.</span><span class="sxs-lookup"><span data-stu-id="0619c-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="0619c-146">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0619c-146">Select **New**.</span></span>
1. <span data-ttu-id="0619c-147">Määrake välja **Rakenduse ID** väärtuseks *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span><span class="sxs-lookup"><span data-stu-id="0619c-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="0619c-148">Valige **Määra roll** ja seejärel valige *Süsteemiadministraator*.</span><span class="sxs-lookup"><span data-stu-id="0619c-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="0619c-149">Kui rolli nimi on *Common Data Service Kasutaja*, valige ka see.</span><span class="sxs-lookup"><span data-stu-id="0619c-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="0619c-150">Korrake eelnevaid samme, kuid seadistage **Rakenduse ID** välja väärtuseks *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span><span class="sxs-lookup"><span data-stu-id="0619c-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="0619c-151">Lisateavet leiate teemast [Rakenduse kasutaja loomine](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="0619c-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="0619c-152">Kui teie Dataverse installi vaikekeel ei ole inglise keel, järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="0619c-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="0619c-153">Avage **Täpsemad seadistused \>Administreerimine \> Keeled**.</span><span class="sxs-lookup"><span data-stu-id="0619c-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="0619c-154">Valige *Inglise keel* (*LanguageCode=1033*) ja valige **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="0619c-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="0619c-155">Lisandmooduli installimine</span><span class="sxs-lookup"><span data-stu-id="0619c-155">Install the add-in</span></span>

<span data-ttu-id="0619c-156">Järgige neid samme lisandmooduli installimiseks Global Inventory Accounting laoarvestuse kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="0619c-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="0619c-157">Global Inventory Accounting avaliku eelvaatesse [registreerumiseks](#sign-up).</span><span class="sxs-lookup"><span data-stu-id="0619c-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="0619c-158">Logige teenusesse [LCS](https://lcs.dynamics.com/Logon/Index) sisse.</span><span class="sxs-lookup"><span data-stu-id="0619c-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="0619c-159">Avage suvand **Eelvaate funktsiooni haldamine**.</span><span class="sxs-lookup"><span data-stu-id="0619c-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="0619c-160">Valige plussmärk (**+**).</span><span class="sxs-lookup"><span data-stu-id="0619c-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="0619c-161">Sisestage väljale **Kood** Global Inventory Accounting lisandmooduli beetavõti.</span><span class="sxs-lookup"><span data-stu-id="0619c-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="0619c-162">(Peaksite olema saanud oma beetavõtme meiliga, kui olete registreerunud.)</span><span class="sxs-lookup"><span data-stu-id="0619c-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="0619c-163">Valige **Tühista blokeerimine**.</span><span class="sxs-lookup"><span data-stu-id="0619c-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="0619c-164">Avage LCS-i keskkond, kuhu soovite teenuse lisada.</span><span class="sxs-lookup"><span data-stu-id="0619c-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="0619c-165">Avage **Kõik üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="0619c-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="0619c-166">Avage **Power Platform integratsioon** ja valige **Seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="0619c-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="0619c-167">Märkige ruut **Power Platform platvormi keskkonna seadistus** dialoogiboksis ja valige seejärel **Seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="0619c-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="0619c-168">Tavaliselt võtab seadistus aega 60 kuni 90 minutit.</span><span class="sxs-lookup"><span data-stu-id="0619c-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="0619c-169">Kui Microsoft Power Platform keskkonna häälestamine on lõpule viidud, valige kiirkaardil **Keskkonna lisandmoodulid** suvand **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="0619c-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="0619c-170">Valige **Globaalne laoarvestus**.</span><span class="sxs-lookup"><span data-stu-id="0619c-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="0619c-171">Täitke paigaldusjuhendit ja nõustuge nõuete ja tingimustega.</span><span class="sxs-lookup"><span data-stu-id="0619c-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="0619c-172">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="0619c-172">Select **Install**.</span></span>
1. <span data-ttu-id="0619c-173">Peaksite nägema kiirkaardil **Keskkonna lisandmoodulid**, et Global Inventory Accounting installitakse.</span><span class="sxs-lookup"><span data-stu-id="0619c-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="0619c-174">Mõne minuti pärast peaks olek *Installimine* muutuma olekuks *Installitud*.</span><span class="sxs-lookup"><span data-stu-id="0619c-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="0619c-175">(Selle muudatuse nägemiseks võib olla vaja lehte värskendada.) Pärast seda on Global Inventory Accounting kasutamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="0619c-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="0619c-176">Integratsiooni seadistamine</span><span class="sxs-lookup"><span data-stu-id="0619c-176">Set up the integration</span></span>

<span data-ttu-id="0619c-177">Järgige neid samme Global Inventory Accounting ja Supply Chain Management vahelise integreerimise häälestamiseks.</span><span class="sxs-lookup"><span data-stu-id="0619c-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="0619c-178">Logige sisse rakendusse Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0619c-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="0619c-179">Avage **Süsteemihaldus \> Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="0619c-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="0619c-180">Valige **Otsi värskendusi**.</span><span class="sxs-lookup"><span data-stu-id="0619c-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="0619c-181">Vahekaardil **Kõik** otsige funktsiooni nimega *Globaalne laoarvestus*.</span><span class="sxs-lookup"><span data-stu-id="0619c-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="0619c-182">Valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="0619c-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="0619c-183">Minge **Globaalne laoarvestus \> Seadistamine \>Globaalse laoarvestuse parameetrid \> Integratsiooniparameetrid**.</span><span class="sxs-lookup"><span data-stu-id="0619c-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="0619c-184">**Andmeteenuse lõpp-punkti** ja **Globaalse laoarvestuse lõpp-punkti** väljadele sisestage URL-id meilist, mille Global Inventory Accounting meeskond saatis eelvaate jaoks registreerumisel.</span><span class="sxs-lookup"><span data-stu-id="0619c-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="0619c-185">Global Inventory Accounting laoarvestus on nüüd kasutamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="0619c-185">Global Inventory Accounting is now ready to use.</span></span>
