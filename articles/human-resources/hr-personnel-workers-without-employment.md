---
title: Tööta töötajad
description: Töötajad, kellel puudub tulevane, aktiivne või ajalooline töösuhe teie organisatsioonis, ilmuvad vormile Töötajad ilma töösuheteta.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1a137de25924f4c4ec6f6b1fe70f9d21af591c0
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924567"
---
# <a name="workers-without-employment"></a><span data-ttu-id="81c26-103">Tööta töötajad</span><span class="sxs-lookup"><span data-stu-id="81c26-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="81c26-104">Töötajad, kellel puudub tulevane, aktiivne või ajalooline töösuhe teie organisatsioonis, ilmuvad vormile **Töötajad ilma töösuheteta**.</span><span class="sxs-lookup"><span data-stu-id="81c26-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="81c26-105">Selle olekuga töötajad võivad ilmuda siis, kui impordite ilma töökirjeta töötajaid või kui kustutate töötaja tööhõive jaotises **Töötajad > Tööhõive ajalugu**.</span><span class="sxs-lookup"><span data-stu-id="81c26-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="81c26-106">Vaikimisi on vorm **Tööhõiveta töötajad** saadaval järgmistele rollidele.</span><span class="sxs-lookup"><span data-stu-id="81c26-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="81c26-107">Inimressursside assistent</span><span class="sxs-lookup"><span data-stu-id="81c26-107">Human Resources Assistant</span></span>
- <span data-ttu-id="81c26-108">Inimressursside haldur</span><span class="sxs-lookup"><span data-stu-id="81c26-108">Human Resources Manager</span></span>
- <span data-ttu-id="81c26-109">Värbaja</span><span class="sxs-lookup"><span data-stu-id="81c26-109">Recruiter</span></span>
- <span data-ttu-id="81c26-110">Hüvitise ja eeliste haldur</span><span class="sxs-lookup"><span data-stu-id="81c26-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="81c26-111">Palgaarvestuse administraator</span><span class="sxs-lookup"><span data-stu-id="81c26-111">Payroll Administrator</span></span>
- <span data-ttu-id="81c26-112">Palgaarvestuse haldur</span><span class="sxs-lookup"><span data-stu-id="81c26-112">Payroll Manager</span></span>
- <span data-ttu-id="81c26-113">Koolitusjuht</span><span class="sxs-lookup"><span data-stu-id="81c26-113">Training Manager</span></span>

<span data-ttu-id="81c26-114">Loendis **Töötajad ilma töösuheteta** saate loetletud isikud kustutada.</span><span class="sxs-lookup"><span data-stu-id="81c26-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="81c26-115">Vaikimisi on see privileeg antud Inimressursside abilise rollile.</span><span class="sxs-lookup"><span data-stu-id="81c26-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="81c26-116">Saate selle privileegi järgmiste sammudega anda teistele rollidele.</span><span class="sxs-lookup"><span data-stu-id="81c26-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="81c26-117">Valige suvand **Süsteemihaldus** ja seejärel valige suvand **Turbekonfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="81c26-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="81c26-118">Vahekaardil **Privileegid** filtreerige loendit **Privileegid** suvandi **Töötajate haldamine** alusel.</span><span class="sxs-lookup"><span data-stu-id="81c26-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="81c26-119">[![Filtreerige privileegide loendit](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="81c26-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="81c26-120">Valige veerus **Viited** suvand **Kuvamenüü üksused**.</span><span class="sxs-lookup"><span data-stu-id="81c26-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="81c26-121">Valige veerus **Kuvamenüü üksused** suvand **HcmWorkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="81c26-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="81c26-122">[![Vali vorm](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="81c26-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="81c26-123">Määrake õigus **Kustuta** olekusse **Luba**.</span><span class="sxs-lookup"><span data-stu-id="81c26-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="81c26-124">Valige vahekaart **Avaldamata objektid**.</span><span class="sxs-lookup"><span data-stu-id="81c26-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="81c26-125">Valige **Avalda kõik**.</span><span class="sxs-lookup"><span data-stu-id="81c26-125">Select **Publish all**.</span></span>

   <span data-ttu-id="81c26-126">[![Avalda muudatused](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="81c26-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]