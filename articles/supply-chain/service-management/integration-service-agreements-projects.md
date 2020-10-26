---
title: Hoolduslepete ja projektide integreerimine
description: Hoolduslepete ja hooldusleppe ridadega töötamisel saate kasutada jaotise Projektihaldus ja raamatupidamine osades seadistatud andmeid.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 578e4b9fe5ef487e999fd0de28d7566bad21fd89
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985579"
---
# <a name="integration-for-service-agreements-and-projects"></a><span data-ttu-id="7b25d-103">Hoolduslepete ja projektide integreerimine</span><span class="sxs-lookup"><span data-stu-id="7b25d-103">Integration for service agreements and projects</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7b25d-104">Hoolduslepete ja hooldusleppe ridadega töötamisel saate kasutada jaotise **Projektihaldus ja raamatupidamine** järgmistes osades seadistatud andmeid.</span><span class="sxs-lookup"><span data-stu-id="7b25d-104">When you work with service agreements and service agreement lines, you use data that is set up in the following areas in **Project management and accounting**.</span></span>

## <a name="project-prices"></a><span data-ttu-id="7b25d-105">Projekti hinnad</span><span class="sxs-lookup"><span data-stu-id="7b25d-105">Project prices</span></span>

<span data-ttu-id="7b25d-106">Hooldusleppe kande omahind ja müügihind saadakse omahinna seadistusest, mis rakendub hooldusleppega seotud projektile.</span><span class="sxs-lookup"><span data-stu-id="7b25d-106">The cost and the sales price for a service agreement transaction are derived from the cost price setup that applies to the project that is attached to the service agreement.</span></span> <span data-ttu-id="7b25d-107">Omahinna ja müügihinna saab seadistada projekti, töötaja või kategooria alusel.</span><span class="sxs-lookup"><span data-stu-id="7b25d-107">Cost and sales prices can be set up by project, employee, and category.</span></span> 

## <a name="project-validation"></a><span data-ttu-id="7b25d-108">Projekti kontrollimine</span><span class="sxs-lookup"><span data-stu-id="7b25d-108">Project validation</span></span>

<span data-ttu-id="7b25d-109">Hooldusleppe real valimiseks saadaval olevaid projekte, töötajaid ja kategooriaid saab limiteerida kontrolli seadistamisega jaotises **Projektihaldus ja raamatupidamine**.</span><span class="sxs-lookup"><span data-stu-id="7b25d-109">The projects, employees, and categories that are available for selection on a service agreement line can be limited by the validation setup in **Project management and accounting**.</span></span> <span data-ttu-id="7b25d-110">Kontrolli seadistamise abil saate juurdepääsu juhtimiseks kombineerida töötajaid, projekte ja kategooriaid.</span><span class="sxs-lookup"><span data-stu-id="7b25d-110">By using the validation setup, you can combine employees, projects, and categories for control access.</span></span> 

## <a name="project-line-properties"></a><span data-ttu-id="7b25d-111">Projektirea atribuudid</span><span class="sxs-lookup"><span data-stu-id="7b25d-111">Project line properties</span></span>

<span data-ttu-id="7b25d-112">Rea atribuut sisestatakse automaatselt hooldusleppe reale.</span><span class="sxs-lookup"><span data-stu-id="7b25d-112">A line property is entered automatically for a service agreement line.</span></span>

<span data-ttu-id="7b25d-113">Rea atribuudid luuakse **Projektihalduse ja raamatupidamise** vormil **Rea atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="7b25d-113">Line properties are created in the **Line properties** form in **Project management and accounting**.</span></span> <span data-ttu-id="7b25d-114">Hooldusleppesse sisestatud rea atribuut seotakse hooldusleppe jaoks valitud projektiga ja seejärel tuletatakse hooldusleppe realt.</span><span class="sxs-lookup"><span data-stu-id="7b25d-114">The line property that is entered on a service agreement is attached to the project that is selected for the service agreement and inherited subsequently by the service agreement line.</span></span> 

## <a name="default-offset-accounts"></a><span data-ttu-id="7b25d-115">Vaikevastaskontod</span><span class="sxs-lookup"><span data-stu-id="7b25d-115">Default offset accounts</span></span>

<span data-ttu-id="7b25d-116">Kui sisestate kulukande, valitakse selle kande jaoks automaatselt kulu vaikevastaskonto.</span><span class="sxs-lookup"><span data-stu-id="7b25d-116">If you enter an expense transaction, a default expense offset account is selected automatically for the transaction.</span></span> <span data-ttu-id="7b25d-117">Kulu vaikevastaskonto seadistatakse praeguse hooldusleppega seotud projekti kohta.</span><span class="sxs-lookup"><span data-stu-id="7b25d-117">The default expense account is set up for the project that is attached to the current service agreement.</span></span>

