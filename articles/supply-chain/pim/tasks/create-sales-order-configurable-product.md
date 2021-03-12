---
title: Müügitellimuse loomine konfigureeritava toote jaoks
description: See protseduur näitab, kuidas rakendada müügitellimusel tootele konfiguratsioonimalli.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77404694b3426f9ef051721191b607f91c908cc4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992316"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="374f3-103">Müügitellimuse loomine konfigureeritava toote jaoks</span><span class="sxs-lookup"><span data-stu-id="374f3-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="374f3-104">See protseduur näitab, kuidas rakendada müügitellimusel tootele konfiguratsioonimalli.</span><span class="sxs-lookup"><span data-stu-id="374f3-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="374f3-105">Selles näites kasutatakse demoettevõtte USMF kõlarimudelit D0006.</span><span class="sxs-lookup"><span data-stu-id="374f3-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="374f3-106">Tavaliselt kasutab seda protseduuri müügitellimuste töötleja.</span><span class="sxs-lookup"><span data-stu-id="374f3-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="374f3-107">Loo müügitellimus</span><span class="sxs-lookup"><span data-stu-id="374f3-107">Create a sales order</span></span>
1. <span data-ttu-id="374f3-108">Klõpsake valikut Müügitellimuse töötlemine ja päring.</span><span class="sxs-lookup"><span data-stu-id="374f3-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="374f3-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="374f3-109">Click New.</span></span>
3. <span data-ttu-id="374f3-110">Klõpsake valikut Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="374f3-110">Click Sales order.</span></span>
4. <span data-ttu-id="374f3-111">Valige US-001 väljalt Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="374f3-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="374f3-112">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="374f3-112">Click OK.</span></span>
6. <span data-ttu-id="374f3-113">Tehke väljal Kaubakood valik D0006.</span><span class="sxs-lookup"><span data-stu-id="374f3-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="374f3-114">Selle ülesande jaoks tuleb valida konfigureeritav toode.</span><span class="sxs-lookup"><span data-stu-id="374f3-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="374f3-115">Klõpsake valikut Toode ja tarnimine.</span><span class="sxs-lookup"><span data-stu-id="374f3-115">Click Product and supply.</span></span>
8. <span data-ttu-id="374f3-116">Klõpsake rida Konfigureeri.</span><span class="sxs-lookup"><span data-stu-id="374f3-116">Click Configure line.</span></span>
    * <span data-ttu-id="374f3-117">Pange tähele, et hind on valitud konfiguratsiooni põhjal muudetud ja välja Lisa kaabel väärtuseks on nüüd määratud True.</span><span class="sxs-lookup"><span data-stu-id="374f3-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="374f3-118">Pange tähele kaabli jaoks valitud vaikehinda ja sätteid.</span><span class="sxs-lookup"><span data-stu-id="374f3-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="374f3-119">Klõpsake valikut Laadi mall.</span><span class="sxs-lookup"><span data-stu-id="374f3-119">Click Load template.</span></span>
    * <span data-ttu-id="374f3-120">Selles näites näete, kuidas rakendada malli eelmääratud konfiguratsiooni valimiseks.</span><span class="sxs-lookup"><span data-stu-id="374f3-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="374f3-121">Kui kasutate seda protseduuri tegevuse juhisena soovite näha teisi saadaolevaid atribuudiväärtusi, peate klõpsama nuppu Ava.</span><span class="sxs-lookup"><span data-stu-id="374f3-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="374f3-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="374f3-122">Click OK.</span></span>
11. <span data-ttu-id="374f3-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="374f3-123">Click OK.</span></span>
12. <span data-ttu-id="374f3-124">Laiendage jaotis Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="374f3-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="374f3-125">Klõpsake vahekaarti Toode.</span><span class="sxs-lookup"><span data-stu-id="374f3-125">Click the Product tab.</span></span>
    * <span data-ttu-id="374f3-126">Kauba konfiguratsioon on nüüd loetletud tootedimensioonide all.</span><span class="sxs-lookup"><span data-stu-id="374f3-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="374f3-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="374f3-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="374f3-128">Valige toote konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="374f3-128">Select the product configuration</span></span>

