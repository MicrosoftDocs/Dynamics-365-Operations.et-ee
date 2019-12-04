---
title: Andmesisestuse hõlbustamiseks kirje malli loomine
description: Selles teemas näidatakse, kuidas luua kirje malli, nii et välja väärtusi, mida tihti kasutatakse, ei peaks iga kirje puhul eraldi sisestama.
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08ee7d0f0ce7e92eaa85137dcd2761bfd702eb8c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181929"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="dd4ea-103">Andmesisestuse hõlbustamiseks kirje malli loomine</span><span class="sxs-lookup"><span data-stu-id="dd4ea-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dd4ea-104">Selles teemas näidatakse, kuidas luua kirje malli, nii et välja väärtusi, mida tihti kasutatakse, ei peaks iga kirje puhul eraldi sisestama.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="dd4ea-105">Selles protseduuris loote uue kirje uutele sülearvutitele, mis tuleks põhivaradele lisada.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="dd4ea-106">See protseduur kasutab USMF-i näidisettevõtet.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="dd4ea-107">Navigeerimispaanil avage **Moodulid > Põhivarad > Põhivarad > Põhivarad**.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="dd4ea-108">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-108">Select **New**.</span></span>
3. <span data-ttu-id="dd4ea-109">Väljale **Põhivara grupp** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="dd4ea-110">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="dd4ea-111">Sisestage näiteks **Ettevõtte juhatuse sülearvuti**.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="dd4ea-112">Sisestage väärtus väljale **Otsi nime**.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="dd4ea-113">Sisestage näiteks **sülearvuti**.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="dd4ea-114">Laiendage jaotist **Tehniline teave**.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="dd4ea-115">Sisestage väärtused väljadele **Mark**, **Mudel** ja **Mudeli aasta**.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="dd4ea-116">Toimingupaanil valige **Suvandid**.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="dd4ea-117">Valige **Kirje teave**.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-117">Select **Record info**.</span></span>
10. <span data-ttu-id="dd4ea-118">Valige **Kasutaja mall**.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-118">Select **User template**.</span></span>
11. <span data-ttu-id="dd4ea-119">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="dd4ea-120">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="dd4ea-121">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-121">Select **OK**.</span></span>
14. <span data-ttu-id="dd4ea-122">Valige suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="dd4ea-122">Select **Close**.</span></span>
