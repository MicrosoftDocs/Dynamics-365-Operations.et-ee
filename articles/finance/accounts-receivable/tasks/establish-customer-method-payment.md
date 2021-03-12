---
title: Kliendi makseviisi määramine
description: Selles teemas kirjeldatakse, kuidas luua kliendi makseviisi.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a948bf772e55f20c7010101fd11da83940a0b268
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990957"
---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="526ae-103">Kliendi makseviisi määramine</span><span class="sxs-lookup"><span data-stu-id="526ae-103">Establish customer method of payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="526ae-104">Selles teemas kirjeldatakse, kuidas luua kliendi makseviisi.</span><span class="sxs-lookup"><span data-stu-id="526ae-104">This topic explains how to create a method of payment for customer payments.</span></span> <span data-ttu-id="526ae-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="526ae-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="526ae-106">Navigeerimispaanil avage **Moodulid > Müügireskontro > Maksete seadistamine > Makseviisid**.</span><span class="sxs-lookup"><span data-stu-id="526ae-106">In the navigation pane, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="526ae-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="526ae-107">Select **New**.</span></span>
3. <span data-ttu-id="526ae-108">Väljas **Makseviis** sisestage selle ID.</span><span class="sxs-lookup"><span data-stu-id="526ae-108">In the **Method of payment** field, enter an ID for the method of payment.</span></span> <span data-ttu-id="526ae-109">Makseviisi ID kuvatakse arvetel ja maksetel, nii et muutke see piisavalt kirjeldavaks, et saada aru, millist tüüpi makse ja millise pangakonto puhul registreeritakse.</span><span class="sxs-lookup"><span data-stu-id="526ae-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="526ae-110">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="526ae-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="526ae-111">Valige, milline makse olek on maksete sisestamiseks vajalik.</span><span class="sxs-lookup"><span data-stu-id="526ae-111">Select what payment status is required in order for payments to be posted.</span></span> <span data-ttu-id="526ae-112">Kliendimakse loomisel saab seda sisestada ainult siis, kui makse olek ühtib makse olekuga, mille siin määratlete.</span><span class="sxs-lookup"><span data-stu-id="526ae-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="526ae-113">Valige, kuidas klientide makseid arvete puhul luua.</span><span class="sxs-lookup"><span data-stu-id="526ae-113">Select how customers payments should be created for invoices.</span></span> <span data-ttu-id="526ae-114">Seda suvandit kasutatakse ainult maksesoovituse käitamisel.</span><span class="sxs-lookup"><span data-stu-id="526ae-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="526ae-115">Maksesoovitust saab kasutada kliendimaksete puhul otsekorralduste tegemisel ja vahendite eraldamisel kliendi pangakontodelt.</span><span class="sxs-lookup"><span data-stu-id="526ae-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="526ae-116">Valige makse tüüp.</span><span class="sxs-lookup"><span data-stu-id="526ae-116">Select the type of payment.</span></span> <span data-ttu-id="526ae-117">Makse tüüp aitab tuvastada, kas maksel toimub kinnitamine või mitte.</span><span class="sxs-lookup"><span data-stu-id="526ae-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="526ae-118">Valige, millisele konto tüübile maksed sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="526ae-118">Select what account type payments will post to.</span></span> <span data-ttu-id="526ae-119">Tavaliselt oleks selle suvandi puhul valitud väärtus Pank.</span><span class="sxs-lookup"><span data-stu-id="526ae-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="526ae-120">Valige pangakonto, kuhu makse kirjendatakse.</span><span class="sxs-lookup"><span data-stu-id="526ae-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="526ae-121">Sisestage pangakande tüüp, et tuvastada teie panga kasutatav makse tüüp.</span><span class="sxs-lookup"><span data-stu-id="526ae-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span> <span data-ttu-id="526ae-122">Pangakande tüüpi kasutatakse panga vastavusse viimise protsessi käigus ja see võib vastavusse viimist lihtsustada.</span><span class="sxs-lookup"><span data-stu-id="526ae-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="526ae-123">Valige, kas see makse sisestatakse ajutiselt vahekontole.</span><span class="sxs-lookup"><span data-stu-id="526ae-123">Select whether this payment will temporarily post to a bridging account.</span></span> <span data-ttu-id="526ae-124">Kui soovite proovida panga tühistamiseks makse puhul ujuvaega, kasutage funktsiooni Vahekonto.</span><span class="sxs-lookup"><span data-stu-id="526ae-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="526ae-125">Makse sisestatakse ajutiselt pearaamatukontole, kuni see panga tühistab, mil makse liigub pangakontole, mille siin määratlesite.</span><span class="sxs-lookup"><span data-stu-id="526ae-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="526ae-126">Valige vahekontole sisestamiseks kasutatav põhikonto.</span><span class="sxs-lookup"><span data-stu-id="526ae-126">Enter the main account used for the bridging posting.</span></span> <span data-ttu-id="526ae-127">See on põhikonto, millele makse vahekonto kasutamisel ajutiselt sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="526ae-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="526ae-128">Elektrooniliste maksete seade määratlemiseks kasutage vahekaarti **Failivorming**</span><span class="sxs-lookup"><span data-stu-id="526ae-128">Use the **File format** tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="526ae-129">Kohustuslike väljade määratlemiseks kasutage vahekaarti **Makseviis**.</span><span class="sxs-lookup"><span data-stu-id="526ae-129">Use the **Payment control** tab to define fields that are mandatory.</span></span> <span data-ttu-id="526ae-130">Näiteks kui vajate kõikide selle makseviisiga maksete deponeerimist, saate selle suvandi sellel vahekaardil valida.</span><span class="sxs-lookup"><span data-stu-id="526ae-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="526ae-131">Kasutage vahekaarti **Makse atribuudid**, määratlemaks, milliseid makse atribuute soovite selle makseviisi puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="526ae-131">Use the **Payment attributes** tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="526ae-132">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="526ae-132">Select **Save**.</span></span>

