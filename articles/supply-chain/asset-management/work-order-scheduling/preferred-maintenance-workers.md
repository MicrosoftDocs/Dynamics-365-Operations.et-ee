---
title: Eelistatud hooldustöötajate seadistus
description: Selles teemas selgitatakse, kuidas sätestada eelistatud hooldustöötajaid varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887407"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="242b9-103">Eelistatud hooldustöötajad</span><span class="sxs-lookup"><span data-stu-id="242b9-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="242b9-104">Saate töötellimuse planeerimisel eelistada, millised hooldustöölised on määratud töötellimuste läbiviimiseks.</span><span class="sxs-lookup"><span data-stu-id="242b9-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="242b9-105">Selle funktsiooni kasutamine on valikuline, kuid see aitab teil töö läbiviimiseks valida kõige kvalifitseerituma hooldustöötaja tema oskuste ja pädevuste alusel.</span><span class="sxs-lookup"><span data-stu-id="242b9-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="242b9-106">Seetõttu kasutatakse töötellimuse planeerimisel **eelistatud hooldustöötaja** seadistust, et määrata, kas kindel hooldustöötaja või töötajate grupp tuleks töötellimuse jaoks planeerida.</span><span class="sxs-lookup"><span data-stu-id="242b9-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="242b9-107">Planeeritakse ainult hooldustöötajaid, kes on saadaval planeerimise ajal.</span><span class="sxs-lookup"><span data-stu-id="242b9-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="242b9-108">Kui eelistatud hooldustöötaja häälestus ühtib planeerimisel töötellimusega, kuid hooldustöötaja on määratud teistele töödele, planeeritakse töötellimus teisele, saadaolevale hooldustöötajale.</span><span class="sxs-lookup"><span data-stu-id="242b9-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="242b9-109">Enne kui saate sätestada eelistatud hooldustöötajaid, peate esiteks sätestama hooldustöötajad ja töötajate rühmad, mis peaksid valikuks saadaval olema.</span><span class="sxs-lookup"><span data-stu-id="242b9-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="242b9-110">Hooldustöötajate ja töötajate gruppide sätestamise kirjeldust vaadake teemast [Hooldustöötajad ja töötajate rühmad](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="242b9-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="242b9-111">Eelistatud hooldustöötajate sätestamine</span><span class="sxs-lookup"><span data-stu-id="242b9-111">Set up preferred workers</span></span>

<span data-ttu-id="242b9-112">Eelistatud hooldustöötaja või töötajate grupp võib olla seotud konkreetse</span><span class="sxs-lookup"><span data-stu-id="242b9-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="242b9-113">kaubandus</span><span class="sxs-lookup"><span data-stu-id="242b9-113">trade</span></span>  
- <span data-ttu-id="242b9-114">Hooldustöö  tüübi variant</span><span class="sxs-lookup"><span data-stu-id="242b9-114">maintenance job type variant</span></span>  
- <span data-ttu-id="242b9-115">Hooldustöö tüüp</span><span class="sxs-lookup"><span data-stu-id="242b9-115">maintenance job type</span></span>  
- <span data-ttu-id="242b9-116">Hooldustöö tüübi kategooria</span><span class="sxs-lookup"><span data-stu-id="242b9-116">maintenance job type category</span></span>  
- <span data-ttu-id="242b9-117">vara</span><span class="sxs-lookup"><span data-stu-id="242b9-117">asset</span></span>  
- <span data-ttu-id="242b9-118">Vara tüüp</span><span class="sxs-lookup"><span data-stu-id="242b9-118">asset type</span></span>  

<span data-ttu-id="242b9-119">Või nende valikute kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="242b9-119">or a combination of those selections.</span></span> <span data-ttu-id="242b9-120">Mida rohkem valikuid te sama kirje jaoks teete, seda täpsem on teie seadistus.</span><span class="sxs-lookup"><span data-stu-id="242b9-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="242b9-121">Klõpsake **Varahaldus** > **Seadistus** > **Töötajad** > **Eelistatud hooldustöötajad**.</span><span class="sxs-lookup"><span data-stu-id="242b9-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="242b9-122">Klõpsake uue kirje loomiseks suvandit **Uus**.</span><span class="sxs-lookup"><span data-stu-id="242b9-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="242b9-123">Alustage, luues "vaikimisi" hooldustöötaja või töötajate grupi seadistuse, millel puuduvad valikud ülaltoodud täpploendi väljadel.</span><span class="sxs-lookup"><span data-stu-id="242b9-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="242b9-124">See tähendab, et teete ainult valiku **Eelistatud hooldustöötajate grupi** väljal või **Eelistatud hooldustöötaja** väljal.</span><span class="sxs-lookup"><span data-stu-id="242b9-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="242b9-125">Alltoodud joonisel näete näidet esimesest kirjest, milles on valitud eelistatud hooldustöötajate grupiks "Taotlused".</span><span class="sxs-lookup"><span data-stu-id="242b9-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="242b9-126">Vaikimisi häälestust kasutatakse töökäsu planeerimisel siis, kui teine spetsiifilisem kombinatsioon ei vasta töökäsu planeerimisel töökäsu sisule.</span><span class="sxs-lookup"><span data-stu-id="242b9-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="242b9-127">Uue kirje loomiseks korrake 2. etappi.</span><span class="sxs-lookup"><span data-stu-id="242b9-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="242b9-128">Tehke nõutavad valikud sõltuvalt eelistatud töötaja või töötajate grupi üksikasjalikust tasemest.</span><span class="sxs-lookup"><span data-stu-id="242b9-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="242b9-129">*Näide:* alltoodud joonisel on kuuendas kirjes hooldustöötaja Shawn Richardson valitud eelistatud töötajaks.</span><span class="sxs-lookup"><span data-stu-id="242b9-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="242b9-130">Ta valitakse automaatselt töötellimuse planeerimisel, mis sisaldab vara "CH-BP1-03-02 ja hooldustöö tüüp "Oskuste hindamine", kui ta on planeeritud ajal saadaval.</span><span class="sxs-lookup"><span data-stu-id="242b9-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="242b9-131">Üldiselt, kui töötellimuse planeerimisel valitakse eelistatud hooldustöötaja, läbib Varahaldus kõik **eelistatud hooldustöötajate** kirjed, et kontrollida võimalikku vastet, kontrollides alati kõige spetsiifilisemat kombinatsiooni esimesena.</span><span class="sxs-lookup"><span data-stu-id="242b9-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="242b9-132">Kui vastet ei leita, kasutatakse "vaikimisi" kirjet, mille valikuks on kas **Eelistatud hooldustöötajate grupi** väli või **Eelistatud hooldustöötaja** väli.</span><span class="sxs-lookup"><span data-stu-id="242b9-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![Joonis 1](media/02-work-order-scheduling.png)

<span data-ttu-id="242b9-134">Saate seadistada ka vastutavad hooldustöötajad, keda saab valida hoolduse taotluse või töötellimuse loomisel.</span><span class="sxs-lookup"><span data-stu-id="242b9-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="242b9-135">**Kõigi töötellimuste** ja **Kõigi hooldusnõuete** korral saate valikut vajadusel redigeerida.</span><span class="sxs-lookup"><span data-stu-id="242b9-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="242b9-136">Lisateabe saamiseks vaadake [Vastutavad hooldustöötajad](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="242b9-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="242b9-137">Töötellimuse planeerimisel arvutatakse erinevad punktisummad, et määrata, millised töötajad peaksid läbi viima töötellimusega seotud tööd (need punktisummad seadistatakse **Varahalduse parameetrite** > **Töötellimuse planeerimise** lingil).</span><span class="sxs-lookup"><span data-stu-id="242b9-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="242b9-138">Kui kaks või rohkem eelistatud hooldustöötajat või vastutavat hooldustöötajat saavad töötellimuse planeerimisel sama punktisumma, valitakse juhuslikult üks töötaja.</span><span class="sxs-lookup"><span data-stu-id="242b9-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="242b9-139">Vastasel juhul on alati kõige kõrgema punktisummaga töötaja see, kes määratakse töötellimuse läbiviimiseks.</span><span class="sxs-lookup"><span data-stu-id="242b9-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

