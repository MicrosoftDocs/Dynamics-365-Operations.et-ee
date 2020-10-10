---
title: Eelistatud hooldustöötajate seadistus
description: Selles teemas selgitatakse, kuidas sätestada eelistatud hooldustöötajaid varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c0637609a34890360a3b81355a8d21ef1b9faf8c
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888925"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="b478e-103">Eelistatud hooldustöötajate seadistus</span><span class="sxs-lookup"><span data-stu-id="b478e-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b478e-104">Saate töötellimuse planeerimisel eelistada, milline hooldustööline või tööliste rühm on määratud töötellimuste läbiviimiseks.</span><span class="sxs-lookup"><span data-stu-id="b478e-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="b478e-105">Selle funktsiooni kasutamine on valikuline, kuid see aitab teil töö läbiviimiseks valida kõige kvalifitseerituma hooldustöötaja tema oskuste ja pädevuste alusel.</span><span class="sxs-lookup"><span data-stu-id="b478e-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="b478e-106">Planeeritakse ainult hooldustöötajaid, kes on saadaval planeerimise ajal.</span><span class="sxs-lookup"><span data-stu-id="b478e-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="b478e-107">Kui eelistatud hooldustöötaja häälestus ühtib planeerimisel töötellimusega, kuid hooldustöötaja on määratud teistele töödele, planeeritakse töötellimus teisele, saadaolevale hooldustöötajale.</span><span class="sxs-lookup"><span data-stu-id="b478e-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="b478e-108">Enne eelistatud hooldustöötajate seadistamist peate esmalt seadistama hooldustöötajad ja töötajate rühmad.</span><span class="sxs-lookup"><span data-stu-id="b478e-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="b478e-109">Hooldustöötajate ja töötajate rühmade sätestamise kirjeldust vaadake teemast [Hooldustöötajad ja töötajate rühmad](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="b478e-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="b478e-110">Eelistatud hooldustöötajate sätestamine</span><span class="sxs-lookup"><span data-stu-id="b478e-110">Set up preferred workers</span></span>

<span data-ttu-id="b478e-111">Eelistatud hooldustöötaja või töötajate rühm võib olla seotud ühe või mitmega järgmistest.</span><span class="sxs-lookup"><span data-stu-id="b478e-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="b478e-112">kaubandus</span><span class="sxs-lookup"><span data-stu-id="b478e-112">trade</span></span>  
- <span data-ttu-id="b478e-113">Hooldustöö  tüübi variant</span><span class="sxs-lookup"><span data-stu-id="b478e-113">maintenance job type variant</span></span>  
- <span data-ttu-id="b478e-114">Hooldustöö tüüp</span><span class="sxs-lookup"><span data-stu-id="b478e-114">maintenance job type</span></span>  
- <span data-ttu-id="b478e-115">Hooldustöö tüübi kategooria</span><span class="sxs-lookup"><span data-stu-id="b478e-115">maintenance job type category</span></span>  
- <span data-ttu-id="b478e-116">vara</span><span class="sxs-lookup"><span data-stu-id="b478e-116">asset</span></span>  
- <span data-ttu-id="b478e-117">Vara tüüp</span><span class="sxs-lookup"><span data-stu-id="b478e-117">asset type</span></span>  

<span data-ttu-id="b478e-118">Mida rohkem valikuid te sama kirje jaoks teete, seda täpsem on teie seadistus.</span><span class="sxs-lookup"><span data-stu-id="b478e-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="b478e-119">Klõpsake **Varahaldus** > **Seadistus** > **Töötajad** > **Eelistatud hooldustöötajad**.</span><span class="sxs-lookup"><span data-stu-id="b478e-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="b478e-120">Klõpsake uue kirje loomiseks suvandit **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b478e-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="b478e-121">Alustage "vaikimisi" hooldustöötaja või töötajate rühma loomisega.</span><span class="sxs-lookup"><span data-stu-id="b478e-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="b478e-122">See tähendab, et teete ainult valiku **Eelistatud hooldustöötajate grupi** väljal või **Eelistatud hooldustöötaja** väljal.</span><span class="sxs-lookup"><span data-stu-id="b478e-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="b478e-123">Alltoodud kuvatõmmisel näete näidet esimesest kirjest, milles on "Taotlused" on valitud rühmaks **Eelistatud hooldustöötajate rühm**.</span><span class="sxs-lookup"><span data-stu-id="b478e-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="b478e-124">Vaikimisi häälestust kasutatakse töökäsu planeerimisel, kui teine spetsiifilisem kombinatsioon ei vasta töökäsu sisule.</span><span class="sxs-lookup"><span data-stu-id="b478e-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="b478e-125">Uue kirje loomiseks korrake 2. etappi.</span><span class="sxs-lookup"><span data-stu-id="b478e-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="b478e-126">Tehke nõutavad valikud sõltuvalt eelistatud töötaja või töötajate grupi üksikasjalikust tasemest.</span><span class="sxs-lookup"><span data-stu-id="b478e-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="b478e-127">*Näide:* alltoodud kuvatõmmisel on kuuendas kirjes hooldustöötaja Shawn Richardson valitud eelistatud töötajaks.</span><span class="sxs-lookup"><span data-stu-id="b478e-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="b478e-128">Ta valitakse automaatselt töötellimuse planeerimisel, mis sisaldab vara "CH-BP1-03-02 ja hooldustöö tüüp "Oskuste hindamine", kui ta on planeeritud ajal saadaval.</span><span class="sxs-lookup"><span data-stu-id="b478e-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="b478e-129">Üldiselt, kui töötellimuse planeerimisel valitakse eelistatud hooldustöötaja, läbib Varahaldus kõik **eelistatud hooldustöötajate** kirjed, et kontrollida võimalikku vastet, kontrollides alati kõige spetsiifilisemat kombinatsiooni esimesena.</span><span class="sxs-lookup"><span data-stu-id="b478e-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="b478e-130">Kui vastet ei leita, kasutatakse "vaikimisi" kirjet, mille valikuks on kas **Eelistatud hooldustöötajate grupi** väli või **Eelistatud hooldustöötaja** väli.</span><span class="sxs-lookup"><span data-stu-id="b478e-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![Joonis 1](media/02-work-order-scheduling.png)

<span data-ttu-id="b478e-132">Saate seadistada ka *vastutavad* hooldustöötajad, keda saab valida hoolduse taotluse või töökäsu loomisel.</span><span class="sxs-lookup"><span data-stu-id="b478e-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="b478e-133">**Kõigi töökäskude** ja **Kõigi hooldusnõuete** korral saate valikut vajadusel redigeerida.</span><span class="sxs-lookup"><span data-stu-id="b478e-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="b478e-134">Lisateabe saamiseks vaadake [Vastutavad hooldustöötajad](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="b478e-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="b478e-135">Töötellimuse planeerimisel arvutatakse erinevad punktisummad, et määrata, millised töötajad peaksid läbi viima töötellimusega seotud tööd (need punktisummad seadistatakse **Varahalduse parameetrite** > **Töötellimuse planeerimise** lingil).</span><span class="sxs-lookup"><span data-stu-id="b478e-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="b478e-136">Kui kaks või rohkem eelistatud hooldustöötajat või vastutavat hooldustöötajat saavad töötellimuse planeerimisel sama punktisumma, valitakse juhuslikult üks töötaja.</span><span class="sxs-lookup"><span data-stu-id="b478e-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="b478e-137">Vastasel juhul on alati kõige kõrgema punktisummaga töötaja see, kes määratakse töötellimuse läbiviimiseks.</span><span class="sxs-lookup"><span data-stu-id="b478e-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

