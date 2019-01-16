---
title: "Spikrisüsteemi ühendamine"
description: "Selles teemas kirjeldatakse Microsoft Dynamics 365 for Finance and Operationsi spikrisüsteemi komponente ning antakse ülevaade nende ühendamisest ja kokkuvõte kohandatud spikri loomisest."
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 673b01648127fe1d19fb3c75c4d6812c4f22c761
ms.contentlocale: et-ee
ms.lasthandoff: 12/18/2018

---

# <a name="connect-the-help-system"></a><span data-ttu-id="5c868-103">Spikrisüsteemi ühendamine</span><span class="sxs-lookup"><span data-stu-id="5c868-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c868-104">Selles teemas kirjeldatakse Microsoft Dynamics 365 for Finance and Operationsi spikrisüsteemi komponente.</span><span class="sxs-lookup"><span data-stu-id="5c868-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="5c868-105">Antakse ülevaade nende komponentide ühendamisest ning kokkuvõte kohandatud spikri loomisest.</span><span class="sxs-lookup"><span data-stu-id="5c868-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="5c868-106">Spikri arhitektuur</span><span class="sxs-lookup"><span data-stu-id="5c868-106">Help architecture</span></span>

<span data-ttu-id="5c868-107">Järgmisel joonisel on näidatud Finance and Operationsi spikrisüsteemi osad.</span><span class="sxs-lookup"><span data-stu-id="5c868-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="5c868-108">Toote sisespikri süsteem toob artikleid Finance and Operationsi saidilt https://docs.microsoft.com ja tegevusejuhistest, mis on salvestatud teenuse Microsoft Dynamics Lifecycle Services (LCS) äriprotsesside modelleerijasse.</span><span class="sxs-lookup"><span data-stu-id="5c868-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="5c868-109">Joonisel tärniga (\*) märgitud funktsioonid on meil plaanis, kuid pole veel saadaval.</span><span class="sxs-lookup"><span data-stu-id="5c868-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="5c868-110">[![Spikri arhitektuur](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="5c868-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="5c868-111">Spikrisüsteemi ühendamine</span><span class="sxs-lookup"><span data-stu-id="5c868-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="5c868-112">Vahekaart **Tegevusjuhised** pole praegu rakendustes Microsoft Dynamics 365 for Talent ja Microsoft Dynamics 365 for Retail saadaval.</span><span class="sxs-lookup"><span data-stu-id="5c868-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="5c868-113">Tegeleme praegu selle funktsiooni lubamisega mõnes tulevases väljaandes.</span><span class="sxs-lookup"><span data-stu-id="5c868-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="5c868-114">Tegevusjuhised rakenduse Talent jaotises Alustamine jäävad kättesaadavaks, hõlmates põhifunktsioone.</span><span class="sxs-lookup"><span data-stu-id="5c868-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="5c868-115">Protseduurispikker on saadaval ka lehel docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) nii rakenduse Retail kui ka Talent puhul.</span><span class="sxs-lookup"><span data-stu-id="5c868-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>

