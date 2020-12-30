---
title: Dokumentide printimise ülevaade
description: Saate printida dokumente kohaliku printeri või võrku ühendatud seadme abil. See artikkel annab ülevaate dokumentide printimisest.
author: TJVass
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1d64a2efeade5e9ba24f4dfe61c861f5a4cbad4
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680092"
---
# <a name="document-printing-overview"></a><span data-ttu-id="13dba-104">Dokumentide printimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="13dba-104">Document printing overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13dba-105">Saate printida dokumente kohaliku printeri või võrku ühendatud seadme abil.</span><span class="sxs-lookup"><span data-stu-id="13dba-105">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="13dba-106">See artikkel annab ülevaate dokumentide printimisest.</span><span class="sxs-lookup"><span data-stu-id="13dba-106">This article provides an overview of how documents are printed.</span></span>

## <a name="printing-overview"></a><span data-ttu-id="13dba-107">Printimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="13dba-107">Printing overview</span></span>

<span data-ttu-id="13dba-108">Rakendus pakub integreeritud teenuseid ja klientrakendusi, mis võimaldavad hõlpsalt luua, salvestada ning levitada äritegevust toetavaid dokumente.</span><span class="sxs-lookup"><span data-stu-id="13dba-108">The application provides integrated services and client applications that make it easy to generate, store, and distribute documents that support business activity.</span></span> <span data-ttu-id="13dba-109">Saate printida dokumente kohaliku printeri või võrku ühendatud seadme abil.</span><span class="sxs-lookup"><span data-stu-id="13dba-109">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="13dba-110">Peale selle saate eksportida lehti ja aruandeid otse kliendist kas PDF-failide või Microsoft Office’i dokumentidena.</span><span class="sxs-lookup"><span data-stu-id="13dba-110">In addition, you can export pages and reports directly from the client, as PDF files or Microsoft Office documents.</span></span> <span data-ttu-id="13dba-111">Lõpuks võimaldab jaotatud töökoormus teil printida äridokumente otse mobiilsest seadmest, kasutades võrguressursse.</span><span class="sxs-lookup"><span data-stu-id="13dba-111">Finally, the distributed workload lets you print business documents directly from a mobile device by using network resources.</span></span> <span data-ttu-id="13dba-112">Kuigi printimisnõuded võivad erineda, peavad kõik valdkonnad tavaliselt äridokumentidest rakenduse abil looma paberdokumendid.</span><span class="sxs-lookup"><span data-stu-id="13dba-112">Although printing requirements might vary, all industries typically must create hard copies of business documents by using the application.</span></span> <span data-ttu-id="13dba-113">Dokumentide printimine võrgusseadmetes hostitud rakendustest toob kaasa ainulaadsed probleemid.</span><span class="sxs-lookup"><span data-stu-id="13dba-113">Printing documents on network devices from hosted applications presents a unique set of challenges.</span></span> <span data-ttu-id="13dba-114">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="13dba-114">Here are some examples:</span></span>

- <span data-ttu-id="13dba-115">Printeridraiverid ei pruugi kasutaja seadmes saadaval olla.</span><span class="sxs-lookup"><span data-stu-id="13dba-115">Print drivers might not be available on the user's device.</span></span>
- <span data-ttu-id="13dba-116">Kasutaja seade ei pruugi olla ettevõtte võrguga ühendatud.</span><span class="sxs-lookup"><span data-stu-id="13dba-116">The user's device might not be connected to the corporate network.</span></span>

<span data-ttu-id="13dba-117">Spetsiaalse hosti abil ja paari lihtsat etappi järgides saavad süsteemiadministraatorid konfigureerida juurutusi, mis võimaldavad kasutajatel printida võrguseadmetes otse ärirakendustest.</span><span class="sxs-lookup"><span data-stu-id="13dba-117">By using a dedicated host and following a few easy steps, system administrators can configure deployments so that users can print directly from business applications on network devices.</span></span>

### <a name="application-printing-scenarios"></a><span data-ttu-id="13dba-118">Rakenduse printimise stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="13dba-118">Application printing scenarios</span></span> 

<span data-ttu-id="13dba-119">Järgmine tabel kirjeldab kolme esmase printimise stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="13dba-119">The following table describes the three primary printing scenarios.</span></span>

