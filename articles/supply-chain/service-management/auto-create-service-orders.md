---
title: Hooldustellimuste loomine automaatselt
description: Saate luua hoolduslepingutel põhinevaid hooldustellimusi hoolduslepingu kehtivusperioodiks.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0189a9f99ffbb6ed2387211ba9e3b9f3bcdb3b52
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561198"
---
# <a name="automatically-create-service-orders"></a><span data-ttu-id="af1d9-103">Hooldustellimuste loomine automaatselt</span><span class="sxs-lookup"><span data-stu-id="af1d9-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="af1d9-104">Saate luua hoolduslepingutel põhinevaid hooldustellimusi hoolduslepingu kehtivusperioodiks.</span><span class="sxs-lookup"><span data-stu-id="af1d9-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="af1d9-105">Hoolduslepingust loodavad hooldustellimused lisatakse kõik hoolduslepingule.</span><span class="sxs-lookup"><span data-stu-id="af1d9-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="af1d9-106">Teenusetellimused luuakse automaatselt järgmistest sätetest:</span><span class="sxs-lookup"><span data-stu-id="af1d9-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="af1d9-107">Hoolduslepingu intervall, mis on hoolduslepingu ridadel seadistatud.</span><span class="sxs-lookup"><span data-stu-id="af1d9-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="af1d9-108">Hoolduslepingu intervall näitab hooldustellimuste ridade loomist sagedust.</span><span class="sxs-lookup"><span data-stu-id="af1d9-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="af1d9-109">Lisateavet vaadake jaotisest [Hooldusintervallid](service-intervals.md).</span><span class="sxs-lookup"><span data-stu-id="af1d9-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="af1d9-110">Periood, mille määratlete hooldusperioodi määramiseks väljadel **Alates kuupäevast** ja **Kuupäevani** vormil **Hooldustellimuste loomine**.</span><span class="sxs-lookup"><span data-stu-id="af1d9-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="af1d9-111">Lisateavet vaadake jaotisest [Hooldustellimuste loomine automaatselt](create-service-orders-automatically.md)</span><span class="sxs-lookup"><span data-stu-id="af1d9-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="af1d9-112">Suvand **Hooldustellimuste ühendamine** hooldusleppe päises.</span><span class="sxs-lookup"><span data-stu-id="af1d9-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="af1d9-113">See suvand määrab, kas hooldustellimuse read luuakse hoolduslepingu alusel ja mis ühendab hooldustellimused lähtuvalt töötajast, hooldustoimingust, hooldusobjektist või hoolduslepingust.</span><span class="sxs-lookup"><span data-stu-id="af1d9-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="af1d9-114">Lisateavet vaadake jaotisest [Hooldustellimuste ühendamine](combine-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="af1d9-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="af1d9-115">Hoolduslepingu real olev suvand **Kellaaja aken**.</span><span class="sxs-lookup"><span data-stu-id="af1d9-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="af1d9-116">Kellaaja aken määrab, kui kaugele saab hooldustellimus liikuda oma arvutatud kuupäeva suhtes.</span><span class="sxs-lookup"><span data-stu-id="af1d9-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="af1d9-117">Lisateavet vaadake jaotisest [Kellaaja aknad](time-windows.md).</span><span class="sxs-lookup"><span data-stu-id="af1d9-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="af1d9-118">Kui hooldustellimuse jaoks määratletud päev ei ole avatuna kalendris, mille valisite vormil <STRONG>Teenuste halduse parameetrid</STRONG>, kuvatakse teade kalendri konflikti kohta.</span><span class="sxs-lookup"><span data-stu-id="af1d9-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="af1d9-119">Seda teadet võite ohutult eirata ning hooldustellimus luuakse ikkagi, kuigi kuupäev on kalendris suletud.</span><span class="sxs-lookup"><span data-stu-id="af1d9-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="af1d9-120">Näide 1</span><span class="sxs-lookup"><span data-stu-id="af1d9-120">Example 1</span></span>

<span data-ttu-id="af1d9-121">Hooldusleping kestab 1. jaanuarist 2012 kuni 31. detsembrini 2012.</span><span class="sxs-lookup"><span data-stu-id="af1d9-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="af1d9-122">Kui määratlete vormil **Hooldustellimuste loomine** hooldusperioodiks ajavahemiku 1. novembrist 2012 kuni 1. veebruarini 2013, siis luuakse hooldustellimusi ajavahemikus 1. novembrist 2012 kuni 31. detsembrini 2012.</span><span class="sxs-lookup"><span data-stu-id="af1d9-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="af1d9-123">Näide 2</span><span class="sxs-lookup"><span data-stu-id="af1d9-123">Example 2</span></span>

<span data-ttu-id="af1d9-124">Hooldusleping kestab 1. jaanuarist 2012 kuni 31. detsembrini 2012.</span><span class="sxs-lookup"><span data-stu-id="af1d9-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="af1d9-125">Hoolduslepingule lisatakse kaks hoolduslepingu rida.</span><span class="sxs-lookup"><span data-stu-id="af1d9-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="af1d9-126">Esimesel hoolduslepingu real on alguskuupäev 2. jaanuar 2012 ja lõppkuupäev 1. märts 2012.</span><span class="sxs-lookup"><span data-stu-id="af1d9-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="af1d9-127">Teisel hoolduslepingu real on alguskuupäev 1. aprill 2012 ja lõppkuupäev 31. detsember 2012.</span><span class="sxs-lookup"><span data-stu-id="af1d9-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="af1d9-128">Te määrate vormil **Hooldustellimuste loomine** perioodi, mis on ajavahemikus 1. oktoober 2012 kuni 31. detsember 2012.</span><span class="sxs-lookup"><span data-stu-id="af1d9-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="af1d9-129">Seetõttu luuakse hooldustellimused ainult teisele lepingureale, sest esimese lepingurea alguskuupäev ja lõppkuupäev on enne hooldustellimuse perioodi, mille määratlesite.</span><span class="sxs-lookup"><span data-stu-id="af1d9-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  


