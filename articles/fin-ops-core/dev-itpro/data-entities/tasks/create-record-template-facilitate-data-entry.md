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
ms.openlocfilehash: ec21415158ad611d0ad55778e76aa128f53561bd
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143380"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="b1633-103">Andmesisestuse hõlbustamiseks kirje malli loomine</span><span class="sxs-lookup"><span data-stu-id="b1633-103">Create a record template to facilitate data entry</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b1633-104">Selles teemas näidatakse, kuidas luua kirje malli, nii et välja väärtusi, mida tihti kasutatakse, ei peaks iga kirje puhul eraldi sisestama.</span><span class="sxs-lookup"><span data-stu-id="b1633-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="b1633-105">Selles protseduuris loote uue kirje uutele sülearvutitele, mis tuleks põhivaradele lisada.</span><span class="sxs-lookup"><span data-stu-id="b1633-105">In this procedure, you'll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="b1633-106">See protseduur kasutab USMF-i näidisettevõtet.</span><span class="sxs-lookup"><span data-stu-id="b1633-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="b1633-107">Navigeerimispaanil avage **Moodulid > Põhivarad > Põhivarad > Põhivarad**.</span><span class="sxs-lookup"><span data-stu-id="b1633-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="b1633-108">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b1633-108">Select **New**.</span></span>
3. <span data-ttu-id="b1633-109">Väljale **Põhivara grupp** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="b1633-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="b1633-110">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="b1633-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="b1633-111">Sisestage näiteks **Ettevõtte juhatuse sülearvuti**.</span><span class="sxs-lookup"><span data-stu-id="b1633-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="b1633-112">Sisestage väärtus väljale **Otsi nime**.</span><span class="sxs-lookup"><span data-stu-id="b1633-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="b1633-113">Sisestage näiteks **sülearvuti**.</span><span class="sxs-lookup"><span data-stu-id="b1633-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="b1633-114">Laiendage jaotist **Tehniline teave**.</span><span class="sxs-lookup"><span data-stu-id="b1633-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="b1633-115">Sisestage väärtused väljadele **Mark**, **Mudel** ja **Mudeli aasta**.</span><span class="sxs-lookup"><span data-stu-id="b1633-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="b1633-116">Toimingupaanil valige **Suvandid**.</span><span class="sxs-lookup"><span data-stu-id="b1633-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="b1633-117">Valige **Kirje teave**.</span><span class="sxs-lookup"><span data-stu-id="b1633-117">Select **Record info**.</span></span>
10. <span data-ttu-id="b1633-118">Valige **Kasutaja mall**.</span><span class="sxs-lookup"><span data-stu-id="b1633-118">Select **User template**.</span></span>
11. <span data-ttu-id="b1633-119">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="b1633-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="b1633-120">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="b1633-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="b1633-121">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1633-121">Select **OK**.</span></span>
14. <span data-ttu-id="b1633-122">Valige suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="b1633-122">Select **Close**.</span></span>

