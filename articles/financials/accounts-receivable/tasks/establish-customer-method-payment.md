--- 
title: "Kliendi makseviisi määramine"
description: Looge kliendimaksete makseviis.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cabcfe83ac83a8210ce4e0d46a08acdc48f4bf3b
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="establish-customer-method-of-payment"></a><span data-ttu-id="8182e-103">Kliendi makseviisi määramine</span><span class="sxs-lookup"><span data-stu-id="8182e-103">Establish customer method of payment</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8182e-104">Looge kliendimaksete makseviis.</span><span class="sxs-lookup"><span data-stu-id="8182e-104">Create a method of payment for customer payments.</span></span> <span data-ttu-id="8182e-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="8182e-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="8182e-106">Avage Müügireskontro > Maksete seadistus > Makseviisid.</span><span class="sxs-lookup"><span data-stu-id="8182e-106">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="8182e-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="8182e-107">Click New.</span></span>
3. <span data-ttu-id="8182e-108">Sisestage makseviisi ID väljale Makseviis.</span><span class="sxs-lookup"><span data-stu-id="8182e-108">In the Method of payment field, enter an ID for the method of payment.</span></span>
    * <span data-ttu-id="8182e-109">Makseviisi ID kuvatakse arvetel ja maksetel, nii et muutke see piisavalt kirjeldavaks, et saada aru, millist tüüpi makse ja millise pangakonto puhul registreeritakse.</span><span class="sxs-lookup"><span data-stu-id="8182e-109">The Method of payment ID is shown on invoices and payments, so make it descriptive enough to understand what type of payment is being recorded, and for what bank account.</span></span>  
4. <span data-ttu-id="8182e-110">Sisestage kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="8182e-110">In the Description field, enter a description.</span></span>
5. <span data-ttu-id="8182e-111">Valige, milline makse olek on maksete sisestamiseks vajalik.</span><span class="sxs-lookup"><span data-stu-id="8182e-111">Select what payment status is required in order for payments to be posted.</span></span>
    * <span data-ttu-id="8182e-112">Kliendimakse loomisel saab seda sisestada ainult siis, kui makse olek ühtib makse olekuga, mille siin määratlete.</span><span class="sxs-lookup"><span data-stu-id="8182e-112">When creating a customer payment, it can only be posted when the payment status matches the payment status you define here.</span></span>  
6. <span data-ttu-id="8182e-113">Valige, kuidas klientide makseid arvete puhul luua.</span><span class="sxs-lookup"><span data-stu-id="8182e-113">Select how customers payments should be created for invoices.</span></span>
    * <span data-ttu-id="8182e-114">Seda suvandit kasutatakse ainult maksesoovituse käitamisel.</span><span class="sxs-lookup"><span data-stu-id="8182e-114">This option is only used when running a payment proposal.</span></span> <span data-ttu-id="8182e-115">Maksesoovitust saab kasutada kliendimaksete puhul otsekorralduste tegemisel ja vahendite eraldamisel kliendi pangakontodelt.</span><span class="sxs-lookup"><span data-stu-id="8182e-115">A payment proposal could be used for customer payments when doing direct debits, and pulling the funds from the customers' bank accounts.</span></span>  
7. <span data-ttu-id="8182e-116">Valige makse tüüp.</span><span class="sxs-lookup"><span data-stu-id="8182e-116">Select the type of payment.</span></span>
    * <span data-ttu-id="8182e-117">Makse tüüp aitab tuvastada, kas maksel toimub kinnitamine või mitte.</span><span class="sxs-lookup"><span data-stu-id="8182e-117">The payment type will help determine whether some validation will occur or not on the payment.</span></span>  
8. <span data-ttu-id="8182e-118">Valige, millisele konto tüübile maksed sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="8182e-118">Select what account type payments will post to.</span></span>
    * <span data-ttu-id="8182e-119">Tavaliselt oleks selle suvandi puhul valitud väärtus Pank.</span><span class="sxs-lookup"><span data-stu-id="8182e-119">Typically, Bank would be selected for this option.</span></span>  
9. <span data-ttu-id="8182e-120">Valige pangakonto, kuhu makse kirjendatakse.</span><span class="sxs-lookup"><span data-stu-id="8182e-120">Select the bank account into which this payment will be recorded.</span></span>
10. <span data-ttu-id="8182e-121">Sisestage pangakande tüüp, et tuvastada teie panga kasutatav makse tüüp.</span><span class="sxs-lookup"><span data-stu-id="8182e-121">Enter the Bank transaction type to identify the type of payment used by your bank.</span></span>
    * <span data-ttu-id="8182e-122">Pangakande tüüpi kasutatakse panga vastavusse viimise protsessi käigus ja see võib vastavusse viimist lihtsustada.</span><span class="sxs-lookup"><span data-stu-id="8182e-122">The bank transaction type is used during the bank reconciliation process, and can make reconciliation easier.</span></span>  
11. <span data-ttu-id="8182e-123">Valige, kas see makse sisestatakse ajutiselt vahekontole.</span><span class="sxs-lookup"><span data-stu-id="8182e-123">Select whether this payment will temporarily post to a bridging account.</span></span>
    * <span data-ttu-id="8182e-124">Kui soovite proovida panga tühistamiseks makse puhul ujuvaega, kasutage funktsiooni Vahekonto.</span><span class="sxs-lookup"><span data-stu-id="8182e-124">If you want to try the float time for a payment to clear the bank, use the Bridging functionality.</span></span> <span data-ttu-id="8182e-125">Makse sisestatakse ajutiselt pearaamatukontole, kuni see panga tühistab, mil makse liigub pangakontole, mille siin määratlesite.</span><span class="sxs-lookup"><span data-stu-id="8182e-125">The payment will temporarily post to a Ledger account until it clears the bank, at which time the payment will move to the bank account you defined here.</span></span>  
12. <span data-ttu-id="8182e-126">Valige vahekontole sisestamiseks kasutatav põhikonto.</span><span class="sxs-lookup"><span data-stu-id="8182e-126">Enter the main account used for the bridging posting.</span></span>
    * <span data-ttu-id="8182e-127">See on põhikonto, millele makse vahekonto kasutamisel ajutiselt sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="8182e-127">This is the main account to which the payment will temporarily post if using bridging.</span></span>  
13. <span data-ttu-id="8182e-128">Vahekaardi Failivorming abil saate määratleda sätte elektrooniliste maksete puhul.</span><span class="sxs-lookup"><span data-stu-id="8182e-128">Use the File format tab to define setting for electronic payments.</span></span>
14. <span data-ttu-id="8182e-129">Kasutage kohustuslike väljade määratlemiseks vahekaarti Makse kontroll.</span><span class="sxs-lookup"><span data-stu-id="8182e-129">Use the Payment control tab to define fields that are mandatory.</span></span>
    * <span data-ttu-id="8182e-130">Näiteks kui vajate kõikide selle makseviisiga maksete deponeerimist, saate selle suvandi sellel vahekaardil valida.</span><span class="sxs-lookup"><span data-stu-id="8182e-130">For example, if you require all payments with this method of payment to be deposited, you can choose that option on this tab.</span></span>  
15. <span data-ttu-id="8182e-131">Kasutage vahekaarti Makse atribuudid, määratlemaks, milliseid makse atribuute soovite selle makseviisi puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="8182e-131">Use the Payment atrributes tab to define which payment attributes you want to use for this method of payment.</span></span>
16. <span data-ttu-id="8182e-132">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="8182e-132">Click Save.</span></span>


