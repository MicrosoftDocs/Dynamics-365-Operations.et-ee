---
title: Tootmisvoo versiooni aegumiskuupäeva määratlemine
description: Tootmisvoo kehtivuse ja töötlemise lõpetamiseks antud kuupäeval või aktiivse versiooni uue versiooniga asendamise plaanimiseks tuleb määrata sellele versioonile aegumiskuupäev.
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
ms.openlocfilehash: 10260290fba02ebf9313d0d1355c9aa28e3509d7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843693"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="c456d-103">Tootmisvoo versiooni aegumiskuupäeva määratlemine</span><span class="sxs-lookup"><span data-stu-id="c456d-103">Define an expiry date for a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c456d-104">Tootmisvoo kehtivuse ja töötlemise lõpetamiseks antud kuupäeval või aktiivse versiooni uue versiooniga asendamise plaanimiseks tuleb määrata sellele versioonile aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="c456d-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="c456d-105">Versiooni pole vaja inaktiveerida.</span><span class="sxs-lookup"><span data-stu-id="c456d-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="c456d-106">Määrake tootmisvoo versiooni lõpetamiseks aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="c456d-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="c456d-107">Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.</span><span class="sxs-lookup"><span data-stu-id="c456d-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="c456d-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c456d-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c456d-109">Valige tootmisvoog, millel on juba määratletud versioon.</span><span class="sxs-lookup"><span data-stu-id="c456d-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="c456d-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c456d-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c456d-111">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="c456d-111">Click Edit.</span></span>
5. <span data-ttu-id="c456d-112">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="c456d-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="c456d-113">Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="c456d-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="c456d-114">Selle aegumiskuupäeva puhul ei käivitu ega aktiveeru uus versioon.</span><span class="sxs-lookup"><span data-stu-id="c456d-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="c456d-115">Samuti ei saa sellele tootmisvoole enam töid luua ega käivitada.</span><span class="sxs-lookup"><span data-stu-id="c456d-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="c456d-116">Alustatud töid saab siiski pärast aegumiskuupäeva lõpetada.</span><span class="sxs-lookup"><span data-stu-id="c456d-116">You can still complete started jobs after the expiration date.</span></span>  

