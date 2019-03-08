---
title: Teenuse tellimused
description: Hooldustellimus näitab hooldustehniku külastust kliendi laoalasse konkreetsel kuupäeval.
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
ms.openlocfilehash: 4da0b965f3719bc16b5a73538df111ff6df071be
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "366508"
---
# <a name="service-orders"></a><span data-ttu-id="dca60-103">Teenuse tellimused</span><span class="sxs-lookup"><span data-stu-id="dca60-103">Service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="dca60-104">Hooldustellimus näitab hooldustehniku külastust kliendi laoalasse konkreetsel kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="dca60-104">A service order represents a visit that a service technician makes to a customer site on a specific date.</span></span> <span data-ttu-id="dca60-105">Iga teenuse tellimus koosneb ühest või mitmest teenuse tellimuse reast.</span><span class="sxs-lookup"><span data-stu-id="dca60-105">Each service order consists of one or more service order lines.</span></span> <span data-ttu-id="dca60-106">Hooldustellimuse ridadel on toodud hooldustehniku töötunnid ning seotud kaubad, kulud ja tasud.</span><span class="sxs-lookup"><span data-stu-id="dca60-106">Service order lines represent the hours of work that must be performed by the service technician, and the related items, expenses, and fees.</span></span>

<span data-ttu-id="dca60-107">Hooldustellimuse reale saab lisada ülesandeid ja objekte.</span><span class="sxs-lookup"><span data-stu-id="dca60-107">You can attach tasks and objects to a service order line.</span></span> <span data-ttu-id="dca60-108">Seejärel saate grupeerida hooldustellimuse ridu ülesande või objekti järgi.</span><span class="sxs-lookup"><span data-stu-id="dca60-108">You can then group service order lines by task or by object.</span></span> <span data-ttu-id="dca60-109">Saate hooldustellimuste ridadele lisada ka laos loetletud kaupu.</span><span class="sxs-lookup"><span data-stu-id="dca60-109">You can also attach items that are listed in inventory to service order lines.</span></span>

## <a name="create-service-orders"></a><span data-ttu-id="dca60-110">Hooldustellimuste loomine</span><span class="sxs-lookup"><span data-stu-id="dca60-110">Create service orders</span></span>

<span data-ttu-id="dca60-111">Saate luua hooldustellimusi teenuseleppe ja selle leppe ridade alusel.</span><span class="sxs-lookup"><span data-stu-id="dca60-111">You can create service orders based on a service agreement and the lines that are contained in that agreement.</span></span> <span data-ttu-id="dca60-112">Kuid saate luua teenuseleppega seotud hooldustellimusi vaid leppes määratud perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="dca60-112">However, you can create service orders that are associated with a service agreement only in the period that is specified in the agreement.</span></span> <span data-ttu-id="dca60-113">Näiteks kui teenuselepe kehtib kalendriaasta 2011 kohta, saate luua hooldustellimusi leppe kohta alates 1. jaanuarist 2011 kuni 31. detsembrini 2011.</span><span class="sxs-lookup"><span data-stu-id="dca60-113">For example, if a service agreement is valid for the 2011 calendar year, you can create service orders for the agreement from January 1, 2011, and December 31, 2011.</span></span>

<span data-ttu-id="dca60-114">Saate hooldustellimusi luua ka eraldi, ilma nende määramiseta leppele.</span><span class="sxs-lookup"><span data-stu-id="dca60-114">You can also create service orders individually, without associating them with an agreement.</span></span> <span data-ttu-id="dca60-115">Neid hooldustellimusi saab kasutada plaanimata või ühekordsete teenusekülastuste haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="dca60-115">These service orders can be used to handle unscheduled or one-time service visits.</span></span> <span data-ttu-id="dca60-116">Näiteks märtsikuus soovib teie klient, et teenust tehtaks kahel masinal lisaks teenuseleppes määratud masinatele.</span><span class="sxs-lookup"><span data-stu-id="dca60-116">For example, in the month of March, your customer wants service to be performed on two machines, in addition to the machines that are specified in the service agreement.</span></span> <span data-ttu-id="dca60-117">Selle ülesande jaoks saate luua hooldustellimusi, kuid ärge seostage neid leppega.</span><span class="sxs-lookup"><span data-stu-id="dca60-117">For this task, you create service orders but do not associate them with an agreement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="dca60-118">Teenuseleppega mitte seostatud hooldustellimuste loomiseks peate valima märkeruudu <STRONG>Luba teenuseleppeta</STRONG> vormis <STRONG>Teenuste halduse parameetrid</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="dca60-118">To create service orders that are not associated with a service agreement, you must select the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form.</span></span></P>

