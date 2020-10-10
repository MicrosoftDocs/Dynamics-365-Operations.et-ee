---
title: Töökäsu tüübid
description: Selles teemas selgitatakse töökäskude tüüpe varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b8e43908e3f13c9e4fd6fab6f1e17a171866b803
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888781"
---
# <a name="work-order-types"></a><span data-ttu-id="299a8-103">Töökäsu tüübid</span><span class="sxs-lookup"><span data-stu-id="299a8-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="299a8-104">Töötellimuse tüüpe kasutatakse töötellimuste kategoriseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="299a8-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="299a8-105">Näiteks võivad teil olla töökäsud, mis on seotud ennetava hoolduse või parandava hooldusega.</span><span class="sxs-lookup"><span data-stu-id="299a8-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="299a8-106">Töökäsu tüüp määratleb alluvuse töökäsu elutsükli mudeliga.</span><span class="sxs-lookup"><span data-stu-id="299a8-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="299a8-107">Töökäsu elutsükli mudel määratleb töökäsu elutsükli olekud, mida saab seadistada töökäsule.</span><span class="sxs-lookup"><span data-stu-id="299a8-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="299a8-108">(Töökäsu elutsükli oleku näideteks on **Loodud**,**Töös** ja **Lõpetatud**.)</span><span class="sxs-lookup"><span data-stu-id="299a8-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="299a8-109">Lisateavet töökäsu elutsükli olekute ja projekti etappide kohta vt [Töökäsu elutsükli olekud](work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="299a8-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="299a8-110">Valige **Varahaldus**\>**Seadistus**\>**Töökäsud** \>**Töökäskude tüübid**.</span><span class="sxs-lookup"><span data-stu-id="299a8-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="299a8-111">Valige uue töökäsu loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="299a8-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="299a8-112">Sisestage väljale **Töökäsu tüüp** töökäsu tüübi ID.</span><span class="sxs-lookup"><span data-stu-id="299a8-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="299a8-113">Väljale **Nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="299a8-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="299a8-114">Valige väljal **Töökäsu töötsükli mudel** töötsükli mudel.</span><span class="sxs-lookup"><span data-stu-id="299a8-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="299a8-115">Seadistage suvand **Üks hooldustöötaja** valikule **Jah**, kui kõik töökäskude tööd, mis on seotud selle tüübi töökäsu, tuleb planeerida samale hooldustöötajale.</span><span class="sxs-lookup"><span data-stu-id="299a8-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="299a8-116">Valige väljal **Kulu tüüp** vastavalt **Korrigeeriv**, **Ennetav** või **Investeering**.</span><span class="sxs-lookup"><span data-stu-id="299a8-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="299a8-117">Kõigil töökäskude töödel peab olema sama kulutüüp.</span><span class="sxs-lookup"><span data-stu-id="299a8-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="299a8-118">Määrake jaotises **Kohustuslik** asjakohased valikud kui **Jah**, et määrata, milline tõrkega seotud või hoolduse seisakuga seotud teave lisatakse seda tüüpi töökäsule.</span><span class="sxs-lookup"><span data-stu-id="299a8-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="299a8-119">Jaotise **Kohustuslik** valikud on seotud valikutega FastTabil **Kinnita** leheküljel **Töökäskude töötsüklite olekud** (**Varahaldus**\> **Seadistus** \> **Töökäsud**\> **Töötsükli olekud).**</span><span class="sxs-lookup"><span data-stu-id="299a8-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="299a8-120">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="299a8-120">Select **Save**.</span></span>

![Töökäsu tüübid](media/16-setup-for-work-orders.png)
