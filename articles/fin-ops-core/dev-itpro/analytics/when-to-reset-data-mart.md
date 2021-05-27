---
title: Millal andmevakka lähtestada?
description: Selles teemas loetletakse tingimused, mida võib saada parandada andmevaka lähtestamisega, ja tingimused, mille korral teie andmevaka lähtestamine on tõenäoliselt abiks.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988988"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="8c040-103">Millal andmevakka lähtestada?</span><span class="sxs-lookup"><span data-stu-id="8c040-103">When to reset a data mart</span></span>

<span data-ttu-id="8c040-104">Andmevaka lähtestamine võib aega võtta.</span><span class="sxs-lookup"><span data-stu-id="8c040-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="8c040-105">Olenevalt olukorrast ei pruugi see toiming olla vajalik lahendus.</span><span class="sxs-lookup"><span data-stu-id="8c040-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="8c040-106">Selles teemas loetletakse nii tingimused, mida võib saada parandada andmevaka lähtestamisega, kui ka tingimused, mille korral teie andmevaka lähtestamine on tõenäoliselt abiks.</span><span class="sxs-lookup"><span data-stu-id="8c040-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="8c040-107">Millal tuleb andmevakk lähtestada?</span><span class="sxs-lookup"><span data-stu-id="8c040-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="8c040-108">Enne andmevaka lähtestamist laakuge järgmist.</span><span class="sxs-lookup"><span data-stu-id="8c040-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="8c040-109">Ühele või mitmele küsimusele jaatavalt vastamine võib näidata, et teie organisatsioon võib andmevaka lähtestamisest kasu saada.</span><span class="sxs-lookup"><span data-stu-id="8c040-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="8c040-110">Kas rakenduse andmebaas taastati?</span><span class="sxs-lookup"><span data-stu-id="8c040-110">Was the application database restored?</span></span>
- <span data-ttu-id="8c040-111">Kui olete avanud tugijuhtumi ja tugiinsener on juhendanud teid lähtestama andmevaka tõrkeotsingu sammu osana?</span><span class="sxs-lookup"><span data-stu-id="8c040-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="8c040-112">Millal pole andmevaka lähtestamine sobiv lahendus?</span><span class="sxs-lookup"><span data-stu-id="8c040-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="8c040-113">Mõne olukorra puhul me ei soovita andmevakka lähtestada.</span><span class="sxs-lookup"><span data-stu-id="8c040-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="8c040-114">Need hõlmavad järgmist.</span><span class="sxs-lookup"><span data-stu-id="8c040-114">These include the following.</span></span> 

- <span data-ttu-id="8c040-115">Teil esineb andmete sünkroonimisega seotud jõudlusprobleeme.</span><span class="sxs-lookup"><span data-stu-id="8c040-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="8c040-116">Kui teil on mõne järgmise põhjuse tõttu korduv lähtestamise muster.</span><span class="sxs-lookup"><span data-stu-id="8c040-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="8c040-117">**Puuduvad andmed**</span><span class="sxs-lookup"><span data-stu-id="8c040-117">**Missing data**</span></span> 
  - <span data-ttu-id="8c040-118">**Kinnise integratsiooni olek**</span><span class="sxs-lookup"><span data-stu-id="8c040-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="8c040-119">**Aegunud kirjed** – aegunud kirjed ei pruugi andmevaka lähtestamist alati õigustada.</span><span class="sxs-lookup"><span data-stu-id="8c040-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="8c040-120">Kui teil on suur andmekomplekt, võtab lähtestamisprotsess aega, kuid tõenäoliselt on see täiustus.</span><span class="sxs-lookup"><span data-stu-id="8c040-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="8c040-121">Millal lähtestada andmevakka?</span><span class="sxs-lookup"><span data-stu-id="8c040-121">What is a data mart reset?</span></span>
- <span data-ttu-id="8c040-122">Lähtestamine algab ainult siis, kui olemasolevad ülesanded on lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="8c040-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="8c040-123">See tagab, et vanu andmeid ei lisata.</span><span class="sxs-lookup"><span data-stu-id="8c040-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="8c040-124">Selles punktis võite näha järgmist teadet: „Andmevaka lähtestamist ei saanud aktiivse ülesande tõttu töödelda.</span><span class="sxs-lookup"><span data-stu-id="8c040-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="8c040-125">Proovige hiljem uuesti.”</span><span class="sxs-lookup"><span data-stu-id="8c040-125">Please try again later.”</span></span>
- <span data-ttu-id="8c040-126">Lähtestamine keelab integratsioonitoimingud ja kustutab kõik andmevaka andmed.</span><span class="sxs-lookup"><span data-stu-id="8c040-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="8c040-127">Integratsioon lubatakse uuesti.</span><span class="sxs-lookup"><span data-stu-id="8c040-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="8c040-128">Kui lähtestan andmed marti, kas kaotan aruanded, mis ma juba kujundanud olen?</span><span class="sxs-lookup"><span data-stu-id="8c040-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="8c040-129">Ei, teie aruandeid talletatakse SQL-tabelites, mida ei mõjuta andmete lähtestamine marti.</span><span class="sxs-lookup"><span data-stu-id="8c040-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="8c040-130">Kui olete mures mõne loodud aruande kaotamise pärast, saate varundada kujundused, mida te ei soovi kaotada.</span><span class="sxs-lookup"><span data-stu-id="8c040-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="8c040-131">Nende varundamiseks avage aruandekujundaja ja minge **Ettevõtte > Ettevõtted > Koosteüksused > Eksport**.</span><span class="sxs-lookup"><span data-stu-id="8c040-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="8c040-132">Kas kõigi kasutajate puhul tuleb andmete lähtestamiseks süsteemist väljuda?</span><span class="sxs-lookup"><span data-stu-id="8c040-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="8c040-133">Ei, kasutajad saavad andmete marti lähtestamise ajal süsteemiga tööd jätkata.</span><span class="sxs-lookup"><span data-stu-id="8c040-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="8c040-134">Kuid enne lähtestamist ei pääse nad juurde aruannetele, mis on loodud finantsaruandluse aru anda.</span><span class="sxs-lookup"><span data-stu-id="8c040-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