| <span data-ttu-id="13dba-120">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="13dba-120">Scenario</span></span>                        | <span data-ttu-id="13dba-121">Eesmärk</span><span class="sxs-lookup"><span data-stu-id="13dba-121">Goal</span></span>                                                      | <span data-ttu-id="13dba-122">Lahendus</span><span class="sxs-lookup"><span data-stu-id="13dba-122">Solution</span></span> |
|---------------------------------|-----------------------------------------------------------|----------|
| <span data-ttu-id="13dba-123">1. Kuvatava printimine</span><span class="sxs-lookup"><span data-stu-id="13dba-123">1. Printing what you see</span></span>        | <span data-ttu-id="13dba-124">Saate printida seda, mida praegu brauseris kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="13dba-124">Print what is currently shown in the browser.</span></span>             | <span data-ttu-id="13dba-125">Brauseris luuakse veebilehe prinditav versioon.</span><span class="sxs-lookup"><span data-stu-id="13dba-125">A "print-friendly" version of the webpage is generated for the browser.</span></span> |
| <span data-ttu-id="13dba-126">2. Interaktiivne printimine</span><span class="sxs-lookup"><span data-stu-id="13dba-126">2. Interactive printing</span></span>         | <span data-ttu-id="13dba-127">Saate printida täppisdokumendi kohalikult ühendatud seadmest.</span><span class="sxs-lookup"><span data-stu-id="13dba-127">Print a precision document on a locally connected device.</span></span> | <span data-ttu-id="13dba-128">Saate eksportida aruande PDF-versiooni ja selle brauseris alla laadida.</span><span class="sxs-lookup"><span data-stu-id="13dba-128">You can export a PDF version of the report and download it to the browser.</span></span> |
| <span data-ttu-id="13dba-129">3. Printimine võrgusseadmes</span><span class="sxs-lookup"><span data-stu-id="13dba-129">3. Printing on a network device</span></span> | <span data-ttu-id="13dba-130">Saate saata täppisdokumendi domeeni printerisse.</span><span class="sxs-lookup"><span data-stu-id="13dba-130">Send a precision document to a domain printer device.</span></span>     | <span data-ttu-id="13dba-131">Täppisdokument saadetakse klientrakendusele, mis töötab kliendi domeenis hostitavas serveris.</span><span class="sxs-lookup"><span data-stu-id="13dba-131">A precision document is sent to a client application that runs on a server that is hosted in the customer's domain.</span></span> |

<span data-ttu-id="13dba-132">Kuna lahendused on erinevad olenevalt stsenaariumist, pakuvad rakendused sisseehitatud teenuseid ja tööriistu, mis aitavad kasutajatel saavutada oma eesmärke:</span><span class="sxs-lookup"><span data-stu-id="13dba-132">Because the solution varies, depending on the scenario, applications provide built-in services and tooling to help users accomplish their goals:</span></span>

- <span data-ttu-id="13dba-133">**1. stsenaariumi** toetab HTML5 kliendi brauseri renderdus.</span><span class="sxs-lookup"><span data-stu-id="13dba-133">**Scenario 1** is supported by the browser's rendering of the HTML5 client.</span></span>
- <span data-ttu-id="13dba-134">**2. stsenaarium** kasutab klientrakendusi ja Microsoft 365 teenuseid.</span><span class="sxs-lookup"><span data-stu-id="13dba-134">**Scenario 2** uses client applications and Microsoft 365 services.</span></span>
- <span data-ttu-id="13dba-135">**3. stsenaarium** nõuab tuge klientrakendustest ja teenustest, mida hostitakse Microsoft Azure’is.</span><span class="sxs-lookup"><span data-stu-id="13dba-135">**Scenario 3** requires support from client applications and from services that are hosted in Microsoft Azure.</span></span>

<span data-ttu-id="13dba-136">Lisaks platvormile, mis juurutatakse Azure’i tellimusse, pakuvad Finance and Operationsi rakendused klientidele integreeritud, esimese osapoole Azure’i rakendust, mis aitab neil printimiseks hõlpsamalt kasutada domeenis hostitud seadmeid.</span><span class="sxs-lookup"><span data-stu-id="13dba-136">In addition to the platform that is deployed to the Azure subscription, Finance and Operations applications provide customers with an integrated, first-party Azure application that helps them more easily use domain-hosted devices to print documents.</span></span>

## <a name="service-overview"></a><span data-ttu-id="13dba-137">Hoolduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="13dba-137">Service overview</span></span>
<span data-ttu-id="13dba-138">Ajal, mil hostitud rakenduste loodud dokmendid ootavad printimist võrku ühendatud seadmes, talletatakse neid Azure’i bloobimälus.</span><span class="sxs-lookup"><span data-stu-id="13dba-138">While documents that are produced by the hosted applications are waiting to be printed on a network-connected device, they are stored in Azure blob storage.</span></span> <span data-ttu-id="13dba-139">[Dokumendi marsruudivaliku agendi installimine võrguprintimise lubamiseks](install-document-routing-agent.md) kasutab Azure’i autentimist, et luua turvaline kanal Azure’i teenustega.</span><span class="sxs-lookup"><span data-stu-id="13dba-139">The [Install the Document Routing Agent to enable network printing](install-document-routing-agent.md) uses Azure authentication to establish a secure channel to the Azure services.</span></span>

