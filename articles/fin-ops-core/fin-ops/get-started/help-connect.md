---
title: Spikri kasutuskogemuse konfigureerimine Finance and Operationsi rakendustes
description: Selles teemas antakse teavet osade Microsoft Dynamics 365 rakenduste spikrisüsteemi komponentide kohta. Samuti selgitatakse, kuidas neid rakendusi ühendada ja esitatakse kohandatud spikri loomise protsessi kokkuvõte.
author: margoc
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0495bbc008ed1760b98c2c1ace63fc4a8b1ab5cc
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694417"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="37af5-104">Spikri kasutuskogemuse konfigureerimine Finance and Operationsi rakendustes</span><span class="sxs-lookup"><span data-stu-id="37af5-104">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37af5-105">Selles teemas antakse ülevaade Finance and Operationsi rakenduste spikrisüsteemi komponentide kohta, nt Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ja Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="37af5-105">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="37af5-106">Samuti selgitatakse selles teemas, kuidas neid komponente ühendada ja esitatakse kohandatud spikri loomise protsessi kokkuvõte.</span><span class="sxs-lookup"><span data-stu-id="37af5-106">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="37af5-107">Spikri arhitektuur</span><span class="sxs-lookup"><span data-stu-id="37af5-107">Help architecture</span></span>

<span data-ttu-id="37af5-108">Finance and Operationsi rakendused hõlmavad mõistete ülevaateid ja muid teemasid, mida avaldatakse saidil [https://docs.microsoft.com/dynamics365](/dynamics365/).</span><span class="sxs-lookup"><span data-stu-id="37af5-108">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="37af5-109">Selle sisu juurde pääseb seejärel tootesisese paani **Spikker** kaudu.</span><span class="sxs-lookup"><span data-stu-id="37af5-109">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="37af5-110">Järgmisel joonisel on näidatud spikrisüsteemi osad.</span><span class="sxs-lookup"><span data-stu-id="37af5-110">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="37af5-111">[![Spikri arhitektuur](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="37af5-111">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="37af5-112">Tootesisene spikrisüsteem toob artikleid saidilt docs.microsoft.com ja teistelt ühendatud veebisaitidelt.</span><span class="sxs-lookup"><span data-stu-id="37af5-112">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="37af5-113">See toob ka teenuse Microsoft Dynamics Lifecycle Services (LCS) äriprotsesside modelleerijas talletatud tegevuse juhiseid.</span><span class="sxs-lookup"><span data-stu-id="37af5-113">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="37af5-114">Tegevuse juhiste lisamine</span><span class="sxs-lookup"><span data-stu-id="37af5-114">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="37af5-115">Vahekaart **Tegevuse juhised** ei ole praegu rakendustes Human Resources ega Commerce saadaval.</span><span class="sxs-lookup"><span data-stu-id="37af5-115">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="37af5-116">Kuid rakenduse Human Resources alustuskogemuse tegevuse juhised jäävad põhifunktsioonide pakkumiseks saadavaks.</span><span class="sxs-lookup"><span data-stu-id="37af5-116">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="37af5-117">Nii rakenduse Human Resources kui ka Commerce protseduurispikker on saadaval ka saidil [https://docs.microsoft.com/dynamics365](/dynamics365/).</span><span class="sxs-lookup"><span data-stu-id="37af5-117">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="37af5-118">Süsteemiadministraatorid saavad lehel **Süsteemi parameetrid** konfigureerida vastavatele tegevuse juhiste teekidele juurdepääsu rakendamise jaoks.</span><span class="sxs-lookup"><span data-stu-id="37af5-118">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="37af5-119">Spikri konfigureerimiseks peate logima sisse kontoga samas rentnikus, kuhu rakendus juurutatakse.</span><span class="sxs-lookup"><span data-stu-id="37af5-119">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="37af5-120">LCS-teegiga ei saa luua ühendust rakenduse eksemplarist, mis töötab virtuaalsel kõvakettal (VHD).</span><span class="sxs-lookup"><span data-stu-id="37af5-120">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="37af5-121">[![Süsteemi parameetrite vorm koos spikrisätetega](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="37af5-121">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="37af5-122">Lahenduse jaoks tegevuse juhiste konfigureerimiseks, järgige lehel **Süsteemi parameetrid** toodud juhiseid.</span><span class="sxs-lookup"><span data-stu-id="37af5-122">To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37af5-123">Vahekaardi **Spikker** esmakordsel avamisel peate looma ühenduse elutsükli teenustega.</span><span class="sxs-lookup"><span data-stu-id="37af5-123">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="37af5-124">Valige kindlasti vormi keskel olev link, oodake, kuni ühendus on loodud, sulgege dialoogiboks ja seejärel valige **OK**, et avada **Parameetrite vormid**.</span><span class="sxs-lookup"><span data-stu-id="37af5-124">Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="37af5-125">[![Ühenda LCS-iga](./media/connect-to-lcs-crop-1024x365.png "Ühenda LCS-iga")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="37af5-125">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="37af5-126">Valige elutsükli teenuste projekt, millega ühendus luua.</span><span class="sxs-lookup"><span data-stu-id="37af5-126">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="37af5-127">Valige BPM-i teegid (valitud projektis), kust tegevuse salvestised tuua.</span><span class="sxs-lookup"><span data-stu-id="37af5-127">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="37af5-128">Valige BPM-i teekide kuvamise järjekord.</span><span class="sxs-lookup"><span data-stu-id="37af5-128">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="37af5-129">Kuvamise järjekord määratleb teekidest pärinevate tegevuse salvestiste kuvamise järjekorra paanil **Spikker**.</span><span class="sxs-lookup"><span data-stu-id="37af5-129">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="37af5-130">Kui olete need toimingud lõpetanud, võite avada paani **Spikker** ja valida vahekaardi **Tegevuse juhised**. Teile kuvatakse nüüd tegevuse juhiseid, mis rakenduvad lehele, millel parajasti rakenduses Finance and Operations olete.</span><span class="sxs-lookup"><span data-stu-id="37af5-130">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="37af5-131">Kui ühtegi ülesande juhist ei leita, saate sisestada märksõnu otsingu kitsendamiseks.</span><span class="sxs-lookup"><span data-stu-id="37af5-131">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="37af5-132">Tõlgitud tegevusjuhiste kuvamine</span><span class="sxs-lookup"><span data-stu-id="37af5-132">Showing translated task guides</span></span>

<span data-ttu-id="37af5-133">Tõlgitud tegevuse juhised avaldati esmakordselt 2016. aasta mai APQC ühendatud teegis ja teegis Alustamine.</span><span class="sxs-lookup"><span data-stu-id="37af5-133">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="37af5-134">Lokaliseeritud tegevuse juhise Spikker vaatamiseks veenduge, et teie Dynamics 365 lahendus oleks ühendatud 2016. aasta mai teegiga.</span><span class="sxs-lookup"><span data-stu-id="37af5-134">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="37af5-135">Kasutajad saavad muuta keelt, milles tegevuse juhis kuvatakse, muutes keelesätetteid jaotises **Suvandid** &gt; **Eelistused**.</span><span class="sxs-lookup"><span data-stu-id="37af5-135">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="37af5-136">Kuigi paljud tegevuse juhised on tõlgitud, ei kuva klient praegu tõlgitud tegevuse juhiste nimesid.</span><span class="sxs-lookup"><span data-stu-id="37af5-136">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="37af5-137">Samuti on praegu 2016. aasta mai teegis tõlkena saadaval ainult 2016. aasta veebruaris välja antud tegevuse juhised.</span><span class="sxs-lookup"><span data-stu-id="37af5-137">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="37af5-138">Microsoft annab välja värskendatud teegi, mis sisaldab täiendavaid tõlkeid.</span><span class="sxs-lookup"><span data-stu-id="37af5-138">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="37af5-139">Kui tegevusjuhis on tõlgitud, siis kuvatakse tegevusjuhise avamisel kogu selle tekst teie valitud keeles.</span><span class="sxs-lookup"><span data-stu-id="37af5-139">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="37af5-140">Kui tegevusjuhist pole veel tõlgitud, siis kuvatakse tegevusjuhise avamisel teie valitud keeles ainult osa tekstist (juhtelementide tekst).</span><span class="sxs-lookup"><span data-stu-id="37af5-140">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="37af5-141">Kohandatud spikri lisamine</span><span class="sxs-lookup"><span data-stu-id="37af5-141">Adding custom Help</span></span>

<span data-ttu-id="37af5-142">Tegevuse juhiseid saate kasutada kohandatud spikri loomiseks või spikri veebisaidi ühendamiseks paaniga **Spikker**.</span><span class="sxs-lookup"><span data-stu-id="37af5-142">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="37af5-143">Kohandatud spikri loomine tegevuse juhiste abil</span><span class="sxs-lookup"><span data-stu-id="37af5-143">Create custom Help by using task guides</span></span>

<span data-ttu-id="37af5-144">Saate luua oma toetatud rakendustele kohandatud spikri, luues tegevuse salvestised, mis kajastavad teie eksemplari, ja salvestades need LCS-i äriprotsesside teeki.</span><span class="sxs-lookup"><span data-stu-id="37af5-144">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="37af5-145">Rakenduse Human Resources jaoks ei saa te kohandatud tegevuse juhiseid luua.</span><span class="sxs-lookup"><span data-stu-id="37af5-145">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="37af5-146">Kui olete partner ja viite teegi üle ettevõtte teegiks ning lisate selle lahendusse, on see teie klientidele kättesaadav.</span><span class="sxs-lookup"><span data-stu-id="37af5-146">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="37af5-147">Võite teha koopia ka APQC teegist Unified Library ja avada siis tegevuse salvestised selles koopias, redigeerida neid ja salvestada oma muudatused.</span><span class="sxs-lookup"><span data-stu-id="37af5-147">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="37af5-148">Lisateavet vt [Tegevuse salvestaja ressursid](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="37af5-148">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="37af5-149">Kohandatud spikrisaidi ühendamine</span><span class="sxs-lookup"><span data-stu-id="37af5-149">Connect a custom Help site</span></span>

<span data-ttu-id="37af5-150">Finance and Operationsi rakendusi kasutatakse harva nende valmislahenduse kujul.</span><span class="sxs-lookup"><span data-stu-id="37af5-150">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="37af5-151">Selle asemel lahendust kohandatakse ja laiendatakse organisatsiooni vajadustele vastavalt.</span><span class="sxs-lookup"><span data-stu-id="37af5-151">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="37af5-152">Saate kohandada ja laiendada ka spikri kasutuskogemust.</span><span class="sxs-lookup"><span data-stu-id="37af5-152">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="37af5-153">Saate näiteks lisada kohandatud spikri tootesisesele paanile **Spikker**.</span><span class="sxs-lookup"><span data-stu-id="37af5-153">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="37af5-154">Microsoft pakub tööriistakomplekti, mis aitab teil juurutada ja ühendada kohandatud spikrit paanile **Spikker**.</span><span class="sxs-lookup"><span data-stu-id="37af5-154">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="37af5-155">Lisateavet selle kohta, kuidas seadistada kohandatud spikri lahendust, mis oleks ühendatud paaniga **Spikker**, vaadake teemast [Kohandatud spikri ülevaade](../../dev-itpro/help/custom-help-overview.md).</span><span class="sxs-lookup"><span data-stu-id="37af5-155">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="37af5-156">Kui soovite teha Microsoftiga koostööd spikri kohandamiseks vajalike tööriistade ja protsessidega, täitke vorm aadressil [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span><span class="sxs-lookup"><span data-stu-id="37af5-156">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="37af5-157">Vt ka</span><span class="sxs-lookup"><span data-stu-id="37af5-157">See also</span></span>

[<span data-ttu-id="37af5-158">Spikrisüsteem</span><span class="sxs-lookup"><span data-stu-id="37af5-158">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="37af5-159">Kohandatud spikri ülevaade</span><span class="sxs-lookup"><span data-stu-id="37af5-159">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="37af5-160">Tegevuse salvestaja ressursid</span><span class="sxs-lookup"><span data-stu-id="37af5-160">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="37af5-161">Dokumentide või koolituse loomine tegevuse salvestaja abil</span><span class="sxs-lookup"><span data-stu-id="37af5-161">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="37af5-162">Kohandatud spikri GitHubi hoidla</span><span class="sxs-lookup"><span data-stu-id="37af5-162">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  
