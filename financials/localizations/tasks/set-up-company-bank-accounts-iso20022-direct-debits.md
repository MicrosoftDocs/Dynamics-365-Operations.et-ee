--- 
title: "Ettevõtte pangakontode seadistamine ISO20022 otsekorralduste jaoks"
description: "See ülesanne annab ülevaate ettevõttekohase pangakonto teabe seadistamise kohta, mis on nõutav kliendi maksefailide loomiseks."
author: mrolecki
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 836433a1a280efde5accba3391519f3c0ce08353
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="4bb75-103">Ettevõtte pangakontode seadistamine ISO20022 otsekorralduste jaoks</span><span class="sxs-lookup"><span data-stu-id="4bb75-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4bb75-104">See ülesanne annab ülevaate ettevõttekohase pangakonto teabe seadistamise kohta, mis on nõutav kliendi maksefailide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="4bb75-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="4bb75-105">Protseduur kasutab näitena ISO-20022 otsekorralduse vormingut.</span><span class="sxs-lookup"><span data-stu-id="4bb75-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="4bb75-106">Muud vormingud võivad nõuda täiendavat seadistusteavet nagu Ettevõtte ID või Sortimiskood.</span><span class="sxs-lookup"><span data-stu-id="4bb75-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="4bb75-107">Selle ülesande loomisel kasutati demoettevõtte DEMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="4bb75-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="4bb75-108">See on teine viiest protseduurist, mis näitab kliendi makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="4bb75-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="4bb75-109">IBAN- ja SWIFT-koodide seadistamine</span><span class="sxs-lookup"><span data-stu-id="4bb75-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="4bb75-110">Avage Sularaha- ja pangahaldus > Pangakontod.</span><span class="sxs-lookup"><span data-stu-id="4bb75-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="4bb75-111">Kasutage kiirfiltrit, et filtrida välja Pangakonto väärtusega DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="4bb75-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="4bb75-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="4bb75-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4bb75-113">Näiteks klõpsake pangakonto üksikasjade avamiseks valikut DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="4bb75-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="4bb75-114">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="4bb75-114">Click Edit.</span></span>
5. <span data-ttu-id="4bb75-115">Laiendage või ahendage jaotist Täiendav identifitseerimine.</span><span class="sxs-lookup"><span data-stu-id="4bb75-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="4bb75-116">Sisestage väärtus väljale IBAN.</span><span class="sxs-lookup"><span data-stu-id="4bb75-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="4bb75-117">Näiteks sisestage DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="4bb75-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="4bb75-118">Sisestage väärtus väljale SWIFT-kood.</span><span class="sxs-lookup"><span data-stu-id="4bb75-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="4bb75-119">Näiteks sisestage DEUTDEFF.</span><span class="sxs-lookup"><span data-stu-id="4bb75-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="4bb75-120">Pange tähele, et SWIFT \ BIC pole paljude maksevormingute puhul nõutav, kuid soovitatav on see pangakonto jaoks registreerida.</span><span class="sxs-lookup"><span data-stu-id="4bb75-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="4bb75-121">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="4bb75-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="4bb75-122">Juriidilise isiku pangakonto seadistamine</span><span class="sxs-lookup"><span data-stu-id="4bb75-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="4bb75-123">Avage Organisatsiooni haldus > Organisatsioonid > Juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="4bb75-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="4bb75-124">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="4bb75-124">Click Edit.</span></span>
3. <span data-ttu-id="4bb75-125">Laiendage või ahendage jaotist Pangakonto teave.</span><span class="sxs-lookup"><span data-stu-id="4bb75-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="4bb75-126">Klõpsake väljal Pangakonto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="4bb75-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="4bb75-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="4bb75-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4bb75-128">Näiteks valige pangakonto DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="4bb75-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="4bb75-129">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="4bb75-129">Click Save.</span></span>


