---
title: Millal andmevakka lähtestada?
description: Selles teemas loetletakse tingimused, mida võib saada parandada andmevaka lähtestamisega, ja tingimused, mille korral teie andmevaka lähtestamine on tõenäoliselt abiks.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71324d4aa2d20dd6ae4729412a017d130ab0144f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563725"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="98b85-103">Millal andmevakka lähtestada?</span><span class="sxs-lookup"><span data-stu-id="98b85-103">When to reset a data mart</span></span>

<span data-ttu-id="98b85-104">Andmevaka lähtestamine võib aega võtta.</span><span class="sxs-lookup"><span data-stu-id="98b85-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="98b85-105">Olenevalt olukorrast ei pruugi see toiming olla vajalik lahendus.</span><span class="sxs-lookup"><span data-stu-id="98b85-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="98b85-106">Selles teemas loetletakse nii tingimused, mida võib saada parandada andmevaka lähtestamisega, kui ka tingimused, mille korral teie andmevaka lähtestamine on tõenäoliselt abiks.</span><span class="sxs-lookup"><span data-stu-id="98b85-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="98b85-107">Millal tuleb andmevakk lähtestada?</span><span class="sxs-lookup"><span data-stu-id="98b85-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="98b85-108">Enne andmevaka lähtestamist laakuge järgmist.</span><span class="sxs-lookup"><span data-stu-id="98b85-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="98b85-109">Ühele või mitmele küsimusele jaatavalt vastamine võib näidata, et teie organisatsioon võib andmevaka lähtestamisest kasu saada.</span><span class="sxs-lookup"><span data-stu-id="98b85-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="98b85-110">Rakenduse andmebaas taastati, kuid andmevaka andmebaasi ei taastatud.</span><span class="sxs-lookup"><span data-stu-id="98b85-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="98b85-111">Raamatupidamisperioodi kohta kuvatakse valesid andmeid, mis pole aruande kujundusega seotud probleemi tulemus.</span><span class="sxs-lookup"><span data-stu-id="98b85-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="98b85-112">Raamatupidamisperioodi kohta kuvatakse valed andmed ja kirjed loetletakse lehel **Integratsiooni olek** integreerimiskatsete all aruandekujundajas (käivitage aruandekujundaja ja valige **Tööriistad > Integratsiooni olek**).</span><span class="sxs-lookup"><span data-stu-id="98b85-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="98b85-113">Olete avanud tugijuhtumi ja tugiinsener on juhendanud teid lähtestama andmevaka tõrkeotsingu sammu osana.</span><span class="sxs-lookup"><span data-stu-id="98b85-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="98b85-114">Millal pole andmevaka lähtestamine sobiv lahendus?</span><span class="sxs-lookup"><span data-stu-id="98b85-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="98b85-115">Mõne olukorra puhul me ei soovita andmevakka lähtestada.</span><span class="sxs-lookup"><span data-stu-id="98b85-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="98b85-116">Need hõlmavad järgmist.</span><span class="sxs-lookup"><span data-stu-id="98b85-116">These include the following.</span></span> 

- <span data-ttu-id="98b85-117">Igal ajal, kui põhjus pole selles teemas loetletud.</span><span class="sxs-lookup"><span data-stu-id="98b85-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="98b85-118">Teil esineb andmete sünkroonimisega seotud jõudlusprobleeme. Sellisel juhul ei ole andmevaka lähtestamine tõenäoliselt abiks.</span><span class="sxs-lookup"><span data-stu-id="98b85-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="98b85-119">Kui teil on mõne järgmise põhjuse tõttu korduv lähtestamise muster.</span><span class="sxs-lookup"><span data-stu-id="98b85-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="98b85-120">**Puuduvad andmed** – kõigepealt eemaldage aruande kujunduse probleemid ja andmete sünkroonimise ajastusprobleemid, näiteks märkate, et faktikaart pole puuduvate andmete sisestamisest alates käivitunud.</span><span class="sxs-lookup"><span data-stu-id="98b85-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="98b85-121">**Integratsiooni kinni jäänud olek** – kui integratsioon on aeglane või näib kinni jäänuna, siis andmevaka lähtestamine tõenäoliselt probleemi ei lahenda.</span><span class="sxs-lookup"><span data-stu-id="98b85-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="98b85-122">**Lähtestamise katsed nurjusid** – kui tehti palju lähtestamise katseid ja need ei õnnestunud puuduvate andmete tõttu, soovitame avada tugijuhtumi ja teha tugiinseneriga koostööd, et analüüsida teie olukorda enne andmete uuesti lähtestamist.</span><span class="sxs-lookup"><span data-stu-id="98b85-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="98b85-123">**Aegunud kirjed** – aegunud kirjed ei pruugi andmevaka lähtestamist alati õigustada.</span><span class="sxs-lookup"><span data-stu-id="98b85-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="98b85-124">Kui teil on suur andmekomplekt, võtab lähtestamisprotsess aega, kuid tõenäoliselt on see täiustus.</span><span class="sxs-lookup"><span data-stu-id="98b85-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="98b85-125">Mida andmevaka lähtestamine ei tee?</span><span class="sxs-lookup"><span data-stu-id="98b85-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="98b85-126">Lähtestamine algab ainult siis, kui olemasolevad ülesanded on lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="98b85-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="98b85-127">See tagab, et vanu andmeid ei lisata.</span><span class="sxs-lookup"><span data-stu-id="98b85-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="98b85-128">Selles punktis võite näha järgmist teadet: „Andmevaka lähtestamist ei saanud aktiivse ülesande tõttu töödelda.</span><span class="sxs-lookup"><span data-stu-id="98b85-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="98b85-129">Proovige hiljem uuesti.”</span><span class="sxs-lookup"><span data-stu-id="98b85-129">Please try again later.”</span></span>
- <span data-ttu-id="98b85-130">Lähtestamine keelab integratsioonitoimingud ja kustutab kõik andmevaka andmed.</span><span class="sxs-lookup"><span data-stu-id="98b85-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="98b85-131">Integratsioon lubatakse uuesti.</span><span class="sxs-lookup"><span data-stu-id="98b85-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="98b85-132">Järgmised punktid määravad kaks asja, mida andmevaka lähtestamine *ei* tee.</span><span class="sxs-lookup"><span data-stu-id="98b85-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="98b85-133">Lähtestamised ei tühjenda aruande kujundusi.</span><span class="sxs-lookup"><span data-stu-id="98b85-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="98b85-134">Lähtestamised ei kustuta ettevõtte ega kasutaja andmeid, kui need pole valitud.</span><span class="sxs-lookup"><span data-stu-id="98b85-134">Resets do not clear company data or user data unless selected.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]