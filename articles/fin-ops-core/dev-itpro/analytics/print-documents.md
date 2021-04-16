---
title: Dokumentide printimise ülevaade
description: Saate printida dokumente kohaliku printeri või võrku ühendatud seadme abil. See artikkel annab ülevaate dokumentide printimisest.
author: RichdiMSFT
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d41e299f0076e1016e8ddae8584bfec338a73a9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749389"
---
# <a name="document-printing-overview"></a><span data-ttu-id="4f759-104">Dokumentide printimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="4f759-104">Document printing overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f759-105">Saate printida dokumente kohaliku printeri või võrku ühendatud seadme abil.</span><span class="sxs-lookup"><span data-stu-id="4f759-105">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="4f759-106">See artikkel annab ülevaate dokumentide printimisest.</span><span class="sxs-lookup"><span data-stu-id="4f759-106">This article provides an overview of how documents are printed.</span></span>

## <a name="printing-overview"></a><span data-ttu-id="4f759-107">Printimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="4f759-107">Printing overview</span></span>

<span data-ttu-id="4f759-108">Rakendus pakub integreeritud teenuseid ja klientrakendusi, mis võimaldavad hõlpsalt luua, salvestada ning levitada äritegevust toetavaid dokumente.</span><span class="sxs-lookup"><span data-stu-id="4f759-108">The application provides integrated services and client applications that make it easy to generate, store, and distribute documents that support business activity.</span></span> <span data-ttu-id="4f759-109">Saate printida dokumente kohaliku printeri või võrku ühendatud seadme abil.</span><span class="sxs-lookup"><span data-stu-id="4f759-109">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="4f759-110">Peale selle saate eksportida lehti ja aruandeid otse kliendist kas PDF-failide või Microsoft Office’i dokumentidena.</span><span class="sxs-lookup"><span data-stu-id="4f759-110">In addition, you can export pages and reports directly from the client, as PDF files or Microsoft Office documents.</span></span> <span data-ttu-id="4f759-111">Lõpuks võimaldab jaotatud töökoormus teil printida äridokumente otse mobiilsest seadmest, kasutades võrguressursse.</span><span class="sxs-lookup"><span data-stu-id="4f759-111">Finally, the distributed workload lets you print business documents directly from a mobile device by using network resources.</span></span> <span data-ttu-id="4f759-112">Kuigi printimisnõuded võivad erineda, peavad kõik valdkonnad tavaliselt äridokumentidest rakenduse abil looma paberdokumendid.</span><span class="sxs-lookup"><span data-stu-id="4f759-112">Although printing requirements might vary, all industries typically must create hard copies of business documents by using the application.</span></span> <span data-ttu-id="4f759-113">Dokumentide printimine võrgusseadmetes hostitud rakendustest toob kaasa ainulaadsed probleemid.</span><span class="sxs-lookup"><span data-stu-id="4f759-113">Printing documents on network devices from hosted applications presents a unique set of challenges.</span></span> <span data-ttu-id="4f759-114">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="4f759-114">Here are some examples:</span></span>

- <span data-ttu-id="4f759-115">Printeridraiverid ei pruugi kasutaja seadmes saadaval olla.</span><span class="sxs-lookup"><span data-stu-id="4f759-115">Print drivers might not be available on the user's device.</span></span>
- <span data-ttu-id="4f759-116">Kasutaja seade ei pruugi olla ettevõtte võrguga ühendatud.</span><span class="sxs-lookup"><span data-stu-id="4f759-116">The user's device might not be connected to the corporate network.</span></span>

<span data-ttu-id="4f759-117">Spetsiaalse hosti abil ja paari lihtsat etappi järgides saavad süsteemiadministraatorid konfigureerida juurutusi, mis võimaldavad kasutajatel printida võrguseadmetes otse ärirakendustest.</span><span class="sxs-lookup"><span data-stu-id="4f759-117">By using a dedicated host and following a few easy steps, system administrators can configure deployments so that users can print directly from business applications on network devices.</span></span>

### <a name="application-printing-scenarios"></a><span data-ttu-id="4f759-118">Rakenduse printimise stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="4f759-118">Application printing scenarios</span></span> 

<span data-ttu-id="4f759-119">Järgmine tabel kirjeldab kolme esmase printimise stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="4f759-119">The following table describes the three primary printing scenarios.</span></span>

