---
title: Kinni jäänud pakett-tööde lähtestamine
description: See teema kirjeldab, kuidas lahendada probleemid pakett-töödega, mis on kinni jäänud.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 906a391b3c28d15445f6ddf0fc547ebcf842ba19
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881756"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="557dd-103">Kinni jäänud pakett-tööde lähtestamine</span><span class="sxs-lookup"><span data-stu-id="557dd-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="557dd-104">Väljasta</span><span class="sxs-lookup"><span data-stu-id="557dd-104">Issue</span></span>

<span data-ttu-id="557dd-105">Microsoft Dynamics 365 Human Resources -il võib tekkida probleeme pakett-töödega, mis on jäänud kinni kas **Teostamise** või **Tühistamise** olekusee ja mida ei saa lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="557dd-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="557dd-106">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="557dd-106">Resolution</span></span>

<span data-ttu-id="557dd-107">Kui pakett-töö on jäänud kinni **Teostamise** või **Tühistamise** olekusse, saate oleku lähtestada, käivitades töö tühistamise.</span><span class="sxs-lookup"><span data-stu-id="557dd-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="557dd-108">Pärast selle tühistamine saate lähtestada pakett-töö, seadistades selle olekusse **Ootel**.</span><span class="sxs-lookup"><span data-stu-id="557dd-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="557dd-109">Seejärel korjatakse see jälle üles, et läbiviia järjekordne planeeritud pakett-töö käivitus.</span><span class="sxs-lookup"><span data-stu-id="557dd-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="557dd-110">**Süsteemihalduse** tööruumis valige leht **Lingid** ja valige **Pakett-tööd**.</span><span class="sxs-lookup"><span data-stu-id="557dd-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="557dd-111">**Pakett-töö** loendilehel valige töö, mida on vaja lähtestada.</span><span class="sxs-lookup"><span data-stu-id="557dd-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="557dd-112">Toiminguribal valige **Sundtühista** ja kinnita tühistamine.</span><span class="sxs-lookup"><span data-stu-id="557dd-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="557dd-113">**Sundtühista** käsk on kättesaadav kui valitud pakett-töö staatus on kas **Käivitamine** või **Tühistamine** ja ühtki paketi käivitamise või tühistamise protsessi ei käitata töö jaoks.</span><span class="sxs-lookup"><span data-stu-id="557dd-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="557dd-114">Tegevusribal vali **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="557dd-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="557dd-115">Lehel **Vali uus olek** valige **Ootamine** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="557dd-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![Valige uus pakett-töö olek](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="557dd-117">Vt ka</span><span class="sxs-lookup"><span data-stu-id="557dd-117">See also</span></span>

[<span data-ttu-id="557dd-118">Jõudluse optimeerimine pakett-tööde planeerimisel pärast tööaega</span><span class="sxs-lookup"><span data-stu-id="557dd-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="557dd-119">Jõudluse optimeerimine automaatsete puhastamisülesannetega</span><span class="sxs-lookup"><span data-stu-id="557dd-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