<span data-ttu-id="dca60-119">**Stsenaarium**</span><span class="sxs-lookup"><span data-stu-id="dca60-119">**Scenario**</span></span>

<span data-ttu-id="dca60-120">Järgmises stsenaariumis kirjeldatakse olukorda, kus on kasulik luua hooldustellimus, mida ei ole seostatud teenuseleppega.</span><span class="sxs-lookup"><span data-stu-id="dca60-120">The following scenario describes another situation where it is useful to create a service order that is not associated with a service agreement.</span></span>

<span data-ttu-id="dca60-121">Ettevõtte dispetšer võtab vastu telefonikõne, kus nõutakse lifti erakorralist teenust.</span><span class="sxs-lookup"><span data-stu-id="dca60-121">The company dispatcher receives a call requesting emergency service on an elevator.</span></span> <span data-ttu-id="dca60-122">Teenuseleppe ja teenuse jaoks projekti seadistamiseks pole aega.</span><span class="sxs-lookup"><span data-stu-id="dca60-122">There is no time to set up a service agreement and a project for the service.</span></span> <span data-ttu-id="dca60-123">Seetõttu loob dispetšer hooldustellimuse otse vormis **Hooldustellimused**, lisab olemasolevale projektile hooldustellimuse ja loob hooldustellimuse read.</span><span class="sxs-lookup"><span data-stu-id="dca60-123">Therefore, the dispatcher creates a service order directly in the **Service orders** form, attaches the service order to an existing project, and creates the service order lines.</span></span> <span data-ttu-id="dca60-124">Dispetšer loob ka olemasolevale hooldustellimusele tööülesande või objekti seose, et kirjendada teenuselepinguga mitte seotud töö.</span><span class="sxs-lookup"><span data-stu-id="dca60-124">The dispatcher also creates a task or object relation for an existing service order, to record work that is not related to the service agreement.</span></span> <span data-ttu-id="dca60-125">Lisateavet vt teemadest [Hooldustellimuste loomine käsitsi](create-service-orders-manually.md) ja [Hooldustoimingute seoste loomine](create-service-task-relations.md).</span><span class="sxs-lookup"><span data-stu-id="dca60-125">For more information, see [Create service orders manually](create-service-orders-manually.md) and [Create service task relations](create-service-task-relations.md).</span></span>

## <a name="monitor-the-progress-of-service-orders"></a><span data-ttu-id="dca60-126">Hooldustellimuste edenemise jälgimine</span><span class="sxs-lookup"><span data-stu-id="dca60-126">Monitor the progress of service orders</span></span>