<span data-ttu-id="5c868-116">Lehel **Süsteemiparameetrid** saavad süsteemiadministraatorid spikrisüsteemi osad juurutamiseks ühendada.</span><span class="sxs-lookup"><span data-stu-id="5c868-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="5c868-117">[![Süsteemi parameetrite vorm koos spikrisätetega](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="5c868-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="5c868-118">Tehke lehel **Süsteemi parameetrid** järgmist.</span><span class="sxs-lookup"><span data-stu-id="5c868-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c868-119">Vahekaardi **Spikker** esmakordsel avamisel peate looma ühenduse elutsükli teenustega.</span><span class="sxs-lookup"><span data-stu-id="5c868-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="5c868-120">Klõpsake kindlasti vormi keskel olevat linki, oodake, kuni ühendus on loodud, sulgege dialoogiboks ja seejärel klõpsake **OK**, et avada **Parameetrite vormid**.</span><span class="sxs-lookup"><span data-stu-id="5c868-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="5c868-121">[![LCS loomiseks](./media/connect-to-lcs-crop-1024x365.png "LCS loomiseks")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="5c868-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="5c868-122">Valige elutsükli teenuste projekt, millega ühendus luua.</span><span class="sxs-lookup"><span data-stu-id="5c868-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="5c868-123">Valige BPM-i teegid (valitud projektis), kust tegevuse salvestised tuua.</span><span class="sxs-lookup"><span data-stu-id="5c868-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>

    - <span data-ttu-id="5c868-124">Finance and Operationsi puhul valige Microsofti sisu jaoks uusim Finance and Operationsi APQC ühendatud teek.</span><span class="sxs-lookup"><span data-stu-id="5c868-124">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span>
    - <span data-ttu-id="5c868-125">Retaili jaoks anname teegi välja lähitulevikus.</span><span class="sxs-lookup"><span data-stu-id="5c868-125">For Retail, we will be releasing a library in the near future.</span></span>
    - <span data-ttu-id="5c868-126">Talenti jaoks pole vaja teeki valida – ühendus õige teegiga on teie eest loodud.</span><span class="sxs-lookup"><span data-stu-id="5c868-126">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span>

3. <span data-ttu-id="5c868-127">Valige BPM-i teekide kuvamise järjekord.</span><span class="sxs-lookup"><span data-stu-id="5c868-127">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="5c868-128">See määrab teekidest pärinevate tegevuse salvestiste kuvamise järjekorra paanil **Spikker**.</span><span class="sxs-lookup"><span data-stu-id="5c868-128">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="5c868-129">Kui olete need toimingud lõpetanud, võite avada paani **Spikker** ja klõpsata vahekaarti **Tegevuse juhised**. Näete nüüd tegevuse juhiseid, mis rakenduvad lehele, millel parajasti Finance and Operationsis olete.</span><span class="sxs-lookup"><span data-stu-id="5c868-129">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations.</span></span> <span data-ttu-id="5c868-130">Kui ühtegi ülesande juhist ei leita, saate sisestada märksõnu otsingu kitsendamiseks.</span><span class="sxs-lookup"><span data-stu-id="5c868-130">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="5c868-131">Tõlgitud tegevusjuhiste kuvamine</span><span class="sxs-lookup"><span data-stu-id="5c868-131">Showing translated task guides</span></span>

<span data-ttu-id="5c868-132">Tõlgitud tegevusjuhised edastati esmakordselt 2016. aasta mai APQC ühendatud teegis ja teegis Alustamine.</span><span class="sxs-lookup"><span data-stu-id="5c868-132">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="5c868-133">Finance and Operationsis lokaliseeritud tegevusjuhise vaatamiseks veenduge, et teil oleks ühendus mai teegiga.</span><span class="sxs-lookup"><span data-stu-id="5c868-133">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="5c868-134">Keelt, milles tegevusjuhis kuvatakse, juhitakse iga kasutaja puhul keelesätetega jaotises **Suvandid** &gt; **Eelistused**.</span><span class="sxs-lookup"><span data-stu-id="5c868-134">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="5c868-135">Kuigi paljud tegevusjuhised on tõlgitud, ei kuva Finance and Operationsi klient praegu tõlgitud tegevusjuhiste nimesid.</span><span class="sxs-lookup"><span data-stu-id="5c868-135">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="5c868-136">Samuti on praegu 2016. aasta mai teegis tõlkena saadaval ainult veebruaris välja antud tegevusjuhised.</span><span class="sxs-lookup"><span data-stu-id="5c868-136">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="5c868-137">Anname välja värskendatud teegi täiendavate tõlgetega.</span><span class="sxs-lookup"><span data-stu-id="5c868-137">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="5c868-138">Kui tegevusjuhis on tõlgitud, siis kuvatakse tegevusjuhise avamisel kogu selle tekst teie valitud keeles.</span><span class="sxs-lookup"><span data-stu-id="5c868-138">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="5c868-139">Kui tegevusjuhist pole veel tõlgitud, siis kuvatakse tegevusjuhise avamisel teie valitud keeles ainult osa tekstist (juhtelementide tekst).</span><span class="sxs-lookup"><span data-stu-id="5c868-139">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="5c868-140">Kohandatud spikri loomine</span><span class="sxs-lookup"><span data-stu-id="5c868-140">Creating custom help</span></span>

<span data-ttu-id="5c868-141">Ülesande juhiseid saate kasutada kohandatud spikri loomiseks või veebisaidi ühendamiseks spikripaaniga.</span><span class="sxs-lookup"><span data-stu-id="5c868-141">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="5c868-142">Kohandatud spikri loomine ülesande juhistega</span><span class="sxs-lookup"><span data-stu-id="5c868-142">Create custom help with task guides</span></span>

<span data-ttu-id="5c868-143">Saate luua oma Finance and Operationsi ja Retaili eksemplarile kohandatud spikri, luues tegevuste salvestised, mis kajastavad teie eksemplari, ja salvestades need LCS-i äriprotsesside teeki.</span><span class="sxs-lookup"><span data-stu-id="5c868-143">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="5c868-144">Kohandatud tegevusjuhiseid ei saa luua Talenti puhul.</span><span class="sxs-lookup"><span data-stu-id="5c868-144">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="5c868-145">Partneritele: kui teete olemasoleva teegi ettevõtte teegiks ja lisate selle lahendusse, on see teie klientidele kättesaadav.</span><span class="sxs-lookup"><span data-stu-id="5c868-145">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="5c868-146">Võite teha koopia ka APQC teegist Unified global library ja avada siis oma eksemplari, avada selle tegevuste salvestised, muuta neid ja salvestada salvestised oma muudatustega.</span><span class="sxs-lookup"><span data-stu-id="5c868-146">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="5c868-147">Lisateavet leiate teemast [Kuidas luua tegevuste salvestisi koolitusel dokumentatsioonina kasutamiseks](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="5c868-147">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="5c868-148">Kohandatud saidi ühendamine</span><span class="sxs-lookup"><span data-stu-id="5c868-148">Connect a custom site</span></span>

<span data-ttu-id="5c868-149">Microsoft pakub tehnilist ülevaadet ja näidiskoodi, mis kirjeldavad kohandatud spikrisaidi loomist ja ühendamist spikripaaniga.</span><span class="sxs-lookup"><span data-stu-id="5c868-149">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="5c868-150">Lisateabe saamiseks vt:</span><span class="sxs-lookup"><span data-stu-id="5c868-150">For more information, see:</span></span>

- [<span data-ttu-id="5c868-151">Kohandatud spikri loomine rakendusele Finance and Operations(tehniline ülevaade)</span><span class="sxs-lookup"><span data-stu-id="5c868-151">Create Custom Help for Finance and Operations (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="5c868-152">Kohandatud spikker – GitHubi hoidla</span><span class="sxs-lookup"><span data-stu-id="5c868-152">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="5c868-153">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="5c868-153">Additional resources</span></span>

[<span data-ttu-id="5c868-154">Spikri ülevaade</span><span class="sxs-lookup"><span data-stu-id="5c868-154">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="5c868-155">Tegevuse salvestaja ülevaade</span><span class="sxs-lookup"><span data-stu-id="5c868-155">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="5c868-156">Kuidas luua tegevuse salvestist dokumentide või koolitusena kasutamiseks</span><span class="sxs-lookup"><span data-stu-id="5c868-156">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)

