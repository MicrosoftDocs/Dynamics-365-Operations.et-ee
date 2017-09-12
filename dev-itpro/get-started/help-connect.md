---
title: "Spikrisüsteemi ühendamine"
description: "Selles teemas kirjeldatakse Microsoft Dynamics 365 for Finance and Operationsi spikrisüsteemi komponente ning antakse ülevaade nende ühendamisest ja kokkuvõte kohandatud spikri loomisest."
author: margoc
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: acb832c422ccb5ddb98d6ddd6b69d2e2c3e11057
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---

# <a name="connect-the-help-system"></a><span data-ttu-id="fe79c-103">Spikrisüsteemi ühendamine</span><span class="sxs-lookup"><span data-stu-id="fe79c-103">Connect the Help system</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fe79c-104">Selles teemas kirjeldatakse Microsoft Dynamics 365 for Finance and Operationsi spikrisüsteemi komponente.</span><span class="sxs-lookup"><span data-stu-id="fe79c-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="fe79c-105">Antakse ülevaade nende komponentide ühendamisest ning kokkuvõte kohandatud spikri loomisest.</span><span class="sxs-lookup"><span data-stu-id="fe79c-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="fe79c-106">Spikri arhitektuur</span><span class="sxs-lookup"><span data-stu-id="fe79c-106">Help architecture</span></span>
<span data-ttu-id="fe79c-107">Järgmisel joonisel on näidatud Finance and Operationsi spikrisüsteemi osad.</span><span class="sxs-lookup"><span data-stu-id="fe79c-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="fe79c-108">Toote sisespikri süsteem toob artikleid Finance and Operationsi saidilt https://docs.microsoft.com ja tegevusejuhistest, mis on salvestatud teenuse Microsoft Dynamics Lifecycle Services (LCS) äriprotsesside modelleerijasse.</span><span class="sxs-lookup"><span data-stu-id="fe79c-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="fe79c-109">Joonisel tärniga (\*) märgitud funktsioonid on meil plaanis, kuid pole veel saadaval.</span><span class="sxs-lookup"><span data-stu-id="fe79c-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="fe79c-110">[![Spikri arhitektuur](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="fe79c-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="fe79c-111">Spikrisüsteemi ühendamine</span><span class="sxs-lookup"><span data-stu-id="fe79c-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="fe79c-112">Vahekaart **Tegevusjuhised** pole praegu rakendustes Microsoft Dynamics 365 for Talent ja Microsoft Dynamics 365 for Retail saadaval.</span><span class="sxs-lookup"><span data-stu-id="fe79c-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="fe79c-113">Tegeleme praegu selle funktsiooni lubamisega mõnes tulevases väljaandes.</span><span class="sxs-lookup"><span data-stu-id="fe79c-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="fe79c-114">Tegevusjuhised rakenduse Talent jaotises Alustamine jäävad kättesaadavaks, hõlmates põhifunktsioone.</span><span class="sxs-lookup"><span data-stu-id="fe79c-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="fe79c-115">Protseduurispikker on saadaval ka lehel docs.microsoft.com site ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)) nii rakenduse Retail kui ka Talent puhul.</span><span class="sxs-lookup"><span data-stu-id="fe79c-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)) for both Retail and Talent.</span></span>
 