<span data-ttu-id="dca60-127">Hooldustellimuse edenemise jälgimiseks läbi eri meeskondade tööprotsesside saate seadistada hooldustellimustele etappide ja põhjusekoodide süsteemi.</span><span class="sxs-lookup"><span data-stu-id="dca60-127">To monitor the progress of a sales order through the different teams and work processes, you can set up a system of stages and reason codes for service orders.</span></span> <span data-ttu-id="dca60-128">Iga etapi jaoks saate määrata lubatud toimingud.</span><span class="sxs-lookup"><span data-stu-id="dca60-128">For each stage, you can specify the actions that are allowed.</span></span> <span data-ttu-id="dca60-129">Lisateavet põhjusekoodide kohta vt teemast [Põhjusekoodide loomine](create-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="dca60-129">For more information, see [Create reason codes](create-reason-codes.md).</span></span>

<span data-ttu-id="dca60-130">**Näide**</span><span class="sxs-lookup"><span data-stu-id="dca60-130">**Example**</span></span>

<span data-ttu-id="dca60-131">Dispetšer kinnitab hooldustellimuse.</span><span class="sxs-lookup"><span data-stu-id="dca60-131">A service order is approved by the dispatcher.</span></span> <span data-ttu-id="dca60-132">Dispetšer värskendab hooldustellimuse etappi ja määrab põhjusekoodi, mis näitab, et hooldustellimus on väljastatud hooldustehnikule.</span><span class="sxs-lookup"><span data-stu-id="dca60-132">The dispatcher updates the stage of the service order and specifies a reason code that indicates that the service order has been released to the service technician.</span></span> <span data-ttu-id="dca60-133">Tehnik läheb kliendi laoalasse ja täidab teenuse.</span><span class="sxs-lookup"><span data-stu-id="dca60-133">The technician goes to the customer site and performs the service.</span></span>

## <a name="specify-item-requirements-for-service-orders"></a><span data-ttu-id="dca60-134">Kaubavajaduse määramine hooldustellimuste jaoks</span><span class="sxs-lookup"><span data-stu-id="dca60-134">Specify item requirements for service orders</span></span>

<span data-ttu-id="dca60-135">Saate määrata hooldustellimuste jaoks vajalikke laokaupu.</span><span class="sxs-lookup"><span data-stu-id="dca60-135">You can specify the inventory items that are required for service orders.</span></span> <span data-ttu-id="dca60-136">Kuid hooldustellimus peab olema seotud projektiga.</span><span class="sxs-lookup"><span data-stu-id="dca60-136">However, the service order must be associated with a project.</span></span> <span data-ttu-id="dca60-137">Teenusetellimuste kaubavajadusi töödeldakse projekti kaudu.</span><span class="sxs-lookup"><span data-stu-id="dca60-137">Item requirements for service orders are processed through a project.</span></span> 

<span data-ttu-id="dca60-138">**Näide**</span><span class="sxs-lookup"><span data-stu-id="dca60-138">**Example**</span></span>

<span data-ttu-id="dca60-139">Teenuseleppest loodud hooldustellimusi töötleb dispetšer.</span><span class="sxs-lookup"><span data-stu-id="dca60-139">The service orders that are created from the service agreement are processed by the dispatcher.</span></span> <span data-ttu-id="dca60-140">Esmasel hooldustellimusel tõdeb dispetšer, et hooldustehnikul on vaja olulist varuosa, mida laos eelnevalt pole.</span><span class="sxs-lookup"><span data-stu-id="dca60-140">For the first service order, the dispatcher realizes that the service technician requires an important spare part that is not in the on-hand inventory.</span></span> <span data-ttu-id="dca60-141">Seetõttu loob dispetšer varuosa kaubavajaduse otse hooldustellimusest.</span><span class="sxs-lookup"><span data-stu-id="dca60-141">Therefore, the dispatcher creates an item requirement for the spare part directly from the service order.</span></span>

## <a name="move-and-post-lines"></a><span data-ttu-id="dca60-142">Ridade teisaldamine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="dca60-142">Move and post lines</span></span>

<span data-ttu-id="dca60-143">Hooldustehnik naaseb teenusekülastuselt ning muudab ja uuendab hooldustellimuste ridu.</span><span class="sxs-lookup"><span data-stu-id="dca60-143">A service technician returns from a service visit, and then modifies and updates the service order lines.</span></span> <span data-ttu-id="dca60-144">Teenusekülastuse ajal täitis tehnik teenusetööd, mis planeeriti järgmiseks teenusekülastuseks.</span><span class="sxs-lookup"><span data-stu-id="dca60-144">During the service visit, the technician performed a service job that was scheduled for the next service visit.</span></span> <span data-ttu-id="dca60-145">Seetõttu teisaldab tehnik read järgmiselt teenusekülastuselt praegusele teenusekülastusele.</span><span class="sxs-lookup"><span data-stu-id="dca60-145">Therefore, the technician moves the lines from the next service visit to the current service visit.</span></span> <span data-ttu-id="dca60-146">Tehnik sisestab hooldustellimuse.</span><span class="sxs-lookup"><span data-stu-id="dca60-146">The technician then posts the service order.</span></span> <span data-ttu-id="dca60-147">Lisateavet vt teemast [Hooldustellimuse ridade teisaldamine](move-service-order-lines.md).</span><span class="sxs-lookup"><span data-stu-id="dca60-147">For more information, see [Move service order lines](move-service-order-lines.md).</span></span>

## <a name="cancel-service-orders"></a><span data-ttu-id="dca60-148">Tühista teenuse tellimused</span><span class="sxs-lookup"><span data-stu-id="dca60-148">Cancel service orders</span></span>

<span data-ttu-id="dca60-149">Üks jaanuariks loodud muudest hooldustellimustest muutub aegunuks, sest töö tühistati.</span><span class="sxs-lookup"><span data-stu-id="dca60-149">One of the other service orders that was generated for the month of January becomes obsolete, because the job is canceled.</span></span> <span data-ttu-id="dca60-150">Seetõttu tühistab dispetšer hooldustellimuse.</span><span class="sxs-lookup"><span data-stu-id="dca60-150">Therefore, the service dispatcher cancels the service order.</span></span> <span data-ttu-id="dca60-151">Lisateavet vt teemast [Hooldustellimuste tühistamine](cancel-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="dca60-151">For more information, see [Cancel service orders](cancel-service-orders.md).</span></span>

## <a name="post-from-projects"></a><span data-ttu-id="dca60-152">Sisestamine projektidest</span><span class="sxs-lookup"><span data-stu-id="dca60-152">Post from projects</span></span>

<span data-ttu-id="dca60-153">Iga nädala lõpus soovib dispetšer sisestada kõik konkreetsele projektile lisatud hooldustellimused.</span><span class="sxs-lookup"><span data-stu-id="dca60-153">At the end of each week, the dispatcher wants to post all service orders that are attached to a specific project.</span></span> <span data-ttu-id="dca60-154">Seega määrab dispetšer asjakohase projekti asukoha vormil **Projektid** ja sisestab lõpetatud hooldustellimused.</span><span class="sxs-lookup"><span data-stu-id="dca60-154">Therefore, the dispatcher locates the relevant project in the **Projects** form and posts the service orders that have been completed.</span></span> <span data-ttu-id="dca60-155">Lisateavet vt teemast [Hooldustellimuste sisestamine (klassi vorm)](https://technet.microsoft.com/en-us/library/aa574685\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="dca60-155">For more information, see [Post service orders (class form)](https://technet.microsoft.com/en-us/library/aa574685\(v=ax.60\)).</span></span>

## <a name="delete-service-orders"></a><span data-ttu-id="dca60-156">Kustuta teenuse tellimused</span><span class="sxs-lookup"><span data-stu-id="dca60-156">Delete service orders</span></span>

<span data-ttu-id="dca60-157">Aasta teisel poolel otsustab teie klient, et teenusekülastused on liiga harvad.</span><span class="sxs-lookup"><span data-stu-id="dca60-157">During the second half of the year, your customer decides that the service visits are too infrequent.</span></span> <span data-ttu-id="dca60-158">Peate looma uue, sagedasema teenusekülastuste seeria teenuselepingu allesjäänud ajaks.</span><span class="sxs-lookup"><span data-stu-id="dca60-158">You must create a new, more frequent series of service visits for the remaining time on the service agreement.</span></span> <span data-ttu-id="dca60-159">Seepärast peate kustutama olemasolevad hooldustellimused ja looma uued hooldustellimused.</span><span class="sxs-lookup"><span data-stu-id="dca60-159">Therefore, you must delete the existing service orders and create new service orders.</span></span> <span data-ttu-id="dca60-160">Lisateavet vt teemast [Hooldustellimuste kustutamine](delete-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="dca60-160">For more information, see [Delete service orders](delete-service-orders.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="dca60-161">Vt ka</span><span class="sxs-lookup"><span data-stu-id="dca60-161">See also</span></span>

<span data-ttu-id="dca60-162">[Teenusetellimused (vorm)](https://technet.microsoft.com/en-us/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="dca60-162">[Service orders (form)](https://technet.microsoft.com/en-us/library/aa554361\(v=ax.60\))</span></span>

  


