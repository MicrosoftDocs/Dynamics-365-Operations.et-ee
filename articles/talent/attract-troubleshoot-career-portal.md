---
title: Attracti kasutajad ei saa karjääriportaalis töökohtadele kandideerida
description: Selles teemas selgitatakse probleemi tõrkeotsingut, kus Attracti kasutajad ei saa karjääriportaalis töödele kandideerida.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460890"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="81b3a-103">Attracti kasutajad ei saa karjääriportaalis töökohtadele kandideerida</span><span class="sxs-lookup"><span data-stu-id="81b3a-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="81b3a-104">Väljasta</span><span class="sxs-lookup"><span data-stu-id="81b3a-104">Issue</span></span>

<span data-ttu-id="81b3a-105">Attracti kasutajad ei saa karjääriportaalis töökohtadele kandideerida.</span><span class="sxs-lookup"><span data-stu-id="81b3a-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="81b3a-106">Kui nad proovivad Dynamics 365 Talent: Attractis loodud töökohale kandideerida, siis brauser laadib pidevalt lehte ega vii tegevust lõpule.</span><span class="sxs-lookup"><span data-stu-id="81b3a-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="81b3a-107">Põhjus</span><span class="sxs-lookup"><span data-stu-id="81b3a-107">Cause</span></span>

<span data-ttu-id="81b3a-108">See probleem ilmneb siis, kui talendisuhete meeskonnal ei ole talendi kasutajarolli.</span><span class="sxs-lookup"><span data-stu-id="81b3a-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="81b3a-109">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="81b3a-109">Resolution</span></span>

<span data-ttu-id="81b3a-110">Määrake talendi kasutajaroll talendisuhete meeskonnale.</span><span class="sxs-lookup"><span data-stu-id="81b3a-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="81b3a-111">Logige sisse [Power Platform i halduskeskusse](https://admin.powerplatform.microsoft.com) mis tahes järgmise administraatori identimisteabega.</span><span class="sxs-lookup"><span data-stu-id="81b3a-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="81b3a-112">Dynamics 365 administraator</span><span class="sxs-lookup"><span data-stu-id="81b3a-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="81b3a-113">Globaalne administraator</span><span class="sxs-lookup"><span data-stu-id="81b3a-113">Global admin</span></span>
   - <span data-ttu-id="81b3a-114">Power Platformi administraator</span><span class="sxs-lookup"><span data-stu-id="81b3a-114">Power Platform admin</span></span>

2. <span data-ttu-id="81b3a-115">Navigeerimispaanil valige **Keskkond** ja seejärel valige keskkond, milles määrata talendi kasutajaroll talendisuhete meeskonnale.</span><span class="sxs-lookup"><span data-stu-id="81b3a-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![Keskkonna valimine](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="81b3a-117">Valige paanil **Keskkonnad** **Keskkonna URL** ja logige sisse keskkonna haldusportaali (nt https:<orgname>.crm.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="81b3a-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="81b3a-118">Valige **Sätted**, valige **Süsteem** ja seejärel valige **Turve**.</span><span class="sxs-lookup"><span data-stu-id="81b3a-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![Turbe juurde liikumine](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="81b3a-120">Valige **Meeskonnad**.</span><span class="sxs-lookup"><span data-stu-id="81b3a-120">Select **Teams**.</span></span>

   ![Meeskondade valimine](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="81b3a-122">Sisestage otsinguväljale **Talendisuhete meeskond** ja valige seejärel otsingutulemustest meeskond.</span><span class="sxs-lookup"><span data-stu-id="81b3a-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="81b3a-123">Valige lindilt **ROLLIDE HALDAMINE**.</span><span class="sxs-lookup"><span data-stu-id="81b3a-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="81b3a-124">Valige dialoogis **Meeskonnarollide haldamine** saadaolevate rollide loendist **Talendi kasutaja** ja seejärel valige rolli rakendamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="81b3a-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![Rolli rakendamine](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="81b3a-126">Testige muudatusi.</span><span class="sxs-lookup"><span data-stu-id="81b3a-126">Test your changes:</span></span>

   1. <span data-ttu-id="81b3a-127">Logige karjääriportaali sisse uues brauseriaknas.</span><span class="sxs-lookup"><span data-stu-id="81b3a-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="81b3a-128">Kandideerige karjääriportaalis tööle.</span><span class="sxs-lookup"><span data-stu-id="81b3a-128">Apply for the job from the career portal.</span></span> 