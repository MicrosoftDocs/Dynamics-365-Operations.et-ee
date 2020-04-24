---
title: Tootmisvoo versiooni aegumiskuupäeva määratlemine
description: Tootmisvoo kehtivuse ja töötlemise lõpetamiseks antud kuupäeval või aktiivse versiooni uue versiooniga asendamise plaanimiseks tuleb määrata sellele versioonile aegumiskuupäev.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d942f54b2739f2ca3dcc3e8b8a497166a8edb42
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212085"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="6c165-103">Tootmisvoo versiooni aegumiskuupäeva määratlemine</span><span class="sxs-lookup"><span data-stu-id="6c165-103">Define an expiry date for a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c165-104">Tootmisvoo kehtivuse ja töötlemise lõpetamiseks antud kuupäeval või aktiivse versiooni uue versiooniga asendamise plaanimiseks tuleb määrata sellele versioonile aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="6c165-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="6c165-105">Versiooni pole vaja inaktiveerida.</span><span class="sxs-lookup"><span data-stu-id="6c165-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="6c165-106">Määrake tootmisvoo versiooni lõpetamiseks aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="6c165-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="6c165-107">Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.</span><span class="sxs-lookup"><span data-stu-id="6c165-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="6c165-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6c165-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6c165-109">Valige tootmisvoog, millel on juba määratletud versioon.</span><span class="sxs-lookup"><span data-stu-id="6c165-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="6c165-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6c165-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6c165-111">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="6c165-111">Click Edit.</span></span>
5. <span data-ttu-id="6c165-112">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6c165-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="6c165-113">Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="6c165-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="6c165-114">Selle aegumiskuupäeva puhul ei käivitu ega aktiveeru uus versioon.</span><span class="sxs-lookup"><span data-stu-id="6c165-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="6c165-115">Samuti ei saa sellele tootmisvoole enam töid luua ega käivitada.</span><span class="sxs-lookup"><span data-stu-id="6c165-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="6c165-116">Alustatud töid saab siiski pärast aegumiskuupäeva lõpetada.</span><span class="sxs-lookup"><span data-stu-id="6c165-116">You can still complete started jobs after the expiration date.</span></span>  

