---
title: Süsteemi Go-live KKK
description: Selles teemas loetletakse Dynamics 365 Human Resourcesi juurutusprojekti kasutuselevõtuga seonduvaid korduma kippuvaid küsimusi.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 64a85840be328702a06779390fe383fd1896fd04
ms.sourcegitcommit: d66fd72342931fad25a696b251c05781280d36c4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/14/2020
ms.locfileid: "4011412"
---
# <a name="go-live-faq"></a><span data-ttu-id="a7f80-103">Süsteemi Go-live KKK</span><span class="sxs-lookup"><span data-stu-id="a7f80-103">Go-live FAQ</span></span> 

<span data-ttu-id="a7f80-104">Selles teemas loetletakse Dynamics 365 Human Resourcesi juurutusprojekti kasutuselevõtuga seonduvaid korduma kippuvaid küsimusi.</span><span class="sxs-lookup"><span data-stu-id="a7f80-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="a7f80-105">Millal ma saan konfigureerida ja taotleda oma töökeskkonda?</span><span class="sxs-lookup"><span data-stu-id="a7f80-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="a7f80-106">Tavaliselt saab töökeskkonda juurutada pärast järgmiste kriteeriumite täitmist.</span><span class="sxs-lookup"><span data-stu-id="a7f80-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="a7f80-107">Kõikide kohanduste kood on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="a7f80-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="a7f80-108">Kasutaja nõusoleku testimine (UAT) on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="a7f80-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="a7f80-109">Klient on lahendusele nõusoleku andnud.</span><span class="sxs-lookup"><span data-stu-id="a7f80-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="a7f80-110">Kasutuselevõttu blokeerivaid probleeme pole.</span><span class="sxs-lookup"><span data-stu-id="a7f80-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="a7f80-111">Kui kvalifitseeritud kliendid on jõudnud sellesse etappi, töötab Microsoft FastTracki meeskond koos projekti meeskonnaga kasutuselevõtu hindamise tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="a7f80-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="a7f80-112">Mis on töökeskkonna juurutamise eeltingimused?</span><span class="sxs-lookup"><span data-stu-id="a7f80-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="a7f80-113">Eeltingimuste loendi leiate teemast  [Kasutuselevõtuks ettevalmistamine](hr-admin-go-live-prepare.md).</span><span class="sxs-lookup"><span data-stu-id="a7f80-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="a7f80-114">Mis on kasutuselevõtu hindamine?</span><span class="sxs-lookup"><span data-stu-id="a7f80-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="a7f80-115">Kasutuselevõtu hindamine on  [Microsoft FastTracki programmi](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview) osa.</span><span class="sxs-lookup"><span data-stu-id="a7f80-115">The go-live assessment is part of the [Microsoft FastTrack program](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span></span> <span data-ttu-id="a7f80-116">Selle läbivaatuse käigus hindab lahenduse arhitekt, kas juurutusprojekt on valmis edukaks üleminekuks ja kasutuselevõtuks.</span><span class="sxs-lookup"><span data-stu-id="a7f80-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="a7f80-117">See läbivaatus on kohustuslik kõigile juurutusprojektidele, enne kui saate taotleda töökeskkonna kasutuselevõtmist.</span><span class="sxs-lookup"><span data-stu-id="a7f80-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="a7f80-118">Meie liivakastikeskkonnad juurutatakse Kesk-USA andmekeskuses.</span><span class="sxs-lookup"><span data-stu-id="a7f80-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="a7f80-119">Soovime, et meie töökeskkonnad oleksid juurutatud Lääne-USA andmekeskuses.</span><span class="sxs-lookup"><span data-stu-id="a7f80-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="a7f80-120">Kas ma saan valida Lääne-USA oma töökeskkonna konfiguratsiooni andmekeskuseks?</span><span class="sxs-lookup"><span data-stu-id="a7f80-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="a7f80-121">LCS ei keela teise andmekeskuse valimist Human Resourcesi keskkonna juurutamisel, kuid soovitame tungivalt mitte valida teist andmekeskust.</span><span class="sxs-lookup"><span data-stu-id="a7f80-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="a7f80-122">Kui soovite oma töökeskkonda Lääne-USA andmekeskusesse, peaksite esmalt oma liivakastikeskkonnad Lääne-USA andmekeskuses uuesti juurutama, neid katsetama ja andma nõusoleku.</span><span class="sxs-lookup"><span data-stu-id="a7f80-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="a7f80-123">Lisateavet õige andmekeskuse valimise kohta leiate teemast [Võrgunõuded](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span><span class="sxs-lookup"><span data-stu-id="a7f80-123">For information about selecting the correct datacenter, see [Network requirements](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="a7f80-124">Mis tasemel juurdepääs mul on Human Resourcesi keskkondade Azure'i ressurssidele?</span><span class="sxs-lookup"><span data-stu-id="a7f80-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="a7f80-125">Human Resourcesi keskkondade juurdepääs on piiratud.</span><span class="sxs-lookup"><span data-stu-id="a7f80-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="a7f80-126">Te ei pääse juurde virtuaalarvutile (VM) või Microsoft Internet Information Servicesi (IIS).</span><span class="sxs-lookup"><span data-stu-id="a7f80-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="a7f80-127">Samuti pole teil andmebaasi juurdepääsu Microsoft SQL Server Management Studio kaudu.</span><span class="sxs-lookup"><span data-stu-id="a7f80-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="a7f80-128">Kuigi te ei pääse oma Azure'i ressurssidele või Dynamics 365 Human Resourcesi keskkonnale juurde otse, on teil täiendavaid funktsioone, mida saate kasutada oma andmetele juurde pääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="a7f80-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="a7f80-129">Saate juurutada Azure SQL-i andmebaasi oma Azure'i rentnikku ja kasutada oma andmebaasi toomise (BYOD) funktsiooni andmete sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="a7f80-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="a7f80-130">Lisateavet leiate teemast [Oma andmebaasi toomine (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="a7f80-130">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span>

- <span data-ttu-id="a7f80-131">Saate kasutada Common Data Service'i integreerimist valitud üksuste sünkroonimiseks Common Data Service'i andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="a7f80-131">You can use Common Data Service integration to synchronize select entities into the Common Data Service database.</span></span> <span data-ttu-id="a7f80-132">Lisateavet vt jaotisest [Common Data Service'i üksused](hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="a7f80-132">For more information, see [Common Data Service entities](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="a7f80-133">Kui tihti minu tööandmebaasi varundatakse?</span><span class="sxs-lookup"><span data-stu-id="a7f80-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="a7f80-134">Andmebaase kaitstakse automaatse varundusega järgmise sagedusega.</span><span class="sxs-lookup"><span data-stu-id="a7f80-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="a7f80-135">Varunduse tüüp</span><span class="sxs-lookup"><span data-stu-id="a7f80-135">Type of backup</span></span> | <span data-ttu-id="a7f80-136">Sagedus</span><span class="sxs-lookup"><span data-stu-id="a7f80-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="a7f80-137">Täielik andmebaasi varundus</span><span class="sxs-lookup"><span data-stu-id="a7f80-137">Full database backup</span></span> | <span data-ttu-id="a7f80-138">Iganädalane</span><span class="sxs-lookup"><span data-stu-id="a7f80-138">Weekly</span></span> |
| <span data-ttu-id="a7f80-139">Eristav andmebaasi varundus</span><span class="sxs-lookup"><span data-stu-id="a7f80-139">Differential database backup</span></span> | <span data-ttu-id="a7f80-140">Iga 12–24 tunni järel</span><span class="sxs-lookup"><span data-stu-id="a7f80-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="a7f80-141">Kandelogi varundus</span><span class="sxs-lookup"><span data-stu-id="a7f80-141">Transaction log backup</span></span> | <span data-ttu-id="a7f80-142">Iga 5–10 minuti järel</span><span class="sxs-lookup"><span data-stu-id="a7f80-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="a7f80-143">Microsoft säilitab piisavalt varukoopiaid selleks, et lubada ajapunktipõhist taastet (PITR) viimase seitsme päeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="a7f80-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last seven days.</span></span> 

<span data-ttu-id="a7f80-144">Lisateabe saamiseks vt jaotist  [Lisateave SQL-i andmebaasi automaatsete varunduste kohta](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span><span class="sxs-lookup"><span data-stu-id="a7f80-144">For more information, see [Learn about automatic SQL Database backups](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="a7f80-145">Kas ma saan taotleda oma andmebaasi varunduse koopiat?</span><span class="sxs-lookup"><span data-stu-id="a7f80-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="a7f80-146">Nr</span><span class="sxs-lookup"><span data-stu-id="a7f80-146">No.</span></span> <span data-ttu-id="a7f80-147">Saate esitada andmebaasi värskendamise teenuse taotluse oma töökeskkonna kopeermiseks liivakastikeskkonda.</span><span class="sxs-lookup"><span data-stu-id="a7f80-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="a7f80-148">Saate juurutada Azure SQL-i andmebaasi oma Azure'i rentnikku ja kasutada BYOD-i funktsiooni andmete sünkroonimiseks töökeskkonnast.</span><span class="sxs-lookup"><span data-stu-id="a7f80-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="a7f80-149">Lisateavet leiate teemast [Oma andmebaasi toomine (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="a7f80-149">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="a7f80-150">Kuidas ma saan teisaldada liivakastikeskkonda töökeskkonna selle kasutuselevõtuks?</span><span class="sxs-lookup"><span data-stu-id="a7f80-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="a7f80-151">Kuna kopeerimise funktsioon ei ole saadaval keskkonna teisaldamiseks liivakastikeskkonnast töökeskkonda, peate kasutama andmepakette andmete teisaldamiseks oma töökeskkonda.</span><span class="sxs-lookup"><span data-stu-id="a7f80-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="a7f80-152">Soovitame säilitada selge loendi üksustest, mis on konfigureeritud teie liivakastikeskkonnas kogu projekti jooksul.</span><span class="sxs-lookup"><span data-stu-id="a7f80-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="a7f80-153">Seejärel katsetage kasutuselevõtuks vajalike andmepakettide ülemineku- ja migreerimisprotsessi.</span><span class="sxs-lookup"><span data-stu-id="a7f80-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="a7f80-154">Kui olete kasutuselevõtuks valmis, peate kõik andmepaketid käsitsi töökeskkonda teisaldama.</span><span class="sxs-lookup"><span data-stu-id="a7f80-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="a7f80-155">Mida teha, kui minu töökeskkond on maas?</span><span class="sxs-lookup"><span data-stu-id="a7f80-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="a7f80-156">Töökeskkonna katkestusest teatamiseks järgige juhiseid jaotises  [Töökeskkonna katkestusest teatamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span><span class="sxs-lookup"><span data-stu-id="a7f80-156">To report a Production outage, follow the process described in [Report a production outage](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="a7f80-157">Vt ka</span><span class="sxs-lookup"><span data-stu-id="a7f80-157">See also</span></span>

 [<span data-ttu-id="a7f80-158">Ettevalmistamine süsteemi Go-Live jaoks</span><span class="sxs-lookup"><span data-stu-id="a7f80-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)