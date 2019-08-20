---
title: Finance and Operationsi ja teenuse Common Data Service algse sünkroonimise täitmise järjestus
description: See teema määrab sünkroonimise järjestuse, mida peate esialgsete andmete loomiseks järgima.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797294"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="00ecf-103">Finance and Operationsi ja teenuse Common Data Service algse sünkroonimise täitmise järjestus</span><span class="sxs-lookup"><span data-stu-id="00ecf-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="00ecf-104">Enne andmete integratsiooni kasutamist peate looma algsed andmed, mis on vajalikud klientide, hankijate ja kontaktide jaoks.</span><span class="sxs-lookup"><span data-stu-id="00ecf-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="00ecf-105">Näiteks kui soovite luua uue üksuse **Hankija rühm** ja sätestada selle **Maksetingimused** väärtuses **Net30**, siis enne, kui proovite luua üksuse **Hankija rühm**, peate veenduma, et **Net30** on olemas nii teenustes Finance and Operations kui ka Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="00ecf-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="00ecf-106">(Tulevikus anname välja kahesuguse kirjutamise platvormi funktsionaalsuse nimega **Algne sünkroonimine**. See teeb ühekordse andmete sünkroonimise teenustes Finance and Operationsi ja Common Data Service topeltkirjutamise seadistuse osana.)</span><span class="sxs-lookup"><span data-stu-id="00ecf-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="00ecf-107">Näpunäited: me anname välja topeltkirjutamise kaardi kõigi viiteandmete jaoks, sealhulgas **Maksetingimused** (Maksetingimused).</span><span class="sxs-lookup"><span data-stu-id="00ecf-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="00ecf-108">Kui teil on juba esialgsed andmed ühes süsteemis, võib väike värskenduse toiming kirjel käivitada selle kirje topeltkirjutamise.</span><span class="sxs-lookup"><span data-stu-id="00ecf-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="00ecf-109">Peate järgima tellimuse tehtejärjestust ja veenduma, et esialgsed andmed on saadaval nii Finance and Operationsis kui ka teenuses Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="00ecf-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="00ecf-110">Tarnija</span><span class="sxs-lookup"><span data-stu-id="00ecf-110">Vendor</span></span>

<span data-ttu-id="00ecf-111">Müüja täitmise järjekord on:</span><span class="sxs-lookup"><span data-stu-id="00ecf-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="00ecf-112">Kliendi organisatsioon</span><span class="sxs-lookup"><span data-stu-id="00ecf-112">Customer (Organization)</span></span>

<span data-ttu-id="00ecf-113">Hankija täitmise järjestus on:</span><span class="sxs-lookup"><span data-stu-id="00ecf-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="00ecf-114">Kontaktisik</span><span class="sxs-lookup"><span data-stu-id="00ecf-114">Contact (Person)</span></span>

<span data-ttu-id="00ecf-115">Kontakti täitmise järjekord on:</span><span class="sxs-lookup"><span data-stu-id="00ecf-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```
