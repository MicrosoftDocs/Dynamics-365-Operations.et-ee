---
title: Rakenduse Attract laiendatavus
description: "See teema kirjeldab, kuidas Microsofti Power Platformiga on võimalik laiendada Microsoft Dynamics 365 for Talent - Attract rakendust."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: b589a6ce02cdc02436e256f9e81346fe8b766687
ms.openlocfilehash: d9e1dd3a67c5f64b5d05f0f171226085138e0b44
ms.contentlocale: et-ee
ms.lasthandoff: 11/12/2018

---

# <a name="extensibility-in-attract"></a><span data-ttu-id="c3521-103">Rakenduse Attract laiendatavus</span><span class="sxs-lookup"><span data-stu-id="c3521-103">Extensibility in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c3521-104">Microsoft Dynamics 365 for Talent on ehitatud lahenduse Common Data Service (CDS) for Apps platvormile ning seda on võimalik mitmel viisil laiendada, kasutades Microsofti Power Platformi ja lahenduse Common Data Service for Apps võimalusi.</span><span class="sxs-lookup"><span data-stu-id="c3521-104">Microsoft Dynamics 365 for Talent is built on top of the Common Data Service (CDS) for Apps platform, and can be extended in various ways by using the Microsoft Power Platform and the capabilities that Common Data Service for Apps offers.</span></span> <span data-ttu-id="c3521-105">Seega saate süsteemi konfigureerida ja isikupärastada, kasutades Microsoft PowerAppsi ja Microsoft Flow'd.</span><span class="sxs-lookup"><span data-stu-id="c3521-105">Therefore, you can configure and personalize the system by using Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="c3521-106">Microsoft Power BI-ga saate ka inimeste kohta täiendavat analüütikat koguda.</span><span class="sxs-lookup"><span data-stu-id="c3521-106">You can also get additional analytics about people by using Microsoft Power BI.</span></span> <span data-ttu-id="c3521-107">Lisaks muudavad uued kohandatud tegevused nagu PowerAppsi ja veebisisu (iFrame'i) tegevused värbamisprotsessi kohandatavamaks kui kunagi varem.</span><span class="sxs-lookup"><span data-stu-id="c3521-107">Furthermore, new custom activities, such as the PowerApps and Web content (iframe) activities, make the hiring process more adaptable than ever.</span></span> <span data-ttu-id="c3521-108">Nende tegevuste abil saate kohandada värbamisprotsessi vastavalt oma ettevõtte vajadustele ja protsessidele ning veenduda, et nii värbamismeeskond kui ka kandidaadid saavad sujuva, kohandatud kogemuse osaliseks.</span><span class="sxs-lookup"><span data-stu-id="c3521-108">By using these activities, you can tailor the hiring process to your business needs and processes, and can make sure that both the hiring team and candidates have a seamless, customized experience.</span></span>

## <a name="take-advantage-of-the-microsoft-power-platform"></a><span data-ttu-id="c3521-109">Kasutage Microsofti Power platformi ära.</span><span class="sxs-lookup"><span data-stu-id="c3521-109">Take advantage of the Microsoft Power platform</span></span> 

<span data-ttu-id="c3521-110">Kuna kõik rakenduse Attract andmed asvuad lahenduses Common Data Service for Apps, saate oma ainulaadsete ärivajaduste Attracti kaasamiseks kasutada Microsofti Power platformi tööriistu.</span><span class="sxs-lookup"><span data-stu-id="c3521-110">Because all the data from Attract resides in Common Data Service for Apps, you can use tools from the Microsoft Power platform to incorporate your unique business needs into Attract.</span></span>

### <a name="powerapps"></a><span data-ttu-id="c3521-111">PowerApps</span><span class="sxs-lookup"><span data-stu-id="c3521-111">PowerApps</span></span>

<span data-ttu-id="c3521-112">PowerAppsi abil saate hõlpsasti luua rakendusi, mis loovad ühenduse teie Attract andmetega ja kasutavad loogika lisamiseks Microsoft Exceli avaldisi.</span><span class="sxs-lookup"><span data-stu-id="c3521-112">You can use PowerApps to easily build apps that connect to your Attract data, and that use expressions like the expressions in Microsoft Excel to add logic.</span></span> <span data-ttu-id="c3521-113">PowerAppsiga loodud rakendused töötavad nii veebis kui ka Apple iOS-is ja Google Android seadmetel.</span><span class="sxs-lookup"><span data-stu-id="c3521-113">Apps that you build by using PowerApps can run on the web, and on Apple iOS and Google Android devices.</span></span>

