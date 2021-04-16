---
title: Rendi kinnitamise töövoogude seadistamine
description: Selles teemas selgitatakse, kuidas seadistada kinnitamise töövoogu, mis käivitub uue rendilepingu loomisel.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4d5416b3b24d5fbb3ac46afb3c672212d41d42d5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827550"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="31155-103">Rendi kinnitamise töövoogude seadistamine</span><span class="sxs-lookup"><span data-stu-id="31155-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31155-104">Selles teemas selgitatakse, kuidas seadistada kinnitamise töövoogu, mis käivitub uue rendilepingu loomisel.</span><span class="sxs-lookup"><span data-stu-id="31155-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="31155-105">Lisateavet töövoo kasutamise kohta vaadake jaotisest [Rendilepingu kinnitamise töövoogude kasutamine](use-create-lease-wrkflw.md).</span><span class="sxs-lookup"><span data-stu-id="31155-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="31155-106">Avage **Vara rentimine \> Seadistus \> Rendi töövoog**.</span><span class="sxs-lookup"><span data-stu-id="31155-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="31155-107">Valige lehel **Rendi töövoog** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="31155-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="31155-108">Kuvatavas dialoogiaknas valige jaotises **Töövoo tüüp** link **Rendi töövoog**.</span><span class="sxs-lookup"><span data-stu-id="31155-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="31155-109">Rakendus avatakse.</span><span class="sxs-lookup"><span data-stu-id="31155-109">The application is opened.</span></span> <span data-ttu-id="31155-110">Pärast selle käitamist logige sisse rakendusse Azure Active Directory (Azure AD) ja teid suunatakse ümber töövoo rakendamise juurde.</span><span class="sxs-lookup"><span data-stu-id="31155-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="31155-111">Lohistage element **Rendi töövoo kinnitamine** töövoogu.</span><span class="sxs-lookup"><span data-stu-id="31155-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="31155-112">Ühendage üks sõlm üksusest **Algus** üksusega **Rendi töövoo kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="31155-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="31155-113">Seejärel ühendage **Rendi töövoo kinnitamine** üksusega **Lõpp**.</span><span class="sxs-lookup"><span data-stu-id="31155-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="31155-114">Topeltklõpsake käsku **Rendi töövoo kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="31155-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="31155-115">Valige **Atribuudid** ja seejärel sisestage jaotises **Põhisätted** töövoole nimi.</span><span class="sxs-lookup"><span data-stu-id="31155-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="31155-116">Sellel lehel saate seadistada töövoole ka rohkem parameetreid.</span><span class="sxs-lookup"><span data-stu-id="31155-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="31155-117">Kui olete aktiveerinud **Automaatsed tegevused**, teeb süsteem automaatselt teatud toiminguid.</span><span class="sxs-lookup"><span data-stu-id="31155-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="31155-118">Teatisi saab saata, kui need on määratletud vahekaardil **Teatised**. Vahekaardil **Täpsemad seaded** saate määrata lõpliku kinnitaja, määrata ajalimiidi ja määrata konkreetsed tegevused, mis tuleb lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="31155-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="31155-119">Kui olete töövoo parameetrite määramise lõpetanud, valige käsk **Sule**.</span><span class="sxs-lookup"><span data-stu-id="31155-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="31155-120">Valige **1. etapp** ja seejärel valige **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="31155-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="31155-121">Sisestage jaotises **Põhisätted** etapile nimi, looge kinnitamiseks teemarida ja määratlege kinnitamise juhendid.</span><span class="sxs-lookup"><span data-stu-id="31155-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="31155-122">Valige lehel **Määramine** määramise tüüp.</span><span class="sxs-lookup"><span data-stu-id="31155-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="31155-123">Kinnitamisele kindlate kasutajate määramiseks valige **Kasutaja**, valige rentimisi kinnitavad kasutajad ja seejärel valige **Sule**.</span><span class="sxs-lookup"><span data-stu-id="31155-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="31155-124">Töövoo loomiseks valige **Salvesta ja sule**.</span><span class="sxs-lookup"><span data-stu-id="31155-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="31155-125">Seejärel, kui teilt küsitakse, valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="31155-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="31155-126">Valige lehel **Loo töövoog** suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="31155-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="31155-127">Valige uus töövoog ja seejärel valige **Versioonid**.</span><span class="sxs-lookup"><span data-stu-id="31155-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="31155-128">Tagamaks, et töövoog oleks aktiivne, valige **Tee aktiivseks**.</span><span class="sxs-lookup"><span data-stu-id="31155-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="31155-129">Valige suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="31155-129">Select **Close**.</span></span> <span data-ttu-id="31155-130">Kuvatakse uus aktiivne versioon.</span><span class="sxs-lookup"><span data-stu-id="31155-130">The new active version appears.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]