| <span data-ttu-id="4f759-120">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="4f759-120">Scenario</span></span>                        | <span data-ttu-id="4f759-121">Eesmärk</span><span class="sxs-lookup"><span data-stu-id="4f759-121">Goal</span></span>                                                      | <span data-ttu-id="4f759-122">Lahendus</span><span class="sxs-lookup"><span data-stu-id="4f759-122">Solution</span></span> |
|---------------------------------|-----------------------------------------------------------|----------|
| <span data-ttu-id="4f759-123">1. Kuvatava printimine</span><span class="sxs-lookup"><span data-stu-id="4f759-123">1. Printing what you see</span></span>        | <span data-ttu-id="4f759-124">Saate printida seda, mida praegu brauseris kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="4f759-124">Print what is currently shown in the browser.</span></span>             | <span data-ttu-id="4f759-125">Brauseris luuakse veebilehe prinditav versioon.</span><span class="sxs-lookup"><span data-stu-id="4f759-125">A "print-friendly" version of the webpage is generated for the browser.</span></span> |
| <span data-ttu-id="4f759-126">2. Interaktiivne printimine</span><span class="sxs-lookup"><span data-stu-id="4f759-126">2. Interactive printing</span></span>         | <span data-ttu-id="4f759-127">Saate printida täppisdokumendi kohalikult ühendatud seadmest.</span><span class="sxs-lookup"><span data-stu-id="4f759-127">Print a precision document on a locally connected device.</span></span> | <span data-ttu-id="4f759-128">Saate eksportida aruande PDF-versiooni ja selle brauseris alla laadida.</span><span class="sxs-lookup"><span data-stu-id="4f759-128">You can export a PDF version of the report and download it to the browser.</span></span> |
| <span data-ttu-id="4f759-129">3. Printimine võrgusseadmes</span><span class="sxs-lookup"><span data-stu-id="4f759-129">3. Printing on a network device</span></span> | <span data-ttu-id="4f759-130">Saate saata täppisdokumendi domeeni printerisse.</span><span class="sxs-lookup"><span data-stu-id="4f759-130">Send a precision document to a domain printer device.</span></span>     | <span data-ttu-id="4f759-131">Täppisdokument saadetakse klientrakendusele, mis töötab kliendi domeenis hostitavas serveris.</span><span class="sxs-lookup"><span data-stu-id="4f759-131">A precision document is sent to a client application that runs on a server that is hosted in the customer's domain.</span></span> |

<span data-ttu-id="4f759-132">Kuna lahendused on erinevad olenevalt stsenaariumist, pakuvad rakendused sisseehitatud teenuseid ja tööriistu, mis aitavad kasutajatel saavutada oma eesmärke:</span><span class="sxs-lookup"><span data-stu-id="4f759-132">Because the solution varies, depending on the scenario, applications provide built-in services and tooling to help users accomplish their goals:</span></span>

- <span data-ttu-id="4f759-133">**1. stsenaariumi** toetab HTML5 kliendi brauseri renderdus.</span><span class="sxs-lookup"><span data-stu-id="4f759-133">**Scenario 1** is supported by the browser's rendering of the HTML5 client.</span></span>
- <span data-ttu-id="4f759-134">**2. stsenaarium** kasutab klientrakendusi ja Microsoft 365 teenuseid.</span><span class="sxs-lookup"><span data-stu-id="4f759-134">**Scenario 2** uses client applications and Microsoft 365 services.</span></span>
- <span data-ttu-id="4f759-135">**3. stsenaarium** nõuab tuge klientrakendustest ja teenustest, mida hostitakse Microsoft Azure’is.</span><span class="sxs-lookup"><span data-stu-id="4f759-135">**Scenario 3** requires support from client applications and from services that are hosted in Microsoft Azure.</span></span>

<span data-ttu-id="4f759-136">Lisaks platvormile, mis juurutatakse Azure’i tellimusse, pakuvad Finance and Operationsi rakendused klientidele integreeritud, esimese osapoole Azure’i rakendust, mis aitab neil printimiseks hõlpsamalt kasutada domeenis hostitud seadmeid.</span><span class="sxs-lookup"><span data-stu-id="4f759-136">In addition to the platform that is deployed to the Azure subscription, Finance and Operations applications provide customers with an integrated, first-party Azure application that helps them more easily use domain-hosted devices to print documents.</span></span>

## <a name="service-overview"></a><span data-ttu-id="4f759-137">Hoolduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="4f759-137">Service overview</span></span>
<span data-ttu-id="4f759-138">Ajal, mil hostitud rakenduste loodud dokmendid ootavad printimist võrku ühendatud seadmes, talletatakse neid Azure’i bloobimälus.</span><span class="sxs-lookup"><span data-stu-id="4f759-138">While documents that are produced by the hosted applications are waiting to be printed on a network-connected device, they are stored in Azure blob storage.</span></span> <span data-ttu-id="4f759-139">[Dokumendi marsruudivaliku agendi installimine võrguprintimise lubamiseks](install-document-routing-agent.md) kasutab Azure’i autentimist, et luua turvaline kanal Azure’i teenustega.</span><span class="sxs-lookup"><span data-stu-id="4f759-139">The [Install the Document Routing Agent to enable network printing](install-document-routing-agent.md) uses Azure authentication to establish a secure channel to the Azure services.</span></span>

