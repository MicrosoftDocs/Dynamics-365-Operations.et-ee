---
title: Protsessi automatiseerimisvoogude kutsumine kvaliteettellimuste loomiseks
description: See teema annab ressursse Power Automate äriprotsesside automatiseerimiseks, kasutades kvaliteettellimuste näidet.
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115177"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a><span data-ttu-id="6dc12-103">Protsessi automatiseerimisvoogude kutsumine kvaliteettellimuste loomiseks</span><span class="sxs-lookup"><span data-stu-id="6dc12-103">Invoke process automation flows to create quality orders</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="6dc12-104">Organisatsioonidel on järjest suurem nõudlus standardsete äriprotsesside automatiseerimiseks, mugavamaks suhtluse pakkumiseks personaliga ja erinevate andmeimpulsside ja -süsteemide kasutamine äriprotsesside automaatseks käivitamiseks.</span><span class="sxs-lookup"><span data-stu-id="6dc12-104">Organizations have an increasing demand to automate standard business processes, provide more convenient interactions to the staff, and utilize various data signals and systems to drive business processes automatically.</span></span> <span data-ttu-id="6dc12-105">Automaatse protsessi automatiseerimise (RPA) puhul saavad ettevõtted kasutada koodita kogemust, et automatiseerida korduvad protsessid, mis koguvad nii efektiivsust Microsoft Power Automate ja täpsust.</span><span class="sxs-lookup"><span data-stu-id="6dc12-105">With robotic process automation (RPA) and Microsoft Power Automate, businesses can use a no-code experience to automate repetitive processes, thus gaining efficiency and accuracy.</span></span>

<span data-ttu-id="6dc12-106">Allalaaditava automatiseerimise lahenduse mall Supply Chain Management näitab, kuidas saab kasutada äriprotsesside automatiseerimiseks, kasutades Power Automate näitena kvaliteettellimusi.</span><span class="sxs-lookup"><span data-stu-id="6dc12-106">The downloadable automation solution template for Supply Chain Management showcases how Power Automate can be used to automate business processes using quality orders as an example.</span></span>

<span data-ttu-id="6dc12-107">Saate automatiseerimislahenduse malli alla laadida [siin](https://aka.ms/D365SCMQualityOrderRPASolution).</span><span class="sxs-lookup"><span data-stu-id="6dc12-107">You can download the automation solution template [here](https://aka.ms/D365SCMQualityOrderRPASolution).</span></span>

<span data-ttu-id="6dc12-108">Selle funktsiooni ja selle võimalustest ülevaate saamiseks vaadake järgmist videot: [kasutage kvaliteettellimuste loomiseks RPA-d rakenduses Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span><span class="sxs-lookup"><span data-stu-id="6dc12-108">For an overview of this feature and its capabilities, see the following video: [Utilize RPA to create quality orders in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span></span>

<span data-ttu-id="6dc12-109">![Automatiseerimisvalikud RPA-ga](media/rpa-automation-options.png "Automatiseerimisvalikud RPA-ga")</span><span class="sxs-lookup"><span data-stu-id="6dc12-109">![Automation options with RPA](media/rpa-automation-options.png "Automation options with RPA")</span></span>

<span data-ttu-id="6dc12-110">Lahenduse Power Automate mall hõlmab pilve automatiseerimisvoogu ja töölaua automatiseerimisvoogu, mis automatiseerib kvaliteettellimuste loomise Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6dc12-110">The Power Automate solution template includes a cloud automation flow and a desktop automation flow that automate the creation of quality orders in Supply Chain Management.</span></span>

<span data-ttu-id="6dc12-111">Automatiseerimist saab käivitada reageerida paljudele sündmustele ja signaalidele, k.a kasutajasisend või masina signaalid (k.a IoT-internet).</span><span class="sxs-lookup"><span data-stu-id="6dc12-111">The automation can be started in response to many events and signals, including user input or machine signals (including the Internet of Things (IoT)).</span></span> <span data-ttu-id="6dc12-112">*Q-tellimus* Power Application näidises sisaldub lahendusrakenduse näide.</span><span class="sxs-lookup"><span data-stu-id="6dc12-112">The *Q-Order* Power Application example is included in the solution template.</span></span> <span data-ttu-id="6dc12-113">See võimaldab kasutajal skannida kauba QR-koodi, sisestada kogust ja lisada pilte kaameraga.</span><span class="sxs-lookup"><span data-stu-id="6dc12-113">It allows the user to scan an item QR code, enter quantity, and attach pictures using a camera.</span></span>

<span data-ttu-id="6dc12-114">Lahenduse parameetrid kaasatakse automatiseerimise konfigureerimiseks tootmisteenuses konkreetse kasutusjuhtumi jaoks.</span><span class="sxs-lookup"><span data-stu-id="6dc12-114">Solution parameters are included to configure the automation for a specific use case in a production facility.</span></span>

<span data-ttu-id="6dc12-115">![Loo kvaliteettellimus](media/rpa-create-quality-roder.png "Loo kvaliteettellimus")</span><span class="sxs-lookup"><span data-stu-id="6dc12-115">![Create quality order](media/rpa-create-quality-roder.png "Create quality order")</span></span>

<span data-ttu-id="6dc12-116">Täielikku etapit-sammulise juhendit selle kohta, kuidas kvaliteettellimuse loomise automaatseks automatiseerimiseks näidislahendust alla laadida, installida ja kasutada, vt [Automate kvaliteettellimuse loomine Dynamics 365 Supply Chain Management Desktop koos rakendusega Robotic Process Automation kasutades Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span><span class="sxs-lookup"><span data-stu-id="6dc12-116">For a complete step-by-step guide about how to download, install, and use the sample solution for automating quality order creation, see [Automate quality order creation on Dynamics 365 Supply Chain Management with Robotic Process Automation using Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span></span>

