---
title: Finance and Operationsi rakenduste ning Common Data Service’i esialgse sünkroonimise täitmise järjekord
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
ms.openlocfilehash: 3110cb809558d168e9d97f640701b249caf73f6c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184504"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="24d81-103">Finance and Operationsi rakenduste ning Common Data Service’i esialgse sünkroonimise täitmise järjekord</span><span class="sxs-lookup"><span data-stu-id="24d81-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="24d81-104">Enne andmete integratsiooni peate looma klientide, tarnijate ja kontaktide puhul kohustuslikud esialgsed andmed.</span><span class="sxs-lookup"><span data-stu-id="24d81-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="24d81-105">Näiteks tahate luua uut üksust **Tarnija rühm** ja määrata selle **Maksetingimused** väärtuseks **Net30**.</span><span class="sxs-lookup"><span data-stu-id="24d81-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="24d81-106">Sel juhul peate enne **Tarnija rühma** üksuse loomise üritust veenduma, et **Net30** on olemas nii rakenduses kui ka Common Data Service’is.</span><span class="sxs-lookup"><span data-stu-id="24d81-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="24d81-107">(Tulevikus väljastab Microsoft topeltkirjutamise platvormi „Algne sünkroonimine“. See funktsioon sünkroniseerib rakenduse ning Common Data Service’i andmeid omavahel ühe korra topeltkirjutamise seadistuse osana.)</span><span class="sxs-lookup"><span data-stu-id="24d81-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="24d81-108">Microsoft väljastab topeltkirjutamise kaardi kõikidele viiteandmetele, sealhulgas **maksetingimustele** (maksetingimused).</span><span class="sxs-lookup"><span data-stu-id="24d81-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="24d81-109">Kui teil on juba esialgsed andmed ühes süsteemis, võib väike värskenduse toiming kirjel käivitada selle kirje topeltkirjutamise.</span><span class="sxs-lookup"><span data-stu-id="24d81-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="24d81-110">Peate järgima järgmist tähtsuse järjekorda ja veenduge, et esialgsed andmed oleksid saadaval nii rakenduses kui ka Common Data Service’is.</span><span class="sxs-lookup"><span data-stu-id="24d81-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="24d81-111">Tarnija</span><span class="sxs-lookup"><span data-stu-id="24d81-111">Vendor</span></span>

<span data-ttu-id="24d81-112">Siin on üksuse **Tarnija** käivitusjärjekord:</span><span class="sxs-lookup"><span data-stu-id="24d81-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="24d81-113">Tarnijagrupp</span><span class="sxs-lookup"><span data-stu-id="24d81-113">Vendor group</span></span>

    1. <span data-ttu-id="24d81-114">Maksetingimused</span><span class="sxs-lookup"><span data-stu-id="24d81-114">Terms of payment</span></span>

        1. <span data-ttu-id="24d81-115">Maksepäev ja selle read</span><span class="sxs-lookup"><span data-stu-id="24d81-115">Payment day and lines</span></span>
        2. <span data-ttu-id="24d81-116">Maksegraafik</span><span class="sxs-lookup"><span data-stu-id="24d81-116">Payment schedule</span></span>

2. <span data-ttu-id="24d81-117">Tarnija makseviis</span><span class="sxs-lookup"><span data-stu-id="24d81-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="24d81-118">Kliendi organisatsioon</span><span class="sxs-lookup"><span data-stu-id="24d81-118">Customer (Organization)</span></span>

<span data-ttu-id="24d81-119">Siin on üksuse **Klient** käivitusjärjekord:</span><span class="sxs-lookup"><span data-stu-id="24d81-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="24d81-120">Kliendigrupp</span><span class="sxs-lookup"><span data-stu-id="24d81-120">Customer group</span></span>

    1. <span data-ttu-id="24d81-121">Maksetingimused</span><span class="sxs-lookup"><span data-stu-id="24d81-121">Terms of payment</span></span>

        1. <span data-ttu-id="24d81-122">Maksepäev ja selle read</span><span class="sxs-lookup"><span data-stu-id="24d81-122">Payment day and lines</span></span>
        2. <span data-ttu-id="24d81-123">Makse</span><span class="sxs-lookup"><span data-stu-id="24d81-123">Payment</span></span> 

2. <span data-ttu-id="24d81-124">Kliendi makseviis</span><span class="sxs-lookup"><span data-stu-id="24d81-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="24d81-125">Kontaktisik</span><span class="sxs-lookup"><span data-stu-id="24d81-125">Contact (Person)</span></span>

<span data-ttu-id="24d81-126">Siin on üksuse **Kontakt** käivitusjärjekord:</span><span class="sxs-lookup"><span data-stu-id="24d81-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="24d81-127">Klient</span><span class="sxs-lookup"><span data-stu-id="24d81-127">Customer</span></span>
2. <span data-ttu-id="24d81-128">Tarnija</span><span class="sxs-lookup"><span data-stu-id="24d81-128">Vendor</span></span>
