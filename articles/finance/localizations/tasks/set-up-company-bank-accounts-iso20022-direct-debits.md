---
title: Ettevõtte pangakontode seadistamine ISO20022 otsekorralduste jaoks
description: See ülesanne annab ülevaate ettevõttekohase pangakonto teabe seadistamise kohta, mis on nõutav kliendi maksefailide loomiseks.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 319bf71982987296a8270f596f8d2bb518dd1790
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819452"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="57ac3-103">Ettevõtte pangakontode seadistamine ISO20022 otsekorralduste jaoks</span><span class="sxs-lookup"><span data-stu-id="57ac3-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57ac3-104">See ülesanne annab ülevaate ettevõttekohase pangakonto teabe seadistamise kohta, mis on nõutav kliendi maksefailide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="57ac3-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="57ac3-105">Protseduur kasutab näitena ISO-20022 otsekorralduse vormingut.</span><span class="sxs-lookup"><span data-stu-id="57ac3-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="57ac3-106">Muud vormingud võivad nõuda täiendavat seadistusteavet nagu Ettevõtte ID või Sortimiskood.</span><span class="sxs-lookup"><span data-stu-id="57ac3-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="57ac3-107">Selle ülesande loomisel kasutati demoettevõtte DEMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="57ac3-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="57ac3-108">See on teine viiest protseduurist, mis näitab kliendi makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="57ac3-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="57ac3-109">IBAN- ja SWIFT-koodide seadistamine</span><span class="sxs-lookup"><span data-stu-id="57ac3-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="57ac3-110">Avage Sularaha- ja pangahaldus > Pangakontod.</span><span class="sxs-lookup"><span data-stu-id="57ac3-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="57ac3-111">Kasutage kiirfiltrit, et filtrida välja Pangakonto väärtusega DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="57ac3-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="57ac3-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="57ac3-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="57ac3-113">Näiteks klõpsake pangakonto üksikasjade avamiseks valikut DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="57ac3-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="57ac3-114">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="57ac3-114">Click Edit.</span></span>
5. <span data-ttu-id="57ac3-115">Laiendage või ahendage jaotist Täiendav identifitseerimine.</span><span class="sxs-lookup"><span data-stu-id="57ac3-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="57ac3-116">Sisestage väärtus väljale IBAN.</span><span class="sxs-lookup"><span data-stu-id="57ac3-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="57ac3-117">Näiteks sisestage DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="57ac3-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="57ac3-118">Sisestage väärtus väljale SWIFT-kood.</span><span class="sxs-lookup"><span data-stu-id="57ac3-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="57ac3-119">Näiteks sisestage DEUTDEFF.</span><span class="sxs-lookup"><span data-stu-id="57ac3-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="57ac3-120">Pange tähele, et SWIFT \ BIC pole paljude maksevormingute puhul nõutav, kuid soovitatav on see pangakonto jaoks registreerida.</span><span class="sxs-lookup"><span data-stu-id="57ac3-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="57ac3-121">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="57ac3-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="57ac3-122">Juriidilise isiku pangakonto seadistamine</span><span class="sxs-lookup"><span data-stu-id="57ac3-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="57ac3-123">Avage Organisatsiooni haldus > Organisatsioonid > Juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="57ac3-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="57ac3-124">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="57ac3-124">Click Edit.</span></span>
3. <span data-ttu-id="57ac3-125">Laiendage või ahendage jaotist Pangakonto teave.</span><span class="sxs-lookup"><span data-stu-id="57ac3-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="57ac3-126">Klõpsake väljal Pangakonto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="57ac3-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="57ac3-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="57ac3-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="57ac3-128">Näiteks valige pangakonto DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="57ac3-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="57ac3-129">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="57ac3-129">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]