<span data-ttu-id="4f759-140">**Käivitamisjärjekord**</span><span class="sxs-lookup"><span data-stu-id="4f759-140">**Execution sequence**</span></span>

1. <span data-ttu-id="4f759-141">Teenus Microsoft SQL Server Reporting Services (SSRS) loob aruande, mis talletatakse Azure’i bloobimälus.</span><span class="sxs-lookup"><span data-stu-id="4f759-141">The report is generated by Microsoft SQL Server Reporting Services (SSRS) and stored in Azure blob storage.</span></span> <span data-ttu-id="4f759-142">Seotud printerisätteid talletatakse koos dokumendiga.</span><span class="sxs-lookup"><span data-stu-id="4f759-142">Attached printer settings are stored together with the document.</span></span>
2. <span data-ttu-id="4f759-143">Dokumendi marsruudivaliku agent esitab Azure’i teenusesiini järjekorda aktiivsete tööde päringu.</span><span class="sxs-lookup"><span data-stu-id="4f759-143">The Document Routing Agent queries the Azure Service Bus queue for active jobs.</span></span>
3. <span data-ttu-id="4f759-144">Dokumendi marsruudivaliku agent laadib dokumendi alla ja spuulib selle võrguprinterisse.</span><span class="sxs-lookup"><span data-stu-id="4f759-144">The document is downloaded by the Document Routing Agent and spooled to the network printer.</span></span>

<span data-ttu-id="4f759-145">Kliendipõhine lahendus võimaldab klientidel hallata oma printimisvajaduste ulatust.</span><span class="sxs-lookup"><span data-stu-id="4f759-145">The client-based solution lets customers manage the scale of their printing needs.</span></span> <span data-ttu-id="4f759-146">Kliendid, kellel on suuremahulised printimise töökoormused, saavad installida mitu dokumendi marsruudivaliku agenti, et suurendada samaaegsete printimistoimingute arvu.</span><span class="sxs-lookup"><span data-stu-id="4f759-146">Customers who have heavy-volume printing workloads can install many Document Routing Agents to increase the number of concurrent printing operations.</span></span> <span data-ttu-id="4f759-147">Samuti võib mõnel kliendil olla vajalik ainult väga väheste dokumendi marsruudivaliku agentide installimine, et täita nende printimisvajadusi.</span><span class="sxs-lookup"><span data-stu-id="4f759-147">Alternatively, some customers require very few installations of the Document Routing Agent to handle their anticipated printing needs.</span></span>

### <a name="service-components-for-network-printing"></a><span data-ttu-id="4f759-148">Võrguprintimise teenusekomponendid</span><span class="sxs-lookup"><span data-stu-id="4f759-148">Service components for network printing</span></span>

<span data-ttu-id="4f759-149">Järgmisel diagrammil on näidatud põhikomponendid, mis toetavad võrguprintimise toiminguid.</span><span class="sxs-lookup"><span data-stu-id="4f759-149">The following diagram shows the basic components that help support network printing operations.</span></span>

<span data-ttu-id="4f759-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span><span class="sxs-lookup"><span data-stu-id="4f759-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span></span>

<span data-ttu-id="4f759-151">Pange tähele, et ühe printeri juurde saab registreerida mitu dokumendi marsruudivaliku agenti.</span><span class="sxs-lookup"><span data-stu-id="4f759-151">Note that a single printer can be registered with multiple Document Routing Agents.</span></span> <span data-ttu-id="4f759-152">Printimiseelistuste lahendamiseks kasutab hostitud teenus võrguteed, mis tuvastab kordumatult iga võrguprinteri.</span><span class="sxs-lookup"><span data-stu-id="4f759-152">To resolve the printer preferences, the hosted service uses the network path that uniquely identifies every network printer.</span></span> <span data-ttu-id="4f759-153">Sellest tulenevalt kuvatakse printer ka siis, kui selle on registreerinud mitu klienti, rakenduste saadaolevate printerite loendis ühe valikuna.</span><span class="sxs-lookup"><span data-stu-id="4f759-153">As a result, even when a printer is registered by multiple clients, it appears as a single selection in the list of printers available in applications.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]