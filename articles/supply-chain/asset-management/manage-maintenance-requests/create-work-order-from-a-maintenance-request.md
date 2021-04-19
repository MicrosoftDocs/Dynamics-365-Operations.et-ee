---
title: Töötellimuste loomine hooldustaotluste põhjal
description: See teema selgitab, kuidas luua varahalduses hoolduse päringust töökäsk.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c360985509f8f1379ed4a9bd17b95f2d8c85340e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808588"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="bb524-103">Töötellimuste loomine hooldustaotluste põhjal</span><span class="sxs-lookup"><span data-stu-id="bb524-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="bb524-104">Pärast hoolduspäringute loomist saate need hõlpsalt töötellimusteks teisendada.</span><span class="sxs-lookup"><span data-stu-id="bb524-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="bb524-105">See teema kirjeldab kiireimat viisi, kuidas töötada hooldustaotlustega, uuendada mitut hooldustaotlust korraga ja seejärel luua töökäsk mitme hooldustaotluse jaoks samal ajal.</span><span class="sxs-lookup"><span data-stu-id="bb524-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="bb524-106">Lehel **Aktiivsed hooldustaotlused** või lehel **Minu funktsionaalsed asukohahoolduse taotlused** saate töötada korraga ka ühe hooldustaotlusega ja teisendada ühe hooldustaotluse töötellimuseks.</span><span class="sxs-lookup"><span data-stu-id="bb524-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="bb524-107">Iga hooldustaotlus võib olla seotud ainult ühe töötellimusega.</span><span class="sxs-lookup"><span data-stu-id="bb524-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="bb524-108">Mitu hooldustaotlust saab siiski lisada ühele töötellimusele, isegi kui hooldustaotlustes on erinevad varad.</span><span class="sxs-lookup"><span data-stu-id="bb524-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="bb524-109">Valige **Varahaldus**\>**Ühised**\>**Hooldustaotlused**\>**Hooldustaotlused**.</span><span class="sxs-lookup"><span data-stu-id="bb524-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="bb524-110">Enne kui saate hooldustaotlusest töökäsu luua, peate hooldustaotluse jaoks valima vähemalt hooldustöö tüübi ja hooldustöö tüübi variandi ning kaubanduse, kui see teave on asjakohane.</span><span class="sxs-lookup"><span data-stu-id="bb524-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="bb524-111">Ruudustiku vaates saate hõlpsasti värskendada hooldustaotluse teavet.</span><span class="sxs-lookup"><span data-stu-id="bb524-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="bb524-112">Kui olete valmis töökäsu looma, valige sellesse kaasatavad hooldustaotlused.</span><span class="sxs-lookup"><span data-stu-id="bb524-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="bb524-113">Kui valite töötellimuseks teisendamiseks mitu hooldustaotlust, tuleb enne töökäsu loomist häälestada mõlemad väljad: **Vara** ja **Hooldustöö tüüp**.</span><span class="sxs-lookup"><span data-stu-id="bb524-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="bb524-114">Kui valite töötellimuseks teisendamiseks ühe hooldustaotluse, tuleb enne töökäsu loomist häälestada üksnes väli **Vara**.</span><span class="sxs-lookup"><span data-stu-id="bb524-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="bb524-115">Töökäsu loomisel saate siiski valida hooldustöö tüübi (ja seotud hooldustöö tüübi variandi ja kaubanduse, kui see teave on asjakohane) dialoogiboksis **Loo töötellimus**.</span><span class="sxs-lookup"><span data-stu-id="bb524-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="bb524-116">Valige **Töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="bb524-116">Select **Work order**.</span></span>
5. <span data-ttu-id="bb524-117">Dialoogiboksis **Loo töökäsk** sätestage väljad ja seejärel klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb524-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="bb524-118">Teateriba võib teid teavitada, et on loodud uus töökäsk.</span><span class="sxs-lookup"><span data-stu-id="bb524-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="bb524-119">Lisaks, kui loote töökäsu, mis põhineb hoolduse taotlusel, kui hoolduse taotlusega seotud vara sisaldub garantiilepingus, teavitab teateriba teid garantiilepingust.</span><span class="sxs-lookup"><span data-stu-id="bb524-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="bb524-120">Valige **Varahaldus**\>**Ühised**\>**Töökäsud**  \>**Kõik töökäsud** ja avage uus töökäsk.</span><span class="sxs-lookup"><span data-stu-id="bb524-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![Uue töökäsu avamine](media/05-manage-maintenance-requests.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]