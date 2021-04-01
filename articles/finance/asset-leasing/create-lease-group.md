---
title: Rendigrupi loomine
description: Selles teemas selgitatakse, kuidas seadistada rendigruppe. Rendigrupid vajalikud uute rendikirjete loomiseks.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e8ad226e87776615d9c19a239e0fb90b648d9c49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210453"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="ed166-104">Rendigrupi loomine</span><span class="sxs-lookup"><span data-stu-id="ed166-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed166-105">Selles teemas selgitatakse, kuidas seadistada rendigruppe.</span><span class="sxs-lookup"><span data-stu-id="ed166-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="ed166-106">Rendigrupid vajalikud uute rendikirjete loomiseks.</span><span class="sxs-lookup"><span data-stu-id="ed166-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="ed166-107">Rendi raamatud on seostatud iga rendigrupiga.</span><span class="sxs-lookup"><span data-stu-id="ed166-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="ed166-108">Rendi raamatud määravad vaikimisi raamatud, mis tuleb iga rendikirje jaoks luua.</span><span class="sxs-lookup"><span data-stu-id="ed166-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="ed166-109">Saate määrata rendigrupile konkreetsed kontod lehel **Rendikirje sisestamise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="ed166-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="ed166-110">Rendi raamatu loomine ja rendigrupi lisamine</span><span class="sxs-lookup"><span data-stu-id="ed166-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="ed166-111">Avage **Vara rentimine \> Seadistus \> Rendigrupid**.</span><span class="sxs-lookup"><span data-stu-id="ed166-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="ed166-112">Rendigrupi lisamiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ed166-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="ed166-113">Ruudustikku lisatakse rida.</span><span class="sxs-lookup"><span data-stu-id="ed166-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="ed166-114">Sisestage välja **Rendigrupp** uuele reale väärtus.</span><span class="sxs-lookup"><span data-stu-id="ed166-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="ed166-115">Sisestage väärtus väljal **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="ed166-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="ed166-116">Teie sisestatud teave lisatakse väljale **Rendigrupp** lehel **Rendikirje lisamine**.</span><span class="sxs-lookup"><span data-stu-id="ed166-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="ed166-117">Raamatu seostamine rendigrupiga</span><span class="sxs-lookup"><span data-stu-id="ed166-117">Associate a book with a lease group</span></span>

<span data-ttu-id="ed166-118">Pärast rendigruppide loomist saate määrata igale grupile raamatu.</span><span class="sxs-lookup"><span data-stu-id="ed166-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="ed166-119">Rendikirje loomisel ja selle rendigrupile määramisel loob süsteem iga raamatu jaoks graafikute kogumi, mis seostatakse selle rendigrupiga.</span><span class="sxs-lookup"><span data-stu-id="ed166-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="ed166-120">Enne rendigrupile määramist tuleb raamatud häälestada.</span><span class="sxs-lookup"><span data-stu-id="ed166-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="ed166-121">Avage **Vara rentimine \> Seadistus \> Rendigrupp**.</span><span class="sxs-lookup"><span data-stu-id="ed166-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="ed166-122">Valige rendigrupp ja valige seejärel **Raamatud**.</span><span class="sxs-lookup"><span data-stu-id="ed166-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="ed166-123">Valige **Uus** ja valige seejärel väljal **Raamatu tüüp** rendigrupile määramiseks raamat.</span><span class="sxs-lookup"><span data-stu-id="ed166-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="ed166-124">Kui renti tuleb arvestada mitmel erineval viisil, saate määrata rendigrupile mitu raamatut.</span><span class="sxs-lookup"><span data-stu-id="ed166-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]