---
title: "Tühista teenuse tellimused"
description: "Saate tühistada hooldustellimuse või hooldustellimuse rea hooldustellimusest endast või tühistada mitu hooldustellimust, käitades perioodilise töö."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8e5ad119c28bba18b75bb5ed7854e94a4e734d55
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="cancel-service-orders"></a><span data-ttu-id="2a96a-103">Tühista teenuse tellimused</span><span class="sxs-lookup"><span data-stu-id="2a96a-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2a96a-104">Saate tühistada hooldustellimuse või hooldustellimuse rea hooldustellimusest endast või tühistada mitu hooldustellimust, käitades perioodilise töö.</span><span class="sxs-lookup"><span data-stu-id="2a96a-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2a96a-105">Hooldustellimusi ei saa tühistada, kui hooldustellimuse etapp tühistamist ei luba, kui hooldustellimusel on kaubavajadused või kui hooldustellimus on juba sisestatud.</span><span class="sxs-lookup"><span data-stu-id="2a96a-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="2a96a-106">Teenusetellimuse tühistamine teenusetellimuse vormilt</span><span class="sxs-lookup"><span data-stu-id="2a96a-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="2a96a-107">Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="2a96a-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="2a96a-108">Valige hooldustellimus ja klõpsake toimingupaanil nuppu **Tühista tellimus**.</span><span class="sxs-lookup"><span data-stu-id="2a96a-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="2a96a-109">Teenusetellimuse rea tühistamine</span><span class="sxs-lookup"><span data-stu-id="2a96a-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="2a96a-110">Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="2a96a-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="2a96a-111">Topeltklõpsake hooldustellimust, mis sisaldab rida, mille soovite tühistada.</span><span class="sxs-lookup"><span data-stu-id="2a96a-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="2a96a-112">Valige hooldustellimuse rida, mille soovite tühistada, ja klõpsake seejärel valikut **Tellimusrea tühistamine**, et muuta rida olekusse **Tühistatud**.</span><span class="sxs-lookup"><span data-stu-id="2a96a-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="2a96a-113">Hooldustellimuse rea tühistamise tagasivõtmiseks ja oleku muutmiseks tagasi olekusse <STRONG>Loodud</STRONG>, klõpsake valikut <STRONG>Tühista loobumine</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2a96a-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="2a96a-114">Mitme teenusetellimuse tühistamine</span><span class="sxs-lookup"><span data-stu-id="2a96a-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="2a96a-115">Klõpsake valikuid **Teenuste haldus** \> **Perioodiline** \> **Hooldustellimused** \> **Tühista hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="2a96a-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="2a96a-116">Klõpsake nuppu **Vali**.</span><span class="sxs-lookup"><span data-stu-id="2a96a-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="2a96a-117">Valige vormi **Päring** veerust **Kriteeriumid** hooldustellimused, mille soovite tühistada.</span><span class="sxs-lookup"><span data-stu-id="2a96a-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="2a96a-118">Klõpsake vormi **Päring** sulgemiseks valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a96a-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="2a96a-119">Märkige ruut **Näita teabelogi**, et luua tühistatud hooldustellimuste loendit kuvav teabelogi.</span><span class="sxs-lookup"><span data-stu-id="2a96a-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="2a96a-120">Märkige ruut **Tühista loobumine**, kui soovite tühistada hooldustellimuse olekut **Tühistatud**.</span><span class="sxs-lookup"><span data-stu-id="2a96a-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="2a96a-121">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a96a-121">Click **OK**.</span></span>

<span data-ttu-id="2a96a-122">Valitud hooldustellimused kas tühistatakse või pööratakse nende edenemise olek **Tühistatud** olekuks **Pooleli**.</span><span class="sxs-lookup"><span data-stu-id="2a96a-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2a96a-123">Kui märgite ruudu <STRONG>Tühista loobumine</STRONG>, siis tühistatakse hooldustellimused edenemisolekuga <STRONG>Tühistatud</STRONG> ja hooldustellimusi edenemisolekuga <STRONG>Pooleli</STRONG> ei tühistata.</span><span class="sxs-lookup"><span data-stu-id="2a96a-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  



