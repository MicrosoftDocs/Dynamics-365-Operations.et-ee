---
title: Turbediagnostika ülesande salvestiste jaoks
description: Selles teemas jagatakse teavet selle kohta, kuidas analüüsida ja hallata tegevuse salvestise põhjal turvaõiguste nõudeid.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 99f9da527e818892eb3f46aceca3cc4588b99e81
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570977"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="27d10-103">Turbediagnostika ülesande salvestiste jaoks</span><span class="sxs-lookup"><span data-stu-id="27d10-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="27d10-104">Enne alustamist</span><span class="sxs-lookup"><span data-stu-id="27d10-104">Before you begin</span></span>

<span data-ttu-id="27d10-105">Selles teemas jagatakse teavet selle kohta, kuidas analüüsida ja hallata tegevuse salvestise põhjal turvaõiguste nõudeid.</span><span class="sxs-lookup"><span data-stu-id="27d10-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="27d10-106">Enne teemas toodud etappide täitmist peab teil olema selle äriprotsessi tegevuse salvestis, mida soovite analüüsida.</span><span class="sxs-lookup"><span data-stu-id="27d10-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="27d10-107">Äriprotsessi salvestamiseks vt teemat [Tegevuse salvestaja vahendid](../../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="27d10-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="27d10-108">Tegevuse salvestise turvalisuse haldamine</span><span class="sxs-lookup"><span data-stu-id="27d10-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="27d10-109">Avage **Süsteemihaldus** > **Turve** > **Tegevuse salvestise turbediagnostika**.</span><span class="sxs-lookup"><span data-stu-id="27d10-109">Go to **System administration** > **Security** > **Security diagnostic for task recording**.</span></span>
2. <span data-ttu-id="27d10-110">Avage tegevuse salvestis selle asukohas.</span><span class="sxs-lookup"><span data-stu-id="27d10-110">Open the task recording from its location.</span></span> <span data-ttu-id="27d10-111">Valige **Ava sellest arvutist** või **Ava rakendusest Lifecycle Services** ja seejärel valige **Sulge**.</span><span class="sxs-lookup"><span data-stu-id="27d10-111">Select **Open from this PC** or **Open from Lifecycle Services**, and then select **Close**.</span></span>
3. <span data-ttu-id="27d10-112">See avab lehe **Turbemenüü käsu üksikasjad**, kus on loetletud protsessi jaoks nõutud turbeobjektid.</span><span class="sxs-lookup"><span data-stu-id="27d10-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="27d10-113">Loetelu ei hõlma menüükäske **Tegevus** ja **Väljund**.</span><span class="sxs-lookup"><span data-stu-id="27d10-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="27d10-114">Valige kasutaja väljal **Kasutaja ID**.</span><span class="sxs-lookup"><span data-stu-id="27d10-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="27d10-115">Kui kasutajal puudub mõne menüükäsu kohta luba, siis uuendatakse välja **Puuduvad load** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="27d10-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes**.</span></span>
  
  ![Turbemenüü käsu üksikasjade leht](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="27d10-117">Valige suvand **Lisa viide**, et näha turbeobjektide loetelu, sealhulgas rollid, kohustused ja privileegid, mis tagavad puuduva loa.</span><span class="sxs-lookup"><span data-stu-id="27d10-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="27d10-118">Valige loendist turbeobjekt.</span><span class="sxs-lookup"><span data-stu-id="27d10-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="27d10-119">Kui **Roll** on valitud, siis valige **Lisa kasutajale roll**.</span><span class="sxs-lookup"><span data-stu-id="27d10-119">If **Role** is selected, select **Add role to user**.</span></span> <span data-ttu-id="27d10-120">See avab lehe **Määra rollidele kasutajaid**.</span><span class="sxs-lookup"><span data-stu-id="27d10-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="27d10-121">Lisainfo saamiseks vt lehte [Kasutajatele turberollide määramine](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="27d10-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="27d10-122">Kui **Kohustus** on valitud, siis valige **Lisa rollile kohustus**, valige rollid, millele tuleks kohustus lisada ning seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="27d10-122">If **Duty** is selected, select **Add duty to role**, select the roles that the duty should be added to, and then select **OK**.</span></span>
    - <span data-ttu-id="27d10-123">Kui **Privileeg** on valitud, siis valige **Lisa kohustustele privileeg**, valige rollid, millele tuleks kohustus lisada ning seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="27d10-123">If **Privilege** is selected, select **Add privilege to duties**, select the roles that the duty should be added to, and then select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]