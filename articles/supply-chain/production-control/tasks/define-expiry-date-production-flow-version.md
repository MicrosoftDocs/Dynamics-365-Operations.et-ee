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
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a595ca4ff9f6753631303b656d56735320a22a69
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975081"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="daa64-103">Tootmisvoo versiooni aegumiskuupäeva määratlemine</span><span class="sxs-lookup"><span data-stu-id="daa64-103">Define an expiry date for a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="daa64-104">Tootmisvoo kehtivuse ja töötlemise lõpetamiseks antud kuupäeval või aktiivse versiooni uue versiooniga asendamise plaanimiseks tuleb määrata sellele versioonile aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="daa64-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="daa64-105">Versiooni pole vaja inaktiveerida.</span><span class="sxs-lookup"><span data-stu-id="daa64-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="daa64-106">Määrake tootmisvoo versiooni lõpetamiseks aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="daa64-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="daa64-107">Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.</span><span class="sxs-lookup"><span data-stu-id="daa64-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="daa64-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="daa64-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="daa64-109">Valige tootmisvoog, millel on juba määratletud versioon.</span><span class="sxs-lookup"><span data-stu-id="daa64-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="daa64-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="daa64-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="daa64-111">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="daa64-111">Click Edit.</span></span>
5. <span data-ttu-id="daa64-112">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="daa64-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="daa64-113">Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="daa64-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="daa64-114">Selle aegumiskuupäeva puhul ei käivitu ega aktiveeru uus versioon.</span><span class="sxs-lookup"><span data-stu-id="daa64-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="daa64-115">Samuti ei saa sellele tootmisvoole enam töid luua ega käivitada.</span><span class="sxs-lookup"><span data-stu-id="daa64-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="daa64-116">Alustatud töid saab siiski pärast aegumiskuupäeva lõpetada.</span><span class="sxs-lookup"><span data-stu-id="daa64-116">You can still complete started jobs after the expiration date.</span></span>  

