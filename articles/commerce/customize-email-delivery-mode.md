---
title: Tehingumeilide kohandamine tarneviisi alusel
description: Selles teemas kirjeldatakse, kuidas seadistada kohandatud meilimalle kindlate teatisetüüpide ja tarneviiside jaoks Microsoft Dynamics 365 Commerce'is.
author: stuharg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: f4ecb990cfe792e92142f922c43c71ef8494e117
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031844"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="47f4a-103">Tehingumeilide kohandamine tarneviisi alusel</span><span class="sxs-lookup"><span data-stu-id="47f4a-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="47f4a-104">Selles teemas kirjeldatakse, kuidas seadistada kohandatud meilimalle kindlate teatisetüüpide ja tarneviiside jaoks Microsoft Dynamics 365 Commerce'is.</span><span class="sxs-lookup"><span data-stu-id="47f4a-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="47f4a-105">Tehingumeile saab nüüd kohandada teatisetüübi (nt **Tellimus on loodud**, **Tellimus on pakitud** või **Tellimus on arveldatud**) ja tarneviisi (nt üleöö, kauplusest kättesaamine või tänaval kättesaamine) kombinatsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="47f4a-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="47f4a-106">Kohandatud tehingumeilid võimaldavad jaemüüjatel täita klientide tellimusi viisil, mis sobib tellimuse tarneviisiga.</span><span class="sxs-lookup"><span data-stu-id="47f4a-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="47f4a-107">Näiteks sündmust „Tellimus on pakitud“ saab kohandada nii, et see annab juhiseid tänaval kättesaamise kohta sellistele klientidele, kes valisid tänaval kättesaamise.</span><span class="sxs-lookup"><span data-stu-id="47f4a-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="47f4a-108">Teise võimalusena võib see anda kättetoimetaja ja tarnimise teavet klientidele, kes otsustavad oma tellimuse tarnida.</span><span class="sxs-lookup"><span data-stu-id="47f4a-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="47f4a-109">Kohandatud tehingumeilide funktsiooni kasutamiseks peate esmalt sisse lülitama funktsiooni **Kohanda tehingumeilimalle tarneviisi järgi**, minnes Commerce'i peakontoris jaotisse **Tööruumid \> Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="47f4a-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="47f4a-110">Meile saab kohandada tarneviisi järgi järgmiste teatisetüüpide korral.</span><span class="sxs-lookup"><span data-stu-id="47f4a-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="47f4a-111">**Tellimuse tühistamine** – see meiliteatise tüüp on uus.</span><span class="sxs-lookup"><span data-stu-id="47f4a-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="47f4a-112">**Tellimus loodud**</span><span class="sxs-lookup"><span data-stu-id="47f4a-112">**Order created**</span></span>
- <span data-ttu-id="47f4a-113">**Tellimus on kinnitatud.**</span><span class="sxs-lookup"><span data-stu-id="47f4a-113">**Order confirmed**</span></span>
- <span data-ttu-id="47f4a-114">**Tellimus on arveldatud** – see meiliteatise tüüp on uus.</span><span class="sxs-lookup"><span data-stu-id="47f4a-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="47f4a-115">Seda saab kasutada teatisetüübi **Tellimus on lähetatud** asemel, mis saadab teatise iga arvesündmuse kohta, mille tarneviis on lähetamine (mitte järeletulemine, kaasavõtmine ega elektrooniline tarneviis).</span><span class="sxs-lookup"><span data-stu-id="47f4a-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="47f4a-116">**Tellimus on komplekteeritud**</span><span class="sxs-lookup"><span data-stu-id="47f4a-116">**Order picked**</span></span>
- <span data-ttu-id="47f4a-117">**Tellimus on pakitud**</span><span class="sxs-lookup"><span data-stu-id="47f4a-117">**Order packed**</span></span>
- <span data-ttu-id="47f4a-118">**Tellimus on järeletulemiseks valmis** – seda teatisetüüpi saab kohandada tarneviisi järgi ainult siis, kui funktsioon **Mitme järeletulemispõhise tarneviisi tugi** on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="47f4a-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="47f4a-119">Sellisel juhul on see teatisetüüp funktsionaalselt samaväärne teatisetüübiga **Tellimus on pakitud**.</span><span class="sxs-lookup"><span data-stu-id="47f4a-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="47f4a-120">**Makse nurjus**</span><span class="sxs-lookup"><span data-stu-id="47f4a-120">**Payment failed**</span></span>
- <span data-ttu-id="47f4a-121">**Asendustellimus on loodud**</span><span class="sxs-lookup"><span data-stu-id="47f4a-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="47f4a-122">Meilimallide konfigureerimine kindlate tarneviiside jaoks</span><span class="sxs-lookup"><span data-stu-id="47f4a-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="47f4a-123">Selle toimingu puhul eeldatakse, et olete juba loonud uued kohandatud meilimallid ja lisanud need lehele **Organisatsiooni meilimallid**.</span><span class="sxs-lookup"><span data-stu-id="47f4a-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="47f4a-124">Lisateavet meilimallide loomise ja üleslaadimise kohta leiate teemast [Meilimallide loomine tehingusündmuste jaoks](email-templates-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="47f4a-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="47f4a-125">Meilimallide konfigureerimiseks kindlate tarneviiside jaoks Commerce'i peakontoris toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="47f4a-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="47f4a-126">Avage **Commerce'i meiliteatise profiil**.</span><span class="sxs-lookup"><span data-stu-id="47f4a-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="47f4a-127">Valige jaotises **Jaemüügisündmuse teatise sätted** olemasolev teatisetüüp.</span><span class="sxs-lookup"><span data-stu-id="47f4a-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="47f4a-128">Samal ajal kui teatisetüüp on ikka valitud, valige **Konfigureeri tarneviise**.</span><span class="sxs-lookup"><span data-stu-id="47f4a-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="47f4a-129">Valige dialoogiboksis **Tarneviisid** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="47f4a-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="47f4a-130">Valige tarneviis uuel real väljal **Tarneviis**.</span><span class="sxs-lookup"><span data-stu-id="47f4a-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="47f4a-131">Valige väljal **Meili ID** meilimall, mille soovite vastendada tarneviisiga.</span><span class="sxs-lookup"><span data-stu-id="47f4a-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="47f4a-132">Märkige ruut **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="47f4a-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="47f4a-133">Täiendavate tarneviiside lisamiseks korrake samme 4–7.</span><span class="sxs-lookup"><span data-stu-id="47f4a-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="47f4a-134">Kui olete lõpetanud, valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="47f4a-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="47f4a-135">Kui müügitellimuse ridade tarneviise on mitu, kasutatakse vaikemalli.</span><span class="sxs-lookup"><span data-stu-id="47f4a-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="47f4a-136">Vaikemall on mall, mis on lehel **Commerce'i meiliteatise profiil** vastendatud teatisetüübiga.</span><span class="sxs-lookup"><span data-stu-id="47f4a-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="47f4a-137">Kui müügitellimusel on tarneviis, mida pole kohandatud meilimalli jaoks konfigureeritud, kasutatakse vaikemeilimalli.</span><span class="sxs-lookup"><span data-stu-id="47f4a-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47f4a-138">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="47f4a-138">Additional resources</span></span>

[<span data-ttu-id="47f4a-139">Kõnekeskuse tellimuste loomine</span><span class="sxs-lookup"><span data-stu-id="47f4a-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="47f4a-140">Kassas tarneviisi muutmine</span><span class="sxs-lookup"><span data-stu-id="47f4a-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)
