---
title: teenustellimuste loomine käsitsi
description: Hooldustellimusi saate luua käsitsi hoolduslepete või vormi **Hooldustellimused** abil.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9fbcdaa50a8f13247c13c1885cdb4ab7f5f39a47
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "310917"
---
# <a name="create-service-orders-manually"></a><span data-ttu-id="634e6-103">teenustellimuste loomine käsitsi</span><span class="sxs-lookup"><span data-stu-id="634e6-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="634e6-104">Hooldustellimusi saate luua käsitsi hoolduslepete või vormi **Hooldustellimused** abil.</span><span class="sxs-lookup"><span data-stu-id="634e6-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="634e6-105">teenustellimuse saate luua ka projekti abil.</span><span class="sxs-lookup"><span data-stu-id="634e6-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="634e6-106">Hooldustellimuste loomiseks saate kasutada automaatseid protsesse.</span><span class="sxs-lookup"><span data-stu-id="634e6-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="634e6-107">Hooldustellimuse käsitsi loomine hooldusleppest</span><span class="sxs-lookup"><span data-stu-id="634e6-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="634e6-108">Klõpsake valikut **Hooldushaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldusleppegrupid**.</span><span class="sxs-lookup"><span data-stu-id="634e6-108">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="634e6-109">Valige teenuslepe või looge uus teenuslepe.</span><span class="sxs-lookup"><span data-stu-id="634e6-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="634e6-110">Vormi **Hooldustellimuste loomine** avamiseks klõpsake vahekaardi **Tarnimine** grupis **Loomine** valikut **Planeeritud hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="634e6-110">Click the **Deliver** tab and in the **Create** group click **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="634e6-111">teenustellimuse käsitsi loomine teenustellimuse vormi abil</span><span class="sxs-lookup"><span data-stu-id="634e6-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="634e6-112">Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="634e6-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="634e6-113">Uue teenustellimuse loomiseks vajutage klahve CTRL+N.</span><span class="sxs-lookup"><span data-stu-id="634e6-113">Press Ctrl+N to create a new service order.</span></span>

