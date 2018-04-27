---
title: "Rakenduse Finance and Operations toodete sünkroonimine rakenduse Field Service toodetega"
description: "See teema käsitleb malle ja aluseks olevat ülesannet, mida kasutatakse toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 699830ce6cd993f3dd3fd4ff744ce5a8b9645c32
ms.contentlocale: et-ee
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="a36c9-103">Rakenduse Finance and Operations toodete sünkroonimine rakenduse Field Service toodetega</span><span class="sxs-lookup"><span data-stu-id="a36c9-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a36c9-104">See teema käsitleb malle ja aluseks olevat ülesannet, mida kasutatakse toodete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="a36c9-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="a36c9-105">Kasutatud mall **Field Service’i tooted (Fin and Opsist Field Service’isse)** põhineb lahenduse Potentsiaalne klient sularahaks mallil **Tooted (Fin and Opsist Salesi) – otse**.</span><span class="sxs-lookup"><span data-stu-id="a36c9-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="a36c9-106">Lisateabe saamiseks vt [Tooted (Fin and Opsist Salesi) – otse](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="a36c9-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="a36c9-107">Selles teemas kirjeldatakse ainult mallide **Field Service’i tooted (Fin and Opsist Field Service’isse)** ja **Tooted (Fin and Opsist Salesi) – otse** erinevusi.</span><span class="sxs-lookup"><span data-stu-id="a36c9-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a36c9-108">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="a36c9-108">Templates and tasks</span></span>

<span data-ttu-id="a36c9-109">**Malli nimi andmete integratsioonis:**</span><span class="sxs-lookup"><span data-stu-id="a36c9-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="a36c9-110">Field Service’i tooted (Fin and Opsist Field Service’isse)</span><span class="sxs-lookup"><span data-stu-id="a36c9-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="a36c9-111">**Ülesande nimi andmete integratsiooni projektis:**</span><span class="sxs-lookup"><span data-stu-id="a36c9-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="a36c9-112">Tooted – tooted</span><span class="sxs-lookup"><span data-stu-id="a36c9-112">Products - Products</span></span>

<span data-ttu-id="a36c9-113">Mall **Field Service’i tooted (Fin and Opsist Field Service’isse)** sisaldab üht vastendust, mida pole mallil **Tooted (Fin and Opsist Salesi) – otse**.</span><span class="sxs-lookup"><span data-stu-id="a36c9-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="a36c9-114">See vastendus tagab, et kohustuslik spetsiifiline Field Service’i väli **Service’i toote tüüp** on õigesti seadistatud.</span><span class="sxs-lookup"><span data-stu-id="a36c9-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="a36c9-115">Kasutatakse järgmist vastendamist.</span><span class="sxs-lookup"><span data-stu-id="a36c9-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="a36c9-116">Välja **Field Service’i toote tüüp** väärtus andmeüksusel **Müüdavad väljastatud tooted** rakenduses Finance and Operations arvutatakse järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a36c9-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="a36c9-117">**Varud:** Toote tüüp = Toote ja kauba mudeligrupp, Ladustatav toode = Tõene</span><span class="sxs-lookup"><span data-stu-id="a36c9-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="a36c9-118">**Mittevarud:** Toote tüüp = Toote ja kauba mudeligrupp, Ladustatav toode = Väär</span><span class="sxs-lookup"><span data-stu-id="a36c9-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="a36c9-119">**Teenus:** Toote tüüp = Teenus</span><span class="sxs-lookup"><span data-stu-id="a36c9-119">**Service:** Product type = Service</span></span>

