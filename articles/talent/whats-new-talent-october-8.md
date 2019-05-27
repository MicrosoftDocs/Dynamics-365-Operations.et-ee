---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent Core HR (1. oktoober 2018)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talent Core HR-i uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 92f06d29dfa8110106a2a0e71434b2c0c75110b5
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517826"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-8-2018"></a><span data-ttu-id="1186e-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent Core HR (8. oktoober 2018)</span><span class="sxs-lookup"><span data-stu-id="1186e-103">What's new or changed in Dynamics 365 for Talent Core HR (October 8, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1186e-104">**Järk 8.1.1050.0**</span><span class="sxs-lookup"><span data-stu-id="1186e-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="1186e-105">Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.</span><span class="sxs-lookup"><span data-stu-id="1186e-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="1186e-106">Luba teiste kuupäevade kasutamist puhkuste järgu alusel (puhkuste haldus)</span><span class="sxs-lookup"><span data-stu-id="1186e-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="1186e-107">Töövõtjale puhkuste andmisel määrab puhkuse järgu alus, kui palju puhkusepäevi töövõtjal on kogunenud.</span><span class="sxs-lookup"><span data-stu-id="1186e-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="1186e-108">Praegu põhinevad need järgud töösuhte alguskuupäeval ja töövõtja staaži kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="1186e-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="1186e-109">Mõnel juhul on organisatsioonidel vaja, et need järgud põhineksid teistel kuupäevadel, näiteks tähtpäeva kuupäeval või tegeliku palkamise kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="1186e-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="1186e-110">Need kuupäevad on juba kasutuses puhkuseplaanis, et määratleda juurdekasvude toimumine, lisatud on nende samade kuupäevade kasutamise võimalus, kui töötaja lisatakse plaani, et määratleda juurdekasvu summa.</span><span class="sxs-lookup"><span data-stu-id="1186e-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="1186e-111">Muud muudatused</span><span class="sxs-lookup"><span data-stu-id="1186e-111">Other changes</span></span>
<span data-ttu-id="1186e-112">Sellesse väljaandesse on lisatud mitmesugused parandused.</span><span class="sxs-lookup"><span data-stu-id="1186e-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="1186e-113">Teadaolev probleem</span><span class="sxs-lookup"><span data-stu-id="1186e-113">Known issue</span></span>

<span data-ttu-id="1186e-114">**Probleem:** töötajale uue manuse lisamisel on nupud **Uus** ja **Redigeeri** hallid. **Lahendus:** enne manuselehe avamist veenduge, et kiirinfod lehel **Töötaja** oleksid suletud.</span><span class="sxs-lookup"><span data-stu-id="1186e-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="1186e-115">Kui kiirinfod on lehe **Töötaja** laadimisel suletud, on manuste nupud lubatud.</span><span class="sxs-lookup"><span data-stu-id="1186e-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="1186e-116">(See probleem lahendatakse järgmisel platvormivärskendusel.)</span><span class="sxs-lookup"><span data-stu-id="1186e-116">(This issue will be fixed in the next platform update.)</span></span>
