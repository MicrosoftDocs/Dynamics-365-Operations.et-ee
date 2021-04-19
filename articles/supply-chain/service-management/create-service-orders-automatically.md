---
title: Hooldustellimuste loomine automaatselt
description: Hooldustellimusi saate luua nii ühe kui ka mitme hooldusleppe jaoks.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: cc06536827320a35a691330d852ba64532604935
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817601"
---
# <a name="create-service-orders-automatically"></a><span data-ttu-id="b1fb5-103">Hooldustellimuste loomine automaatselt</span><span class="sxs-lookup"><span data-stu-id="b1fb5-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b1fb5-104">Hooldustellimusi saate luua nii ühe kui ka mitme hooldusleppe jaoks.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="b1fb5-105">Loodud hooldustellimusi saate vaadata vormil **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="b1fb5-106">Hooldustellimusi luuakse ainult hooldusleppe kehtivusperioodi ajaks.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="b1fb5-107">Kui osa vormil **Hooldustellimuste loomine** määratud intervallist on hooldusleppe alguskuupäevast varasem või lõppkuupäevast hilisem, luuakse hooldustellimused ainult hooldusleppe kuupäevadesse jääva intervalliosa jaoks.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="b1fb5-108">Kui loote hooldustellimused hooldusleppe realt käsitsi või automaatselt, peab hoolduslepe jääma rea algus- ja lõppkuupäevade ajaintervalli piiresse, kui te ei määratle real lõppkuupäeva.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="b1fb5-109">Teenustellimuste automaatne loomine ühe teenusleppe jaoks</span><span class="sxs-lookup"><span data-stu-id="b1fb5-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="b1fb5-110">Klõpsake valikut **Hooldushaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldusleppegrupid**.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="b1fb5-111">Valige soovitud teenusleping.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="b1fb5-112">Klõpsake vahekaarti **Tarnimine** ja seejärel valikut **Planeeritud hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="b1fb5-113">Hooldusperioodi määratlemiseks sisestage soovitud kuupäevad väljadele **Kuupäevast** ja **Kuupäevani**.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="b1fb5-114">Loodud hooldustellimuste loendi kuvamiseks märkige ruut **Näita teabelogi**.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="b1fb5-115">Valige kandetüübid väljagrupis **Kaasa kandetüübid**.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="b1fb5-116">Kandetüübid tähistavad teenusleppes loodavaid ridu ning iga valitud kandetüübi puhul luuakse mitu teenustellimust, sõltuvalt teenusleppe real määratud teenusintervallist.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="b1fb5-117">Puuduvate hooldustellimuste loomiseks pidevast hooldustellimuste sarjast märkige ruut **Pidev**.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="b1fb5-118">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="b1fb5-119">Teenustellimuste automaatne loomine mitme teenusleppe jaoks</span><span class="sxs-lookup"><span data-stu-id="b1fb5-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="b1fb5-120">Klõpsake valikuid **Teeninduse haldus** \> **Perioodiline** \> **Hooldustellimused** \> **Hooldustellimuste loomine**.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="b1fb5-121">Hooldustellimuste loomisel kasutatavate kriteeriumite lisamiseks või kustutamiseks saate valikuid teha, klõpsates käsku **Vali**.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="b1fb5-122">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1fb5-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1fb5-123">Vt ka</span><span class="sxs-lookup"><span data-stu-id="b1fb5-123">See also</span></span>

[<span data-ttu-id="b1fb5-124">Teenuse tellimused</span><span class="sxs-lookup"><span data-stu-id="b1fb5-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="b1fb5-125">Hooldustellimuste loomine automaatselt</span><span class="sxs-lookup"><span data-stu-id="b1fb5-125">Automatically create service orders</span></span>](auto-create-service-orders.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]