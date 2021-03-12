---
title: Teenuse tellimuse kaubanõuded
description: Kui teil on vaja teenusetellimuse jaoks konkreetseid kaupu reserveerida, saate selle jaoks luua laokauba vajadused.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b0ed409dc4ab39e55c198b8738c9722213b0cba
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001270"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="b2f82-103">Teenuse tellimuse kaubanõuded</span><span class="sxs-lookup"><span data-stu-id="b2f82-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b2f82-104">Saate luua hooldustellimuse klientidele osutatavate teenuste jälgimiseks ja haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="b2f82-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="b2f82-105">Kui teil on vaja teenusetellimuse jaoks konkreetseid kaupu reserveerida, saate selle jaoks luua laokauba vajadused.</span><span class="sxs-lookup"><span data-stu-id="b2f82-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="b2f82-106">Kaubavajadust saab laost kohe tarbida või see võib algatada kauba tootmistellimuse.</span><span class="sxs-lookup"><span data-stu-id="b2f82-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="b2f82-107">Kasutades kaubakannete asemel kaubavajadusi, saate planeerida tarne just selleks ajaks, mil kaupa tegelikult kasutatakse, luua ostutellimuse, kaasata kauba kaubandusleppe raamistikku ja kaasata kaubavajaduse tootmisplaanidesse.</span><span class="sxs-lookup"><span data-stu-id="b2f82-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="b2f82-108">Teenusetellimuste kaubavajadusi töödeldakse projekti kaudu.</span><span class="sxs-lookup"><span data-stu-id="b2f82-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="b2f82-109">Teenusetellimusele kaubavajaduse loomiseks peab teenusetellimus olema projektiga seotud.</span><span class="sxs-lookup"><span data-stu-id="b2f82-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="b2f82-110">Niipea, kui teenustellimusele on kaubavajadus loodud, saab seda vaadata üksikus teenustellimuses moodulis **Projekt** või vormi **Müügitellimus** kaudu.</span><span class="sxs-lookup"><span data-stu-id="b2f82-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="b2f82-111">Kaubavajaduse vaatamine teenustellimusest</span><span class="sxs-lookup"><span data-stu-id="b2f82-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="b2f82-112">Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="b2f82-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="b2f82-113">Klõpsake suvandit **Lähetus** ja seejärel suvandit **Kaubavajadus**, et avada vorm **Kaubavajadused**.</span><span class="sxs-lookup"><span data-stu-id="b2f82-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="b2f82-114">Klõpsake vahekaarti **Projekt** ja vaadake, kas väljal **Hooldustellimus** on kaubavajaduse hooldustellimused.</span><span class="sxs-lookup"><span data-stu-id="b2f82-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="b2f82-115">Kaubavajadustega teenustellimuste kustutamine</span><span class="sxs-lookup"><span data-stu-id="b2f82-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="b2f82-116">Kui kaubavajadus luuake teenustellimusel, siis ei saa teenustellimust kustutada.</span><span class="sxs-lookup"><span data-stu-id="b2f82-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="b2f82-117">Kaubavajadus tuleb kustutada enne teenustellimuse kustutamist.</span><span class="sxs-lookup"><span data-stu-id="b2f82-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="b2f82-118">Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="b2f82-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="b2f82-119">Klõpsake suvandit **Lähetus** ja seejärel suvandit **Kaubavajadus**, et avada vorm **Kaubavajadused**.</span><span class="sxs-lookup"><span data-stu-id="b2f82-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="b2f82-120">Vormil on teenusetellimuses loodud kaubavajadused.</span><span class="sxs-lookup"><span data-stu-id="b2f82-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="b2f82-121">Valige kustutamiseks kaubavajadus ja klõpsake siis käsku **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="b2f82-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="b2f82-122">või</span><span class="sxs-lookup"><span data-stu-id="b2f82-122">–or–</span></span>

1.  <span data-ttu-id="b2f82-123">Klõpsake valikuid **Projektihaldus ja raamatupidamine** \> **Üldine** \> **Projektid** \> **Kõik projektid**.</span><span class="sxs-lookup"><span data-stu-id="b2f82-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="b2f82-124">Avage projekt, milles on teenusetellimus, milles on loodud kaubavajadus.</span><span class="sxs-lookup"><span data-stu-id="b2f82-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="b2f82-125">Klõpsake vormil **Projektid** parempoolsel paanil suvandit **Kaubavajadused**.</span><span class="sxs-lookup"><span data-stu-id="b2f82-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="b2f82-126">Vorm **Kaubavajadused** kuvab valitud projektiga seotud kaubavajadused.</span><span class="sxs-lookup"><span data-stu-id="b2f82-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="b2f82-127">Valige kustutamiseks kaubavajadus ja klõpsake siis käsku **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="b2f82-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2f82-128">Vt ka</span><span class="sxs-lookup"><span data-stu-id="b2f82-128">See also</span></span>

<span data-ttu-id="b2f82-129">[Kaubavajadused (vorm)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="b2f82-129">[Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span></span>