<span data-ttu-id="13dba-140">**Käivitamisjärjekord**</span><span class="sxs-lookup"><span data-stu-id="13dba-140">**Execution sequence**</span></span>

1. <span data-ttu-id="13dba-141">Teenus Microsoft SQL Server Reporting Services (SSRS) loob aruande, mis talletatakse Azure’i bloobimälus.</span><span class="sxs-lookup"><span data-stu-id="13dba-141">The report is generated by Microsoft SQL Server Reporting Services (SSRS) and stored in Azure blob storage.</span></span> <span data-ttu-id="13dba-142">Seotud printerisätteid talletatakse koos dokumendiga.</span><span class="sxs-lookup"><span data-stu-id="13dba-142">Attached printer settings are stored together with the document.</span></span>
2. <span data-ttu-id="13dba-143">Dokumendi marsruudivaliku agent esitab Azure’i teenusesiini järjekorda aktiivsete tööde päringu.</span><span class="sxs-lookup"><span data-stu-id="13dba-143">The Document Routing Agent queries the Azure Service Bus queue for active jobs.</span></span>
3. <span data-ttu-id="13dba-144">Dokumendi marsruudivaliku agent laadib dokumendi alla ja spuulib selle võrguprinterisse.</span><span class="sxs-lookup"><span data-stu-id="13dba-144">The document is downloaded by the Document Routing Agent and spooled to the network printer.</span></span>

<span data-ttu-id="13dba-145">Kliendipõhine lahendus võimaldab klientidel hallata oma printimisvajaduste ulatust.</span><span class="sxs-lookup"><span data-stu-id="13dba-145">The client-based solution lets customers manage the scale of their printing needs.</span></span> <span data-ttu-id="13dba-146">Kliendid, kellel on suuremahulised printimise töökoormused, saavad installida mitu dokumendi marsruudivaliku agenti, et suurendada samaaegsete printimistoimingute arvu.</span><span class="sxs-lookup"><span data-stu-id="13dba-146">Customers who have heavy-volume printing workloads can install many Document Routing Agents to increase the number of concurrent printing operations.</span></span> <span data-ttu-id="13dba-147">Samuti võib mõnel kliendil olla vajalik ainult väga väheste dokumendi marsruudivaliku agentide installimine, et täita nende printimisvajadusi.</span><span class="sxs-lookup"><span data-stu-id="13dba-147">Alternatively, some customers require very few installations of the Document Routing Agent to handle their anticipated printing needs.</span></span>

### <a name="service-components-for-network-printing"></a><span data-ttu-id="13dba-148">Võrguprintimise teenusekomponendid</span><span class="sxs-lookup"><span data-stu-id="13dba-148">Service components for network printing</span></span>

<span data-ttu-id="13dba-149">Järgmisel diagrammil on näidatud põhikomponendid, mis toetavad võrguprintimise toiminguid.</span><span class="sxs-lookup"><span data-stu-id="13dba-149">The following diagram shows the basic components that help support network printing operations.</span></span>

<span data-ttu-id="13dba-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span><span class="sxs-lookup"><span data-stu-id="13dba-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span></span>

<span data-ttu-id="13dba-151">Pange tähele, et ühe printeri juurde saab registreerida mitu dokumendi marsruudivaliku agenti.</span><span class="sxs-lookup"><span data-stu-id="13dba-151">Note that a single printer can be registered with multiple Document Routing Agents.</span></span> <span data-ttu-id="13dba-152">Printimiseelistuste lahendamiseks kasutab hostitud teenus võrguteed, mis tuvastab kordumatult iga võrguprinteri.</span><span class="sxs-lookup"><span data-stu-id="13dba-152">To resolve the printer preferences, the hosted service uses the network path that uniquely identifies every network printer.</span></span> <span data-ttu-id="13dba-153">Sellest tulenevalt kuvatakse printer ka siis, kui selle on registreerinud mitu klienti, rakenduste saadaolevate printerite loendis ühe valikuna.</span><span class="sxs-lookup"><span data-stu-id="13dba-153">As a result, even when a printer is registered by multiple clients, it appears as a single selection in the list of printers available in applications.</span></span>