## <a name="project-categories"></a><span data-ttu-id="7b25d-118">Projekti kategooriad</span><span class="sxs-lookup"><span data-stu-id="7b25d-118">Project categories</span></span>

<span data-ttu-id="7b25d-119">Hooldusleppe ridade jaoks saadaval olevad kategooriad saate seadistada **Projektihalduse ja raamatupidamise** vormil **Projekti kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="7b25d-119">The categories that are available for service agreement lines are set up in the **Project categories** form in **Project management and accounting**.</span></span> 

> [!NOTE]
> <P><span data-ttu-id="7b25d-120">Valimiseks on saadaval kategooriad, mille puhul on valitud märkeruut <STRONG>Aktiivne töölehtedel</STRONG> vahekaardil <STRONG>Projekt</STRONG> vormil <STRONG>Projekti kategooriad</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="7b25d-120">Categories that have the <STRONG>Active in journals</STRONG> check box selected on the <STRONG>Project</STRONG> tab in the <STRONG>Project categories</STRONG> form are available for selection.</span></span> <span data-ttu-id="7b25d-121">Ent kui on valitud märkeruut <STRONG>Passiivsed kategooriad</STRONG> vahekaardil <STRONG>Töölehed</STRONG> vormil <STRONG>Projektihalduse ja raamatupidamise parameetrid</STRONG>, on kõik kategooriad valimiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="7b25d-121">However, if the <STRONG>Inactive categories</STRONG> check box is selected on the <STRONG>Journals</STRONG> tab in the <STRONG>Project management and accounting parameters</STRONG> form, all categories are available for selection.</span></span></P>

## <a name="project-parameters"></a><span data-ttu-id="7b25d-122">Projekti parameetrid</span><span class="sxs-lookup"><span data-stu-id="7b25d-122">Project parameters</span></span>

<span data-ttu-id="7b25d-123">Kui valitud on märkeruut **Töötajad, kellega on leping lõpetatud** vahekaardil **Töölehed** vormil **Projektihalduse ja raamatupidamise parameetrid**, saate passiivseid ja aktiivseid töötajaid valida vormidel **Hoolduslepped** ja **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="7b25d-123">If the **Terminated workers** field on the **Journals** tab in the **Project management and accounting parameters** form is selected, you can select inactive employees and active employees in the **Service agreements** and **Service orders** forms.</span></span>

<span data-ttu-id="7b25d-124">Samuti saate lubada väljad **Algusaeg** ja **Lõppaeg** vahekaardil **Projekt** vormil **Hooldustellimused**, et sisestada hooldustellimuse ridadele algus- ja lõppaeg.</span><span class="sxs-lookup"><span data-stu-id="7b25d-124">Also, you can enable the **Start time** and **End time** fields on the **Project** tab in the **Service orders** form to enter starting and ending times on service order lines.</span></span>

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a><span data-ttu-id="7b25d-125">Hooldustellimuste algus- ja lõppaja funktsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="7b25d-125">Enable the starting and ending time feature for service orders</span></span>

1.  <span data-ttu-id="7b25d-126">Klõpsake valikuid **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Projektihalduse ja raamatupidamise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="7b25d-126">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="7b25d-127">Klõpsake vahekaarti **Töölehed** ja seejärel valige märkeruut **Näita algus-/lõppaegu**.</span><span class="sxs-lookup"><span data-stu-id="7b25d-127">Click the **Journals** tab, and then select the **Show start/end times** check box.</span></span>

3.  <span data-ttu-id="7b25d-128">Klõpsake valikuid **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Töölehed** \> **Töölehenimed**.</span><span class="sxs-lookup"><span data-stu-id="7b25d-128">Click **Project management and accounting** \> **Setup** \> **Journals** \> **Journal names**.</span></span>

4.  <span data-ttu-id="7b25d-129">Valige hooldustellimusega seotud töölehe nimi.</span><span class="sxs-lookup"><span data-stu-id="7b25d-129">Select the journal name that is attached to the service order.</span></span>

5.  <span data-ttu-id="7b25d-130">Klõpsake vahekaarti **Üldine** ja seejärel valige märkeruut **Näita algus-/lõppaegu**.</span><span class="sxs-lookup"><span data-stu-id="7b25d-130">Click the **General** tab, and then select the **Show start/end times** check box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7b25d-131">Valige hooldustellimuse töölehe nimi väljal <STRONG>Tund</STRONG> vahekaardil <STRONG>Töölehed</STRONG> vormil <STRONG>Teenuste halduse parameetrid</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="7b25d-131">Select the journal name for the service order in the <STRONG>Hour</STRONG> field on the <STRONG>Journals</STRONG> tab in the <STRONG>Service management parameters</STRONG> form.</span></span></P>





