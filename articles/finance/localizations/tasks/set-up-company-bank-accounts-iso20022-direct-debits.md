---
title: Ettevõtte pangakontode seadistamine ISO20022 otsekorralduste jaoks
description: See ülesanne annab ülevaate ettevõttekohase pangakonto teabe seadistamise kohta, mis on nõutav kliendi maksefailide loomiseks.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 652d8aa8f78d9a12ee390d23904f2c94d9bcf684
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442287"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="c465f-103">Ettevõtte pangakontode seadistamine ISO20022 otsekorralduste jaoks</span><span class="sxs-lookup"><span data-stu-id="c465f-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c465f-104">See ülesanne annab ülevaate ettevõttekohase pangakonto teabe seadistamise kohta, mis on nõutav kliendi maksefailide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="c465f-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="c465f-105">Protseduur kasutab näitena ISO-20022 otsekorralduse vormingut.</span><span class="sxs-lookup"><span data-stu-id="c465f-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="c465f-106">Muud vormingud võivad nõuda täiendavat seadistusteavet nagu Ettevõtte ID või Sortimiskood.</span><span class="sxs-lookup"><span data-stu-id="c465f-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="c465f-107">Selle ülesande loomisel kasutati demoettevõtte DEMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="c465f-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="c465f-108">See on teine viiest protseduurist, mis näitab kliendi makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="c465f-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="c465f-109">IBAN- ja SWIFT-koodide seadistamine</span><span class="sxs-lookup"><span data-stu-id="c465f-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="c465f-110">Avage Sularaha- ja pangahaldus > Pangakontod.</span><span class="sxs-lookup"><span data-stu-id="c465f-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="c465f-111">Kasutage kiirfiltrit, et filtrida välja Pangakonto väärtusega DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="c465f-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="c465f-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c465f-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c465f-113">Näiteks klõpsake pangakonto üksikasjade avamiseks valikut DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="c465f-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="c465f-114">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="c465f-114">Click Edit.</span></span>
5. <span data-ttu-id="c465f-115">Laiendage või ahendage jaotist Täiendav identifitseerimine.</span><span class="sxs-lookup"><span data-stu-id="c465f-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="c465f-116">Sisestage väärtus väljale IBAN.</span><span class="sxs-lookup"><span data-stu-id="c465f-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="c465f-117">Näiteks sisestage DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="c465f-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="c465f-118">Sisestage väärtus väljale SWIFT-kood.</span><span class="sxs-lookup"><span data-stu-id="c465f-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="c465f-119">Näiteks sisestage DEUTDEFF.</span><span class="sxs-lookup"><span data-stu-id="c465f-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="c465f-120">Pange tähele, et SWIFT \ BIC pole paljude maksevormingute puhul nõutav, kuid soovitatav on see pangakonto jaoks registreerida.</span><span class="sxs-lookup"><span data-stu-id="c465f-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="c465f-121">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="c465f-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="c465f-122">Juriidilise isiku pangakonto seadistamine</span><span class="sxs-lookup"><span data-stu-id="c465f-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="c465f-123">Avage Organisatsiooni haldus > Organisatsioonid > Juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="c465f-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="c465f-124">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="c465f-124">Click Edit.</span></span>
3. <span data-ttu-id="c465f-125">Laiendage või ahendage jaotist Pangakonto teave.</span><span class="sxs-lookup"><span data-stu-id="c465f-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="c465f-126">Klõpsake väljal Pangakonto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c465f-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c465f-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c465f-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c465f-128">Näiteks valige pangakonto DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="c465f-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="c465f-129">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="c465f-129">Click Save.</span></span>

