---
title: Kaubavajaduse loomine teenustellimusest
description: Kui teil on vaja teenusetellimuse jaoks konkreetseid kaupu reserveerida, saate selle jaoks luua laokauba vajadused.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b342b20cc11addc53fc6ea4e1a23d3b449eb9ee
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257937"
---
# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="e26c3-103">Kaubavajaduse loomine teenustellimusest</span><span class="sxs-lookup"><span data-stu-id="e26c3-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e26c3-104">Saate luua hooldustellimuse klientidele osutatavate teenuste jälgimiseks ja haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="e26c3-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="e26c3-105">Kui teil on vaja teenusetellimuse jaoks konkreetseid kaupu reserveerida, saate selle jaoks luua laokauba vajadused.</span><span class="sxs-lookup"><span data-stu-id="e26c3-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="e26c3-106">Kaubavajadust saab laost kohe tarbida või see võib algatada kauba tootmistellimuse.</span><span class="sxs-lookup"><span data-stu-id="e26c3-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="e26c3-107">Kasutades kaubakannete asemel kaubavajadusi, saate planeerida tarne just selleks ajaks, mil kaupa tegelikult kasutatakse, luua ostutellimuse, kaasata kauba kaubandusleppe raamistikku ja kaasata kaubavajaduse tootmisplaanidesse.</span><span class="sxs-lookup"><span data-stu-id="e26c3-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="e26c3-108">Teenusetellimuste kaubavajadusi töödeldakse projekti kaudu.</span><span class="sxs-lookup"><span data-stu-id="e26c3-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="e26c3-109">Teenusetellimusele kaubavajaduse loomiseks peab olema projektile määratud teenusetellimus.</span><span class="sxs-lookup"><span data-stu-id="e26c3-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="e26c3-110">Pärast hooldustellimusele kaubavajaduse loomist saate valitud projekti kaubavajadust vormil **Projektid** vaadata.</span><span class="sxs-lookup"><span data-stu-id="e26c3-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="e26c3-111">Teenustellimusele kaubavajaduse loomine</span><span class="sxs-lookup"><span data-stu-id="e26c3-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="e26c3-112">Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="e26c3-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="e26c3-113">Valige teenusetellimus, millele soovite kaubavajaduse luua.</span><span class="sxs-lookup"><span data-stu-id="e26c3-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="e26c3-114">Klõpsake **toimingupaani** vahekaardil **Lähetus** valikut **Kaubavajadus**.</span><span class="sxs-lookup"><span data-stu-id="e26c3-114">On the **Action Pane**, on the **Dispatch** tab, click **Item requirement**.</span></span>

4.  <span data-ttu-id="e26c3-115">Sisestage vormil **Kaubavajadused** nõutava kauba teave.</span><span class="sxs-lookup"><span data-stu-id="e26c3-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="e26c3-116">Konkreetsete väljade kohta lisateabe saamiseks vt jaotist [Kaubavajadused (vorm)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="e26c3-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="e26c3-117">Teenusleppele kaubavajaduse loomine</span><span class="sxs-lookup"><span data-stu-id="e26c3-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="e26c3-118">Klõpsake valikut **Hooldushaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldusleppegrupid**.</span><span class="sxs-lookup"><span data-stu-id="e26c3-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="e26c3-119">Avage teenuselepe, millele soovite kaubavajaduse luua.</span><span class="sxs-lookup"><span data-stu-id="e26c3-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="e26c3-120">Uue rea loomiseks klõpsake kiirkaardi **Read** valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e26c3-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="e26c3-121">Valige **Kaup** väljal **Kande tüüp**.</span><span class="sxs-lookup"><span data-stu-id="e26c3-121">In the **Transaction type** field, select **Item**.</span></span>

5.  <span data-ttu-id="e26c3-122">Valige **Kaubavajadus** väljal **Kauba seadistus**.</span><span class="sxs-lookup"><span data-stu-id="e26c3-122">In the **Item setup** field, select **Item requirement**.</span></span>

6.  <span data-ttu-id="e26c3-123">Valige väljal **Kaubakood** kaup, mis on hooldusleppe jaoks vajalik.</span><span class="sxs-lookup"><span data-stu-id="e26c3-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="e26c3-124">Valige kiirkaardi **Rea üksikasjad** vahekaardi **Toote dimensioonid** väljal **Laoala** kauba laoala.</span><span class="sxs-lookup"><span data-stu-id="e26c3-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="e26c3-125">Lepperealt hooldustellimuse loomiseks kiirkaardil **Read** klõpsake valikut **Hooldustellimuste loomine** ja sisestage seejärel asjakohane teave vormi **Hooldustellimuste loomine**.</span><span class="sxs-lookup"><span data-stu-id="e26c3-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders**, and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="e26c3-126">Vt ka</span><span class="sxs-lookup"><span data-stu-id="e26c3-126">See also</span></span>

<span data-ttu-id="e26c3-127">[Hooldustellimuste loomine automaatselt](create-service-orders-automatically.md)</span><span class="sxs-lookup"><span data-stu-id="e26c3-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]