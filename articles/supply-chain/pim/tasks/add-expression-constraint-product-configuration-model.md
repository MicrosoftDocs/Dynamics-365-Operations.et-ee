---
title: Avaldise piirangu lisamine toote konfiguratsioonimudelile
description: See protseduur näitab, kuidas saate lisada toote konfiguratsioonimudelile uue piiranguavaldise.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920877"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="38bcf-103">Avaldise piirangu lisamine toote konfiguratsioonimudelile</span><span class="sxs-lookup"><span data-stu-id="38bcf-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38bcf-104">See protseduur näitab, kuidas saate lisada toote konfiguratsioonimudelile uue piiranguavaldise.</span><span class="sxs-lookup"><span data-stu-id="38bcf-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="38bcf-105">See näitab, kuidas saate lasta lisada kõlarile nurgakaitsme, kui kasutaja on valinud metallist esivõre.</span><span class="sxs-lookup"><span data-stu-id="38bcf-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="38bcf-106">See protseduur kasutab komponenti Tipptasemel kõlar demoettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="38bcf-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>

## <a name="create-an-expression-constraint"></a><span data-ttu-id="38bcf-107">Avaldise piirangu loomine</span><span class="sxs-lookup"><span data-stu-id="38bcf-107">Create an expression constraint</span></span>

1. <span data-ttu-id="38bcf-108">Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.</span><span class="sxs-lookup"><span data-stu-id="38bcf-108">Go to **Product information management \> Products \> Product configuration models**.</span></span>
3. <span data-ttu-id="38bcf-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="38bcf-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="38bcf-110">Selles näites kasutatakse tipptasemel kõlari mudelit.</span><span class="sxs-lookup"><span data-stu-id="38bcf-110">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="38bcf-111">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="38bcf-111">In the list, select the link in the selected row.</span></span>
5. <span data-ttu-id="38bcf-112">Laiendage jaotist **Piirangud**.</span><span class="sxs-lookup"><span data-stu-id="38bcf-112">Expand the **Constraints** section.</span></span>
6. <span data-ttu-id="38bcf-113">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="38bcf-113">Select **Add**.</span></span>
7. <span data-ttu-id="38bcf-114">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="38bcf-114">Select **Create**.</span></span>
8. <span data-ttu-id="38bcf-115">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="38bcf-115">In the **Name** field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="38bcf-116">Sisesta avaldis</span><span class="sxs-lookup"><span data-stu-id="38bcf-116">Enter expression</span></span>

1. <span data-ttu-id="38bcf-117">Valige **Redigeeri avaldis**.</span><span class="sxs-lookup"><span data-stu-id="38bcf-117">Select **Edit expression**.</span></span>
    * <span data-ttu-id="38bcf-118">Kui avate selles etapis ülesande salvestises kasutajaliidese, saate kasutada piiranguavaldise koostamiseks IntelliSense’i ja sümbolite loendit.</span><span class="sxs-lookup"><span data-stu-id="38bcf-118">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="38bcf-119">Sisestage väljale **ConstraintBody** tekst Implies[FrontGrill=="Metal", CornerProtection].</span><span class="sxs-lookup"><span data-stu-id="38bcf-119">In the **ConstraintBody** field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="38bcf-120">See avaldise loogika väidab: kui esivõre on metallist, tuleb valida nurkade kaitse suvand.</span><span class="sxs-lookup"><span data-stu-id="38bcf-120">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="38bcf-121">Valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="38bcf-121">Select **Validate**.</span></span>
    * <span data-ttu-id="38bcf-122">Kontrollimisfunktsioon vaatab piiranguavaldise läbi ja kontrollib süntaksivigu.</span><span class="sxs-lookup"><span data-stu-id="38bcf-122">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="38bcf-123">Valige suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="38bcf-123">Select **Close**.</span></span>
5. <span data-ttu-id="38bcf-124">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="38bcf-124">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]