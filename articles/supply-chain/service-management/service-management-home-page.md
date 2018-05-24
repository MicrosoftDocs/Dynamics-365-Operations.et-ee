---
title: Teenuste halduse
description: "Teenuste haldusega saate luua teenuseleppeid ja hooldustellimusi, hallata hooldustellimusi ja kliendi päringuid ning hallata ja analüüsida teenuste pakkumist klientidele."
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: et-ee
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a><span data-ttu-id="b3593-103">Teenuste halduse</span><span class="sxs-lookup"><span data-stu-id="b3593-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b3593-104">**Teenuste haldusega** saate luua teenuseleppeid ja hooldustellimusi, hallata hooldustellimusi ja kliendi päringuid ning hallata ja analüüsida teenuste pakkumist klientidele.</span><span class="sxs-lookup"><span data-stu-id="b3593-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="b3593-105">Hoolduslepingutega saate määrata ressursid, mida kasutatakse tüüpilisel teenusekülastusel.</span><span class="sxs-lookup"><span data-stu-id="b3593-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="b3593-106">Hoolduslepingutega saate ka vaadata, kuidas neid ressursse kliendile arveldatakse.</span><span class="sxs-lookup"><span data-stu-id="b3593-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="b3593-107">Hooldusleping võib sisaldada ka teenustaseme lepingut, millega määratakse reageerimisaeg ja pakutakse võimalusi tegelikult kulunud aega salvestada.</span><span class="sxs-lookup"><span data-stu-id="b3593-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="b3593-108">Saate luua hooldustellimusi, et hallata teavet hooldustehniku plaanitud ja plaanimata külastuste kohta kliendi asukohta.</span><span class="sxs-lookup"><span data-stu-id="b3593-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="b3593-109">Hooldustellimustes on näiteks järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="b3593-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="b3593-110">Hooldustehniku kulutatav töötundide arv</span><span class="sxs-lookup"><span data-stu-id="b3593-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="b3593-111">Teenuse või parandustöö tüüp</span><span class="sxs-lookup"><span data-stu-id="b3593-111">The type of service or repair</span></span>

3.  <span data-ttu-id="b3593-112">Parandatav kaup, sh sümptomite ja diagnoosi üksikasjad</span><span class="sxs-lookup"><span data-stu-id="b3593-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="b3593-113">Hooldamise või parandamisega seotud kulud ja tasud</span><span class="sxs-lookup"><span data-stu-id="b3593-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="b3593-114">Kliendid saavad esitada teenusenõudeid interneti kaudu, kasutades ettevõtteportaali.</span><span class="sxs-lookup"><span data-stu-id="b3593-114">Customers can submit service requests through the Internet by using the Enterprise Portal.</span></span> <span data-ttu-id="b3593-115">Saate neid taotlusi vastu võtta, käidelda ja edasi saata.</span><span class="sxs-lookup"><span data-stu-id="b3593-115">You can receive, process, and dispatch these requests.</span></span> <span data-ttu-id="b3593-116">Pärast hooldustellimuse loomist saate kasutada edenemise jälgimiseks hoolduse etappe ning määrata reegleid igas etapis tehtavate toimingute kohta.</span><span class="sxs-lookup"><span data-stu-id="b3593-116">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="b3593-117">Kui hooldustellimus on lõpetatud, saate tellimuse lõpetatuks märkida ja seejärel arveldusprotsessi alustamiseks sisestada.</span><span class="sxs-lookup"><span data-stu-id="b3593-117">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="b3593-118">Aruandlustarvikutega saate jälgida hooldustellimuse veeriseid ja tellimuste kandeid ning printida töökirjeldusi ja sissetulekuid.</span><span class="sxs-lookup"><span data-stu-id="b3593-118">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="b3593-119">Äriprotsessid</span><span class="sxs-lookup"><span data-stu-id="b3593-119">Business processes</span></span>

<span data-ttu-id="b3593-120">Järgmisel diagrammil on näha kõrge taseme äriprotsessid **teenuste halduseks** ja kohad, kus teenuseprotsessid liituvad teiste moodulitega rakenduses Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b3593-120">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="b3593-121">[![Teenuste halduse äriprotsessi diagramm](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="b3593-121">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="b3593-122">Hoolduse halduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="b3593-122">Service management at a glance</span></span>

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b3593-123">Olulised ülesanded</span><span class="sxs-lookup"><span data-stu-id="b3593-123">Important tasks</span></span></p></th>
<th><p><span data-ttu-id="b3593-124">Peamised vormid</span><span class="sxs-lookup"><span data-stu-id="b3593-124">Primary forms</span></span></p></th>
<th><p><span data-ttu-id="b3593-125">Levinud aruanded</span><span class="sxs-lookup"><span data-stu-id="b3593-125">Popular reports</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3593-126">Hoolduslepete täitmine</span><span class="sxs-lookup"><span data-stu-id="b3593-126">Fulfill service agreements</span></span></a></p></td>
<td><p><span data-ttu-id="b3593-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Teenuseleping (vorm)</a></span><span class="sxs-lookup"><span data-stu-id="b3593-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Service agreements (form)</a></span></span></p></td>
<td><p><span data-ttu-id="b3593-128"><strong>Teenuse tellimuse kasum</strong></span><span class="sxs-lookup"><span data-stu-id="b3593-128"><strong>Service order margin</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3593-129">Kliendipäringute käsitlemine</span><span class="sxs-lookup"><span data-stu-id="b3593-129">Handle customer inquiries</span></span></a></p></td>
<td><p><span data-ttu-id="b3593-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Teenusetellimused (vorm)</a></span><span class="sxs-lookup"><span data-stu-id="b3593-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Service orders (form)</a></span></span></p></td>
<td><p><span data-ttu-id="b3593-131"><strong>Töö kirjeldus</strong></span><span class="sxs-lookup"><span data-stu-id="b3593-131"><strong>Work description</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b3593-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Lähetustahvel (vorm)</a></span><span class="sxs-lookup"><span data-stu-id="b3593-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Dispatch board (form)</a></span></span></p></td>
<td><p><span data-ttu-id="b3593-133"><strong>Kanne – kordustellimus</strong></span><span class="sxs-lookup"><span data-stu-id="b3593-133"><strong>Transaction - subscription</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b3593-134"><strong>Kordustellimuse tasu kanded</strong></span><span class="sxs-lookup"><span data-stu-id="b3593-134"><strong>Subscription fee transactions</strong></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a><span data-ttu-id="b3593-135">Hoolduse halduse ühendamine</span><span class="sxs-lookup"><span data-stu-id="b3593-135">Integration of Service management</span></span>

<span data-ttu-id="b3593-136">Teenuste haldust saab liita järgmiste moodulitega rakenduses Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b3593-136">Service management can be integrated with the following modules in Microsoft Dynamics 365 for Finance and Operations:</span></span>

  - [<span data-ttu-id="b3593-137">Müük ja turundus</span><span class="sxs-lookup"><span data-stu-id="b3593-137">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)

  - [<span data-ttu-id="b3593-138">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="b3593-138">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


