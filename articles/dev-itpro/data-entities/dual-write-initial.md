---
title: Finance and Operationsi ning Common Data Service’i esialgse sünkroonimise täitmise järjekord
description: Selles peatükis kirjeldatakse sünkroonimise järjekorda, mida peate järgima esialgsete andmete loomisel.
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
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873124"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="6fc49-103">Finance and Operationsi ning Common Data Service’i esialgse sünkroonimise täitmise järjekord</span><span class="sxs-lookup"><span data-stu-id="6fc49-103">Execution order for initial synchronization of Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="6fc49-104">Enne andmete integratsiooni peate looma klientide, tarnijate ja kontaktide puhul kohustuslikud esialgsed andmed.</span><span class="sxs-lookup"><span data-stu-id="6fc49-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="6fc49-105">Näiteks tahate luua uut üksust **Tarnija rühm** ja määrata selle **Maksetingimused** väärtuseks **Net30**.</span><span class="sxs-lookup"><span data-stu-id="6fc49-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="6fc49-106">Sel juhul peate enne **Tarnija rühma** üksuse loomise üritust veenduma, et **Net30** on olemas nii Microsoft Dynamics 365 for Finance and Operationsis kui ka Common Data Service’is.</span><span class="sxs-lookup"><span data-stu-id="6fc49-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both Microsoft Dynamics 365 for Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="6fc49-107">(Tulevikus väljastab Microsoft topeltkirjutamise platvormi „Algne sünkroonimine“. See funktsioon sünkroniseerib Finance and Operationsi ning Common Data Service’i andmeid omavahel ühe korra topeltkirjutamise seadistuse osana.)</span><span class="sxs-lookup"><span data-stu-id="6fc49-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="6fc49-108">Microsoft väljastab topeltkirjutamise kaardi kõikidele viiteandmetele, sealhulgas **maksetingimustele** (maksetingimused).</span><span class="sxs-lookup"><span data-stu-id="6fc49-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="6fc49-109">Kui teil on juba esialgsed andmed ühes süsteemis, võib väike värskenduse toiming kirjel käivitada selle kirje topeltkirjutamise.</span><span class="sxs-lookup"><span data-stu-id="6fc49-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="6fc49-110">Peate järgima järgmist tähtsuse järjekorda ja veenduge, et esialgsed andmed oleksid saadaval nii Finance and Operationsis kui ka Common Data Service’is.</span><span class="sxs-lookup"><span data-stu-id="6fc49-110">You must follow the following order of precedence and make sure that the initial data is available in both Finance and Operations and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="6fc49-111">Tarnija</span><span class="sxs-lookup"><span data-stu-id="6fc49-111">Vendor</span></span>

<span data-ttu-id="6fc49-112">Siin on üksuse **Tarnija** käivitusjärjekord:</span><span class="sxs-lookup"><span data-stu-id="6fc49-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="6fc49-113">Tarnijagrupp</span><span class="sxs-lookup"><span data-stu-id="6fc49-113">Vendor group</span></span>

    1. <span data-ttu-id="6fc49-114">Maksetingimused</span><span class="sxs-lookup"><span data-stu-id="6fc49-114">Terms of payment</span></span>

        1. <span data-ttu-id="6fc49-115">Maksepäev ja selle read</span><span class="sxs-lookup"><span data-stu-id="6fc49-115">Payment day and lines</span></span>
        2. <span data-ttu-id="6fc49-116">Maksegraafik</span><span class="sxs-lookup"><span data-stu-id="6fc49-116">Payment schedule</span></span>

2. <span data-ttu-id="6fc49-117">Tarnija makseviis</span><span class="sxs-lookup"><span data-stu-id="6fc49-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="6fc49-118">Kliendi organisatsioon</span><span class="sxs-lookup"><span data-stu-id="6fc49-118">Customer (Organization)</span></span>

<span data-ttu-id="6fc49-119">Siin on üksuse **Klient** käivitusjärjekord:</span><span class="sxs-lookup"><span data-stu-id="6fc49-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="6fc49-120">Kliendigrupp</span><span class="sxs-lookup"><span data-stu-id="6fc49-120">Customer group</span></span>

    1. <span data-ttu-id="6fc49-121">Maksetingimused</span><span class="sxs-lookup"><span data-stu-id="6fc49-121">Terms of payment</span></span>

        1. <span data-ttu-id="6fc49-122">Maksepäev ja selle read</span><span class="sxs-lookup"><span data-stu-id="6fc49-122">Payment day and lines</span></span>
        2. <span data-ttu-id="6fc49-123">Makse</span><span class="sxs-lookup"><span data-stu-id="6fc49-123">Payment</span></span> 

2. <span data-ttu-id="6fc49-124">Kliendi makseviis</span><span class="sxs-lookup"><span data-stu-id="6fc49-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="6fc49-125">Kontaktisik</span><span class="sxs-lookup"><span data-stu-id="6fc49-125">Contact (Person)</span></span>

<span data-ttu-id="6fc49-126">Siin on üksuse **Kontakt** käivitusjärjekord:</span><span class="sxs-lookup"><span data-stu-id="6fc49-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="6fc49-127">Klient</span><span class="sxs-lookup"><span data-stu-id="6fc49-127">Customer</span></span>
2. <span data-ttu-id="6fc49-128">Tarnija</span><span class="sxs-lookup"><span data-stu-id="6fc49-128">Vendor</span></span>
