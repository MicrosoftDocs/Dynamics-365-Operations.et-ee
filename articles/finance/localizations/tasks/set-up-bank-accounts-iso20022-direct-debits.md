---
title: Klientide ja kliendi pangakontode seadistamine ISO20022 otsekorralduste jaoks
description: See ülesanne annab ülevaate kliendi pangakonto ja kliendi otsekorralduse loa seadistamise kohta, mis on nõutav ISO20022 otsekorralduse kliendi maksefaili loomiseks.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85c1faebe9a61ad2e708ba26c7a5f0cad15f5f8b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988197"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="2d019-103">Klientide ja kliendi pangakontode seadistamine ISO20022 otsekorralduste jaoks</span><span class="sxs-lookup"><span data-stu-id="2d019-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2d019-104">See ülesanne annab ülevaate kliendi pangakonto ja kliendi otsekorralduse loa seadistamise kohta, mis on nõutav ISO20022 otsekorralduse kliendi maksefaili loomiseks.</span><span class="sxs-lookup"><span data-stu-id="2d019-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="2d019-105">Olenevalt seadistatud kliendi maksevormingutest võib olla kliendi või kliendi pangakonto puhul vaja lisateavet, mida see protseduur ei sisalda.</span><span class="sxs-lookup"><span data-stu-id="2d019-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="2d019-106">Ülesande loomisel kasutati demoettevõtte DEMF, mille juriidilise isiku esmaseks aadressiks on Saksamaa, andmeid.</span><span class="sxs-lookup"><span data-stu-id="2d019-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="2d019-107">See on neljas viiest protseduurist, mis näitab kliendi makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="2d019-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="2d019-108">Kliendi pangakonto seadistamine</span><span class="sxs-lookup"><span data-stu-id="2d019-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="2d019-109">Avage Müügireskontro > Kliendid > Kõik kliendid.</span><span class="sxs-lookup"><span data-stu-id="2d019-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="2d019-110">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="2d019-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2d019-111">Näiteks saate filtrida välja Konto väärtuse DE-010 järgi.</span><span class="sxs-lookup"><span data-stu-id="2d019-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="2d019-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="2d019-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2d019-113">Klõpsake toimingupaanil suvandit Klient.</span><span class="sxs-lookup"><span data-stu-id="2d019-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="2d019-114">Klõpsake valikut Pangakontod.</span><span class="sxs-lookup"><span data-stu-id="2d019-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="2d019-115">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2d019-115">Click New.</span></span>
7. <span data-ttu-id="2d019-116">Sisestage väärtus väljale Pangakonto.</span><span class="sxs-lookup"><span data-stu-id="2d019-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="2d019-117">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="2d019-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="2d019-118">Näiteks sisestage EUR-pank.</span><span class="sxs-lookup"><span data-stu-id="2d019-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="2d019-119">Sisestage väärtus väljale Pangagrupid või valige see.</span><span class="sxs-lookup"><span data-stu-id="2d019-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="2d019-120">Sisestage väärtus väljale IBAN.</span><span class="sxs-lookup"><span data-stu-id="2d019-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="2d019-121">Näiteks sisestage DE36200400000628808808.</span><span class="sxs-lookup"><span data-stu-id="2d019-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="2d019-122">Sisestage väärtus väljale SWIFT-kood.</span><span class="sxs-lookup"><span data-stu-id="2d019-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="2d019-123">Näiteks sisestage COBADEFFXXX.</span><span class="sxs-lookup"><span data-stu-id="2d019-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="2d019-124">Pange tähele, et SWIFT \ BIC pole paljude maksevormingute puhul nõutav, kuid soovitatav on see pangakonto jaoks registreerida.</span><span class="sxs-lookup"><span data-stu-id="2d019-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="2d019-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2d019-125">Click Save.</span></span>
13. <span data-ttu-id="2d019-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2d019-126">Close the page.</span></span>
14. <span data-ttu-id="2d019-127">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="2d019-127">Click Edit.</span></span>
15. <span data-ttu-id="2d019-128">Laiendage jaotist Makse vaikeandmed.</span><span class="sxs-lookup"><span data-stu-id="2d019-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="2d019-129">Sisestage väärtus väljale Pangakonto või valige see.</span><span class="sxs-lookup"><span data-stu-id="2d019-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="2d019-130">Otsekorralduse loa lisamine</span><span class="sxs-lookup"><span data-stu-id="2d019-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="2d019-131">Laiendage jaotist Otsekorralduse load.</span><span class="sxs-lookup"><span data-stu-id="2d019-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="2d019-132">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="2d019-132">Click Add.</span></span>
3. <span data-ttu-id="2d019-133">Sisestage väärtus väljale Kreeditori pangakonto või valige see.</span><span class="sxs-lookup"><span data-stu-id="2d019-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="2d019-134">Valige näiteks DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="2d019-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="2d019-135">Sisestage kuupäev väljale Allkirjastamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="2d019-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="2d019-136">Kuupäevavärskenduse kinnitamiseks klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="2d019-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="2d019-137">Sisestage väärtus väljale Allkirjastamise koht või valige see.</span><span class="sxs-lookup"><span data-stu-id="2d019-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="2d019-138">Sisestage number väljale Eeldatav maksete arv.</span><span class="sxs-lookup"><span data-stu-id="2d019-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="2d019-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2d019-139">Click OK.</span></span>
9. <span data-ttu-id="2d019-140">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2d019-140">Click Save.</span></span>