<span data-ttu-id="fe79c-116">Lehel **Süsteemiparameetrid** saavad süsteemiadministraatorid spikrisüsteemi osad juurutamiseks ühendada.</span><span class="sxs-lookup"><span data-stu-id="fe79c-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="fe79c-117">[![Süsteemi parameetrite vorm koos spikri sätetega](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Järgige lehel **Süsteemi parameetrid** järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="fe79c-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe79c-118">Vahekaardi **Spikker** esmakordsel avamisel peate looma ühenduse elutsükli teenustega.</span><span class="sxs-lookup"><span data-stu-id="fe79c-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="fe79c-119">Klõpsake kindlasti vormi keskel olevat linki, oodake, kuni ühendus on loodud, sulgege dialoogiboks ja seejärel klõpsake lehe **Süsteemi parameetrid** avamiseks **OK**.[![LCS-iga ühenduse loomine](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="fe79c-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="fe79c-120">Valige elutsükli teenuste projekt, millega ühendus luua.</span><span class="sxs-lookup"><span data-stu-id="fe79c-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="fe79c-121">Valige BPM-i teegid (valitud projektis), kust tegevuse salvestised tuua.</span><span class="sxs-lookup"><span data-stu-id="fe79c-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="fe79c-122">Finance and Operationsi puhul valige Microsofti sisu jaoks 2017. aasta veebruari Microsoft Dynamics 365 for Finance and Operationsi QPC ühendatud teek.</span><span class="sxs-lookup"><span data-stu-id="fe79c-122">For Finance and Operations, for Microsoft content, select the February 2017 QPC Unified Library for Microsoft Dynamics 365 for Finance and Operations.</span></span> 
    - <span data-ttu-id="fe79c-123">Retaili jaoks anname teegi välja juulis.</span><span class="sxs-lookup"><span data-stu-id="fe79c-123">For Retail, we will be releasing a library in July.</span></span> 
    - <span data-ttu-id="fe79c-124">Talenti jaoks pole vaja teeki valida – ühendus õige teegiga on teie eest loodud.</span><span class="sxs-lookup"><span data-stu-id="fe79c-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="fe79c-125">Valige BPM-i teekide kuvamise järjekord.</span><span class="sxs-lookup"><span data-stu-id="fe79c-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="fe79c-126">See määrab teekidest pärinevate tegevuse salvestiste kuvamise järjekorra paanil **Spikker**.</span><span class="sxs-lookup"><span data-stu-id="fe79c-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="fe79c-127">Kui olete need toimingud lõpetanud, võite avada paani **Spikker** ja klõpsata vahekaarti **Tegevuse juhised**.</span><span class="sxs-lookup"><span data-stu-id="fe79c-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab.</span></span> <span data-ttu-id="fe79c-128">Näete nüüd ülesande juhiseid, mis rakenduvad lehele, millel parajasti Finance and Operationsis olete.</span><span class="sxs-lookup"><span data-stu-id="fe79c-128">You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="fe79c-129">Kui ühtegi ülesande juhist ei leita, saate sisestada märksõnu otsingu kitsendamiseks.</span><span class="sxs-lookup"><span data-stu-id="fe79c-129">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="fe79c-130">Tõlgitud tegevusjuhiste kuvamine</span><span class="sxs-lookup"><span data-stu-id="fe79c-130">Showing translated task guides</span></span>

<span data-ttu-id="fe79c-131">Tõlgitud tegevusjuhised edastati esmakordselt 2016. aasta mai APQC ühendatud teegis ja teegis Alustamine.</span><span class="sxs-lookup"><span data-stu-id="fe79c-131">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="fe79c-132">Finance and Operationsis lokaliseeritud tegevusjuhise vaatamiseks veenduge, et teil oleks ühendus mai teegiga.</span><span class="sxs-lookup"><span data-stu-id="fe79c-132">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="fe79c-133">Keelt, milles tegevusjuhis kuvatakse, juhitakse iga kasutaja puhul keelesätetega jaotises **Suvandid** &gt; **Eelistused**.</span><span class="sxs-lookup"><span data-stu-id="fe79c-133">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="fe79c-134">Kuigi paljud tegevusjuhised on tõlgitud, ei kuva Finance and Operationsi klient praegu tõlgitud tegevusjuhiste nimesid.</span><span class="sxs-lookup"><span data-stu-id="fe79c-134">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="fe79c-135">Samuti on praegu 2016. aasta mai teegis tõlkena saadaval ainult veebruaris välja antud tegevusjuhised.</span><span class="sxs-lookup"><span data-stu-id="fe79c-135">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="fe79c-136">Anname välja värskendatud teegi täiendavate tõlgetega.</span><span class="sxs-lookup"><span data-stu-id="fe79c-136">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="fe79c-137">Kui tegevusjuhis on tõlgitud, siis kuvatakse tegevusjuhise avamisel kogu selle tekst teie valitud keeles.</span><span class="sxs-lookup"><span data-stu-id="fe79c-137">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="fe79c-138">Kui tegevusjuhist pole veel tõlgitud, siis kuvatakse tegevusjuhise avamisel teie valitud keeles ainult osa tekstist (juhtelementide tekst).</span><span class="sxs-lookup"><span data-stu-id="fe79c-138">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="fe79c-139">Kohandatud spikri loomine</span><span class="sxs-lookup"><span data-stu-id="fe79c-139">Creating custom help</span></span>
<span data-ttu-id="fe79c-140">Saate luua oma Finance and Operationsi ja Retaili eksemplarile kohandatud spikri, luues tegevuste salvestised, mis kajastavad teie eksemplari, ja salvestades need LCS-i äriprotsesside teeki.</span><span class="sxs-lookup"><span data-stu-id="fe79c-140">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="fe79c-141">Kohandatud tegevusjuhiseid ei saa luua Talenti puhul.</span><span class="sxs-lookup"><span data-stu-id="fe79c-141">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="fe79c-142">Partneritele: kui teete olemasoleva teegi ettevõtte teegiks ja lisate selle lahendusse, on see teie klientidele kättesaadav.</span><span class="sxs-lookup"><span data-stu-id="fe79c-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="fe79c-143">Võite teha koopia ka APQC teegist Unified global library ja avada siis oma eksemplari, avada selle tegevuste salvestised, muuta neid ja salvestada salvestised oma muudatustega.</span><span class="sxs-lookup"><span data-stu-id="fe79c-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="fe79c-144">Lisateavet leiate teemast [Kuidas luua tegevuste salvestisi koolitusel dokumentatsioonina kasutamiseks](../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="fe79c-144">For more information, see [How to create a task recording to use as documentation or training](../user-interface/task-recorder.md).</span></span>

<a name="see-also"></a><span data-ttu-id="fe79c-145">Vt ka</span><span class="sxs-lookup"><span data-stu-id="fe79c-145">See also</span></span>
--------

[<span data-ttu-id="fe79c-146">Spikri ülevaade</span><span class="sxs-lookup"><span data-stu-id="fe79c-146">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="fe79c-147">Tegevuse salvestaja ülevaade</span><span class="sxs-lookup"><span data-stu-id="fe79c-147">Task recorder overview</span></span>](../user-interface/task-recorder.md)

[<span data-ttu-id="fe79c-148">Kuidas luua tegevuse salvestist dokumentide või koolitusena kasutamiseks</span><span class="sxs-lookup"><span data-stu-id="fe79c-148">How to create a task recording to use as documentation or training</span></span>](../user-interface/task-recorder-training-docs.md)