<span data-ttu-id="c3521-114">Näiteks saate ülikoolide karjäärimessid värbajate jaoks lihtsamaks muuta, luues kergema rakenduse, mis võimaldab värbajatel CV-sid skannida ja rakenduses Attract kandidaate ametipositsioonidele esitada.</span><span class="sxs-lookup"><span data-stu-id="c3521-114">For example, you can make university career fairs easier for recruiters by building a lightweight app that lets them scan resumes and feed candidates to a position in Attract.</span></span> <span data-ttu-id="c3521-115">Teise võimalusena võite luua rakenduse, mis aitab rahuldada teie ettevõtte vastavause vajadusi.</span><span class="sxs-lookup"><span data-stu-id="c3521-115">Alternatively, you can build an app that helps meet your organization's compliance needs.</span></span> <span data-ttu-id="c3521-116">Lisateavet PowerAppsi ja selle abil rakenduste loomise kohta vt [Andmete integreerimine lahendusse Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps).</span><span class="sxs-lookup"><span data-stu-id="c3521-116">For more information about PowerApps and how to use it to build apps, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps).</span></span>

### <a name="microsoft-flow"></a><span data-ttu-id="c3521-117">Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="c3521-117">Microsoft Flow</span></span> 

<span data-ttu-id="c3521-118">Saate kasutada Microsoft Flowd automaatsete töövoogude loomiseks, mis töötavad rakenduse Attract andmetel.</span><span class="sxs-lookup"><span data-stu-id="c3521-118">You can use Microsoft Flow to create automated workflows that run on top of Attract data.</span></span> <span data-ttu-id="c3521-119">Saate hõlpsalt luua ühenduse sadade populaarsete rakenduste ja teenustega, ilma et peaksite koodi kirjutama.</span><span class="sxs-lookup"><span data-stu-id="c3521-119">You can easily connect to hundreds of popular apps and services without having to write code.</span></span> <span data-ttu-id="c3521-120">Luues teenuses Common Data Service for Apps vooge, mis suhtlevad rakendustega Attract Job, Candidate ja Application, saate automatiseerida mitmesuguseid toiminguid.</span><span class="sxs-lookup"><span data-stu-id="c3521-120">By building flows that interact with the Attract Job, Candidate, and Application entities in Common Data Service for Apps, you can automate various actions.</span></span> <span data-ttu-id="c3521-121">Näiteks kui kandidaat võtab pakkumise vastu, võib saata teatise värbamismeeskonnale, või võib uudisest teavitada ka Twitteris.</span><span class="sxs-lookup"><span data-stu-id="c3521-121">For example, when a candidate accepts an offer, a notification can be sent to an onboarding team, or the news can be announced on Twitter.</span></span> <span data-ttu-id="c3521-122">Voogude kohta lisateabe saamiseks vt [Microsoft Flow dokumentatsiooni](https://docs.microsoft.com/en-us/flow/).</span><span class="sxs-lookup"><span data-stu-id="c3521-122">For more information about flows, see the [Microsoft Flow documentation](https://docs.microsoft.com/en-us/flow/).</span></span>

### <a name="power-bi"></a><span data-ttu-id="c3521-123">Power BI</span><span class="sxs-lookup"><span data-stu-id="c3521-123">Power BI</span></span>

<span data-ttu-id="c3521-124">Power BI võimaldab teil koostada ja vaadata kohandatud aruandeid ja arumatuurlaudu, mis annavad teile sügavama ülevaate teie rakenduse Attract andmetest.</span><span class="sxs-lookup"><span data-stu-id="c3521-124">Power BI lets you build and view custom reports and dashboards that give you deeper insight into your Attract data.</span></span> <span data-ttu-id="c3521-125">Lisateavet Power BI ja interaktiivsete aruannete ning armatuurlaudade loomise kohta vt [Power BI dokumentatsioonist](https://docs.microsoft.com/en-us/power-bi/).</span><span class="sxs-lookup"><span data-stu-id="c3521-125">For more information about Power BI and how to build interactive reports and dashboards, see the [Power BI documentation](https://docs.microsoft.com/en-us/power-bi/).</span></span>

### <a name="custom-activities"></a><span data-ttu-id="c3521-126">Kohandatud tegevused</span><span class="sxs-lookup"><span data-stu-id="c3521-126">Custom activities</span></span> 

<span data-ttu-id="c3521-127">Saate lisada kohandatud tegevusi (nt PowerApps ja veebisisu (iFrame'i) tegevusi) tööprotsessi malli tasemel või uue töö loomisel.</span><span class="sxs-lookup"><span data-stu-id="c3521-127">You can add custom activities, such as the PowerApps apps and Web content (iframe) activities, at the level of the job process template or while you're creating a new job.</span></span> <span data-ttu-id="c3521-128">Need tegevused võimaldavad teil kohandada värbamisprotsessi ja tuua organisatsiooni ainulaadse äriloogika rakendusse Attract.</span><span class="sxs-lookup"><span data-stu-id="c3521-128">These activities let you customize the hiring process and bring business logic that is unique to your organization into Attract.</span></span>

#### <a name="powerapps-activity"></a><span data-ttu-id="c3521-129">PowerAppsi tegevus</span><span class="sxs-lookup"><span data-stu-id="c3521-129">PowerApps activity</span></span> 

<span data-ttu-id="c3521-130">PowerApps tegevus võimaldab töö või tööportsessi malli loojal PowerAppsi rakenduse värbamisvoogu kaasata.</span><span class="sxs-lookup"><span data-stu-id="c3521-130">The PowerApps activity lets the creator of a job or job process template embed a PowerApps app in the hiring flow.</span></span> <span data-ttu-id="c3521-131">Pärast rakenduse loomist ja avaldamist saate selle rakenduse ID sisestada tegevuse konfiguratsioonidesse.</span><span class="sxs-lookup"><span data-stu-id="c3521-131">After you create and publish the app, you can enter its app ID in the activity configurations.</span></span> <span data-ttu-id="c3521-132">PowerApps rakendust kasutades saate lugeda ja kirjutada andmeid teenusesse Common Data Service for Apps.</span><span class="sxs-lookup"><span data-stu-id="c3521-132">By using a PowerApps app, you can read and write data into Common Data Service for Apps.</span></span> <span data-ttu-id="c3521-133">Saate rakenduse isegi vooga siduda.</span><span class="sxs-lookup"><span data-stu-id="c3521-133">You can even link the app to a flow.</span></span> <span data-ttu-id="c3521-134">Näiteks on teil rakendus, mida värbajad kasutavad telefoniintervjuude ajal vormi täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="c3521-134">For example, you have an app that recruiters use to fill in a form while they conduct phone interviews.</span></span> <span data-ttu-id="c3521-135">Sellisel juhul saate linkida rakenduse vooga, mis hindab, kas kandidaadiga saab kandideerimisprotsessis edasi liikuda.</span><span class="sxs-lookup"><span data-stu-id="c3521-135">In this case, you can link the app to a flow that evaluates whether an applicant can be advanced further in the job application process.</span></span> <span data-ttu-id="c3521-136">Sellist tüüpi tegevusi näevad vaid värbamismeeskonna liikmed.</span><span class="sxs-lookup"><span data-stu-id="c3521-136">This type of activity can be viewed only by members of the hiring team.</span></span> <span data-ttu-id="c3521-137">Lisateabe saamiseks PowerAppsi tegevuste konfigureerimise kohta vt [Tegevused rakenduses Attract](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="c3521-137">For more information about how to configure the PowerApps activity, see [Activities in Attract](./activities-attract.md).</span></span>

> [!NOTE]
> <span data-ttu-id="c3521-138">Tegevus PowerApps on saadaval ainult tervikliku värbamise lisandmooduli korral.</span><span class="sxs-lookup"><span data-stu-id="c3521-138">The PowerApps activity is available only with the Comprehensive hiring add-on.</span></span>

#### <a name="web-content-iframe-activity"></a><span data-ttu-id="c3521-139">Veebisisu (iFrame'i) tegevus</span><span class="sxs-lookup"><span data-stu-id="c3521-139">Web content (iframe) activity</span></span>

<span data-ttu-id="c3521-140">Veebisisu (IFRAME'i) tegevus võimaldab teil kaasatada kohandatud veebilahenduse, mille olete loonud värbamisprotsessis või kandidaadi portaalis.</span><span class="sxs-lookup"><span data-stu-id="c3521-140">The Web content (iframe) activity lets you embed a custom web solution that you've built in the hiring process or the Candidate portal.</span></span> <span data-ttu-id="c3521-141">Saate lugeda ja kirjutada andmeid vahetult teenusest Common Data Service for Apps.</span><span class="sxs-lookup"><span data-stu-id="c3521-141">You can read and write data directly from Common Data Service for Apps.</span></span> <span data-ttu-id="c3521-142">Lisaks saate kohandada lahenduse nii, et see käivitab voogusid või kasutab ära Microsoft Azure'i funktsioone.</span><span class="sxs-lookup"><span data-stu-id="c3521-142">You can also customize the solution so that it triggers flows or takes advantage of Microsoft Azure functions.</span></span> <span data-ttu-id="c3521-143">Lisateabe saamiseks veebisisu tegevuste konfigureerimise kohta vt [Tegevused rakenduses Attract](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="c3521-143">For more information about how to configure the Web content activity, see [Activities in Attract](./activities-attract.md).</span></span>

> [!NOTE]
> <span data-ttu-id="c3521-144">Tegevus Veebisisu on saadaval ainult tervikliku värbamise lisandmooduli korral.</span><span class="sxs-lookup"><span data-stu-id="c3521-144">The Web content activity is available only with the Comprehensive hiring add-on.</span></span>
