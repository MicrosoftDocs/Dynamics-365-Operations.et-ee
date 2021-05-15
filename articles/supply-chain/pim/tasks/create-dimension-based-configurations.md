---
title: Dimensioonipõhiste konfiguratsioonide loomine
description: See protseduur selgitab, kuidas määratleda dimensioonipõhise toote konfiguratsiooni.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 584bb558ee0afeaffaeb003e9f1d1b0bca42d19d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920677"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="b2efc-103">Dimensioonipõhiste konfiguratsioonide loomine</span><span class="sxs-lookup"><span data-stu-id="b2efc-103">Create dimension-based configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2efc-104">See protseduur selgitab, kuidas määratleda dimensioonipõhise toote konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="b2efc-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="b2efc-105">See on viimane protseduur seerias, mis selgitab kombinatsioonide loomist dimensioonipõhise konfiguratsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="b2efc-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="b2efc-106">Selle protseduuri käivitamine sõltub andmetest, mis on loodud seitsmes eelnevas salvestises.</span><span class="sxs-lookup"><span data-stu-id="b2efc-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="b2efc-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="b2efc-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="b2efc-108">Dimensioonipõhise tooteetaloni otsimine</span><span class="sxs-lookup"><span data-stu-id="b2efc-108">Find the dimension-based product master</span></span>

1. <span data-ttu-id="b2efc-109">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="b2efc-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b2efc-110">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b2efc-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b2efc-111">Valige dimensioonipõhine tooteetalon, mille lõite 8 salvestuse esimese salvestuses.</span><span class="sxs-lookup"><span data-stu-id="b2efc-111">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="b2efc-112">Konfiguratsioonide loomine</span><span class="sxs-lookup"><span data-stu-id="b2efc-112">Create configurations</span></span>

1. <span data-ttu-id="b2efc-113">Klõpsake toimingupaanil **Tehnika** suvandile **Konfiguratsioonide haldamine**.</span><span class="sxs-lookup"><span data-stu-id="b2efc-113">On the **Engineering** Action Pane, select **Maintain configurations**.</span></span>
1. <span data-ttu-id="b2efc-114">Valige **Konfigureeri**.</span><span class="sxs-lookup"><span data-stu-id="b2efc-114">Select **Configure**.</span></span>
1. <span data-ttu-id="b2efc-115">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b2efc-115">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="b2efc-116">Sisestage või valige väärtus väljale **Kauba kood**.</span><span class="sxs-lookup"><span data-stu-id="b2efc-116">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="b2efc-117">Valige mis tahes kaup esimeses konfiguratsioonigrupis.</span><span class="sxs-lookup"><span data-stu-id="b2efc-117">Select any of the items in the first configuration group.</span></span>  
1. <span data-ttu-id="b2efc-118">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b2efc-118">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="b2efc-119">Sisestage või valige väärtus väljale **Kauba kood**.</span><span class="sxs-lookup"><span data-stu-id="b2efc-119">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="b2efc-120">Valige mis tahes kaup teisest konfiguratsioonigrupist.</span><span class="sxs-lookup"><span data-stu-id="b2efc-120">Select any item from the second configuration group.</span></span>  
1. <span data-ttu-id="b2efc-121">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2efc-121">Select **OK**.</span></span>
1. <span data-ttu-id="b2efc-122">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b2efc-122">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="b2efc-123">Sisestage väljale **Konfiguratsioon** väärtus.</span><span class="sxs-lookup"><span data-stu-id="b2efc-123">In the **Configuration** field, type a value.</span></span>
    * <span data-ttu-id="b2efc-124">Sisestage konfiguratsiooni nimi, mis lihtsustab konfiguratsiooni tuvastamist.</span><span class="sxs-lookup"><span data-stu-id="b2efc-124">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
1. <span data-ttu-id="b2efc-125">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="b2efc-125">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="b2efc-126">Sisestage konfiguratsiooni kirjeldus, mis selgitab, mida see sisaldab.</span><span class="sxs-lookup"><span data-stu-id="b2efc-126">Enter a description of the configuration to explain what it contains.</span></span>  
1. <span data-ttu-id="b2efc-127">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2efc-127">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]