---
title: Värbamistöörühma loomine, kasutades rakendust Dynamics 365 for Talent - Onboard
description: Selles teemas selgitatakse, kuidas kasutada Microsoft Dynamics 365 for Talent - Onboard rakendust, et luua sisseelamismeeskonnad.
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 996fc42881ce708992614c58877927e03bbf78bf
ms.sourcegitcommit: 9f762fa89c5b432667aa156c22d679a7f601952d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/08/2019
ms.locfileid: "1731435"
---
# <a name="create-a-hiring-team-by-using-dynamics-365-for-talent-onboard"></a><span data-ttu-id="01275-103">Värbamistöörühma loomine, kasutades rakendust Dynamics 365 for Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="01275-103">Create a hiring team by using Dynamics 365 for Talent: Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="01275-104">Microsoft Dynamics 365 for Talent: Onboardis saate luua värbamismeeskonnad.</span><span class="sxs-lookup"><span data-stu-id="01275-104">In Microsoft Dynamics 365 for Talent: Onboard, you can create hiring teams.</span></span> <span data-ttu-id="01275-105">Seejärel saate igale meeskonnale määrata sisseelamisjuhendid ja -mallid.</span><span class="sxs-lookup"><span data-stu-id="01275-105">You can then assign onboarding guides and templates to each team.</span></span>

## <a name="create-a-hiring-team"></a><span data-ttu-id="01275-106">Värbamistöörühma loomine</span><span class="sxs-lookup"><span data-stu-id="01275-106">Create a hiring team</span></span>

1. <span data-ttu-id="01275-107">Valige vasakpoolses menüüs **Meeskonnad**.</span><span class="sxs-lookup"><span data-stu-id="01275-107">On the left menu, select **Teams**.</span></span>
2. <span data-ttu-id="01275-108">Valige jaotises **Meeskonnad** **Lisa** (plussmärk \[**+**\]) paan.</span><span class="sxs-lookup"><span data-stu-id="01275-108">Under **Teams**, select the **Add** (plus sign \[**+**\]) tile.</span></span>
3. <span data-ttu-id="01275-109">Sisestage dialoogiboksis **Uue meeskonna loomine** **Meeskonna nime** alla värbamismeeskonna nimi.</span><span class="sxs-lookup"><span data-stu-id="01275-109">In the **Create a new team** dialog box, under **Team name**, enter a name for the hiring team.</span></span>

    ![[<span data-ttu-id="01275-110">Uue meeskonna loomine Onboardis</span><span class="sxs-lookup"><span data-stu-id="01275-110">Creating a new team in Onboard</span></span>](./media/onboard-create-team.png)](./media/onboard-create-team.png)

4. <span data-ttu-id="01275-111">Sisestage jaotises **Valige meeskonna liikmed** iga meeskonnaliikme nimi või meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="01275-111">Under **Choose team members**, enter the name or email address of each team member.</span></span>

    <span data-ttu-id="01275-112">Meeskonnaliikmete eemaldamiseks valige **X**, mis kuvatakse välja all nende nime kõrval.</span><span class="sxs-lookup"><span data-stu-id="01275-112">To remove team members, select the **X** that appears next to their name under the box.</span></span>

5. <span data-ttu-id="01275-113">Uute meeskonnaliikmete meiliga sisselülitamiseks lülitage sisse suvand **Saada meil uutele liikmetele**.</span><span class="sxs-lookup"><span data-stu-id="01275-113">To email new team members, turn on the **Send an email to the new members** option.</span></span>
6. <span data-ttu-id="01275-114">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="01275-114">Select **Create**.</span></span>
7. <span data-ttu-id="01275-115">Kui olete teatanud, et soovite saata meiliga uued meeskonnaliikmed, redigeerige meili järgmises dialoogiboksis ja valige **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="01275-115">If you indicated that you want to email new team members, edit the email in the next dialog box, and then select **Done**.</span></span>

## <a name="assign-onboarding-guides-to-a-hiring-team"></a><span data-ttu-id="01275-116">Värbamismeeskonnale sisseelamisjuhendite määramine</span><span class="sxs-lookup"><span data-stu-id="01275-116">Assign onboarding guides to a hiring team</span></span>

