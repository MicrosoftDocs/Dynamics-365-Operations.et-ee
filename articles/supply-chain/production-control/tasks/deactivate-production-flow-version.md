---
title: Tootmisvoo versiooni desaktiveerimine
description: Kui aktiivset tootmisvoo versiooni pole enam vaja, võib selle inaktiveerida.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c9646a01924255b8b1b40fc2a5684ba30967fe1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843837"
---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="af134-103">Tootmisvoo versiooni desaktiveerimine</span><span class="sxs-lookup"><span data-stu-id="af134-103">Deactivate a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af134-104">Kui aktiivset tootmisvoo versiooni pole enam vaja, võib selle inaktiveerida.</span><span class="sxs-lookup"><span data-stu-id="af134-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="af134-105">Peaksite kasutama seda valikut ainult juhul, kui kõik kanban-reeglid ja tegevused on lõppenud ning neid ei aktiveerita enam.</span><span class="sxs-lookup"><span data-stu-id="af134-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="af134-106">Arvestage, et kõigi selle tootmisvoo versiooniga seotud kanban-reeglite aegumiskuupäevaks määratakse praegune kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="af134-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="af134-107">Aktiivse tootmisvoo versiooni muutmiseks kaaluge aktiivsele versioonile aegumiskuupäeva määramist ja looge uus versioon.</span><span class="sxs-lookup"><span data-stu-id="af134-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="af134-108">See võimaldab uue versiooni ja seotud kanban-reeglite koostamise ajal tootmistegevusi jätkata.</span><span class="sxs-lookup"><span data-stu-id="af134-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="af134-109">Aktiivse tootmisvoo versiooni aegunuks märkimiseks tuleb määrata aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="af134-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="af134-110">Selles mõttes on inaktiveerimine pigem erand kui reegel.</span><span class="sxs-lookup"><span data-stu-id="af134-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="af134-111">Selle protseduuri jaoks on vaja tootmisvoogu, mille versiooni saab inaktiveerida.</span><span class="sxs-lookup"><span data-stu-id="af134-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="af134-112">Ärge proovige seda tootmiskeskkonnas, kui te pole 100% kindel, et versioon on täiesti aegunud.</span><span class="sxs-lookup"><span data-stu-id="af134-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="af134-113">Tootmisvoo versiooni desaktiveerimine</span><span class="sxs-lookup"><span data-stu-id="af134-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="af134-114">Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.</span><span class="sxs-lookup"><span data-stu-id="af134-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="af134-115">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="af134-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="af134-116">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="af134-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="af134-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="af134-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="af134-118">Klõpsake käsku Inaktiveeri.</span><span class="sxs-lookup"><span data-stu-id="af134-118">Click Deactivate.</span></span>
    * <span data-ttu-id="af134-119">Ärge jätkake, kui te ei ole 100% kindel, et tootmisvoo versioon on aegunud.</span><span class="sxs-lookup"><span data-stu-id="af134-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="af134-120">Nupu OK klõpsamisel aeguvad kõik aktiivsed kanban-reeglid ja kõik selle tootmisvoo versiooni tootmis- ja täiendamistegevused peatatakse.</span><span class="sxs-lookup"><span data-stu-id="af134-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="af134-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="af134-121">Click OK.</span></span>

