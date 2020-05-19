---
title: Turbediagnostika ülesande salvestiste jaoks
description: Selles teemas jagatakse teavet selle kohta, kuidas analüüsida ja hallata tegevuse salvestise põhjal turvaõiguste nõudeid.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: fada3abb9362426c7c9ec33f5d25552edf3ef630
ms.sourcegitcommit: 71fec2553158c332ce4d4bfcedc2c1ab58c1a1a5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/06/2020
ms.locfileid: "3340671"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="e8e9a-103">Turbediagnostika ülesande salvestiste jaoks</span><span class="sxs-lookup"><span data-stu-id="e8e9a-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="e8e9a-104">Enne alustamist</span><span class="sxs-lookup"><span data-stu-id="e8e9a-104">Before you begin</span></span>

<span data-ttu-id="e8e9a-105">Selles teemas jagatakse teavet selle kohta, kuidas analüüsida ja hallata tegevuse salvestise põhjal turvaõiguste nõudeid.</span><span class="sxs-lookup"><span data-stu-id="e8e9a-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="e8e9a-106">Enne teemas toodud etappide täitmist peab teil olema selle äriprotsessi tegevuse salvestis, mida soovite analüüsida.</span><span class="sxs-lookup"><span data-stu-id="e8e9a-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="e8e9a-107">Äriprotsessi salvestamiseks vt teemat [Tegevuse salvestaja vahendid](../../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="e8e9a-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="e8e9a-108">Tegevuse salvestise turvalisuse haldamine</span><span class="sxs-lookup"><span data-stu-id="e8e9a-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="e8e9a-109">Avage **Süsteemihaldus** > **Turve** > **Tegevuse salvestise turbediagnostika**.</span><span class="sxs-lookup"><span data-stu-id="e8e9a-109">Go to **System administration** > **Security** > **Security diagnostic for task recording**.</span></span>
2. <span data-ttu-id="e8e9a-110">Avage tegevuse salvestis selle asukohas.</span><span class="sxs-lookup"><span data-stu-id="e8e9a-110">Open the task recording from its location.</span></span> <span data-ttu-id="e8e9a-111">Valige **Ava sellest arvutist** või **Ava rakendusest Lifecycle Services** ja seejärel valige **Sulge**.</span><span class="sxs-lookup"><span data-stu-id="e8e9a-111">Select **Open from this PC** or **Open from Lifecycle Services**, and then select **Close**.</span></span>
3. <span data-ttu-id="e8e9a-112">See avab lehe **Turbemenüü käsu üksikasjad**, kus on loetletud protsessi jaoks nõutud turbeobjektid.</span><span class="sxs-lookup"><span data-stu-id="e8e9a-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="e8e9a-113">Loetelu ei hõlma menüükäske **Tegevus** ja **Väljund**.</span><span class="sxs-lookup"><span data-stu-id="e8e9a-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="e8e9a-114">Valige kasutaja väljal **Kasutaja ID**.</span><span class="sxs-lookup"><span data-stu-id="e8e9a-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="e8e9a-115">Kui kasutajal puudub mõne menüükäsu kohta luba, siis uuendatakse välja **Puuduvad load** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e8e9a-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes**.</span></span>
  
  ![Turbemenüü käsu üksikasjade leht](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="e8e9a-117">Valige suvand **Lisa viide**, et näha turbeobjektide loetelu, sealhulgas rollid, kohustused ja privileegid, mis tagavad puuduva loa.</span><span class="sxs-lookup"><span data-stu-id="e8e9a-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="e8e9a-118">Valige loendist turbeobjekt.</span><span class="sxs-lookup"><span data-stu-id="e8e9a-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="e8e9a-119">Kui **Roll** on valitud, siis valige **Lisa kasutajale roll**.</span><span class="sxs-lookup"><span data-stu-id="e8e9a-119">If **Role** is selected, select **Add role to user**.</span></span> <span data-ttu-id="e8e9a-120">See avab lehe **Määra rollidele kasutajaid**.</span><span class="sxs-lookup"><span data-stu-id="e8e9a-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="e8e9a-121">Lisainfo saamiseks vt lehte [Kasutajatele turberollide määramine](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="e8e9a-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="e8e9a-122">Kui **Kohustus** on valitud, siis valige **Lisa rollile kohustus**, valige rollid, millele tuleks kohustus lisada ning seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8e9a-122">If **Duty** is selected, select **Add duty to role**, select the roles that the duty should be added to, and then select **OK**.</span></span>
    - <span data-ttu-id="e8e9a-123">Kui **Privileeg** on valitud, siis valige **Lisa kohustustele privileeg**, valige rollid, millele tuleks kohustus lisada ning seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8e9a-123">If **Privilege** is selected, select **Add privilege to duties**, select the roles that the duty should be added to, and then select **OK**.</span></span>