1. <span data-ttu-id="01275-117">Valige vasakpoolses menüüs **Meeskonnad**.</span><span class="sxs-lookup"><span data-stu-id="01275-117">On the left menu, select **Teams**.</span></span>
2. <span data-ttu-id="01275-118">Valige meeskond.</span><span class="sxs-lookup"><span data-stu-id="01275-118">Select the team.</span></span>
3. <span data-ttu-id="01275-119">Valige vahekaardil **Juhendid** valik **Lisa juhendid**.</span><span class="sxs-lookup"><span data-stu-id="01275-119">On the **Guides** tab, select **Add guides**.</span></span>

    ![[<span data-ttu-id="01275-120">Sisseelamisjuhendite lisamine meeskonnale</span><span class="sxs-lookup"><span data-stu-id="01275-120">Adding onboarding guides to a team</span></span>](./media/onboard-add-guides-to-team.png)](./media/onboard-add-guides-to-team.png)

4. <span data-ttu-id="01275-121">Märkige ruut iga sisseelamisjuhendi kohta, mida soovite meeskonnale määrata, ja seejärel valige käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="01275-121">Select the check box for each onboarding guide that you want to assign to the team, and then select **Add**.</span></span>

    ![[<span data-ttu-id="01275-122">Sisseelamisjuhendite valimine meeskonnale lisamiseks</span><span class="sxs-lookup"><span data-stu-id="01275-122">Selecting the onboarding guides to add to the team</span></span>](./media/onboard-select-guides.png)](./media/onboard-select-guides.png)

## <a name="assign-onboarding-templates-to-a-hiring-team"></a><span data-ttu-id="01275-123">Värbamismeeskonnale sisseelamismallide määramine</span><span class="sxs-lookup"><span data-stu-id="01275-123">Assign onboarding templates to a hiring team</span></span>

1. <span data-ttu-id="01275-124">Valige vasakpoolses menüüs **Meeskonnad**.</span><span class="sxs-lookup"><span data-stu-id="01275-124">On the left menu, select **Teams**.</span></span>
2. <span data-ttu-id="01275-125">Valige meeskond.</span><span class="sxs-lookup"><span data-stu-id="01275-125">Select the team.</span></span>
3. <span data-ttu-id="01275-126">Valige vahekaardil **Mallid** valik **Lisa mallid**.</span><span class="sxs-lookup"><span data-stu-id="01275-126">On the **Templates** tab, select **Add templates**.</span></span>

    ![[<span data-ttu-id="01275-127">Mallide lisamine meeskonnale</span><span class="sxs-lookup"><span data-stu-id="01275-127">Adding templates to a team</span></span>](./media/onboard-add-templates-to-team.png)](./media/onboard-add-templates-to-team.png)

4. <span data-ttu-id="01275-128">Märkige ruut iga malli kohta, mida soovite meeskonnale määrata, ja seejärel valige käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="01275-128">Select the check box for each template that you want to assign to the team, and then select **Add**.</span></span>

    ![[<span data-ttu-id="01275-129">Mallide valimine meeskonnale lisamiseks</span><span class="sxs-lookup"><span data-stu-id="01275-129">Selecting the templates to add to the team</span></span>](./media/onboard-select-templates.png)](./media/onboard-select-templates.png)

### <a name="see-also"></a><span data-ttu-id="01275-130">Vt ka</span><span class="sxs-lookup"><span data-stu-id="01275-130">See also</span></span>

- [<span data-ttu-id="01275-131">Proovige või ostke Onboardi rakendus</span><span class="sxs-lookup"><span data-stu-id="01275-131">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="01275-132">Mis on uut?</span><span class="sxs-lookup"><span data-stu-id="01275-132">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="01275-133">Väljalaskemärkmed</span><span class="sxs-lookup"><span data-stu-id="01275-133">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="01275-134">Toe hankimine</span><span class="sxs-lookup"><span data-stu-id="01275-134">Get support</span></span>](./talent-support.md)