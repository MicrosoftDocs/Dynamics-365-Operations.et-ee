---
title: Hoolduslepete arendamise ja sisseseadmise ülevaade
description: Hoolduslepetes saate määrata ressursid, mida kasutatakse tüüpilisel hoolduskülastusel, ning kuidas neid ressursse kliendiga arveldatakse.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86855e8893cdf5d6e53cb34465480ade06a6da95
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258490"
---
# <a name="develop-and-establish-service-agreements-overview"></a><span data-ttu-id="7daa0-103">Hoolduslepete arendamise ja sisseseadmise ülevaade</span><span class="sxs-lookup"><span data-stu-id="7daa0-103">Develop and establish service agreements overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7daa0-104">Hoolduslepetes saate määrata ressursid, mida kasutatakse tüüpilisel hoolduskülastusel, ning kuidas neid ressursse kliendiga arveldatakse.</span><span class="sxs-lookup"><span data-stu-id="7daa0-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="7daa0-105">Iga hoolduslepe on lisatud projekti juurde, mille kaudu kanded sisestatakse ja arveldatakse.</span><span class="sxs-lookup"><span data-stu-id="7daa0-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="7daa0-106">Te saate siiski ka arveldada hooldustellimuste kandeid vahetult projekti kaudu, ilma et ühendaksite hooldustellimuse esmalt hooldusleppega.</span><span class="sxs-lookup"><span data-stu-id="7daa0-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="7daa0-107">Võite otsustada toimida nii juhul, kui hooldustellimus on ühekordne hoolduskülastus ning hoolduskannete töötlemise vajadus kaalub kiiresti üles klienti puudutava üksikasjaliku hooldusleppe teabe haldamise ajaperioodil.</span><span class="sxs-lookup"><span data-stu-id="7daa0-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="7daa0-108">Teenuseleping</span><span class="sxs-lookup"><span data-stu-id="7daa0-108">Service agreement</span></span>

<span data-ttu-id="7daa0-109">Igas hooldusleppes peate määrama projekti, hooldusleppe ID ja hooldusleppegrupi.</span><span class="sxs-lookup"><span data-stu-id="7daa0-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="7daa0-110">Hooldusleppegruppi saab kasutada hoolduslepete sortimiseks ja korraldamiseks.</span><span class="sxs-lookup"><span data-stu-id="7daa0-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="7daa0-111">Hooldusleppe päis hõlmab järgmiseid sätteid, mis kehtivad kõikide lisatud lepinguridade puhul.</span><span class="sxs-lookup"><span data-stu-id="7daa0-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="7daa0-112">Kas hoolduslepe on peatatud.</span><span class="sxs-lookup"><span data-stu-id="7daa0-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="7daa0-113">Kui hoolduslepe on peatatud, ei saa hooldusleppest hooldustellimusi luua.</span><span class="sxs-lookup"><span data-stu-id="7daa0-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="7daa0-114">teenuselepingu kestus;</span><span class="sxs-lookup"><span data-stu-id="7daa0-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="7daa0-115">kuidas teenusetellimuste ridu teenusetellimustesse ühendada;</span><span class="sxs-lookup"><span data-stu-id="7daa0-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="7daa0-116">Kas hoolduslepe on mall.</span><span class="sxs-lookup"><span data-stu-id="7daa0-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="7daa0-117">Hooldusleppe päises saate seadistada ka kõik hooldusobjektid ja hooldustoimingud, mida saab hooldusleppe raames kasutada, sisestades kindlad hooldustoiminguid või hooldusobjektid, mis seotakse leppe eri ridadega.</span><span class="sxs-lookup"><span data-stu-id="7daa0-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="7daa0-118">Hooldusleppe päisest saate ka kopeerida hooldusleppe read või hooldusmalli read praegusesse hooldusleppesse.</span><span class="sxs-lookup"><span data-stu-id="7daa0-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="7daa0-119">Võite peatada hoolduslepped ja lõpetada individuaalsed hooldusleppe read.</span><span class="sxs-lookup"><span data-stu-id="7daa0-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="7daa0-120">Kui valite märkeruudu **Peatatud** hooldustellimuse real, ei saa te teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="7daa0-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="7daa0-121">Luua hooldusleppest automaatselt või käsitsi hooldustellimusi.</span><span class="sxs-lookup"><span data-stu-id="7daa0-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="7daa0-122">Kui valite märkeruudu **Seisatud** hooldustellimuse real, ei saa te teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="7daa0-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="7daa0-123">Luua hooldusleppe reast automaatselt või käsitsi hooldustellimusi.</span><span class="sxs-lookup"><span data-stu-id="7daa0-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="7daa0-124">kopeerida teenusetellimuse rea teise teenuselepingusse või teenusetellimusse.</span><span class="sxs-lookup"><span data-stu-id="7daa0-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="7daa0-125">Kui hoolduslepe on peatatud, lõpetatakse kõik seotud read hoolimata nende individuaalsest olekust.</span><span class="sxs-lookup"><span data-stu-id="7daa0-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="7daa0-126">Hooldusleppe read</span><span class="sxs-lookup"><span data-stu-id="7daa0-126">Service-agreement lines</span></span>

<span data-ttu-id="7daa0-127">Iga hooldusleppe rida kirjeldab üksikasjalikult kavandatava hooldustöö sisu.</span><span class="sxs-lookup"><span data-stu-id="7daa0-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="7daa0-128">Need read hõlmavad järgmisi sätteid.</span><span class="sxs-lookup"><span data-stu-id="7daa0-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="7daa0-129">Kandetüüp ja kandetüübi kirjeldus;</span><span class="sxs-lookup"><span data-stu-id="7daa0-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="7daa0-130">töötaja, kes teeb teenusetöid;</span><span class="sxs-lookup"><span data-stu-id="7daa0-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="7daa0-131">objektid, millel tuleb teenuselepingu alusel teenust teha;</span><span class="sxs-lookup"><span data-stu-id="7daa0-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="7daa0-132">sagedus, mil töö tehakse ning registreeritakse kaup, kulu ja tasukanded;</span><span class="sxs-lookup"><span data-stu-id="7daa0-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="7daa0-133">Kellaaja aken, mille ajal saab hooldustellimuste ridu grupeerida hooldustellimusse.</span><span class="sxs-lookup"><span data-stu-id="7daa0-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="7daa0-134">Hooldustoimingud, mida kasutatakse lepperidade komplektide grupeerimiseks tööülesannetesse ning hooldustehnikutele ja klientidele kokkuvõtlikult kirjeldamiseks, millist hooldustoimingut läbi viia.</span><span class="sxs-lookup"><span data-stu-id="7daa0-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="7daa0-135">Kas rida peatatakse.</span><span class="sxs-lookup"><span data-stu-id="7daa0-135">Whether a line is stopped.</span></span> <span data-ttu-id="7daa0-136">Kui rida peatatakse, ei saa te sellele üksikreale hooldustellimusi luua.</span><span class="sxs-lookup"><span data-stu-id="7daa0-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="7daa0-137">Projektisätted, nt kategooria ja rea atribuut.</span><span class="sxs-lookup"><span data-stu-id="7daa0-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7daa0-138">Seotud teemad</span><span class="sxs-lookup"><span data-stu-id="7daa0-138">Related topics</span></span>

[<span data-ttu-id="7daa0-139">Hoolduslepete loomine</span><span class="sxs-lookup"><span data-stu-id="7daa0-139">Create service agreements</span></span>](create-service-agreements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]