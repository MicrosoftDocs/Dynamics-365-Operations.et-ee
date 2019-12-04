---
title: EUR-00015 Osapoole otsing KM ID abil
description: See protseduur näitab, kuidas teha osapoole otsingut, kasutades registreerimise ID-d.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, DirPartTaxRegistrationSearch
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0427b6e961173543f860ef6e098fc6248afd3aa
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183595"
---
# <a name="eur-00015-party-search-using-vat-id"></a><span data-ttu-id="422e3-103">EUR-00015 Osapoole otsing KM ID abil</span><span class="sxs-lookup"><span data-stu-id="422e3-103">EUR-00015 Party search using VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="422e3-104">See protseduur näitab, kuidas teha osapoole otsingut, kasutades registreerimise ID-d.</span><span class="sxs-lookup"><span data-stu-id="422e3-104">This procedure shows how to complete a party search using a registration ID.</span></span> <span data-ttu-id="422e3-105">Enne seda protseduuri tuleb seadistada KM ID-d ja sisestada hankijate, klientide või juriidiliste isikute KM ID-d.</span><span class="sxs-lookup"><span data-stu-id="422e3-105">Before you can complete this procedure, you must set up VAT IDs and enter any VAT IDs for vendors, customers, or legal entities.</span></span>

<span data-ttu-id="422e3-106">See protseduur kohaldub kõigile Euroopa riikidele/piirkondadele.</span><span class="sxs-lookup"><span data-stu-id="422e3-106">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="422e3-107">Protseduuri loomisel kasutati demoettevõtte DEMF, mille esmaseks aadressiks on Saksamaa, andmeid.</span><span class="sxs-lookup"><span data-stu-id="422e3-107">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="422e3-108">See protseduur on mõeldud ostureskontro juhile või müügireskontro juhile.</span><span class="sxs-lookup"><span data-stu-id="422e3-108">This procedure is intended for an accounts payable manager or accounts receivable manager.</span></span> <span data-ttu-id="422e3-109">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="422e3-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="422e3-110">Avage Organisatsioonihaldus > Globaalne aadressiraamat > Globaalne aadressiraamat.</span><span class="sxs-lookup"><span data-stu-id="422e3-110">Go to Organization administration > Global address book > Global address book.</span></span>
2. <span data-ttu-id="422e3-111">Klõpsake valikut Registreerimise ID otsing.</span><span class="sxs-lookup"><span data-stu-id="422e3-111">Click Registration ID search.</span></span>
3. <span data-ttu-id="422e3-112">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="422e3-112">Click Add.</span></span>
4. <span data-ttu-id="422e3-113">Sisestage või valige väärtus väljal Registreerimise tüüp.</span><span class="sxs-lookup"><span data-stu-id="422e3-113">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="422e3-114">Näiteks kui soovite leida osapooli, kelle registreerimise ID tüüp on KM ID, valige KM ID.</span><span class="sxs-lookup"><span data-stu-id="422e3-114">For example, if you wanted to find parties with a registration ID of type VAT ID, select VAT ID.</span></span>  
5. <span data-ttu-id="422e3-115">Sisestage või valige väärtus väljal Riik/piirkond.</span><span class="sxs-lookup"><span data-stu-id="422e3-115">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="422e3-116">Sisestage näiteks DEU.</span><span class="sxs-lookup"><span data-stu-id="422e3-116">For example, enter DEU.</span></span>  
6. <span data-ttu-id="422e3-117">Tippige väärtus väljale Registreerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="422e3-117">In the Registration number field, type a value.</span></span>
7. <span data-ttu-id="422e3-118">Klõpsake käsku Otsi.</span><span class="sxs-lookup"><span data-stu-id="422e3-118">Click Find.</span></span>
    * <span data-ttu-id="422e3-119">Kuvatakse kõik selle registreerimise ID-ga osapooled.</span><span class="sxs-lookup"><span data-stu-id="422e3-119">All parties with that registration ID will be displayed.</span></span>  
