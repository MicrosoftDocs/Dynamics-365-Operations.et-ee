--- 
title: "Kliendi maksetasude määramine"
description: Looge kliendimaksete maksetasud.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 3be8db49bab80fa8765b685d73d54a42975870c3
ms.contentlocale: et-ee
ms.lasthandoff: 09/11/2018

---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="542fd-103">Kliendi maksetasude määramine</span><span class="sxs-lookup"><span data-stu-id="542fd-103">Establish customer payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="542fd-104">Looge kliendimaksete maksetasud.</span><span class="sxs-lookup"><span data-stu-id="542fd-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="542fd-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="542fd-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="542fd-106">Avage Müügireskontro > Maksete seadistus > Maksetasu.</span><span class="sxs-lookup"><span data-stu-id="542fd-106">Go to Accounts receivable > Payments setup > Payment fee.</span></span>
2. <span data-ttu-id="542fd-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="542fd-107">Click New.</span></span>
3. <span data-ttu-id="542fd-108">Sisestage tasu ID väljale Tasu ID.</span><span class="sxs-lookup"><span data-stu-id="542fd-108">In the Fee ID field, enter a Fee ID.</span></span>
    * <span data-ttu-id="542fd-109">Tasu ID kuvatakse makse töölehtedel, mistõttu muutke see kirjeldavaks, et aru saada, millist tasu hinnatakse.</span><span class="sxs-lookup"><span data-stu-id="542fd-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="542fd-110">Sisestage tasu nimi väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="542fd-110">In the Name field, enter a fee Name.</span></span>
5. <span data-ttu-id="542fd-111">Sisestage tasu kirjeldus väljale Tasu kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="542fd-111">In the Fee description field, enter a description for the fee.</span></span>
6. <span data-ttu-id="542fd-112">Valige, kas tasu määratakse kliendi või pearaamatu kontole.</span><span class="sxs-lookup"><span data-stu-id="542fd-112">Select whether the fee will be charged to the Customer or a Ledger account.</span></span>
    * <span data-ttu-id="542fd-113">Kui hinnatakse kliendi tasu, valige suvand Klient.</span><span class="sxs-lookup"><span data-stu-id="542fd-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="542fd-114">Kui tasu hinnatakse teie organisatsiooni kuluna, valige Pearaamat.</span><span class="sxs-lookup"><span data-stu-id="542fd-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="542fd-115">Selle ülesande puhul valige Klient.</span><span class="sxs-lookup"><span data-stu-id="542fd-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="542fd-116">Valige töölehe tüüp, mis saab seda maksetasu kasutada.</span><span class="sxs-lookup"><span data-stu-id="542fd-116">Select the type of  journal that can use this payment fee.</span></span>
    * <span data-ttu-id="542fd-117">Nende tasude kasutamisel kliendimakseteks on töölehe tüübiks tõenäoliselt Kliendimakse.</span><span class="sxs-lookup"><span data-stu-id="542fd-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="542fd-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="542fd-118">Click Save.</span></span>
9. <span data-ttu-id="542fd-119">Klõpsake suvandit Maksetasu seadistus.</span><span class="sxs-lookup"><span data-stu-id="542fd-119">Click Payment fee setup.</span></span>
    * <span data-ttu-id="542fd-120">Makse tasu seadistust kasutatakse kriteeriumide määratlemiseks, mil maksetasu hinnatakse.</span><span class="sxs-lookup"><span data-stu-id="542fd-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="542fd-121">Näiteks saate määrata, et tasu arvutatakse, kui pangakontoks on USMF OPER ja makseviisiks on tšekk.</span><span class="sxs-lookup"><span data-stu-id="542fd-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="542fd-122">Valige kas Tabel, Grupp või Kõik, et määratleda, millistele pangakontodele see tasu määratakse.</span><span class="sxs-lookup"><span data-stu-id="542fd-122">Select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span>
    * <span data-ttu-id="542fd-123">Kui valite suvandi Kõik, võidakse seda tasu hinnata kõigil pangakontodel.</span><span class="sxs-lookup"><span data-stu-id="542fd-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="542fd-124">Valides suvandi Tabel, võidakse seda tasu hinnata ainult teie valitud pangakontol.</span><span class="sxs-lookup"><span data-stu-id="542fd-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="542fd-125">Suvandi Grupp valimisel võidakse seda tasu hinnata ainult valitud pangagrupi pangakontodel.</span><span class="sxs-lookup"><span data-stu-id="542fd-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="542fd-126">Valige kas pangagrupp või pangakonto.</span><span class="sxs-lookup"><span data-stu-id="542fd-126">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="542fd-127">Suvandi Tabel valimisel kuvab otsing pangakontod.</span><span class="sxs-lookup"><span data-stu-id="542fd-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="542fd-128">Suvandi Grupp valimisel kuvab otsing pangagrupid.</span><span class="sxs-lookup"><span data-stu-id="542fd-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="542fd-129">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="542fd-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="542fd-130">Valige Makseviis, mis selle tasu puhul määratakse.</span><span class="sxs-lookup"><span data-stu-id="542fd-130">Select the Method of payment for which this fee will be assessed.</span></span>
    * <span data-ttu-id="542fd-131">Näiteks võite määrata tasu klientidele, kui nad saadavad makseid pigem tšekina kui elektroonilise maksena.</span><span class="sxs-lookup"><span data-stu-id="542fd-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="542fd-132">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="542fd-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="542fd-133">Vajaduse korral sisestage makse valuuta.</span><span class="sxs-lookup"><span data-stu-id="542fd-133">If relevant, enter a payment currency.</span></span>
    * <span data-ttu-id="542fd-134">Makse valuutat kasutatakse tasu määramise täiendavate kriteeriumidena.</span><span class="sxs-lookup"><span data-stu-id="542fd-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="542fd-135">Näiteks võib teie pank nõuda lisatasu USA dollarites saadud maksete eest, kuna nad teevad üldjuhul tehinguid ainult eurodes.</span><span class="sxs-lookup"><span data-stu-id="542fd-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="542fd-136">Valige, kas tasu on protsent, summa või intervall.</span><span class="sxs-lookup"><span data-stu-id="542fd-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="542fd-137">Sisestage kas tasu protsent või summa.</span><span class="sxs-lookup"><span data-stu-id="542fd-137">Enter either percentage or amount of the fee.</span></span>
    * <span data-ttu-id="542fd-138">Kui välja Protsent/summa väärtuseks on Protsent, on siin sisestatud väärtus protsent.</span><span class="sxs-lookup"><span data-stu-id="542fd-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="542fd-139">Kui välja Protsent/summa väärtuseks on Summa, on siin sisestatud väärtus summa.</span><span class="sxs-lookup"><span data-stu-id="542fd-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="542fd-140">Kui välja Protsent/summa väärtuseks on Intervall, kasutage kihtide määratlemiseks vahekaarti Intervall.</span><span class="sxs-lookup"><span data-stu-id="542fd-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="542fd-141">Valige tasu valuuta väljalt Tasu valuuta.</span><span class="sxs-lookup"><span data-stu-id="542fd-141">In the Fee currency field, select the currency of the fee.</span></span>
    * <span data-ttu-id="542fd-142">See on valuuta, milles tasu luuakse.</span><span class="sxs-lookup"><span data-stu-id="542fd-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="542fd-143">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="542fd-143">Click Save.</span></span>


