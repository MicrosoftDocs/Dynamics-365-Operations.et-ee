---
title: Müügitellimuse loomine konfigureeritava toote jaoks
description: See protseduur näitab, kuidas rakendada müügitellimusel tootele konfiguratsioonimalli.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921285"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="3f978-103">Müügitellimuse loomine konfigureeritava toote jaoks</span><span class="sxs-lookup"><span data-stu-id="3f978-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f978-104">See protseduur näitab, kuidas rakendada müügitellimusel tootele konfiguratsioonimalli.</span><span class="sxs-lookup"><span data-stu-id="3f978-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="3f978-105">Selles näites kasutatakse demoettevõtte USMF kõlarimudelit D0006.</span><span class="sxs-lookup"><span data-stu-id="3f978-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="3f978-106">Tavaliselt kasutab seda protseduuri müügitellimuste töötleja.</span><span class="sxs-lookup"><span data-stu-id="3f978-106">Typically, a sales order processor uses this procedure.</span></span>

## <a name="create-a-sales-order"></a><span data-ttu-id="3f978-107">Loo müügitellimus</span><span class="sxs-lookup"><span data-stu-id="3f978-107">Create a sales order</span></span>

1. <span data-ttu-id="3f978-108">Minge **müügi ja turunduse \> tööruumides \> müügitellimuse töötlemisele ja päringule**.</span><span class="sxs-lookup"><span data-stu-id="3f978-108">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="3f978-109">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="3f978-109">Select **New**.</span></span>
1. <span data-ttu-id="3f978-110">Valige **Müügitellimus**.</span><span class="sxs-lookup"><span data-stu-id="3f978-110">Select **Sales order**.</span></span>
1. <span data-ttu-id="3f978-111">Valige *US-001* väljalt **Kliendi konto**.</span><span class="sxs-lookup"><span data-stu-id="3f978-111">In the **Customer account** field, select *US-001*.</span></span> 
1. <span data-ttu-id="3f978-112">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f978-112">Select **OK**.</span></span>
1. <span data-ttu-id="3f978-113">Valige väljal **Kaubakood** väärtus *D0006*.</span><span class="sxs-lookup"><span data-stu-id="3f978-113">In the **Item number** field, select *D0006*.</span></span>
    * <span data-ttu-id="3f978-114">Selle ülesande jaoks tuleb valida konfigureeritav toode.</span><span class="sxs-lookup"><span data-stu-id="3f978-114">For this task, you must select a configurable product.</span></span>  
1. <span data-ttu-id="3f978-115">Klõpsake valikut  **Toode ja tarnimine**.</span><span class="sxs-lookup"><span data-stu-id="3f978-115">Select **Product and supply**.</span></span>
1. <span data-ttu-id="3f978-116">Valige **Konfigureeri joont**.</span><span class="sxs-lookup"><span data-stu-id="3f978-116">Select **Configure line**.</span></span>
    * <span data-ttu-id="3f978-117">Pange tähele, et hind on valitud konfiguratsiooni põhjal muudetud ja välja **Lisa kaabel** väärtuseks on nüüd määratud *True*.</span><span class="sxs-lookup"><span data-stu-id="3f978-117">Note that the price has changed, based on the configuration that was selected, and that the **Include cable** field is now set to *True*.</span></span>  
    * <span data-ttu-id="3f978-118">Pange tähele kaabli jaoks valitud vaikehinda ja sätteid.</span><span class="sxs-lookup"><span data-stu-id="3f978-118">Note the default price and the settings that are selected for the cable.</span></span>  
1. <span data-ttu-id="3f978-119">Valige **Malli laadimine**.</span><span class="sxs-lookup"><span data-stu-id="3f978-119">Select **Load template**.</span></span>
    * <span data-ttu-id="3f978-120">Selles näites näete, kuidas rakendada malli eelmääratud konfiguratsiooni valimiseks.</span><span class="sxs-lookup"><span data-stu-id="3f978-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="3f978-121">Kui kasutate seda protseduuri tegevuse juhisena soovite näha teisi saadaolevaid atribuudiväärtusi, peate klõpsama nuppu **Ava**.</span><span class="sxs-lookup"><span data-stu-id="3f978-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must select the **Unlock** button.</span></span>  
1. <span data-ttu-id="3f978-122">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f978-122">Select **OK**.</span></span>
1. <span data-ttu-id="3f978-123">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f978-123">Select **OK**.</span></span>
1. <span data-ttu-id="3f978-124">Laiendage jaotist **Rea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="3f978-124">Expand the **Line details** section.</span></span>
1. <span data-ttu-id="3f978-125">Valige vahekaart **Toode**.</span><span class="sxs-lookup"><span data-stu-id="3f978-125">Select the **Product** tab.</span></span>
    * <span data-ttu-id="3f978-126">Kauba konfiguratsioon on nüüd loetletud tootedimensioonide all.</span><span class="sxs-lookup"><span data-stu-id="3f978-126">The configuration of the item is now listed under the product dimensions.</span></span>  
1. <span data-ttu-id="3f978-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3f978-127">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]