3.  <span data-ttu-id="634e6-114">Looge teenustellimuse jaoks teenustellimuse read.</span><span class="sxs-lookup"><span data-stu-id="634e6-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="634e6-115">Kui on valitud märkeruut <STRONG>Luba hooldusleppeta</STRONG> vormil <STRONG>Teenuste halduse parameetrid</STRONG>, saate sisestada kandeid hooldustellimuse ridadelt, sidumata hooldustellimust hooldusleppega.</span><span class="sxs-lookup"><span data-stu-id="634e6-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="634e6-116">Kui ruut on tühjendatud, tuleb käsitsi loodud teenustellimuse enne teenustellimuse ridade sisestamist siduma projektiga.</span><span class="sxs-lookup"><span data-stu-id="634e6-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="634e6-117">Hooldustellimuse loomine projektist</span><span class="sxs-lookup"><span data-stu-id="634e6-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="634e6-118">Klõpsake valikuid **Projektihaldus ja raamatupidamine** \> **Üldine** \> **Projektid** \> **Kõik projektid**.</span><span class="sxs-lookup"><span data-stu-id="634e6-118">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="634e6-119">Klõpsake vormi **Projektid** **toimingupaanil** vahekaarti **Halda** \> **Teenus** \> **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="634e6-119">In the **Projects** form, on the **Action pane**, click the **Manage** tab \> click **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="634e6-120">Järgige eelmist protseduuri, et luua hooldustellimus käsitsi vormil **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="634e6-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="634e6-121">Väljal **Projekti ID** kuvatakse projekti viide.</span><span class="sxs-lookup"><span data-stu-id="634e6-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="634e6-122">Kui on valitud märkeruut <STRONG>Luba hooldusleppeta</STRONG> vormil <STRONG>Teenuste halduse parameetrid</STRONG>, saate sisestada kandeid hooldustellimuse ridadelt, sidumata hooldustellimust hooldusleppega.</span><span class="sxs-lookup"><span data-stu-id="634e6-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="634e6-123">Kui ruut on tühjendatud, tuleb käsitsi loodud teenustellimuse enne teenustellimuse ridade sisestamist siduma projektiga.</span><span class="sxs-lookup"><span data-stu-id="634e6-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="634e6-124">Hooldustellimuse loomine vormilt Müügitellimus</span><span class="sxs-lookup"><span data-stu-id="634e6-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="634e6-125">Vormilt **Müügitellimused** saate hooldustellimuse luua viisardi **Loo müügitellimuse põhjal uus hooldustellimus** abil.</span><span class="sxs-lookup"><span data-stu-id="634e6-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="634e6-126">Klõpsake valikuid **Müük ja turundus** \> **Üldine** \> **Müügitellimused** \> **Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="634e6-126">Click **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="634e6-127">Avage asjakohane müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="634e6-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="634e6-128">Viisardi **Loo müügitellimuse põhjal uus hooldustellimus** käivitamiseks klõpsake vahekaardil **Müügitellimus** valikut **Hooldustellimus**.</span><span class="sxs-lookup"><span data-stu-id="634e6-128">On the **Sales order** tab, click **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="634e6-129">Klõpsake valikut **Järgmine \>** ja seejärel tehke lehel **Vali hooldustellimuse jaoks lepe** järgmist.</span><span class="sxs-lookup"><span data-stu-id="634e6-129">Click **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="634e6-130">Kasutage välja **Hoolduslepe**, et valida hoolduslepe, millega uus hooldustellimus siduda.</span><span class="sxs-lookup"><span data-stu-id="634e6-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="634e6-131">Valikuline: kasutage loendit **Projekti ID**, et siduda hooldustellimus kindla projektiga.</span><span class="sxs-lookup"><span data-stu-id="634e6-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="634e6-132">Klõpsake valikut **Järgmine \>** ja seejärel tehke lehel **Loo hooldustellimus** järgmist.</span><span class="sxs-lookup"><span data-stu-id="634e6-132">Click **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="634e6-133">Sisestage kuupäev ja kellaaeg, millal hoolduskutse algab, väljale **Eelistatud teenuseaeg**.</span><span class="sxs-lookup"><span data-stu-id="634e6-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="634e6-134">Valikuline: saate väljal **Kirjeldus** olevat teksti muuta.</span><span class="sxs-lookup"><span data-stu-id="634e6-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="634e6-135">Vaikimisi sisaldab see väli hooldusleppe kirjeldust, mille valisite eelmisel lehel.</span><span class="sxs-lookup"><span data-stu-id="634e6-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="634e6-136">Valige väljal **Vastutaja** leppe eest vastutava töötaja ID ja kui teate, siis sisestage ka hoolduskutse kliendi eelistatud tehniku ID.</span><span class="sxs-lookup"><span data-stu-id="634e6-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="634e6-137">Valige väljal **Kontakti ID** kliendi ettevõttest isik, kellega selle hooldustellimuse asjus ühendust võtta.</span><span class="sxs-lookup"><span data-stu-id="634e6-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="634e6-138">Klõpsake valikut **Järgmine \>** ja seejärel **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="634e6-138">Click **Next \>**, and then click **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="634e6-139">Vt ka</span><span class="sxs-lookup"><span data-stu-id="634e6-139">See also</span></span>

[<span data-ttu-id="634e6-140">Teenusetellimused</span><span class="sxs-lookup"><span data-stu-id="634e6-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="634e6-141">Hooldustellimuste loomine automaatselt</span><span class="sxs-lookup"><span data-stu-id="634e6-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="634e6-142">[Teenusetellimuste loomine (klass Vormid)](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="634e6-142">[Create service orders (class form)](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\))</span></span> 

