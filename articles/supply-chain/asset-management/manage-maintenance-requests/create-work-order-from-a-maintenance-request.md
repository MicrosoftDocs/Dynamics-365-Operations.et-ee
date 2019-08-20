---
title: Töötellimuste loomine hooldustaotluste põhjal
description: See teema selgitab, kuidas luua varahalduses hoolduse päringust töökäsk.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3f7af87f359cfe3a606c8be857dd905bfef75e97
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847455"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="8a93d-103">Töötellimuste loomine hooldustaotluste põhjal</span><span class="sxs-lookup"><span data-stu-id="8a93d-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="8a93d-104">Pärast hoolduspäringute loomist saate need hõlpsalt töötellimusteks teisendada.</span><span class="sxs-lookup"><span data-stu-id="8a93d-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="8a93d-105">See teema kirjeldab kiireimat viisi, kuidas töötada hooldustaotlustega, uuendada mitut hooldustaotlust korraga ja seejärel luua töökäsk mitme hooldustaotluse jaoks samal ajal.</span><span class="sxs-lookup"><span data-stu-id="8a93d-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="8a93d-106">Lehel **Aktiivsed hooldustaotlused** või lehel **Minu funktsionaalsed asukohahoolduse taotlused** saate töötada korraga ka ühe hooldustaotlusega ja teisendada ühe hooldustaotluse töötellimuseks.</span><span class="sxs-lookup"><span data-stu-id="8a93d-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="8a93d-107">Iga hooldustaotlus võib olla seotud ainult ühe töötellimusega.</span><span class="sxs-lookup"><span data-stu-id="8a93d-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="8a93d-108">Mitu hooldustaotlust saab siiski lisada ühele töötellimusele, isegi kui hooldustaotlustes on erinevad varad.</span><span class="sxs-lookup"><span data-stu-id="8a93d-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="8a93d-109">Valige **Varahaldus**\>**Ühised**\>**Hooldustaotlused**\>**Hooldustaotlused**.</span><span class="sxs-lookup"><span data-stu-id="8a93d-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="8a93d-110">Enne kui saate hooldustaotlusest töökäsu luua, peate hooldustaotluse jaoks valima vähemalt hooldustöö tüübi ja hooldustöö tüübi variandi ning kaubanduse, kui see teave on asjakohane.</span><span class="sxs-lookup"><span data-stu-id="8a93d-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="8a93d-111">Ruudustiku vaates saate hõlpsasti värskendada hooldustaotluse teavet.</span><span class="sxs-lookup"><span data-stu-id="8a93d-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="8a93d-112">Kui olete valmis töökäsu looma, valige sellesse kaasatavad hooldustaotlused.</span><span class="sxs-lookup"><span data-stu-id="8a93d-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="8a93d-113">Kui valite töötellimuseks teisendamiseks mitu hooldustaotlust, tuleb enne töökäsu loomist häälestada mõlemad väljad: **Vara** ja **Hooldustöö tüüp**.</span><span class="sxs-lookup"><span data-stu-id="8a93d-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="8a93d-114">Kui valite töötellimuseks teisendamiseks ühe hooldustaotluse, tuleb enne töökäsu loomist häälestada üksnes väli **Vara**.</span><span class="sxs-lookup"><span data-stu-id="8a93d-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="8a93d-115">Töökäsu loomisel saate siiski valida hooldustöö tüübi (ja seotud hooldustöö tüübi variandi ja kaubanduse, kui see teave on asjakohane) dialoogiboksis **Loo töötellimus**.</span><span class="sxs-lookup"><span data-stu-id="8a93d-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="8a93d-116">Valige **Töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="8a93d-116">Select **Work order**.</span></span>
5. <span data-ttu-id="8a93d-117">Dialoogiboksis **Loo töökäsk** sätestage väljad ja seejärel klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a93d-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="8a93d-118">Teateriba võib teid teavitada, et on loodud uus töökäsk.</span><span class="sxs-lookup"><span data-stu-id="8a93d-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="8a93d-119">Lisaks, kui loote töökäsu, mis põhineb hoolduse taotlusel, kui hoolduse taotlusega seotud vara sisaldub garantiilepingus, teavitab teateriba teid garantiilepingust.</span><span class="sxs-lookup"><span data-stu-id="8a93d-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="8a93d-120">Valige **Varahaldus**\>**Ühised**\>**Töökäsud**  \>**Kõik töökäsud** ja avage uus töökäsk.</span><span class="sxs-lookup"><span data-stu-id="8a93d-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![Joonis 1](media/05-manage-maintenance-requests.png)

